---
title: Empêcher le courrier d’être marqué comme courrier indésirable dans Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 34823bbc-a3e3-4949-ba42-97c73997eeed
description: Découvrez comment empêcher le courrier d’être déplacé dans le dossier Courrier indésirable et marqué comme courrier indésirable dans Office 365.
ms.openlocfilehash: f7ba560b4eb30abcda4c97617ead883659558bd8
ms.sourcegitcommit: 6d72cdb882b93edf6dfddb5ff2e6d8a16e2fa0bc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25596717"
---
# <a name="how-to-prevent-real-email-from-being-marked-as-spam-in-office-365"></a>Empêcher le courrier d’être marqué comme courrier indésirable dans Office 365

 **Votre courrier est marqué comme courrier indésirable dans Office 365 ? Suivez ces conseils.**
  
Exchange Online Protection (EOP) tente de filtrer le courrier indésirable pour débarrasser votre boîte de réception du contenu que vous ne voulez pas voir. Mais il arrive qu’EOP filtre des messages que vous voulez voir.
  
## <a name="determine-the-reason-why-the-message-was-marked-as-spam"></a>Identifier pourquoi le message a été marqué comme courrier indésirable

Dans Office 365, de nombreux problèmes liés au courrier indésirable peuvent être résolus en [affichant les en-têtes de message](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) et en identifiant l’origine du problème. Si un en-tête de message nommé X-Forefront-Antispam-Report contenant la chaîne SFV:NSPM s’affiche, cela signifie qu’Exchange Online Protection (EOP) a analysé le message et l’a considéré comme du courrier indésirable. Dans ce cas, nous vous recommandons vivement d’[utiliser le complément Message de notification](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) pour nous aider à améliorer nos filtres. Si cette valeur n’apparaît pas dans les en-têtes, cela peut signifier que le message n’a pas été jusqu’au bout de l’analyse de courrier indésirable, ou qu’il y a eu un problème de configuration ayant entraîné le traitement du message comme un courrier indésirable. Pour en savoir plus, consultez l’article relatif aux [en-têtes de messages anti-courrier indésirable](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).
  
Dans l’en-tête, repérez les titres et les valeurs suivantes.
  
### <a name="x-forefront-antispam-report"></a>X-Forefront-Antispam-Report

- **SFV:BLK** Indique que le message a été marqué comme courrier indésirable, car l’adresse d’envoi figure dans la liste des expéditeurs bloqués du destinataire. 
    
- **SFV:SKS** Indique que le message a été marqué comme courrier indésirable avant le filtrage du contenu. Cela peut signifier qu’une règle de transport a marqué le message comme courrier indésirable. Exécutez un suivi des messages pour vérifier si une règle de transport s’est déclenchée et aurait pu configurer un seuil de probabilité de courrier indésirable élevé (SCL). 
    
- **SFV:SKB** Indique que le message a été marqué comme courrier indésirable, car il correspond à une liste d’expéditeurs bloqués dans la stratégie de filtrage du courrier indésirable. 
    
