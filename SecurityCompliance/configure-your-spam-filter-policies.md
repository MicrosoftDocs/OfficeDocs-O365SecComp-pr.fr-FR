---
title: Configuration de vos stratégies de filtrage du courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 316544cb-db1d-4c25-a5b9-c73bbcf53047
ms.collection:
- M365-security-compliance
description: Les paramètres de filtrage du courrier indésirable de base incluent la sélection de l'action à effectuer sur les messages identifiés comme courrier indésirable, ainsi que le filtrage des messages rédigés dans des langues spécifiques ou envoyés à partir de pays ou régions spécifiques.
ms.openlocfilehash: 20c1e60f10b2cdf12bb2a62afa80f56904a7a3f2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216784"
---
# <a name="configure-your-spam-filter-policies"></a>Configuration de vos stratégies de filtrage du courrier indésirable
  
Les paramètres de filtrage du courrier indésirable de base incluent la sélection de l'action à effectuer sur les messages identifiés comme courrier indésirable. Les paramètres de stratégie de filtrage du courrier inDésirable sont appliqués uniquement aux messages entrants. Vous pouvez modifier la stratégie de filtrage du courrier indésirable par défaut pour configurer vos paramètres de filtrage du courrier indésirable à l'échelle de l'entreprise et créer des stratégies personnalisées de filtrage du courrier indésirable, puis les appliquer à des utilisateurs, des groupes ou des domaines spécifiques de votre organisation Les stratégies personnalisées prévalent toujours sur la stratégie par défaut. Vous pouvez modifier l'ordre dans lequel vos stratégies personnalisées s'exécutent en modifiant la priorité de chaque stratégie personnalisée; Toutefois, seule la stratégie de priorité la plus élevée s'applique si plusieurs stratégies répondent aux critères définis. 
  
> [!IMPORTANT]
> Pour les clients autonomes Exchange Online Protection (EOP): par défaut, les filtres de courrier indésirable EOP envoient des messages détectés par courrier indésirable dans le dossier de courrier inDésirable de chaque destinataire. Toutefois, pour vous assurer que l'action **déplacer le message vers le dossier** courrier indésirable fonctionne pour les boîtes aux lettres locales, vous devez configurer les règles de transport Exchange sur vos serveurs locaux pour détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, consultez [la rubrique s'assurer que le courrier indésirable est acheminé vers le dossier de courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
## <a name="what-you-must-know-before-you-begin"></a>Ce que vous devez savoir avant de commencer

Durée d'exécution estimée : 30 minutes
  
Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée blocage du courrier indésirable dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Pour obtenir des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, reportez-vous à l’article **Raccourcis clavier dans le Centre d’administration Exchange**.
  
## <a name="use-the-security--compliance-center-scc-to-configure-spam-filter-policies"></a>Utiliser le centre de sécurité & Compliance Center pour configurer des stratégies de filtrage du courrier indésirable

1. Dans le centre de sécurité & conformité (SCC), accédez à **protection contre le courrier**indésirable de la **stratégie** \> de **gestion** \> des menaces.
    
2. Effectuez l'une des opérations suivantes dans la page **paramètres du blocage du courrier** indésirable: 
    
      - Passez en revue la stratégie à l'échelle de l'entreprise par défaut sous les paramètres standard.
    
      - Cliquez sur l' **onglet personnalisé** , modifiez le sélecteur de **paramètres personnalisés** en le définissant sur **activé**, puis![cliquez sur](media/ITPro-EAC-AddIcon.gif) le bouton * * ajouter **une Creatge un** bouton de stratégie pour créer une stratégie de filtrage du courrier indésirable personnalisée pouvant être appliquée à des utilisateurs, des groupes, et les domaines de votre organisation. Vous pouvez également modifier des stratégies personnalisées existantes en double-cliquant dessus. 
    
3. Pour les stratégies personnalisées uniquement, spécifiez un nom pour cette stratégie. Vous pouvez également spécifier une description plus détaillée. Vous ne pouvez pas renommer la stratégie par défaut.<br/><br/>Remarque: lorsque vous créez une stratégie, tous les paramètres de configuration apparaissent sur un seul écran. En revanche, lorsque vous modifiez une stratégie, vous devez naviguer sur plusieurs écrans. Les paramètres sont les mêmes dans les deux cas, mais le reste de cette procédure explique comment accéder à ces paramètres lors de la modification d'une stratégie. 
  
