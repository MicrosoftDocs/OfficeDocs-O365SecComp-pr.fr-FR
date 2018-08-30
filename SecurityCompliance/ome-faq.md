---
title: FAQ sur le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/23/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0432dce9-d9b6-4e73-8a13-4a932eb0081e
description: Vous avez une question sur le fonctionnement des nouvelles fonctionnalités de protection de message dans Office 365 ? Recherchez une réponse ici.
ms.openlocfilehash: d435642d8ea98d37a58b28b55c9c1e68c746600c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559249"
---
# <a name="office-365-message-encryption-faq"></a>FAQ sur le chiffrement de messages Office 365

Vous avez une question sur le fonctionnement des nouvelles fonctionnalités de protection de message dans Office 365 ? Recherchez une réponse ici. En outre, jetez un œil à [Forum aux questions sur la protection de données dans Azure la Protection des informations](https://docs.microsoft.com/information-protection/get-started/faqs-rms) pour obtenir des réponses aux questions sur le service de protection des données, Azure Rights Management, dans la Protection des informations Azure. 
  
## <a name="what-is-office-365-message-encryption-ome"></a>Nouveautés d’Office 365 Message Encryption (OME) ?

OME combine de cryptage de messages et les fonctionnalités de gestion des droits. Protection des informations Azure sont équipées des fonctionnalités de gestion des droits.
  
## <a name="who-can-use-ome"></a>Qui peut utiliser OME ?

Vous pouvez utiliser les nouvelles fonctionnalités pour OME dans les conditions suivantes :
  
- Si vous avez jamais configuré OME ou IRM pour Exchange Online dans Office 365.
    
- Si vous avez configuré OME et IRM, vous pouvez utiliser ces étapes si vous utilisez le service de Azure Rights Management à partir de la Protection des informations Azure.
    
- Si vous utilisez Exchange Online avec Active Directory Rights Management Services AD RMS, vous ne pouvez pas activer ces nouvelles fonctionnalités immédiatement. Au lieu de cela, vous devez [migrer AD RMS pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) tout d’abord. Lorsque vous avez terminé la migration, vous pouvez configurer correctement OME. 
    
    Si vous choisissez de continuer à utiliser sur site AD RMS avec Exchange Online au lieu de la migration vers Azure la Protection des informations, vous ne pourrez pas utiliser ces nouvelles fonctionnalités.
    
## <a name="what-subscriptions-do-i-need-to-use-the-new-ome-capabilities"></a>Les abonnements ai-je besoin pour utiliser les nouvelles fonctionnalités OME ?

Pour utiliser les nouvelles fonctionnalités OME, vous devez parmi les plans suivants :
  
- Office 365, le chiffrement de messages est proposé dans le cadre d’Office 365 E3 et E5, Microsoft E3 et E5, Office 365 A1, A3 et A5 et Office 365 G3 et G5. Clients n’avez pas besoin de licences supplémentaires afin de recevoir les nouvelles fonctionnalités de protection par la Protection des informations Azure. 
    
- Vous pouvez également ajouter des plans recevoir les nouvelles fonctionnalités d’Office 365 Message Encryption Azure informations Protection Plan 1 à la suivante : Exchange Online Plan 1, Exchange Online Plan 2, Office 365 F1, Office 365 entreprise Essentials, Office 365 entreprise Premium, ou Office 365 entreprise E1.
    
- Chaque utilisateur bénéficiant de chiffrement de messages Office 365 doit être sous licence pour être couverts par la fonctionnalité.
    
- Pour obtenir la liste complète consultez les [descriptions du service Exchange Online](https://technet.microsoft.com/library/exchange-online-service-description.aspx) pour Office 365 Message Encryption. 
    
## <a name="can-i-use-exchange-online-with-bring-your-own-key-byok-in-azure-information-protection"></a>Puis-je utiliser Exchange Online avec mettre votre propre clé (BYOK) dans la Protection des informations Azure ?

Oui ! Microsoft recommande que vous effectuez les étapes pour configurer BYOK avant de configurer OME.
  
Pour plus d’informations sur BYOK, voir [planification et l’implémentation de votre clé de client Azure la Protection des informations](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).
  
## <a name="do-ome-and-byok-with-azure-information-protection-change-microsofts-approach-to-third-party-data-requests-such-as-subpoenas"></a>OME et BYOK avec la Protection des informations Azure modifient l’approche de Microsoft pour les demandes de données tiers tels que comparaître ?

Non. OME et l’option pour fournir et contrôler vos propres clés de chiffrement, appelées BYOK, à partir de la Protection des informations Azure ne sont pas conçus pour répondre à comparaître de l’application de la réglementation. OME, avec BYOK pour la Protection des informations Azure, a été conçu pour les clients de respect de la réglementation. Microsoft prend très au sérieux tiers demandes de données du client. En tant qu’un fournisseur de services en nuage, nous toujours représenter la confidentialité des données du client. En cas de nous obtenons aux citations à comparaître, nous toujours tenter de rediriger le tiers au client afin d’obtenir les informations. (Veuillez lire le blog de Brad Smith : [protéger les données de clients de gouvernement snooping](https://blogs.microsoft.com/blog/2013/12/04/protecting-customer-data-from-government-snooping/)). Nous publier régulièrement des informations détaillées de la demande de que réception. Pour plus d’informations concernant les demandes de données tierce, consultez [réponse aux administrations et les demandes de l’application de la réglementation pour accéder aux données client](https://www.microsoft.com/en-us/trustcenter/privacy/govt-requests-for-data) sur le Center Trust Microsoft. En outre, voir « Divulgation des données du client » dans les [Termes du contrat de Services en ligne (OST)](https://www.microsoft.com/en-us/Licensing/product-licensing/products.aspx).
  
## <a name="how-is-this-feature-related-to-legacy-office-365-message-encryption-ome-and-information-rights-management-irm-features"></a>Comment cette fonctionnalité est liée aux fonctionnalités d’Office 365 Message Encryption (OME) et Information Rights Management (IRM) héritées ?

Nouvelles fonctionnalités pour le chiffrement de messages Office 365 sont une évolution du IRM existant et les solutions OME héritées. Le tableau suivant fournit plus de détails.
  
**Comparaison des OME hérité, IRM et nouvelles fonctionnalités OME**

|**Fonctionnalité**|**Versions antérieures d’OME**|**IRM**|**Nouvelles fonctionnalités de OME**|
|:-----|:-----|:-----|:-----|
|**Envoyer un message électronique chiffré**|Uniquement par le biais de règles de flux de messagerie Exchange|Utilisateur final initiée à partir d’Outlook pour PC, Outlook pour Mac ou Outlook sur le web ; ou Exchange par le biais de règles de flux de messagerie.|Utilisateur final initiée à partir d’Outlook pour PC, Outlook pour Mac ou Outlook sur le web ; ou par le biais de règles de flux de messagerie|
|**Gestion des droits**|-|Effectuez l’option pas transférer et modèles personnalisés|Effectuez l’option pas transférer, option chiffrer uniquement, modèles personnalisés et par défaut|
|**Prise en charge du type de destinataire**|Destinataires externes|Destinataires internes|Destinataires internes et externes|
|**Expérience de destinataire**|Destinataires externes a reçu un message HTML qu’ils téléchargement et ouvert dans un navigateur ou application mobile.|Les destinataires internes reçu uniquement messagerie chiffrée dans Outlook pour PC, Outlook pour Mac et Outlook sur le web.|Destinataires internes et externes recevoir du courrier électronique dans Outlook pour PC, Outlook pour Mac, Outlook sur le web, Outlook pour Android et Outlook pour iOS, ou via un portail web, quel que soit leur soient ou non dans la même organisation Office 365 ou dans n’importe quel Office 365 organisation. Le portail OME ne requiert aucun téléchargement distinct.|
|**Alliance de prise en charge votre propre clé**|Non disponible|Non disponible| BYOK pris en charge|

## <a name="how-do-i-enable-the-new-ome-capabilities-for-my-organization"></a>Comment activer les nouvelles fonctionnalités OME pour mon organisation ?

Consultez la rubrique [configurer de nouvelles fonctionnalités d’Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md).
  
## <a name="will-the-previous-version-of-ome-be-deprecated"></a>Sera déconseillée la version précédente d’OME ?

Vous pouvez toujours utiliser la version précédente d’OME, il ne sera pas déconseillé pour l’instant. Toutefois, nous conseillons vivement aux organisations d’utiliser la solution OME nouvelle et améliorée. Les clients qui n’ont pas déjà déployé OME ne pouvez pas configurer un nouveau déploiement de la version précédente d’OME.
  
## <a name="my-organization-uses-active-directory-rights-management-can-i-use-this-functionality"></a>Mon organisation utilise Active Directory Rights Management, puis-je utiliser cette fonctionnalité ?

Non. Si vous utilisez Exchange Online avec Active Directory Rights Management Services AD RMS, vous ne pouvez pas activer ces nouvelles fonctionnalités immédiatement. Au lieu de cela, vous devez [migrer AD RMS pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms) tout d’abord. 
  
## <a name="my-organization-has-an-exchange-hybrid-deployment-can-i-use-this-feature"></a>Mon organisation possède un déploiement Exchange hybride. Puis-je utiliser cette fonctionnalité ?

Les utilisateurs peuvent envoyer des messages chiffrés à l’aide de règles de flux de messagerie Exchange Online sur site. Pour ce faire, vous devez router le courrier électronique via Exchange Online.
  
## <a name="what-email-client-do-i-need-to-use-in-order-to-create-an-ome-encrypted-message-what-applications-are-supported-for-sending-protected-messages"></a>Le client de messagerie dois-je utiliser afin de créer un message chiffré OME ? Quelles applications sont pris en charge pour l’envoi de messages protégés ?

Vous pouvez créer des messages protégés à partir de 2016 Outlook et Outlook 2013 pour PC et Mac et à partir d’Outlook sur le web.
  
## <a name="what-email-clients-are-supported-to-read-and-reply-to-protected-emails"></a>Les clients de messagerie sont prises en charge pour lire et répondre aux messages électroniques protégés ?

Vous pouvez lire et répondre à partir d’Outlook pour PC et Mac (2013 et 2016), Outlook sur le web et Outlook mobile (Android et iOS) si vous êtes un utilisateur d’Office 365. Vous pouvez également utiliser le client de messagerie natifs iOS si votre organisation l’autorise. Si vous êtes un utilisateur d’Office 365, vous pouvez lire et répondre aux messages chiffrés sur le site web par le biais de votre navigateur web.
  
## <a name="what-file-types-are-supported-as-attachments-in-protected-emails-do-attachments-inherit-the-protection-policies-associated-with-protected-emails"></a>Quels types de fichiers sont pris en charge en tant que pièces jointes dans les messages électroniques protégés ? Pièces jointes héritent des stratégies de protection associés avec les messages électroniques protégés ?

Vous pouvez attacher tout type de fichier à un message protégé, mais les stratégies de protection sont appliquées sur le fichier formats mentionné [ici](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide-file-types). 
  
Si un format de fichier est pris en charge, tel qu’un fichier Word, Excel et PowerPoint, le fichier est toujours protégé, même une fois que la pièce jointe a été téléchargée par le destinataire. Par exemple, si une pièce jointe est protégée par ne pas transférer et le destinataire d’origine télécharge et transfère la pièce jointe à un destinataire, le nouveau destinataire ne sera pas en mesure d’ouvrir le fichier protégé.
  
## <a name="are-pdf-file-attachments-supported"></a>Pièces jointes PDF sont pris en charge ?

Si vous joignez un fichier PDF à un message protégé, le message sera protégé, mais aucune protection supplémentaire ne sera appliquée au fichier PDF une fois que le destinataire a reçues. Cela signifie que les destinataire peuvent enregistrer sous, transférer, copier et imprimer le fichier PDF.
  
## <a name="are-onedrive-for-business-attachments-supported"></a>Sont OneDrive pour les pièces jointes métiers pris en charge ?

Pas encore. OneDrive pour les pièces jointes de l’entreprise ne sont pas prises en charge et les utilisateurs finaux ne peuvent pas chiffrer un message contenant un pièce jointe Business OneDrive dans le nuage.
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies"></a>Puis-je chiffrer automatiquement des messages en définissant des stratégies ?

Oui. Utiliser les règles de flux de messagerie dans Exchange Online pour chiffrer automatiquement les messages en fonction de certaines conditions. Par exemple, vous pouvez créer des stratégies basées sur le destinataire, ID de domaine du destinataire, ou sur le contenu dans le corps ou l’objet du message. Voir [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365.](define-mail-flow-rules-to-encrypt-email.md)
  
## <a name="can-i-automatically-encrypt-messages-by-setting-up-policies-in-data-loss-prevention-dlp-through-the-security-amp-compliance-center"></a>Je peux automatiquement chiffrer les messages en définissant des stratégies dans Data Loss Prevention (DLP) par le biais de la sécurité &amp; centre de conformité ?

Actuellement vous pouvez uniquement définir des règles de flux de messagerie dans Exchange Online. Chiffrement n’est actuellement pas pris en charge dans DLP par le biais de la sécurité &amp; centre de conformité.
  
## <a name="can-i-customize-encrypted-messages-with-my-company-branding"></a>Puis-je personnaliser les messages chiffrés avec personnalisation de mon entreprise ?

Oui ! Pour plus d’informations sur la personnalisation des messages électroniques et le portail OME, consultez la rubrique Ajouter la marque de votre organisation à vos messages chiffrés. Voir [Ajouter marque de votre organisation à vos messages chiffrés.](add-your-organization-brand-to-encrypted-messages.md)
  
## <a name="are-there-any-reporting-capabilities-or-insights-for-encrypted-emails"></a>Existe-t-il des rapports insights pour les messages électroniques chiffrés ou fonctionnalités ?

Pas à ce stade, mais seront prochainement disponibles.
  
## <a name="can-i-use-message-encryption-with-compliance-features-such-as-ediscovery"></a>Puis-je utiliser le chiffrement de messages avec des fonctionnalités de conformité telles que la découverte électronique ?

Oui. Tous les messages électroniques chiffrés sont accessibles aux fonctionnalités de conformité d’Office 365.
  

