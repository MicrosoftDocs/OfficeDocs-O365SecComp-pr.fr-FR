---
title: Informations héritées pour le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.assetid: 5986b9e1-c824-4f8f-9b7d-a2b0ae2a7fe9
description: Si vous n'avez pas encore déplacé votre organisation Office 365 vers les nouvelles fonctionnalités OME, mais que vous avez déjà déployé OME, les informations contenues dans cet article s'appliquent à votre organisation. Microsoft vous recommande de planifier la migration vers les nouvelles fonctionnalités de OME dès que cela est raisonnable pour votre organisation. Pour obtenir des instructions, consultez la rubrique Set up New Office 365 message enCryption Capabilities Built-Top of Azure information protection. Si vous souhaitez en savoir plus sur la façon dont les nouvelles fonctionnalités fonctionnent en premier, consultez la rubrique Office 365 message enCryption. Le reste de cet article fait référence au comportement d'OME avant la publication des nouvelles fonctionnalités OME.
ms.openlocfilehash: 1f809ca996f072269f40bcb6c7ce6f7a420cccb1
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219254"
---
# <a name="legacy-information-for-office-365-message-encryption"></a>Informations héritées pour le chiffrement de messages Office 365

Si vous n'avez pas encore déplacé votre organisation Office 365 vers les nouvelles fonctionnalités OME, mais que vous avez déjà déployé OME, les informations contenues dans cet article s'appliquent à votre organisation. Microsoft vous recommande de planifier la migration vers les nouvelles fonctionnalités de OME dès que cela est raisonnable pour votre organisation. Pour obtenir des instructions, consultez la rubrique [set up New Office 365 message Encryption Capabilities Built-Top of Azure information protection](set-up-new-message-encryption-capabilities.md). Si vous souhaitez en savoir plus sur la façon dont les nouvelles fonctionnalités fonctionnent en premier, consultez la rubrique [Office 365 message](ome.md)Encryption. Le reste de cet article fait référence au comportement d'OME avant la publication des nouvelles fonctionnalités OME.
  
Avec le chiffrement de messages Office 365, votre organisation peut envoyer et recevoir des messages électroniques chiffrés entre des personnes à l'intérieur et à l'extérieur de votre organisation. Le chiffrement de messages Office 365 fonctionne avec Outlook.com, Yahoo, Gmail et d'autres services de messagerie. Le chiffrement des messages électroniques permet de s'assurer que seuls les destinataires prévus peuvent afficher le contenu du message.
  
Voici quelques exemples :
  
- Un employé de la banque envoie des relevés de carte de crédit aux clients.
    
- Un représentant de société d'assurance fournit des informations de stratégie aux clients
    
- Un courtier hypothécaire demande des informations financières à un client pour une demande de prêt
    
- Un fournisseur de soins d'intégrité envoie des informations médicales aux patients.
    
- Un avocat envoie des informations confidentielles à un client ou à un autre avocat
    
## <a name="how-office-365-message-encryption-works-without-the-new-capabilities"></a>Fonctionnement du chiffrement de messages Office 365 sans les nouvelles fonctionnalités

Le chiffrement de messages Office 365 est un service en ligne qui repose sur Microsoft Azure Rights Management (Azure RMS). Avec Azure RMS, les administrateurs peuvent définir des règles de flux de messagerie pour déterminer les conditions de chiffrement. Par exemple, une règle peut exiger le chiffrement de tous les messages adressés à un destinataire spécifique.
  
Regardez cette courte vidéo pour voir comment le chiffrement de messages Office 365 fonctionne sans les nouvelles fonctionnalités.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c55540e7-f7f0-42f5-b254-4b2d2fbb1d63?autoplay=false]
  
