---
title: Gérer le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 5/8/2019
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Une fois que vous avez terminé la configuration d’Office 365 message Encryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons. Par exemple, vous pouvez configurer s’il faut activer des codes de passe unique, afficher le bouton protéger dans Outlook sur le Web, et bien plus encore. Les tâches décrites dans cet article expliquent comment procéder.
ms.openlocfilehash: 1afaaea3cd744878630598acd3f02dc7dc70e9cb
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834923"
---
# <a name="manage-office-365-message-encryption"></a>Gérer le chiffrement de messages Office 365

Une fois que vous avez terminé la configuration d’Office 365 message Encryption (OME), vous pouvez personnaliser la configuration de votre déploiement de plusieurs façons. Par exemple, vous pouvez configurer s’il faut activer des codes de passe unique, afficher le bouton **protéger** dans Outlook sur le Web, et bien plus encore. Les tâches décrites dans cet article expliquent comment procéder.

## <a name="manage-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Gérer si Google, Yahoo et les destinataires de comptes Microsoft peuvent utiliser ces comptes pour se connecter au portail de chiffrement des messages Office 365

Lorsque vous configurez les nouvelles fonctionnalités de chiffrement de messages Office 365, les utilisateurs de votre organisation peuvent envoyer des messages à des destinataires qui se trouvent en dehors de votre organisation Office 365. Si le destinataire utilise un *ID* de société comme un compte Google, un compte Yahoo ou un compte Microsoft, le destinataire peut se connecter au portail OME à l’aide d’un identifiant social. Si vous le souhaitez, vous pouvez choisir de ne pas autoriser les destinataires à utiliser des ID sociaux pour se connecter au portail OME.
  
### <a name="to-manage-whether-recipients-can-use-social-ids-to-sign-in-to-the-ome-portal"></a>Pour savoir si les destinataires peuvent utiliser des ID sociaux pour se connecter au portail OME
  
1. [Connectez-vous à Exchange Online à l’aide de Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).