- **SFV:BULK** Indique que la valeur BCL figurant dans l’en-tête X-Microsoft-Antispam dépasse le seuil de probabilité de courrier en nombre défini pour le filtrage de contenu. Le courrier en nombre désigne le courrier auquel les utilisateurs peuvent être abonnés mais qui est considéré comme indésirable. Dans l’en-tête de messages X-Microsoft-Antispam, recherchez la propriété BCL (seuil de probabilité de courrier en nombre). Si cette valeur est inférieure au seuil défini dans le filtre anti-courrier indésirable, nous vous recommandons d’ajuster ce seuil pour que ces messages en nombre soient marqués comme courrier indésirable. Les utilisateurs tolèrent différemment le courrier en nombre et ont différentes préférences concernant son [traitement](https://blogs.msdn.microsoft.com/tzink/2014/08/25/different-levels-of-bulk-mail-filtering-in-office-365/). Vous pouvez créer des stratégies ou des règles différentes selon les préférences des utilisateurs.
    
- **CAT:SPOOF** ou **CAT:PHISH** Indique que le message semble être falsifié, ce qui signifie que la source du message ne peut pas être validée et pourrait être suspecte. Si l’expéditeur est valide, il doit s’assurer qu’une configuration SPF et DKIM adaptée est mise en place. Vérifiez l’en-tête Authentication-Results pour obtenir des informations complémentaires. Même s’il est difficile de convaincre tous les expéditeurs d’utiliser des méthodes d’authentification de messagerie appropriées, ignorer ces vérifications peut être très dangereux et entraîner des failles de sécurité. 
    
### <a name="x-customspam"></a>x-customspam

- La présence de cet en-tête indique que le message a été marqué comme courrier indésirable, car l’une des [options avancées de filtrage anti-courrier indésirable est activée](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx) dans votre filtre anti-courrier indésirable. Sauf si vous avez besoin de ces fonctionnalités, nous vous conseillons d’utiliser les paramètres par défaut. 
    
## <a name="solutions-to-additional-causes-of-too-much-spam"></a>Solutions à appliquer en cas de courrier indésirable excessif

Pour travailler efficacement, Exchange Online Protection (EOP) exige que les administrateurs effectuent certaines tâches. Si vous n’êtes pas l’administrateur de votre client Office 365 et que vous recevez trop de courrier indésirable, nous vous recommandons de travailler avec votre administrateur sur ces tâches. Dans le cas contraire, vous pouvez passer directement à la section dédiée aux utilisateurs.
  
### <a name="for-admins"></a>Pour les administrateurs

- **Pointez vos enregistrements DNS vers Office 365** Pour qu’EOP vous protège efficacement du courrier indésirable, les enregistrements DNS de votre serveur de messagerie (MX) pour tous les domaines doivent pointer vers Office 365 uniquement. Si votre MX ne pointe pas vers Office 365, EOP ne filtre pas le courrier indésirable pour vos utilisateurs. Si vous voulez utiliser un autre service ou dispositif pour filtrer le courrier indésirable dans votre domaine, pensez à désactiver la protection contre le courrier indésirable dans EOP. Pour cela, vous pouvez créer une règle de transport qui définit la valeur SCL sur -1. Si, plus tard, vous décidez d’utiliser EOP, pensez à supprimer cette règle de transport. 
    
- **Désactivez le filtrage SmartScreen dans Outlook** Si vos utilisateurs utilisent le client Outlook pour ordinateur de bureau, ils doivent désactiver la fonctionnalité de filtrage SmartScreen, qui n’est plus disponible. Si elle est activée, elle peut générer des faux positifs. Ignorez cette étape si vous exécutez un client Outlook pour ordinateur de bureau mis à jour. 
    
- **Activez le complément Message de notification pour les utilisateurs** Nous vous recommandons vivement d’[activer le complément Message de notification pour vos utilisateurs](enable-the-report-message-add-in.md). En tant qu’administrateur, vous pouvez également consulter les commentaires envoyés par vos utilisateurs et utiliser des modèles pour ajuster les paramètres qui peuvent être à l’origine des problèmes.
    
- **Autorisez immédiatement un expéditeur** Si vous avez besoin d’autoriser immédiatement un expéditeur, nous vous recommandons vivement d’**autoriser UNIQUEMENT les adresses IP d’un expéditeur particulier**. Vous pouvez également autoriser un expéditeur et vérifier que l’expéditeur passe au travers de la vérification d’authentification telles que SPF ou DKIM, en créant une règle de transport qui recherche **à la fois** le domaine de l’expéditeur et un en-tête Authentication-Results positif. 
    
### <a name="for-users"></a>Pour les utilisateurs

- **Signalez le courrier indésirable à Microsoft** Signalez les messages indésirables à Microsoft à l’aide du [complément Message de notification](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Vous pouvez également envoyer un message à junk@office365.microsoft.com et joindre un ou plusieurs messages au rapport.
    
    **Important** Si vous ne transférez pas les messages en pièces jointes, [les en-têtes seront manquants et nous ne serons pas en mesure d’améliorer](https://blogs.msdn.microsoft.com/tzink/2017/11/30/when-creating-support-tickets-about-spam-be-sure-to-include-message-headers/) le filtre anti-courrier indésirable dans Office 365. 
    
- **Ajoutez un expéditeur à votre liste d’expéditeurs autorisés (avec parcimonie)** En dernier recours, vous pouvez [le bloquer ou l’autoriser (paramètres du courrier indésirable)](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). Si vous le faites, une tentative de hameçonnage ciblée peut être autorisée dans votre boîte de réception.
    