Lorsqu'une personne envoie un message électronique dans Exchange Online qui correspond à une règle de chiffrement, le message est envoyé avec une pièce jointe HTML. Le destinataire ouvre la pièce jointe HTML et suit les instructions pour afficher le message chiffré sur le portail de chiffrement des messages Office 365. Le destinataire peut choisir d'afficher le message en se connectant à l'aide d'un compte Microsoft ou d'un travail ou d'un établissement scolaire associé à Office 365, ou à l'aide d'un code d'accès unique. Ces deux options permettent de s'assurer que seul le destinataire concerné peut consulter le message chiffré. Ce processus est très différent pour les nouvelles fonctionnalités de OME.
  
Le diagramme suivant résume le passage d’un message électronique dans le processus de chiffrement et de déchiffrement.
  
![Diagramme montrant le cheminement d’un message électronique chiffré](media/O365-Office365MessageEncryption-Concept.png)
  
Pour plus d'informations, consultez les [informations de service pour le chiffrement de messages Office 365 hérité avant la publication des nouvelles fonctionnalités OME](legacy-information-for-message-encryption.md#LegacyServiceInfo).
  
## <a name="defining-mail-flow-rules-for-office-365-message-encryption-that-dont-use-the-new-ome-capabilities"></a>Définition des règles de flux de messagerie pour le chiffrement de messages Office 365 qui n'utilisent pas les nouvelles fonctionnalités OME

Pour activer le chiffrement des messages Office 365 sans les nouvelles fonctionnalités, les administrateurs Exchange Online et Exchange Online Protection définissent les règles de flux de messagerie Exchange. Ces règles déterminent les conditions dans lesquelles les messages électroniques doivent être chiffrés, ainsi que les conditions de suppression du chiffrement de messages. Lorsqu'une action de chiffrement est définie pour une règle, tous les messages qui correspondent aux conditions de la règle sont chiffrés avant d'être envoyés.
  
Les règles de flux de messagerie sont flexibles, ce qui vous permet de combiner des conditions afin de répondre à des exigences spécifiques en matière de sécurité dans une seule règle. Par exemple, vous pouvez créer une règle pour chiffrer tous les messages qui contiennent des mots clés spécifiés et qui sont adressés à des destinataires externes. Le chiffrement de messages Office 365 chiffre également les réponses provenant de destinataires de messages chiffrés, et vous pouvez créer une règle qui déchiffre les réponses à des fins de commodité pour vos utilisateurs de messagerie. De cette façon, les utilisateurs de votre organisation n'ont pas besoin de se connecter au portail de chiffrement pour afficher les réponses.
  
Pour plus d'informations sur la création de règles de flux de messagerie Exchange, voir [define Rules for Office 365 message](define-mail-flow-rules-to-encrypt-email.md)Encryption.
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Envoyer, consulter et répondre à des messages électroniques chiffrés

Avec le chiffrement de messages Office 365, les messages électroniques sont chiffrés automatiquement, en fonction des règles définies par l'administrateur. Un message électronique comportant un message chiffré arrive dans la boîte de réception du destinataire avec un fichier HTML joint.
  
Les destinataires suivent les instructions contenues dans le message pour ouvrir la pièce jointe et s'authentifier à l'aide d'un compte Microsoft ou d'un travail ou d'un établissement scolaire associé à Office 365. Si les destinataires n'ont pas de compte, ils sont dirigés vers la création d'un compte Microsoft qui leur permet de se connecter pour afficher le message chiffré. Par ailleurs, les destinataires peuvent choisir d'obtenir un code d'accès unique pour afficher le message. Une fois que vous vous êtes connecté ou que vous avez utilisé un code d'accès unique, les destinataires peuvent afficher le message déchiffré et envoyer une réponse chiffrée.
  
## <a name="customize-encrypted-messages-with-office-365-message-encryption"></a>Personnaliser les messages chiffrés avec le chiffrement de messages Office 365

