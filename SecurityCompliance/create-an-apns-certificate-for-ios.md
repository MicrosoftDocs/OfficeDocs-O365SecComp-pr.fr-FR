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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258618"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>Créer un certificat APNs pour les appareils iOS

 Pour gérer des appareils iOS comme iPad et iPhone dans la gestion des appareils mobiles pour Office 365, vous devez créer un certificat APNs. 
  
Pour ce faire, suivez les étapes indiquées dans le lien **configurer** sur la page du portail. (Accédez à \> **stratégies** \> de sécurité du centre de sécurité ** &amp; conformité** **gestion** \> des périphériques **gérer les paramètres**.)
  
![Configurer la gestion des appareils mobiles requise et les étapes recommandées](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.
    
2. Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember. 
    
    ![Boîte de dialogue installer le certificat APN](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3.  Select **Next**. 
    
4.  Create an APN certificate.
    
  - Select **Apple APNS Portal** to open the Apple Push Certificates Portal.  
    
    ![Boîte de dialogue installer le certificat de notification APN avec le portail Apple APNS sélectionné](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Sign in with an Apple ID.
    
    > [!IMPORTANT]
    > Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate. 
  
  - Select **Create a Certificate** and accept the **Terms of Use**.
    
  - **Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.
    
  - **Download** the APN certificate created by the Apple Push Certificate Portal to your computer. 
    
    > [!TIP]
    > If you're having trouble downloading the certificate, refresh your browser. 
  
5. Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page. 
    
6.  Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.
    
    ![Cliquez sur le bouton Parcourir pour sélectionner le certificat APNS que vous avez téléchargé depuis Apple.](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Select **Finish**.
    
Revenez aux \> **stratégies** \> de sécurité du centre de sécurité ** &amp; conformité** **gestion** \> des appareils **gérer les paramètres** pour terminer l'installation. 
  

