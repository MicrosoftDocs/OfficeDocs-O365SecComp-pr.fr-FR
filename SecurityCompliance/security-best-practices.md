---
title: Meilleures pratiques de sécurité pour Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: Réduire le risque d’une violation de données ou d’un compte compromis en suivant ces meilleures pratiques recommandées.
ms.openlocfilehash: 63bda11afdd1e02e9e12e8c505aca7100c4deade
ms.sourcegitcommit: a36d2692396786f49c8765c65145e5093578e9a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2018
ms.locfileid: "25498090"
---
# <a name="security-best-practices-for-office-365"></a>Meilleures pratiques de sécurité pour Office 365

Réduire le risque d’une violation de données ou d’un compte compromis en suivant ces meilleures pratiques recommandées.
  
Cet article contient une liste rapide des meilleures pratiques. Pour plus d’une analyse approfondie et pour plus d’informations sur la configuration de sécurité, consultez la rubrique [Guide de sécurité Office 365 : principaux des priorités pour les 30 premiers jours, 90 jours et au-delà de](security-roadmap.md). Dans cet article, vous trouverez des informations selon des enquêtes d’attaques concrètes, où nos experts en sécurité Microsoft Office 365 supérieurs fournissent accompagnement comment évaluer les risques et implémenter la sécurité, de conformité et informations essentielles contrôles de protection pour protéger votre organisation cliente Office 365. Vous allez apprendre à classer les menaces et contre les menaces se traduire par une stratégie technique, puis placez une approche systématique pour implémenter les fonctionnalités et les contrôles.
  
## <a name="use-office-365-secure-score"></a>Utilisez le Score sécurisé Office 365

Score sécurisé est un outil analytique sécurité recommande ce que vous pouvez faire pour réduire encore le risque. Score sécurisé examine vos paramètres Office 365 et les activités et les compare à une base établie par Microsoft. Vous obtiendrez un score dépendent de comment aligné avec les meilleures pratiques de sécurité. Pour plus d’informations sur la façon d’obtenir le Score d’informations sécurisé et l’utiliser pour renforcer la sécurité de votre organisation Office 365, voir [Présentation de la note de sécuriser Office 365](office-365-secure-score.md).
  
Vous souhaitez essayer de Score d’informations sécurisé ?
  
