---
title: Configuration de vos stratégies de filtrage du courrier indésirable
ms.author: krowley
author: kccross
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
description: Paramètres du filtre de courrier indésirable de base sont sélection de l’action à effectuer sur les messages identifiés comme courrier indésirable et choisir de filtrer les messages qui sont enregistrés dans des langues spécifiques ou envoyés à partir de certains pays ou régions.
ms.openlocfilehash: 64b66f53bb56c404acefebd4fa9d211f5458f29f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29614478"
---
# <a name="configure-your-spam-filter-policies"></a>Configuration de vos stratégies de filtrage du courrier indésirable
  
Paramètres du filtre de courrier indésirable de base sont sélection de l’action à effectuer sur les messages identifiés comme courrier indésirable et choisir de filtrer les messages qui sont enregistrés dans des langues spécifiques ou envoyés à partir de certains pays ou régions. Paramètres de stratégie de filtre de courrier indésirable sont appliquées à des messages que les messages. Vous pouvez modifier la stratégie de filtrage du courrier indésirable par défaut pour configurer vos paramètres de filtrage du courrier indésirable de l’entreprise et créer des stratégies de filtrage anti-spam personnalisés, puis les appliquer à des utilisateurs spécifiques, des groupes ou des domaines de votre organisation. Stratégies personnalisées sont toujours prioritaires sur la stratégie par défaut. Vous pouvez modifier l’ordre dans lequel vos stratégies personnalisées pour s’exécuter en modifiant la priorité de chaque stratégie personnalisée.
  
> [!IMPORTANT]
> Pour les clients autonomes Exchange Online Protection (EOP) : par défaut, les filtres anti-spam EOP envoient des messages de courrier indésirable détectés au dossier courrier indésirable de chaque destinataire. Toutefois, afin de vous assurer que l’action **déplacer le message vers le dossier courrier indésirable** fonctionne pour les boîtes aux lettres locales, vous devez configurer les règles de Transport Exchange sur vos serveurs sur site pour détecter les en-têtes de spam ajoutés par EOP. Pour plus d’informations, voir [vous assurer que le courrier indésirable est routé vers le dossier courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md). 
  
## <a name="what-you-must-know-before-you-begin"></a>Vous devez connaître avant de commencer

