---
title: Chiffrement dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/15/2019
audience: Admin
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
description: Avec Office 365, votre contenu est chiffré au repos et en transit avec le chiffrement, les protocoles et les technologies les plus puissants disponibles. Obtenez une vue d’ensemble du chiffrement dans Office 365.
ms.openlocfilehash: 1dd31990e4a284c81ce9fa8b2aced45b8a06a0c6
ms.sourcegitcommit: 01f827d7a3fe6d982924cabb0bcc8d6a19ecc57c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/16/2019
ms.locfileid: "36436294"
---
# <a name="encryption-in-office-365"></a>Chiffrement dans Office 365

Le chiffrement est une partie importante de votre stratégie de protection des informations et de protection des informations. Cet article fournit une vue d’ensemble du chiffrement pour Office 365. Obtenez de l’aide sur les tâches de chiffrement comme la configuration du chiffrement pour votre organisation et la protection par mot de passe des documents Office.
  
- Pour plus d’informations sur les certificats et les technologies, tels que TLS, voir informations [de référence technique sur le chiffrement dans Office 365](technical-reference-details-about-encryption.md).

- Pour plus d’informations sur la configuration ou la configuration du chiffrement pour votre organisation, consultez la rubrique [configurer le chiffrement dans Office 365 Enterprise](set-up-encryption.md).

## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>Qu’est-ce que le chiffrement et comment fonctionne-t-il dans Office 365?

Le processus de chiffrement encode vos données (appelées en tant que texte brut) en texte chiffré. Contrairement au texte brut, le texte chiffré ne peut pas être utilisé par des personnes ou des ordinateurs sauf et jusqu’à ce que le texte chiffré soit déchiffré. Le déchiffrement nécessite une clé de chiffrement dont les utilisateurs autorisés disposent uniquement. Le chiffrement permet de garantir que seuls les destinataires autorisés peuvent déchiffrer votre contenu. Le contenu inclut des fichiers, des messages électroniques, des entrées de calendrier, etc.
  
Le chiffrement n’empêche pas l’interception de contenu. Le chiffrement fait partie d’une stratégie de protection des informations plus importante pour votre organisation. En utilisant le chiffrement, vous vous assurez que seules les personnes autorisées peuvent utiliser les données chiffrées.
  
Vous pouvez avoir plusieurs couches de chiffrement en même temps. Par exemple, vous pouvez chiffrer les messages électroniques, ainsi que les canaux de communication via lesquels votre courrier électronique transite. Avec Office 365, vos données sont chiffrées au repos et en transit à l’aide de plusieurs protocoles de chiffrement forts, ainsi que des technologies qui incluent TLS/SSL (Transport Layer Security/Secure Sockets Layer), IPSec (Internet Protocol Security) et le chiffrement avancé Standard (AES).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Chiffrement des données au repos et des données en transit

 **Des exemples de données au repos incluent des** fichiers que vous avez téléchargés vers une bibliothèque SharePoint, des données Project Online, des documents que vous avez téléchargés dans une réunion Skype entreprise, des messages électroniques et des pièces jointes que vous avez stockés dans des dossiers dans votre Office 365 boîtes aux lettres et fichiers que vous avez téléchargés vers OneDrive entreprise.
  
 Parmi les **exemples de données en transit** , citons les messages électroniques qui sont en cours de remise, ou les conversations qui ont lieu lors d’une réunion en ligne. Dans Office 365, les données sont en transit chaque fois que l’appareil d’un utilisateur communique avec un serveur Office 365, ou lorsqu’un serveur Office 365 communique avec un autre serveur.
  
Avec Office 365, plusieurs couches et types de chiffrement collaborent pour sécuriser vos données. Le tableau suivant contient des exemples, avec des liens vers des informations supplémentaires.
  
