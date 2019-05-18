---
title: Configurer votre service EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/23/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: d74c6ddf-11b0-43ee-b298-8bb0340895f0
description: Cette rubrique explique comment configurer Microsoft Exchange Online Protection (EOP). Si vous avez été redirigé depuis l'Assistant Domaines Office 365, revenez à l'Assistant Domaines Office 365 si vous ne souhaitez pas utiliser Exchange Online Protection. Si vous recherchez plus d'informations sur la configuration des connecteurs, consultez la rubrique Configure mail flow using connectors in Office 365.
ms.openlocfilehash: 93c6cbe41177103778bf96ca652d9d2889849372
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153056"
---
# <a name="set-up-your-eop-service"></a>Configurer votre service EOP

Cette rubrique explique comment configurer Microsoft Exchange Online Protection (EOP). Si vous avez été redirigé depuis l'Assistant Domaines Office 365, revenez à l'Assistant Domaines Office 365 si vous ne souhaitez pas utiliser Exchange Online Protection. Si vous recherchez plus d'informations sur la configuration des connecteurs, consultez la rubrique [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx).
  
> [!NOTE]
> Elle suppose que vous disposez de boîtes aux lettres locales et que vous voulez les protéger avec EOP (scénario dit « autonome »). Si vous voulez héberger toutes vos boîtes aux lettres dans le nuage avec Exchange Online, il n'est pas nécessaire de réaliser toutes les étapes décrites dans cette rubrique. Accédez à [Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286312) pour vous inscrire et acheter des boîtes aux lettres en nuage. Si vous voulez héberger certaines de vos boîtes aux lettres localement et d'autres dans le nuage, il s'agit d'un scénario hybride. Des paramètres de flux de messagerie plus avancés sont requis. La rubrique [Exchange Server 2013 Hybrid Deployments](http://technet.microsoft.com/library/59e32000-4fcf-417f-a491-f1d8f9aeef9b.aspx) explique le flux de messagerie hybride et comporte des liens vers des ressources indiquant comment le configurer. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer

- Durée d'exécution estimée de cette tâche : 1 heure
    
- Pour configurer les connecteurs, vous devez disposer d'un compte d'administrateur global Office 365 ou d'administrateur d'entreprise Exchange (groupe de rôles Gestion de l'organisation). Pour plus d'informations sur la liaison entre les autorisations Office 365 et les autorisations Exchange, voir [À propos des rôles d'administrateur Office 365](https://go.microsoft.com/fwlink/p/?LinkID=335814).
    
- Si vous ne vous êtes pas inscrit à EOP, consultez la page [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=282660), et choisissez d'acheter ou d'essayer le service. 
    
- Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
    
> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="how-do-you-do-this"></a>Comment procéder ?

### <a name="step-1-use-the-microsoft-365-admin-center-to-add-and-verify-your-domain"></a>Étape 1: utiliser le centre d’administration Microsoft 365 pour ajouter et vérifier votre domaine

1. Dans le centre d’administration Microsoft 365, accédez à **configuration** pour ajouter votre domaine au service. 
    
    Vous ne savez pas où trouver le centre d’administration Microsoft 365? Pour plus d’informations, consultez la rubrique à [propos du centre d’administration Microsoft 365](https://go.microsoft.com/fwlink/p/?LinkId=521888).
    
2. Suivez les étapes pour ajouter les enregistrements DNS applicables à votre fournisseur d'hébergement DNS afin de vérifier l'appartenance du domaine.
    
> [!TIP]
> Les rubriques [Ajouter votre domain à Office 365](https://support.office.com/en-us/article/add-a-domain-to-office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611) et [Créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS](https://support.office.com/en-us/article/create-dns-records-at-any-dns-hosting-provider-for-office-365-7b7b075d-79f9-4e37-8a9e-fb60c1d95166) constituent des ressources utiles à consulter lors de l'ajout de votre domaine au service et de la configuration de DNS. 
  
### <a name="step-2-add-recipients-and-optionally-enable-dbeb"></a>Étape 2 : Ajouter des destinataires et éventuellement activer DBEB

Avant de configurer votre flux de messagerie vers et depuis le service EOP, nous vous recommandons d'ajouter vos destinataires au service. Il existe plusieurs méthodes pour mener à bien cette opération, comme indiqué dans [Gestion des utilisateurs de messagerie dans EOP](manage-mail-users-in-eop.md). Aussi, si vous souhaitez activer le blocage du périmètre basé sur l'annuaire (DBEB) afin d'appliquer la vérification du destinataire dans le service après avoir ajouté vos destinataires, vous devez définir votre type de domaine sur Faisant autorité. Pour plus d'informations sur le DBEB, consultez la rubrique [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).
  
### <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Étape 3 : Utiliser le CAE pour configurer le flux de messagerie

Créez des connecteurs dans le Centre d'administration Exchange (CAE) qui activent le flux de messagerie entre EOP et vos serveurs de messagerie locaux. Pour plus d'informations, consultez la rubrique [Set up connectors to route mail between Office 365 and your own email servers](http://technet.microsoft.com/library/2e93fd60-a5ef-4e64-8e62-2b862b2d1033.aspx).
  
#### <a name="how-do-you-know-this-task-worked"></a>Comment savoir si cette tâche a fonctionné ?

Utilisez l'Analyseur de connectivité à distance pour exécuter un test qui vérifie le flux de messages entre le service et votre environnement. Pour plus d'informations, consultez la section « Utiliser l'Analyseur de connectivité à distance pour tester la remise du courrier électronique » de la rubrique [Testing Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx).
  
### <a name="step-4-allow-inbound-port-25-smtp-access"></a>Étape 4 : Autoriser l’accès SMTP entrant sur le port 25

Après avoir configuré les connecteurs, attendez 72 heures avant d'autoriser la propagation de vos mises à jour d'enregistrement DNS. Ensuite, limitez le trafic SMTP entrant sur le port 25 au niveau du pare-feu ou des serveurs de messagerie de façon à accepter uniquement le courrier électronique en provenance des centres de données EOP, en particulier des adresses IP répertoriées dans [Adresses IP d'Exchange Online Protection](exchange-online-protection-ip-addresses.md). Cela protège votre environnement local en limitant l'étendue des messages entrants. Si des paramètres définis sur votre serveur de messagerie contrôlent les adresses IP autorisées à se connecter pour le relais de messagerie, mettez-les à jour également.
  
> [!TIP]
> Configurez les paramètres du serveur SMTP en définissant l'expiration du délai de connexion sur 60 secondes. Ce paramétrage est acceptable dans la plupart des cas, et autorise un certain délai, par exemple, si le message envoyé contient une pièce jointe volumineuse. 
  
### <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Étape 5 : Utiliser l'environnement de ligne de commande Exchange Management Shell pour vérifier que le courrier indésirable est routé vers le dossier Courrier indésirable de chaque utilisateur

Pour vous assurer que le courrier indésirable est correctement routé vers le dossier Courrier indésirable de chaque utilisateur, vous pouvez effectuer quelques opérations de configuration. Les étapes sont fournies dans la procédure [vous assurer que le courrier indésirable est acheminé vers le dossier de courrier indésirable de chaque utilisateur](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).
  
Si vous ne souhaitez pas déplacer les messages vers le dossier Courrier indésirable de chaque utilisateur, vous pouvez choisir une autre action en modifiant vos stratégies de filtrage de contenu dans le Centre d'administration Exchange. Pour plus d'informations, consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](../configure-your-spam-filter-policies.md).
  
### <a name="step-6-use-the-microsoft-365-admin-center-to-point-your-mx-record-to-eop"></a>Étape 6: utiliser le centre d’administration Microsoft 365 pour faire pointer votre enregistrement MX vers EOP

Suivez les étapes de configuration de domaine Office 365 pour mettre à jour votre enregistrement MX pour votre domaine, de sorte que votre courrier entrant circule dans EOP. Veillez à pointer directement votre enregistrement MX vers EOP plutôt que de faire relayer votre courrier électronique vers EOP par un service de filtrage tiers. Pour plus d'informations, vous pouvez de nouveau vous reporter à la rubrique [Créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider).
  
#### <a name="how-do-you-know-this-task-worked"></a>Comment savoir si cette tâche a fonctionné ?

Utilisez l'Analyseur de connectivité à distance pour exécuter un test qui vérifie votre enregistrement MX. Pour plus d'informations, consultez la section « Utiliser l'Analyseur de connectivité à distance pour tester votre enregistrement MX et le connecteur sortant » de la rubrique [Testing Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx). 
  
À ce stade, vous avez vérifié la fourniture de service pour un connecteur local sortant correctement configuré et vous vous êtes assuré que votre enregistrement MX pointe vers EOP. Vous pouvez désormais exécuter les tests supplémentaires suivants afin de vérifier qu'un courrier électronique est bien remis par le service à votre environnement local :
  
- Dans l'Analyseur de connectivité à distance, cliquez sur l'onglet **Office 365**, puis exécutez le test **Courrier SMTP entrant** situé sous **Tests E-mail sur Internet**. 
    
- Envoyez un message électronique à partir d'un compte de messagerie basé sur le web vers un destinataire de messagerie de votre organisation dont le domaine correspond au domaine ajouté au service. Vérifiez la remise du message à la boîte aux lettres locale à l'aide de Microsoft Outlook ou d'un autre client de messagerie.
    
- Si vous souhaitez effectuer un test de message sortant, vous pouvez envoyer un message électronique d'un utilisateur de votre organisation vers un compte de messagerie basé sur le web et confirmer sa réception.
    
> [!TIP]
> Une fois votre configuration terminée, aucune étape supplémentaire n'est requise pour activer la suppression du courrier indésirable et des programmes malveillants par EOP. Ces opérations sont effectuées automatiquement. Vous pouvez cependant adapter vos paramètres aux exigences de votre entreprise à l'aide du CAE. Pour plus d'informations, consultez la rubrique [Anti-Spam and Anti-Malware Protection](http://technet.microsoft.com/library/93c6c227-7442-4293-b64d-ec8f15c928db.aspx). > Votre service étant désormais opérationnel, nous vous recommandons de lire la rubrique [Meilleures pratiques de configuration d'EOP](best-practices-for-configuring-eop.md), qui décrit les paramètres recommandés et les éléments à prendre en compte suite à la configuration d'EOP. 
  

