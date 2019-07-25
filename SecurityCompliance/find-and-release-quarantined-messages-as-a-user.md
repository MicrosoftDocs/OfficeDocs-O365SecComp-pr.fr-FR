---
title: Rechercher et débloquer les messages en quarantaine en tant qu’utilisateur dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 05/19/2018
audience: Consumer/IW
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
ms.collection:
- M365-security-compliance
description: 'En tant qu’utilisateur Office 365, vous pouvez gérer votre propre courrier indésirable mis en quarantaine de deux manières : en répondant aux notifications de courrier indésirable qui vous sont directement envoyées (si votre administrateur l’a configuré) ou en utilisant la fonction de quarantaine du courrier indésirable dans le &amp;Centre de sécurité et conformité.'
ms.openlocfilehash: 20758876dbfe51f47d66c3c1eef4dcb3cee49768
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854578"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a>Rechercher et débloquer les messages en quarantaine en tant qu’utilisateur dans Office 365

En tant qu’utilisateur Office 365, vous pouvez gérer les messages mis en quarantaine plutôt que les messages qui vous sont envoyés de deux manières : en [répondant aux notifications de courrier indésirable qui vous sont directement envoyées](use-spam-notifications-to-release-and-report-quarantined-messages.md)(si votre administrateur l’a configuré) ou en utilisant le &amp;Centre de sécurité et conformité. 
  
> [!NOTE]
> En tant qu’administrateur, vous pouvez [gérer les messages en quarantaine](manage-quarantined-messages-and-files.md) pour d’autres utilisateurs de votre organisation. 
  
## <a name="view-messages-that-were-sent-to-quarantine-instead-of-to-you"></a>Afficher les messages mis en quarantaine, sans vous avoir été envoyés

1. Connectez-vous à Office 365 et[accédez au Centre de sécurité et conformité](go-to-the-securitycompliance-center.md)à l’aide de votre compte professionnel ou scolaire. 
    
