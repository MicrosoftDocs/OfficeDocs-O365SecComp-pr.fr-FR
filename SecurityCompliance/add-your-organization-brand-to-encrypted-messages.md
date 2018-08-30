---
title: Ajouter la marque de votre organisation à vos messages chiffrés
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/2/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: 'En tant qu’administrateur Exchange, vous pouvez appliquer aux messages électroniques chiffrés de votre organisation et le contenu du portail de chiffrement de personnalisation de votre organisation. '
ms.openlocfilehash: 2f34b5cea3155f587fd7787f1f69270d1373400b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528120"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Ajouter la marque de votre organisation à vos messages chiffrés

En tant qu’un administrateur Exchange Online ou Exchange Online Protection, vous pouvez appliquer à votre société pour personnaliser l’apparence des messages électroniques de chiffrement de messages Office 365 de votre organisation et le contenu du portail de chiffrement. Les applets de commande Get-OMEConfiguration et Set-OMEConfiguration Windows PowerShell, vous pouvez personnaliser les aspects suivants de l’expérience d’affichage pour les destinataires de messages électroniques chiffrés :
  
- Le texte d’introduction du message électronique contenant le message chiffré
    
- Le texte d’exclusion de responsabilité du message électronique contentant le message chiffré
    
- Texte qui apparaît dans le portail OME
    
- Logo qui apparaît dans le message électronique et le portail OME
    
- Couleur d’arrière-plan dans le message électronique et le portail OME
    
Vous pouvez également rétablir l’apparence par défaut à tout moment.
  
||
|:-----|
|Cet article fait partie d’une plus grande série d’articles sur Office 365 Message Encryption. Cet article est destiné aux administrateurs et les professionnels de l’informatique. Si vous êtes simplement vous recherchez des informations sur l’envoi ou la réception d’un message chiffré, vous trouverez la liste des articles inclus dans [Office 365 Message Encryption (OME)](ome.md) et recherchez l’article qui vous convient le mieux à vos besoins. |
||
   
**Pour personnaliser l’apparence des OME portail et au courrier électronique messages chiffrés par OME avec la marque de votre organisation**
  
1. Se connecter à Exchange Online à l’aide de Remote PowerShell, comme indiqué dans [se connecter à Exchange Online à l’aide de Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Utilisez l’applet de commande Set-OMEConfiguration comme décrit dans [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) ou utilisez le tableau suivant pour obtenir des instructions. 
    
**Options de personnalisation du chiffrement**

|**Pour personnaliser cette fonctionnalité de l’expérience de chiffrement**|**Utilisez ces commandes**|
|:-----|:-----|
|Texte par défaut qui accompagne les messages électroniques chiffrés. Le texte par défaut s’affiche au-dessus les instructions pour l’affichage des messages chiffrés  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only."` <br/> |
|Texte qui s’affiche en haut du portail d’affichage du message chiffré<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formats de fichier pris en charge : .png, .jpg, .bmp ou .tiff  <br/> Taille optimale du fichier de logo : moins de 40 Ko  <br/> Taille optimale de l’image de logo : 170x70 pixels  <br/> |
|Couleur d’arrière-plan  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -BackgroundColor "#ffffff"` <br/> |
   
**Pour supprimer les personnalisations de marque les messages OME portail et au courrier électronique chiffrés par OME**
  
1. Se connecter à Exchange Online à l’aide de Remote PowerShell, comme indiqué dans [se connecter à Exchange Online à l’aide de Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Utilisez l’applet de commande Set-OMEConfiguration comme décrit dans [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). Pour supprimer votre organisation de marque les personnalisations à partir de la DisclaimerText, EmailText, et les valeurs PortalText, définissez la valeur sur une chaîne vide, `""`. Pour tous les images des valeurs, telles que Logo, définissez la valeur sur `"$null"`.
    
**Options de personnalisation du chiffrement**

**Pour annuler cette fonctionnalité de chiffrement et rétablir le texte et l’image par défaut**|**Utilisez ces commandes**|
|:-----|:-----|
|Texte par défaut qui accompagne les messages électroniques chiffrés  <br/> Texte par défaut qui s’affiche au-dessus des instructions relatives à l’affichage des messages chiffrés  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemple :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Texte qui s’affiche en haut du portail d’affichage du message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Revenir exemple par défaut :** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Revenir exemple par défaut :** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
|Couleur d’arrière-plan  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Revenir exemple par défaut :** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null` <br/> |
   

