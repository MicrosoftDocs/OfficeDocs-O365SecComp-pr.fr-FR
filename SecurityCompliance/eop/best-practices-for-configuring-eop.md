---
title: Meilleures pratiques de configuration d’EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: faf1efd1-3b0c-411a-804d-17f37292eac0
description: Pour vous donner un maximum de chances de succès et éviter les erreurs courantes de configuration, suivez ces recommandations relatives aux meilleures pratiques pour Exchange Online Protection (EOP).
ms.openlocfilehash: c60e3d62cc758a75f85d6cb149c8e13492cad35c
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150286"
---
# <a name="best-practices-for-configuring-eop"></a>Meilleures pratiques de configuration d’EOP
  
Pour vous donner un maximum de chances de succès et éviter les erreurs courantes de configuration, suivez ces recommandations relatives aux meilleures pratiques pour Exchange Online Protection (EOP). En règle générale, nous vous recommandons d'utiliser les paramètres de configuration par défaut. Cette rubrique part de l'hypothèse que vous avez déjà effectué le processus de configuration. Si vous n'avez pas encore configuré EOP, consultez la rubrique [Configurer votre service EOP](set-up-your-eop-service.md).
  
## <a name="use-a-test-domain"></a>Utiliser un domaine de test

Nous vous recommandons d’utiliser un domaine, un sous-domaine ou un domaine au volume restreint de test pour tester les fonctionnalités des services avant de les implémenter sur des domaines de production au volume plus important.
  
## <a name="synchronize-recipients"></a>Synchronisation des destinataires

Si votre organisation dispose de comptes d'utilisateur dans un environnement Active Directory local, vous pouvez synchroniser ces comptes avec Azure Active Directory dans le cloud. L'utilisation de la synchronisation d'annuaires est recommandée. Pour en savoir plus sur les avantages de la synchronisation d'annuaires et pour connaître les étapes de sa configuration, voir [Gestion des utilisateurs de messagerie dans EOP](manage-mail-users-in-eop.md).
  
## <a name="spf-record-customization-to-help-prevent-spoofing"></a>Personnalisation d’enregistrement SPF pour éviter toute usurpation

Lors de la configuration d'EOP, vous avez ajouté à vos enregistrements DNS un enregistrement SPF (sender policy framework) pour EOP. L'enregistrement SPF permet d'empêcher les falsifications d'adresse. Pour plus d’informations sur la façon dont un enregistrement SPF empêche l’usurpation d’identité et sur la façon d’ajouter vos adresses IP locales à l’enregistrement SPF, consultez la rubrique [set up SPF in Office 365 pour éviter l’usurpation](../set-up-spf-in-office-365-to-help-prevent-spoofing.md). 
  
## <a name="set-anti-spam-options"></a>Définition des options anti-courrier indésirable

