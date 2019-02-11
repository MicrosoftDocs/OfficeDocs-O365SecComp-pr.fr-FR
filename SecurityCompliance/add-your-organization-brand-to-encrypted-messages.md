---
title: Ajouter la marque de votre organisation à vos messages chiffrés
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: En tant qu’administrateur Exchange, vous pouvez appliquer aux messages électroniques chiffrés de votre organisation et le contenu du portail de chiffrement de personnalisation de votre organisation.
ms.openlocfilehash: 4b22b72a8b77c2978a7cf25166978759119c272c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696218"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Ajouter la marque de votre organisation à vos messages chiffrés

En tant qu’un administrateur Exchange Online ou Exchange Online Protection, vous pouvez appliquer à votre société pour personnaliser l’apparence des messages électroniques de chiffrement de messages Office 365 de votre organisation et le contenu du portail de chiffrement. Les applets de commande Get-OMEConfiguration et Set-OMEConfiguration Windows PowerShell, vous pouvez personnaliser les aspects suivants de l’expérience d’affichage pour les destinataires de messages électroniques chiffrés :
  
- Le texte d’introduction du message électronique contenant le message chiffré
- Le texte d’exclusion de responsabilité du message électronique contentant le message chiffré
- Texte qui apparaît dans le portail OME
- Logo qui apparaît dans le message électronique et le portail OME
- Couleur d’arrière-plan dans le message électronique et le portail OME

Vous pouvez également rétablir l’apparence par défaut à tout moment.

Si vous souhaitez plus de contrôle, vous pouvez créer plusieurs modèles pour les messages électroniques chiffrés provenant de votre organisation. À l’aide de ces modèles, vous pouvez contrôler plus que l’apparence des messages électroniques, mais également de contrôler les composants de l’expérience de l’utilisateur final. Par exemple, vous pouvez spécifier ou non destinataires de messagerie dont ce modèle est appliqué et qui utilisent Microsoft Accounts, Yahoo et Google peuvent utiliser ces comptes pour se connecter au portail Office 365 Message Encryption. Vous pouvez utiliser des modèles pour répondre à plusieurs cas d’utilisation, telles que :

- Modèles pour chaque service, par exemple Finance, ventes, etc. ;
- Modèles de différents produits
- Modèles pour différentes régions ou différents pays

Une fois que vous avez créé les modèles, vous pouvez les appliquer aux messages électroniques chiffrés à l’aide de règles de flux de messagerie Exchange. Tous les messages électroniques qui sont personnalisés à l’aide de ces modèles peuvent être révoqués.
  
||
|:-----|
|Cet article fait partie d’une plus grande série d’articles sur Office 365 Message Encryption. Cet article est destiné aux administrateurs et les professionnels de l’informatique. Si vous êtes simplement vous recherchez des informations sur l’envoi ou la réception d’un message chiffré, vous trouverez la liste des articles inclus dans [Office 365 Message Encryption (OME)](ome.md) et recherchez l’article qui vous convient le mieux à vos besoins. |
||

## <a name="create-branding-templates"></a>Créer des modèles de personnalisation

Vous créez des modèles de personnalisation pour votre organisation dans Windows PowerShell avec l’applet de commande New-OMEConfiguration. Une fois que vous avez créé le modèle, vous définissez les éléments du modèle à l’aide de l’applet de commande Set-OMEConfiguration. Vous pouvez créer plusieurs modèles.

![Composants de messagerie personnalisables](media/ome-template-breakout.png)
  
1. À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. L’applet de commande New-OMEConfiguration permet de créer un nouveau modèle.
     ```powershell
     New-OMEConfiguration -Identity <OMEConfigurationIdParameter>
     ```
     Par exemple,
     ```powershell
     New-OMEConfiguration -Identity <Branding template 1>
     ```
3. Définir les personnalisations pour le modèle que vous venez de définir à l’aide de l’applet de commande Set-OMEConfiguration comme décrit dans [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration) ou utilisez le tableau suivant pour obtenir des instructions.

|**Pour personnaliser cette fonctionnalité de l’expérience de chiffrement**|**Utilisez ces commandes**|
|:-----|:-----|
|Couleur d’arrière-plan  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formats de fichier pris en charge : .png, .jpg, .bmp ou .tiff  <br/> Taille optimale du fichier de logo : moins de 40 Ko  <br/> Taille optimale de l’image de logo : 170x70 pixels  <br/> |
|Texte en regard d’adresse e-mail et le nom de l’expéditeur| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -IntroductionText "<String up to 1024 characters>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|Texte qui apparaît sur le bouton « Lire le Message »| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -ReadButtonText "<String up to 1024 characters>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|Texte qui apparaît au-dessus, sous le bouton « Lire le Message »| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|Texte qui s’affiche en haut du portail d’affichage du message chiffré<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|Pour activer ou désactiver l’authentification avec un code d’accès unique pour ce modèle personnalisé| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -OTPEnabled <$true|$false>` <br/> **Exemples :** <br/>Pour activer les codes secrets unique pour ce modèle personnalisé <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> Pour désactiver les codes secrets unique pour ce modèle personnalisé <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|Pour activer ou désactiver l’authentification avec des identités Microsoft, Google ou Yahoo pour ce modèle personnalisé| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -SocialIdSignIn <$true|$false>` <br/> **Exemples :** <br/>Pour activer l’ID de mise en réseau pour ce modèle personnalisé <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> Pour désactiver la mise en réseau ID de ce modèle personnalisé <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="to-remove-brand-customizations-from-the-ome-portal-and-email-messages-encrypted-by-ome"></a>Pour supprimer les personnalisations de marque les messages OME portail et au courrier électronique chiffrés par OME
  