4. Sur la page **actions à effectuer pour les messages électroniques en nombre et le courrier indésirable**, sous **Courrier indésirable** et **Courrier indésirable à niveau de confiance élevé**, sélectionnez l'action à effectuer pour les messages électroniques en nombre et le courrier indésirable entrant. Par défaut, l'option **Déplacer les messages vers le dossier Courrier indésirable** est sélectionnée. Les autres valeurs possibles sont les suivantes : 
    
      - **Supprimer le message** Supprime le message entier, pièces jointes comprises. 
        
      - **Mettre en quarantaine le message** Envoie le message en quarantaine au lieu de le remettre à ses destinataires. Si vous sélectionnez cette option, dans la zone d'entrée **Conserver les courriers indésirables pendant (jours)**, spécifiez le nombre de jours pendant lesquels le courrier indésirable restera en quarantaine. (Il sera automatiquement supprimé à l'issue de cette période. La valeur par défaut est 15 jours, ce qui est également la valeur maximale. La valeur minimale est 1 jour.)<br/><br/>Conseil: pour plus d'informations sur la façon dont les administrateurs peuvent gérer les messages électroniques qui se trouvent en quarantaine dans le centre d'administration Exchange, consultez la rubrique [mise en quarantaine](quarantine.md) et [Rechercher et débloquer les messages mis en quarantaine en tant qu'administrateur](find-and-release-quarantined-messages-as-an-administrator.md). > pour plus d'informations sur la façon de configurer les messages de notification de courrier indésirable à envoyer aux utilisateurs, consultez la rubrique [configure end-user spam notifications in EOP](configure-end-user-spam-notifications-in-eop.md) ou configure [End-user spam notifications in Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 
  
      - **Déplacer le message dans le dossier Courrier indésirable** Envoie le message au dossier Courrier indésirable des destinataires spécifiés. Il s'agit de l'action par défaut pour les deux niveaux de seuil de confiance.<br/><br/>**IMPORTANT: pour les clients Exchange Online Protection (EOP): pour que cette action fonctionne avec les boîtes aux lettres locales, vous devez configurer deux règles de transport Exchange sur vos serveurs locaux pour détecter les en-têtes de courrier indésirable ajoutés par EOP. Pour plus d'informations, consultez [la rubrique s'assurer que le courrier indésirable est acheminé vers le dossier de courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).**
  
      - **Ajouter un en-tête X** Envoie le message aux destinataires spécifiés, mais ajoute un texte d'en-tête X à l'en-tête du message afin d'identifier le message en tant que courrier indésirable. En utilisant ce texte comme identificateur, vous pouvez éventuellement créer des règles de boîte de réception ou utiliser un appareil en aval pour agir sur le message. Le texte de l'en-tête X par défaut est **ce message semble être du courrier**indésirable.<br/>Vous pouvez personnaliser le texte d'en-tête X à l'aide de la zone de **texte ajouter ce texte d'en-tête x** . Si vous personnalisez le texte d'en-tête X, gardez à l'esprit les conditions suivantes: 
    
      - Si vous spécifiez uniquement l'en-tête \< dans l' *en-tête*\>de format, où \<il n'y a pas d'espaces dans l' *en-*\>tête, un signe deux-points est ajouté au texte personnalisé, suivi du texte par défaut. Par exemple, si vous spécifiez «This-is-My-Custom-Header», le texte de l'en-tête X s'affiche sous la forme «This-is-My-Custom-header: ce message semble être un courrier indésirable».       
        
      - Si vous incluez des espaces dans le texte d'en-tête personnalisé ou si vous ajoutez le signe deux-points vous-même (par exemple, «X il s'agit de mon en-tête personnalisé» ou «X-This-is-My-Custom-header:»), le texte de l'en-tête X reprend sa valeur par défaut, «X-This
    
      - Vous ne pouvez pas spécifier le texte d'en \< -tête dans l' *en-tête*  \>format:\<  *value*  \>. Dans ce cas, les deux valeurs précédant et suivant le signe deux-points sont ignorées et le texte par défaut de l'en-tête X apparaît: «X-ce-is-courrier inDésirable: ce message semble être un courrier indésirable». 
      
      - Sachez que les messages avec cet en-tête X peuvent toujours être déplacés vers le dossier courrier inDésirable de la boîte aux lettres en raison de la configuration indésirable des boîtes aux lettres Vous pouvez modifier ce paramètre en désactivant cette fonctionnalité à l'aide de Set-MailboxJunkEmailConfiguration.
        
      - **Ajouter la ligne d'objet avec du texte** Envoie le message aux destinataires voulus, mais ajoute à la ligne d'objet le texte que vous spécifiez dans la **ligne d'objet du préfixe avec cette** zone d'entrée de texte. En utilisant ce texte comme identificateur, vous pouvez éventuellement créer des règles pour filtrer ou acheminer les messages selon vos besoins. 
        
      - **Rediriger le message vers une adresse e-mail** Envoie le message à une adresse e-mail spécifiée au lieu des destinataires prévus. Spécifiez l'adresse de redirection dans la zone d'entrée **Rediriger vers cette adresse e-mail**.<br/><br/>Remarque: pour plus d'informations sur les niveaux de confiance du courrier indésirable, voir [niveaux de probabilité de courrier](spam-confidence-levels.md)indésirable. 
  
