---
title: Informations héritées pour le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
ms.assetid: 5986b9e1-c824-4f8f-9b7d-a2b0ae2a7fe9
description: Si vous n’avez pas encore déplacé votre organisation Office 365 pour les nouvelles fonctionnalités OME, mais vous avez déjà déployé OME, les informations contenues dans cet article s’applique à votre organisation. Microsoft vous recommande de vous un plan pour la déplacer vers les nouvelles fonctionnalités OME dès que possible pour votre organisation. Pour plus d’informations, voir la rubrique Set up des nouvelles fonctionnalités d’Office 365 Message Encryption greffées Azure la Protection des informations. Si vous souhaitez en savoir plus sur le fonctionnement tout d’abord les nouvelles fonctionnalités, voir Office 365 Message Encryption. Le reste de cet article fait référence au comportement OME avant la publication des nouvelles fonctionnalités OME.
ms.openlocfilehash: d5b21cbe0004ca7bda38085bd5d8ef5f2a22b04e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528188"
---
# <a name="legacy-information-for-office-365-message-encryption"></a>Informations héritées pour le chiffrement de messages Office 365

Si vous n’avez pas encore déplacé votre organisation Office 365 pour les nouvelles fonctionnalités OME, mais vous avez déjà déployé OME, les informations contenues dans cet article s’applique à votre organisation. Microsoft vous recommande de vous un plan pour la déplacer vers les nouvelles fonctionnalités OME dès que possible pour votre organisation. Pour plus d’informations, voir [configurer les nouvelles fonctionnalités d’Office 365 Message Encryption greffées Azure la Protection des informations](set-up-new-message-encryption-capabilities.md). Si vous souhaitez en savoir plus sur le fonctionnement tout d’abord les nouvelles fonctionnalités, voir [Office 365 Message Encryption](ome.md). Le reste de cet article fait référence au comportement OME avant la publication des nouvelles fonctionnalités OME.
  
Avec Office 365 Message Encryption, votre organisation peut envoyer et recevoir des messages électroniques chiffrés entre les personnes à l’intérieur et à l’extérieur de votre organisation. Office 365 Message Encryption fonctionne avec Outlook.com, Yahoo, Gmail et autres services de messagerie. Chiffrement des messages électroniques contribue à garantie que destiné uniquement les destinataires permettre afficher le contenu du message.
  
Voici quelques exemples :
  
- Un employé de banque envoie des relevés de carte de crédit aux clients
    
- Un représentant compagnie d’assurance fournit des détails de la stratégie pour les clients
    
- Un courtier emprunt demande des informations financières à partir d’un client pour une demande de prêt
    
- Un fournisseur de soins de santé envoie des informations de santé à des patients
    
- Quand un avocat envoie des informations confidentielles à un client ou un autre avocat
    
## <a name="how-office-365-message-encryption-works-without-the-new-capabilities"></a>Fonctionnement d’Office 365 Message Encryption sans les nouvelles fonctionnalités

Chiffrement de messages Office 365 est un service en ligne qui repose sur Microsoft Azure Rights Management (Services RMS Azure). Avec RMS Azure, les administrateurs peuvent définir des règles de flux de messagerie pour déterminer les conditions de chiffrement. Par exemple, une règle peut exiger le chiffrement de tous les messages adressés à un destinataire spécifique.
  
Regardez cette vidéo pour voir comment Office 365 Message Encryption fonctionne sans les nouvelles fonctionnalités.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c55540e7-f7f0-42f5-b254-4b2d2fbb1d63?autoplay=false]
  
Lorsqu’une personne envoie un message électronique dans Exchange Online qui correspond à une règle de chiffrement, le message est envoyé avec une pièce jointe HTML. Le destinataire ouvre la pièce jointe HTML et suivre les instructions pour afficher le message chiffré sur le portail Office 365 Message Encryption. Le destinataire peut choisir d’afficher le message en vous connectant avec un compte Microsoft ou une école associé à Office 365 ou de travail, ou à l’aide d’un code secret unique. Les deux options de vous assurer que seul le destinataire peut afficher le message chiffré. Ce processus est très différent pour les nouvelles fonctionnalités d’OME.
  
Le diagramme suivant résume le passage d’un message électronique dans le processus de chiffrement et de déchiffrement.
  
![Diagramme montrant le cheminement d’un message électronique chiffré](media/O365-Office365MessageEncryption-Concept.png)
  
