---
title: Configurez le chiffrement dans Office 365 pour entreprises
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/2/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e86fc991-0161-4f01-9c1c-d25e87733d06
description: Avec Office 365, certaines fonctionnalités de chiffrement sont activées par défaut ; autres fonctionnalités peuvent être configurées pour répondre à certaines exigences légales ou conformité.
ms.openlocfilehash: 80deced80283ac36d82ac15cee9af6d390c4749a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527851"
---
# <a name="set-up-encryption-in-office-365-enterprise"></a>Configurez le chiffrement dans Office 365 pour entreprises

Chiffrement peut protéger votre contenu à partir de la lecture par des utilisateurs non autorisés. Étant donné que [le chiffrement dans Office 365](encryption.md) peut être effectué à l’aide de diverses technologies et les méthodes, il n’existe pas un seul emplacement où vous activer ou configurez le chiffrement. Cet article fournit des informations sur les différentes manières, vous pouvez configurer ou configurer le chiffrement dans le cadre de votre stratégie de protection des informations. 
  
> [!TIP]
> Si vous recherchez des informations plus techniques de chiffrement, voir [informations de référence technique de chiffrement dans Office 365](technical-reference-details-about-encryption.md). 
  
Avec Office 365, plusieurs fonctionnalités de chiffrement sont disponibles par défaut. Les fonctionnalités de chiffrement supplémentaires peuvent être configurées pour répondre à certaines exigences légales ou conformité. Le tableau suivant décrit plusieurs méthodes de chiffrement pour les différents scénarios.
  
|**Scénario**|**Méthodes de chiffrement**|
|:-----|:-----|
|Les fichiers sont enregistrés sur les ordinateurs Windows  <br/> |Le chiffrement au niveau de l’ordinateur peut être effectué à l’aide de BitLocker sur les périphériques Windows. En tant qu’administrateur d’entreprise ou professionnels de l’informatique, vous pouvez définir à l’aide de Microsoft Deployment Toolkit (MDT). Consultez la rubrique [Set up MDT pour BitLocker](https://go.microsoft.com/fwlink/?linkid=849282).<br/> |
|Les fichiers sont enregistrés sur les appareils mobiles  <br/> |Certains types d’appareils mobiles chiffrer les fichiers qui sont enregistrés dans ces périphériques par défaut. Avec les [fonctionnalités de gestion des périphériques mobiles intégrées à Office 365](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0), vous pouvez définir des stratégies qui déterminent s’il faut autoriser les périphériques mobiles accéder aux données dans Office 365. Par exemple, vous pouvez définir une stratégie qui autorise uniquement les périphériques qui chiffrer le contenu pour accéder aux données d’Office 365. Voir [créer et déployer des stratégies de sécurité des périphériques](https://support.office.com/article/d310f556-8bfb-497b-9bd7-fe3c36ea2fd6).<br/> Pour un contrôle supplémentaire sur les appareils mobiles comment interagir avec Office 365, vous pouvez envisager d’ajouter [Intune Microsoft](https://aka.ms/qzln04). Voir [choisir entre Mobile Device Manager pour Office 365 et Microsoft Intune](https://support.office.com/article/c93d9ab9-efb2-4349-9b93-30c30562ee22).<br/> |
|Vous devez contrôler les clés de chiffrement utilisés pour chiffrer les données dans les centres de données de Microsoft  <br/> | En tant qu’un administrateur Office 365, vous pouvez contrôler les clés de chiffrement de votre organisation, puis configurez Office 365 pour les utiliser pour chiffrer vos données au repos dans les centres de données de Microsoft.  <br/> [Contrôle de vos données dans Office 365 à l’aide de la clé de client](controlling-your-data-using-customer-key.md) <br/> [Clé de client pour le Forum aux questions Office 365](service-encryption-with-customer-key-faq.md) <br/> |
|Communiquent personnes par courrier électronique (Exchange Online)  <br/> | En tant qu’un administrateur Exchange Online, vous disposez de plusieurs options de configuration du chiffrement de courrier électronique. Cela inclut :<br/>  À l’aide du [chiffrement de messages Office 365 (OME)](set-up-new-message-encryption-capabilities.md) avec Azure Rights Management (Services RMS Azure) pour permettre aux utilisateurs d’envoyer des messages chiffrés à l’intérieur ou à l’extérieur de votre organisation  <br/>  À l’aide de [S/MIME pour la signature et le chiffrement](https://aka.ms/c6dozg) pour chiffrer et signer numériquement les messages électroniques  <br/>  [Configurer les connecteurs pour le flux de messagerie sécurisée avec une autre organisation](https://aka.ms/hs809p) utilisant le protocole TLS <br/>  Consultez la rubrique [chiffrement de messagerie dans Office 365](https://aka.ms/hic3f7).  <br/> |
|Les fichiers sont accessibles à partir des sites d’équipe ou des bibliothèques de documents (OneDrive for Business ou SharePoint Online)  <br/> |Lorsque vous travaillez avec des fichiers enregistrés dans OneDrive pour les professionnels ou SharePoint Online personnes, les connexions TLS sont utilisées. Il est intégré à Office 365 automatiquement. Voir [chiffrement des données dans OneDrive for Business et SharePoint Online](https://go.microsoft.com/fwlink/?linkid=526379).<br/> |
|Les fichiers sont partagés dans les réunions en ligne et des conversations par messagerie instantanée (Skype pour Business Online)  <br/> |Lorsque vous travaillez avec des fichiers à l’aide de Skype pour Business Online personnes, TLS est utilisé pour la connexion. Il est intégré à Office 365 automatiquement. Voir [sécurité et archivage (Skype pour les entreprises en ligne)](https://aka.ms/nuq4ws).<br/> |
   
## <a name="additional-information"></a>Informations supplémentaires

Pour en savoir plus sur les solutions de protection de fichiers qui incluent des options de chiffrement, voir [Solutions de Protection des fichiers dans Office 365](https://www.microsoft.com/en-us/download/details.aspx?id=55523).
  

