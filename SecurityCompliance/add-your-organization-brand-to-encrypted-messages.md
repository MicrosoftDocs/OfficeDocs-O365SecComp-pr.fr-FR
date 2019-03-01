---
title: Ajouter la marque de votre organisation à vos messages chiffrés
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
ms.collection:
- M365-security-compliance
description: En tant qu'administrateur Exchange, vous pouvez appliquer la personnalisation de votre organisation aux messages électroniques chiffrés de votre organisation et au contenu du portail de chiffrement.
ms.openlocfilehash: b15bb058d68d0f1783d2a689fff180a2bf48023e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341705"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Ajouter la marque de votre organisation à vos messages chiffrés

En tant qu'administrateur Exchange Online ou Exchange Online Protection, vous pouvez appliquer votre marque de société pour personnaliser l'apparence des messages électroniques de chiffrement des messages Office 365 de votre organisation et le contenu du portail de chiffrement. À l'aide des applets de commande Windows PowerShell Get-OMEConfiguration et Set-OMEConfiguration, vous pouvez personnaliser les aspects suivants de l'expérience d'affichage pour les destinataires de messages électroniques chiffrés:
  
- Le texte d’introduction du message électronique contenant le message chiffré
- Le texte d’exclusion de responsabilité du message électronique contentant le message chiffré
- Texte qui apparaît dans le portail OME
- Logo qui apparaît dans le message électronique et dans le portail OME
- Couleur d'arrière-plan dans le message électronique et le portail OME

Vous pouvez également rétablir l’apparence par défaut à tout moment.

Si vous souhaitez davantage de contrôle, vous pouvez créer plusieurs modèles pour les messages électroniques chiffrés provenant de votre organisation. Ces modèles vous permettent de contrôler plus que l'apparence des messages électroniques, mais aussi de contrôler les éléments de l'expérience de l'utilisateur final. Par exemple, vous pouvez spécifier si les destinataires de messages auxquels ce modèle est appliqué et ceux qui utilisent Google, Yahoo et les comptes Microsoft peuvent utiliser ces comptes pour se connecter au portail de chiffrement de messages Office 365. Vous pouvez utiliser des modèles pour répondre à plusieurs cas d'utilisation, par exemple:

- Modèles pour chaque service, tels que finance, ventes, etc.
- Modèles pour différents produits
- Modèles pour différentes régions géographiques ou pays

Une fois que vous avez créé les modèles, vous pouvez les appliquer à des messages électroniques chiffrés à l'aide de règles de flux de messagerie Exchange. Tous les messages personnalisés à l'aide de ces modèles peuvent être révoqués.
  
||
|:-----|
|Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins.|
||

## <a name="create-branding-templates"></a>Créer des modèles de personnalisation

Vous créez des modèles de personnalisation pour votre organisation dans Windows PowerShell à l'aide de la cmdlet New-OMEConfiguration. Une fois que vous avez créé le modèle, vous définissez les éléments du modèle à l'aide de la cmdlet Set-OMEConfiguration. Vous pouvez créer plusieurs modèles.

![Composants de messagerie personnalisables](media/ome-template-breakout.png)
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Utilisez la cmdlet New-OMEConfiguration pour créer un nouveau modèle.

   ```powershell
   New-OMEConfiguration -Identity <OMEConfigurationIdParameter>
   ```
   Par exemple,

   ```powershell
   New-OMEConfiguration -Identity <Branding template 1>
   ```
3. Définissez les personnalisations pour le modèle que vous venez de définir à l'aide de la cmdlet Set-OMEConfiguration comme décrit dans [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration) ou utilisez le tableau suivant pour obtenir des instructions.

|**Pour personnaliser cette fonctionnalité de l’expérience de chiffrement**|**Utilisez ces commandes**|
|:-----|:-----|
|Couleur d'arrière-plan|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"`|
|Logo|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formats de fichier pris en charge : .png, .jpg, .bmp ou .tiff  <br/> Taille optimale du fichier de logo : moins de 40 Ko  <br/> Taille optimale de l’image de logo : 170x70 pixels|
|Texte en regard du nom et de l'adresse de messagerie de l'expéditeur|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -IntroductionText "<String up to 1024 characters>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|Texte qui apparaît sur le bouton «Lire le message»|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -ReadButtonText "<String up to 1024 characters>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|Texte qui apparaît au-dessus du bouton «Lire le message»|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|Texte qui s’affiche en haut du portail d’affichage du message chiffré|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."`|
|Pour activer ou désactiver l'authentification avec un code d'accès unique pour ce modèle personnalisé|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -OTPEnabled <$true|$false>` <br/> **Exemples :** <br/>Pour activer les codes secrets à usage unique pour ce modèle personnalisé <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> Pour désactiver les codes secrets à usage unique pour ce modèle personnalisé <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|Pour activer ou désactiver l'authentification avec des identités Microsoft, Google ou Yahoo pour ce modèle personnalisé|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -SocialIdSignIn <$true|$false>` <br/> **Exemples :** <br/>Pour activer les ID de mise en réseau pour ce modèle personnalisé <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> Pour désactiver les ID de mise en réseau pour ce modèle personnalisé <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="to-remove-brand-customizations-from-the-ome-portal-and-email-messages-encrypted-by-ome"></a>Pour supprimer les personnalisations de la marque du portail OME et des messages électroniques chiffrés par OME
  