En tant qu'administrateur Exchange Online et Exchange Online Protection, vous pouvez personnaliser vos messages chiffrés. Par exemple, vous pouvez ajouter la marque et le logo de votre entreprise, spécifier une introduction et ajouter le texte de la clause d'exclusion de responsabilité dans les messages chiffrés et dans le portail où les destinataires affichent vos messages chiffrés. À l'aide des applets de commande Windows PowerShell, vous pouvez personnaliser les aspects suivants de l'expérience d'affichage pour les destinataires de messages électroniques chiffrés:
  
- Le texte d’introduction du message électronique contenant le message chiffré
    
- Le texte d’exclusion de responsabilité du message électronique contentant le message chiffré
    
- Le texte du portail qui apparaîtra dans le portail d’affichage des messages
    
- Le logo qui apparaîtra dans le message électronique et le portail d’affichage
    
Vous pouvez également rétablir l’apparence par défaut à tout moment.
  
L’exemple suivant montre un logo personnalisé pour ContosoPharma dans la pièce jointe d’un message électronique :
  
![Exemple de page de visualisation de message chiffré](media/TA-OME-3attachment2.jpg)
  
 **Pour personnaliser les messages électroniques de chiffrement et le portail de chiffrement avec la marque de votre organisation**
  
1. Connectez-vous à Exchange Online à l'aide de Remote PowerShell, comme décrit dans [connexion à Exchange Online à l'aide de Remote PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated).
    
2. Utilisez la cmdlet Set-OMEConfiguration comme décrit ici: [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) ou utilisez le tableau suivant pour obtenir des instructions. 
    
   **Options de personnalisation du chiffrement**

|**Pour personnaliser cette fonctionnalité de l’expérience de chiffrement**|**Utilisez ces commandes Windows PowerShell**|
|:-----|:-----|
|Texte par défaut qui accompagne les messages électroniques chiffrés  <br/> Texte par défaut qui s’affiche au-dessus des instructions relatives à l’affichage des messages chiffrés  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<string of up to 1024 characters>"` <br/> **Exemple :** `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system"` <br/> |
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<your disclaimer statement, string of up to 1024 characters>"` <br/> **Exemple :** `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only"` <br/> |
|Texte qui s’affiche en haut du portail d’affichage du message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<text for your portal, string of up to 128 characters>"` <br/> **Exemple :** `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal"` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Exemple :** `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Formats de fichier pris en charge : .png, .jpg, .bmp ou .tiff  <br/> Taille optimale du fichier de logo : moins de 40 Ko  <br/> Taille optimale de l’image de logo : 170x70 pixels  <br/> |
   
 **Pour supprimer les personnalisations de la marque du chiffrement des messages électroniques et du portail de chiffrement**
  
1. Connectez-vous à Exchange Online à l'aide de Remote PowerShell, comme décrit dans [connexion à Exchange Online à l'aide de Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Utilisez la cmdlet Set-OMEConfiguration comme décrit ici: [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). Pour supprimer les personnalisations personnalisées de votre organisation des valeurs DisclaimerText, EmailText et PortalText, définissez la valeur sur une chaîne vide, `""`. Pour toutes les valeurs d'image, telles que logo, définissez la `"$null"`valeur sur.
    
   **Options de personnalisation du chiffrement**