5. Sous **courrier en nombre**, vous pouvez sélectionner un seuil pour traiter les messages électroniques en masse comme du courrier indésirable. Ce seuil est basé sur le niveau de réclamation en bloc du message. Vous pouvez choisir un paramètre de seuil compris entre 1 et 9, où 1 indique la plupart des messages électroniques en nombre comme du courrier indésirable et 9 la plupart des messages électroniques en nombre. Le service effectue ensuite l'action configurée, telle que l'envoi du message au dossier de courrier inDésirable du destinataire. Consultez la rubrique [valeurs de niveau de réclamation en bloc](bulk-complaint-level-values.md) et [quelle est la différence entre courrier indésirable et courrier électronique en masse?](what-s-the-difference-between-junk-email-and-bulk-email.md) pour plus d'informations. 
    
6. Dans la page **Listes rouges**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours marquées comme courrier indésirable. Le service applique l'action configurée de courrier indésirable à probabilité élevée sur le courrier électronique correspondant à ces entrées. 
    
      - Ajoutez des expéditeurs indésirables à la liste de blocage des expéditeurs. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les adresses des expéditeurs à bloquer dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur **OK** pour revenir à la page **Listes rouges**. 
        
      - Ajoutez des domaines indésirables à la liste des domaines bloqués. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les domaines à bloquer dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur **OK** pour revenir à la page **Listes rouges**.<br/><br/>**ATTENTION: Si vous bloquez des domaines de niveau supérieur, il est probable que le courrier électronique que vous souhaitez utiliser soit marqué comme courrier indésirable.** 
  
7. Dans la page **Listes vertes**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours remises dans la boîte de réception. Le courrier électronique provenant de ces entrées n'est pas traité par le filtre de courrier indésirable. 
    
      - Ajoutez des expéditeurs approuvés à la liste des expéditeurs autorisés. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les adresses des expéditeurs à autoriser dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur OK pour revenir à la page **Listes vertes**. 
        
      - Ajoutez des domaines approuvés à la liste de domaines autorisés. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les domaines à autoriser dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur OK pour revenir à la page **Listes vertes**.<br/><br/>**ATTENTION: Si vous autorisez des domaines de niveau supérieur, il est probable que le courrier électronique indésirable sera remis dans une boîte de réception.** 
  
8. Sur la page **courrier IndésirAble international** , vous pouvez filtrer les messages électroniques rédigés dans des langues spécifiques ou provenant de pays ou régions spécifiques. Vous pouvez configurer jusqu'à 86 langues différentes et 250 différentes régions. Le service applique l'action configurée pour le courrier indésirable à niveau de fiabilité élevée. 
    
9. Activez la case à cocher **Filtrer les messages électroniques écrits dans les langues suivantes** pour activer cette fonctionnalité. Cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter, puis, dans la boîte de dialogue de sélection, effectuez vos choix (la sélection multiple est prise en charge). Par exemple, si vous choisissez de filtrer les messages écrits en arabe (AR) et que le **message de mise en quarantaine** est votre action configurée pour les messages de courrier indésirable à niveau de confiance élevée, tous les messages écrits en arabe sont mis en quarantaine. Cliquez sur **OK** pour revenir au volet **courrier indésirable international** . 
    
10. Activez la case à cocher **Filtrer les messages électroniques envoyés de la région ou des pays suivants** pour activer cette fonctionnalité. Cliquez ![sur icône](media/ITPro-EAC-AddIcon.gif)ajouter, puis, dans la boîte de dialogue de sélection, effectuez vos choix (la sélection multiple est prise en charge). Par exemple, si vous choisissez de filtrer tous les messages envoyés à partir d'Australie (au) et que le **message de mise en quarantaine** est votre action configurée pour les messages de courrier indésirable à niveau de fiabilité élevée, tous les messages envoyés à partir de l'Australie seront mis en quarantaine. Cliquez sur **OK** pour revenir au volet **courrier indésirable international** .<br/><br/>Par défaut, si aucune option de courrier indésirable international n'est sélectionnée, le service applique le filtrage de courrier indésirable standard à tous les messages envoyés, quelle qu'en soit la langue ou la région d'origine. Les messages sont analysés et les actions configurées sont appliquées si le message est identifié comme courrier indésirable ou comme courrier indésirable à probabilité élevée. 
  