Gérez vos paramètres de filtre de connexion en ajoutant des adresses IP aux listes d'adresses IP autorisées et d'adresses IP bloquées, et en sélectionnant l'option **Activer la liste fiable**, qui doit réduire le nombre de faux positifs (courrier valide classé comme courrier indésirable) que vous recevez. Pour plus d’informations, consultez [la rubrique Configure the connection filter Policy](../configure-the-connection-filter-policy.md). Pour plus d'informations sur d'autres paramètres de courrier indésirable applicables à l'ensemble de l'organisation, consultez les rubriques relatives aux procédures permettant de [s'assurer qu'un message n'est pas marqué comme courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=534224) et de [bloquer le courrier indésirable avec le filtre anti-courrier indésirable d'Office 365 pour éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225). Ces procédures sont utiles si vous avez un contrôle de niveau administrateur et que vous souhaitez éviter les faux positifs ou les faux négatifs.
  
Gérez vos filtres de contenu en examinant et éventuellement en modifiant les paramètres par défaut. Par exemple, vous pouvez modifier l’action qui se produit sur les messages détectés par courrier indésirable. Si vous souhaitez adopter une approche agressive pour le filtrage du courrier indésirable, vous pouvez configurer les options de filtrage avancé du courrier indésirable. Nous vous recommandons de tester ces options avant de les implémenter dans votre environnement de production (en les activant), il est recommandé que les organisations concernées par le hameçonnage activent l' **enregistrement SPF: option Hard Fail** . Pour plus d’informations, consultez [la rubrique configurer vos stratégies de filtrage du courrier](../configure-your-spam-filter-policies.md) indésirable et [options de filtrage avancé](../advanced-spam-filtering-asf-options.md)
  
> [!IMPORTANT]
> Si vous utilisez l’action de filtrage de contenu par défaut, **déplacer le message vers le dossier**courrier indésirable, afin de vous assurer que cette action fonctionnera avec les boîtes aux lettres locales, vous devez configurer des règles de flux de messagerie Exchange (également appelées règles de transport) sur votre site local. serveurs permettant de détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, voir [Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
Nous vous recommandons de consulter le [Forum aux questions sur la protection](../anti-spam-protection-faq.md)contre le courrier indésirable, y compris la section méthodes recommandées pour la réception des messages sortants, qui vous permettront de garantir la remise de votre courrier sortant.
  
À des fins d'analyse, vous pouvez soumettre à Microsoft des faux négatifs (programmes malveillants) et des faux positifs (programmes non malveillants) de plusieurs façons. Pour plus d’informations, consultez la rubrique soumettre des messages de courrier indésirable, des courriers indésirables [et des tentatives de hameçonnage à Microsoft pour analyse](../submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).
  
## <a name="set-anti-malware-options"></a>Définition des options anti-programme malveillant

Consultez et réglez précisément vos paramètres de filtrage des programmes malveillants dans le Centre d'administration Exchange (CAE). Pour plus d’informations, consultez la rubrique [configure anti-malware Policies](../configure-anti-malware-policies.md). Nous vous recommandons également de lire les autres questions fréquemment posées et les réponses relatives à la protection contre les programmes malveillants dans notre Forum aux questions sur la [protection anti-programme malveillant ](../anti-malware-protection-faq-eop.md).
  
Si vous êtes préoccupé par le fait que les fichiers exécutables peuvent contenir des programmes malveillants, vous pouvez créer une règle de flux de messagerie Exchange qui bloque toute pièce jointe comportant un contenu exécutable. Suivez les étapes de [réduction des menaces de programmes malveillants via le blocage des pièces jointes dans Exchange Online Protection](https://support.microsoft.com/kb/2959596) pour bloquer les types de fichiers mentionnés dans [utiliser des règles de flux de messagerie pour inspecter les pièces jointes des messages dans Exchange Online](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection).
  
Vous pouvez utiliser le filtre de types de pièces jointes courantes dans le CAE. Sélectionnez **protection** \> **filtres anti-programme malveillant**. Vous pouvez créer une règle de flux de messagerie qui bloque toute pièce jointe de courrier électronique dont le contenu est exécutable. 
  
Pour renforcer la protection, nous vous recommandons également de bloquer tout ou partie des extensions suivantes à l'aide de règles de flux de messagerie : ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh. Pour ce faire, vous pouvez utiliser la condition **Toute extension de fichier joint contient ces mots**. 
  
Les administrateurs et les utilisateurs finaux peuvent soumettre un programme malveillant ayant franchi les filtres ou un fichier qu'ils estiment avoir été identifié à tort comme programme malveillant en l'envoyant à Microsoft pour analyse. Pour plus d'informations, voir [Submitting malware and non-malware to Microsoft for analysis](../submitting-malware-and-non-malware-to-microsoft-for-analysis.md).
  
## <a name="create-mail-flow-rules"></a>Création de règles de flux de messagerie

Créez des règles de flux de messagerie (également appelées règles de transport) ou des filtres personnalisés pour répondre aux besoins de votre entreprise.
  
Lorsque vous déployez une nouvelle règle en production, commencez par sélectionner l'un des modes test pour voir son effet. Lorsque vous estimez que la règle fonctionne de la manière souhaitée, modifiez son mode d'effet en le définissant sur **Appliquer**.
  
Lors du déploiement d'une nouvelle règle, songez à ajouter l'action supplémentaire **Générer un rapport d'incident** pour contrôler son action. 
  
Si vous êtes dans une configuration de déploiement hybride, une partie de votre organisation étant locale et une autre dans Office 365, vous pouvez créer des règles qui s'appliquent à l'organisation toute entière. Pour ce faire, utilisez des conditions disponibles tant localement que dans Office 365. Si la plupart des conditions sont disponibles dans les deux déploiements, un petit ensemble d'entre elles est spécifique d'un scénario de déploiement particulier. Pour plus d’informations, consultez la rubrique [règles de flux de messagerie (règles de transport) dans Exchange Online](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx).
  
Pour vérifier les pièces jointes de courriers électroniques en transit au sein de votre organisation, vous pouvez mettre en place des règles de flux de messagerie. Prenez ensuite des mesures sur les messages qui ont été inspectés en fonction du contenu ou des caractéristiques de ces pièces jointes. Pour plus d'informations, consultez la rubrique [Use mail flow rules to inspect message attachments](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx).
  
### <a name="phishing-and-spoofing-prevention"></a>Lutte contre les attaques par hameçonnage et l’usurpation d’identité

Vous pouvez améliorer la protection anti-hameçonnage en détectant quand des informations personnelles quittent l’organisation dans un e-mail. Par exemple, vous pouvez utiliser les expressions régulières suivantes dans des règles de flux de messagerie pour détecter la transmission de données ou d’informations financières personnelles susceptibles de compromettre la confidentialité :
  
- \d\d\d\d\s\d\d\d\d\s\d\d\d\d\s\d\d\d\d (Visa MasterCard)
    
- \d\d\d\d\s\d\d\d\d\d\d\s\d\d\d\d\d (American Express)
    
- \d\d\d\d\d\d\d\d\d\d\d\d\d\d\d\d (n'importe quel numéro à 16 chiffres)
    
- \d\d\d\-\d\d\-\d\d\d\d (numéros de sécurité sociale)
    
Il est également possible d'empêcher toute attaque par courrier indésirable et hameçonnage en bloquant les courriers électroniques malveillants entrants qui sembleraient avoir été envoyés depuis votre propre domaine. Par exemple, vous pouvez créer une règle de flux de messagerie rejetant les messages envoyés depuis le nom de domaine de votre société vers le même nom de domaine afin de bloquer ce type d'expéditeur factice.
  
> [!CAUTION]
> Nous vous recommandons de ne créer cette règle de rejet que lorsque vous êtes certain qu’aucun courrier légitime transmis depuis votre nom de domaine n’est envoyé via Internet à votre serveur de messagerie. Ce peut être le cas lorsqu’un message est envoyé par un utilisateur de votre organisation à un destinataire externe, puis retransmis à un autre destinataire au sein de votre organisation. 
  
### <a name="extension-blocking"></a>Blocage des extensions

Si vous êtes préoccupé par le fait que les fichiers exécutables peuvent contenir des programmes malveillants, vous pouvez configurer des stratégies de blocage des programmes malveillants qui bloquent toute pièce jointe comportant un contenu exécutable. Suivez les étapes décrites dans [configure anti-malware Policies](../configure-anti-malware-policies.md).
  
Pour renforcer la protection, nous vous recommandons également de bloquer tout ou partie des extensions suivantes : ade, adp, ani, bas, bat, chm, cmd, com, cpl, crt, hlp, ht, hta, inf, ins, isp, job, js, jse, lnk, mda, mdb, mde, mdz, msc, msi, msp, mst, pcd, reg, scr, sct, shs, url, vb, vbe, vbs, wsc, wsf, wsh.
  
## <a name="reporting-and-troubleshooting"></a>Génération de rapports et dépannage

Résoudre les problèmes et tendances généraux à l’aide des rapports dans le centre d’administration. Pour trouver des données concernant un point précis d'un message, utilisez l'outil de suivi des messages. Pour plus d'informations sur la génération de rapports, consultez la rubrique [Création de rapports et suivi des messages dans Exchange Online Protection](reporting-and-message-trace-in-exchange-online-protection.md). Pour plus d'informations sur l'outil de suivi des messages, consultez la rubrique [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx).
  
## <a name="for-more-information"></a>Pour plus d’informations

[Forum Aux Questions d'ordre général concernant Exchange Online Protection (EOP)](eop-general-faq.md)
  
[Aide et support pour EOP](help-and-support-for-eop.md)
  
[Comment s'assurer qu'un message n'est pas marqué comme du courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

