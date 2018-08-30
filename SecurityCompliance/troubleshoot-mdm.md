---
title: Résoudre les problèmes d’inscription de périphérique avec Mobile Device Manager pour Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/17/2015
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c863b2bf-45f3-483a-ba05-29fc7f4d6434
description: Si vous exécutez des problèmes lorsque vous tentez d’inscrire un appareil Mobile Device Management (MDM) pour Office 365, essayez les étapes répertoriées ici pour localiser le problème. Si les étapes générales ne résout pas le problème, voir une des sections ultérieure avec les étapes spécifiques pour votre type de périphérique.
ms.openlocfilehash: 490259fc623b38ab5ad6cf8553c5074c77b77426
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272109"
---
# <a name="troubleshoot-device-enrollment-with-mdm-for-office-365"></a>Résoudre les problèmes d’inscription de périphérique avec Mobile Device Manager pour Office 365

Si vous exécutez des problèmes lorsque vous tentez d’inscrire un appareil Mobile Device Management (MDM) pour Office 365, essayez les étapes répertoriées ici pour localiser le problème. Si les étapes générales ne résout pas le problème, voir une des sections ultérieure avec les étapes spécifiques pour votre type de périphérique.
  
## <a name="steps-to-try-first"></a>Étapes à essayer en premier

Pour commencer, vérifiez les points suivants :
  
- Assurez-vous que le périphérique n’est pas déjà inscrit avec un autre fournisseur de gestion des appareils mobiles, tels que Intune.
    
- Assurez-vous que le périphérique est défini sur la date et l’heure.
    
- Basculer vers un autre Wi-Fi ou le réseau cellulaire sur l’appareil.
    
- Pour les appareils Android ou iOS, désinstallez et réinstallez l’application de portail d’entreprise Intune sur l’appareil.
    
## <a name="ios-phone-or-tablet"></a>iOS téléphone ou tablette

- Assurez-vous que vous avez [configurer un certificat APNs](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).
    
- Dans **paramètres** \> **Général** \> **profil** (ou la **Gestion des périphériques**), assurez-vous qu’un **Profil de gestion** n’est pas déjà installé. S’il s’agit, supprimez-le. 
    
- Si vous voyez le message d’erreur « Échec du périphérique inscrire, » se connecter à Office 365 et assurez-vous qu’une licence qui inclut Exchange Online a été attribuée à l’utilisateur qui est connecté au périphérique.
    
- Si vous voyez le message d’erreur « Échec de profil à installer, », essayez l’une des options suivantes :
    
  - Assurez-vous que Safari est le navigateur par défaut sur l’appareil et que les cookies ne sont pas désactivés.
    
  - Redémarrer le périphérique, puis accédez à portal.manage.microsoft.com, connectez-vous avec votre ID d’utilisateur Office 365 et le mot de passe et essayer d’installer le profil manuellement.
    
## <a name="windows-rt-tablet"></a>Tablette Windows RT

- Assurez-vous que votre domaine est [configuré dans Office 365 pour fonctionner avec Mobile Device Manager](set-up-mobile-device-management.md).
    
- Assurez-vous que l’utilisateur est choix **Activer** plutôt que de choisir **joindre**.
    
## <a name="windows-phone"></a>Windows Phone

- Assurez-vous que votre domaine est [configuré dans Office 365 pour fonctionner avec Mobile Device Manager](set-up-mobile-device-management.md).
    
- Assurez-vous que le périphérique est en cours d’exécution Windows 8.1 ou version ultérieure.
    
## <a name="android-phone-or-tablet"></a>Téléphone Android ou tablette

- Assurez-vous que le périphérique est en cours d’exécution Android 4.0 ou version ultérieure.
    
- Si vous voyez le message d’erreur « Nous n’inscrire ce périphérique, » se connecter à Office 365 et assurez-vous qu’une licence qui inclut Exchange Online a été attribuée à l’utilisateur qui est connecté au périphérique.
    
- Vérifiez la **Zone de Notification** sur le périphérique pour voir si toutes les actions de l’utilisateur final sont en attente et si elles sont, effectuez les actions. 
    

