---
title: Créer un certificat APNs pour les appareils iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Pour gérer les périphériques iOS comme iPad et l’iPhone dans Gestion des périphériques mobiles pour Office 365, procédez comme suit pour créer un certificat APNs.
ms.openlocfilehash: 28e8888d7dd57c3052cdcb5994725f11a5f0445f
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272049"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>Créer un certificat APNs pour les appareils iOS

 Pour gérer les périphériques iOS comme iPad et l’iPhone dans Gestion des périphériques mobiles pour Office 365, vous devez créer un certificat APNs. 
  
Pour ce faire, suivez les étapes à partir du lien **configurer** sur la page du portail. (Atteindre **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **Device management** \> **Gérer les paramètres**.)
  
![Configurer la gestion des appareils mobiles requis et les étapes recommandées](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. En regard de **configurer un certificat APNs pour les appareils iOS**, sélectionnez **configurer**.
    
2. Sélectionnez **télécharger votre fichier CSR** et enregistrez la demande de signature de certificat vers un quelque part sur votre ordinateur que vous allez vous souvenir. 
    
    ![Installer la boîte de dialogue certificat point](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. Cliquez sur **suivant**.
    
4. Créer un certificat de point.
    
  - Sélectionnez **Apple APNS portail** pour ouvrir le portail de certificats Push Apple. 
    
    ![Installer point cert boîte de dialogue avec Apple APNS portail sélectionné](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Connectez-vous à l’aide d’un ID d’Apple.
    
    > [!IMPORTANT]
    > Utilisez une société Qu'apple ID associé à un compte de messagerie qui restera avec votre organisation, même si l’utilisateur qui gère le compte. Enregistrez ce code, car vous devez utiliser le même ID lorsqu’il est temps de renouveler le certificat. 
  
  - Sélectionnez **créer un certificat** et accepter les **Conditions d’utilisation**.
    
  - **Accédez** à la demande de signature de certificat vous avez téléchargé sur votre ordinateur à partir d’Office 365 et sélectionnez **Télécharger**.
    
  - **Télécharger** le certificat point créé par le portail de certificat Push Apple à votre ordinateur. 
    
    > [!TIP]
    > Si vous rencontrez des difficultés à télécharger le certificat, actualisez votre navigateur. 
  
5. Revenir à Office 365, puis cliquez sur **suivant** pour accéder à la page **APNS télécharger le certificat** . 
    
6. Recherchez le certificat point que vous avez téléchargé à partir du portail de certificats Push Apple.
    
    ![Cliquez sur le bouton Parcourir pour sélectionner le certificat APNS que vous avez téléchargé à partir d’Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Sélectionnez **Terminer**.
    
Revenez à **sécurité &amp; centre de conformité** \> **stratégies de sécurité** \> **Device management** \> **Gérer les paramètres** pour terminer l’installation. 
  

