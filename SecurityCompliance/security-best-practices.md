---
title: Meilleures pratiques de sécurité pour Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: Réduisez le potentiel d'une violation de données ou d'un compte compromis en suivant ces meilleures pratiques recommandées.
ms.openlocfilehash: bd4b911cd5972b7d6dc9b55c17e375d326b1d571
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31026335"
---
# <a name="security-best-practices-for-office-365"></a>Meilleures pratiques de sécurité pour Office 365

Réduisez le potentiel d'une violation de données ou d'un compte compromis en suivant ces meilleures pratiques recommandées.
  
Cet article contient une liste rapide des meilleures pratiques. Pour une analyse plus approfondie et des informations sur la configuration de la sécurité, voir la feuille de [route de sécurité Office 365: priorités principales des 30 premiers jours, 90 jours et](security-roadmap.md)plus. Dans cet article, vous trouverez des informations basées sur des recherches d'attaques réelles, où nos experts Microsoft Office 365 Cybersecurity fournissent un coaching sur la façon d'évaluer les risques et d'implémenter la sécurité, la conformité et les informations les plus critiques. contrôles de protection pour protéger votre client Office 365. Vous apprendrez à définir la priorité des menaces, à traduire les menaces dans une stratégie technique, puis à adopter une approche systématique de l'implémentation des fonctionnalités et des contrôles.
  
## <a name="use-office-365-secure-score"></a>Utiliser le score de sécurité Office 365

Secure score est un outil d'analyse de la sécurité qui vous recommande ce que vous pouvez faire pour réduire davantage les risques. Le score de sécurité examine vos paramètres et activités Office 365 et les compare à une base établie par Microsoft. Vous obtiendrez un score en fonction de l'alignement des meilleures pratiques en matière de sécurité. Pour plus d'informations sur la façon d'obtenir un score sécurisé et de l'utiliser pour renforcer la sécurité de votre organisation Office 365, consultez [la rubrique Présentation du score de sécurité office 365](office-365-secure-score.md).
  
Vous souhaitez essayer le score de sécurité?
  
