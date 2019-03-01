---
title: Réduire le courrier indésirable dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 07824c51-2c45-4005-8596-03c0d7c4ff2a
description: Découvrez les méthodes fréquemment utilisées pour réduire le courrier indésirable dans Office 365.
ms.openlocfilehash: 0cc07d543618b154570231dcf1d45b39cfe20fec
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295507"
---
# <a name="how-to-reduce-spam-email-in-office-365"></a>Réduire le courrier indésirable dans Office 365

 **Vous recevez trop de courrier indésirable dans Office 365 ? Suivez ces conseils.**
  
Nous vous recommandons vivement de signaler les messages de faux négatifs en [à l’aide du complément Message rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) Aidez-nous à améliorer notre filtres. En outre, vous pouvez transférer le message *tant que pièce jointe* junk@office365.microsoft.com ou phish@office365.microsoft.com (s’il s’agit hameçon).

>[Avertissement] Si vous pensez que le message est indésirable, il est dans le dossier courrier indésirable, qui ne doit pas être un problème. Si vous souhaitez ne figure pas dans la boîte aux lettres, vous devez modifier la stratégie anti-courrier indésirable pour mettre en quarantaine le message. Plus d’informations sur la mise en quarantaine un message est accessible dans [mise en quarantaine courriers électroniques dans Office 365](quarantine-email-messages.md).

## <a name="fixing-allowed-spam"></a>Résolution du courrier indésirable autorisé

Souvent, nous voyons que les clients obtiennent un courrier indésirable dans leur boîte de réception en raison de configurations incorrectes. Le plus courant consiste à configurer vos domaines dans une règle de transport à contourner les filtres ou répertoriant vos domaines dans la liste des expéditeurs/safe autorisés. Ce n’est pas bon, car ces messages ignorent le filtrage du courrier indésirable et pourraient sinon être capturés.  

## <a name="solutions-to-other-common-causes-of-getting-too-much-spam"></a>Solutions à appliquer en cas de courrier indésirable excessif

Pour éviter que vous receviez trop de courrier indésirable, Exchange Online Protection (EOP) exige que les administrateurs effectuent certaines tâches. Si vous n’êtes pas l’administrateur de votre client Office 365 et que vous recevez trop de courrier indésirable, nous vous recommandons de travailler avec votre administrateur sur ces tâches. Dans le cas contraire, vous pouvez passer directement à la section dédiée aux utilisateurs.
  
### <a name="for-admins"></a>Pour les administrateurs

- **Pointez vos enregistrements DNS vers Office 365** Pour qu’EOP vous protège au mieux du courrier indésirable, les enregistrements DNS de votre serveur de messagerie (MX) pour tous les domaines doivent pointer vers Office 365 uniquement. Consultez l’article sur la [création d’enregistrements DNS pour Office 365 pendant la gestion de vos enregistrements DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).
    
- **Activez la règle de courrier indésirable dans toutes les boîtes aux lettres** L’action de filtrage du courrier indésirable est définie par défaut sur **Déplacer le message vers le dossier Courrier indésirable**. S’il s’agit de l’action favorite active de la stratégie anti-courrier indésirable, [la règle de courrier indésirable doit également être activée](https://support.office.com/fr-FR/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089) dans chaque boîte aux lettres. Pour le vérifier, vous pouvez exécuter la cmdlet Get-MailboxJunkEmailConfiguration dans une ou plusieurs boîtes aux lettres. Par exemple, vous pouvez vérifier toutes les boîtes aux lettres en exécutant la commande suivante : Get-MailboxJunkEmailConfiguration -Identity \* | Where {$_.Enabled -eq $false}
    
    Quand le résultat s’affiche, la propriété Enable doit être définie sur True. Si elle est définie sur False, vous pouvez exécuter la commande Set-MailboxJunkEmailConfiguration pour la définir sur True.
    
- **Créez des règles de flux de messagerie dans Exchange Server local** Si vous utilisez Exchange Online Protection, mais que vos boîtes aux lettres se trouvent dans l’environnement Exchange Server local, créez des règles de flux de messagerie dans l’environnement Exchange Server local. Consultez les [instructions relatives à EOP](https://docs.microsoft.com/previous-versions/exchange-server/exchange-150/jj900470(v=exchg.150)).
    
- **Marquez le courrier en nombre comme courrier indésirable** Le courrier en nombre désigne le courrier auquel les utilisateurs peuvent être abonnés mais qui est considéré comme indésirable. Dans l’en-tête de messages X-Microsoft-Antispam, recherchez la propriété BCL (seuil de probabilité de courrier en nombre). Si cette valeur est inférieure au seuil défini dans le filtre anti-courrier indésirable, nous vous recommandons d’ajuster ce seuil pour que ces messages en nombre soient marqués comme courrier indésirable. Les utilisateurs tolèrent différemment le courrier en nombre et ont différentes préférences concernant son [traitement](https://docs.microsoft.com/fr-FR/office365/SecurityCompliance/bulk-complaint-level-values). Vous pouvez créer des stratégies ou des règles différentes selon les préférences des utilisateurs. 
    
- **Bloquez immédiatement un expéditeur** Si vous devez immédiatement bloquer un expéditeur, vous pouvez bloquer son adresse e-mail, son domaine ou son adresse IP. Consultez l’article sur le [blocage du courrier indésirable avec le filtre Office 365 pour éviter les faux négatifs](create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365.md#use-the-eac-to-create-a-transport-rule-that-blocks-messages-sent-from-a-domain-or-user). Une entrée dans la liste verte d’un utilisateur final peut remplacer un blocage défini par l’administrateur.
    
- **Activez le complément Message de notification pour les utilisateurs** Nous vous recommandons vivement d’[activer le complément Message de notification pour vos utilisateurs](enable-the-report-message-add-in.md). En tant qu’administrateur, vous pouvez également consulter les commentaires envoyés par vos utilisateurs et utiliser des modèles pour ajuster les paramètres qui peuvent être à l’origine des problèmes.
    
### <a name="for-users"></a>Pour les utilisateurs

- **Activez la règle de courrier indésirable et vérifiez votre liste verte** Vérifiez que la règle de l’action anti-courrier indésirable est activée et que l’expéditeur ou le domaine de l’expéditeur ne peut pas être remplacé dans votre liste verte. Pour accéder à ces paramètres, accédez aux paramètres du courrier indésirable [Bloquer ou autoriser](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). Ici, vous pouvez également choisir de bloquer l’adresse e-mail ou le domaine de l’expéditeur.
    
- **Signalez le courrier indésirable à Microsoft** Signalez les messages indésirables à Microsoft à l’aide du [complément Message de notification](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Vous pouvez également envoyer un message à junk@office365.microsoft.com et joindre un ou plusieurs messages au rapport.
    
    **Important** Si vous ne transférez pas les messages en pièces jointes, les en-têtes seront manquants et nous ne serons pas en mesure d’améliorer le filtre anti-courrier indésirable dans Office 365. 
    
- **Désabonnez-vous du courrier en nombre** Si vous vous êtes abonné à ce message (bulletin d’informations, annonce de produit, etc.) et qu’il contient un lien Se désabonner provenant d’une source de confiance, nous vous recommandons simplement de vous désabonner. Généralement, Office 365 ne traite pas ces messages comme du courrier indésirable. Vous pouvez également choisir de bloquer l’expéditeur, ou de demander à votre administrateur de modifier les paramètres pour que tout le courrier en nombre soit traité comme du courrier indésirable.
