---
title: Chiffrement dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
ms.collection:
- M365-security-compliance
- Strat_O365_IP
description: Avec Office 365, votre contenu est chiffré au repos et en transit, en utilisant le chiffrement, les protocoles et les technologies les plus puissants disponibles. Obtenez une vue d'ensemble du chiffrement dans Office 365.
ms.openlocfilehash: 7a73d3d3b24e28f8795ec93ac05dbc383b525906
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31026325"
---
# <a name="encryption-in-office-365"></a>Chiffrement dans Office 365

Le chiffrement est une partie importante de vos stratégies de protection des informations et de protection des informations. Lisez cet article pour obtenir une vue d'ensemble du chiffrement utilisé pour toutes les versions d'Office 365 et obtenir de l'aide sur les tâches de chiffrement, de la configuration du chiffrement de votre organisation à la protection par mot de passe des documents Office.
  
- Si vous recherchez des informations sur les certificats et les technologies telles que TLS, consultez les [Détails de référence technique sur le chiffrement dans Office 365](technical-reference-details-about-encryption.md).

- Si vous recherchez des informations sur la façon de configurer ou de configurer le chiffrement pour votre organisation, consultez la rubrique [configurer le chiffrement dans Office 365 Enterprise](set-up-encryption.md).

## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>Qu'est-ce que le chiffrement et comment fonctionne-t-il dans Office 365?

À un niveau élevé, le chiffrement est le processus de codage de vos données (appelé texte brut) en texte chiffré qui ne peut pas être utilisé par des personnes ou des ordinateurs sauf et jusqu'à ce que le texte chiffré soit déchiffré. Le déChiffrement nécessite une clé de chiffrement dont les utilisateurs autorisés disposent uniquement. Le chiffrement permet de garantir que seuls les destinataires autorisés peuvent déchiffrer votre contenu, comme les messages électroniques et les fichiers.
  
Le chiffrement n'empêche pas le contenu, comme les fichiers, les messages électroniques, les entrées de calendrier et ainsi de suite, de rencontrer des mauvaises mains. Le chiffrement fait partie d'une stratégie de protection des informations plus importante pour votre organisation. En utilisant le chiffrement, vous pouvez vous assurer que seuls les personnes qui doivent être en mesure d'utiliser des données chiffrées sont en mesure de le faire.
  
Vous pouvez avoir plusieurs couches de chiffrement en même temps. Par exemple, vous pouvez chiffrer les messages électroniques, ainsi que les canaux de communication via lesquels votre courrier électronique transite. Avec Office 365, vos données sont chiffrées au repos et en transit à l'aide de plusieurs protocoles de chiffrement forts, ainsi que des technologies qui incluent TLS/SSL (Transport Layer Security/Secure Sockets Layer), IPSec (Internet Protocol Security) et le chiffrement avancé Standard (AES).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Chiffrement des données au repos et des données en transit

 **Des exemples de données dans Rest incluent des** fichiers qui ont été téléchargés dans une bibliothèque SharePoint, des données Project Online, des documents qui ont été téléchargés dans une réunion Skype entreprise, des messages électroniques et des pièces jointes stockés dans des dossiers dans votre Office 365 boîte aux lettres et fichiers téléchargés vers OneDrive entreprise. 
  
 Parmi les **exemples de données en transit** , citons les messages électroniques qui sont en cours de remise, ou les conversations qui ont lieu lors d'une réunion en ligne. Dans Office 365, les données sont en transit chaque fois que l'appareil d'un utilisateur communique avec un serveur Office 365, ou lorsqu'un serveur Office 365 communique avec un autre serveur. 
  
Avec Office 365, vous pouvez utiliser plusieurs couches et types de chiffrement pour sécuriser vos données. Le tableau suivant contient des exemples, avec des liens vers des informations supplémentaires.
  
