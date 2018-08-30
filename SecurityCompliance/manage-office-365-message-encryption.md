---
title: Gérer le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
description: Une fois que vous avez terminé la configuration d’Office 365 Message Encryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons. Par exemple, vous pouvez configurer s’il faut activer les codes secrets unique, afficher le bouton protéger dans Outlook sur le web et bien plus encore. Les tâches de cet article décrivent comment.
ms.openlocfilehash: ddc86bdf0d0ce5480587862a4ed438b6c138987f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527840"
---
# <a name="manage-office-365-message-encryption"></a>Gérer le chiffrement de messages Office 365

Une fois que vous avez terminé la configuration d’Office 365 Message Encryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons. Par exemple, vous pouvez configurer s’il faut activer les codes secrets unique, afficher le bouton **protéger** dans Outlook sur le web et bien plus encore. Les tâches de cet article décrivent comment. 
  
||
|:-----|
|Cet article fait partie d’une plus grande série d’articles sur Office 365 Message Encryption. Cet article est destiné aux administrateurs et les professionnels de l’informatique. Si vous êtes simplement vous recherchez des informations sur l’envoi ou la réception d’un message chiffré, vous trouverez la liste des articles inclus dans [Office 365 Message Encryption (OME)](ome.md) et recherchez l’article qui vous convient le mieux à vos besoins. |
   
## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Gestion des si les destinataires de Google, Yahoo et Account Microsoft peuvent utiliser ces comptes pour se connecter au portail Office 365 Message Encryption
<a name="PermitSocialID"> </a>

Par défaut, lorsque vous configurez les nouvelles fonctionnalités de chiffrement de messages Office 365, les utilisateurs de votre organisation peuvent envoyer des messages à des destinataires qui sont en dehors de votre organisation Office 365. Si le destinataire utilise un *ID de mise en réseau* comme un compte Google, Yahoo compte ou compte Microsoft, le destinataire peut se connecter au portail OME à l’aide de l’ID de mise en réseau. Si vous le souhaitez, vous pouvez choisir ne pas afin que les destinataires à utiliser des ID de mise en réseau pour se connecter au portail OME. 
  
 **Pour gérer ou non autoriser les destinataires à utiliser des ID de mise en réseau pour se connecter au portail OME**
  
1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Exécutez l’applet de commande Set-OMEConfiguration avec le paramètre SocialIdSignIn comme suit :
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true |$false >
  ```

    Par exemple, pour désactiver les codes de mise en réseau :
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

    Pour activer les codes de mise en réseau :
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a>Gestion de l’utilisation des codes d’accès unique pour la connexion au portail Office 365 Message Encryption
<a name="GenerateOTPC"> </a>

Par défaut, si le destinataire d’un message chiffré par OME n’utilise pas Outlook, quel que soit le compte utilisé par le destinataire, le destinataire reçoit un lien web-affichage durée limitée qui leur permet de lire le message. Cela inclut un code secret unique. En tant qu’administrateur, vous pouvez gérer les codes d’accès unique peuvent servir pour vous connecter au portail OME ou non.
  
 **Pour gérer les codes secrets unique sont générés pour OME ou non**
  
1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Exécutez l’applet de commande Set-OMEConfiguration avec le paramètre OTPEnabled comme suit :
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true |$false >
  ```

    Par exemple, pour désactiver les codes secrets unique :
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
  ```

    Pour activer les codes secrets unique :
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
  ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a>Gestion de l’affichage du bouton protection dans Outlook sur le web
<a name="DisplayProtectButton"> </a>

Par défaut, le bouton **protéger** dans Outlook sur le site web n’est pas activé lorsque vous configurez OME. En tant qu’administrateur, vous pouvez gérer s’il faut afficher ce bouton pour les utilisateurs finaux. 
  
 **Pour gérer ou non le bouton protéger s’affiche dans Outlook sur le web**
  
1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Exécutez l’applet de commande Set-IRMConfiguration avec le paramètre - SimplifiedClientAccessEnabled comme suit :
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true |$false >
  ```

    Par exemple, pour désactiver le bouton **protéger** : 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

    Pour activer le bouton **protéger** : 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
  ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>Activer le service côté le déchiffrement des messages électroniques pour les utilisateurs de l’application messagerie iOS
<a name="EnableServiceSideDecrypt"> </a>

L’application de messagerie iOS ne peut pas déchiffrer les messages protégés avec Office 365 Message Encryption. En tant qu’un administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les messages remis à l’application de messagerie iOS. Lorsque vous choisissez pour ce faire, le service envoie une copie du message déchiffrée au périphérique iOS. Le message est stocké déchiffré sur le périphérique client. Le message conserve également des informations sur les droits d’utilisation du même si l’application de messagerie iOS ne s’applique pas les droits d’utilisation du côté client à l’utilisateur. Cela signifie que l’utilisateur peut copier ou imprimer le message, même s’ils n’ont pas été les droits à le faire. Toutefois, si l’utilisateur tente d’effectuer une action qui requiert le serveur de messagerie Office 365, tels que de transférer le message, le serveur ne permettra pas l’action si l’utilisateur n’a pas été le droit d’utilisation à le faire. Toutefois, les utilisateurs finaux peuvent contourner restriction d’utilisation ne pas transférer à transférer le message à partir d’un compte différent dans leur application de messagerie iOS quel que soit ou non paramétrer le déchiffrement côté service de messagerie, des pièces jointes chiffrées et des droits protégés par la messagerie ne peuvent pas être affichés dans l’application de messagerie iOS.
  
