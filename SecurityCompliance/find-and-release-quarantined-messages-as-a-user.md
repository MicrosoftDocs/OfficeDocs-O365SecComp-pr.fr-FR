---
title: Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/19/2018
ms.audience: Consumer/IW
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MEW150
ms.assetid: efff08ec-68ff-4099-89b7-266e3c4817be
description: 'En tant qu’un utilisateur d’Office 365, vous pouvez gérer vos propres messages mis en quarantaine du courrier indésirable d’une des deux façons : en répondant spam notifications envoyées directement (si votre administrateur a configuré cette fonctionnalité), ou à l’aide de la fonctionnalité de mise en quarantaine du courrier indésirable dans la sécurité &amp; la conformité Centre.'
ms.openlocfilehash: 728273838d9e592e17638638258f481830bc0bbe
ms.sourcegitcommit: f7fff49ae0b1c3056faa58d73c1070cb4e638fbf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018888"
---
# <a name="find-and-release-quarantined-messages-as-a-user-in-office-365"></a>Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur dans Office 365

En tant qu’un utilisateur d’Office 365, vous pouvez gérer les messages qui ont été mis en quarantaine au lieu de reçu de deux façons : en [répondre aux notifications de courrier indésirable envoyé directement](use-spam-notifications-to-release-and-report-quarantined-messages.md) (si votre administrateur a configuré cette), ou à l’aide de la sécurité &amp; centre de conformité. 
  
> [!NOTE]
> Si vous êtes un administrateur, vous pouvez [Gérer les messages mis en quarantaine](manage-quarantined-messages-and-files.md) par d’autres personnes dans votre organisation. 
  
## <a name="view-messages-that-were-sent-to-quarantine-instead-of-to-you"></a>Afficher les messages qui ont été mis en quarantaine au lieu de vous

1. Connectez-vous à Office 365 et [accédez au centre de conformité et de sécurité](go-to-the-securitycompliance-center.md) à l’aide de votre compte professionnel ou de l’école. 
    
2. Sur la gauche, développez **Threat Management**, sélectionnez **révision**, puis **mise en quarantaine**.
    
    > [!TIP]
    > Pour accéder directement à la page **mise en quarantaine** dans la sécurité &amp; centre de conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)
  
Par défaut, la sécurité &amp; centre de conformité affiche tous les messages électroniques qui ont été mis en quarantaine en tant que courrier indésirable. Les messages sont triés de la plus récente à la plus ancienne en fonction de la **Date** du message a été reçu. **L’expéditeur**, **l’objet**et la date d’expiration (sous **date d’expiration** ) sont également affichées pour chaque message. Vous pouvez trier sur un champ en cliquant sur l’en-tête de colonne correspondant ; Cliquez sur un en-tête de colonne une deuxième fois afin d’inverser l’ordre de tri. 
  
Vous pouvez afficher une liste de tous les messages mis en quarantaine, ou vous pouvez rechercher des messages spécifiques par le filtrage. Vous pouvez uniquement effectuer des opérations en bloc sur jusqu'à 100 éléments, afin que le filtrage permet également de réduire votre jeu de résultats si vous disposez de plusieurs qui. Vous pouvez rapidement filtrer les messages pour une raison unique en choisissant une option dans la liste déroulante. Les options sont les suivantes :
  
- Messages identifiés comme courrier indésirable. Ces messages mis en quarantaine sont affichées par défaut.
    
- Messages identifiés comme courrier indésirable.
    
Une fois que vous trouvez un message en quarantaine spécifique, cliquez sur le message pour afficher les détails et effectuer des actions. Vous pouvez libérer le message vers votre boîte aux lettres, afficher un aperçu du message, téléchargez le message ou supprimer le message en quarantaine immédiatement.
  
> [!NOTE]
> Vous devez disposer des autorisations d’administrateur dans Office 365 pour travailler avec des messages mis en quarantaine qui ont été envoyés à d’autres utilisateurs. 
  
## <a name="to-filter-and-find-quarantined-messages"></a>Pour filtrer et rechercher les messages mis en quarantaine

Si vous avez un grand nombre d’éléments mis en quarantaine, vous pouvez réduire le nombre à un ensemble gérable en filtrant les.
  
1. Dans la page **mise en quarantaine** , choisissez si vous souhaitez afficher **le courrier indésirable** ou **en bloc** des messages mis en quarantaine. 
    
