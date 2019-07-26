---
title: Configuration de vos stratégies de filtrage du courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/05/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 316544cb-db1d-4c25-a5b9-c73bbcf53047
ms.collection:
- M365-security-compliance
description: Les paramètres du filtre de courrier indésirable de base incluent la sélection de l’action à effectuer sur les messages identifiés comme indésirables.
ms.openlocfilehash: e06714e4a27601c7606c580551217155688a6169
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854658"
---
# <a name="configure-your-spam-filter-policies"></a>Configuration de vos stratégies de filtrage du courrier indésirable
Les paramètres du filtre de courrier indésirable incluent la sélection de l’action à effectuer sur les messages identifiés comme indésirables. Les paramètres de la stratégie de filtrage de courrier indésirable sont appliqués uniquement aux messages entrants et sont de deux sortes :

  - Par défaut : la stratégie de filtrage du courrier indésirable par défaut est utilisée pour configurer les paramètres de filtrage du courrier indésirable dans l’organisation. Cette stratégie ne peut pas être renommée et est toujours activée.

  - Personnalisé : les stratégies personnalisées de filtrage de courrier indésirable peuvent être précises et appliquées à des utilisateurs, des groupes ou des domaines spécifiques au sein de votre organisation. Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez modifier l’ordre d’exécution de vos stratégies personnalisées en modifiant la priorité de chaque stratégie personnalisée. Toutefois, seule la stratégie priorité la plus élevée (par exemple, chiffre le plus proche de 0) s’applique si plusieurs stratégies remplissent les critères définis.

## <a name="what-you-must-know-before-you-begin"></a>À savoir avant de commencer

Durée d'exécution estimée : 30 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Anti-spam » dans la rubrique [Autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx).

Les paramètres de stratégie de filtrage du courrier indésirable se trouvent dans le centre de sécurité & conformité (SCC). Pour plus d’informations, voir [Aller au Centre de sécurité et conformité Office 365 aux utilisateurs](go-to-the-securitycompliance-center.md). La page des paramètres anti-courrier indésirable se trouve dans la section \> **anti-courrier indésirable de la stratégie** \> ** de gestion ** \> **des menaces SCC.

## <a name="access-and-create-spam-filter-policies"></a>Accéder aux stratégies de filtrage d’accès et de création de courrier indésirable

Dans la page Paramètres anti-courrier indésirable, les paramètres par défaut peuvent être affichés sous l’onglet standard. Pour modifier ces paramètres, accédez à l'onglet**personnalisé**. Vous pourrez voir et configurer certains des paramètres par défaut dans la stratégie de filtrage du courrier indésirable par défaut.

Pour activer des paramètres plus personnalisés ou ajouter des stratégies personnalisées, définissez le sélecteur paramètres personnalisés sur **activé pour activer les stratégies personnalisées de filtrage de courrier indésirable. Vous pouvez afficher les stratégies personnalisées existantes en les développant à partir de cet emplacement.

## <a name="configure-custom-spam-filter-policy-settings"></a>Configurer les paramètres de stratégie de filtrage de courrier indésirable personnalisés

1. Sélectionnez, puis cliquez sur**modifier la stratégie** si vous modifiez une stratégie, sinon, cliquez sur**créer une stratégie**

2. Vous pouvez spécifier un nom unique pour les stratégies personnalisées, mais vous ne pouvez pas renommer celui défini par défaut. Vous pouvez autrement spécifier une description plus détaillée.