Durée d'exécution estimée : 30 minutes
  
Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations dont vous avez besoin, consultez l’entrée de blocage du courrier indésirable dans la rubrique [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
  
Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
  
## <a name="use-the-exchange-admin-center-eac-to-configure-spam-filter-policies"></a>Utilisation du Centre d'administration Exchange (CAE) pour configurer les stratégies de filtrage du courrier indésirable

1. Dans le Centre d'administration Exchange (CAE), accédez à **Protection** \> **Filtre de courrier indésirable**.
    
2. Effectuez l'une des opérations suivantes dans la page **Général**: 
    
      - Double-cliquez sur la stratégie par défaut afin de modifier cette dernière pour l'ensemble de l'organisation.
    
      - Cliquez sur l'icône ![Icône Ajouter](media/ITPro-EAC-AddIcon.gif) **Nouveau** pour créer une stratégie personnalisée de filtrage du courrier indésirable applicable à des utilisateurs, des groupes et des domaines au sein de votre organisation. Vous pouvez également modifier des stratégies personnalisées en double-cliquant dessus. 
    
3. Pour les stratégies personnalisées, spécifiez un nom pour cette stratégie. Si vous le souhaitez, vous pouvez également spécifier une description plus détaillée. Vous ne pouvez pas renommer la stratégie par défaut.<br/><br/>Remarque : Lorsque vous créez une stratégie, tous les paramètres de configuration apparaissent sur un seul écran. En revanche, lorsque vous modifiez une stratégie, vous devez parcourir plusieurs écrans. Les paramètres sont les mêmes dans les deux cas, mais le reste de cette procédure décrit comment accéder à ces paramètres lorsque vous modifiez une stratégie. 
  
4. Sur la page **actions à effectuer pour les messages électroniques en nombre et le courrier indésirable**, sous **Courrier indésirable** et **Courrier indésirable à niveau de confiance élevé**, sélectionnez l'action à effectuer pour les messages électroniques en nombre et le courrier indésirable entrant. Par défaut, l'option **Déplacer les messages vers le dossier Courrier indésirable** est sélectionnée. Les autres valeurs possibles sont les suivantes : 
    
      - **Supprimer le message** Supprime le message entier, pièces jointes comprises. 
        
      - **Mettre en quarantaine le message** Envoie le message en quarantaine au lieu de le remettre à ses destinataires. Si vous sélectionnez cette option, dans la zone d'entrée **Conserver les courriers indésirables pendant (jours)**, spécifiez le nombre de jours pendant lesquels le courrier indésirable restera en quarantaine. (Il sera automatiquement supprimé à l'issue de cette période. La valeur par défaut est 15 jours, ce qui est également la valeur maximale. La valeur minimale est 1 jour.)<br/><br/>Conseil : Pour plus d’informations sur la façon dont les administrateurs peuvent gérer les messages électroniques qui se trouvent dans la mise en quarantaine dans le CAE, voir [mise en quarantaine](quarantine.md) et [Rechercher et débloquer les messages mis en quarantaine en tant qu’administrateur](find-and-release-quarantined-messages-as-an-administrator.md). > pour plus d’informations sur la configuration de notification de courrier indésirable à envoyer aux utilisateurs, reportez-vous à [l’utilisateur final Configure dans EOP les notifications de courrier indésirable](configure-end-user-spam-notifications-in-eop.md) ou [configurer pour l’utilisateur final de spam notifications dans Exchange Online](configure-end-user-spam-notifications-in-exchange-online.md). 
  
      - **Déplacer le message dans le dossier Courrier indésirable** Envoie le message au dossier Courrier indésirable des destinataires spécifiés. Il s'agit de l'action par défaut pour les deux niveaux de seuil de confiance.<br/><br/>**IMPORTANT : Pour les clients Exchange Online Protection (EOP) : afin que cette action travailler avec des boîtes aux lettres locales, vous devez configurer deux règles de Transport Exchange sur vos serveurs sur site pour détecter les en-têtes de spam ajoutés par EOP. Pour plus d’informations, voir [vous assurer que le courrier indésirable est routé vers le dossier courrier indésirable de chaque utilisateur](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).**
  
      - **Ajouter un en-tête X** Envoie le message aux destinataires spécifiés, mais ajoute du texte d’en-tête X à l’en-tête de message afin d’identifier le message comme courrier indésirable. À l’aide de ce texte en tant qu’identificateur, vous pouvez éventuellement créer des règles de boîte de réception ou utiliser un périphérique en aval pour agir sur le message. Le texte d’en-tête X par défaut est **ce message s’affiche comme courrier indésirable**.<br/>Vous pouvez personnaliser le texte d’en-tête X à l’aide de la zone de saisie **Ajouter ce texte d’en-tête X** . Si vous personnalisez le texte d’en-tête X, prenez note des conditions suivantes : 
    
      - Si vous spécifiez uniquement l’en-tête dans le format \< *en-tête*\>, lorsqu’il n’y a aucuns espaces dans le \< *en-tête*\>, un signe deux-points sera ajouté au texte personnalisé, suivi du texte par défaut. Par exemple, si vous spécifiez « Ce-est-mon-custom-header », le texte d’en-tête X apparaît sous la forme « ce est-mon-personnalisé-en-tête : ce message s’affiche comme courrier indésirable. »       
        
      - Si vous incluez des espaces dans le texte d’en-tête personnalisé, ou si vous ajoutez le signe deux-points vous-même (tel que « X il s’agit de l’en-tête personnalisé » ou « X-This-is-my-custom-header : »), le texte d’en-tête X rétablit la valeur par défaut en tant que » X ce-est-courrier indésirable : ce message s’affiche comme courrier indésirable. »
    
      - Vous ne pouvez pas spécifier le texte d’en-tête au format \< *en-tête*  \>:\<  *valeur*  \>. Si vous procédez ainsi, les deux valeurs avant et après le signe deux-points sera ignoré et le texte d’en-tête X par défaut s’affiche à la place : « X ce-est-courrier indésirable : ce message s’affiche comme courrier indésirable. » 
      
      - N’oubliez pas que les messages électroniques avec cet en-tête X-peuvent être toujours déplacés vers dossier de courrier indésirable de boîte aux lettres en raison de la configuration indésirable des boîtes aux lettres. Vous pouvez le modifier en désactivant cette fonctionnalité avec Set-MailboxJunkEmailConfiguration.
        
      - **Ligne d’objet Prepend avec du texte** Envoie le message aux destinataires appropriés, mais ajoute la ligne d’objet avec le texte que vous spécifiez dans la zone d’entrée **du message avec le texte de préfixe** . À l’aide de ce texte en tant qu’identificateur, vous pouvez également créer des règles pour filtrer ou acheminer les messages que nécessaire. 
        
      - **Rediriger le message vers une adresse e-mail** Envoie le message à une adresse e-mail spécifiée au lieu des destinataires prévus. Spécifiez l'adresse de redirection dans la zone d'entrée **Rediriger vers cette adresse e-mail**.<br/><br/>Remarque : Pour plus d’informations sur les niveaux de confiance du courrier indésirable, voir [Spam confidence levels](spam-confidence-levels.md). 
  