11. Sur la page **Options avancées** , vous pouvez sélectionner **activé**, **désactivé**ou **test** pour chaque option de filtrage avancé du courrier indésirable. 
    
12. **Sur** Les messages sont activement filtrés en fonction de la règle associée à cette option. Les messages sont marqués comme courrier indésirable ou les scores de courrier indésirable augmentent, en fonction des options que vous activez. 
    
13. **Désactivé** Aucune action n'est appliquée sur les messages qui répondent aux critères de filtrage du courrier indésirable. Par défaut, toutes les options sont désactivées. 
    
14. **Test** Aucune action n'est effectuée sur les messages qui répondent aux critères de filtrage du courrier indésirable. Toutefois, les messages peuvent être balisés en ajoutant un en-tête X avant d'être remis au destinataire concerné. Cet en-tête X vous permet de savoir quelle option ASF a été mise en correspondance. Si vous avez spécifié **test** pour l'une des options avancées, vous pouvez configurer les paramètres du mode test suivants pour qu'ils soient appliqués lorsqu'une correspondance est établie avec une option activée pour le test: 
    
      - **Aucune** Aucune action en mode test n'est appliquée au message. Il s'agit du paramétrage par défaut. 
        
      - **Ajouter le texte d'en-tête X de test par défaut** La sélection de cette option envoie le message aux destinataires spécifiés, mais ajoute également un en-tête X spécial au message pour l'identifier comme ayant correspondu à une option de filtrage avancé du courrier indésirable spécifique. 
        
      - **Envoyer un message CCI à cette adresse** La sélection de cette option envoie une copie carbone invisible du message à l'adresse de messagerie que vous spécifiez dans la zone d'entrée. <br/><br/>Pour plus d'informations sur les options de filtrage avancé du courrier indésirable, notamment des descriptions de chaque option et du texte d'en-tête X associé à chacun d'eux, voir [Options avancées de filtrage du courrier](advanced-spam-filtering-asf-options.md)indésirable. 
  
15. Pour les stratégies personnalisées uniquement, cliquez sur l'élément **de menu appliquer à** , puis créez une règle basée sur une condition pour spécifier les utilisateurs, les groupes et les domaines auxquels cette stratégie doit être appliquée. Vous pouvez créer plusieurs conditions, si elles sont uniques. 
    
      - Pour sélectionner des utilisateurs, sélectionnez **le destinataire est**. Dans la boîte de dialogue suivante, sélectionnez un ou plusieurs expéditeurs de votre entreprise dans la liste sélecteur d'utilisateur, puis cliquez sur **Ajouter**. Pour ajouter des expéditeurs qui ne figurent pas dans la liste, entrez leurs adresses de messagerie, puis cliquez sur **vérifier les noms**. Dans cette zone, vous pouvez également utiliser des caractères génériques pour plusieurs adresses de messagerie (par \* @ exemple: _nomdomaine_). Lorsque vous avez terminé vos sélections, cliquez sur **OK** pour revenir à l'écran principal. 
        
      - Pour sélectionner des groupes, sélectionnez **le destinataire est membre de**. Ensuite, dans la boîte de dialogue suivante, sélectionnez ou spécifiez les groupes. Cliquez sur **OK** pour revenir à l'écran principal. 
        
      - Pour sélectionner des domaines, sélectionnez **le domaine du destinataire est**. Ensuite, dans la boîte de dialogue suivante, ajoutez les domaines. Cliquez sur **OK** pour revenir à l'écran principal.<br/><br/>Vous pouvez créer des exceptions au sein de la règle. Par exemple, vous pouvez filtrer les messages de tous les domaines à l'exception d'un domaine donné. Cliquez sur **Ajouter une exception**, puis créez vos conditions d'exception de la même manière que vous avez créé les autres conditions.<br/><br/>L'application d'une stratégie de courrier indésirable à un groupe est prise en charge uniquement pour les **groupes de sécurité à extension messagerie**. 
  
16. Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie s'affiche dans le volet droit.

