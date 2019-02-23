---
title: Rechercher et débloquer les messages mis en quarantaine en tant qu'utilisateur dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/19/2018
ms.audience: Consumer/IW
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
ms.collection:
- M365-security-compliance
description: "En tant qu'utilisateur d'Office 365, vous pouvez gérer vos propres messages de courrier indésirable mis en quarantaine de l'une des deux façons suivantes: en répondant aux notifications de courrier indésirable qui vous sont envoyées directement (si votre administrateur a configuré cette fonctionnalité &amp; ) ou en utilisant la fonctionnalité de mise en quarantaine du courrier indésirable dans la conformité de sécurité. Interactif."
ms.openlocfilehash: acbf862f05a9282a26444b738400d29c03d07f1f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214994"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a>Rechercher et débloquer les messages mis en quarantaine en tant qu'utilisateur dans Office 365

En tant qu'utilisateur d'Office 365, vous pouvez gérer les messages qui ont été envoyés en quarantaine au lieu de vous envoyer de l'une des deux façons suivantes: en [répondant aux notifications de courrier](use-spam-notifications-to-release-and-report-quarantined-messages.md) indésirable qui vous ont été envoyées directement (si votre &amp; administrateur a configuré cela) ou à l'aide du centre de sécurité conformité. 
  
> [!NOTE]
> Si vous êtes administrateur, vous pouvez [gérer les messages mis en quarantaine](manage-quarantined-messages-and-files.md) pour d'autres personnes de votre organisation. 
  
## <a name="view-messages-that-were-sent-to-quarantine-instead-of-to-you"></a>Afficher les messages qui ont été envoyés en quarantaine au lieu de vous

1. Connectez-vous à Office 365 et [accédez au centre de sécurité et de conformité](go-to-the-securitycompliance-center.md) à l'aide de votre compte professionnel ou scolaire. 
    
2. À gauche, développez **gestion des menaces**, **** réViser, puis **mettre en quarantaine**.
    
    > [!TIP]
    > Pour accéder directement à la page de **mise en quarantaine** dans &amp; le centre de sécurité conformité, utilisez l'URL suivante: >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
Par défaut, le centre &amp; de sécurité conformité affiche tous les messages électroniques mis en quarantaine en tant que courrier indésirable. Les messages sont triés du plus récent au plus ancien en fonction de la **Date** de réception du message. L' **expéditeur**, l' **objet**et la date d'expiration ( **** sous expire) sont également affichés pour chaque message. Vous pouvez effectuer un tri sur un champ en cliquant sur l'en-tête de colonne correspondant; Cliquez une deuxième fois sur un en-tête de colonne pour inverser l'ordre de tri. 
  
Vous pouvez afficher la liste de tous les messages mis en quarantaine, ou vous pouvez rechercher des messages spécifiques en les filtrant. Vous pouvez uniquement effectuer des opérations en bloc sur un maximum de 100 éléments, de sorte que le filtrage peut également contribuer à réduire votre jeu de résultats si vous avez plus de. Vous pouvez rapidement filtrer les messages pour une seule raison de mise en quarantaine en choisissant une option dans la liste déroulante. Les options sont les suivantes:
  
- Message identifié comme courrier indésirable. Par défaut, ces messages mis en quarantaine sont affichés.
    
- Courrier électronique identifié comme courrier en nombre.
    
Une fois que vous avez trouvé un message en quarantaine spécifique, cliquez sur le message pour en afficher les détails et prendre des mesures. Vous pouvez diffuser le message vers votre boîte aux lettres, afficher un aperçu du message, Télécharger le message ou supprimer immédiatement le message de la mise en quarantaine.
  
> [!NOTE]
> Vous devez disposer des autorisations d'administrateur dans Office 365 pour utiliser des messages mis en quarantaine qui ont été envoyés à d'autres utilisateurs. 
  
## <a name="to-filter-and-find-quarantined-messages"></a>Pour filtrer et rechercher les messages mis en quarantaine

Si vous avez un grand nombre d'éléments mis en quarantaine, vous pouvez réduire le nombre à un ensemble gérable en les filtrant.
  
1. Sur la page **mise en quarantaine** , indiquez si vous souhaitez afficher les messages de courrier indésirable ou mis **en** quarantaine. **** 
    