|**Types de contenu**|**Technologies de chiffrement**|**Ressources pour en savoir plus**|
|:-----|:-----|:-----|
|Fichiers sur un appareil. Ces fichiers peuvent inclure des messages électroniques enregistrés dans un dossier, des documents Office enregistrés sur un ordinateur, une tablette ou un téléphone ou des données enregistrées dans le Cloud Microsoft.  <br/> |BitLocker dans les centres de connaissances Microsoft. BitLocker peut également être utilisé sur les ordinateurs clients, tels que les ordinateurs Windows et les tablettes  <br/> Gestionnaire de clés distribuées (DKM) dans les centres de distribution Microsoft  <br/> Clé client pour Office 365  <br/> |[Centre informatique Windows: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Centre de gestion de la confidentialité Microsoft: chiffrement](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Série de contrôles de sécurité du Cloud: chiffrement des données au repos](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online](exchange-online-secures-email-secrets.md) <br/> [Contrôle de vos données dans Office 365 à l'aide de la Clé client](controlling-your-data-using-customer-key.md). <br/> |
|Fichiers en transit entre les utilisateurs. Ces fichiers peuvent inclure des documents Office ou des éléments de liste SharePoint partagés entre les utilisateurs.  <br/> |TLS pour les fichiers en transit  <br/> |[Chiffrement de données dans OneDrive Entreprise et SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Skype entreprise Online: sécurité et archivage](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|Courrier électronique en transit entre les destinataires. Ce message inclut le courrier électronique hébergé par Exchange Online.  <br/> |Chiffrement de messages Office 365 avec Azure Rights Management, S/MIME et TLS pour le courrier électronique en transit  <br/> |[Chiffrement de messages Office 365 (OME)](ome.md) <br/> [Chiffrement du courrier électronique dans Office 365](email-encryption.md) <br/> [Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |

## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>Qu’en est-il si j’ai besoin de plus de contrôle sur le chiffrement pour répondre aux exigences de sécurité et de conformité?

Office 365 fournit des solutions gérées par Microsoft pour le chiffrement de volume, le chiffrement de fichiers et le chiffrement de boîtes aux lettres dans Office 365. En outre, Office 365 fournit des solutions de chiffrement que vous pouvez gérer et contrôler. Ces solutions de chiffrement sont basées sur Azure.
  
Pour en savoir plus, consultez les ressources suivantes:
  
- [Qu’est-ce que Azure Rights Management?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)

- [Activer la gestion des droits dans le centre d’administration](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)

- [Set up Information Rights Management (IRM) in SharePoint admin center](set-up-irm-in-sp-admin-center.md)

- [Contrôle de vos données dans Office 365 à l'aide de la Clé client](controlling-your-data-using-customer-key.md).

## <a name="how-do-i"></a>Procédures

|**Pour effectuer cette tâche**|**Voir les ressources suivantes**|
|:-----|:-----|
|Configurer le chiffrement pour mon organisation  <br/> |[Configurer le chiffrement dans Office 365 Entreprise](set-up-encryption.md) <br/> |
|Afficher des détails sur les certificats, les technologies et les suites de chiffrement TLS dans Office 365  <br/> |[Détails techniques sur le chiffrement dans Office 365](technical-reference-details-about-encryption.md) <br/> |
|Utiliser des messages chiffrés sur un appareil mobile  <br/> |[Afficher des messages chiffrés sur votre appareil Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [Afficher des messages chiffrés sur votre iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|Chiffrer un document à l’aide de la protection par mot de passe  <br/><br/>  La protection par mot de passe n’est pas prise en charge dans Office 365 dans un navigateur. Utiliser les versions de bureau de Word, Excel et PowerPoint pour la protection par mot de passe. |[Ajouter ou supprimer la protection dans votre document, classeur ou présentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) <br/> Choisissez une section **Ajouter une protection** , puis sélectionnez **chiffrer avec mot de passe**.  |
|Supprimer le chiffrement d’un document  <br/> |[Ajouter ou supprimer la protection dans votre document, classeur ou présentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) <br/> Choisissez une section **protection contre la suppression** , puis consultez supprimer le chiffrement du **mot de passe**.  |

## <a name="related-topics"></a>Sujets associés

[Planifier les fonctionnalités de protection des informations et de sécurité d’Office 365](plan-for-security-and-compliance.md)

[10 façons de sécuriser les offres Office 365 et Microsoft 365 Business](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data?view=o365-worldwide)