1. [Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Utilisez l’applet de commande Set-OMEConfiguration comme décrit dans [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration). Pour supprimer votre organisation de marque les personnalisations à partir de la DisclaimerText, EmailText, et les valeurs PortalText, définissez la valeur sur une chaîne vide, `""`. Pour tous les images des valeurs, telles que Logo, définissez la valeur sur `"$null"`.

**Options de personnalisation du chiffrement**

**Pour annuler cette fonctionnalité de chiffrement et rétablir le texte et l’image par défaut**|**Utilisez ces commandes**|
|:-----|:-----|
|Texte par défaut qui accompagne les messages électroniques chiffrés  <br/> Texte par défaut qui s’affiche au-dessus des instructions relatives à l’affichage des messages chiffrés| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
|Texte qui s’affiche en haut du portail d’affichage du message chiffré| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Revenir exemple par défaut :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logo| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Revenir exemple par défaut :** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
|Couleur d’arrière-plan| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Revenir exemple par défaut :** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|

## <a name="create-an-exchange-mail-flow-rule-that-applies-custom-branding-to-encrypted-emails"></a>Créer une règle de flux de messagerie Exchange qui s’applique de personnalisation pour les messages électroniques chiffrés

Une fois que vous avez créé un modèle de personnalisation, vous pouvez créer règles de flux de messagerie Exchange pour appliquer cette personnalisation en fonction de certaines conditions. Une telle règle appliquera design personnalisé dans les scénarios suivants :

- Si le message a été chiffré manuellement par l’utilisateur final à partir des clients Outlook ou OWA
- Si le message électronique a été automatiquement chiffré par une règle de flux de messagerie Exchange ou une stratégie de Data Loss Prevention Office 365

Pour plus d’informations sur la façon de créer une règle de flux de messagerie Exchange qui s’applique le chiffrement, consultez la rubrique [règles de flux de messagerie définir pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).

1. Dans un navigateur web, avec un compte professionnel ou de l’école bénéficie des autorisations d’administrateur global, [se connecter à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Choisissez la vignette de **l’administrateur** .

3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.

4. Dans le CAE, accédez à **flux de messagerie** \> **règles** et sélectionnez **Nouveau** ![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **créer une nouvelle règle**. Pour plus d’informations sur l’utilisation du centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Dans **nom**, tapez un nom pour la règle, comme la personnalisation pour le service commercial.

6. Dans **appliquer cette règle si** une condition, sélectionnez la condition que **l’expéditeur se trouve à l’intérieur de l’organisation** ainsi que d’autres conditions que vous souhaitez dans la liste des conditions disponibles. Par exemple, vous pouvez souhaiter appliquer un modèle particulier personnalisation :

     - Chiffrées tous les messages électroniques envoyés à partir de membres du service finance
     - Messages électroniques chiffrés envoyés avec un certain mot clé tels que « Partenaire » ou « Externe »
     - Messages électroniques chiffrés envoyés à un domaine spécifique

7. **Procédez comme suit**, sélectionnez **Modifier la sécurité des messages** > **appliquer de personnalisation pour les messages OME**. Ensuite, dans la liste déroulante, sélectionnez un modèle de personnalisation de ceux que vous avez créé.
8. (Facultatif) Si vous souhaitez que la règle de flux de messagerie également appliquer le chiffrement personnalisé en plus de personnalisation, **procédez comme suit**, sélectionnez **Modifier la sécurité des messages** , puis choisissez **Appliquer le chiffrement de messages Office 365 et de protection par des droits**. Sélectionnez un modèle RMS à partir de la liste, cliquez sur **Enregistrer**, puis cliquez sur **OK**.
  
     La liste des modèles inclut tous les modèles par défaut et les options, ainsi que des modèles personnalisés que vous avez créé pour utilisent par Office 365. Si la liste est vide, assurez-vous que vous avez configuré le chiffrement de messages Office 365 avec les nouvelles fonctionnalités comme décrit dans [installer les nouvelles fonctionnalités d’Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md). Pour plus d’informations sur les modèles par défaut, voir [configuration et gestion des modèles pour la Protection des informations Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Pour plus d’informations sur l’option **Ne pas transférer** , voir [l’option ne pas transférer les messages électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Pour plus d’informations sur l’option **chiffrer uniquement** , voir [option chiffrer uniquement pour les courriers électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

     Vous pouvez choisir **d’Ajouter une action** si vous souhaitez spécifier une autre action.
