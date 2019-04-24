---
title: Configurer le chiffrement dans Office 365 Entreprise
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/2/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e86fc991-0161-4f01-9c1c-d25e87733d06
description: Avec Office 365, certaines fonctionnalités de chiffrement sont activées par défaut; d'autres fonctionnalités peuvent être configurées pour répondre à certaines exigences légales ou de conformité.
ms.openlocfilehash: 1bc4ceb7762c96f55c03f89e7c448f9e4073063e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260792"
---
# <a name="set-up-encryption-in-office-365-enterprise"></a>Configurer le chiffrement dans Office 365 Entreprise

Le chiffrement peut empêcher la lecture de votre contenu par des utilisateurs non autorisés. Étant donné que le [chiffrement dans Office 365](encryption.md) peut être réalisé à l'aide de différentes technologies et méthodes, il n'y a pas un seul emplacement où vous activez ou configurez le chiffrement. Cet article fournit des informations sur les différentes façons de configurer ou de configurer le chiffrement dans le cadre de votre stratégie de protection des informations.
  
> [!TIP]
> Si vous recherchez des détails techniques supplémentaires sur le chiffrement, voir [informations de référence technique sur le chiffrement dans Office 365](technical-reference-details-about-encryption.md).
  
Avec Office 365, plusieurs fonctionnalités de chiffrement sont disponibles par défaut. Des fonctionnalités de chiffrement supplémentaires peuvent être configurées pour répondre à certaines exigences légales ou de conformité. Le tableau suivant décrit plusieurs méthodes de chiffrement pour différents scénarios.
  
|**Scénario**|**Méthodes de chiffrement**|
|:-----|:-----|
|Les fichiers sont enregistrés sur les ordinateurs Windows  <br/> |Le chiffrement au niveau de l'ordinateur peut être réalisé à l'aide de BitLocker sur les appareils Windows. En tant qu'administrateur d'entreprise ou professionnel de l'informatique, vous pouvez le configurer à l'aide de Microsoft Deployment Toolkit (MDT). Consultez la rubrique [set up MDT for BitLocker](https://go.microsoft.com/fwlink/?linkid=849282).  <br/> |
|Les fichiers sont enregistrés sur des appareils mobiles  <br/> |Certains types d'appareils mobiles chiffrent les fichiers qui sont enregistrés par défaut sur ces appareils. Grâce aux [fonctionnalités de gestion des appareils mobiles intégrée pour office 365](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0), vous pouvez définir des stratégies qui déterminent si les appareils mobiles doivent être autorisés à accéder aux données dans Office 365. Par exemple, vous pouvez définir une stratégie qui autorise uniquement les appareils qui chiffrent du contenu pour accéder aux données Office 365. Voir [créer et déployer des stratégies de sécurité des appareils](https://support.office.com/article/d310f556-8bfb-497b-9bd7-fe3c36ea2fd6).  <br/> Pour un contrôle supplémentaire sur la façon dont les appareils mobiles interagissent avec Office 365, vous pouvez envisager d'ajouter [Microsoft Intune](https://aka.ms/qzln04). Voir [choisir entre MDM pour Office 365 et Microsoft Intune](https://support.office.com/article/c93d9ab9-efb2-4349-9b93-30c30562ee22).  <br/> |
|Vous avez besoin de contrôler les clés de chiffrement utilisées pour chiffrer vos données dans les centres de données de Microsoft  <br/> | En tant qu'administrateur Office 365, vous pouvez contrôler les clés de chiffrement de votre organisation, puis configurer Office 365 pour les utiliser afin de chiffrer vos données au repos dans les centres de données de Microsoft.  <br/> [Contrôle de vos données dans Office 365 à l'aide de la Clé client](controlling-your-data-using-customer-key.md). <br/> [Clé client pour le Forum aux questions Office 365](service-encryption-with-customer-key-faq.md) <br/> |
|Les personnes communiquent par courrier électronique (Exchange Online)  <br/> | En tant qu'administrateur Exchange Online, vous disposez de plusieurs options pour configurer le chiffrement du courrier électronique. Ces approches sont les suivantes :  <br/>  Utilisation du chiffrement de [messages Office 365 (OME)](set-up-new-message-encryption-capabilities.md) avec Azure Rights Management (Azure RMS) pour permettre aux utilisateurs d'envoyer des messages chiffrés à l'intérieur ou à l'extérieur de votre organisation  <br/>  Utilisation [de S/MIME pour la signature et](https://aka.ms/c6dozg) le chiffrement des messages pour chiffrer et signer numériquement les messages électroniques  <br/>  Utilisation de TLS pour [configurer des connecteurs pour un flux de messagerie sécurisé avec une autre organisation](https://aka.ms/hs809p) <br/>  Voir [chiffrement des messages électroniques dans Office 365](https://aka.ms/hic3f7).  <br/> |
|Les fichiers sont accessibles à partir de sites d'équipe ou de bibliothèques de documents (OneDrive entreprise ou SharePoint Online)  <br/> |Lorsque des utilisateurs travaillent sur des fichiers enregistrés dans OneDrive entreprise ou SharePoint Online, les connexions TLS sont utilisées. Cette intégration est automatiquement intégrée à Office 365. Voir [chiffrement des données dans OneDrive entreprise et SharePoint Online](https://go.microsoft.com/fwlink/?linkid=526379).  <br/> |
|Les fichiers sont partagés dans les réunions en ligne et les conversations par messagerie instantanée (Skype entreprise Online)  <br/> |Lorsque des utilisateurs travaillent sur des fichiers à l'aide de Skype entreprise Online, TLS est utilisé pour la connexion. Cette intégration est automatiquement intégrée à Office 365. Voir [sécurité et archivage (Skype entreprise Online)](https://aka.ms/nuq4ws).  <br/> |

## <a name="additional-information"></a>Informations supplémentaires

Pour en savoir plus sur les solutions de protection des fichiers qui incluent des options de chiffrement, consultez la rubrique [File Protection Solutions in Office 365](https://www.microsoft.com/en-us/download/details.aspx?id=55523).