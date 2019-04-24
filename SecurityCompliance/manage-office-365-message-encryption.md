---
title: Gérer le chiffrement de messages Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- M365-security-compliance
description: Une fois que vous avez terminé la configuration d'Office 365 message enCryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons. Par exemple, vous pouvez configurer s'il faut activer des codes de passe unique, afficher le bouton protéger dans Outlook sur le Web, et bien plus encore. Les tâches décrites dans cet article expliquent comment procéder.
ms.openlocfilehash: 7b5297ae42d3efa071408540863c6ff7dbdee407
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259812"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="4e9e1-105">Gérer le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="4e9e1-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="4e9e1-106">Une fois que vous avez terminé la configuration d'Office 365 message enCryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-106">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways.</span></span> <span data-ttu-id="4e9e1-107">Par exemple, vous pouvez configurer s'il faut activer des codes de passe unique, afficher le bouton **protéger** dans Outlook sur le Web, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-107">For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more.</span></span> <span data-ttu-id="4e9e1-108">Les tâches décrites dans cet article expliquent comment procéder.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-108">The tasks in this article describe how.</span></span>
  
||
|:-----|
|<span data-ttu-id="4e9e1-109">Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-109">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="4e9e1-110">Cet article est destiné aux administrateurs et ITPros.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-110">This article is intended for administrators and ITPros.</span></span> <span data-ttu-id="4e9e1-111">Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-111">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="4e9e1-112">La gestion de la possibilité pour les destinataires de comptes Google, Yahoo et Microsoft de se connecter au portail de chiffrement des messages Office 365</span><span class="sxs-lookup"><span data-stu-id="4e9e1-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="4e9e1-113">Par défaut, lorsque vous configurez les nouvelles fonctionnalités de chiffrement de messages Office 365, les utilisateurs de votre organisation peuvent envoyer des messages à des destinataires qui se trouvent en dehors de votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-113">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization.</span></span> <span data-ttu-id="4e9e1-114">Si le destinataire utilise un *ID social* comme un compte Google, un compte Yahoo ou un compte Microsoft, le destinataire peut se connecter au portail OME à l'aide de l'identifiant social.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-114">If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID.</span></span> <span data-ttu-id="4e9e1-115">Si vous le souhaitez, vous pouvez choisir de ne pas autoriser les destinataires à utiliser des ID sociaux pour se connecter au portail OME.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-115">If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="4e9e1-116">Pour gérer l'autorisation ou non des destinataires à utiliser les ID sociaux pour se connecter au portail OME</span><span class="sxs-lookup"><span data-stu-id="4e9e1-116">To manage whether or not to allow recipients to use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="4e9e1-117">[Connectez-vous à Exchange Online à l'aide de Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-117">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="4e9e1-118">Exécutez la cmdlet Set-OMEConfiguration avec le paramètre SocialIdSignIn comme suit:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-118">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   <span data-ttu-id="4e9e1-119">Par exemple, pour désactiver les ID de mise en réseau:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-119">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="4e9e1-120">Pour activer les ID de mise en réseau:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-120">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="4e9e1-121">Gestion de l'utilisation de codes d'accès unique pour se connecter au portail de chiffrement des messages Office 365</span><span class="sxs-lookup"><span data-stu-id="4e9e1-121">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="4e9e1-122">Par défaut, si le destinataire d'un message chiffré par OME n'utilise pas Outlook, quel que soit le compte utilisé par le destinataire, le destinataire reçoit un lien d'affichage Web de temps limité qui lui permet de lire le message.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-122">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message.</span></span> <span data-ttu-id="4e9e1-123">Cela inclut un code d'accès unique.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-123">This includes a one-time pass code.</span></span> <span data-ttu-id="4e9e1-124">En tant qu'administrateur, vous pouvez gérer si les codes de passe unique peuvent être utilisés pour se connecter au portail OME.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-124">As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a><span data-ttu-id="4e9e1-125">Pour gérer la génération ou non de codes d'accès à la fois pour OME</span><span class="sxs-lookup"><span data-stu-id="4e9e1-125">To manage whether or not one-time pass codes are generated for OME</span></span>
  
1. <span data-ttu-id="4e9e1-126">À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-126">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="4e9e1-127">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-127">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="4e9e1-128">Exécutez la cmdlet Set-OMEConfiguration avec le paramètre OTPEnabled:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-128">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="4e9e1-129">Par exemple, pour désactiver les codes d'accès à usage unique:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-129">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="4e9e1-130">Pour activer les codes d'accès à usage unique:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-130">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="4e9e1-131">Gestion de l'affichage du bouton protéger dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="4e9e1-131">Managing the display of the Protect button in Outlook on the web</span></span>