2. À gauche, développez **Gestion des menaces**, sélectionnez **Révision**, puis **Quarantaine**.
    
    > [!TIP]
    > Pour accéder directement à la page **Quarantaine](go-to-the-securitycompliance-center.md) du Centre de sécurité](go-to-the-securitycompliance-center.md) et conformité, utilisez cette URL :> [https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
Par défaut, le Centre de sécurité&amp; et conformité affiche tous les messages e-mail mis en quarantaine en tant que courrier indésirable. Les messages sont triés du plus récent au plus ancien en fonction de leur **date** de réception. **Expéditeur**, **Objet** et la date d’expiration (sous **Expire**) sont également affichés pour chaque message. Vous pouvez trier un champ en cliquant sur l’en-tête de colonne correspondant. Cliquez une deuxième fois sur un en-tête de colonne pour inverser l’ordre de tri. 
  
Vous pouvez afficher la liste de tous les messages en quarantaine ou rechercher des messages spécifiques à l’aide du filtrage. Les opérations en bloc se limitent à 100 éléments et dès lors, le filtrage permet de réduire votre jeu de résultats en présence de plus d’éléments. Vous pouvez rapidement filtrer les messages pour une même raison de mise en quarantaine en sélectionnant une option à partir de la liste déroulante. Les options suivantes sont disponibles : 
  
- Courrier identifié comme courrier indésirable. Ces messages en quarantaine s’affichent par défaut.
    
- Courrier identifié comme courrier en nombre.
    
Après avoir trouvé un message en quarantaine spécifique, cliquez sur ce message pour afficher des détails le concernant et effectuer des actions. Vous pouvez diffuser le message dans votre boîte de réception, afficher un aperçu du message, télécharger le message ou supprimer immédiatement le message en quarantaine.
  
> [!NOTE]
> Dans Office 365, vous devez disposer d’autorisations d’administrateur pour utiliser les messages en quarantaine envoyés à d’autres utilisateurs. 
  
## <a name="to-filter-and-find-quarantined-messages"></a>Filtrer et rechercher les messages en quarantaine

En présence de nombreux éléments en quarantaine, vous pouvez limiter leur nombre en les filtrant.
  
1. Sur la page **Quarantaine**, indiquez si vous souhaitez afficher les messages en quarantaine liés au **courrier indésirable** ou au **courrier en nombre**. 
    
2. Sous **Trier les résultats par**, sélectionnez une combinaison de conditions en définissant les filtres qui conviennent (actuellement, vous ne pouvez pas utiliser de caractères génériques). Vous pouvez choisir parmi plusieurs conditions, notamment les suivantes :
    
  - **ID du message** Utilisez cet ID pour sélectionner un message spécifique, sous réserve de le connaître. 
    
    Par exemple, si un message est envoyé par un utilisateur de votre organisation, ou adressé à ce dernier, mais n'atteint jamais sa destination, vous pouvez rechercher le message à l'aide de la fonctionnalité de suivi des messages. (voir [Suivre un message et voir les résultats](https://go.microsoft.com/fwlink/?LinkId=799737)). Si vous découvrez que le message a été mis en quarantaine, parce qu'il correspond à une règle de messagerie ou a été identifié comme un courrier indésirable, vous pouvez facilement le retrouver en spécifiant son ID. Veillez à inclure la chaîne ID complète du message. Celle-ci peut comprendre des crochets (\<\>), par exemple : 
    
    \<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Adresse e-mail de l’expéditeur** Optez pour un filtrage basé sur l’adresse e-mail de l’expéditeur. 
    
  - **Adresse e-mail du destinataire** Optez pour un filtrage basé sur l’adresse e-mail du destinataire. 
    
  - **Objet** Entrez l’objet d’une adresse e-mail que vous souhaitez trouver. 
    
  - **Plage de dates** Vous pouvez choisir de filtrer selon la date à laquelle le fichier ou le message a été mis en quarantaine. Vous pouvez spécifier la date ou un intervalle de temps, avec dates et heures. 
    
  - **Date d’expiration**Pour effectuer une recherche par date d’expiration, sélectionnez **Filtre avancé**. Vous pouvez sélectionner les messages qui seront supprimés de la quarantaine au cours des prochaines 24 heures (**Aujourd’hui**), au cours des prochaines 48 heures (**2 prochains jours**), au cours de la semaine à venir (**7 prochains jours**) ou vous pouvez sélectionner un intervalle de temps personnalisé.
    
    > [!IMPORTANT]
    > Par défaut, le courrier indésirable et le courrier en nombre restent en quarantaine pendant 30 jours. Toutefois, cet intervalle de temps peut être configuré et votre administrateur peut avoir défini une période de rétention en quarantaine différente. Quand Office 365 supprime un message en quarantaine, vous ne pouvez pas le récupérer. 
  
## <a name="view-details-for-a-specific-message"></a>Afficher des détails pour un message spécifique

Après avoir sélectionné un message, vous pouvez consulter un récapitulatif de ses propriétés dans un volet à droite de la page.
  
- **ID du message :** identificateur unique du message. 
    
- **Adresse de l’expéditeur :**. personne qui a envoyé le message. 
    
- **Reçu :** date de réception du message. 
    
- **Objet : **texte de la ligne d’objet du message. 
    
- **Raison de mise en quarantaine :** indique si un message a été identifié comme **courrier indésirable** ou **courrier en nombre**.
    
- **Expire :** date à laquelle le message sera supprimé de la quarantaine. 
    
- **Diffusé à :** toutes les adresses e-mail (le cas échéant) auxquelles le message a été diffusé. 
    
- **Pas encore diffusé à**. Toutes les adresses e-mail (le cas échéant) auxquelles le message n’a pas encore été diffusé. Sélectionnez **Diffuser** si vous souhaitez que le message apparaisse dans votre boîte de réception (pour plus d’informations sur la diffusion de messages, voir la section suivante). 
    
Pour obtenir plus de détails sur le message, sélectionnez l’une des options suivantes :
  
- **Afficher l’en-tête du message** Sélectionnez ce lien pour afficher le texte d’en-tête du message. Pour analyser l’en-tête en détail, copiez le texte d’en-tête du message dans votre Presse-papiers, puis sélectionnez **Analyseur d’en-tête de message Microsoft**pour accéder à l’Analyseur de connectivité à distance (cliquez avec le bouton droit et sélectionnez Ouvrir dans un nouvel onglet si vous ne souhaitez pas laisser Office 365 accomplir cette tâche). Collez l’en-tête du message dans la section Analyseur d’en-tête de message de la page, puis sélectionnez Analyser les en-têtes. 
    
- **Aperçu du message** Vous permet de consulter les versions brutes ou HTML du texte du corps du message. Au format HTML, les liens sont désactivés. 
    
## <a name="manage-your-quarantined-messages"></a>Gérer vos messages en quarantaine

Après avoir sélectionné un message ou un groupe de messages, vous disposez de plusieurs options pour gérer les messages en quarantaine.
  
- Ne rien faire. Si vous choisissez de ne rien faire, Office 365 supprimera automatiquement le message arrivé à expiration. Pour rappel, quand Office 365 supprime un message mis en quarantaine, vous ne pouvez pas le récupérer.
    
- **Diffuser un message** Diffusez un message (ou plusieurs messages) mis en quarantaine pour l’envoyer vers votre boîte de réception. Lorsque vous diffusez un message, vous avez la possibilité de signaler ce message à Microsoft à des fins d’analyse. 
    
    Lorsque vous choisissez de signaler un message de type faux positif, le message est signalé à l’équipe d’analyse de courrier indésirable de Microsoft. Cette équipe évalue et analyse les messages de type faux positif, et selon les résultats de l’analyse, les règles de filtrage du courrier indésirable du service peuvent être ajustées pour permettre l’acheminement des messages.
    
- **Télécharger le message** Vous permet de télécharger le message sous forme de fichier .eml. Après avoir téléchargé un message, vous pouvez consulter le fichier .eml à l’aide de votre client de messagerie avant de le diffuser. 
    
- **Supprimer de la mise en quarantaine** Supprime immédiatement le message de la mise en quarantaine, sans diffuser le message dans votre boîte de réception. 
    

