---
title: Configuration de vos stratégies de filtrage du courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 316544cb-db1d-4c25-a5b9-c73bbcf53047
ms.collection:
- M365-security-compliance
description: Les paramètres de filtrage du courrier indésirable de base incluent la sélection de l’action à effectuer sur les messages identifiés comme courrier indésirable.
ms.openlocfilehash: be99c017a5038fbfb431edbcf2d65c877d92388c
ms.sourcegitcommit: 5a93c2f3df35d06a59a7fbaff5c91f7afde11781
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2019
ms.locfileid: "34857654"
---
# <a name="configure-your-spam-filter-policies"></a>Configuration de vos stratégies de filtrage du courrier indésirable
Les paramètres de filtrage du courrier indésirable incluent la sélection de l’action à effectuer sur les messages identifiés comme courrier indésirable. Les paramètres de stratégie de filtrage du courrier indésirable sont appliqués aux messages entrants uniquement et il existe deux types:

  - Valeur par défaut: la stratégie de filtrage du courrier indésirable par défaut est utilisée pour configurer les paramètres de filtrage du courrier indésirable dans l’entreprise Cette stratégie ne peut pas être renommée et est toujours active.

  - Personnalisé: les stratégies personnalisées de filtrage du courrier indésirable peuvent être granulaires et appliquées à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation. Les stratégies personnalisées priment toujours sur la stratégie par défaut. Vous pouvez modifier l’ordre dans lequel vos stratégies personnalisées s’exécutent en modifiant la priorité de chaque stratégie personnalisée; Toutefois, seule la stratégie dont la priorité est la plus élevée (par exemple, le nombre le plus proche de 0) s’applique si plusieurs stratégies répondent aux critères définis.

## <a name="what-you-must-know-before-you-begin"></a>Ce que vous devez savoir avant de commencer

Durée d'exécution estimée : 30 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l’entrée blocage du courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .

Les paramètres de stratégie de filtrage du courrier indésirable sont tous dans le centre de sécurité & conformité (SCC). Pour plus d’informations, [consultez le centre de conformité Office 365 Security &](go-to-the-securitycompliance-center.md). La page des paramètres de blocage du courrier indésirable se trouve dans la section **anti-spam** de la **stratégie** \> de **gestion** \> des menaces SCC \> .

## <a name="access-and-create-spam-filter-policies"></a>Accès et création de stratégies de filtrage du courrier indésirable

Dans la page Paramètres de blocage du courrier indésirable, les paramètres par défaut peuvent être affichés sous l’onglet standard. Pour modifier ces paramètres, accédez à l’onglet **personnalisé** . Vous pourrez voir et configurer certains des paramètres par défaut dans la stratégie de filtrage du courrier indésirable par défaut.

Pour activer des paramètres plus personnalisés ou ajouter des stratégies personnalisées, définissez le sélecteur de **paramètres personnalisés** sur **activé** pour activer les stratégies personnalisées de filtrage du courrier indésirable. Vous pouvez afficher les stratégies personnalisées existantes en les développant à partir d’ici.

## <a name="configure-custom-spam-filter-policy-settings"></a>Configurer les paramètres de stratégie de filtrage du courrier indésirable

1. Sélectionnez et cliquez sur **modifier la stratégie** si vous modifiez une stratégie; dans le cas contraire, cliquez sur **créer une stratégie** .

2. Vous pouvez spécifier un nom unique pour les stratégies personnalisées, mais vous ne pouvez pas renommer la stratégie par défaut. Vous pouvez également spécifier une description plus détaillée pour n’importe quelle stratégie.

