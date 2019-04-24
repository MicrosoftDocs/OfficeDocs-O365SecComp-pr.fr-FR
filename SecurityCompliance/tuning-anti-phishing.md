---
title: Réglage de la protection anti-hameçonnage dans Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Les administrateurs peuvent apprendre à identifier les raisons et le mode de réception des messages de hameçonnage, ainsi que la marche à suivre pour éviter d'autres messages de phishing à l'avenir.
ms.openlocfilehash: c3025267ad8e01c18de618c85127dfe1077a16aa
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264316"
---
# <a name="tune-anti-phishing-protection-in-office-365"></a>Réglage de la protection anti-hameçonnage dans Office 365

Bien qu'Office 365 offre une variété de fonctionnalités anti-hameçonnage qui sont activées par défaut, il est possible que certains messages de phishing continuent à accéder à vos boîtes aux lettres. Cette rubrique décrit ce que vous pouvez faire pour découvrir pourquoi un message de hameçonnage s'affiche, et ce que vous pouvez faire pour ajuster les paramètres anti-hameçonnage de votre organisation Exchange Online sans que cela ne _soit pire_.

## <a name="first-things-first-deal-with-any-compromised-accounts-and-make-sure-you-block-any-more-phishing-messages-from-getting-through"></a>Tout d'abord: traitez les comptes compromis et assurez-vous de bloquer les messages de hameçonnage

Si le compte d'un destinataire a été compromis suite à un message de hameçonnage, suivez les étapes décrites dans la [réponse à un compte de messagerie compromis dans Office 365](responding-to-a-compromised-email-account.md).

Si votre abonnement inclut la protection avancée contre les menaces (ATP), vous pouvez utiliser [Office 365 Threat Intelligence](office-365-ti.md) pour identifier les autres utilisateurs qui ont également reçu le message de hameçonnage. Vous disposez d'options supplémentaires pour bloquer les messages de hameçonnage:

- [Liens fiables ATP](set-up-atp-safe-links-policies.md)

- [Pièces jointes fiables ATP](set-up-atp-safe-attachments-policies.md)

- [Stratégies anti-hameçonnage ATP](set-up-anti-phishing-policies.md). Notez que vous pouvez augmenter temporairement les **seuils de phishing avancés** dans la stratégie, **de standard** à **agressif**, **plus agressif**ou **plus agressif**.

Vérifiez que ces fonctionnalités ATP sont activées.

## <a name="report-the-phishing-message-to-microsoft"></a>Signaler le message de hameçonnage à Microsoft

La création de rapports sur les messages de hameçonnage est utile pour régler les filtres utilisés pour protéger tous les clients dans Office 365.