3. Sous la section **actions de courrier indésirable et en bloc** :

  - Sélectionnez une action pour le **courrier indésirable**, **le courrier indésirable à haute fiabilité**, les** messages hameçons ** et les types d’**e-mails en bloc**. Les valeurs disponibles sont : 

    - **Déplacer le message dans le dossier Courrier indésirable** Envoie le message au dossier Courrier indésirable des destinataires spécifiés. Il s’agit de l’action par défaut pour le courrier indésirable, le courrier indésirable hautement fiable et le bloc.<br/><br/>

    > [!NOTE]
    > Afin que cette action fonctionne sur des boîtes aux lettres locales, vous devez configurer deux règles de flux mail Exchange (règles de transport) sur vos serveurs locaux de manière à détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, voir [Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). Cette étape est importante pour les clients d'Exchange Online Protection (EOP) autonome uniquement.

    - **Ajouter un en-tête X**: Envoie le message aux destinataires spécifiés, mais y ajoute le texte d'en-tête X l'identifiant comme courrier indésirable pour identifier le message comme indésirable. En vous basant sur ce texte comme identificateur, vous pouvez éventuellement créer des règles de boîte de réception ou utiliser un appareil en aval pour agir sur le message. Le texte d’en-tête X par défaut est **Ce message semble être un courrier indésirable**.<br/>Vous pouvez personnaliser le texte d'en-tête X avec la zone de texte **Ajouter ce texte d'en-tête X**. Si vous personnalisez le texte d'en-tête X, prenez en compte les conditions suivantes : 
    
      - Si vous indiquez uniquement l’en-tête au format \< *en-tête*  \>, dans lequel il n’y a aucun espace dans l’\<  *en-tête*  \>, le signe deux-points sera ajouté à la fin du texte personnalisé, suivi du texte par défaut. Par exemple, si vous indiquez « Voici mon en-tête personnalisé », le texte de l’en-tête X s’affichera comme ceci : « Voici mon en-tête personnalisé : ce message semble être un courrier indésirable. » 
        
      - Si vous insérez des espaces dans le texte d'en-tête personnalisé ou si vous ajoutez les deux-points vous-même, par exemple « Voici mon en-tête personnalisé » ou « Voici-mon-en-tête-personnalisé », le texte d'en-tête X revient à la valeur par défaut « Ce-message-est-un-courrier-indésirable : ce message semble être un courrier indésirable. »
    
      - Vous ne pouvez pas indiquer le texte d’en-tête au format\< *en-tête*  \>:\<  *valeur*  \>. Si vous le faites, les valeurs précédant et suivant le signe deux-points sont ignorées et le texte d'en-tête X par défaut apparaît à la place : « Ce message est un courrier indésirable : ce message semble être un courrier indésirable. » 
      
      - Notez que les messages avec cet en-tête X peuvent être déplacés vers le dossier courrier indésirable de la boîte aux lettres en raison de la configuration de la boîte aux lettres indésirable. Vous pouvez modifier cette option en désactivant cette fonctionnalité avec l’option Set-MailboxJunkEmailConfiguration.

    - **Ajouter un texte au début de la ligne d'objet** Envoie le message à ses destinataires après avoir ajouté au début de la ligne d'objet le texte spécifié dans la zone d'entrée **Préfixer la ligne d'objet avec ce texte**. Si vous utilisez ce texte en tant qu'identificateur, vous pouvez créer des règles pour filtrer ou router les messages selon vos besoins. 

    - **Rediriger le message vers une adresse e-mail**: Envoie le message à une adresse e-mail spécifiée au lieu des destinataires prévus. Spécifiez l'adresse de redirection dans la zone d'entrée **Rediriger vers cette adresse de messagerie**.

    - **Supprimer le message**: Supprime le message entier, pièces jointes comprises. 
        
    - **Mettre en quarantaine le message**: Envoie le message en quarantaine au lieu de le remettre à ses destinataires. Il s’agit de l’action par défaut pour les hameçons. Si vous sélectionnez cette option, dans la zone d'entrée **Conserver les courriers indésirables pendant (jours)**, spécifiez le nombre de jours pendant lesquels le courrier indésirable restera en quarantaine. (Il sera automatiquement supprimé à l'issue de cette période. La valeur par défaut est 30 jours, ce qui est également la valeur maximale. La valeur minimale est 1 jour.)<br/><br/>Conseil : Pour plus d'informations sur la manière dont les administrateurs peuvent gérer les messages électroniques mis en quarantaine dans le CAE, consultez les rubriques [Mise en quarantaine](quarantine.md) et [Rechercher et débloquer les messages mis en quarantaine en tant qu'administrateur](find-and-release-quarantined-messages-as-an-administrator.md). > Pour plus d’informations sur la configuration des messages de notification de courrier indésirable à envoyer aux utilisateurs, voir [Configurer des notifications de courrier indésirable pour l’utilisateur final dans EOP](configure-end-user-spam-notifications-in-eop.md) ou [configurer des notifications de courrier indésirable pour l’utilisateur final dans Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 

  - Configurer **sélectionnez le seuil** pour déterminer la façon dont vous voulez traiter les courriers électroniques en bloc comme du courrier indésirable, en fonction du niveau de réclamation en bloc (BCL) du message. Vous pouvez choisir un paramètre de seuil compris allant de 1 et 9, où 1 marque la plupart des messages électroniques en nombre en tant que courrier indésirable, et 9 autorise la remise de la plupart des messages électroniques en nombre. Le service effectue ensuite l’action configurée, comme par exemple l’envoi du message dans le dossier Courrier indésirable du destinataire. Pour plus de détails, consultez [Valeurs BCL](bulk-complaint-level-values.md) et [Quelle est la différence entre courrier indésirable et message électronique en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md). 

4. Dans la page de**propriétés du courrier indésirable**, vous pouvez configurer les options de mode de test pour la stratégie en configurant les éléments suivants : 
    
      - **Aucune** Aucune action en mode test n'est appliquée au message. Valeur par défaut. 
        
      - **Ajouter le texte d’en-tête X de test par défaut** L’activation de cette option a pour effet d’envoyer le message à ses destinataires après y avoir ajouté un en-tête X spécial l’identifiant comme ayant rencontré une option spécifique de filtrage avancé du courrier indésirable.  
        
      - **Envoyer un message Cci à cette adresse** L’activation de cette option a pour effet d’envoyer une copie carbone invisible du message à l’adresse de courrier que vous spécifiez dans cette zone d’entrée.  <br/><br/>Pour plus d'informations sur les options avancées de filtrage avancé du courrier indésirable, y compris sur les descriptions de chaque option et du texte d'en-tête X associé à chaque option, voir [Options de filtrage avancé du courrier indésirable](advanced-spam-filtering-asf-options.md).

5. Pour les stratégies personnalisées uniquement, cliquez sur l'option de menu **Appliquer à**, puis créez un règle basée sur une condition pour spécifier les utilisateurs, groupes ou domaines auxquels cette stratégie s'applique. Vous pouvez créer plusieurs conditions pour autant qu'elles soient uniques. 
    
      - Pour sélectionner des utilisateurs, cliquez sur **Le destinataire est**. Dans la boîte de dialogue suivante, sélectionnez un ou plusieurs expéditeurs de votre organisation dans la liste du sélecteur, puis cliquez sur **Ajouter**. Pour ajouter des expéditeurs ne figurant pas dans la liste, entrez leurs adresses de messagerie, puis cliquez sur **Vérifier les noms**. Dans ce champ, vous pouvez également entrer des caractères génériques pour sélectionner plusieurs adresses de messagerie (par exemple : \*@ _domainname_). Une fois les sélections effectuées, cliquez sur **OK** pour revenir à l'écran principal. 
        
      - Pour sélectionner des groupes, sélectionnez**le destinataire est membre de**. Ensuite, dans la boîte de dialogue suivante, sélectionnez ou spécifiez les groupes. Cliquez sur **ok** pour revenir à l'écran principal. 
        
      - Pour sélectionner des domaines, sélectionnez le **domaine du destinataire est**. Ensuite, dans la boîte de dialogue suivante, ajoutez les domaines. Cliquez sur **ok** pour revenir à l'écran principal. <br/><br/>Vous pouvez créer des exceptions dans la règle. Par exemple, pour filtrer les messages de tous les domaines, sauf un domaine particulier. Cliquez sur **Ajouter une exception**, puis créez vos conditions d'exception de la même manière que vous avez créé les autres conditions.<br/><br/>L’application d’une stratégie de courrier indésirable à un groupe est prise en charge uniquement pour les **groupes de sécurité à extension messagerie**. 
  
6. Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie s'affiche dans le volet droit.

La stratégie par défaut ne peut pas être désactivée ou supprimée et les stratégies personnalisées ont toujours priorité sur la stratégie par défaut. Pour les stratégies personnalisées, vous pouvez cocher ou décocher des cases dans la colonne **ACTIVÉ** afin de les activer ou désactiver. Par défaut, toutes les stratégies sont activées. Pour supprimer une stratégie personnalisée, sélectionnez-la, cliquez sur l'![Icône Supprimer](media/ITPro-EAC-DeleteIcon.gif)**Supprimer**, puis confirmez sa suppression.

> [!TIP]
> Vous pouvez modifier leur priorité (ordre d'exécution) en cliquant sur les flèches haut![Icône flèche vers le haut](media/ITPro-EAC-UpArrowIcon.gif) et bas![Icône de flèche vers le bas](media/ITPro-EAC-DownArrowIcon.gif). La stratégie dont la **PRIORITÉ** est **0** s’exécute d’abord, suivie des stratégies dont l’ordre de priorité est **1**, **2**, etc. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Utilisation de PowerShell à distance pour configurer les stratégies de filtrage du courrier indésirable

Vous pouvez également configurer et appliquer des stratégies de filtrage du contenu indésirable dans PowerShell. Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554). Pour apprendre à utiliser Windows PowerShell afin d’établir une connexion à Exchange Online Protection, voir [Connexion à Exchange Online Protection à l’aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).
  
- [Get-HostedContentFilterPolicy](http://technet.microsoft.com/library/d510471a-dda5-4df7-b3f8-2ee7a1948436.aspx) Afficher vos paramètres de filtrage du courrier indésirable. 
    
- [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) Modifier vos paramètres de filtrage du courrier indésirable. 
    
- [New-HostedContentFilterPolicy](http://technet.microsoft.com/library/4d15128d-9e16-42a1-8ac5-36f07d4bbbf0.aspx) Créer une stratégie de filtrage du courrier indésirable personnalisée. 
    
- [Remove-HostedContentFilterPolicy](http://technet.microsoft.com/library/9fe1fe03-8f83-41e3-9bf5-084a392784d6.aspx) Supprimer une stratégie de filtrage du courrier indésirable personnalisée. 
    
Pour appliquer une stratégie de filtrage du courrier indésirable personnalisée à des utilisateurs, à des groupes et/ou à des domaines, utilisez la cmdlet [New-HostedContentFilterRule](http://technet.microsoft.com/library/2df13ba9-1eb0-4da3-bd72-a79d5fa15e26.aspx) (pour créer une règle de filtrage pouvant être appliquée aux stratégies personnalisées) ou la cmdlet [Set-HostedContentFilterRule](http://technet.microsoft.com/library/ba259260-ffd3-43f3-8ef4-9d8659679d02.aspx) (pour modifier une règle de filtrage existante pouvant être appliquée aux stratégies personnalisées). Utilisez les cmdlets [Enable-HostedContentFilterRule](http://technet.microsoft.com/library/354ece28-dcde-4b5f-88ed-475115e7ea78.aspx) ou [Disable-HostedContentFilterRule](http://technet.microsoft.com/library/c1f8dafc-ef5d-47e3-b0fb-71a88e145fc5.aspx) pour activer ou désactiver la règle appliquée à la stratégie. 
  
## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vous assurer que le courrier indésirable est correctement détecté et traité, vous pouvez envoyer un message GTUBE via le service. Comme le fichier test d’antivirus EICAR, le message GTUBE teste le service pour vérifier qu’il détecte le courrier indésirable entrant. Un message GTUBE doit toujours être détecté comme courrier indésirable par le filtre de courrier indésirable, et les actions appliquées au message doivent correspondre aux paramètres que vous avez configurés.
  
Incluez le texte GTUBE suivant dans une ligne d'un message électronique, sans espaces ni sauts de ligne :
  
```
XJS*C4JDBQADN1.NSBN3*2IDNEN*GTUBE-STANDARD-ANTI-UBE-TEST-EMAIL*C.34X
```

## <a name="fine-tuning-your-spam-filter-policy-to-prevent-false-positives-and-false-negatives"></a>Optimisation de votre stratégie de filtrage de courrier indésirable pour éviter les faux positifs et les faux négatifs

Vous pouvez activer des techniques de filtrage avancé du courrier indésirable si vous souhaitez adopter une approche plus agressive du filtrage du courrier indésirable. Pour plus d'informations sur les paramètres de courrier indésirable généraux applicables à l'ensemble de l'organisation, consultez les rubriques relatives aux procédures visant à [empêcher que des courriers électroniques faux positifs soient marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkId=534224) et à [bloquer du courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](reduce-spam-email.md). Elles sont utiles si vous disposez d’un contrôle de niveau administrateur et que vous souhaitez éviter les faux positifs ou les faux négatifs.

## <a name="allowblock-lists"></a>Listes autorisé/bloqué

Dans certains cas, nos filtres ne recevront pas le message ou l’accès à nos systèmes prend du temps. Dans ce cas, la stratégie anti-courrier indésirable dispose d’une liste Autoriser et d’une liste de blocage disponible pour remplacer le verdict actuel. Cette option doit être utilisée avec modération uniquement dans la mesure où les listes peuvent être ingérables et temporaires dans la mesure où la pile de filtrage doit faire ce qu’elles sont censées faire.

Les listes verte et rouge sont configurées dans le cadre de la stratégie anti-courrier indésirable du client :

1. Dans la section **Listes vertes**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours remises dans la boîte de réception. Le courrier électronique provenant de ces entrées n’est pas traité par le filtre de courrier indésirable. 
    
      - Ajoutez des expéditeurs approuvés à la liste des expéditeurs autorisés. Cliquez sur **Modifier**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les adresses des expéditeurs à autoriser dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l’aide d’un point-virgule ou d’un retour à la ligne. Cliquez sur **Enregistrer** pour revenir à la page **Listes vertes**. 
        
      - Ajoutez des domaines approuvés à la liste de domaines autorisés. Cliquez sur **Modifier**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les domaines à autoriser dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l’aide d’un point-virgule ou d’un retour à la ligne. Cliquez sur **Enregistrer** pour revenir à la page **Listes vertes**. 

> [!CAUTION]
> Vous ne devez jamais répertorier les domaines acceptés (domaines qui vous appartiennent) ou les domaines communs tels que Microsoft.com, office.com, etc. à une liste verte. Cela permettrait aux usurpateurs d’envoyer des courriers non restreints à votre organisation.

2. Dans la page **Listes rouges**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours marquées comme courrier indésirable. Le service applique l’action configurée de courrier indésirable à probabilité élevée sur le courrier électronique correspondant à ces entrées. 
    
      - Ajoutez des expéditeurs indésirables à la liste de blocage des expéditeurs. Cliquez sur **Modifier**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les adresses des expéditeurs à bloquer dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l’aide d’un point-virgule ou d’un retour à la ligne. Cliquez sur **OK** pour revenir à la page **Listes rouges**. 
        
      - Ajoutez des domaines indésirables à la liste des domaines bloqués. Cliquez sur **Modifier**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les domaines à bloquer dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l’aide d’un point-virgule ou d’un retour à la ligne. Cliquez sur **OK** pour revenir à la page **Listes rouges**.

> [!TIP]
>  Dans certains cas, il est possible que votre organisation n’accepte pas le verdict fourni par le service. Dans ce cas, vous souhaiterez peut-être conserver le contenu permanent de la liste verte ou rouge. Toutefois, si vous comptez placer un domaine sur la liste verte pendant une période prolongée, demandez à l’expéditeur de vérifier que le domaine est authentifié et qu’il est paramétré sur DMARC refuser si ce n’est pas le cas.

## <a name="for-more-information"></a>Pour plus d'informations
<a name="sectionSection6"> </a>

[Configuration de votre domaine pour DMARC](use-dmarc-to-validate-email.md)
  
[Mise en quarantaine](quarantine.md)
  
[Empêcher le marquage des faux positifs comme courrier indésirable à l’aide d’une liste fiable ou d’autres techniques](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquer le courrier indésirable à l’aide du filtre d’Office 365 afin d’éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225)

[Seuils de probabilité de courrier indésirable](spam-confidence-levels.md)
  

