---
title: FAQ sur le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 02/11/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: Vous avez une question sur la façon dont les nouvelles fonctionnalités de protection des messages dans Office 365 fonctionnent? Recherchez une réponse ici.
ms.openlocfilehash: 651d3f5953f0a6864259ed3a0c8ecde79f40d631
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217114"
---
# <a name="office-365-message-encryption-faq"></a>FAQ sur le chiffrement de messages Office 365

Vous avez une question sur la façon dont les nouvelles fonctionnalités de protection des messages dans Office 365 fonctionnent? Recherchez une réponse ici. Consultez également les [questions fréquemment posées sur la protection des données dans Azure information protection](https://docs.microsoft.com/information-protection/get-started/faqs-rms) pour obtenir des réponses aux questions sur le service de protection des données, Azure Rights Management, dans Azure information protection.

||
|:-----|
|Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins. |
||
  
## <a name="what-is-office-365-message-encryption-ome"></a>Qu'est-ce que le chiffrement de messages Office 365 (OME)?

OME combine les fonctionnalités de chiffrement de courrier électronique et de gestion des droits. Les fonctionnalités de gestion des droits sont gérées par Azure information protection.
  
## <a name="who-can-use-ome"></a>Qui peut utiliser OME?

Vous pouvez utiliser les nouvelles fonctionnalités de OME dans les conditions suivantes:
  
- Si vous n'avez jamais configuré OME ou IRM pour Exchange Online dans Office 365.
    
- Si vous avez configuré OME et IRM, vous pouvez suivre ces étapes si vous utilisez le service Azure Rights Management à partir d'Azure information protection.
    
- Si vous utilisez Exchange Online avec Active Directory Rights Management Services (AD RMS), vous ne pouvez pas activer immédiatement ces nouvelles fonctionnalités. Au lieu de cela, vous devez d'abord [migrER AD RMS vers Azure information protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) . Une fois la migration terminée, vous pouvez configurer OME. 
    
    Si vous choisissez de continuer à utiliser AD RMS sur site avec Exchange Online au lieu de migrer vers Azure information protection, vous ne pourrez pas utiliser ces nouvelles fonctionnalités.
    
## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a>Quels sont les abonnements nécessaires pour utiliser les nouvelles fonctionnalités d'OME?

Pour utiliser les nouvelles fonctionnalités de OME, vous avez besoin de l'un des plans suivants:
  
- Le chiffrement de messages Office 365 est proposé dans le cadre d'Office 365 Enterprise E3 et E5, de Microsoft entreprise E3 et E5, de Microsoft 365 Business, de Office 365 a1, a3 et a5, ainsi que d'Office 365 pour le gouvernement G3 et G5. Les clients n'ont pas besoin de licences supplémentaires pour recevoir les nouvelles fonctionnalités de protection optimisées par Azure information protection. 
    
- Vous pouvez également ajouter le plan de protection des informations Azure 1 aux plans suivants pour recevoir les nouvelles fonctionnalités de chiffrement des messages Office 365: Exchange Online plan 1, Exchange Online plan 2, Office 365 F1, Office 365 Business Essentials, Office 365 Business Premium ou Office 365 entreprise E1.
    
- Chaque utilisateur bénéficiant d'Office 365 le chiffrement de messages doit être concédé sous licence pour être couvert par la fonctionnalité.
    
- Pour obtenir la liste complète, consultez les [descriptions de service Exchange Online](https://technet.microsoft.com/library/exchange-online-service-description.aspx) pour le chiffrement de messages Office 365. 
    
## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a>Puis-je utiliser Exchange Online avec votre propre clé (BYOK) dans Azure information protection?

OK! Microsoft vous recommande d'effectuer les étapes de configuration de BYOK avant de configurer OME.
  
Pour plus d'informations sur BYOK, consultez [la rubrique planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>OME et BYOK avec Azure information protection modifient l'approche de Microsoft pour les demandes de données tierces telles que les demandes?

Nbre. OME et l'option permettant de fournir et de contrôler vos propres clés de chiffrement, appelées BYOK, à partir d'Azure information protection n'ont pas été conçues pour répondre aux apports à l'application de la Loi. OME, avec BYOK pour Azure information protection, a été conçu pour les clients orientés sur la conformité. Microsoft prend des demandes tierces de données client très sérieusement. En tant que fournisseur de services Cloud, nous sommes toujours le partisan de la confidentialité des données client. Dans le cas où nous obtenons une demande, nous tentons toujours de rediriger la tierce partie vers le client pour obtenir les informations. (Lisez le blog de Brad Smith: [protection des données client de l'espionnage public](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Nous publions régulièrement des informations détaillées sur la demande que nous recevons. Pour plus d'informations sur les demandes de données tierces, consultez la rubrique relative à la [réponse aux demandes d'autorisation du gouvernement et de la loi pour accéder aux données client](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) dans le centre de gestion de la confidentialité Microsoft. Consultez également la section «Divulgation des données client» dans les [services en ligne (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a>En quoi cette fonctionnalité est-elle associée aux fonctionnalités de chiffrement de messages Office 365 (OME) et de gestion des droits relatifs à l'information (IRM) héritées?

Les nouvelles fonctionnalités pour le chiffrement de messages Office 365 sont une évolution de la gestion des droits relatifs à l'information (IRM) et aux solutions OME héritées existantes. Le tableau suivant fournit plus de détails.
  
**Comparaison des fonctionnalités héritées de OME, de gestion des droits relatifs à l'information et de nouvelles OME**

|**Fonctionnalité**|**Versions antérieures d'OME**|**IRM**|**Nouvelles fonctionnalités OME**|
|:-----|:-----|:-----|:-----|
|**Envoi d'un message électronique chiffré**|Uniquement par le biais des règles de flux de messagerie Exchange|L'utilisateur final a initié à partir d'Outlook pour PC, Outlook pour Mac ou Outlook sur le Web; ou via les règles de flux de messagerie Exchange|L'utilisateur final a initié à partir d'Outlook pour PC, Outlook pour Mac ou Outlook sur le Web; ou via des règles de flux de messagerie|
|**Gestion des droits**|-|Option ne pas transférer et modèles personnalisés|Option ne pas transférer, option de chiffrement uniquement, modèles par défaut et modèles personnalisés|
|**Type de destinataire pris en charge**|Destinataires externes uniquement|Destinataires internes uniquement|Destinataires internes et externes|
|**Expérience pour le destinataire**|Les destinataires externes ont reçu un message HTML qu'ils ont téléchargés et ouverts dans un navigateur ou une application mobile téléchargée.|Les destinataires internes ont reçu uniquement des messages chiffrés dans Outlook pour PC, Outlook pour Mac et Outlook sur le Web.|Les destinataires internes et externes reçoivent des courriers électroniques dans Outlook pour PC, Outlook pour Mac, Outlook sur le Web, Outlook pour Android et Outlook pour iOS, ou via un portail Web, qu'ils se trouvent ou non dans la même organisation Office 365 ou dans n'importe quelle Office 365 Département. Le portail OME ne requiert pas de téléchargement séparé.|
|**Apporter votre propre prise en charge de clés**|Non disponible|Non disponible| BYOK pris en charge|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a>Comment activer les nouvelles fonctionnalités de OME pour mon organisation?

Consultez la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md).
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a>La version précédente de OME sera-t-elle déconseillée?

Vous pouvez toujours utiliser la version précédente de OME, elle ne sera pas désapprouvée pour le moment. Toutefois, nous encourageons vivement les organisations à utiliser la solution OME nouvelle et améliorée. Les clients qui n'ont pas encore déployé OME ne peuvent pas configurer un nouveau déploiement de la version précédente de OME.
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a>Mon organisation utilise Active Directory Rights Management, puis-je utiliser cette fonctionnalité?

Nbre. Si vous utilisez Exchange Online avec Active Directory Rights Management Services (AD RMS), vous ne pouvez pas activer immédiatement ces nouvelles fonctionnalités. Au lieu de cela, vous devez d'abord [migrER AD RMS vers Azure information protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) . 
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a>Mon organisation a un déploiement hybride Exchange. Puis-je utiliser cette fonctionnalité?

Les utilisateurs locaux peuvent envoyer des messages chiffrés à l'aide de règles de flux de messagerie Exchange Online. Pour ce faire, vous devez acheminer le courrier électronique via Exchange Online. Pour plus d'informations, voir [partie 2: configurer la messagerie pour qu'elle circule depuis votre serveur de messagerie vers Office 365](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail#part-2-configure-mail-to-flow-from-your-email-server-to-office-365).
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a>Quel client de messagerie dois-je utiliser pour créer un message chiffré OME? Quelles sont les applications prises en charge pour l'envoi de messages protégés?

Vous pouvez créer des messages protégés à partir d'Outlook 2016 et Outlook 2013 pour PC et Mac, et à partir d'Outlook sur le Web.
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a>Quels sont les clients de messagerie pris en charge pour lire et répondre aux messages électroniques protégés?

Vous pouvez lire et répondre à Outlook pour PC et Mac (2013 et 2016), Outlook sur le Web et Outlook Mobile (Android et iOS) si vous êtes un utilisateur d'Office 365. Vous pouvez également utiliser le client de messagerie natif iOS si votre organisation l'autorise. Si vous êtes un utilisateur non-Office 365, vous pouvez lire et répondre à des messages chiffrés sur le Web via votre navigateur Web.
  
## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a>Quels types de fichiers sont pris en charge en tant que pièces jointes dans les courriels protégés? Les pièces jointes héritent-elles des stratégies de protection associées aux courriers électroniques protégés?

Vous pouvez attacher n'importe quel type de fichier à un message protégé, mais les stratégies de protection ne sont appliquées qu'aux formats de fichier mentionnés [ici](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types). 
  
Si un format de fichier est pris en charge, par exemple un fichier Word, Excel ou PowerPoint, le fichier est toujours protégé, même après le téléchargement de la pièce jointe par le destinataire. Par exemple, si une pièce jointe est protégée par ne pas transférer, et que le destinataire d'origine télécharge et transfère la pièce jointe à un nouveau destinataire, le nouveau destinataire ne pourra pas ouvrir le fichier protégé.
  
## <a name="are-pdf-file-attachments-supported"></a>Les pièces jointes aux fichiers PDF sont-elles prises en charge?

Si vous joignez un fichier PDF à un message protégé, le message lui-même est protégé, mais aucune protection supplémentaire n'est appliquée au fichier PDF une fois que le destinataire l'a reçu. Cela signifie que le destinataire peut enregistrer sous, transférer, copier et imprimer le fichier PDF.
  
## <a name="are-onedrive-for-business-attachments-supported"></a>Les pièces jointes OneDrive entreprise sont-elles prises en charge?

Pas encore. Les pièces jointes OneDrive entreprise ne sont pas prises en charge et les utilisateurs finaux ne peuvent pas chiffrer un message qui contient une pièce jointe de OneDrive entreprise sur le Cloud.
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a>Puis-je chiffrer automatiquement les messages en configurant des stratégies?

OK. Utilisez des règles de flux de messagerie dans Exchange Online pour chiffrer automatiquement un message en fonction de certaines conditions. Par exemple, vous pouvez créer des stratégies basées sur l'ID de destinataire, le domaine du destinataire ou le contenu dans le corps ou l'objet du message. Consultez la rubrique [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365.](define-mail-flow-rules-to-encrypt-email.md)
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a>Puis-je chiffrer automatiquement les messages en configurant des stratégies de protection contre la perte de &amp; données (DLP) via le centre de sécurité conformité?

OK! Vous pouvez configurer des règles de flux de messagerie dans Exchange Online ou à l'aide de &amp; DLP dans le centre de sécurité conformité.
  
## <a name="can-i-open-encrypted-messages-sent-to-a-shared-mailbox"></a>Puis-je ouvrir des messages chiffrés envoyés à une boîte aux lettres partagée?

Les messages actuellement chiffrés ne sont pas pris en charge pour une boîte aux lettres partagée.

## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a>Puis-je personnaliser les messages chiffrés avec mon entreprise?

OK! Pour plus d'informations sur la personnalisation des messages électroniques et sur le portail OME, reportez-vous à la rubrique ajouter la marque de votre organisation à vos messages chiffrés. Consultez la rubrique [Ajouter la marque de votre organisation à vos messages chiffrés.](add-your-organization-brand-to-encrypted-messages.md)
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a>Existe-t-il des fonctionnalités de création de rapports ou des informations pour les messages électroniques chiffrés?

Pas pour le moment, mais bientôt disponible.
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a>Puis-je utiliser le chiffrement de messages avec des fonctionnalités de conformité telles que eDiscovery?

OK. Tous les messages électroniques chiffrés sont détectables par les fonctionnalités de conformité d'Office 365.
  

