---
title: Lutter contre le courrier indésirable envoyé à Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5fd7d05b-96db-456f-81d6-1ac0e5bff530
ms.collection:
- M365-security-compliance
description: La feuille de route sécurité de messagerie de Microsoft implique une approche inter-produits sans correspondance. La technologie de filtrage anti-spam et anti-hameçonnage d'Exchange Online Protection (EOP) est appliquée sur les plateformes de messagerie de Microsoft pour fournir aux utilisateurs les innovations et les outils anti-spam et anti-hameçonnage les plus récents dans tout le réseau. L'objectif d'EOP est de proposer un service de messagerie complet et utilisable qui vous aide à détecter le courrier indésirable, les menaces d'e-mails frauduleux (hameçonnage) et les logiciels malveillants, et de protéger les utilisateurs.
ms.openlocfilehash: 510b04d3f111c269d5f8579abcc809ddc283636b
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30692853"
---
# <a name="fighting-junk-email-sent-to-office-365"></a>Lutter contre le courrier indésirable envoyé à Office 365

La feuille de route sécurité de messagerie de Microsoft implique une approche inter-produits sans correspondance. La technologie de filtrage anti-spam et anti-hameçonnage d'Exchange Online Protection (EOP) est appliquée sur les plateformes de messagerie de Microsoft pour fournir aux utilisateurs les innovations et les outils anti-spam et anti-hameçonnage les plus récents dans tout le réseau. L'objectif d'EOP est de proposer un service de messagerie complet et utilisable qui vous aide à détecter le courrier indésirable, les menaces d'e-mails frauduleux (hameçonnage) et les logiciels malveillants, et de protéger les utilisateurs.
  
## <a name="the-challenge"></a>Défi à relever

La messagerie électronique est devenue un outil de communication important non seulement pour les consommateurs, mais aussi pour le marketing, l’assistance technique, les organisations de ventes et les entreprises de toutes tailles. Au fur et à mesure que la messagerie électronique prend de l’importance, la mauvaise utilisation qui en est faite aussi. Le courrier indésirable non surveillé peut surcharger les boîtes de réception et les réseaux, affecter la satisfaction des utilisateurs et entraver l’efficacité des communications d’e-mails légitimes. C’est pourquoi Microsoft continue à investir dans les technologies anti-spam. En bref, cela commence par la détection et le filtrage du courrier indésirable.  
  
## <a name="our-efforts"></a>Nos efforts

EOP offre une procédure permettant de réduire l’impact négatif du courrier indésirable sur l’expérience de messagerie des utilisateurs.
  
### <a name="exchange-online-protection-technology"></a>Technologie d’Exchange Online Protection

Pour réduire le courrier indésirable, EOP inclut une protection contre le courrier indésirable à l’aide de technologies de filtrage EOP propriétaires qui identifient et distinguent le courrier indésirable du courrier légitime. Le filtrage de contenu EOP tire ses leçons des menaces de courrier indésirable et de hameçonnage connues et des commentaires des utilisateurs de notre plateforme consommateur, Outlook.com. Ces types de données permettent aux technologies EOP de s’entraîner à reconnaître le courrier légitime et le courrier indésirable. Ils sont cruciaux pour la réputation de l’expéditeur. Les commentaires continus des utilisateurs d’EOP du programme de classification du courrier indésirable garantissent que les technologies EOP sont constamment formées et améliorées.
  
#### <a name="how-does-eop-work"></a>Comment fonctionne EOP ?

Lorsqu'un utilisateur externe envoie un courrier électronique à un utilisateur EOP, les technologies de filtrage EOP évaluent le contenu du message et attribuent une valeur au message selon la probabilité qu'il s'agisse de courrier indésirable. Cette valeur est stockée en tant que propriété de message appelée Seuil de probabilité de courrier indésirable (SCL - Spam Confidence Level ) avec le message lui-même. La valeur SCL reste avec le message lors de son envoi à d'autres couches de protection anti-spam dans EOP. 
  
Les règles dans EOP sont définies pour traiter les messages électroniques avec différentes valeurs SCL. Si un message a une valeur SCL supérieure à un certain seuil, il est considéré comme du courrier indésirable. Le message est mis en quarantaine ou remis dans le dossier de courrier indésirable de l'utilisateur en fonction de la façon dont l'administrateur système configure l'option de remise de courrier indésirable.
  
#### <a name="eop-filters"></a>Filtres EOP

Outre les technologies de filtrage anti-spam, EOP offre également à l’administrateur système la possibilité de définir des niveaux de filtre pour personnaliser davantage la remise des messages à ses comptes d’utilisateurs. Les administrateurs peuvent facilement ajouter un nom d'expéditeur ou de domaine à la liste des domaines et des expéditeurs autorisés afin que les e-mails provenant de cet expéditeur ou domaine ne soient jamais traités comme du courrier indésirable, quel que soit le contenu du message. Pour plus d'informations, consultez la rubrique liste des expéditeurs autorisés [et des expéditeurs bloqués dans Exchange Online](safe-sender-and-blocked-sender-lists-faq.md).
  
