---
title: Protéger les boîtes aux lettres locales avec Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/1/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- GEU150
- GMA150
- GPA150
- MET150
ms.assetid: c5e95951-da67-4ec7-92c5-982abd477e69
description: Même si vous envisagez d’héberger tout ou partie de vos boîtes aux lettres locales, vous pouvez toujours protéger les boîtes aux lettres avec Exchange Online Protection (EOP). Pour configurer des connecteurs, votre compte doit être un administrateur Global de Office 365, ou un administrateur d’entreprise Exchange (le groupe de rôles de gestion de l’organisation). Pour plus d’informations sur comment Office 365 autorisations par rapport aux autorisations Exchange, voir affectation rôles d’administrateur dans Office 365 exécuté par 21Vianet. Si tous vos boîtes aux lettres Exchange sont locaux, procédez comme suit pour configurer votre service EOP.
ms.openlocfilehash: 4751bb2183e61d292805d1799519644b77b08c2a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528753"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a>Protéger les boîtes aux lettres locales avec Exchange Online Protection

> [!NOTE]
> Cet article s’applique uniquement à Office 365 exécuté par 21Vianet en Chine. 
  
Même si vous envisagez d’héberger tout ou partie de vos boîtes aux lettres locales, vous pouvez toujours protéger les boîtes aux lettres avec Exchange Online Protection (EOP). Pour configurer des connecteurs, votre compte doit être un administrateur Global de Office 365, ou un administrateur d’entreprise Exchange (le groupe de rôles de gestion de l’organisation). Pour plus d’informations sur comment Office 365 autorisations par rapport aux autorisations Exchange, voir [affectation rôles d’administrateur dans Office 365 exécuté par 21Vianet](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac). Si tous vos boîtes aux lettres Exchange sont locaux, procédez comme suit pour configurer votre service EOP. 
  
## <a name="step-1-use-the-office-365-admin-center-to-add-and-verify-your-domain"></a>Étape 1 : utiliser le Centre d'administration Office 365 pour ajouter et vérifier votre domaine

1. Dans le Centre d'administration Office 365, accédez à Installation pour ajouter votre domaine au service.
    
2.  Suivez les étapes décrites dans le portail pour ajouter les enregistrements DNS applicables à votre fournisseur d’hébergement DNS afin de vérifier la propriété du domaine. 
    
> [!TIP]
> [Ajouter votre domaine et aux utilisateurs d’Office 365 exécuté par 21Vianet](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) et [créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) sont des ressources utiles pour référence lorsque vous ajoutez votre domaine au service et configurez le système DNS. 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a>Étape 2 : Ajouter des destinataires et configurer le type de domaine

Avant de configurer votre flux de messagerie vers et depuis le service EOP, nous vous recommandons d'ajouter vos destinataires au service. Il existe plusieurs méthodes pour mener à bien cette opération, comme indiqué dans [Gestion des utilisateurs de messagerie dans EOP](https://go.microsoft.com/fwlink/?LinkId=506782). Aussi, si vous souhaitez activer le blocage du périmètre basé sur l'annuaire (DBEB) afin d'appliquer la vérification du destinataire dans le service après avoir ajouté vos destinataires, vous devez définir votre type de domaine sur Faisant autorité. Pour plus d'informations sur le DBEB, consultez la rubrique [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781).
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Étape 3 : Utiliser le CAE pour configurer le flux de messagerie