Pour plus d’informations, voir [informations de Service de chiffrement de messages Office 365 hérité avant la publication de nouvelles fonctionnalités OME](legacy-information-for-message-encryption.md#LegacyServiceInfo).
  
## <a name="defining-mail-flow-rules-for-office-365-message-encryption-that-dont-use-the-new-ome-capabilities"></a>Définition des règles de flux de messagerie pour Office 365 Message Encryption qui n’utilisent pas les nouvelles fonctionnalités OME

Pour activer le chiffrement de messages Office 365 sans les nouvelles fonctionnalités, les administrateurs Exchange Online et Exchange Online Protection définissent des règles de flux de messagerie Exchange. Ces règles déterminent dans un message quelles conditions les messages doivent être chiffrées, ainsi que les conditions de suppression du chiffrement de message. Lorsqu’une action de chiffrement est définie pour une règle, tous les messages qui correspondent aux conditions de règle sont chiffrées avant qu’ils sont envoyés.
  
Règles de flux de messagerie sont flexibles, ce qui vous permet de combiner des conditions pour satisfaire des exigences de sécurité spécifiques dans une règle unique. Par exemple, vous pouvez créer une règle pour chiffrer tous les messages qui contiennent des mots clés spécifiés et sont adressés à des destinataires externes. Chiffrement de messages Office 365 chiffre également les réponses des destinataires des messages chiffrés, et vous pouvez créer une règle qui déchiffre les réponses en tant que pratique pour vos utilisateurs de messagerie. De cette façon, les utilisateurs dans votre organisation ne doivent se connecter au portail de chiffrement pour afficher les réponses.
  
Pour plus d’informations sur la façon de créer des règles de flux de messagerie Exchange, voir [Définir des règles pour Office 365 Message Encryption](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Envoyer, consulter et répondre à des messages électroniques chiffrés

Avec Office 365 Message Encryption, les messages électroniques sont chiffrés automatiquement, selon des règles définies par l’administrateur. Un message électronique qui porte un message chiffré arrive dans la boîte de réception du destinataire avec un fichier HTML joint.
  
Destinataires suivent les instructions indiquées dans le message pour ouvrir la pièce jointe et de s’authentifier en utilisant un compte Microsoft ou une école associé à Office 365 ou travail. Si le destinataire ne dispose d’un compte, ils sont dirigés pour créer un compte qui vous permet de les connecter pour afficher le message chiffré de Microsoft. Les destinataires peuvent également choisir obtenir un code d’accès unique pour afficher le message. Après l’ouverture de session ou à l’aide d’un code secret unique, les destinataires peuvent afficher le message déchiffré et envoyer une réponse chiffrée.
  
## <a name="customize-encrypted-messages-with-office-365-message-encryption"></a>Personnalisation des messages chiffrés avec Office 365 Message Encryption

En tant qu’un administrateur Exchange Online et Exchange Online Protection, vous pouvez personnaliser vos messages chiffrés. Par exemple, vous pouvez ajouter la marque de votre société et le logo, spécifiez une introduction et ajouter du texte de notification d’exclusion dans les messages chiffrés et dans le portail où destinataires afficher vos messages chiffrés. À l’aide des applets de commande Windows PowerShell, vous pouvez personnaliser les aspects suivants de l’expérience d’affichage pour les destinataires de messages électroniques chiffrés :
  
- Le texte d’introduction du message électronique contenant le message chiffré
    
- Le texte d’exclusion de responsabilité du message électronique contentant le message chiffré
    
- Le texte du portail qui apparaîtra dans le portail d’affichage des messages
    
- Le logo qui apparaîtra dans le message électronique et le portail d’affichage
    
Vous pouvez également rétablir l’apparence par défaut à tout moment.
  
L’exemple suivant montre un logo personnalisé pour ContosoPharma dans la pièce jointe d’un message électronique :
  
![Exemple de page de visualisation de message chiffré](media/TA-OME-3attachment2.jpg)
  
 **Pour personnaliser les messages électroniques chiffrés et le portail de chiffrement avec la marque de votre organisation**
  
1. Se connecter à Exchange Online à l’aide de Remote PowerShell, comme indiqué dans [se connecter à Exchange Online à l’aide de Remote PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated).
    
2. Utilisez l’applet de commande Set-OMEConfiguration comme décrit ici : [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) ou utilisez le tableau suivant pour obtenir des instructions. 
    
   **Options de personnalisation du chiffrement**

|**Pour personnaliser cette fonctionnalité de l’expérience de chiffrement**|**Utilisez ces commandes Windows PowerShell**|
|:-----|:-----|
|Texte par défaut qui accompagne les messages électroniques chiffrés  <br/> Texte par défaut qui s’affiche au-dessus des instructions relatives à l’affichage des messages chiffrés  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<string of up to 1024 characters>"` <br/> **Exemple :**`Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system"` <br/> |
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<your disclaimer statement, string of up to 1024 characters>"` <br/> **Exemple :**`Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only"` <br/> |
|Texte qui s’affiche en haut du portail d’affichage du message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<text for your portal, string of up to 128 characters>"` <br/> **Exemple :**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal"` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemple :**`Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formats de fichier pris en charge : .png, .jpg, .bmp ou .tiff  <br/> Taille optimale du fichier de logo : moins de 40 Ko  <br/> Taille optimale de l’image de logo : 170x70 pixels  <br/> |
   
 **Pour supprimer les personnalisations de la marque de messages électroniques chiffrés et le portail de chiffrement**
  
1. Se connecter à Exchange Online à l’aide de Remote PowerShell, comme indiqué dans [se connecter à Exchange Online à l’aide de Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Utilisez l’applet de commande Set-OMEConfiguration comme décrit ici : [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). Pour supprimer votre organisation de marque les personnalisations à partir de la DisclaimerText, EmailText, et les valeurs PortalText, définissez la valeur sur une chaîne vide, `""`. Pour tous les images des valeurs, telles que Logo, définissez la valeur sur `"$null"`.
    
   **Options de personnalisation du chiffrement**

|**Pour annuler cette fonctionnalité de chiffrement et rétablir le texte et l’image par défaut**|**Utilisez ces commandes Windows PowerShell**|
|:-----|:-----|
|Texte par défaut qui accompagne les messages électroniques chiffrés  <br/> Texte par défaut qui s’affiche au-dessus des instructions relatives à l’affichage des messages chiffrés  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemple :**`Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemple :**`Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Texte qui s’affiche en haut du portail d’affichage du message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Exemple retour à la valeur par défaut :**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Exemple retour à la valeur par défaut :**`Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
   
## <a name="service-information-for-legacy-office-365-message-encryption-prior-to-the-release-of-the-new-ome-capabilities"></a>Informations de service de chiffrement de messages Office 365 hérité dans les versions antérieures des nouvelles fonctionnalités OME
<a name="LegacyServiceInfo"> </a>

Le tableau suivant fournit des détails techniques pour le service de chiffrement de messages Office 365 avant la publication de nouvelles fonctionnalités OME.
  
|**Détails du service**|**Description**|
|:-----|:-----|
|Exigences relatives aux périphériques client  <br/> |Les messages chiffrés peuvent être affichés sur tous les périphériques client, tant que la pièce jointe HTML peut être ouverte dans un navigateur moderne qui prend en charge la publication de formulaire.  <br/> |
|Algorithme de chiffrement et conformité aux normes FIPS (Federal Information Processing Standards)  <br/> |Chiffrement de messages Office 365 utilise les mêmes clés de chiffrement en tant que Windows Azure Information Rights Management (IRM) et prend en charge le chiffrement Mode 2 (clé 2K pour RSA) et 256 bits pour les systèmes SHA-1. Pour plus d’informations sur les modes de chiffrement sous-jacent IRM, voir [Modes de chiffrement AD RMS](http://technet.microsoft.com/library/hh867439%28WS.10%29.aspx).<br/> |
|Types de messages pris en charge  <br/> |Chiffrement de messages Office 365 est uniquement pris en charge pour les éléments qui ont un ID de classe de message de **IPM. Remarque**. Pour plus d’informations, voir [types d’éléments et classes de message](https://msdn.microsoft.com/library/office/ff861573.aspx).<br/> |
|Tailles limites des messages  <br/> |Chiffrement de messages Office 365 peuvent chiffrer les messages de jusqu'à 25 Mo. Pour plus d’informations sur les tailles limites des messages, consultez la rubrique [Limites d’Exchange Online](http://technet.microsoft.com/library/exchange-online-limits.aspx).<br/> |
|Stratégies de rétention de messagerie Exchange Online  <br/> |Exchange Online ne stocke pas les messages chiffrés.  <br/> |
|Prise en charge linguistique pour le chiffrement de messages Office 365  <br/> | Le chiffrement de messages Office 365 prend en charge les langues d’Office 365 comme suit :  <br/>  Les messages électroniques entrants et fichiers HTML joints sont localisés en fonction des paramètres de langue de l’expéditeur.  <br/>  Le portail d’affichage est localisé en fonction des paramètres de navigateur du destinataire.  <br/>  Le corps (contenu) du message chiffré n’est pas localisé.  <br/> |
|Informations de confidentialité pour le portail OME et l’application Visionneuse OME  <br/> |La [Office 365 Messaging Encryption Portal privacy statement](protected-message-viewer-portal-privacy-statement.md) fournit des informations détaillées sur ce que fait et ne fait pas Microsoft avec vos informations privées.  <br/> |
   
## <a name="frequently-asked-questions-about-legacy-ome"></a>Forum aux Questions sur OME hérité
<a name="LegacyServiceInfo"> </a>

Vous avez des questions sur le chiffrement de messages Office 365 ? Voici quelques réponses. Si vous ne trouvez pas ce dont vous avez besoin, consultez les forums de la Communauté Office 365 au niveau de [la Communauté Office 365](http://community.office365.com/en-us/forums/default.aspx).
  
 **Q : Mes utilisateurs envoient des messages électroniques chiffrés à des destinataires extérieurs à votre organisation. Existe-t-il quelque chose destinataires externes ont à effectuer pour lire et répondre aux messages électroniques qui sont chiffrées avec le chiffrement de messages Office 365 ?**
  
Les destinataires externes à votre organisation qui reçoivent des messages chiffrés Office 365 peuvent les afficher de l’une des deux manières suivantes :
  
- En vous connectant avec un compte Microsoft ou un compte professionnel ou de l’école associé à Office 365.
    
- Code d’accès en utilisant un unique.
    
 **Q. Les messages électroniques chiffrés Office 365 sont-ils stockés dans le nuage ou sur les serveurs Microsoft ?**
  
Non, les messages chiffrés sont conservés sur le système de messagerie du destinataire, et lorsque le destinataire ouvre le message, celui-ci est publié temporairement pour l’affichage sur les serveurs Office 365. Les messages ne sont pas stockées il.
  
 **Q. Puis-je personnaliser les messages chiffrés avec ma marque ?**
  
Oui. Vous pouvez utiliser les cmdlets Windows PowerShell pour personnaliser le texte par défaut qui apparaît en haut des messages électroniques chiffrés, la clause d’exclusion de responsabilité et le logo que vous souhaitez utiliser pour le message électronique et le portail de chiffrement. Pour plus d’informations, voir [Add branding to encrypted messages](add-your-organization-brand-to-encrypted-messages.md).
  
 **Q. Le service exige-t-il une licence pour chaque utilisateur de mon organisation ?**
  
Une licence est obligatoire pour chaque utilisateur de l’organisation qui envoie des messages chiffrés.
  
 **Q. Les destinataires externes exigent-ils des abonnements ?**
  
Non, les destinataires externes n’ont pas besoin d’un abonnement pour lire ou répondre à des messages chiffrés. 
  
 **Q : comment est différent de Rights Management Services (RMS) Office 365 Message Encryption ?**
  
RMS fournit des fonctionnalités de Protection des droits des informations pour les courriers électroniques internes d’une organisation en fournissant des modèles intégrés, tels que : ne pas transférer et confidentiel. Chiffrement des messages électroniques Office 365 Message Encryption prend en charge pour les messages envoyés aux destinataires externes, ainsi que les destinataires internes.
  
 **Q : comment est différent de S/MIME Office 365 Message Encryption ?**
  
S/MIME est essentiellement une technologie de chiffrement côté client et exige une gestion de certificats et une infrastructure de publication complexes. Le chiffrement de messages Office 365 utilise des règles de transport et ne dépend pas de la publication de certificats.
  
 **Q. Puis-je lire les messages chiffrés sur des appareils mobiles ?**
  
Oui, vous pouvez afficher des messages sur Android et iOS en téléchargeant la visionneuse OME des applications à partir de la [lecture Google stocker](http://go.microsoft.com/fwlink/?LinkID=525995&amp;clcid=0x409) et l' [application Apple stocker](http://go.microsoft.com/fwlink/?LinkID=525996&amp;clcid=0x409). Ouvrez la pièce jointe HTML dans l’application Observateur OME et puis suivez les instructions pour ouvrir votre message chiffré. Pour d’autres périphériques mobiles, vous pouvez ouvrir la pièce jointe HTML tant que votre client de messagerie prend en charge la publication de formulaire.
  
 **Q. Les réponses et les messages transférés sont-ils chiffrés ?**
  
Oui. Les réponses restent chiffrées pendant toute la durée du thread.
  
 **Q. Le chiffrement de messages Office 365 fournit-il une localisation ?**
  
Le contenu HTML et les messages électroniques entrants sont localisés en fonction des paramètres de messagerie de l’expéditeur. Le portail d’affichage est localisé en fonction des paramètres de navigateur du destinataire. Cependant, le corps réel (le contenu) du message chiffré n’est pas localisé.
  
 **Q. Quel est la méthode de chiffrement de messages utilisée par Office 365 ?**
  
La fonction de chiffrement de messages d’Office 365 utilise RMS (Rights Management Services) comme infrastructure de chiffrement. La méthode de chiffrement utilisée dépend de l’endroit où vous obtenez les clés RMS servant à chiffrer et déchiffrer les messages.
  
- Si vous utilisez Microsoft Azure RMS pour obtenir les clés, chiffrement Mode 2 est utilisé. Chiffrement Mode 2 est une implémentation de chiffrement AD RMS mis à jour et améliorée. Il prend en charge 2048 RSA pour la signature et le chiffrement et SHA-256 pour la signature.
    
- Si vous utilisez Active Directory (AD) RMS pour obtenir les clés, le mode de chiffrement 1 ou 2 est utilisé. La méthode utilisée dépend de votre déploiement AD RMS local. Le mode de chiffrement 1 est le processus de chiffrement d’origine AD RMS. Il prend en charge RSA 1024 pour la signature et le chiffrement, et SHA-1 pour la signature. Ce mode est encore pris en charge par toutes les versions actuelles de RMS.
    
Pour plus d’informations, voir [Modes de chiffrement AD RMS](http://go.microsoft.com/fwlink/p/?LinkId=398616).
  
 **Q. Pourquoi certains messages chiffrés déclarent-ils provenir de l’adresse Office365@messaging.microsoft.com ?**
  
Lorsqu’une réponse chiffrée est envoyée à partir du portail de chiffrement ou via l’application Visionneuse OME, l’adresse de messagerie de l’expéditeur est définie sur Office365@messaging.microsoft.com, car le message chiffré est envoyé par le biais d’un point de terminaison Microsoft. Cela permet d’éviter que les messages chiffrés soient marqués comme courrier indésirable. Le nom affiché dans le message électronique et l’adresse dans le portail de chiffrement ne sont pas modifiés en raison de cet étiquetage. En outre, cet étiquetage s’applique uniquement aux messages envoyés via le portail, et non par le biais de n’importe quel autre client de messagerie.
  
 **Q : je suis un abonné Exchange Hosted Encryption (EHE). Où puis-je obtenir plus d’informations sur la mise à niveau vers Office 365 Message Encryption ?**
  
Tous les clients EHE ont été mis à niveau vers Office 365 Message Encryption. Pour plus d’informations, visitez le [Centre de mise à niveau du chiffrement Exchange hébergé](http://go.microsoft.com/fwlink/p/?LinkID=511077).
  
 **Q : ai-je besoin pour ouvrir des URL, adresses IP, ou les ports dans le pare-feu de votre organisation pour prendre en charge le chiffrement de messages Office 365 ?**
  
Oui. Vous devez ajouter des URL à la liste d’adresses autorisées pour Exchange Online afin que votre organisation permette l’authentification des messages chiffrés par Office 365. Pour obtenir la liste des URL Exchange Online, voir [Office 365 URLs and IP Address Ranges](https://support.office.com/article/f57e35b7-0a45-42f0-855e-11aa5e7f13fd.aspx)
  
 **Q : À combien de destinataires puis-je envoyer un message chiffré par Office 365 ?**
  
Le nombre maximal de destinataires pour un message chiffré est basé sur le nombre de caractères dans le champ **à** du message. Lorsqu’il est associé (après l’extension de liste de distribution), adresses des destinataires dans **le champ** ne doivent pas dépasser 11,980 caractères. Étant donné que les adresses de messagerie peuvent varier en caractères, il n’est pas un nombre maximal de destinataires standard pour un message chiffré. 
  
 **Q : Est-il possible de révoquer un message envoyé à un destinataire particulier ?**
  
Non. Vous ne pouvez pas annuler un message à une personne particulière après son envoi.
  
 **Q : Puis-je afficher un rapport des messages chiffrés qui ont été reçus et lus ?**
  
Il n’est pas un rapport qui indique si un message chiffré a été affiché, mais il existe des rapports Office 365 disponibles que vous pouvez exploiter pour déterminer le nombre de messages qui correspondent à une règle de transport spécifique, par exemple.
  
 **Q. Que fait Microsoft des informations que je fournis par le biais du portail OME et de l’application Visionneuse OME ?**
  
[déclaration de confidentialité de portail de chiffrement de messagerie Office 365](protected-message-viewer-portal-privacy-statement.md) fournit des informations détaillées sur ce que Microsoft fait et ne fait pas avec vos informations personnelles. 
  