3. Dans la section **actions de courrier indésirable et en bloc** :

  - Sélectionnez une action pour le **** courrier indésirable, le courrier indésirable à **fiabilité élevée**, le **courrier électronique de hameçonnage**et les types de **messages électroniques en nombre** . Les valeurs disponibles sont : 

    - **Déplacer le message vers le dossier** courrier indésirable: Envoie le message au dossier courrier indésirable des destinataires spécifiés. Il s’agit de l’action par défaut pour le courrier indésirable, le courrier indésirable à fiabilité élevée et l’encombrement.<br/><br/>

    > [!NOTE]
    > Pour que cette action fonctionne avec les boîtes aux lettres locales, vous devez configurer deux règles de flux de messagerie Exchange (également appelées règles de transport) sur vos serveurs locaux pour détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d’informations, consultez la rubrique How to [s’assure que le courrier indésirable est acheminé vers le dossier de courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). Cette étape est essentielle pour les clients autonomes Exchange Online Protection (EOP).

    - **Ajouter un en-tête X:** Envoie le message aux destinataires spécifiés, mais ajoute un texte d’en-tête X à l’en-tête du message afin d’identifier le message en tant que courrier indésirable. En utilisant ce texte comme identificateur, vous pouvez éventuellement créer des règles de boîte de réception ou utiliser un appareil en aval pour agir sur le message. Le texte d'en-tête X par défaut est **Ce message semble être un courrier indésirable**.<br/>Vous pouvez personnaliser le texte d’en-tête X à l’aide de la zone de **texte ajouter ce texte d’en-tête x** . Si vous personnalisez le texte d’en-tête X, gardez à l’esprit les conditions suivantes: 
    
      - Si vous spécifiez uniquement l’en-tête \< dans l' *en-tête*\>de format, où \<il n’y a pas d’espaces dans l' *en-*\>tête, un signe deux-points est ajouté au texte personnalisé, suivi du texte par défaut.       Par exemple, si vous spécifiez «This-is-My-Custom-Header», le texte de l’en-tête X s’affiche sous la forme «This-is-My-Custom-header: ce message semble être un courrier indésirable». 
        
      - Si vous incluez des espaces dans le texte d’en-tête personnalisé ou si vous ajoutez le signe deux-points vous-même (par exemple, «X il s’agit de mon en-tête personnalisé» ou «X-This-is-My-Custom-header:»), le texte de l’en-tête X reprend sa valeur par défaut, «X-This
    
      - Vous ne pouvez pas spécifier le texte d’en \< -tête dans l' *en-tête*  \>format:\<  *value*  \>. Dans ce cas, les deux valeurs précédant et suivant le signe deux-points sont ignorées et le texte par défaut de l’en-tête X apparaît: «X-ce-is-courrier indésirable: ce message semble être un courrier indésirable». 
      
      - Sachez que les messages avec cet en-tête X peuvent toujours être déplacés vers le dossier courrier indésirable de la boîte aux lettres en raison de la configuration indésirable des boîtes aux lettres Vous pouvez modifier ce paramètre en désactivant cette fonctionnalité à l’aide de Set-MailboxJunkEmailConfiguration.

    - **Ajouter une ligne d’objet avec du texte:** Envoie le message aux destinataires voulus, mais ajoute à la ligne d’objet le texte que vous spécifiez dans la **ligne d’objet du préfixe avec cette** zone d’entrée de texte. En utilisant ce texte comme identificateur, vous pouvez éventuellement créer des règles pour filtrer ou acheminer les messages selon vos besoins. 

    - **Rediriger le message vers l’adresse de messagerie:** Envoie le message à une adresse de messagerie désignée plutôt qu’aux destinataires prévus. Spécifiez l'adresse de redirection dans la zone d'entrée **Rediriger vers cette adresse e-mail**.

    - **Message de suppression:** Supprime l’intégralité du message, y compris toutes les pièces jointes. 
        
    - **Message de mise en quarantaine:** Envoie le message en quarantaine au lieu de l’envoyer aux destinataires prévus. Il s’agit de l’action par défaut pour le hameçonnage. Si vous sélectionnez cette option, dans la zone d'entrée **Conserver les courriers indésirables pendant (jours)**, spécifiez le nombre de jours pendant lesquels le courrier indésirable restera en quarantaine. (Il sera automatiquement supprimé à l'issue de cette période. La valeur par défaut est de 30 jours, c’est-à-dire la valeur maximale. La valeur minimale est 1 jour.)<br/><br/>Conseil: pour plus d’informations sur la façon dont les administrateurs peuvent gérer les messages électroniques qui se trouvent en quarantaine dans le centre d’administration Exchange, consultez la rubrique [mise en quarantaine](quarantine.md) et [Rechercher et débloquer les messages mis en quarantaine en tant qu’administrateur](find-and-release-quarantined-messages-as-an-administrator.md). > pour plus d’informations sur la façon de configurer les messages de notification de courrier indésirable à envoyer aux utilisateurs, consultez la rubrique [configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md) ou configure [End-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 

  - Configurer: **sélectionnez le seuil** pour déterminer la manière dont vous souhaitez traiter les messages électroniques en masse en tant que courrier indésirable, en fonction du niveau de réclamation en masse (BCL) du message. Vous pouvez choisir un paramètre de seuil compris entre 1 et 9, où 1 indique la plupart des messages électroniques en nombre comme du courrier indésirable et 9 la plupart des messages électroniques en nombre. Le service effectue ensuite l'action configurée, comme par exemple l'envoi du message dans le dossier Courrier indésirable du destinataire. Consultez la rubrique [valeurs de niveau de réclamation en bloc](bulk-complaint-level-values.md) et [quelle est la différence entre courrier indésirable et courrier électronique en masse?](what-s-the-difference-between-junk-email-and-bulk-email.md) pour plus d’informations. 

4. Sur la page **Propriétés du courrier** indésirable, vous pouvez définir les options de mode test pour la stratégie en configurant les éléments suivants: 
    
      - **Aucune** Aucune action en mode test n'est appliquée au message. Il s'agit du paramétrage par défaut. 
        
      - **Ajouter le texte d’en-tête X de test par défaut** La sélection de cette option envoie le message aux destinataires spécifiés, mais ajoute également un en-tête X spécial au message pour l’identifier comme ayant correspondu à une option de filtrage avancé du courrier indésirable spécifique. 
        
      - **Envoyer un message CCI à cette adresse** La sélection de cette option envoie une copie carbone invisible du message à l’adresse de messagerie que vous spécifiez dans la zone d’entrée. <br/><br/>Pour plus d’informations sur les options de filtrage avancé du courrier indésirable, notamment des descriptions de chaque option et du texte d’en-tête X associé à chacun d’eux, voir [Options avancées de filtrage du courrier](advanced-spam-filtering-asf-options.md)indésirable.

5. Pour les stratégies personnalisées uniquement, cliquez sur l’élément **de menu appliquer à** , puis créez une règle basée sur une condition pour spécifier les utilisateurs, les groupes et les domaines auxquels cette stratégie doit être appliquée. Vous pouvez créer plusieurs conditions, si elles sont uniques. 
    
      - Pour sélectionner des utilisateurs, cliquez sur **Le destinataire est**. Dans la boîte de dialogue suivante, sélectionnez un ou plusieurs expéditeurs de votre entreprise dans la liste sélecteur d’utilisateur, puis cliquez sur **Ajouter**. Pour ajouter des expéditeurs qui ne figurent pas dans la liste, entrez leurs adresses de messagerie, puis cliquez sur **vérifier les noms**. Dans ce champ, vous pouvez également entrer des caractères génériques pour sélectionner plusieurs adresses de messagerie (par exemple : \*@ _domainname_). Lorsque vous avez terminé vos sélections, cliquez sur **OK** pour revenir à l’écran principal. 
        
      - Pour sélectionner des groupes, sélectionnez **le destinataire est membre de**. Ensuite, dans la boîte de dialogue suivante, sélectionnez ou spécifiez les groupes. Cliquez sur **OK** pour revenir à l'écran principal. 
        
      - Pour sélectionner des domaines, sélectionnez **le domaine du destinataire est**. Ensuite, dans la boîte de dialogue suivante, ajoutez les domaines. Cliquez sur **OK** pour revenir à l'écran principal. <br/><br/>Vous pouvez créer des exceptions au sein de la règle. Par exemple, vous pouvez filtrer les messages de tous les domaines à l’exception d’un domaine donné. Cliquez sur **Ajouter une exception**, puis créez vos conditions d’exception de la même manière que vous avez créé les autres conditions.<br/><br/>L’application d’une stratégie de courrier indésirable à un groupe est prise en charge uniquement pour les **groupes de sécurité à extension messagerie**. 
  
6. Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie s'affiche dans le volet droit.

La stratégie par défaut ne peut pas être désactivée ou supprimée et les stratégies personnalisées ont toujours priorité sur la stratégie par défaut. Pour les stratégies personnalisées, vous pouvez activer ou désactiver les cases à cocher dans la colonne **activé** pour les activer ou les désactiver. Par défaut, toutes les stratégies sont activées. Pour supprimer une stratégie personnalisée, sélectionnez-la, cliquez sur ![l’icône](media/ITPro-EAC-DeleteIcon.gif) **** de suppression de l’icône de suppression, puis confirmez la suppression de la stratégie.

> [!TIP]
> Vous pouvez modifier la priorité (ordre en cours) de vos stratégies personnalisées en ![cliquant sur l'](media/ITPro-EAC-UpArrowIcon.gif) icône de flèche ![vers le haut](media/ITPro-EAC-DownArrowIcon.gif) et la flèche vers le bas. La stratégie dont la **priorité** est **0** s’exécute en premier, suivie de **1**, puis de **2**, et ainsi de suite. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Utilisation de PowerShell à distance pour configurer les stratégies de filtrage du courrier indésirable

Vous pouvez également configurer et appliquer des stratégies de filtrage du contenu indésirable dans PowerShell. Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554). Pour apprendre à utiliser Windows PowerShell afin de vous connecter à Exchange Online Protection, consultez la rubrique [Connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).
  
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

Vous pouvez activer les techniques avancées de filtrage du courrier indésirable si vous souhaitez adopter une approche plus agressive pour le filtrage du courrier indésirable. Pour plus d'informations sur les paramètres de courrier indésirable généraux applicables à l'ensemble de l'organisation, consultez les rubriques relatives aux procédures visant à [empêcher que des courriers électroniques faux positifs soient marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkId=534224) et à [bloquer du courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](reduce-spam-email.md). Elles sont utiles si vous disposez d'un contrôle de niveau administrateur et que vous souhaitez éviter les faux positifs ou les faux négatifs.

## <a name="allowblock-lists"></a>Listes verte/rouge

Il arrivera que nos filtres manquent le message ou que nos systèmes prennent du temps pour y accéder. Dans ce cas, la stratégie de blocage du courrier indésirable dispose d’une liste verte et d’une liste rouge permettant de remplacer le verdict en cours. Cette option ne doit être utilisée avec parcimonie que car les listes peuvent devenir ingérables et temporairement, car notre pile de filtrage doit faire ce qu’elle est censé effectuer.

Les listes verte et rouge sont toutes deux configurées dans le cadre de la stratégie de blocage du courrier indésirable du client:

1. Dans la section **autoriser les listes** , vous pouvez spécifier des entrées, telles que des expéditeurs ou des domaines, qui seront toujours remises dans la boîte de réception. Le courrier électronique provenant de ces entrées n’est pas traité par le filtre de courrier indésirable. 
    
      - Ajoutez des expéditeurs approuvés à la liste des expéditeurs autorisés. Cliquez sur **modifier**![l'](media/ITPro-EAC-AddIcon.gif)icône Ajouter, puis, dans la boîte de dialogue de sélection, ajoutez les adresses de l’expéditeur que vous souhaitez autoriser. Vous pouvez séparer les entrées à l’aide d’un point-virgule ou d’un retour à la ligne. Cliquez sur **Enregistrer** pour revenir à la page **listes vertes** . 
        
      - Ajoutez des domaines approuvés à la liste de domaines autorisés. Cliquez sur **modifier**![l'](media/ITPro-EAC-AddIcon.gif)icône Ajouter, puis, dans la boîte de dialogue de sélection, ajoutez les domaines que vous souhaitez autoriser. Vous pouvez séparer les entrées à l’aide d’un point-virgule ou d’un retour à la ligne. Cliquez sur **Enregistrer** pour revenir à la page **listes vertes** . 

> [!CAUTION]
> Vous ne devez jamais répertorier les domaines acceptés (domaines que vous possédez) ou les domaines courants tels que Microsoft.com, office.com, etc., dans une liste verte. Cela permettrait aux usurpateurs d’envoyer des courriers non restreints à votre organisation.

2. Dans la page **Listes rouges**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours marquées comme courrier indésirable. Le service applique l'action configurée de courrier indésirable à probabilité élevée sur le courrier électronique correspondant à ces entrées. 
    
      - Ajoutez des expéditeurs indésirables à la liste de blocage des expéditeurs. Cliquez sur **modifier**![l'](media/ITPro-EAC-AddIcon.gif)icône Ajouter, puis, dans la boîte de dialogue de sélection, ajoutez les adresses de l’expéditeur que vous souhaitez bloquer. Vous pouvez séparer les entrées à l’aide d’un point-virgule ou d’un retour à la ligne. Cliquez sur **Enregistrer** pour revenir à la page **listes rouges** . 
        
      - Ajoutez des domaines indésirables à la liste des domaines bloqués. Cliquez sur **modifier**![l'](media/ITPro-EAC-AddIcon.gif)icône Ajouter, puis, dans la boîte de dialogue de sélection, ajoutez les domaines que vous souhaitez bloquer. Vous pouvez séparer les entrées à l’aide d’un point-virgule ou d’un retour à la ligne. Cliquez sur **Enregistrer** pour revenir à la page **listes rouges** .

> [!TIP]
>  Il peut y avoir des situations dans lesquelles votre organisation ne peut pas accepter le verdict fourni par le service. Dans ce cas, vous souhaiterez peut-être conserver la liste autoriser ou bloquer en permanence. Toutefois, si vous envisagez de placer un domaine dans la liste verte pendant de longues périodes, vous devez indiquer à l’expéditeur de s’assurer que son domaine est authentifié et qu’il est défini sur DMARC refuser s’il ne l’est pas.

## <a name="for-more-information"></a>Pour plus d’informations
<a name="sectionSection6"> </a>

[Configuration de votre domaine pour DMARC](use-dmarc-to-validate-email.md)
  
[Mise en quarantaine](quarantine.md)
  
[Éviter les courriers électroniques faux positifs marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225)

[Seuils de probabilité de courrier indésirable](spam-confidence-levels.md)
  

