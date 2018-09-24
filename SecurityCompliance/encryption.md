---
title: Chiffrement dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
description: Avec Office 365, votre contenu est chiffré au repos et en transit, à l’aide du chiffrement, les protocoles et les technologies disponibles puissant. Obtenir une vue d’ensemble du chiffrement dans Office 365.
ms.openlocfilehash: a9f37fddf28461ee4912e0b8a1f5b922c59c009f
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972286"
---
# <a name="encryption-in-office-365"></a>Chiffrement dans Office 365

Chiffrement constitue une part importante de vos stratégies de protection des informations et de protection fichier. Lisez cet article pour obtenir une vue d’ensemble de cryptage utilisé pour toutes les versions d’Office 365 et obtenir de l’aide avec des tâches de chiffrement, à partir de la configuration de chiffrement pour votre organisation à des documents Office Protection par mot de passe.
  
- Si vous recherchez des informations sur les certificats et de technologies telles que TLS, voir [informations de référence technique de chiffrement dans Office 365](technical-reference-details-about-encryption.md).
    
- Si vous recherchez des informations sur la configuration ou la définition de chiffrement pour votre organisation, voir [configurer le chiffrement dans Office 365 pour entreprises](set-up-encryption.md).
    
## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>Quel est le chiffrement, et comment elle fonctionne dans Office 365 ?

À un niveau élevé, le chiffrement est le processus de codage des données (désignées en tant que texte brut) en texte chiffré qui ne peut être utilisé par les personnes ou les ordinateurs jusqu'à ce que le texte chiffré est déchiffré. Le déchiffrement nécessite une clé de chiffrement que seuls les utilisateurs. Chiffrement garantit que seuls les destinataires autorisés peuvent déchiffrer votre contenu, tels que les messages électroniques et des fichiers.
  
Chiffrement en elle-même n’empêche pas de contenu, tels que des fichiers, des messages électroniques, des entrées de calendrier, etc., tombent dans les mains. Chiffrement fait partie d’une stratégie de protection des informations plus grande pour votre organisation. À l’aide de chiffrement, vous pouvez aider à garantir que seuls les utilisateurs doivent être en mesure d’utiliser les données chiffrées sont en mesure de.
  
Vous pouvez avoir plusieurs couches de chiffrement en place en même temps. Par exemple, vous pouvez crypter les messages électroniques, ainsi que les canaux de communication via lequel passe votre courrier électronique. Avec Office 365, vos données sont chiffrées au repos et en transit, à l’aide de plusieurs protocoles de cryptage et les technologies qui incluent le chiffrement avancée, sécurité du protocole Internet (IPSec) et Transport Layer Security/Secure Sockets Layer (SSL/TLS) Standard (AES).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Chiffrement des données au repos et des données en transit

 Fichiers qui ont été téléchargés dans une bibliothèque SharePoint, les données Project Online, les documents qui ont été téléchargés dans un Skype pour la réunion, les messages électroniques et les pièces jointes qui sont stockés dans des dossiers dans Office 365 entreprise des exemples **de données au repos** boîte aux lettres et les fichiers téléchargés vers OneDrive entreprise. 
  
 Les exemples **de données en transit** de messages électroniques qui sont en cours de transmission, ou des conversations qui ont lieu dans une réunion en ligne. Dans Office 365, les données sont en transit chaque fois que le périphérique d’un utilisateur communique avec un serveur d’Office 365, ou lorsqu’un serveur Office 365 communique avec un autre serveur. 
  
Avec Office 365, vous pouvez avoir plusieurs calques et les types de chiffrement collaborer pour sécuriser vos données. Le tableau suivant comprend certains exemples, avec des liens vers des informations supplémentaires.
  