2. Exécutez la cmdlet Set-OMEConfiguration avec le paramètre SocialIdSignIn comme suit:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -SocialIdSignIn <$true|$false>
   ```

   Par exemple, pour désactiver les ID de mise en réseau:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   Pour activer les ID de mise en réseau:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="manage-the-use-of-one-time-pass-codes-for-the-office-365-message-encryption-portal"></a>Gérer l’utilisation de codes d’accès unique pour le portail de chiffrement des messages Office 365

Si le destinataire d’un message chiffré par OME n’utilise pas Outlook, quel que soit le compte utilisé par le destinataire, le destinataire reçoit un lien d’affichage Web de temps limité qui lui permet de lire le message. Ce lien inclut un code d’accès unique. En tant qu’administrateur, vous pouvez décider si les destinataires peuvent utiliser des codes de transmission à usage unique pour se connecter au portail OME.
  
### <a name="to-manage-whether-ome-generates-one-time-pass-codes"></a>Pour gérer si OME génère des codes d’accès en une seule fois
  
1. Utilisez un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365 et démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-OMEConfiguration avec le paramètre OTPEnabled:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   Par exemple, pour désactiver les codes d’accès à usage unique:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   Pour activer les codes d’accès à usage unique:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="manage-the-display-of-the-protect-button-in-outlook-on-the-web"></a>Gérer l’affichage du bouton protéger dans Outlook sur le Web

Le bouton **protéger** dans Outlook sur le Web est désactivé lorsque vous configurez ome. En tant qu’administrateur, vous pouvez gérer l’affichage de ce bouton pour les utilisateurs finaux.
  
### <a name="to-manage-whether-the-protect-button-appears-in-outlook-on-the-web"></a>Pour gérer l’affichage du bouton protéger dans Outlook sur le Web
  
1. Utilisez un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365 et démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

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

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>Activer le déchiffrement côté service des messages électroniques pour les utilisateurs de l’application de messagerie iOS

L’application de messagerie iOS ne peut pas déchiffrer les messages protégés avec le chiffrement de messages Office 365. En tant qu’administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les messages remis à l’application de messagerie iOS. Lorsque vous choisissez d’utiliser le déchiffrement côté service, le service envoie une copie déchiffrée du message à l’appareil iOS. L’appareil client stocke une copie déchiffrée du message. Le message conserve également des informations sur les droits d’utilisation, même si l’application de messagerie iOS n’applique pas de droits d’utilisation côté client à l’utilisateur. L’utilisateur peut copier ou imprimer le message même s’il ne dispose pas des droits nécessaires pour le faire. Toutefois, si l’utilisateur tente d’effectuer une action qui nécessite le serveur de messagerie Office 365, par exemple le transfert du message, le serveur n’autorise pas l’action si l’utilisateur n’a pas le droit d’utilisation. Toutefois, les utilisateurs finaux peuvent contourner les restrictions d’utilisation «ne pas transférer» en transférant le message à partir d’un compte différent au sein de l’application de messagerie iOS. Que vous configurez le déchiffrement côté service du courrier, les pièces jointes aux messages chiffrés et protégés par des droits ne peuvent pas être visualisées dans l’application de messagerie iOS.
  
Si vous choisissez de ne pas autoriser les messages déchiffrés à être envoyés aux utilisateurs de l’application de messagerie iOS, les utilisateurs reçoivent un message qui indique qu’ils ne disposent pas des droits pour afficher le message. Par défaut, le déchiffrement côté service des messages électroniques n’est pas activé.
  
Pour plus d’informations et pour une vue de l’expérience client, consultez la rubrique [afficher des messages chiffrés sur votre iPhone ou iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).
  
### <a name="to-manage-whether-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>Pour gérer si les utilisateurs de l’application de messagerie iOS peuvent afficher les messages protégés par le chiffrement de messages Office 365
  
1. Utilisez un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365 et démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-ActiveSyncOrganizations avec le paramètre AllowRMSSupportForUnenlightenedApps:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   Par exemple, pour configurer le service afin de déchiffrer les messages avant qu’ils soient envoyés à des applications non satisfaites, telles que l’application de messagerie iOS:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   Ou, pour configurer le service de sorte qu’il n’envoie pas de messages déchiffrés à des applications incorrectes:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>Activer le déchiffrement côté service des pièces jointes de courrier électronique pour les clients de messagerie de navigateur Web

En règle générale, lorsque vous utilisez le chiffrement de messages Office 365, les pièces jointes sont automatiquement chiffrées. En tant qu’administrateur Office 365, vous pouvez appliquer le déchiffrement côté service pour les pièces jointes que les utilisateurs téléchargent à partir d’un navigateur Web.
  
Lorsque vous utilisez le déchiffrement côté service, le service envoie une copie déchiffrée du fichier sur l’appareil. Le message est toujours chiffré. La pièce jointe conserve également des informations sur les droits d’utilisation, même si le navigateur n’applique pas de droits d’utilisation côté client à l’utilisateur. L’utilisateur peut copier ou imprimer la pièce jointe du message, même s’il ne dispose pas des droits nécessaires pour le faire. Toutefois, si l’utilisateur tente d’effectuer une action qui nécessite le serveur de messagerie Office 365, comme le transfert de la pièce jointe, le serveur n’autorise pas l’action si l’utilisateur n’a pas le droit d’utilisation à ce propos.
  
Que vous configurez le déchiffrement côté service des pièces jointes, les utilisateurs ne peuvent pas afficher les pièces jointes aux messages chiffrés et protégés par des droits dans l’application de messagerie iOS.
  
Si vous choisissez de ne pas autoriser les pièces jointes déchiffrées, ce qui correspond à la valeur par défaut, les utilisateurs reçoivent un message qui indique qu’ils ne disposent pas des droits pour afficher la pièce jointe.
  
Pour plus d’informations sur la façon dont Office 365 implémente le chiffrement pour les messages électroniques et les pièces jointes avec l’option de chiffrement uniquement, reportez-vous à la rubrique [option chiffrer uniquement pour les messages électroniques.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
### <a name="to-manage-whether-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>Pour gérer si les pièces jointes sont déchiffrées lors du téléchargement à partir d’un navigateur Web
  
1. Utilisez un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365 et démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-IRMConfiguration avec le paramètre DecryptAttachmentFromPortal:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   Par exemple, pour configurer le service afin de déchiffrer les pièces jointes lorsqu’un utilisateur les télécharge à partir d’un navigateur Web:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   Pour configurer le service de sorte qu’il quitte les pièces jointes chiffrées lorsqu’il est téléchargé, procédez comme suit:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail--office-365-advanced-message-encryption-only"></a>Vérifier que tous les destinataires externes utilisent le portail OME pour lire le courrier chiffré — Office 365 Advanced message Encryption only

Si vous disposez d’Office 365 Advanced message Encryption, vous pouvez utiliser des modèles personnalisés pour obliger les destinataires à recevoir un message de wrapper qui les oblige à lire des messages chiffrés dans le portail OME au lieu d’utiliser Outlook ou Outlook sur le Web. Vous souhaiterez peut-être procéder ainsi si vous avez besoin d’un plus grand contrôle sur la façon dont les destinataires utilisent les messages qu’ils reçoivent. Par exemple, si des destinataires externes affichent le courrier électronique dans le portail Web, vous pouvez définir une date d’expiration pour le courrier électronique et vous pouvez révoquer le courrier électronique. Ces fonctionnalités sont uniquement prises en charge par le biais du portail OME. Vous pouvez utiliser l’option chiffrer et l’option ne pas transférer lors de la création des règles de flux de messagerie.

### <a name="create-a-custom-template-to-force-all-external-recipients-to-use-the-ome-portal-and-for-encrypted-email-to-be-revocable-and-expire-in-7-days"></a>Créer un modèle personnalisé pour obliger tous les destinataires externes à utiliser le portail OME et à révocabler les messages chiffrés et à les expirer dans 7 jours

1. Utilisez un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365 et démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet New-OMEConfiguration:

   ```powershell
   New-OMEConfiguration -Identity "<template name>" -ExternalMailExpiryInDays 7
   ```

   où `template name` est le nom que vous souhaitez utiliser pour le modèle de personnalisation de Message Office 365. For example,

   ```powershell
   New-OMEConfiguration -Identity "<One week expiration>" -ExternalMailExpiryInDays 7
   ```

3. Exécutez la cmdlet New-TransportRule:

   ```powershell
   New-TransportRule -name "<mail flow rule name>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "<option name>" -ApplyRightsProtectionCustomizationTemplate "<template name>"
   ```

    oà¹ :

   - `mail flow rule name`est le nom que vous souhaitez utiliser pour la nouvelle règle de flux de messagerie.

   - `option name`est soit `Encrypt` ou `Do Not Forward`.

   - `template name`est le nom que vous avez attribué au modèle personnalisé, par exemple `One week expiration`.

   Pour chiffrer tous les messages électroniques externes avec le modèle «expiration d’une semaine» et appliquer l’option de chiffrement uniquement:

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Encrypt" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

   Pour chiffrer tous les messages électroniques externes avec le modèle «expiration d’une semaine» et appliquer l’option ne pas transférer:

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Do Not Forward" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

## <a name="customize-the-appearance-of-email-messages-and-the-ome-portal"></a>Personnaliser l’apparence des messages électroniques et le portail OME

Pour plus d’informations sur la façon de personnaliser OME pour votre organisation, consultez la rubrique [Ajouter la marque de votre organisation à vos messages chiffrés](add-your-organization-brand-to-encrypted-messages.md).
  
## <a name="disable-the-new-capabilities-for-ome"></a>Désactiver les nouvelles fonctionnalités pour OME

Nous espérons qu’il n’y parviendra pas, mais si vous le souhaitez, la désactivation des nouvelles fonctionnalités de OME est très simple. Tout d’abord, vous devez supprimer toutes les règles de flux de messagerie que vous avez créées qui utilisent les nouvelles fonctionnalités de OME. Pour plus d’informations sur la suppression des règles de flux de messagerie, consultez la rubrique [Manage mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Ensuite, effectuez ces étapes dans Exchange Online PowerShell.
  
### <a name="to-disable-the-new-capabilities-for-ome"></a>Pour désactiver les nouvelles fonctionnalités de OME
  
1. À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Si vous avez activé le bouton **protéger** dans Outlook sur le Web, désactivez-le en exécutant la cmdlet Set-IRMConfiguration avec le paramètre SimplifiedClientAccessEnabled. Sinon, ignorez cette étape.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. Désactivez les nouvelles fonctionnalités de OME en exécutant l’applet de commande Set-IRMConfiguration avec le paramètre AzureRMSLicensingEnabled défini sur false:

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
