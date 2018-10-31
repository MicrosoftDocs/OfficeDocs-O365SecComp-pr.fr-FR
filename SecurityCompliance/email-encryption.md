---
title: Chiffrement du courrier électronique dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c0d87cbe-6d65-4c03-88ad-5216ea5564e8
description: Comparaison des options de chiffrement dans Office 365, notamment Office Message de chiffrement S/MIME, Information Rights Management (IRM) et en savoir plus sur la sécurité TLS (Transport Layer).
ms.openlocfilehash: c9c83283cab09ac81ab2856aec53fe8682ec45b8
ms.sourcegitcommit: c05076501dfe118e575998ecfc08ad69d13c8abc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25853079"
---
# <a name="email-encryption-in-office-365"></a>Chiffrement du courrier électronique dans Office 365

Cet article compare les options de chiffrement dans Office 365, notamment Office Message de chiffrement S/MIME, Information Rights Management (IRM) et présente Transport Layer Security (TLS).
  
Office 365 offre plusieurs options de chiffrement pour vous aider à répondre à vos besoins de sécurité de messagerie électronique. Cet article présente trois méthodes pour chiffrer un message électronique dans Office 365. Si vous souhaitez en savoir plus sur toutes les fonctionnalités de sécurité dans Office 365, visitez le [Centre de gestion de la confidentialité Office 365](http://go.microsoft.com/fwlink/p/?LinkID=282470). Cet article présente les trois types de chiffrement disponible pour les administrateurs Office 365 aider à la messagerie sécurisée dans Office 365 :
  
- Chiffrement des messages Office (OME).
    
- S/MIME (Secure/Multipurpose Internet Mail Extension).
    
- Gestion des droits relatifs à l’information (IRM).
    
## <a name="what-is-email-encryption-and-how-does-office-365-use-it"></a>Qu’est-ce que le chiffrement des messages électroniques et comment Office 365 l’utilise-t-il ?

Le chiffrement est le processus par lequel les informations sont codées afin que seul un destinataire autorisé puisse décoder et de consommer les informations. Office 365 utilise le chiffrement de deux manières : en tant que client contrôle et dans le service. Dans le service, le chiffrement est utilisé dans Office 365 par défaut ; vous n’êtes pas obligé de configurer rien. Par exemple, Office 365 utilise Transport Layer Security (TLS) pour chiffrer la connexion, ou session, entre deux serveurs. 
  
Voici comment fonctionne généralement de cryptage de messages :
  
- Un message est chiffré ou transformé de texte brut en texte chiffré illisible, sur l’ordinateur de l’expéditeur ou par un serveur central pendant que le message est en transit.
    
- Le message reste dans le texte chiffré lorsqu’il est en transit afin de protéger contre en cours de lecture au cas où le message est intercepté.
    
- Une fois que le destinataire a reçu le message, celui-ci est de nouveau transformé en texte brut lisible de l’une des deux manières suivantes :
    
  - L’ordinateur du destinataire utilise une clé pour déchiffrer le message, ou
    
  - Un serveur central déchiffre le message au destinataire, après la validation de l’identité du destinataire.
    
Pour plus d’informations sur la façon dont Office 365 sécurise les communications entre les serveurs, tels qu’entre des organisations dans Office 365 ou entre Office 365 et un partenaire approuvé en dehors d’Office 365, voir [comment Exchange Online utilise TLS pour la messagerie sécurisée connexions dans Office 365](exchange-online-uses-tls-to-secure-email-connections.md).
  
Regardez cette vidéo pour une présentation du [chiffrement dans Office 365](https://www.youtube.com/watch?v=KmfxCd5ublI).
  
## <a name="comparing-email-encryption-options-available-in-office-365"></a>Comparaison des options de chiffrement des messages électroniques disponibles dans Office 365

||        ![Illustration conceptuelle qui décrit OME](media/2bf27b5e-bbb3-46d1-95bf-884dc27a746c.png)                 |        ![Illustration conceptuelle qui décrit IRM](media/9c0cc444-9448-40c6-b244-8fcc593a64e0.png)                 |        ![Illustration conceptuelle qui décrit SMIME](media/ae4613a8-c17e-47e1-8e13-12e891e43744.png)                |
|:-----|:-----|:-----|:-----|
|De quoi s’agit-il ?  <br/> |Le chiffrement des messages Office 365 (OME) est un service basé sur Azure Rights Management (Azure RMS) qui vous permet d’envoyer des messages chiffrés à des personnes internes ou externes à votre organisation, quelle que soit l’adresse de messagerie de destination (Gmail, Yahoo! Mail, Outlook.com, etc.).  <br/> En tant qu’administrateur, vous pouvez configurer des règles de transport qui définissent les conditions de chiffrement. Lorsqu’un utilisateur envoie un message qui correspond à une règle, le chiffrement est automatiquement appliqué.  <br/> Pour afficher les messages chiffrés, les destinataires peuvent obtenir un code secret unique, la connexion avec un compte Microsoft ou la connexion avec un travail ou école compte associé à Office 365. Destinataires peuvent également envoyer des réponses chiffrés. Un abonnement à Office 365 pour afficher des messages chiffrés ou envoyer des réponses chiffrées ne sont nécessaires.  <br/> |IRM est une solution de chiffrement qui applique également des restrictions d’utilisation aux messages électroniques. Cette solution permet d’empêcher que des informations sensibles ne soient imprimées, transmises ou copiées par des personnes non autorisées.  <br/> Les fonctionnalités IRM dans Office 365 utilisent Azure Rights Management (Azure RMS). 
  <br/> |S/MIME est une solution basée sur certificat de chiffrement qui permet de chiffrer et de signer numériquement un message. Le chiffrement du message permet de s’assurer que seul le destinataire peut ouvrir et lire le message. Une signature numérique permet au destinataire de valider l’identité de l’expéditeur.  <br/> Les signatures numériques et le chiffrement des messages sont possibles grâce à l’utilisation de certificats numériques uniques qui contiennent les clés pour la vérification des signatures numériques et le chiffrement ou le déchiffrement des messages.  <br/> Pour utiliser S/MIME, vous devez disposer des clés publiques sur le fichier pour chaque destinataire. Destinataires doivent gérer leurs propres clés privées, qui doivent rester sécurisés. Si les clés privées d’un destinataire sont compromises, le destinataire doit obtenir une nouvelle clé privée et à redistribuer les clés publiques à tous les expéditeurs potentiels.  <br/> |
|Que fait-il ?  <br/> | OME :  <br/>  Chiffre les messages envoyés à des destinataires internes ou externes.  <br/>  Permet aux utilisateurs d’envoyer des messages chiffrés à n’importe quelle adresse de messagerie électronique, y compris Outlook.com, Yahoo! Mail et Gmail.  <br/>  Vous permet, en tant qu’administrateur, pour personnaliser le message électronique portail pour refléter la marque de votre organisation d’affichage.  <br/>  Microsoft gère en toute sécurité et stocke les clés, afin que vous n’avez pas besoin.  <br/>  Aucun logiciel spécial côté client n’est nécessaire tant que le message chiffré (envoyé en tant que pièce jointe HTML) peut être ouvert dans un navigateur.  <br/> | IRM :  <br/>  Utilise le chiffrement et les restrictions d’utilisation pour fournir une protection en ligne et hors ligne pour les messages électroniques et les pièces jointes.  <br/>  Vous donne, en votre qualité d’administrateur, la possibilité de configurer des règles de transport ou des règles de protection Outlook pour appliquer automatiquement la gestion des droits relatifs à l’information (IRM) aux messages sélectionnés.  <br/>  Permet aux utilisateurs d’appliquer manuellement des modèles dans Outlook ou Outlook Web App.  <br/> |S/MIME gère l’authentification des expéditeurs par les signatures numériques et la confidentialité des messages par le chiffrement.  <br/> |
|Que ne fait-il pas ?  <br/> |OME ne vous permettre d’appliquer des restrictions d’utilisation pour les messages. Par exemple, vous ne pouvez pas l’utiliser pour arrêter un destinataire de transférer ou l’impression d’un message chiffré.  <br/> |Certaines applications ne peuvent pas en charge IRM dans les messages sur tous les périphériques. Pour plus d’informations sur ces et d’autres produits qui prennent en charge le message électronique IRM, voir [fonctionnalités du périphérique Client](https://technet.microsoft.com/library/dn655136.aspx#BKMK_ClientCapabilities).<br/> |S/MIME n’autorise pas les messages chiffrés à analyser pour les programmes malveillants, le courrier indésirable ou aux stratégies.  <br/> |
|Recommandations et exemples de scénarios  <br/> | Nous vous recommandons d’utiliser OME lorsque vous souhaitez envoyer des informations sensibles à des personnes extérieures à votre organisation, qu’ils soient consommateurs et autres entreprises. Par exemple :  <br/>  Quand un employé de banque envoie des relevés de carte de crédit aux clients ;  <br/>  Un cabinet médical l’envoi des dossiers médicaux à un patient  <br/>  Quand un avocat envoie des informations juridiques à caractère confidentiel à un autre avocat.  <br/> | Nous vous recommandons d’utiliser la gestion des droits relatifs à l’information (IRM) lorsque vous souhaitez appliquer des restrictions d’utilisation et le chiffrement. Par exemple :  <br/>  Un responsable de l’envoi d’informations confidentielles à son équipe sur un nouveau produit s’applique à l’option « Ne pas transférer ».  <br/>  Un dirigeant doit envoyer une proposition d’appel d’offres à une autre société ; elle contient une pièce jointe d’un partenaire qui utilise Office 365 ; le message électronique et la pièce jointe doivent tous deux être protégés.  <br/> | Nous recommandons l’utilisation de S/MIME lors de votre organisation ou organisation du destinataire nécessite un chiffrement égal à true.  <br/>  S/MIME est la solution utilisée le plus couramment dans les scénarios suivants :  <br/>  Des agences gouvernementales communiquant avec des agences gouvernementales  <br/>  Une entreprise communiquant avec une agence gouvernementale  <br/> |
   
## <a name="what-encryption-options-are-available-for-my-office-365-subscription"></a>Quelles options de chiffrement sont disponibles pour mon abonnement à Office 365 ?

Pour plus d’informations sur les options de chiffrement de courrier électronique pour votre abonnement Office 365, voir la [description du service Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-service-description.aspx). Ici, vous trouverez plus d’informations sur les fonctionnalités de chiffrement suivantes :
  
- Azure RMS, y compris les fonctionnalités IRM et OME
    
- S/MIME
    
- TLS
    
- Chiffrement des données stockées (via BitLocker)
    
## <a name="what-about-encryption-for-data-at-rest"></a>Qu’en est-il du chiffrement des données stockées ?

« Données au repos » fait référence à des données qui n’est pas activement en transit. Dans Office 365, les données de messagerie au repos sont chiffrées à l’aide du chiffrement de lecteur BitLocker. BitLocker chiffre les disques durs de centres de données Office 365 pour fournir une meilleure protection contre les accès non autorisés. Pour plus d’informations, voir [Vue d’ensemble de BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=394737).
  
## <a name="more-information-about-email-encryption-options-in-office-365"></a>Pour plus d’informations sur les options de chiffrement des messages électroniques, accédez à Office 365

Pour plus d’informations sur les options de chiffrement des messages électroniques dans cet article, ainsi que sur le protocole TLS, consultez les articles suivants :
  
 **OME**
  
[Chiffrement de messages Office 365 (OME)](ome.md)
  
 **IRM**
  
[Gestion des droits relatifs à l'information dans Exchange Online](https://technet.microsoft.com/en-us/library/jj983436%28v=exchg.150%29.aspx)
  
[What ' s Azure Rights Management ?](https://technet.microsoft.com/library/jj585026)
  
 **S/MIME**
  
[S/MIME pour la signature et le chiffrement des messages](https://technet.microsoft.com/library/dn626158)
  
[Présentation de S/MIME](https://technet.microsoft.com/library/aa995740%28v=exchg.65%29.aspx)
  
[Cryptographie à clé publique](https://technet.microsoft.com/library/aa998077%28v=exchg.65%29.aspx)
  
 **TLS**
  
[Configurer le flux de messagerie personnalisé à l’aide de connecteurs dans Office 365](https://technet.microsoft.com/en-us/library/jj723138%28v=exchg.150%29.aspx)
  