|**Pour annuler cette fonctionnalité de chiffrement et rétablir le texte et l’image par défaut**|**Utilisez ces commandes Windows PowerShell**|
|:-----|:-----|
|Texte par défaut qui accompagne les messages électroniques chiffrés  <br/> Texte par défaut qui s’affiche au-dessus des instructions relatives à l’affichage des messages chiffrés  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Exemple :** `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Déclaration de non-responsabilité du message électronique qui contient le message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Exemple :** `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Texte qui s’affiche en haut du portail d’affichage du message chiffré  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Exemple de rétablissement de la valeur par défaut:**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Exemple de rétablissement de la valeur par défaut:**`Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
   
## <a name="service-information-for-legacy-office-365-message-encryption-prior-to-the-release-of-the-new-ome-capabilities"></a>Informations sur les services pour le chiffrement de messages Office 365 hérité avant la publication des nouvelles fonctionnalités OME
<a name="LegacyServiceInfo"> </a>

Le tableau suivant fournit des détails techniques sur le service de chiffrement de messages Office 365 avant la publication des nouvelles fonctionnalités OME.
  
|**Détails du service**|**Description**|
|:-----|:-----|
|Exigences relatives aux périphériques client  <br/> |Les messages chiffrés peuvent être affichés sur tous les périphériques client, tant que la pièce jointe HTML peut être ouverte dans un navigateur moderne qui prend en charge la publication de formulaire.  <br/> |
|Algorithme de chiffrement et conformité aux normes FIPS (Federal Information Processing Standards)  <br/> |Le chiffrement de messages Office 365 utilise les mêmes clés de chiffrement que la gestion des droits relatifs à l'information (IRM) de Windows Azure et prend en charge le mode de chiffrement 2 (clé 2K pour les clés RSA et 256 bits pour les systèmes SHA-1). Pour plus d'informations sur les modes de chiffrement IRM sous-jacents, consultez la rubrique [AD RMS Cryptographic modes](http://technet.microsoft.com/library/hh867439%28WS.10%29.aspx).<br/> |
|Types de messages pris en charge  <br/> |Le chiffrement de messages Office 365 est uniquement pris en charge pour les éléments dont l'ID de classe de message est **IPM. Note**. Pour plus d'informations, consultez la rubrique [types d'éléments et classes de messages](https://msdn.microsoft.com/library/office/ff861573.aspx).<br/> |
|Tailles limites des messages  <br/> |Le chiffrement de messages Office 365 peut chiffrer des messages jusqu'à 25 mégaoctets. Pour plus d'informations sur les limites de taille des messages, consultez la rubrique [limites d'Exchange Online](http://technet.microsoft.com/library/exchange-online-limits.aspx).<br/> |
|Stratégies de rétention des messages électroniques Exchange Online  <br/> |Exchange Online ne stocke pas les messages chiffrés.  <br/> |
|Prise en charge linguistique pour le chiffrement de messages Office 365  <br/> | Le chiffrement de messages Office 365 prend en charge les langues d’Office 365 comme suit :  <br/>  Les messages électroniques entrants et les fichiers HTML joints sont localisés en fonction des paramètres de langue de l'expéditeur.  <br/>  Le portail d’affichage est localisé en fonction des paramètres de navigateur du destinataire.  <br/>  Le corps (contenu) du message chiffré n’est pas localisé.  <br/> |
|Informations de confidentialité pour le portail OME et l’application Visionneuse OME  <br/> |La [Office 365 Messaging Encryption Portal privacy statement](protected-message-viewer-portal-privacy-statement.md) fournit des informations détaillées sur ce que fait et ne fait pas Microsoft avec vos informations privées.  <br/> |
   
## <a name="frequently-asked-questions-about-legacy-ome"></a>Forum aux questions sur les OME héritées
<a name="LegacyServiceInfo"> </a>

Vous avez des questions sur le chiffrement de messages Office 365? Voici quelques réponses. Si vous ne trouvez pas ce dont vous avez besoin, consultez les forums de la communauté Office 365 sur la [communauté office 365](http://community.office365.com/en-us/forums/default.aspx).
  
 **Q. mes utilisateurs envoient des messages électroniques chiffrés à des destinataires externes à notre organisation. Y a-t-il quelque chose que les destinataires externes doivent faire pour lire et répondre aux messages électroniques chiffrés avec le chiffrement de messages Office 365?**
  
Les destinataires externes à votre organisation qui reçoivent des messages chiffrés Office 365 peuvent les afficher de l’une des deux manières suivantes :
  
- En vous connectant avec un compte Microsoft ou un compte professionnel ou scolaire associé à Office 365.
    
- À l'aide d'un code d'accès unique.
    
 **Q. Les messages électroniques chiffrés Office 365 sont-ils stockés dans le nuage ou sur les serveurs Microsoft ?**
  
Non, les messages chiffrés sont conservés sur le système de courrier du destinataire, et lorsque le destinataire ouvre le message, il est temporairement publié pour l'affichage sur les serveurs Office 365. Les messages ne sont pas stockés à cet emplacement.
  
 **Q. Puis-je personnaliser les messages chiffrés avec ma marque ?**
  
Oui. Vous pouvez utiliser les cmdlets Windows PowerShell pour personnaliser le texte par défaut qui apparaît en haut des messages électroniques chiffrés, la clause d’exclusion de responsabilité et le logo que vous souhaitez utiliser pour le message électronique et le portail de chiffrement. Pour plus d’informations, voir [Add branding to encrypted messages](add-your-organization-brand-to-encrypted-messages.md).
  
 **Q. Le service exige-t-il une licence pour chaque utilisateur de mon organisation ?**
  
Une licence est obligatoire pour chaque utilisateur de l’organisation qui envoie des messages chiffrés.
  
 **Q. Les destinataires externes exigent-ils des abonnements ?**
  
Non, les destinataires externes n’ont pas besoin d’un abonnement pour lire ou répondre à des messages chiffrés. 
  
 **Q. Comment le chiffrement de messages Office 365 est-il différent des services RMS (Rights Management Services)?**
  
RMS fournit des fonctionnalités de protection des droits relatifs à l'information pour les messages électroniques internes d'une organisation en fournissant des modèles intégrés, tels que: ne pas transférer et confidentiel. Le chiffrement de messages Office 365 prend en charge le chiffrement des messages électroniques envoyés aux destinataires externes ainsi qu'aux destinataires internes.
  
 **Q. Comment le chiffrement de messages Office 365 est-il différent de S/MIME?**
  
S/MIME est essentiellement une technologie de chiffrement côté client et exige une gestion de certificats et une infrastructure de publication complexes. Le chiffrement de messages Office 365 utilise des règles de transport et ne dépend pas de la publication de certificats.
  
 **Q. Puis-je lire les messages chiffrés sur des appareils mobiles ?**
  
Oui, vous pouvez afficher les messages sur Android et iOS en téléchargeant les applications de la visionneuse OME à partir de [Google Play Store](http://go.microsoft.com/fwlink/?LinkID=525995&amp;clcid=0x409) et d' [Apple App Store](http://go.microsoft.com/fwlink/?LinkID=525996&amp;clcid=0x409). Ouvrez la pièce jointe HTML dans l'application visionneuse OME, puis suivez les instructions pour ouvrir votre message chiffré. Pour les autres appareils mobiles, vous pouvez ouvrir la pièce jointe HTML sous réserve que votre client de messagerie prenne en charge le formulaire post.
  
 **Q. Les réponses et les messages transférés sont-ils chiffrés ?**
  
Oui. Les réponses restent chiffrées pendant toute la durée du thread.
  
 **Q. Le chiffrement de messages Office 365 fournit-il une localisation ?**
  
Le contenu HTML et les messages électroniques entrants sont localisés en fonction des paramètres de messagerie de l’expéditeur. Le portail d’affichage est localisé en fonction des paramètres de navigateur du destinataire. Cependant, le corps réel (le contenu) du message chiffré n’est pas localisé.
  
 **Q. Quel est la méthode de chiffrement de messages utilisée par Office 365 ?**
  
La fonction de chiffrement de messages d’Office 365 utilise RMS (Rights Management Services) comme infrastructure de chiffrement. La méthode de chiffrement utilisée dépend de l’endroit où vous obtenez les clés RMS servant à chiffrer et déchiffrer les messages.
  
- Si vous utilisez Microsoft Azure RMS pour obtenir les clés, le mode de chiffrement 2 est utilisé. Le mode de chiffrement 2 est une implémentation de chiffrement AD RMS mise à jour et améliorée. Il prend en charge RSA 2048 pour la signature et le chiffrement, et prend en charge SHA-256 pour la signature.
    
- Si vous utilisez Active Directory (AD) RMS pour obtenir les clés, le mode de chiffrement 1 ou 2 est utilisé. La méthode utilisée dépend de votre déploiement AD RMS local. Le mode de chiffrement 1 est le processus de chiffrement d’origine AD RMS. Il prend en charge RSA 1024 pour la signature et le chiffrement, et SHA-1 pour la signature. Ce mode est encore pris en charge par toutes les versions actuelles de RMS.
    
Pour plus d'informations, consultez la rubrique [AD RMS Cryptographic modes](http://go.microsoft.com/fwlink/p/?LinkId=398616).
  
 **Q. Pourquoi certains messages chiffrés déclarent-ils provenir de l’adresse Office365@messaging.microsoft.com ?**
  
Lorsqu’une réponse chiffrée est envoyée à partir du portail de chiffrement ou via l’application Visionneuse OME, l’adresse de messagerie de l’expéditeur est définie sur Office365@messaging.microsoft.com, car le message chiffré est envoyé par le biais d’un point de terminaison Microsoft. Cela permet d’éviter que les messages chiffrés soient marqués comme courrier indésirable. Le nom affiché dans le message électronique et l’adresse dans le portail de chiffrement ne sont pas modifiés en raison de cet étiquetage. En outre, cet étiquetage s’applique uniquement aux messages envoyés via le portail, et non par le biais de n’importe quel autre client de messagerie.
  
 **Q. je suis un abonné EHE (Exchange Hosted enCryption). Où puis-je en savoir plus sur la mise à niveau vers le chiffrement de messages Office 365?**
  
Tous les clients EHE ont été mis à niveau vers le chiffrement de messages Office 365. Pour plus d'informations, visitez le [Centre de mise à niveau de chiffreMent hébergé Exchange](http://go.microsoft.com/fwlink/p/?LinkID=511077).
  
 **Q. dois-je ouvrir des URL, des adresses IP ou des ports dans le pare-feu de mon organisation pour prendre en charge le chiffrement des messages Office 365?**
  
Oui. Vous devez ajouter des URL à la liste d’adresses autorisées pour Exchange Online afin que votre organisation permette l’authentification des messages chiffrés par Office 365. Pour obtenir la liste des URL Exchange Online, voir [Office 365 URLs and IP Address Ranges](https://support.office.com/article/f57e35b7-0a45-42f0-855e-11aa5e7f13fd.aspx)
  
 **Q : À combien de destinataires puis-je envoyer un message chiffré par Office 365 ?**
  
Le nombre maximal de destinataires pour un message chiffré est basé sur le nombre de caractères contenus dans le champ **à** . Lorsqu'il est combiné (après l'extension de la liste de distribution), les adresses des destinataires dans le champ **à** ne doivent pas dépasser 11 980 caractères. Étant donné que les adresses de messagerie peuvent varier en caractères, il n'existe pas de limite de destinataires standard pour un seul message chiffré. 
  
 **Q : Est-il possible de révoquer un message envoyé à un destinataire particulier ?**
  
Nbre. Vous ne pouvez pas révoquer un message à une personne particulière une fois qu'il a été envoyé.
  
 **Q : Puis-je afficher un rapport des messages chiffrés qui ont été reçus et lus ?**
  
Il n'existe pas de rapport qui indique si un message chiffré a été affiché, mais il existe des rapports Office 365 que vous pouvez utiliser pour déterminer le nombre de messages qui correspondent à une règle de transport spécifique, par exemple.
  
 **Q. Que fait Microsoft des informations que je fournis par le biais du portail OME et de l’application Visionneuse OME ?**
  
La [déclaration de confidentialité du portail de chiffreMent de messagerie Office 365](protected-message-viewer-portal-privacy-statement.md) fournit des informations détaillées sur ce que Microsoft fait et ne fait pas avec vos informations personnelles. 
  

