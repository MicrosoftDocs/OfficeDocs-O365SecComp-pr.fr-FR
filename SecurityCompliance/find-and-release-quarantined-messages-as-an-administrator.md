---
title: Rechercher et débloquer les messages mis en quarantaine en tant qu'administrateur
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: ab95bf17-bb09-4dd1-9990-ddd02ddecf05
description: Cette rubrique explique comment les administrateurs Exchange Online et Exchange Online Protection (EOP) peuvent rechercher, récupérer et signaler les messages mis en quarantaine dans le Centre d'administration Exchange (CAE).
ms.openlocfilehash: 5ebe65bf703087e8ad4bace827d84833eddb038f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027481"
---
# <a name="find-and-release-quarantined-messages-as-an-administrator"></a>Rechercher et débloquer les messages mis en quarantaine en tant qu'administrateur

Cette rubrique explique comment les administrateurs Exchange Online et Exchange Online Protection (EOP) peuvent rechercher, récupérer et signaler les messages mis en quarantaine dans le Centre d'administration Exchange (CAE). Office 365 envoie les messages en quarantaine soit parce qu'ils ont été identifiés comme courrier indésirable, soit parce qu'ils tombaient sous le coup d'une règle de transport. 
  
Utilisez la sécurité &amp; centre de conformité au lieu du CAE pour effectuer l’une de ces tâches, ainsi qu’afficher et travailler avec des messages qui ont été mis en quarantaine parce qu’ils contiennent des programmes malveillants. Pour plus d’informations, voir les [messages électroniques de mise en quarantaine dans Office 365](https://support.office.com/en-US/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).
  
Les messages mis en quarantaine sont répertoriés sur la page de **mise en quarantaine** dans le CAE. Par défaut, les messages sont triés du plus récent au plus ancien sur la base du champ **REÇU**. Les valeurs **EXPÉDITEUR**, **OBJET** et **EXPIRE** sont également indiquées pour chaque message. Vous pouvez ordonner les messages en fonction des valeurs de l'un ou l'autre de ces champs en cliquant sur leur en-tête. Pour inverser l'ordre, cliquez sur l'en-tête de colonne une seconde fois. La page de **mise en quarantaine** affiche un maximum de 500 messages. 
  
Vous pouvez consulter la liste de tous les messages mis en quarantaine, ou rechercher des messages spécifiques en indiquant des critères de filtrage (le filtrage peut également vous aider à réduire l'ensemble de résultats si vous avez plus de 500 messages). Après avoir recherché et localisé un message spécifique mis en quarantaine, vous pouvez consulter ses détails. Vous pouvez également effectuer les actions suivantes :
  
- Diffuser le message à un ou plusieurs destinataires, et éventuellement le signaler comme faux positif (« légitime ») à l'équipe d'analyse du courrier indésirable de Microsoft, qui l'évaluera et l'analysera. Selon les résultats de l'analyse, les règles de filtrage de contenu du courrier indésirable du service peuvent être ajustées pour autoriser le message.
    
- Diffuser le message et autoriser tous les futurs messages provenant de cet expéditeur.
    
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer
<a name="sectionSection0"> </a>

- Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations dont vous avez besoin, consultez l’entrée « Quarantaine » dans la rubrique [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Vous pouvez diffuser ou signaler plusieurs messages à la fois sur la page de **mise en quarantaine**. Vous pouvez également créer un script Windows PowerShell à distance pour accomplir cette tâche. Utilisez la cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) pour rechercher des messages et la cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) pour les diffuser. 
    
- Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013**Raccourcis clavier dans le Centre d'administration Exchange**.
    
> [!TIP]
> Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351). 
  
## <a name="use-advanced-search-to-filter-and-locate-quarantined-messages"></a>Utilisation de la recherche avancée pour filtrer et rechercher des messages
<a name="BKMK_UseAdvancedSearchtoFilterMessages"> </a>

Dans le centre d'administration Exchange, une recherche avancée vous permet de filtrer des éléments mis en quarantaine sur la base de diverses conditions. Vous pouvez utiliser ces conditions séparément ou les combiner. La recherche fournit la liste des messages qui répondent à tous vos critères de filtrage.
  
1. Dans le CAE, accédez à **Protection** \> **Quarantaine**, puis cliquez sur **Recherche avancée**.
    
2. Dans la fenêtre **Recherche avancée**, sélectionnez une combinaison quelconque des conditions suivantes. Pour sélectionner une condition, activez la case à cocher associée. Les caractères génériques ne sont pas pris en charge. 
    
