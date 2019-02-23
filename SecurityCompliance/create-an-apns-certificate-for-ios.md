---
title: Créer un certificat APNs pour les appareils iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Pour gérer les appareils iOS comme iPad et iPhone dans la gestion des appareils mobiles pour Office 365, procédez comme suit pour créer d'abord un certificat APNs.
ms.openlocfilehash: 5f82690f0add5f1aae95a089d9cdfc0b320ae596
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220454"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>Créer un certificat APNs pour les appareils iOS

 Pour gérer des appareils iOS comme iPad et iPhone dans la gestion des appareils mobiles pour Office 365, vous devez créer un certificat APNs. 
  
Pour ce faire, suivez les étapes indiquées dans le lien **configurer** sur la page du portail. (Accédez à \> **stratégies** \> de sécurité du centre de sécurité ** &amp; conformité** **gestion** \> des périphériques **gérer les paramètres**.)
  
![Configurer la gestion des appareils mobiles requise et les étapes recommandées](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. En regard de **configurer un certificat APNs pour les appareils iOS**, sélectionnez **configurer**.
    
2. Sélectionnez **Télécharger votre fichier CSR** et enregistrez la demande de signature de certificat à un endroit de votre ordinateur dont vous vous souviendrez. 
    
    ![Boîte de dialogue installer le certificat APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. Sélectionnez **Suivant**.
    
4. Créez un certificat APN.
    
  - Sélectionnez **Apple APNs Portal** pour ouvrir le portail Appled Certificates. 
    
    ![Boîte de dialogue installer le certificat de notification APN avec le portail Apple APNS sélectionné](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Connectez-vous avec un ID Apple.
    
    > [!IMPORTANT]
    > Utilisez l'ID d'une société associée à un compte de messagerie qui restera avec votre organisation, même si l'utilisateur qui gère le compte le quitte. Enregistrez cet ID car vous devrez utiliser le même ID lorsqu'il est temps de renouveler le certificat. 
  
  - Sélectionnez **créer un certificat** et accepter les **conditions d'utilisation**.
    
  - **Accédez** à la demande de signature de certificat que vous avez téléchargée sur votre ordinateur à partir d'Office 365 et sélectionnez **Télécharger**.
    
  - **Téléchargez** le certificat APN créé par le portail de certificats poussés Apple sur votre ordinateur. 
    
    > [!TIP]
    > Si vous ne parvenez pas à télécharger le certificat, actualisez votre navigateur. 
  
5. ReVenez à Office 365 et sélectionnez **suivant** pour accéder à la page **Télécharger le certificat APNs** . 
    
6. Accédez au certificat APN que vous avez téléchargé à partir du portail Apple des certificats poussés.
    
    ![Cliquez sur le bouton Parcourir pour sélectionner le certificat APNS que vous avez téléchargé depuis Apple.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Sélectionnez **Terminer**.
    
Revenez aux \> **stratégies** \> de sécurité du centre de sécurité ** &amp; conformité** **gestion** \> des appareils **gérer les paramètres** pour terminer l'installation. 
  