À l’aide d’un compte professionnel ou de l’école qui a été affecté le rôle d’Office 365, [les rôles d’administration sur Office 365](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) , [se connecter à Office 365](https://www.office.com/signin).
  
Accès sécurisé Score à [https://SecureScore.office.com](https://SecureScore.office.com).
  
## <a name="use-multi-factor-authentication-mfa"></a>Utiliser l’authentification multifacteur (MFA)

MFA ajoute une couche de protection supplémentaire à une stratégie de mot de passe fort en demandant aux utilisateurs à remercier un appel téléphonique, message texte ou une notification de l’application sur leur téléphone active après avoir entré correctement leur mot de passe. Avec MFA en place, les comptes d’utilisateurs Office 365 sont toujours protégés contre les accès non autorisés même si le mot de passe d’un utilisateur est compromise. Les comptes sont protégées car pas l’accès à un compte jusqu'à une fois le défi supplémentaire a été satisfait. Un mot de passe compromis ou volé ne suffit pas.
  
- [Offre pour l'authentification multifacteur des déploiements Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Configurer l’authentification multifacteur pour les utilisateurs d’Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a>Utilisation de la sécurité d’application Office 365 dans le nuage

Définir des stratégies en fonction des besoins de votre entreprise pour suivre l’activité anormale et d’agir. Configurer les alertes de sécurité pour application Cloud Microsoft Office 365 afin que les administrateurs peuvent vérifier activité utilisateur inhabituelle ou risqué, telles que le téléchargement de grandes quantités de données, plusieurs Échec de tentatives de connexion ou des connexions à partir d’une adresse IP inconnue ou dangereuse. Pour les organisations avec un plan Office 365 entreprise E5, vous pouvez démarrer à l’aide d’Office 365 Cloud application sécurité immédiatement. Si vous disposez d’un plan d’entreprise différents, vous pouvez acheter Office 365 Cloud application sécurité comme module complémentaire.
  
- [Vue d’ensemble de la sécurité des application Cloud O365](office-365-cas-overview.md)
    
- [Activer la sécurité des applications cloud Office 365](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a>Flux de messagerie sécurisée

Implémenter les riches fonctionnalités dans Exchange Online Protection et obtenir une plus grande assurance sur l’identité de l’expéditeur de chaque message électronique et protéger contre les programmes malveillants inconnus, les virus et URL malveillantes transmis par le biais de messages électroniques.
  
- Configurer des stratégies de [Protection de blocage du courrier indésirable messagerie Office 365](anti-spam-protection.md) pour votre organisation. 
    
- En savoir plus sur, puis utilisez [protection contre les menaces avancées pour les pièces jointes fiables et les liens sécurisés](https://technet.microsoft.com/library/mt148491.aspx).
    
- [Ajouter la protection anti-programme malveillant à votre organisation](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).
    
- En savoir plus sur et activer des [conseils de sécurité dans les messages électroniques dans Office 365](safety-tips-in-office-365.md) pour vos utilisateurs. 
    
- Si vous utilisez un domaine personnalisé pour votre organisation dans Office 365, configurer SPF, DKIM, puis DMARC pour valider les messages envoyés par votre organisation et afin d’empêcher l’usurpation d’identité :
    
  - [Configurer SPF dans Office 365 afin d’empêcher l’usurpation d’identité](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Utilisez DKIM pour valider le courrier sortant envoyé à partir de votre domaine personnalisé dans Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).
    
  - [Utiliser DMARC pour valider le courrier dans Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
## <a name="enable-mailbox-audit-logging"></a>Activer l'enregistrement d'audit de boîte aux lettres

Certains l’enregistrement d’audit est activée automatiquement pour vous dans Office 365 ; Toutefois, l’enregistrement d’audit boîte aux lettres n’est pas activé par défaut. Vous activez l’enregistrement d’audit pour toutes les boîtes aux lettres d’utilisateur dans Office 365 à l’aide d’Exchange Online PowerShell. Pour plus d’informations, voir [Activer la boîte aux lettres de l’audit dans Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
Une fois que vous avez activé vous enregistrement d’audit peut [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md) permettant de savoir qui a ouvert une session dans vos boîtes aux lettres utilisateur, envoyé de messages et autres activités effectuées par le propriétaire de boîte aux lettres, un utilisateur délégué, ou un administrateur. Pour obtenir la liste des activités de boîte aux lettres qui sont inclus dans Office 365 journal d’audit par défaut, voir les [activités de boîte aux lettres Exchange](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).
  
Pour plus d’informations sur les autres actions que vous pouvez effectuer avec le journal d’audit, telle que la modification de la quantité de temps pour enregistrer les entrées dans le journal d’audit, voir [enregistrement dans Exchange 2016 d’audit de boîte aux lettres](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).
  
## <a name="configure-data-loss-prevention-dlp"></a>Configurer la protection contre la perte de données (DLP)

DLP permet d’identifier les données sensibles et créer des stratégies qui permettent d’empêcher les utilisateurs d’accidentellement ou intentionnellement partage des données. DLP fonctionne sur Office 365, notamment Exchange Online, SharePoint Online et OneDrive afin que vos utilisateurs de rester conformes sans interrompre leur travail. Pour plus d’informations, voir [vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).
  
## <a name="use-customer-lockbox"></a>Utilisez la zone de sécurité client

En tant qu’un administrateur Office 365, vous pouvez utiliser la zone de sécurité client pour contrôler la façon dont un ingénieur du support technique Microsoft accède à vos données pendant une session de l’aide. Dans les cas où l’ingénieur requiert l’accès à vos données à résoudre les problèmes et à résoudre un problème, zone de sécurité client vous permet d’approuver ou refuser la demande d’accès. Si vous l’approuver, l’ingénieur peut accéder aux données. Chaque demande a un délai d’expiration et une fois que le problème est résolu, la demande est fermée et l’accès a été révoqué. Zone de sécurité client est inclus dans le plan Office 365 pour entreprises 5, ou vous pouvez acheter un abonnement distinct avec tout autre plan d’entreprise Office 365. Pour plus d’informations, voir [Demandes de zone de sécurité du client Office 365](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).
  
## <a name="try-it-yourself"></a>Essayer
<a name="SecureScore"> </a>

Consultez ces fonctionnalités de sécurité fonctionne dans un abonnement d’évaluation Office 365 avant de les adopter en production.
  
- [Créer un abonnement d’évaluation d’Office 365](https://technet.microsoft.com/library/mt736406.aspx)
    
- [Configurer et tester MFA pour un compte d’utilisateur](https://technet.microsoft.com/library/mt492459.aspx)
    
- [Configurer et tester la sécurité d’application Office 365 dans le nuage pour vous avertir d’activité de l’administrateur global](https://technet.microsoft.com/library/mt757250.aspx)
    
- [Configurer et tester DAV pour le courrier électronique suspect](https://technet.microsoft.com/library/mt490479.aspx)
    
- Vérifiez le [Score de sécuriser Office 365](https://securescore.office.com/) pour votre abonnement d’évaluation pour chacune des étapes ci-dessus 
    