5. Sous **messages électroniques en masse**, vous pouvez sélectionner un seuil pour traiter les messages électroniques en masse comme du courrier indésirable. Ce seuil est basé sur le niveau de réclamation en bloc du message. Vous pouvez choisir un paramètre de seuil de 1 à 9, où 1 indique la plupart des messages électroniques en masse comme du courrier indésirable et 9 permet la plupart des e-mails être remis. Ensuite, le service effectue l’action configurée, telles que l’envoi du message vers dossier de courrier indésirable du destinataire. Voir les [valeurs au niveau de réclamation en bloc](bulk-complaint-level-values.md) et [Quelle est la différence entre courrier indésirable et les messages électroniques en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md) pour plus d’informations. 
    
6. Dans la page **Listes rouges**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours marquées comme courrier indésirable. Le service applique l'action configurée de courrier indésirable à probabilité élevée sur le courrier électronique correspondant à ces entrées. 
    
      - Ajoutez des expéditeurs indésirables à la liste de blocage des expéditeurs. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les adresses des expéditeurs à bloquer dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur **OK** pour revenir à la page **Listes rouges**. 
        
      - Ajoutez des domaines indésirables à la liste des domaines bloqués. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les domaines à bloquer dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur **OK** pour revenir à la page **Listes rouges**.<br/><br/>**Attention : Si vous bloquez des domaines de premier niveau, il est probable que courrier électronique que vous souhaitez sera marqué comme courrier indésirable.** 
  
7. Dans la page **Listes vertes**, vous pouvez indiquer des entrées, telles que des expéditeurs ou des domaines, qui seront toujours remises dans la boîte de réception. Le courrier électronique provenant de ces entrées n'est pas traité par le filtre de courrier indésirable. 
    
      - Ajoutez des expéditeurs approuvés à la liste des expéditeurs autorisés. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les adresses des expéditeurs à autoriser dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur OK pour revenir à la page **Listes vertes**. 
        
      - Ajoutez des domaines approuvés à la liste de domaines autorisés. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis ajoutez les domaines à autoriser dans la boîte de dialogue de sélection. Vous pouvez séparer les entrées à l'aide d'un point-virgule ou d'un retour à la ligne. Cliquez sur OK pour revenir à la page **Listes vertes**.<br/><br/>**Attention : Si vous autorisez les domaines de premier niveau, il est probable que messagerie vous ne voulez pas qu’est remis à une boîte de réception.** 
  
8. Dans la page **Du courrier indésirable International** , vous pouvez filtrer les messages électroniques qui sont enregistrés dans des langues spécifiques ou envoyés à partir de certains pays ou régions. Vous pouvez configurer jusqu'à 250 différentes régions et de 86 différentes langues. Le service s’applique l’action configurée pour le courrier indésirable fiables. 
    
9. Activez la case à cocher de **filtrer les messages électroniques écrites dans les langues suivantes** pour activer cette fonctionnalité. Cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif)et puis, dans la boîte de dialogue de sélection, faites votre choix (sélection multiple est prise en charge). Par exemple, si vous sélectionnez cette option pour filtrer les messages écrits en arabe (AR) et **message de quarantaine** est votre action configurée pour les messages de courrier indésirable de niveau de confiance élevé, écrits en arabe tous les messages seront mis en quarantaine. Cliquez sur **OK** pour revenir au volet de **Courrier indésirable International** . 
    
10. Activez la case à cocher **filtrer les messages électroniques envoyés à partir de suivant pays ou régions** pour activer cette fonctionnalité. Cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif)et puis, dans la boîte de dialogue de sélection, faites votre choix (sélection multiple est prise en charge). Par exemple, si vous sélectionnez cette option pour filtrer tous les messages envoyés à partir de l’Australie (AU) et **message de quarantaine** est votre action configurée pour fiables de courrier indésirable, puis tous les messages émanant d’Australie seront mis en quarantaine. Cliquez sur **OK** pour revenir au volet de **Courrier indésirable International** .<br/><br/>Par défaut, si aucune option de courrier indésirable international n'est sélectionnée, le service applique le filtrage de courrier indésirable standard à tous les messages envoyés, quelle qu'en soit la langue ou la région d'origine. Les messages sont analysés et les actions configurées sont appliquées si le message est identifié comme courrier indésirable ou comme courrier indésirable à probabilité élevée. 
  
11. Dans la page **Options avancées** , vous pouvez sélectionner **, **désactivé**ou **Test** **pour chaque option de filtrage avancé du courrier indésirable. 
    
12. **Sur** Les messages sont filtrés activement en fonction de la règle associée à cette option. Messages sont soit marqués comme courrier indésirable ou sera ont leur score de spam augmenté, en selon les options que vous allumez. 
    
13. **Désactivé** Aucune action n'est appliquée sur les messages qui répondent aux critères de filtrage du courrier indésirable. Par défaut, toutes les options sont désactivées. 
    