À l'aide d'un compte professionnel ou scolaire auquel a été attribué le rôle Office [365 admin Roles sur](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) Office 365, [Connectez-vous à Office 365](https://www.office.com/signin).
  
Accès sécurisé à [https://SecureScore.office.com](https://SecureScore.office.com).
  
## <a name="use-multi-factor-authentication-mfa"></a>Utiliser l'authentification multifacteur (MFA)

MFA ajoute une couche de protection supplémentaire à une stratégie de mot de passe fort en demandant aux utilisateurs d'accuser réception d'un appel téléphonique, d'un message texte ou d'une notification d'application sur leur téléphone intelligent après avoir entré correctement leur mot de passe. Avec l'authentification multiFACTEUR en place, les comptes d'utilisateur Office 365 sont toujours protégés contre les accès non autorisés même si le mot de passe d'un utilisateur est compromis. Les comptes sont protégés car l'accès n'est accordé à un compte qu'une fois que la demande supplémentaire a été satisfaite. Un mot de passe compromis ou volé n'est pas suffisant.
  
- [Planifier l'authentification multifacteur pour les déploiements d'Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)

- [Configurer l’authentification multifacteur pour les utilisateurs d’Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)

## <a name="use-office-365-cloud-app-security"></a>Utilisation de la sécurité des applications Cloud Office 365

ConFigurez des stratégies basées sur les besoins de votre entreprise pour suivre les activités anormales et agir sur celle-ci. ConFigurez les alertes avec la sécurité des applications Cloud Office 365 afin que les administrateurs puissent consulter les activités utilisateur inhabituelles ou risquées, telles que le téléchargement de grandes quantités de données, l'échec des tentatives de connexion multiples ou les connexions à partir d'une adresse IP inconnue ou dangereuse. Pour les organisations disposant d'un plan Office 365 Enterprise E5, vous pouvez commencer à utiliser Office 365 Cloud App Security immédiatement. Si vous avez un autre plan d'entreprise, vous pouvez acheter la sécurité des applications Cloud d'Office 365 en tant que module complémentaire.
  
- [Vue d'ensemble de la sécurité des applications Cloud Office 365](office-365-cas-overview.md)

- [Activer la sécurité des applications Cloud Office 365](turn-on-office-365-cas.md)

## <a name="secure-mail-flow"></a>Flux de messagerie sécurisé

Implémentez l'ensemble riche des fonctionnalités dans Exchange Online Protection et bénéficiez d'une plus grande fiabilité de l'identité de l'expéditeur de chaque message électronique, ainsi que de la protection contre les programmes malveillants inconnus, les virus et les URL malveillantes transmises par courrier électronique.
  
- ConFigurez les stratégies de protection contre le courrier inDésirable pour votre organisation dans [Office 365](anti-spam-protection.md) .

- Découvrez, puis utilisez la [protection avancée contre les menaces pour les pièces jointes et les liens fiables](https://technet.microsoft.com/library/mt148491.aspx).

- [Ajoutez une protection contre les programmes malveillants à votre organisation](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).

- Découvrez et activez les [conseils de sécurité dans les messages électroniques dans Office 365](safety-tips-in-office-365.md) pour vos utilisateurs.

- Si vous utilisez un domaine personnalisé pour votre organisation dans Office 365, configurez SPF, DKIM, puis DMARC pour valider le courrier électronique envoyé par votre organisation et empêcher l'usurpation:

  - [Configurez SPF dans Office 365 pour éviter l'usurpation](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).

  - [Utilisez DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).

  - [Utiliser DMARC pour valider les messages électroniques dans Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).

## <a name="enable-mailbox-audit-logging"></a>Activer l’enregistrement d’audit de boîte aux lettres

Certains enregistrements d'audit sont automatiquement activés dans Office 365; Toutefois, l'enregistrement d'audit de boîte aux lettres n'est pas activé par défaut. Vous activez la journalisation d'audit pour toutes les boîtes aux lettres utilisateur dans Office 365 à l'aide d'Exchange Online PowerShell. Pour plus d'informations, consultez la rubrique [activation de l'audit des boîtes aux lettres dans Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).
  
Une fois que vous avez activé la journalisation d'audit, vous pouvez [effectuer des recherches &amp; dans le journal d'audit dans le centre de sécurité conformité d'Office 365](search-the-audit-log-in-security-and-compliance.md) pour savoir qui s'est connecté à vos boîtes aux lettres d'utilisateurs, envoyer des messages et d'autres activités effectuées par le propriétaire de la boîte aux lettres, un utilisateur délégué ou un administrateur. Pour obtenir la liste des activités de boîte aux lettres incluses dans le journal d'audit Office 365 par défaut, consultez la rubrique [Exchange Mailbox Activities](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).
  
Pour plus d'informations sur les autres actions que vous pouvez effectuer avec le journal d'audit, telles que la modification de la durée d'enregistrement des entrées dans le journal d'audit, consultez la rubrique [enregistrement d'audit des boîtes aux lettres dans Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).
  
## <a name="configure-data-loss-prevention-dlp"></a>Configurer la protection contre la perte de données (DLP)

DLP vous permet d'identifier les données sensibles et de créer des stratégies qui permettent d'empêcher les utilisateurs de partager accidentellement ou intentionnellement les données. DLP fonctionne dans Office 365, y compris Exchange Online, SharePoint Online et OneDrive, afin que vos utilisateurs puissent rester conformes sans interrompre leur flux de travail. Pour plus d’informations, reportez-vous à [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).
  
## <a name="use-customer-lockbox"></a>Utiliser le référentiel sécurisé du client

En tant qu'administrateur Office 365, vous pouvez utiliser le référentiel sécurisé du client pour contrôler la manière dont un technicien du support technique Microsoft accède à vos données pendant une session d'aide. Dans le cas où l'ingénieur requiert l'accès à vos données pour résoudre un problème, le référentiel sécurisé vous permet d'approuver ou de rejeter la demande d'accès. Si vous l'approuvez, l'ingénieur peut accéder aux données. Chaque demande a un délai d'expiration, et une fois que le problème est résolu, la demande est fermée et l'accès révoqué. Le référentiel sécurisé du client est inclus dans le plan Office 365 entreprise E5 ou vous pouvez acheter un abonnement distinct avec tout autre plan d'entreprise Office 365. Pour plus d'informations, reportez-vous à la rubrique [Office 365 customEr Lockbox demandes](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).
  
## <a name="try-it-yourself"></a>Essayez-le
<a name="SecureScore"> </a>

Consultez ces fonctionnalités de sécurité dans un abonnement d'évaluation Office 365 avant de les adopter en production.
  
- [Création d'un abonnement d'évaluation Office 365](https://technet.microsoft.com/library/mt736406.aspx)

- [Configurer et tester l'authentification multiFACTEUR pour un compte d'utilisateur](https://technet.microsoft.com/library/mt492459.aspx)

- [Configurer et tester la sécurité des applications Cloud Office 365 pour vous informer de l'activité d'administration globale](https://technet.microsoft.com/library/mt757250.aspx)

- [Configurer et tester la protection avancée contre les menaces pour le courrier suspect](https://technet.microsoft.com/library/mt490479.aspx)

- Vérifiez le [score de sécurité Office 365](https://securescore.office.com/) pour votre abonnement à la version d'évaluation pour chacune des étapes ci-dessus.