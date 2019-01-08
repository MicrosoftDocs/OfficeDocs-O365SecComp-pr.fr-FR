---
title: Gérer le chiffrement de messages Office 365
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
ms.openlocfilehash: 460ac0bba4d10fe8bef896a23a20f74527f031b2
ms.sourcegitcommit: bd1762ccf63c7d2ad8b49a936115171c72fb2c0f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27750053"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="93436-105">Gérer le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="93436-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="93436-p102">Une fois que vous avez terminé la configuration d’Office 365 Message Encryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons. Par exemple, vous pouvez configurer s’il faut activer les codes secrets unique, afficher le bouton **protéger** dans Outlook sur le web et bien plus encore. Les tâches de cet article décrivent comment.</span><span class="sxs-lookup"><span data-stu-id="93436-p102">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways. For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more. The tasks in this article describe how.</span></span> 
  
||
|:-----|
|<span data-ttu-id="93436-p103">Cet article fait partie d’une plus grande série d’articles sur Office 365 Message Encryption. Cet article est destiné aux administrateurs et les professionnels de l’informatique. Si vous êtes simplement vous recherchez des informations sur l’envoi ou la réception d’un message chiffré, vous trouverez la liste des articles inclus dans [Office 365 Message Encryption (OME)](ome.md) et recherchez l’article qui vous convient le mieux à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="93436-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and IT Pros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="93436-112">Gestion des si les destinataires de Google, Yahoo et Account Microsoft peuvent utiliser ces comptes pour se connecter au portail Office 365 Message Encryption</span><span class="sxs-lookup"><span data-stu-id="93436-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="93436-p104">Par défaut, lorsque vous configurez les nouvelles fonctionnalités de chiffrement de messages Office 365, les utilisateurs de votre organisation peuvent envoyer des messages à des destinataires qui sont en dehors de votre organisation Office 365. Si le destinataire utilise un *ID de mise en réseau* comme un compte Google, Yahoo compte ou compte Microsoft, le destinataire peut se connecter au portail OME à l’aide de l’ID de mise en réseau. Si vous le souhaitez, vous pouvez choisir ne pas afin que les destinataires à utiliser des ID de mise en réseau pour se connecter au portail OME.</span><span class="sxs-lookup"><span data-stu-id="93436-p104">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization. If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID. If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span> 
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="93436-116">Pour gérer ou non autoriser les destinataires à utiliser des ID de mise en réseau pour se connecter au portail OME</span><span class="sxs-lookup"><span data-stu-id="93436-116">To manage whether or not to allow recipients to use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="93436-117">[Se connecter à Exchange Online à l’aide de PowerShell à distance](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="93436-117">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="93436-118">Exécutez l’applet de commande Set-OMEConfiguration avec le paramètre SocialIdSignIn comme suit :</span><span class="sxs-lookup"><span data-stu-id="93436-118">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
  ```

  <span data-ttu-id="93436-119">Par exemple, pour désactiver les codes de mise en réseau :</span><span class="sxs-lookup"><span data-stu-id="93436-119">For example, to disable social IDs:</span></span>
  
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

  <span data-ttu-id="93436-120">Pour activer les codes de mise en réseau :</span><span class="sxs-lookup"><span data-stu-id="93436-120">To enable social IDs:</span></span>

  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="93436-121">Gestion de l’utilisation des codes d’accès unique pour la connexion au portail Office 365 Message Encryption</span><span class="sxs-lookup"><span data-stu-id="93436-121">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="93436-p105">Par défaut, si le destinataire d’un message chiffré par OME n’utilise pas Outlook, quel que soit le compte utilisé par le destinataire, le destinataire reçoit un lien web-affichage durée limitée qui leur permet de lire le message. Cela inclut un code secret unique. En tant qu’administrateur, vous pouvez gérer les codes d’accès unique peuvent servir pour vous connecter au portail OME ou non.</span><span class="sxs-lookup"><span data-stu-id="93436-p105">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message. This includes a one-time pass code. As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a><span data-ttu-id="93436-125">Pour gérer les codes secrets unique sont générés pour OME ou non</span><span class="sxs-lookup"><span data-stu-id="93436-125">To manage whether or not one-time pass codes are generated for OME</span></span>
  
1. <span data-ttu-id="93436-p106">À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="93436-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="93436-128">Exécutez l’applet de commande Set-OMEConfiguration avec le paramètre OTPEnabled :</span><span class="sxs-lookup"><span data-stu-id="93436-128">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>```

   <span data-ttu-id="93436-129">Par exemple, pour désactiver les codes secrets unique :</span><span class="sxs-lookup"><span data-stu-id="93436-129">For example, to disable one-time pass codes:</span></span>

   ```Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false```

   <span data-ttu-id="93436-130">Pour activer les codes secrets unique :</span><span class="sxs-lookup"><span data-stu-id="93436-130">To enable one-time pass codes:</span></span>

   ```Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="93436-131">Gestion de l’affichage du bouton protection dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="93436-131">Managing the display of the Protect button in Outlook on the web</span></span>

<span data-ttu-id="93436-p107">Par défaut, le bouton **protéger** dans Outlook sur le site web n’est pas activé lorsque vous configurez OME. En tant qu’administrateur, vous pouvez gérer s’il faut afficher ce bouton pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="93436-p107">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME. As an administrator, you can manage whether or not to display this button to end users.</span></span> 
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="93436-134">Pour gérer ou non le bouton protéger s’affiche dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="93436-134">To manage whether or not the Protect button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="93436-p108">À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="93436-p108">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="93436-137">Exécutez l’applet de commande Set-IRMConfiguration avec le paramètre - SimplifiedClientAccessEnabled :</span><span class="sxs-lookup"><span data-stu-id="93436-137">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>```

   <span data-ttu-id="93436-138">Par exemple, pour désactiver le bouton **protéger** :</span><span class="sxs-lookup"><span data-stu-id="93436-138">For example, to disable the **Protect** button:</span></span>

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $false```

   <span data-ttu-id="93436-139">Pour activer le bouton **protéger** :</span><span class="sxs-lookup"><span data-stu-id="93436-139">To enable the **Protect** button:</span></span>

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $true```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="93436-140">Activer le service côté le déchiffrement des messages électroniques pour les utilisateurs de l’application messagerie iOS</span><span class="sxs-lookup"><span data-stu-id="93436-140">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="93436-p109">L’application de messagerie iOS ne peut pas déchiffrer les messages protégés avec Office 365 Message Encryption. En tant qu’un administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les messages remis à l’application de messagerie iOS. Lorsque vous choisissez pour ce faire, le service envoie une copie du message déchiffrée au périphérique iOS. Le message est stocké déchiffré sur le périphérique client. Le message conserve également des informations sur les droits d’utilisation du même si l’application de messagerie iOS ne s’applique pas les droits d’utilisation du côté client à l’utilisateur. Cela signifie que l’utilisateur peut copier ou imprimer le message, même s’ils n’ont pas été les droits à le faire. Toutefois, si l’utilisateur tente d’effectuer une action qui requiert le serveur de messagerie Office 365, tels que de transférer le message, le serveur ne permettra pas l’action si l’utilisateur n’a pas été le droit d’utilisation à le faire. Toutefois, les utilisateurs finaux peuvent contourner restriction d’utilisation ne pas transférer à transférer le message à partir d’un compte différent dans leur application de messagerie iOS quel que soit ou non paramétrer le déchiffrement côté service de messagerie, des pièces jointes chiffrées et des droits protégés par la messagerie ne peuvent pas être affichés dans l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="93436-p109">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption. As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app. When you choose to do this, the service sends a decrypted copy of the message to the iOS device. The message is stored decrypted on the client device. The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user. This means that the user can copy or print the message even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so. However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app. Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="93436-p110">Si vous choisissez de ne pas autoriser les messages déchiffrés soient envoyées aux utilisateurs de l’application de messagerie iOS, les utilisateurs reçoivent un message qui indique qu’ils ne possèdent les droits pour afficher le message. Par défaut, côté service déchiffrement des messages électroniques n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="93436-p110">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message. By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="93436-152">Pour plus d’informations et pour une vue de l’expérience du client, consultez la section «[Afficher les messages chiffrés sur votre iPhone ou l’iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)» dans [permet d’afficher des messages chiffrés sur votre iPhone ou l’iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="93436-152">For more information, and for a view of the client experience, see the section, "[View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" in [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="93436-153">Pour gérer les utilisateurs de l’application de messagerie iOS ou non peuvent afficher des messages protégés par le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="93436-153">To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="93436-p111">À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="93436-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="93436-156">Exécutez l’applet de commande Set-ActiveSyncOrganizations avec le paramètre AllowRMSSupportForUnenlightenedApps :</span><span class="sxs-lookup"><span data-stu-id="93436-156">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>```

   <span data-ttu-id="93436-157">Par exemple, pour configurer le service pour déchiffrer des messages avant de les envoyer aux applications unenlightened tels que les e/s application de messagerie :</span><span class="sxs-lookup"><span data-stu-id="93436-157">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true```

   <span data-ttu-id="93436-158">Ou, pour configurer le service ne pas pour envoyer des messages déchiffrés aux applications unenlightened :</span><span class="sxs-lookup"><span data-stu-id="93436-158">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="93436-159">Activer le déchiffrement côté service des pièces jointes de courrier électronique pour les clients de messagerie de navigateur web</span><span class="sxs-lookup"><span data-stu-id="93436-159">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="93436-p112">En règle générale, lorsque vous utilisez le chiffrement de messages Office 365, les pièces jointes sont automatiquement chiffrés. En tant qu’un administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les pièces jointes que les utilisateurs téléchargent à partir d’un navigateur web.</span><span class="sxs-lookup"><span data-stu-id="93436-p112">Normally, when you use Office 365 message encryption, attachments are automatically encrypted. As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span> 
  
<span data-ttu-id="93436-p113">Lorsque vous choisissez pour ce faire, le service envoie une copie du fichier déchiffrée à l’appareil. Le message est toujours chiffré. La pièce jointe conserve également des informations sur les droits d’utilisation du même si le navigateur ne s’applique pas les droits d’utilisation du côté client à l’utilisateur. Cela signifie que l’utilisateur peut copier ou imprimer la pièce jointe, même s’ils n’ont pas été les droits à le faire. Toutefois, si l’utilisateur tente d’effectuer une action qui requiert le serveur de messagerie Office 365, tels que le transfert de la pièce jointe, le serveur ne permettra pas l’action si l’utilisateur n’a pas été le droit d’utilisation à le faire.</span><span class="sxs-lookup"><span data-stu-id="93436-p113">When you choose to do this, the service sends a decrypted copy of the file to the device. The message is still encrypted. The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user. This means that the user can copy or print the email attachment even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="93436-167">Quelle que soit la si vous configurez le déchiffrement côté service des pièces jointes, les pièces jointes de chiffré et il messagerie protégé par des droits ne peuvent pas être consultée dans l’application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="93436-167">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="93436-168">Si vous choisissez de ne pas autoriser les pièces jointes de courrier électronique déchiffré, qui est la valeur par défaut, les utilisateurs reçoivent un message qui indique qu’ils ne possèdent les droits pour afficher les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="93436-168">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="93436-169">Pour plus d’informations sur comment Office 365 implémente le chiffrement pour les messages électroniques et des pièces jointes avec l’option de chiffrer, voir [option chiffrer uniquement pour les courriers électroniques.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="93436-169">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="93436-170">Pour gérer ou non les pièces jointes sont déchiffrées au téléchargement à partir d’un navigateur web</span><span class="sxs-lookup"><span data-stu-id="93436-170">To manage whether or not email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="93436-p114">À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="93436-p114">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="93436-173">Exécutez l’applet de commande Set-IRMConfiguration avec le paramètre DecryptAttachmentFromPortal :</span><span class="sxs-lookup"><span data-stu-id="93436-173">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>```

   <span data-ttu-id="93436-174">Par exemple, pour configurer le service pour déchiffrer les pièces jointes lorsqu’un utilisateur télécharge les à partir d’un navigateur web :</span><span class="sxs-lookup"><span data-stu-id="93436-174">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal $true```

   <span data-ttu-id="93436-175">Pour configurer le service pour laisser les pièces jointes de courrier électronique chiffré en tant qu’ils reçoivent lors du téléchargement :</span><span class="sxs-lookup"><span data-stu-id="93436-175">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```Set-IRMConfiguration -DecryptAttachmentFromPortal $false```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="93436-176">Personnaliser l’apparence des messages électroniques et le portail OME</span><span class="sxs-lookup"><span data-stu-id="93436-176">Customizing the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="93436-177">Pour plus d’informations sur la façon dont vous pouvez personnaliser OME pour votre organisation, voir [Ajouter la marque de votre organisation à vos messages chiffrés](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="93436-177">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="93436-178">Désactiver les nouvelles fonctionnalités pour OME</span><span class="sxs-lookup"><span data-stu-id="93436-178">Disabling the new capabilities for OME</span></span>

<span data-ttu-id="93436-p115">Nous espérons qu’il n’est pas fourni, mais si vous avez besoin, désactiver les nouvelles fonctionnalités pour OME est très simple. Tout d’abord, vous devez supprimer tout les règles de flux de messagerie que vous avez créé et qui utilisent les nouvelles fonctionnalités d’OME. Pour plus d’informations sur la suppression des règles de flux de messagerie, voir [Gérer les règles de flux de messagerie](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Ensuite, effectuez ces étapes dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="93436-p115">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward. First, you'll need to remove any mail flow rules you've created that use the new OME capabilities. For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="93436-183">Pour désactiver les nouvelles fonctionnalités pour OME</span><span class="sxs-lookup"><span data-stu-id="93436-183">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="93436-p116">À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="93436-p116">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="93436-p117">Si vous avez activé le bouton **protéger** dans Outlook sur le web, le désactiver en exécutant l’applet de commande Set-IRMConfiguration avec le paramètre SimplifiedClientAccessEnabled. Sinon, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="93436-p117">If you enabled the **Protect** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter. Otherwise, skip this step.</span></span>

   ```Set-IRMConfiguration -SimplifiedClientAccessEnabled $false```

3. <span data-ttu-id="93436-188">Désactiver les nouvelles fonctionnalités pour OME en exécutant l’applet de commande Set-IRMConfiguration avec le paramètre AzureRMSLicensingEnabled défini sur false :</span><span class="sxs-lookup"><span data-stu-id="93436-188">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```Set-IRMConfiguration -AzureRMSLicensingEnabled $false```