|**Types de contenu**|**Technologies de chiffrement**|**Ressources pour en savoir plus**|
|:-----|:-----|:-----|
|Fichiers sur un appareil. Cela peut inclure des messages électroniques enregistrés dans un dossier, les documents Office enregistrés sur un ordinateur, une tablette ou un téléphone ou des données enregistrées dans le nuage de Microsoft.  <br/> |BitLocker dans les centres de données Microsoft. Vous pouvez également utiliser BitLocker sur les ordinateurs clients, tels que les ordinateurs Windows et tablettes  <br/> Gestionnaire de clé distribué (DKM) dans des centres de données Microsoft  <br/> Clé de client pour Office 365  <br/> |[Windows IT Center : BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Centre de gestion de la confidentialité Microsoft : le chiffrement](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Sécurité du nuage contrôle série : chiffrer les données au repos](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online](exchange-online-secures-email-secrets.md) <br/> [Contrôler vos données dans Office 365 à l'aide de la clé client](controlling-your-data-using-customer-key.md) <br/> |
|Fichiers en transit entre les utilisateurs. Cela peut inclure des documents Office ou les éléments de liste SharePoint partagés entre les utilisateurs.  <br/> |TLS pour les fichiers en transit  <br/> |[Chiffrement de données dans OneDrive Entreprise et SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Skype pour les entreprises en ligne : sécurité et archivage](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|En transit entre les destinataires de messagerie. Cela inclut la messagerie hébergée par Exchange Online.  <br/> |Chiffrement de messages Office 365 avec Azure Rights Management, S/MIME et TLS pour le courrier électronique en transit  <br/> |[Chiffrement de messages Office 365 (OME)](ome.md) <br/> [Chiffrement du courrier dans Office 365](email-encryption.md) <br/> [Mode d’utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie dans Office 365](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |
   
## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>Que se passe-t-il si j’ai besoin davantage de contrôle sur le chiffrement pour répondre aux besoins de sécurité et de conformité ?

En plus de solutions Microsoft géré de chiffrement de volume, chiffrement de fichier et le chiffrement de boîte aux lettres dans Office 365, les options de client géré peuvent servir pour répondre aux besoins de sécurité et de conformité plus strictes. Ces solutions utilisent Azure Rights Management (Services RMS Azure) avec Office 365.
  
Voir les ressources suivantes pour en savoir plus :
  
- [What ' s Azure Rights Management ?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
    
- [Azure Rights Management dans le Centre d’administration Office 365](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)
    
- [Définir des Information Rights Management (IRM) dans le centre d’administration SharePoint](set-up-irm-in-sp-admin-center.md)
    
## <a name="how-do-i"></a>Comment faire ?

|**Pour effectuer cette tâche**|**Consultez les ressources suivantes**|
|:-----|:-----|
|Configurer le chiffrement pour mon organisation  <br/> |[Configurer le chiffrement dans Office 365 Entreprise](set-up-encryption.md) <br/> |
|Afficher plus d’informations sur les certificats, les technologies et les suites de chiffrement TLS dans Office 365  <br/> |[Informations techniques de chiffrement dans Office 365](technical-reference-details-about-encryption.md) <br/> |
|Travailler avec des messages chiffrés sur un appareil mobile  <br/> |[Afficher les messages chiffrés sur votre appareil Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [Afficher les messages chiffrés sur votre iPhone ou l’iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|Chiffrer un document à l’aide de la protection du mot de passe  <br/><br/>  Actuellement, mot de passe n’est pas pris en charge dans Office Online. Utilisez des versions de bureau de Word, Excel et PowerPoint pour la protection du mot de passe.           |[Ajouter ou supprimer la protection dans votre document, classeur ou une présentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Sélectionnez une section de **protection d’ajouter** et de voir **chiffrer avec mot de passe** )  <br/> |
|Supprimer le chiffrement d’un document  <br/> |[Ajouter ou supprimer la protection dans votre document, classeur ou une présentation](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Sélectionnez une section de **suppression de la protection** et de voir **Supprimer le chiffrement de mot de passe** )  <br/> |
   
## <a name="related-topics"></a>Voir aussi

[Planifier des fonctionnalités de protection des informations de sécurité et Office 365](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[Sécurité et conformité dans Office 365 pour entreprises - aide d’administration](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)
  

