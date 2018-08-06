---
title: Création de rapports et suivi des messages dans Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: Microsoft Exchange Online Protection (EOP) offre un grand nombre de rapports qui peuvent vous aider à déterminer l'état général de votre organisation. Il existe également des outils vous permettant de résoudre des problèmes liés à des événements spécifiques (comme un message n'arrivant pas aux destinataires appropriés) et des rapports d'audit pour vous aider à respecter les exigences de conformité. Le tableau suivant décrit les rapports et les outils de dépannage disponibles pour les administrateurs EOP.
ms.openlocfilehash: 01a09b2b4b72161352af3793686c6cc888e44e29
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027141"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a>Création de rapports et suivi des messages dans Exchange Online Protection

Microsoft Exchange Online Protection (EOP) offre de nombreux rapports qui peuvent vous aider à déterminent l’état global et l’intégrité de votre organisation. Il existe également des outils pour vous aider à résoudre des événements spécifiques (par exemple, un message qui arrivent ne pas à ses destinataires) et les rapports d’audit à l’aide des exigences de conformité. 

## <a name="usage-reports"></a>Rapports d’utilisation

**Groupes Office 365 activité** Permet d'afficher des informations sur le nombre de Groupes Office 365 qui sont créées et utilisées.  

**Activité de messagerie** Permet d'afficher des informations sur le nombre de messages envoyés, reçus et lus dans votre organisation et par des utilisateurs spécifiques.  

**Utilisation de l’application messagerie** Afficher des informations sur les applications de messagerie qui sont utilisés. Cela inclut le nombre total de connexions pour chaque application et les versions d’Outlook qui sont connectent.  

**Utilisation de boîtes aux lettres** Permet d'afficher les informations sur l'espace de stockage utilisé, la consommation de quota, le nombre d'éléments et la dernière activité (activité d'envoi ou de lecture) des boîtes aux lettres.

Voir les ressources suivantes pour plus d’informations :

- [Rapports d’Office 365 dans le centre d’administration - groupes d’Office 365](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [Rapports Office 365 dans le Centre d'administration - Activité du courrier électronique](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [Rapports Office 365 dans le Centre d'administration - Utilisation des applications de messagerie](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [Rapports Office 365 dans le Centre d'administration - Utilisation des boîtes aux lettres](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-office-365-admin-center"></a>Sécurité &amp; des rapports de conformité dans le centre d’administration d’Office 365

Ces rapports enrichies offrent une expérience de création de rapports interactif pour les administrateurs d’EOP, qui inclut les informations de synthèse et la possibilité d’exploration pour plus d’informations.  

**Protection avancée contre les menaces (ATP)** Permet d'afficher des informations sur les liens fiables et pièces jointes fiables qui font partie de la fonctionnalité.  

**EOP** Afficher des informations sur la détection de programmes malveillants, courrier falsifié, détections de courrier indésirable et flux de messagerie à partir de votre organisation.  

[Afficher les rapports de protection contre les menaces avancées et Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a>Rapports personnalisés à l’aide de Microsoft Graph

Créer par programme des rapports qui sont disponibles dans le centre d’administration d’Office 365 à l’aide de Microsoft Graph voir les sujets secondaires de [l’utilisation des rapports d’utilisation d’Office 365 dans Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135) 

##<a name="custom-reports-using-reporting-web-services"></a>Rapports personnalisés à l’aide des services web de rapport

Créer par programme des rapports dans disponibles Exchange Online Protection PowerShell cmdlets de rapports à l’aide de REST/ODATA2 filtrage de requête.

Consultez la rubrique [Services Office 365 Reporting Web](https://go.microsoft.com/fwlink/p/?LinkId=279926) 

##<a name="message-trace"></a>Suivi des messages

Suit les messages pendant leur acheminement via EOP. Vous pouvez déterminer si un message électronique a été reçu, rejeté, différé ou remis par le service. Il indique également les actions exécutées sur le message avant qu’elle atteint son état final.  

Vous pouvez ainsi répondre efficacement aux questions de vos utilisateurs, résoudre les problèmes de flux de messagerie et valider les modifications de stratégie, tout en réduisant la nécessité de demander de l'aide à l'assistance technique.  

Voir [suivi d’un Message électronique](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx) 

## <a name="audit-logging"></a>Journalisation d'audit

Retrace le suivi des modifications spécifiques apportées par les administrateurs à votre organisation. Ces rapports peuvent vous aider à résoudre les problèmes de configuration ou de rechercher la cause de sécurité ou des problèmes liés à la conformité.  voir les [rapports d’audit dans EOP](auditing-reports-in-eop.md) 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a>Disponibilité et latence des rapports et des données de suivi des messages

Le tableau suivant présente la disponibilité des rapports et des données de suivi des messages EOP, ainsi que leur latence.
  
||||
|:-----|:-----|:-----|
|**Type de rapport** <br/> |**Données disponibles pendant (période rétrospective)** <br/> |**Latence** <br/> |
|Rapports de synthèse de protection de messagerie  <br/> |90 jours  <br/> |L'agrégation quasi-complète des données des messages dure entre 24 et 48 heures. Des modifications agrégées incrémentielles mineures peuvent se produire jusqu'à 5 jours.  <br/> |
|Rapports de détails de protection de messagerie  <br/> |90 jours  <br/> |Pour les données de détail de moins de 7 jours, les données apparaissent normalement dans les 24 heures, mais leur génération peut durer jusqu’à 48 heures. Il est possible que des modifications incrémentielles mineures soient apportées pendant 5 jours.  <br/> Pour les messages remontant à plus de sept jours, la génération des résultats détaillés peut prendre plusieurs heures.  <br/> |
|Données de suivi des messages  <br/> |90 jours  <br/> |Lorsque vous effectuez un suivi de messages remontant à moins de 7 jours, ces derniers apparaissent normalement dans les 5 à 30 minutes.  <br/> Lorsque vous effectuez un suivi de messages remontant à plus de 7 jours, la génération des résultats peut prendre plusieurs heures.  <br/> |
   
> [!NOTE]
> La disponibilité et la latence des données sont les mêmes, qu'elles soient demandées par Centre d'administration Office 365 ou Remote PowerShell. 
  