Créer des connecteurs dans le centre d’administration Exchange (EAC) qui permettent de flux de messagerie entre EOP et vos serveurs de messagerie local. Pour obtenir des instructions détaillées, voir [Create requis pour configurer le flux de messagerie de base via EOP connecteurs](https://go.microsoft.com/fwlink/?LinkId=506780).
  
 Comment savoir si cette tâche a fonctionné ? 
  
 Utilisez l’Analyseur de connectivité à distance pour exécuter le test de flux de messagerie entre le service et de votre environnement. Pour plus d’informations, voir la section « Utiliser l’Analyseur de connectivité à distance pour tester la remise du courrier électronique » dans le [Test du flux de messagerie avec l’Analyseur de connectivité à distance](https://go.microsoft.com/fwlink/?LinkId=506784).
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a>Étape 4 : Autoriser l'accès SMTP entrant sur le port 25

Une fois que vous avez configuré les connecteurs, attendez que les 72 heures pour autoriser la propagation de vos mises à jour des enregistrements DNS. Limitez le trafic SMTP-port 25 entrant sur vos serveurs de messagerie ou de pare-feu pour accepter le courrier uniquement dans les centres de données EOP, notamment des adresses IP répertoriés à [l’URL et l’adresse IP plages pour Office 365 exécuté par 21Vianet](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection). Cela protège votre environnement local en limitant l’étendue de vous pouvez recevoir les messages entrants. En outre, si vous disposez des paramètres sur votre serveur de messagerie qui contrôlent les adresses IP autorisées à se connecter pour le relais de messagerie, mettre à jour ces paramètres.
  
> [!TIP]
> Configurez les paramètres du serveur SMTP en définissant l'expiration du délai de connexion sur 60 secondes. Ce paramétrage est acceptable dans la plupart des cas, et autorise un certain délai, par exemple, si le message envoyé contient une pièce jointe volumineuse. 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Étape 5 : Utiliser l'environnement de ligne de commande Exchange Management Shell pour vérifier que le courrier indésirable est routé vers le dossier Courrier indésirable de chaque utilisateur

Pour vous assurer que courrier non sollicité (indésirable) est correctement routé vers le dossier courrier indésirable de chaque utilisateur, vous devez effectuer quelques étapes de configuration. Les étapes sont fournies dans [vous assurer que le courrier indésirable est routé vers le dossier courrier indésirable de chaque utilisateur](https://go.microsoft.com/fwlink/?LinkId=506804). Si vous ne souhaitez pas déplacer les messages vers le dossier courrier indésirable de chaque utilisateur, vous pouvez choisir une autre action en modifiant vos stratégies de filtrage de contenu dans le centre d’administration Exchange. Pour plus d’informations, voir [Configurer les stratégies de filtrage de contenu](https://go.microsoft.com/fwlink/?LinkId=506805). 
  
## <a name="step-6-use-the-office-365-admin-center-to-point-your-mx-record-to-eop"></a>Étape 6 : utiliser le Centre d'administration Office 365 pour faire pointer votre enregistrement MX vers EOP

Suivez les étapes de configuration de domaine Office 365 pour mettre à jour votre enregistrement MX pour votre domaine, afin que votre courrier électronique entrant circule dans EOP. Pour plus d’informations, vous pouvez ensuite référencer [créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b).
  
Comment savoir si cette tâche a fonctionné ?
  
 Utilisez l’Analyseur de connectivité à distance pour exécuter un test qui vérifie votre enregistrement MX. Pour plus d’informations, voir la section « Utiliser l’Analyseur de connectivité à distance pour tester votre enregistrement MX et le connecteur sortant » dans le [Test du flux de messagerie avec l’Analyseur de connectivité à distance](https://go.microsoft.com/fwlink/?LinkId=506784). 
  
À ce stade, vous avez vérifié la fourniture de service pour un connecteur local sortant correctement configuré et vous vous êtes assuré que votre enregistrement MX pointe vers EOP. Vous pouvez désormais exécuter les tests supplémentaires suivants afin de vérifier qu'un courrier électronique est bien remis par le service à votre environnement local :
  
- Dans l'Analyseur de connectivité à distance, cliquez sur l'onglet **Office 365**, puis exécutez le test **Courrier SMTP entrant** situé sous **Tests E-mail sur Internet**.
    
- Envoyez un message électronique à partir d'un compte de messagerie basé sur le web vers un destinataire de messagerie de votre organisation dont le domaine correspond au domaine ajouté au service. Vérifiez la remise du message à la boîte aux lettres locale à l'aide de Microsoft Outlook ou d'un autre client de messagerie.
    
- Si vous souhaitez effectuer un test de message sortant, vous pouvez envoyer un message électronique d'un utilisateur de votre organisation vers un compte de messagerie basé sur le web et confirmer sa réception.
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a>Moins courantes : une configuration hybride avec des boîtes aux lettres locales et dans le nuage

Si vous avez Exchange boîtes aux lettres locales et une ou plusieurs boîtes aux lettres dans le nuage dans Exchange Online, vous disposez d’une configuration *hybride* . Dans une configuration hybride, fonctionnalités telles que des informations de disponibilité du partage de calendrier et le routage du courrier collaborer dans votre environnement local et environnements en nuage. Vous pouvez avoir une configuration hybride en place pendant la transition de boîtes aux lettres vers Exchange Online. Un environnement hybride est configuré différemment de protection autonome EOP. 
  
Vous pouvez choisir un scénario hybride pour tirer parti de la messagerie en nuage pour la plupart de vos employés. Vous pouvez le faire lors héberge également des boîtes aux lettres locales ; par exemple, pour votre service juridique. 
  
Une configuration hybride peut s’avérer complexe, mais elle comporte de nombreux avantages. Pour en savoir plus sur la configuration de scénarios hybrides avec Exchange, voir [fonctionnalités de déploiement de configuration d’Exchange hybride avec Office 365 exécuté par 21Vianet](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d).
  