1. **ID du message** Vous pouvez utiliser ce paramètre pour effectuer une recherche ciblée d'un message spécifique. Par exemple, si un message est envoyé par un utilisateur de votre organisation, ou adressé à ce dernier, mais n'atteint jamais sa destination, vous pouvez rechercher le message à l'aide de la fonctionnalité de suivi des messages. Pour plus d'informations, consultez la rubrique [Exécution d'un suivi de message et affichage des résultats](http://technet.microsoft.com/library/74a9fc59-7e0e-4832-baf9-2a86418b0079.aspx). Si vous découvrez que le message a été mis en quarantaine, parce qu'il correspond à une règle ou a été identifié comme un courrier indésirable, vous pouvez facilement le retrouver en spécifiant son ID. Veillez à inclure toute la chaîne d'ID de message. Celle-ci peut comprendre des crochets (\<\>). 
    
2. **Adresse de messagerie de l'expéditeur** Spécifiez l'adresse de messagerie de la personne qui a envoyé le message. 
    
3. **Adresse de messagerie du destinataire** Spécifiez l'adresse de messagerie du destinataire du message. 
    
4. **Objet** Spécifiez le texte de la ligne d'objet du message. 
    
5. **Reçu** Vous pouvez indiquer que le message a été mis en quarantaine au cours des dernières 24 heures ( **Aujourd'hui**), au cours des dernières 48 heures ( **2 derniers jours**), au cours de la semaine écoulée ( **7 derniers jours**) ou vous pouvez sélectionner un intervalle de temps personnalisé au cours duquel le message a été mis en quarantaine. 
    
6. **Expire** Vous pouvez indiquer que le message sera supprimé de la quarantaine au cours des prochaines 24 heures ( **Aujourd'hui**), au cours des prochaines 48 heures ( **2 prochains jours**), au cours de la semaine à venir ( **7 prochains jours**) ou vous pouvez sélectionner un intervalle de temps personnalisé au cours duquel le message sera supprimé de la quarantaine.
    
    > [!IMPORTANT]
    > Par défaut, les messages de courrier indésirable mis en quarantaine sont conservés en quarantaine pendant 15 jours, tandis que les messages mis en quarantaine qui correspondent à une règle de transport sont maintenus en quarantaine pendant 7 jours. Une fois cette période écoulée, Office 365 supprime les messages qui ne peuvent ensuite plus être récupérés. La période de conservation des messages mis en quarantaine qui correspondent à une règle de transport n'est pas configurable. Vous pouvez raccourcir la période de rétention à l'aide du paramètre **Conserver les courriers indésirables pendant (jours)** dans vos stratégies de filtrage du contenu. Pour plus d'informations, consultez la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). 
  
7. **Type** Vous pouvez spécifier si le message recherché a été mis en quarantaine parce qu'il a été identifié comme **Courrier indésirable** ou parce qu'il correspondait à une **Règle de transport**.
    
3. Pour lancer la recherche avancée, cliquez sur **OK**. 
    
    > [!NOTE]
    > Pour effacer vos critères de recherche et afficher tous les messages en quarantaine, désactivez toutes les cases à cocher dans la fenêtre **Recherche avancée**, puis cliquez sur **OK**. 
  
Une fois la recherche de messages effectuée, les résultats correspondant aux critères que vous avez spécifiés s'affichent dans l'interface utilisateur. Le CAE ne permet pas d'afficher plus de 500. 
  
## <a name="view-details-about-a-specific-quarantined-message"></a>Affichage des détails sur un message mis en quarantaine
<a name="BKMK_ViewDetailsAboutaSpecificQuarantinedMessage"> </a>

Après avoir localisé un message spécifique sur la page de **mise en quarantaine**, vous pouvez en afficher les détails. 
  
1. Sur la page de **mise en quarantaine**, sélectionnez un message spécifique et un récapitulatif de ses propriétés dans le volet de détails sur la droite de l'écran. 
    
    Les valeurs d' **État du message** sont les suivantes : 
    
  - **Type** Indique si le message a été identifié comme **Courrier indésirable** ou correspondait à une **Règle de transport**.
    
  - **Expire** Date à laquelle le message sera supprimé de la quarantaine. 
    
    Les valeurs de **Détails du message** sont les suivantes : 
    
  - **Expéditeur** Adresse de messagerie de la personne ayant envoyé le message. 
    
  - **Objet** Texte de la ligne d'objet du message. 
    
  - **Reçu** Date à laquelle le message a été mis en quarantaine. 
    
  - **Taille** Taille du message exprimée en kilo-octets (Ko), ou en mégaoctets (Mo) si elle est supérieure à 999 Ko. 
    
  - **Afficher l'en-tête du message** Cliquez sur ce lien pour ouvrir la boîte de dialogue **en-tête de message**, qui permet de voir le texte de l'en-tête du message. Vous pouvez également copier le texte de l'en-tête du message dans le Presse-papiers et le coller dans l'[Analyseur d'en-tête de message](https://testconnectivity.microsoft.com/?tabid=mha). Une fois dans l'Analyseur d'en-tête de message, cliquez sur **Analyser les en-têtes** afin de récupérer des informations sur l'en-tête. 
    
    > [!TIP]
    > Pour plus d'informations sur les champs d'en-tête de message anti-courrier indésirable spécifiques insérés par le service, consultez la rubrique [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md). 
  
  - **Aperçu du message électronique** Cliquez sur ce lien pour passer en revue le texte du message. 
    
2. Si vous double-cliquez sur un message en quarantaine, la fenêtre **Message en quarantaine** s'ouvre en affichant les informations suivantes : 
    
  - **Envoyé à** Liste de toutes les adresses de messageries auxquelles le message a été envoyé. 
    
  - **Non encore envoyé à** Liste de toutes les adresses de messageries auxquelles le message n'a pas encore été envoyé. Pour libérer le message, vous pouvez cliquer sur le lien **Envoyer à**. Pour plus d'informations, consultez la rubrique suivante. 
    
  - **ID du message** Identificateur du message Internet (également appelé ID du client) figurant dans l'en-tête du message. 
    
    Pour revenir au volet principal de la quarantaine, cliquez sur **Fermer**. 
    
## <a name="release-messages-from-quarantine"></a>Diffusion des messages en quarantaine
<a name="sectionSection3"> </a>

Si vous souhaitez diffuser des messages à des destinataires, vos options sont les suivantes :
  
- [Diffuser un message en quarantaine et autoriser les futurs messages provenant de l'expéditeur](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessageallowfuturemessagesfromsender)
    
- [Diffuser un message en quarantaine à des destinataires spécifiques sans le signaler comme faux positif](find-and-release-quarantined-messages-as-an-administrator.md#Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive)
    
- [Diffuser un ou plusieurs messages en quarantaine à tous les destinataires](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipients)
    
- [Diffuser un ou plusieurs messages en quarantaine à tous les destinataires et signaler les faux positifs](find-and-release-quarantined-messages-as-an-administrator.md#Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives)
    
### <a name="release-a-quarantined-message-and-allow-future-messages-from-the-sender"></a>Diffuser un message en quarantaine et autoriser les futurs messages provenant de l'expéditeur
<a name="Releasequarantinedmessageallowfuturemessagesfromsender"> </a>

1. Dans le CAE, accédez à **Protection** \> **Quarantaine**.
    
2. Cliquez sur un message pour la sélectionner, puis cliquez sur l'icône **Diffuser le message** comme illustré dans la capture d'écran suivante. 
  
![Illustre la page de mise en quarantaine avec l'icône du message de libération mise en surbrillance et l'affichage des options de libération](media/36ee081f-3e30-40c9-8ce3-240cee1970cc.png)
  
Cliquez sur **Diffuser le message sélectionné et autoriser l'expéditeur** dans la liste déroulante. 
    
3. La boîte de dialogue **Diffuser le message et autoriser l'expéditeur** s'ouvre. Si vous voulez signaler le message à Microsoft, cliquez sur **Diffuser et autoriser**. Le message est diffusé à tous les destinataires auxquels il est adressé et tous les futurs messages provenant de cet expéditeur sont autorisés. Toutefois, si ce message a été mis en quarantaine en raison d'une règle de transport ou de son envoi par un expéditeur bloqué, les futurs messages de cet expéditeur continueront à être bloqués. 
    
### <a name="release-a-quarantined-message-to-specific-recipients-without-reporting-it-as-a-false-positive"></a>Diffuser un message en quarantaine à des destinataires spécifiques sans le signaler comme faux positif
<a name="Releasequarantinedmessagetospecificrecipientswithoutreportingasfalsepositive"> </a>

1. Dans le CAE, accédez à **Protection** \> **Quarantaine**.
    
2. Sélectionnez un message, cliquez sur l'icône **Diffuser le message**, puis sur **Diffuser le message à un ou plusieurs destinataires spécifiques** dans la liste déroulante. 
    
3. Dans la boîte de dialogue **Libérer le message**, sélectionnez l'une des options suivantes : 
    
  - **Envoyer le message à tous les destinataires** Si vous sélectionnez cette option, sachez qu'il n'est pas possible d'envoyer un message plus d'une fois au même destinataire. Si un destinataire a déjà reçu le message, ce dernier ne lui sera plus envoyé. 
    
  - **Diffuser le message aux destinataires spécifiés** Sélectionnez les destinataires auprès desquels vous voulez diffuser le message. Étant donné qu'un message ne peut être envoyé qu'une seule fois à chaque destinataire, seuls les destinataires auxquels il peut être envoyé figurent dans la liste. Vous pouvez sélectionner plusieurs destinataires. Une fois votre sélection faite, cliquez sur **Ajouter**.
    
4. Cliquez sur **Libérer**. 
    
Si vous cliquez sur l'icône **Actualiser**![Icône Actualiser](media/ITPro-EAC-RefreshIcon.png) pour actualiser vos données, puis que vous double-cliquez sur le message, vous devriez voir que celui-ci a été libéré et envoyé aux destinataires appropriés 
  
### <a name="release-one-or-more-quarantined-messages-to-all-recipients"></a>Diffuser un ou plusieurs messages en quarantaine à tous les destinataires
<a name="Releaseoneormorequarantinedmessagestoallrecipients"> </a>

1. Dans le CAE, accédez à **Protection** \> **Quarantaine**.
    
2. Cliquez sur un message pour le sélectionner, ou utilisez la touche MAJ pour sélectionner plusieurs messages. Cliquez sur l'icône **Diffuser le message**. 
    
3. Cliquez sur **Diffuser les messages sélectionnés à TOUS les destinataires** dans la liste déroulante. 
    
4. La boîte de dialogue d'avertissement s'ouvre. Lisez l'avertissement et sélectionnez **Oui**si vous souhaitez continuer. Si vous sélectionnez cette option, sachez qu'il n'est pas possible d'envoyer un message plus d'une fois au même destinataire. Si un destinataire a déjà reçu le message, ce dernier ne lui sera plus envoyé. 
    
### <a name="release-one-or-more-quarantined-messages-to-all-recipients-and-report-false-positives"></a>Diffuser un ou plusieurs messages en quarantaine à tous les destinataires et signaler les faux positifs
<a name="Releaseoneormorequarantinedmessagestoallrecipientsandreportfalsepositives"> </a>

1. Dans le CAE, accédez à **Protection** \> **Quarantaine**.
    
2. Cliquez sur un message pour le sélectionner, ou utilisez la touche MAJ pour sélectionner plusieurs messages. Cliquez sur l'icône **Diffuser le message**. 
    
3. Cliquez sur **Diffuser les messages sélectionnés et les signaler comme faux positifs** dans la liste déroulante. 
    
4. La boîte de dialogue d'avertissement s'ouvre. Lisez l'avertissement et sélectionnez **Oui**si vous souhaitez continuer. Si vous sélectionnez cette option, sachez qu'il n'est pas possible d'envoyer un message plus d'une fois au même destinataire. Si un destinataire a déjà reçu le message, ce dernier ne lui sera plus envoyé. 
    
     Si vous sélectionnez cette option, le message est envoyé à tous les destinataires qui ne l'ont pas encore reçu. S'il s'agit d'un message mis en quarantaine car identifié comme un courrier indésirable, il sera également signalé à l'équipe d'analyse du courrier indésirable de Microsoft, qui l'évaluera et l'analysera. Selon les résultats de l'analyse, les règles de filtrage de contenu de courrier indésirable peuvent être ajustées pour autoriser le message. 
    
> [!TIP]
> Assurez-vous que le message n'est pas marqué comme courrier indésirable en suivant les étapes de la rubrique [Comment s'assurer qu'un message n'est pas marqué comme courrier indésirable](how-to-help-ensure-that-a-message-isn-t-marked-as-spam.md). 
  
Si vous cliquez sur l'icône **Actualiser**![Icône Actualiser](media/ITPro-EAC-RefreshIcon.png) pour actualiser vos données, puis que vous double-cliquez sur le message, vous devriez voir que celui-ci a été libéré et envoyé aux destinataires appropriés 
  
## <a name="for-more-information"></a>Pour plus d'informations
<a name="sectionSection4"> </a>

[FAQ sur la mise en quarantaine](quarantine-faq.md)
  