14. **Test** Aucune action sur les messages qui répondent aux critères du filtre de courrier indésirable. Toutefois, les messages peuvent être marquées en ajoutant un en-tête X-lorsqu’ils sont remis au destinataire. Cet en-tête X vous permet de savoir quelle option ASF a été mis en correspondance. Si vous avez spécifié pour une des options avancées de **Test** , vous pouvez configurer les paramètres de mode de test suivants à appliquer lorsqu’une correspondance est établie avec une option de test : 
    
      - **Aucune** Aucune action en mode test n'est appliquée au message. Il s'agit du paramétrage par défaut. 
        
      - **Ajouter la valeur par défaut de test en-tête X** Cette option envoie le message aux destinataires spécifiés, mais ajoute également un en-tête X spécial pour le message pour l’identifier comme un spécifique avancé du courrier indésirable option de filtrage ne correspondant. 
        
      - **Envoyer un message Cci à cette adresse** Cette option envoie une copie carbone invisible du message à l’adresse de messagerie que vous spécifiez dans la zone d’entrée. <br/><br/>Pour plus d’informations sur l’options, notamment des descriptions sur chaque option et le texte d’en-tête X associé à chacun d’eux, de filtrage avancé du courrier indésirable, consultez la rubrique [options de filtrage avancé du courrier indésirable](advanced-spam-filtering-asf-options.md). 
  
15. Pour les stratégies personnalisées uniquement, cliquez sur l’élément de menu **Appliquer** , puis créer une règle basée sur une condition pour spécifier les utilisateurs, groupes et domaines à laquelle appliquer cette stratégie. Vous pouvez créer plusieurs conditions, si elles sont uniques. 
    
      - Pour sélectionner les utilisateurs, sélectionnez **le destinataire est**. Dans la boîte de dialogue qui apparaît, sélectionnez un ou plusieurs des expéditeurs de votre société dans la liste de sélecteur d’utilisateur, puis cliquez sur **Ajouter**. Pour ajouter des expéditeurs qui ne figurent pas dans la liste, tapez leurs adresses de messagerie, puis cliquez sur **vérifier les noms**. Dans cette zone, vous pouvez également utiliser des caractères génériques pour plusieurs adresses de messagerie (par exemple : \* @  _domainname_). Lorsque vous avez terminé vos sélections, cliquez sur **OK** pour revenir à l’écran principal. 
        
      - Pour sélectionner des groupes, sélectionnez **le destinataire est membre**. Puis, dans la boîte de dialogue, sélectionnez ou spécifier les groupes. Cliquez sur **OK** pour revenir à l’écran principal. 
        
      - Pour sélectionner les domaines, sélectionnez **le domaine du destinataire**. Puis, dans la boîte de dialogue, ajoutez les domaines. Cliquez sur **OK** pour revenir à l’écran principal.<br/><br/>Vous pouvez créer des exceptions à l’intérieur de la règle. Par exemple, vous pouvez filtrer les messages provenant de tous les domaines à l’exception d’un domaine. Cliquez sur **Ajouter une exception**, puis créer vos conditions d’exception de la même manière que vous avez créé les autres conditions.<br/><br/>Appliquer une stratégie de courrier indésirable à un groupe est pris en charge uniquement pour les **Groupes de sécurité avec messagerie**. 
  
16. Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie s'affiche dans le volet droit.

> [!TIP]
>  Vous pouvez activez ou désactivez les cases à cocher dans la colonne **activé** pour activer ou désactiver vos stratégies personnalisées. Par défaut, toutes les stratégies sont activées. La stratégie par défaut ne peut pas être désactivée. > pour supprimer une stratégie personnalisée, sélectionnez la stratégie, cliquez sur le ![icône de suppression](media/ITPro-EAC-DeleteIcon.gif) **Supprimer** l’icône, puis vérifiez que vous souhaitez supprimer la stratégie. Impossible de supprimer la stratégie par défaut. les stratégies personnalisées > sont toujours prioritaires sur la stratégie par défaut. Stratégies personnalisées s’exécutent dans l’ordre inverse dans lequel vous avez créé (de la plus ancienne à la plus récente), mais vous pouvez modifier la priorité (marche) de vos stratégies personnalisées en cliquant sur le ![d’icône de flèche](media/ITPro-EAC-UpArrowIcon.gif) flèche vers le haut et ![icône représentant une flèche vers le bas](media/ITPro-EAC-DownArrowIcon.gif) vers le bas flèche. La stratégie qui a une **priorité** **0** s’exécutera en premier, suivi par **1**, puis **2**et ainsi de suite. 
  
## <a name="use-remote-powershell-to-configure-spam-filter-policies"></a>Utilisation de PowerShell à distance pour configurer les stratégies de filtrage du courrier indésirable

Vous pouvez également configurer et appliquer des stratégies de filtrage du courrier indésirable dans PowerShell. Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554). Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, voir [se connecter à Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290).
  
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
  