Si vous choisissez de ne pas autoriser les messages déchiffrés soient envoyées aux utilisateurs de l’application de messagerie iOS, les utilisateurs reçoivent un message qui indique qu’ils ne possèdent les droits pour afficher le message. Par défaut, côté service déchiffrement des messages électroniques n’est pas activé.
  
Pour plus d’informations et pour une vue de l’expérience du client, consultez la section «[Afficher les messages chiffrés sur votre iPhone ou l’iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)» dans [permet d’afficher des messages chiffrés sur votre iPhone ou l’iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).
  
 **Pour gérer les utilisateurs de l’application de messagerie iOS ou non peuvent afficher des messages protégés par le chiffrement de messages Office 365**
  
1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Exécutez l’applet de commande Set-ActiveSyncOrganizations avec le paramètre AllowRMSSupportForUnenlightenedApps comme suit :
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true |$false >
  ```

    Par exemple, pour configurer le service pour déchiffrer des messages avant de les envoyer aux applications unenlightened tels que les e/s application de messagerie :
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
  ```

    Par exemple, pour configurer le service ne pas pour envoyer des messages déchiffrés aux applications unenlightened :
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
  ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>Activer le déchiffrement côté service des pièces jointes de courrier électronique pour les clients de messagerie de navigateur web
<a name="EnableServiceSideDecrypt"> </a>

En règle générale, lorsque vous utilisez le chiffrement de messages Office 365, les pièces jointes sont automatiquement chiffrés. En tant qu’un administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les pièces jointes que les utilisateurs téléchargent à partir d’un navigateur web. 
  
Lorsque vous choisissez pour ce faire, le service envoie une copie du fichier déchiffrée à l’appareil. Le message est toujours chiffré. La pièce jointe conserve également des informations sur les droits d’utilisation du même si le navigateur ne s’applique pas les droits d’utilisation du côté client à l’utilisateur. Cela signifie que l’utilisateur peut copier ou imprimer la pièce jointe, même s’ils n’ont pas été les droits à le faire. Toutefois, si l’utilisateur tente d’effectuer une action qui requiert le serveur de messagerie Office 365, tels que le transfert de la pièce jointe, le serveur ne permettra pas l’action si l’utilisateur n’a pas été le droit d’utilisation à le faire.
  
Quelle que soit la si vous configurez le déchiffrement côté service des pièces jointes, les pièces jointes de chiffré et il messagerie protégé par des droits ne peuvent pas être consultée dans l’application de messagerie iOS.
  
Si vous choisissez de ne pas autoriser les pièces jointes de courrier électronique déchiffré, qui est la valeur par défaut, les utilisateurs reçoivent un message qui indique qu’ils ne possèdent les droits pour afficher les pièces jointes. \* \* \* insérer une image ?
  
Pour plus d’informations sur comment Office 365 implémente le chiffrement pour les messages électroniques et des pièces jointes avec l’option de chiffrer, voir [option chiffrer uniquement pour les courriers électroniques.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
 **Pour gérer ou non les pièces jointes sont déchiffrées au téléchargement à partir d’un navigateur web**
  
1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Exécutez l’applet de commande Set-IRMConfiguration avec le paramètre DecryptAttachmentFromPortal comme suit :
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal <$true |$false >
  ```

    Par exemple, pour configurer le service pour déchiffrer les pièces jointes lorsqu’un utilisateur télécharge les à partir d’un navigateur web :
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $true
  ```

    Pour configurer le service pour laisser les pièces jointes de courrier électronique chiffré en tant qu’ils reçoivent lors du téléchargement :
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $false
  ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a>Personnaliser l’apparence des messages électroniques et le portail OME
<a name="CustomizeAppearance"> </a>

Pour plus d’informations sur la façon dont vous pouvez personnaliser OME pour votre organisation, voir [Ajouter la marque de votre organisation à vos messages chiffrés](add-your-organization-brand-to-encrypted-messages.md).
  
## <a name="disabling-the-new-capabilities-for-ome"></a>Désactiver les nouvelles fonctionnalités pour OME
<a name="CustomizeAppearance"> </a>

Nous espérons qu’il n’est pas fourni, mais si vous avez besoin, désactiver les nouvelles fonctionnalités pour OME est très simple. Tout d’abord, vous devez supprimer tout les règles de flux de messagerie que vous avez créé et qui utilisent les nouvelles fonctionnalités d’OME. Pour plus d’informations sur la suppression des règles de flux de messagerie, voir [Gérer les règles de flux de messagerie](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Ensuite, effectuez ces étapes dans Exchange Online PowerShell.
  
 **Pour désactiver les nouvelles fonctionnalités pour OME**
  
1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).
    
2. Si vous avez activé le bouton protéger dans Outlook sur le web, le désactiver en exécutant l’applet de commande Set-IRMConfiguration avec le paramètre SimplifiedClientAccessEnabled comme suit :
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

3. Exécutez l’applet de commande Set-IRMConfiguration avec le paramètre AzureRMSLicensingEnabled comme suit :
    
  ```
  Set-IRMConfiguration -AzureRMSLicensingEnabled $false
  ```