<span data-ttu-id="4e9e1-132">Par défaut, le bouton **protéger** dans Outlook sur le Web n'est pas activé lorsque vous configurez ome.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-132">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME.</span></span> <span data-ttu-id="4e9e1-133">En tant qu'administrateur, vous pouvez gérer l'affichage ou non de ce bouton pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-133">As an administrator, you can manage whether or not to display this button to end users.</span></span>
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="4e9e1-134">Pour gérer le fait que le bouton protéger apparaisse ou non dans Outlook sur le Web</span><span class="sxs-lookup"><span data-stu-id="4e9e1-134">To manage whether or not the Protect button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="4e9e1-135">À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-135">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="4e9e1-136">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-136">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="4e9e1-137">Exécutez la cmdlet Set-IRMConfiguration avec le paramètre-SimplifiedClientAccessEnabled:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-137">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="4e9e1-138">Par exemple, pour désactiver le bouton **protéger** :</span><span class="sxs-lookup"><span data-stu-id="4e9e1-138">For example, to disable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="4e9e1-139">Pour activer le bouton **protéger** :</span><span class="sxs-lookup"><span data-stu-id="4e9e1-139">To enable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="4e9e1-140">Activer le déchiffrement côté service des messages électroniques pour les utilisateurs de l'application de messagerie iOS</span><span class="sxs-lookup"><span data-stu-id="4e9e1-140">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="4e9e1-141">L'application de messagerie iOS ne peut pas déchiffrer les messages protégés avec le chiffrement de messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-141">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption.</span></span> <span data-ttu-id="4e9e1-142">En tant qu'administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les messages remis à l'application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-142">As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app.</span></span> <span data-ttu-id="4e9e1-143">Lorsque vous choisissez de le faire, le service envoie une copie déchiffrée du message au périphérique iOS.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-143">When you choose to do this, the service sends a decrypted copy of the message to the iOS device.</span></span> <span data-ttu-id="4e9e1-144">Le message est stocké déchiffré sur le périphérique client.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-144">The message is stored decrypted on the client device.</span></span> <span data-ttu-id="4e9e1-145">Le message conserve également des informations sur les droits d'utilisation, même si l'application de messagerie iOS n'applique pas de droits d'utilisation côté client à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-145">The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="4e9e1-146">Cela signifie que l'utilisateur peut copier ou imprimer le message même s'il ne dispose pas des droits nécessaires pour le faire.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-146">This means that the user can copy or print the message even if they did not originally have the rights to do so.</span></span> <span data-ttu-id="4e9e1-147">Toutefois, si l'utilisateur tente d'effectuer une action qui nécessite le serveur de messagerie Office 365, comme le transfert du message, le serveur n'autorise pas l'action si l'utilisateur n'a pas le droit d'utilisation à ce propos.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-147">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so.</span></span> <span data-ttu-id="4e9e1-148">Toutefois, les utilisateurs finaux peuvent contourner ne pas transférer la restriction d'utilisation en transférant le message à partir d'un compte différent dans son application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-148">However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app.</span></span> <span data-ttu-id="4e9e1-149">Que vous configurez le déchiffrement côté service du courrier, toutes les pièces jointes aux messages chiffrés et protégés par des droits ne peuvent pas être affichées dans l'application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-149">Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="4e9e1-150">Si vous choisissez de ne pas autoriser les messages déchiffrés à être envoyés aux utilisateurs de l'application de messagerie iOS, les utilisateurs reçoivent un message qui indique qu'ils ne disposent pas des droits pour afficher le message.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-150">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message.</span></span> <span data-ttu-id="4e9e1-151">Par défaut, le déchiffrement côté service des messages électroniques n'est pas activé.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-151">By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="4e9e1-152">Pour plus d'informations et pour une vue de l'expérience client, consultez la rubrique [afficher des messages chiffrés sur votre iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-152">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="4e9e1-153">Pour gérer si les utilisateurs de l'application de messagerie iOS peuvent afficher les messages protégés par le chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="4e9e1-153">To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="4e9e1-154">À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-154">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="4e9e1-155">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-155">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="4e9e1-156">Exécutez la cmdlet Set-ActiveSyncOrganizations avec le paramètre AllowRMSSupportForUnenlightenedApps:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-156">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="4e9e1-157">Par exemple, pour configurer le service afin de déchiffrer les messages avant qu'ils soient envoyés à des applications non prévues telles que l'application de messagerie iOS:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-157">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="4e9e1-158">Ou, pour configurer le service de sorte qu'il n'envoie pas de messages déchiffrés à des applications incorrectes:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-158">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="4e9e1-159">Activer le déchiffrement côté service des pièces jointes de courrier électronique pour les clients de messagerie de navigateur Web</span><span class="sxs-lookup"><span data-stu-id="4e9e1-159">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="4e9e1-160">En règle générale, lorsque vous utilisez le chiffrement de messages Office 365, les pièces jointes sont automatiquement chiffrées.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-160">Normally, when you use Office 365 message encryption, attachments are automatically encrypted.</span></span> <span data-ttu-id="4e9e1-161">En tant qu'administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les pièces jointes que les utilisateurs téléchargent à partir d'un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-161">As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="4e9e1-162">Lorsque vous choisissez de le faire, le service envoie une copie déchiffrée du fichier sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-162">When you choose to do this, the service sends a decrypted copy of the file to the device.</span></span> <span data-ttu-id="4e9e1-163">Le message est toujours chiffré.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-163">The message is still encrypted.</span></span> <span data-ttu-id="4e9e1-164">La pièce jointe de courrier conserve également des informations sur les droits d'utilisation, même si le navigateur n'applique pas de droits d'utilisation côté client à l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-164">The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user.</span></span> <span data-ttu-id="4e9e1-165">Cela signifie que l'utilisateur peut copier ou imprimer la pièce jointe de courrier électronique même si, à l'origine, il ne dispose pas des droits nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-165">This means that the user can copy or print the email attachment even if they did not originally have the rights to do so.</span></span> <span data-ttu-id="4e9e1-166">Toutefois, si l'utilisateur tente d'effectuer une action qui nécessite le serveur de messagerie Office 365, comme le transfert de la pièce jointe, le serveur n'autorise pas l'action si l'utilisateur n'a pas le droit d'utilisation à ce propos.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-166">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="4e9e1-167">Que vous configurez le déchiffrement côté service des pièces jointes, les pièces jointes aux messages chiffrés et protégés par des droits ne peuvent pas être affichées dans l'application de messagerie iOS.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-167">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="4e9e1-168">Si vous choisissez de ne pas autoriser les pièces jointes déchiffrées, ce qui correspond à la valeur par défaut, les utilisateurs reçoivent un message qui indique qu'ils ne disposent pas des droits pour afficher la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-168">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="4e9e1-169">Pour plus d'informations sur la façon dont Office 365 implémente le chiffrement pour les messages électroniques et les pièces jointes avec l'option de chiffrement uniquement, reportez-vous à la rubrique [option chiffrer uniquement pour les messages électroniques.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="4e9e1-169">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="4e9e1-170">Pour gérer si les pièces jointes de courrier sont déchiffrées lors du téléchargement à partir d'un navigateur Web</span><span class="sxs-lookup"><span data-stu-id="4e9e1-170">To manage whether or not email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="4e9e1-171">À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-171">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="4e9e1-172">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-172">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="4e9e1-173">Exécutez la cmdlet Set-IRMConfiguration avec le paramètre DecryptAttachmentFromPortal:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-173">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   <span data-ttu-id="4e9e1-174">Par exemple, pour configurer le service afin de déchiffrer les pièces jointes lorsqu'un utilisateur les télécharge à partir d'un navigateur Web:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-174">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   <span data-ttu-id="4e9e1-175">Pour configurer le service de sorte qu'il quitte les pièces jointes chiffrées lorsqu'il est téléchargé, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-175">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="4e9e1-176">Personnalisation de l'apparence des messages électroniques et du portail OME</span><span class="sxs-lookup"><span data-stu-id="4e9e1-176">Customizing the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="4e9e1-177">Pour plus d'informations sur la façon de personnaliser OME pour votre organisation, consultez la rubrique [Ajouter la marque de votre organisation à vos messages chiffrés](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-177">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="4e9e1-178">DésActivation des nouvelles fonctionnalités pour OME</span><span class="sxs-lookup"><span data-stu-id="4e9e1-178">Disabling the new capabilities for OME</span></span>

<span data-ttu-id="4e9e1-179">Nous espérons qu'il n'y parviendra pas, mais si vous le souhaitez, la désactivation des nouvelles fonctionnalités de OME est très simple.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-179">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward.</span></span> <span data-ttu-id="4e9e1-180">Tout d'abord, vous devez supprimer toutes les règles de flux de messagerie que vous avez créées qui utilisent les nouvelles fonctionnalités de OME.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-180">First, you'll need to remove any mail flow rules you've created that use the new OME capabilities.</span></span> <span data-ttu-id="4e9e1-181">Pour plus d'informations sur la suppression des règles de flux de messagerie, consultez la rubrique [Manage mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-181">For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span></span> <span data-ttu-id="4e9e1-182">Ensuite, effectuez ces étapes dans Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-182">Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="4e9e1-183">Pour désactiver les nouvelles fonctionnalités de OME</span><span class="sxs-lookup"><span data-stu-id="4e9e1-183">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="4e9e1-184">À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-184">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="4e9e1-185">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="4e9e1-185">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="4e9e1-186">Si vous avez activé le bouton **protéger** dans Outlook sur le Web, désactivez-le en exécutant la cmdlet Set-IRMConfiguration avec le paramètre SimplifiedClientAccessEnabled.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-186">If you enabled the **Protect** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter.</span></span> <span data-ttu-id="4e9e1-187">Sinon, ignorez cette étape.</span><span class="sxs-lookup"><span data-stu-id="4e9e1-187">Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="4e9e1-188">DésActivez les nouvelles fonctionnalités de OME en exécutant l'applet de commande Set-IRMConfiguration avec le paramètre AzureRMSLicensingEnabled défini sur false:</span><span class="sxs-lookup"><span data-stu-id="4e9e1-188">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