1. [Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Utilisez la cmdlet **Set-OMEConfiguration** comme décrit dans [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration). Pour supprimer les personnalisations personnalisées de votre organisation des valeurs DisclaimerText, EmailText et PortalText, définissez la valeur sur une chaîne vide, `""`. Pour toutes les valeurs d'image, telles que logo, définissez la `"$null"`valeur sur.

**Options de personnalisation du chiffrement**

**Pour annuler cette fonctionnalité de chiffrement et rétablir le texte et l’image par défaut**|**Utilisez ces commandes**|
|:-----|:-----|
|Texte par défaut qui accompagne les messages électroniques chiffrés  <br/> Texte par défaut qui s’affiche au-dessus des instructions relatives à l’affichage des messages chiffrés|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
|Texte qui s’affiche en haut du portail d’affichage du message chiffré|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Exemple de rétablissement de la valeur par défaut:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""`|
|Logo|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Exemple de rétablissement de la valeur par défaut:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
|Couleur d'arrière-plan|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Exemple de rétablissement de la valeur par défaut:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|

## <a name="create-an-exchange-mail-flow-rule-that-applies-custom-branding-to-encrypted-emails"></a>Créer une règle de flux de messagerie Exchange qui applique une personnalisation aux courriers électroniques chiffrés

Une fois que vous avez créé un modèle de personnalisation, vous pouvez créer des règles de flux de messagerie Exchange pour appliquer cette personnalisation en fonction de certaines conditions. Une telle règle applique une personnalisation personnalisée dans les scénarios suivants:

- Si le courrier électronique a été chiffré manuellement par l'utilisateur final à partir des clients Outlook ou Outlook sur le Web (anciennement appelé Outlook Web App)
- Si le courrier électronique a été automatiquement chiffré par une règle de flux de messagerie Exchange ou une stratégie de protection contre la perte de données Office 365

Pour plus d'informations sur la création d'une règle de flux de messagerie Exchange qui applique le chiffrement, voir [définir des règles de flux de messagerie pour chiffrer des messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).

1. Dans un navigateur Web, à l'aide d'un compte professionnel ou scolaire auquel des autorisations d'administrateur général ont été accordées, [Connectez-vous à Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Sélectionnez la vignette **admin** .

3. Dans le Centre d'administration Office 365, choisissez **Centres d'administration** \> **Exchange**.

4. Dans le centre d'administration Exchange, accédez à **règles** de **flux** \> de messagerie et sélectionnez **nouvelle** ![icône](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **créer une nouvelle règle**. Pour plus d'informations sur l'utilisation du centre d'administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Dans **nom**, tapez un nom pour la règle, par exemple, personnalisation pour le service des ventes.

6. Dans **appliquer cette règle si** vous sélectionnez une condition, sélectionnez la condition que **l'expéditeur se trouve à l'intérieur de l'organisation** , ainsi que d'autres conditions de votre choix dans la liste des conditions disponibles. Par exemple, vous pouvez appliquer un modèle de personnalisation particulier à:

     - Tous les messages chiffrés envoyés par les membres du service financier
     - Messages chiffrés envoyés avec un mot clé tel que «externe» ou «partenaire»
     - Messages chiffrés envoyés à un domaine particulier

7. Dans **effectuer les opérations suivantes**, sélectionnez **modifier la sécurité** > des messages appliquer la personnalisation**aux messages OME**. Ensuite, dans la liste déroulante, sélectionnez un modèle de personnalisation parmi ceux que vous avez créés.
8. Module Si vous souhaitez que la règle de flux de messagerie applique également le chiffrement en plus de la personnalisation, dans **effectuer les opérations suivantes**, sélectionnez **modifier la sécurité des messages** , puis appliquer le chiffrement de **messages Office 365 et protection des droits**. Sélectionnez un modèle RMS dans la liste, cliquez sur **Enregistrer**, puis choisissez **OK**.
  
     La liste des modèles inclut tous les modèles et options par défaut, ainsi que tous les modèles personnalisés que vous avez créés pour être utilisés par Office 365. Si la liste est vide, vérifiez que vous avez configuré le chiffrement de messages Office 365 avec les nouvelles fonctionnalités, comme décrit dans la rubrique [set up New Office 365 message Encryption Capabilities](set-up-new-message-encryption-capabilities.md). Pour plus d'informations sur les modèles par défaut, reportez-vous à la rubrique [Configuring and Managing Templates for Azure information protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Pour plus d'informations sur l'option **ne pas transférer** , reportez-vous à l' [option ne pas transférer pour les messages électroniques](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Pour plus d'informations sur l'option **chiffrer uniquement** , reportez-vous à la rubrique [chiffrer uniquement](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

     Vous pouvez choisir **Ajouter une action** si vous souhaitez spécifier une autre action.
