---
title: Gérer le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
description: Une fois que vous avez terminé la configuration d'Office 365 message enCryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons. Par exemple, vous pouvez configurer s'il faut activer des codes de passe unique, afficher le bouton protéger dans Outlook sur le Web, et bien plus encore. Les tâches décrites dans cet article expliquent comment procéder.
ms.openlocfilehash: 8b044898efb1ef86790773cd3f8e8061523b0ec0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213754"
---
# <a name="manage-office-365-message-encryption"></a>Gérer le chiffrement de messages Office 365

Une fois que vous avez terminé la configuration d'Office 365 message enCryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons. Par exemple, vous pouvez configurer s'il faut activer des codes de passe unique, afficher le bouton **protéger** dans Outlook sur le Web, et bien plus encore. Les tâches décrites dans cet article expliquent comment procéder.
  
||
|:-----|
|Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins. |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>La gestion de la possibilité pour les destinataires de comptes Google, Yahoo et Microsoft de se connecter au portail de chiffrement des messages Office 365

Par défaut, lorsque vous configurez les nouvelles fonctionnalités de chiffrement de messages Office 365, les utilisateurs de votre organisation peuvent envoyer des messages à des destinataires qui se trouvent en dehors de votre organisation Office 365. Si le destinataire utilise un *ID social* comme un compte Google, un compte Yahoo ou un compte Microsoft, le destinataire peut se connecter au portail OME à l'aide de l'identifiant social. Si vous le souhaitez, vous pouvez choisir de ne pas autoriser les destinataires à utiliser des ID sociaux pour se connecter au portail OME.
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a>Pour gérer l'autorisation ou non des destinataires à utiliser les ID sociaux pour se connecter au portail OME
  
