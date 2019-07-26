---
title: Chiffrement du courrier électronique dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
ms.collection:
- M365-security-compliance
description: Compare les options de chiffrement dans Office 365, notamment la fonctionnalité de chiffrement des messages Office (OME), S/MIME, la gestion des droits relatifs à l’information (IRM), et présente le protocole TLS.
ms.openlocfilehash: dba0c0d890a7018f9ca5daab2c1e88c4d234c5c3
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854678"
---
# <a name="email-encryption-in-office-365"></a>Chiffrement du courrier électronique dans Office 365

Cet article compare les options de chiffrement dans Office 365, notamment la fonctionnalité de chiffrement des messages Office (OME), S/MIME, la gestion des droits relatifs à l’information (IRM), et présente le protocole TLS.
  
Office 365 propose plusieurs options de chiffrement pour vous aider à répondre aux besoins de votre entreprise pour la sécurité des messages électroniques. Cet article présente les trois méthodes de chiffrement de courrier électronique dans Office 365. Si vous voulez en savoir plus sur toutes les fonctionnalités de sécurité dans Office 365, visitez le [centre de gestion de la confidentialité Office 365](http://go.microsoft.com/fwlink/p/?LinkID=282470). Cet article présente les trois types de chiffrement disponibles pour aider les administrateurs Office 365 à sécuriser les messages électroniques dans Office 365 :
  
- Chiffrement des messages Office (OME).
    
- S/MIME (Secure/Multipurpose Internet Mail Extension).
    
- Gestion des droits relatifs à l’information (IRM).
    
## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a>Qu’est-ce que le chiffrement des messages électroniques et comment Office 365 l’utilise-t-il ?

Le chiffrement est le processus par lequel les informations sont encodées afin que seul un destinataire autorisé puisse les décoder et les utiliser. Office 365 utilise le chiffrement de deux manières : dans le service et sous la forme d’un contrôle client. Dans le service, le chiffrement est utilisé par défaut dans Office 365 ; vous n’êtes pas obligé de configurer quoi que ce soit. Par exemple, Office 365 utilise le protocole TLS (Transport Layer Security) pour chiffrer la connexion ou la session entre deux serveurs. 
  
Voici comment fonctionne généralement le chiffrement des messages :
  
- Un message est chiffré ou transformé de texte brut en texte chiffré illisible, soit sur l’ordinateur de l’expéditeur, soit via un serveur central lorsque le message est en transit.
    
- Le message reste en texte chiffré tant qu’il est en transit pour qu’il ne puisse pas être lu s’il venait à être intercepté.
    
- Une fois que le destinataire a reçu le message, celui-ci est de nouveau transformé en texte brut lisible de l’une des deux manières suivantes :
    
  - L’ordinateur du destinataire utilise une clé pour déchiffrer le message, ou
    
  - Un serveur central déchiffre le message pour le compte du destinataire, après avoir validé l’identité du destinataire.
    
Pour plus d’informations sur la façon dont Office 365 sécurise les communications entre des serveurs, par exemple entre des organisations dans Office 365 ou entre Office 365 et un serveur de messagerie approuvé en dehors d’Office 365, voir la rubrique décrivant [comment Exchange Online utilise le protocole TLS pour sécuriser les connexions dans Office 365](exchange-online-uses-tls-to-secure-email-connections.md).
  
Regardez cette vidéo pour obtenir une présentation [du chiffrement dans Office 365](https://www.youtube.com/watch?v=KmfxCd5ublI).
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Comparaison des options de chiffrement des messages électroniques disponibles dans Office 365

||![Illustration conceptuelle qui décrit OME](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)|![Illustration conceptuelle qui décrit IRM](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)|![Illustration conceptuelle qui décrit SMIME](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)|
|:-----|:-----|:-----|:-----|
|De quoi s’agit-il ?|Le chiffrement des messages Office 365 (OME) est un service basé sur Azure Rights Management (Azure RMS) qui vous permet d’envoyer des messages chiffrés à des personnes internes ou externes à votre organisation, quelle que soit l’adresse de messagerie de destination (Gmail, Yahoo! Mail, Outlook.com, etc.).  <br/> En tant qu’administrateur, vous pouvez configurer des règles de transport qui définissent les conditions de chiffrement. Lorsqu’un utilisateur envoie un message qui correspond à une règle, le chiffrement est automatiquement appliqué.  <br/> Pour afficher les messages chiffrés, les destinataires peuvent obtenir un code secret à usage unique, se connecter à l’aide d’un compte Microsoft ou se connecter à l’aide d’un compte professionnel ou scolaire associé à Office 365. Les destinataires peuvent également envoyer des réponses chiffrées. Ils n’ont pas besoin de disposer d’un abonnement à Office 365 pour afficher des messages chiffrés ni pour envoyer des réponses chiffrées.|IRM est une solution de chiffrement qui applique également des restrictions d’utilisation aux messages électroniques. Cette solution permet d’empêcher que des informations sensibles ne soient imprimées, transmises ou copiées par des personnes non autorisées.  <br/> Les fonctionnalités IRM dans Office 365 utilisent Azure Rights Management (Azure RMS).|S/MIME est une solution de chiffrement basé sur les certificats qui vous permet de chiffrer et de signer numériquement un message. Le chiffrement des messages permet de garantir que seul le destinataire prévu puisse ouvrir et lire le message. Une signature numérique permet au destinataire de valider l’identité de l’expéditeur.  <br/> Les signatures numériques et le chiffrement des messages sont possibles grâce à l’utilisation de certificats numériques uniques qui contiennent les clés pour la vérification des signatures numériques et le chiffrement ou le déchiffrement des messages.  <br/> Pour utiliser S/MIME, vous devez disposer des clés publiques sur fichier pour chaque destinataire. Les destinataires doivent tenir à jour leurs propres clés privées, car elles doivent rester sécurisées. Si les clés privées d’un destinataire sont compromises, le destinataire doit obtenir une nouvelle clé privée et redistribuer les clés publiques à tous les expéditeurs potentiels.|
|Que fait-il ?|OME :  <br/>  Chiffre les messages envoyés à des destinataires internes ou externes.  <br/>  Permet aux utilisateurs d’envoyer des messages chiffrés à n’importe quelle adresse de messagerie électronique, y compris Outlook.com, Yahoo! Mail et Gmail.  <br/>  Vous permet, en tant qu’administrateur, de personnaliser le portail d’affichage des messages électroniques pour qu’il corresponde à la marque de votre organisation.  <br/>  Microsoft gère et stocke les clés de manière sécurisée, vous n’avez donc pas à vous en occuper.  <br/>  Aucun logiciel spécial côté client n’est nécessaire tant que le message chiffré (envoyé en tant que pièce jointe HTML) peut être ouvert dans un navigateur.|IRM :  <br/>  Utilise le chiffrement et les restrictions d’utilisation pour fournir une protection en ligne et hors ligne pour les messages électroniques et les pièces jointes.  <br/>  Vous donne, en votre qualité d’administrateur, la possibilité de configurer des règles de transport ou des règles de protection Outlook pour appliquer automatiquement la gestion des droits relatifs à l’information (IRM) aux messages sélectionnés.  <br/>  Permet aux utilisateurs d’appliquer manuellement des modèles dans Outlook ou Outlook sur le web (auparavant Outlook Web App).|S/MIME gère l’authentification des expéditeurs par les signatures numériques et la confidentialité des messages par le chiffrement.|
|Que ne fait-il pas ?|OME ne vous permet pas d’appliquer des restrictions d’utilisation aux messages. Par exemple, vous ne pouvez pas l’utiliser pour empêcher un destinataire de transférer ou d’imprimer un message chiffré.|Certaines applications peuvent ne pas prendre en charge les messages électroniques IRM sur tous les périphériques. Pour plus d’informations sur ces produits et d’autres produits qui prennent en charge le courrier IRM, voir [fonctionnalités des appareils clients](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).|S/MIME ne permet pas l’analyse des messages chiffrés pour détecter les logiciels malveillants et le courrier indésirable ou y appliquer des stratégies.|
|Recommandations et exemples de scénarios|Nous vous recommandons d’utiliser OME lorsque vous souhaitez envoyer des informations professionnelles sensibles à des personnes extérieures à votre organisation, qu’il s’agisse de clients ou d’autres entreprises. Par exemple :  <br/>  Quand un employé de banque envoie des relevés de carte de crédit aux clients ;  <br/>  Quand un cabinet médical envoie un dossier médical à un patient   <br/>  Quand un avocat envoie des informations juridiques à caractère confidentiel à un autre avocat.|Nous vous recommandons d’utiliser la gestion des droits relatifs à l’information (IRM) lorsque vous souhaitez appliquer des restrictions d’utilisation et le chiffrement. Par exemple :  <br/>  Un responsable qui envoie des données confidentielles à son équipe sur un nouveau produit applique l’option « Ne pas transférer ».  <br/>  Un dirigeant doit envoyer une proposition d’appel d’offres à une autre société ; elle contient une pièce jointe d’un partenaire qui utilise Office 365 ; le message électronique et la pièce jointe doivent tous deux être protégés.|Nous vous recommandons d’utiliser S/MIME lorsque votre organisation ou l’organisation du destinataire requiert un véritable chiffrement de pair à pair.  <br/>  S/MIME est la solution utilisée le plus couramment dans les scénarios suivants :  <br/>  Des agences gouvernementales communiquant avec des agences gouvernementales  <br/>  Une entreprise communiquant avec une agence gouvernementale|
   
## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a>Quelles options de chiffrement sont disponibles pour mon abonnement à Office 365 ?

Pour plus d’informations sur les options de chiffrement de courrier pour votre abonnement Office 365, voir la [description du service Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-service-description.aspx). Vous y trouverez des informations sur les fonctionnalités de chiffrement suivantes :
  
- Azure RMS, y compris les fonctionnalités IRM et OME
    
- S/MIME
    
- TLS
    
- Chiffrement des données stockées (via BitLocker)
    
## <a name="what-about-encryption-for-data-at-rest"></a>Qu’en est-il du chiffrement des données stockées ?

Le terme « Données au repos » fait référence aux données qui ne sont pas activement en transit. Dans Office 365, les données stockées de messages électroniques sont chiffrées à l’aide du chiffrement de lecteur BitLocker. BitLocker chiffre les disques durs dans les centres de données Office 365 pour fournir une protection améliorée contre les accès non autorisés. Pour plus d’informations, voir [Vue d’ensemble des étiquettes](https://go.microsoft.com/fwlink/p/?LinkId=394737).
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a>Pour plus d’informations sur les options de chiffrement des messages électroniques, accédez à Office 365

Pour plus d’informations sur les options de chiffrement des messages électroniques dans cet article, ainsi que sur le protocole TLS, consultez les articles suivants :
  
 **OME**
  
[Chiffrement de messages Office 365 (OME)](ome.md)
  
 **IRM**
  
[Gestion des droits relatifs à l'information dans Exchange Online](https://technet.microsoft.com/en-us/library/jj983436%28v=exchg.150%29.aspx)
  
[Qu’est-ce que Azure Rights Management?](https://technet.microsoft.com/library/jj585026)
  
 **S/MIME**
  
[S/MIME pour la signature et le chiffrement des messages](https://technet.microsoft.com/library/dn626158)
  
[Présentation de S/MIME](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[Présentation de la cryptographie par clé publique](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
 **TLS**
  
[Configurer le flux de courrier personnalisé à l’aide de connecteurs dans Office 365](https://technet.microsoft.com/en-us/library/jj723138%28v=exchg.150%29.aspx)
  