2. Sous **trier les résultats par**, sélectionnez n’importe quelle combinaison des conditions en définissant le filtre approprié ou des filtres (vous ne pouvez pas utiliser des caractères génériques pour l’instant). Il existe plusieurs conditions, que vous pouvez choisir, notamment les suivantes :
    
  - **ID de message** Permet de sélectionner un message spécifique lorsque vous connaissez l’ID de message. 
    
    Par exemple, si un message spécifique est envoyé par ou destiné à être, un utilisateur dans votre organisation, mais il n’a jamais atteint sa destination, vous pouvez rechercher pour le message à l’aide d’un suivi des messages (voir [exécuter un suivi des messages et afficher les résultats](https://go.microsoft.com/fwlink/?LinkId=799737)). Si vous découvrez que le message a été mis en quarantaine, peut-être parce qu’il correspondait à une règle de flux de messagerie ou a été identifié comme courrier indésirable, puis retrouver facilement ce message en quarantaine en spécifiant son ID de Message. Veillez à inclure toute la chaîne d’ID de Message. Cela peut inclure des signes (\<\>), par exemple :
    
    \<79239079-D95A-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com\>
    
  - **Adresse de messagerie de l’expéditeur** Choisir de filtrer par une adresse de messagerie unique de l’expéditeur. 
    
  - **Adresse de messagerie de destinataire** Choisir de filtrer par une adresse de messagerie du destinataire unique. 
    
  - **Objet** Entrez l’objet d’une adresse de messagerie à rechercher. 
    
  - **Plage de dates** Vous pouvez choisir de filtrer par date que le message a été mis en quarantaine. Vous pouvez spécifier la date ou une plage de dates, y compris l’heure. 
    
  - **Date d’expiration** Pour filtrer par date d’expiration, cliquez sur **filtre avancé**. Vous pouvez sélectionner les messages seront supprimés de la mise en quarantaine dans les 24 heures ( **aujourd'hui**), dans les 48 heures ( **suivant 2 jours**), au sein de la semaine suivante ( **Next 7 jours**), ou vous pouvez sélectionner un intervalle de temps personnalisé.
    
    > [!IMPORTANT]
    > Par défaut, les messages de courrier indésirable et en bloc sont conservés dans la mise en quarantaine pendant 30 jours. Toutefois, cette période est configurable et votre administrateur peut avoir défini une période de rétention de mise en quarantaine. Lorsque Office 365 supprime un message de mise en quarantaine, vous ne pouvez pas le récupérer. 
  
## <a name="view-details-for-a-specific-message"></a>Afficher les détails d’un message spécifique

Après avoir sélectionné un message, vous verrez un résumé des propriétés de message dans un volet sur le côté droit de la page.
  
- **ID de message :** Identificateur unique pour le message. 
    
- **Adresse de l’expéditeur :** Qui a envoyé le message. 
    
- **Reçus :** La date de que réception du message. 
    
- **Objet :** Le texte de la ligne objet du message. 
    
- **Raison de mettre en quarantaine :** Indique si un message a été identifié comme **courrier indésirable** ou **en bloc**.
    
- **Expire :** La date lorsque le message sera supprimé de la mise en quarantaine. 
    
- **À :** Toutes les adresses de messagerie (le cas échéant) à laquelle le message a été envoyé. 
    
- **N’est pas encore publié à :** Toutes les adresses de messagerie (le cas échéant) à laquelle le message n’a pas été envoyé. Vous pouvez choisir la **version** si vous souhaitez le message vers votre boîte aux lettres (plus d’informations sur libération des messages dans la section suivante). 
    
Vous pouvez obtenir davantage d’informations sur le message en choisissant une des options suivantes :
  
- **En-tête du message** Choisissez cette option pour afficher le texte d’en-tête de message. Pour analyser l’en-tête de la profondeur, copier le texte d’en-tête de message dans le Presse-papiers, puis cliquez sur **L’analyseur en-tête de Message de Microsoft** pour accéder à l’Analyseur de connectivité à distance (avec le bouton droit et sélectionnez Ouvrir dans un nouvel onglet, si vous ne souhaitez pas laisser Office 365 Effectuez cette tâche). Coller l’en-tête du message sur la page dans la section analyseur d’en-tête de Message, puis choisissez analyser les en-têtes. 
    
- **Aperçu du message** Vous permet de voir brute ou versions HTML du texte du corps de message. Dans l’affichage HTML, les liens sont désactivés. 
    
## <a name="manage-your-quarantined-messages"></a>Gérer les messages mis en quarantaine

Après avoir sélectionné un message ou un groupe de messages, vous disposez de plusieurs options pour la gestion des messages en quarantaine.
  
- Ne rien faire. Si vous choisissez de ne rien faire, le message sera supprimé par Office 365 automatiquement à expiration. N’oubliez pas lorsqu’Office 365 supprime un message de quarantaine, vous ne pouvez pas le récupérer.
    
- **Libérer le message** Libérer un message mis en quarantaine (ou ensemble de messages) pour que le message est envoyé à votre boîte aux lettres. Lorsque vous relâchez un message, vous avez la possibilité de signaler le message à Microsoft pour analyse. 
    
    Lorsque vous choisissez de signaler un message, également appelé signale un message comme faux positif, le message est envoyé à l’équipe d’analyse de courrier indésirable Microsoft. L’équipe évalue et analyse des messages faux positifs et, en fonction des résultats de l’analyse, les règles de filtrage du courrier indésirable à l’échelle du service peuvent être ajustés pour autoriser les messages par le biais de.
    
- **Téléchargement des messages** Vous permet de télécharger le message comme un fichier .eml. Une fois que vous téléchargez un message, vous pouvez consulter le fichier .eml à l’aide de votre client de messagerie avant de libérer le message. 
    
- **Supprimer la mise en quarantaine** Supprime immédiatement le message en quarantaine sans libérer le message vers votre boîte aux lettres. 
    