### <a name="phishing-protection"></a>Protection contre le hameçonnage

Le hameçonnage est une forme d’usurpation d’identité. Il représente l’une des menaces qui évolue le plus vite sur Internet. Vous pouvez souvent identifier un message de hameçonnage lorsqu’il demande des informations personnelles ou financières ou inclut un lien vers un site web qui demande de telles informations. EOP offre une protection contre le hameçonnage dans le cadre des technologies de filtrage EOP propriétaires. Les technologies de filtrage EOP analysent les e-mails pour tenter de détecter les liens frauduleux ou les domaines usurpés afin de protéger les utilisateurs contre ces types d’escroqueries en ligne.
  
#### <a name="how-does-phishing-protection-work"></a>Comment fonctionne la protection contre le hameçonnage ?

Souvent, un e-mail de hameçonnage est envoyé avec un lien qui, une fois que l'utilisateur clique dessus, le redirige vers un site web frauduleux qui semble valide (par exemple, votre établissement financier ou service en ligne). Généralement, ce site de hameçonnage invite l'utilisateur à saisir des informations personnelles telles que les noms d'utilisateur, les mots de passe et les numéros de sécurité sociale. Toutes les informations saisies sur le site de hameçonnage aident son auteur à voler votre identité. En utilisant des logos et des noms de marque approuvés connus, les auteurs de hameçonnage peuvent sembler légitimes. La technologie de filtrage de hameçonnage proposée dans EOP recherche des caractéristiques de hameçonnage potentielles dans les e-mails. Si elle en trouve, l'e-mail est déplacé vers le dossier de courrier indésirable.
  
Microsoft concentre ses efforts en matière de technologie anti-hameçonnage à deux niveaux : tout d'abord en empêchant les e-mails d'hameçonnage d'atteindre les utilisateurs, puis en évitant que les utilisateurs ne soient trompés par des e-mails et des sites web falsifiés. 
  
> [!TIP]
> Internet Explorer version 7 et supérieure bloque ou avertit les utilisateurs lorsqu'ils visitent des sites de hameçonnage potentiels ou connus afin qu'ils ne se retrouvent pas piégés et amenés à fournir des informations personnelles.[Vérifiez que vos possédez la dernière version d'Internet Explorer](https://www.microsoft.com/windows/ie/default.mspx). 
  
#### <a name="authentication"></a>Authentification

L'usurpation de domaine est un moyen d'imiter une adresse e-mail légitime afin de donner une apparence légitime à un e-mail frauduleux. L'usurpation est utilisée par des personnes ou des organisations malveillantes dans des escroqueries d'hameçonnage pour inciter les utilisateurs à divulguer des informations personnelles confidentielles. La divulgation de ces informations peut conduire à un vol d'identité et à d'autres types de fraude.
  
EOP utilise Sender Protection Framework (SPF), DomainKeys Identified Mail (DKIM), et Domain-based Message Authentication, Reporting, and Conformance (DMARC), ainsi que d'autres authentifications implicites pour vérifier que les messages proviennent du domaine dont ils sont supposés provenir. Nous conseillons à tous les expéditeurs d'utiliser SPF et DKIM pour protéger leurs destinataires contre les escroqueries de courrier indésirable et de hameçonnage. Nous conseillons aux expéditeurs de penser à publier une authentification DMARC pour rejeter ou mettre en quarantaine les messages provenant d'expéditeurs non autorisés.
  
- Pour en savoir plus sur SPF, voir [RFC 7208](https://tools.ietf.org/html/rfc7208) et [Sender Policy Framework](http://www.openspf.org/).
    
- Pour plus d'informations sur DKIM, voir [RFC 6376](https://tools.ietf.org/html/rfc6376) et [DKIM.org](http://dkim.org/).
    
- Pour en savoir plus sur DMARC, voir [DMARC.org](https://dmarc.org/).
    
### <a name="legislation"></a>Législation

Chez Microsoft, nous pensons que l’évolution de nouvelles technologies et de l’auto-réglementation requiert la prise en charge de cadres juridiques et d’une politique gouvernementale efficaces. La prolifération du courrier indésirable dans le monde a poussé de nombreux organes législatifs à réglementer les e-mails commerciaux. De nombreux pays/régions ont désormais des lois de lutte contre le courrier indésirable. Aux États-Unis, des lois au niveau fédéral et au niveau de l’État régissent le courrier indésirable, et cette approche complémentaire contribue à réduire le courrier indésirable tout en permettant au commerce électronique légitime de prospérer. Le CAN-SPAM Act développe les outils disponibles pour limiter les messages électroniques frauduleux et trompeurs.
  