|**Types de contenu**|**Technologies de chiffrement**|**Ressources pour en savoir plus**|
|:-----|:-----|:-----|
|Fichiers sur un appareil. Cela peut inclure les messages électroniques enregistrés dans un dossier, les documents Office enregistrés sur un ordinateur, une tablette ou un téléphone, ou les données enregistrées dans le Cloud Microsoft.  <br/> |BitLocker dans les centres de connaissances Microsoft. BitLocker peut également être utilisé sur les ordinateurs clients, tels que les ordinateurs Windows et les tablettes  <br/> Gestionnaire de clés distribuées (DKM) dans les centres de distribution Microsoft  <br/> Clé client pour Office 365  <br/> |[Centre informatique Windows: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Centre de gestion de la confidentialité Microsoft: chiffrement](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Série de contrôles de sécurité du Cloud: chiffrement des données au repos](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online](exchange-online-secures-email-secrets.md) <br/> [Contrôle de vos données dans Office 365 à l'aide de la Clé client](controlling-your-data-using-customer-key.md). <br/> |
|Fichiers en transit entre les utilisateurs. Cela peut inclure des documents Office ou des éléments de liste SharePoint partagés entre les utilisateurs.  <br/> |TLS pour les fichiers en transit  <br/> |[Chiffrement de données dans OneDrive Entreprise et SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Skype entreprise Online: sécurité et archivage](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|Courrier électronique en transit entre les destinataires. Cela inclut le courrier électronique hébergé par Exchange Online.  <br/> |Chiffrement de messages Office 365 avec Azure Rights Management, S/MIME et TLS pour le courrier électronique en transit  <br/> |[Chiffrement de messages Office 365 (OME)](ome.md) <br/> [Chiffrement du courrier électronique dans Office 365](email-encryption.md) <br/> [Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |

## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>Qu'en est-il si j'ai besoin de plus de contrôle sur le chiffrement pour répondre aux exigences de sécurité et de conformité?

Outre les solutions gérées par Microsoft de chiffrement de volume, de chiffrement de fichiers et de chiffrement de boîtes aux lettres dans Office 365, les options gérées par le client peuvent être utilisées pour répondre aux exigences de conformité et de sécurité plus strictes. De telles solutions utilisent Azure Rights Management (Azure RMS) avec Office 365.
  
Pour en savoir plus, consultez les ressources suivantes:
  
- [Qu'est-ce que Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)

- [Azure Rights Management dans le Centre d’administration Office 365](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)

- [Set up Information Rights Management (IRM) in SharePoint admin center](set-up-irm-in-sp-admin-center.md)

## <a name="how-do-i"></a>Procédures

|**Pour effectuer cette tâche**|**Voir les ressources suivantes**|
|:-----|:-----|
|Configurer le chiffrement pour mon organisation  <br/> |[Configurer le chiffrement dans Office 365 Entreprise](set-up-encryption.md) <br/> |
|Afficher des détails sur les certificats, les technologies et les suites de chiffrement TLS dans Office 365  <br/> |[Détails techniques sur le chiffrement dans Office 365](technical-reference-details-about-encryption.md) <br/> |
|Utiliser des messages chiffrés sur un appareil mobile  <br/> |[Afficher des messages chiffrés sur votre appareil Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [Afficher des messages chiffrés sur votre iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|Chiffrer un document à l'aide de la protection par mot de passe  <br/><br/>  Actuellement, la protection par mot de passe n'est pas prise en charge dans Office Online. Utiliser les versions de bureau de Word, Excel et PowerPoint pour la protection par mot de passe.           |[Ajouter ou supprimer la protection dans votre document, classeur ou présentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Choisissez une section **Ajouter une protection** , puis reportez-vous **à chiffrer avec mot de passe** )  <br/> |
|Supprimer le chiffrement d'un document  <br/> |[Ajouter ou supprimer la protection dans votre document, classeur ou présentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Choisissez une section **protection contre la suppression** , puis voir supprimer le chiffrement du **mot de passe** )  <br/> |

## <a name="related-topics"></a>Voir aussi

[Planifier les fonctionnalités de protection des informations et de sécurité d'Office 365](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[Sécurité et conformité dans Office 365 pour les entreprises-aide de l'administrateur](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)
  