1. [Connectez-vous à Exchange Online à l'aide de Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).

2. Exécutez la cmdlet Set-OMEConfiguration avec le paramètre SocialIdSignIn comme suit:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   Par exemple, pour désactiver les ID de mise en réseau:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   Pour activer les ID de mise en réseau:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a>Gestion de l'utilisation de codes d'accès unique pour se connecter au portail de chiffrement des messages Office 365

Par défaut, si le destinataire d'un message chiffré par OME n'utilise pas Outlook, quel que soit le compte utilisé par le destinataire, le destinataire reçoit un lien d'affichage Web de temps limité qui lui permet de lire le message. Cela inclut un code d'accès unique. En tant qu'administrateur, vous pouvez gérer si les codes de passe unique peuvent être utilisés pour se connecter au portail OME.
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a>Pour gérer la génération ou non de codes d'accès à la fois pour OME
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-OMEConfiguration avec le paramètre OTPEnabled:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   Par exemple, pour désactiver les codes d'accès à usage unique:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   Pour activer les codes d'accès à usage unique:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a>Gestion de l'affichage du bouton protéger dans Outlook sur le Web

Par défaut, le bouton **protéger** dans Outlook sur le Web n'est pas activé lorsque vous configurez ome. En tant qu'administrateur, vous pouvez gérer l'affichage ou non de ce bouton pour les utilisateurs finaux.
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a>Pour gérer le fait que le bouton protéger apparaisse ou non dans Outlook sur le Web
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-IRMConfiguration avec le paramètre-SimplifiedClientAccessEnabled:

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   Par exemple, pour désactiver le bouton **protéger** :

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   Pour activer le bouton **protéger** :

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>Activer le déchiffrement côté service des messages électroniques pour les utilisateurs de l'application de messagerie iOS

L'application de messagerie iOS ne peut pas déchiffrer les messages protégés avec le chiffrement de messages Office 365. En tant qu'administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les messages remis à l'application de messagerie iOS. Lorsque vous choisissez de le faire, le service envoie une copie déchiffrée du message au périphérique iOS. Le message est stocké déchiffré sur le périphérique client. Le message conserve également des informations sur les droits d'utilisation, même si l'application de messagerie iOS n'applique pas de droits d'utilisation côté client à l'utilisateur. Cela signifie que l'utilisateur peut copier ou imprimer le message même s'il ne dispose pas des droits nécessaires pour le faire. Toutefois, si l'utilisateur tente d'effectuer une action qui nécessite le serveur de messagerie Office 365, comme le transfert du message, le serveur n'autorise pas l'action si l'utilisateur n'a pas le droit d'utilisation à ce propos. Toutefois, les utilisateurs finaux peuvent contourner ne pas transférer la restriction d'utilisation en transférant le message à partir d'un autre compte dans son application de messagerie iOS. que vous configurez le déchiffrement côté service des messages, toutes les pièces jointes aux messages chiffrés et protégés par des droits. ne peut pas être affiché dans l'application de messagerie iOS.
  
Si vous choisissez de ne pas autoriser les messages déchiffrés à être envoyés aux utilisateurs de l'application de messagerie iOS, les utilisateurs reçoivent un message qui indique qu'ils ne disposent pas des droits pour afficher le message. Par défaut, le déchiffrement côté service des messages électroniques n'est pas activé.
  
Pour plus d'informations et pour une vue de l'expérience client, consultez la rubrique [afficher des messages chiffrés sur votre iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>Pour gérer si les utilisateurs de l'application de messagerie iOS peuvent afficher les messages protégés par le chiffrement de messages Office 365
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-ActiveSyncOrganizations avec le paramètre AllowRMSSupportForUnenlightenedApps:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   Par exemple, pour configurer le service afin de déchiffrer les messages avant qu'ils soient envoyés à des applications non prévues telles que l'application de messagerie iOS:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   Ou, pour configurer le service de sorte qu'il n'envoie pas de messages déchiffrés à des applications incorrectes:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>Activer le déchiffrement côté service des pièces jointes de courrier électronique pour les clients de messagerie de navigateur Web

En règle générale, lorsque vous utilisez le chiffrement de messages Office 365, les pièces jointes sont automatiquement chiffrées. En tant qu'administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les pièces jointes que les utilisateurs téléchargent à partir d'un navigateur Web.
  
Lorsque vous choisissez de le faire, le service envoie une copie déchiffrée du fichier sur l'appareil. Le message est toujours chiffré. La pièce jointe de courrier conserve également des informations sur les droits d'utilisation, même si le navigateur n'applique pas de droits d'utilisation côté client à l'utilisateur. Cela signifie que l'utilisateur peut copier ou imprimer la pièce jointe de courrier électronique même si, à l'origine, il ne dispose pas des droits nécessaires. Toutefois, si l'utilisateur tente d'effectuer une action qui nécessite le serveur de messagerie Office 365, comme le transfert de la pièce jointe, le serveur n'autorise pas l'action si l'utilisateur n'a pas le droit d'utilisation à ce propos.
  
Que vous configurez le déchiffrement côté service des pièces jointes, les pièces jointes aux messages chiffrés et protégés par des droits ne peuvent pas être affichées dans l'application de messagerie iOS.
  
Si vous choisissez de ne pas autoriser les pièces jointes déchiffrées, ce qui correspond à la valeur par défaut, les utilisateurs reçoivent un message qui indique qu'ils ne disposent pas des droits pour afficher la pièce jointe.
  
Pour plus d'informations sur la façon dont Office 365 implémente le chiffrement pour les messages électroniques et les pièces jointes avec l'option de chiffrement uniquement, reportez-vous à la rubrique [option chiffrer uniquement pour les messages électroniques.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>Pour gérer si les pièces jointes de courrier sont déchiffrées lors du téléchargement à partir d'un navigateur Web
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-IRMConfiguration avec le paramètre DecryptAttachmentFromPortal:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   Par exemple, pour configurer le service afin de déchiffrer les pièces jointes lorsqu'un utilisateur les télécharge à partir d'un navigateur Web:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   Pour configurer le service de sorte qu'il quitte les pièces jointes chiffrées lorsqu'il est téléchargé, procédez comme suit:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a>Personnalisation de l'apparence des messages électroniques et du portail OME

Pour plus d'informations sur la façon de personnaliser OME pour votre organisation, consultez la rubrique [Ajouter la marque de votre organisation à vos messages chiffrés](add-your-organization-brand-to-encrypted-messages.md).
  
## <a name="disabling-the-new-capabilities-for-ome"></a>DésActivation des nouvelles fonctionnalités pour OME

Nous espérons qu'il n'y parviendra pas, mais si vous le souhaitez, la désactivation des nouvelles fonctionnalités de OME est très simple. Tout d'abord, vous devez supprimer toutes les règles de flux de messagerie que vous avez créées qui utilisent les nouvelles fonctionnalités de OME. Pour plus d'informations sur la suppression des règles de flux de messagerie, consultez la rubrique [Manage mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Ensuite, effectuez ces étapes dans Exchange Online PowerShell.
  
### <a name="to-disable-the-new-capabilities-for-ome"></a>Pour désactiver les nouvelles fonctionnalités de OME
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Si vous avez activé le bouton **protéger** dans Outlook sur le Web, désactivez-le en exécutant la cmdlet Set-IRMConfiguration avec le paramètre SimplifiedClientAccessEnabled. Sinon, ignorez cette étape.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. DésActivez les nouvelles fonctionnalités de OME en exécutant l'applet de commande Set-IRMConfiguration avec le paramètre AzureRMSLicensingEnabled défini sur false:

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