2. Sous **Trier les résultats par**, choisissez n'importe quelle combinaison de conditions en définissant le filtre ou les filtres appropriés (vous ne pouvez pas utiliser de caractères génériques pour le moment). Vous pouvez choisir plusieurs conditions, notamment les suivantes:
    
  - **ID du message** Utilisez cette option pour sélectionner un message spécifique lorsque vous êtes informé de l'ID du message. 
    
    Par exemple, si un message spécifique est envoyé par un utilisateur de votre organisation ou s'il est destiné à celui-ci, mais qu'il n'a jamais atteint sa destination, vous pouvez rechercher le message à l'aide d'un suivi des messages (consultez [la rubrique exécution d'un suivi de message et affichage des résultats](https://go.microsoft.com/fwlink/?LinkId=799737)). Si vous découvrez que le message a été envoyé en quarantaine, peut-être parce qu'il correspond à une règle de flux de messagerie ou qu'il a été identifié comme courrier indésirable, vous pouvez facilement trouver ce message en quarantaine en spécifiant son ID de message. Veillez à inclure la chaîne d'ID de message complète. Cela peut inclure des chevrons\<\>(), par exemple:
    
    \<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Adresse de messagerie** de l'expéditeur Choisissez de filtrer par une adresse de messagerie d'expéditeur unique. 
    
  - **Adresse de messagerie du destinataire** Choisissez de filtrer par une seule adresse de courrier de destinataire. 
    
  - **Objet** Entrez l'objet de l'adresse de messagerie que vous souhaitez trouver. 
    
  - **Plage de dates** Vous pouvez choisir de filtrer selon la date à laquelle le message a été envoyé en quarantaine. Vous pouvez spécifier la date ou une plage de dates, y compris l'heure. 
    
  - **Date d'expiration** Pour filtrer par date d'expiration, choisissez **filtre avancé**. Vous pouvez sélectionner les messages qui seront supprimés de la quarantaine au cours des prochaines 24 heures ( **aujourd'hui**), au cours des prochaines 48 heures ( **2 prochains jours**), au cours de la semaine suivante (7 prochains **jours**) ou vous pouvez sélectionner un intervalle de temps personnalisé.
    
    > [!IMPORTANT]
    > Par défaut, le courrier indésirable et les messages en masse sont conservés en quarantaine pendant 30 jours. Toutefois, cette période est configurable et votre administrateur peut avoir défini une période de rétention de quarantaine différente. Lorsque Office 365 supprime un message de la mise en quarantaine, vous ne pouvez pas le récupérer. 
  
## <a name="view-details-for-a-specific-message"></a>Afficher les détails d'un message spécifique

Une fois que vous avez sélectionné un message, un résumé des propriétés du message s'affiche dans un volet sur le côté droit de la page.
  
- **ID du message:** Identificateur unique du message. 
    
- **Adresse de l'expéditeur:** Qui a envoyé le message. 
    
- **Reçu:** Date à laquelle le message a été reçu. 
    
- **Objet:** Texte de la ligne d'objet du message. 
    
- **Raison de la mise en quarantaine:** Indique si un message a été identifié comme **courrier** indésirable ou **en bloc**.
    
- **Date d'expiration:** Date à laquelle le message sera supprimé de la quarantaine. 
    
- **Publié dans:** Toutes les adresses de messagerie (le cas échéant) vers lesquelles le message a été publié. 
    
- **Pas encore publié dans:** Toutes les adresses de messagerie (le cas échéant) auxquelles le message n'a pas été libéré. Vous pouvez choisir **Release** si vous souhaitez diffuser le message vers votre boîte aux lettres (en savoir plus sur la publication des messages dans la section suivante). 
    
Vous pouvez obtenir encore plus d'informations sur le message en choisissant l'une des options suivantes:
  
- **Afficher l'en-tête de message** Choisissez cette sélection pour afficher le texte d'en-tête du message. Pour analyser l'en-tête en profondeur, copiez le texte d'en-tête de message dans votre presse-papiers, puis choisissez analyseur d' **en-têtes de message Microsoft** pour accéder à l'analyseUr de connectivité à distance (cliquez avec le bouton droit et choisissez Ouvrir dans un nouvel onglet si vous ne souhaitez pas laisser Office 365 Effectuez cette tâche). Collez l'en-tête du message sur la page dans la section analyseur d'en-têtes de message, puis choisissez analyser les en-têtes. 
    
- **Aperçu du message** Permet d'afficher les versions brutes ou HTML du texte du corps du message. En mode HTML, les liens sont désactivés. 
    
## <a name="manage-your-quarantined-messages"></a>Gérer les messages mis en quarantaine

Une fois que vous avez sélectionné un message ou un groupe de messages, vous disposez de plusieurs options pour la gestion des messages en quarantaine.
  
- Ne rien faire. Si vous choisissez de ne rien faire, le message sera automatiquement supprimé par Office 365 lors de son expiration. N'oubliez pas que lorsque Office 365 supprime un message de la mise en quarantaine, vous ne pouvez pas le récupérer.
    
- **Message de publication** Diffuser un message en quarantaine (ou un ensemble de messages) de sorte que le message soit envoyé à votre boîte aux lettres. Lorsque vous libérez un message, vous avez la possibilité de signaler le message à Microsoft pour analyse. 
    
    Lorsque vous choisissez de signaler un message, également appelé «signalement d'un message comme faux positif», le message est signalé à l'équipe d'analyse du courrier inDésirable de Microsoft. L'équipe évalue et analyse les messages faux positifs et, en fonction des résultats de l'analyse, les règles de filtrage de contenu de courrier indésirable à l'échelle du service peuvent être ajustées pour autoriser ces messages.
    
- **Télécharger le message** Vous permet de télécharger le message en tant que fichier. eml. Une fois que vous avez téléchargé un message, vous pouvez examiner le fichier. eml à l'aide de votre client de messagerie avant de publier le message. 
    
- **Supprimer de la quarantaine** Supprime le message immédiatement de la mise en quarantaine sans diffuser le message à votre boîte aux lettres. 
    