Envoyer le message de hameçonnage _en tant que pièce jointe_ dans un nouveau message, autrement vide, dans **Phish@office365.microsoft.com**. Ne transférez pas uniquement le message d'origine; dans le cas contraire, nous ne pouvons pas examiner les en-têtes de message d'origine. Vous pouvez également utiliser le complément de [message de rapport](https://docs.microsoft.com/office365/securitycompliance/enable-the-report-message-add-in) dans Outlook ou Outlook sur le Web (anciennement appelé Outlook Web App).

Pour plus d'informations, consultez la rubrique [Soumission des messages indésirables, légitimes ou des tentatives de hameçonnage à Microsoft pour analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).

## <a name="inspect-the-message-headers"></a>Inspecter les en-têtes de message

Vous pouvez examiner les en-têtes du message de hameçonnage pour voir s'il y a quelque chose que vous pouvez faire vous-même pour empêcher d'autres messages de phishing de venir. En d'autres termes, l'examen des en-têtes de messages peut vous aider à identifier tous les paramètres de votre organisation qui ont été chargés d'autoriser les messages de hameçonnage dans.

Plus précisément, vous devez vérifier le champ d'en-tête **X-Forefront-antispam-Report** dans les en-têtes de message pour obtenir des indications de courrier indésirable ignoré ou de filtrage du courrier indésirable dans la valeur de filtrage du courrier indésirable (SFV). Les messages qui ignorent le filtrage auront une `SCL:-1`entrée de, ce qui signifie que l'un de vos paramètres a autorisé ce message en remplaçant le courrier indésirable ou le score de phishing déterminé par le service. Pour plus d'informations sur l'obtention des en-têtes de message et la liste complète des en-têtes de message anti-courrier indésirable et anti-hameçonnage disponibles, consultez la rubrique [anti-spam message headers](https://docs.microsoft.com/office365/SecurityCompliance/anti-spam-message-headers).

## <a name="best-practices-to-stay-protected"></a>Meilleures pratiques pour rester protégé

- Sur une base mensuelle, exécutez le score de sécurité [office 365](office-365-secure-score.md) pour évaluer les paramètres de sécurité de votre organisation Office 365.

- Consultez régulièrement le [rapport](learn-about-spoof-intelligence.md) d'aide à la décision et activez la protection contre l' [usurpation d'identité dans la stratégie anti-hameçonnage](learn-about-spoof-intelligence.md#configuring-the-anti-spoofing-policy) pour **mettre en quarantaine** les messages suspects au lieu de les transmettre au dossier de courrier indésirable de l'utilisateur.

- Examinez régulièrement le [rapport d'état de protection contre les menaces](view-reports-for-atp.md#threat-protection-status-report).

- Certains clients peuvent accidentellement autoriser les messages d'hameçonnage en plaçant leurs propres domaines dans la liste autoriser l'expéditeur ou autoriser le domaine dans les stratégies de blocage du courrier indésirable. Si vous choisissez de le faire, vous devez utiliser une extrême prudence. Bien que cette configuration autorise certains messages légitimes, elle autorise également les messages malveillants qui seraient normalement bloqués par le courrier indésirable Office 365 et/ou les filtres anti-hameçonnage.

  La meilleure façon de traiter les messages légitimes bloqués par Office 365 (faux positifs) qui impliquent des expéditeurs dans votre domaine est de configurer entièrement et complètement les enregistrements SPF, DKIM et DMARC dans le système DNS pour _tous_ vos domaines de messagerie dans Office 365:

  - Vérifiez que votre enregistrement SPF identifie _toutes les_ sources de courrier pour les expéditeurs de votre domaine (n'oubliez pas les services tiers).

  - Utilisez la défaillance matérielle\-() pour vous assurer que les expéditeurs non autorisés sont rejetés par les systèmes de messagerie qui sont configurés pour le faire. Vous pouvez utiliser l'Assistant d'aide à la [décision](https://docs.microsoft.com/office365/securitycompliance/learn-about-spoof-intelligence) pour identifier les expéditeurs qui utilisent votre domaine afin que vous puissiez inclure des expéditeurs tiers autorisés dans votre enregistrement SPF.

  Pour obtenir des instructions de configuration, voir:
  
  - [Configurer SPF dans Office 365 pour empêcher l’usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md)

  - [Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md)

  - [Utiliser DMARC pour valider les messages électroniques dans Office 365](use-dmarc-to-validate-email.md)

- Dans la mesure du possible, nous vous recommandons de livrer le courrier électronique pour votre domaine directement à Office 365. En d'autres termes, pointez l'enregistrement MX de votre domaine Office 365 vers Office 365. Exchange Online Protection (EOP) est capable de fournir la meilleure protection aux utilisateurs de votre nuage lorsque leur courrier est remis directement à Office 365. Si vous devez utiliser un système d'hygiène de messagerie tiers devant l'environnement EOP, vérifiez que vous avez suivi les conseils [ici](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-mail-flow-using-third-party-cloud).

- L'authentification multifacteur (MFA) est une excellente façon d'empêcher les comptes compromis. Vous devez sérieusement envisager d'activer l'authentification multiFACTEUR pour tous vos utilisateurs. Pour une approche progressive, commencez par activer l'authentification multiFACTEUR pour vos utilisateurs les plus sensibles (administrateurs, cadres, etc.) avant d'activer l'authentification multiFACTEUR pour tout le monde. Pour obtenir des instructions, consultez la rubrique [set up Multi-Factor Authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication).

- Les règles de transfert vers des destinataires externes sont souvent utilisées par des agresseurs pour extraire des données. Utilisez les informations relatives **aux règles de transfert de boîte aux lettres** dans [Office 365 Secure score](office-365-secure-score.md) pour rechercher et même empêcher le transfert des règles vers des destinataires externes. Pour plus d'informations, consultez la rubrique [minimisation des règles de transfert externe des clients avec le score sécurisé](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/).