La stratégie par défaut ne peut pas être désactivée ou supprimée et les stratégies personnalisées ont toujours priorité sur la stratégie par défaut. Pour les stratégies personnalisées, vous pouvez activer ou désactiver les cases à cocher dans la colonne **activé** pour les activer ou les désactiver. Par défaut, toutes les stratégies sont activées. Pour supprimer une stratégie personnalisée, sélectionnez-la, cliquez sur ![l'icône](media/ITPro-EAC-DeleteIcon.gif) **** de suppression de l'icône de suppression, puis confirmez la suppression de la stratégie.

> [!TIP]
>  Vous pouvez modifier la priorité (ordre en cours) de vos stratégies personnalisées en ![cliquant sur l'](media/ITPro-EAC-UpArrowIcon.gif) icône de flèche ![vers le haut](media/ITPro-EAC-DownArrowIcon.gif) et la flèche vers le bas. La stratégie dont la **priorité** est **0** s'exécute en premier, suivie de **1**, puis de **2**, et ainsi de suite. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Utilisation de PowerShell à distance pour configurer les stratégies de filtrage du courrier indésirable

Vous pouvez également configurer et appliquer des stratégies de filtrage du courrier indésirable dans PowerShell. Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554). Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).
  
- [Get-HostedContentFilterPolicy](http://technet.microsoft.com/library/d510471a-dda5-4df7-b3f8-2ee7a1948436.aspx) Afficher vos paramètres de filtrage du courrier indésirable. 
    
- [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) Modifier vos paramètres de filtrage du courrier indésirable. 
    
- [New-HostedContentFilterPolicy](http://technet.microsoft.com/library/4d15128d-9e16-42a1-8ac5-36f07d4bbbf0.aspx) Créer une stratégie de filtrage du courrier indésirable personnalisée. 
    
- [Remove-HostedContentFilterPolicy](http://technet.microsoft.com/library/9fe1fe03-8f83-41e3-9bf5-084a392784d6.aspx) Supprimer une stratégie de filtrage du courrier indésirable personnalisée. 
    
Pour appliquer une stratégie de filtrage du courrier indésirable personnalisée à des utilisateurs, à des groupes et/ou à des domaines, utilisez la cmdlet [New-HostedContentFilterRule](http://technet.microsoft.com/library/2df13ba9-1eb0-4da3-bd72-a79d5fa15e26.aspx) (pour créer une règle de filtrage pouvant être appliquée aux stratégies personnalisées) ou la cmdlet [Set-HostedContentFilterRule](http://technet.microsoft.com/library/ba259260-ffd3-43f3-8ef4-9d8659679d02.aspx) (pour modifier une règle de filtrage existante pouvant être appliquée aux stratégies personnalisées). Utilisez les cmdlets [Enable-HostedContentFilterRule](http://technet.microsoft.com/library/354ece28-dcde-4b5f-88ed-475115e7ea78.aspx) ou [Disable-HostedContentFilterRule](http://technet.microsoft.com/library/c1f8dafc-ef5d-47e3-b0fb-71a88e145fc5.aspx) pour activer ou désactiver la règle appliquée à la stratégie. 
  
## <a name="how-do-you-know-this-worked"></a>Comment savoir si cela a fonctionné ?

Pour vous assurer que le courrier indésirable est correctement détecté et traité, vous pouvez envoyer un message GTUBE via le service. Comme le fichier test d'antivirus EICAR, le message GTUBE teste le service pour vérifier qu'il détecte le courrier indésirable entrant. Un message GTUBE doit toujours être détecté comme courrier indésirable par le filtre de courrier indésirable, et les actions appliquées au message doivent correspondre aux paramètres que vous avez configurés.
  
Incluez le texte GTUBE suivant dans une ligne d'un message électronique, sans espaces ni sauts de ligne :
  
```
XJS*C4JDBQADN1.NSBN3*2IDNEN*GTUBE-STANDARD-ANTI-UBE-TEST-EMAIL*C.34X
```

## <a name="fine-tuning-your-spam-filter-policy-to-prevent-false-positives-and-false-negatives"></a>Optimisation de votre stratégie de filtrage de courrier indésirable pour éviter les faux positifs et les faux négatifs

Vous pouvez activer des options de filtrage avancé du courrier indésirable si vous souhaitez adopter une approche agressive du filtrage du courrier indésirable. Pour plus d'informations sur les paramètres de courrier indésirable généraux applicables à l'ensemble de l'organisation, consultez les rubriques relatives aux procédures visant à [empêcher que des courriers électroniques faux positifs soient marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkId=534224) et à [bloquer du courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225). Elles sont utiles si vous disposez d'un contrôle de niveau administrateur et que vous souhaitez éviter les faux positifs ou les faux négatifs.
   
## <a name="for-more-information"></a>Pour plus d'informations
<a name="sectionSection6"> </a>

[Configurer la stratégie de filtrage des connexions](configure-the-connection-filter-policy.md)
  
[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  
[Mise en quarantaine](quarantine.md)
  
[Éviter les courriers électroniques faux positifs marqués comme courrier indésirable à l'aide d'une liste fiable ou d'autres techniques](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

