---
title: Configuration de la stratégie de filtrage des connexions
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
description: Pour vous assurer que le courrier envoyé des personnes de que confiance n’est pas bloqué, vous pouvez utiliser la stratégie de filtrage de connexion pour créer une liste verte, également appelé une liste d’expéditeurs autorisés, des adresses IP que vous approuvez. Vous pouvez également créer une liste des expéditeurs bloqués.
ms.openlocfilehash: d106e55779c6246b77018fef3ab9d58fa759d99e
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027601"
---
# <a name="configure-the-connection-filter-policy"></a>Configuration de la stratégie de filtrage des connexions
 
Nous avons tous des amis et des partenaires professionnels en qui nous avons confiance. Cela peut être frustrant de retrouver leurs messages électroniques dans votre dossier de courrier indésirable, ou même complètement bloqués par un filtre de blocage du courrier indésirable. Si vous voulez vous assurer que les messages envoyés par des personnes de confiance ne sont pas bloqués, vous pouvez utiliser la stratégie de filtrage des connexions pour créer une liste d'adresses IP approuvées (également appelée liste d'expéditeurs autorisés) en lesquelles vous avez confiance. Vous pouvez également créer une liste d'expéditeurs bloqués, qui est une liste d'adresses IP, généralement d'expéditeurs de courrier indésirable connus, desquels vous ne voulez jamais recevoir de messages électroniques.
  
 Pour plus d'informations sur d'autres paramètres de courrier indésirable applicables à l'ensemble de l'organisation, consultez les rubriques relatives aux procédures permettant de [s'assurer qu'un message n'est pas marqué comme courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=534224) et de [bloquer le courrier indésirable avec le filtre anti-courrier indésirable d'Office 365 pour éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225). Ces procédures sont utiles si vous disposez d'un contrôle de niveau administrateur et que vous souhaitez éviter les faux positifs ou les faux négatifs.
  
La vidéo suivante montre les étapes de configuration de la stratégie de filtrage des connexions :
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer ?
<a name="sectionSection0"> </a>

- Durée d'exécution estimée : 15 minutes
    
- Vous devez avoir les autorisations avant de pouvoir effectuer cette procédure, ou procédures. Pour voir les autorisations dont vous avez besoin, consultez l’entrée « Anti-spam » dans la rubrique [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Pour obtenir l'adresse IP de l'expéditeur pour lequel vous souhaitez autoriser ou bloquer les messages, vous pouvez consulter l'en-tête Internet du message. Recherchez l'en-tête CIP comme décrit dans [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md). Pour plus d'informations sur l'affichage de l'en-tête d'un message dans plusieurs clients de messagerie, consultez la rubrique [Analyseur d'en-têtes de message](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
    
- Les courriers électroniques envoyés depuis une adresse IP dans la liste d'adresses IP bloquées sont rejetés, ne sont pas marqués comme courriers indésirables et aucun filtrage supplémentaire n'est appliqué.
    
- La procédure de filtre de connexion suivante peut également être effectuée via PowerShell à distance. Utilisez l’applet de commande [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) pour passer en revue vos paramètres et le [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) pour modifier vos paramètres de stratégie de filtrage de connexion. Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, voir [se connecter à Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>Utilisation du Centre d'administration Exchange (CAE) pour modifier la stratégie par défaut de filtrage des connexions
<a name="sectionSection1"> </a>

Créez une liste d'adresses IP approuvées ou bloquées en modifiant la stratégie de filtrage des connexions dans le Centre d'administration Exchange (CAE). Les paramètres de stratégie de filtrage des connexions sont appliqués uniquement aux messages entrants.
  
1. Dans le Centre d'administration Exchange (CAE), accédez à **Protection** \> **Filtre des connexions**, puis double-cliquez sur la stratégie par défaut.
    
2. Cliquez sur l'option de menu **Filtrage des connexions**, puis créez les listes nécessaires : une liste d'adresses IP approuvées, une liste d'adresses IP bloquées ou les deux. 
    
    Pour créer ces listes, cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.png). Dans la boîte de dialogue qui s'affiche, spécifiez l'adresse ou la plage d'adresses IP, puis cliquez sur **OK**. Pour ajouter d'autres adresses, répétez ce processus (vous pouvez également modifier ou supprimer des adresses IP après les avoir ajoutées).
    
    > [!NOTE]
    >  Si vous ajoutez une adresse IP aux deux listes, les messages envoyés par cette adresse IP seront autorisés. >  Les adresses IP IPV4 doivent être spécifiées au format nnn.nnn.nnn.nnn, où nnn est un nombre compris entre 0 et 255. Vous pouvez également spécifier des plages CIDR (Classless Inter-Domain Routing) au format nnn.nnn.nnn.nnn/rr, où rr est un nombre compris entre 24 et 32. Pour spécifier des plages en dehors de celle comprise entre 24 et 32, consultez la rubrique [Considérations concernant la configuration des listes vertes IP](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). >  Vous pouvez spécifier 1273 entrées maximum, sachant qu'une entrée est une adresse IP unique ou une plage CIDR d'adresses IP entre /24 et /32. >  Si vous envoyez des messages chiffrés via TLS, les adresses IPv6 et les plages d'adresses ne sont pas prises en charge. 
  
3. Vous pouvez également cocher la case **Activer la liste approuvée** pour éviter que les messages de certains expéditeurs connus soient bloqués. Comment ? Microsoft souscrit à des sources tierces d'expéditeurs dignes de confiance. Avec cette liste approuvée, les messages des expéditeurs fiables ne sont pas marqués en tant que courrier indésirable par erreur. Nous vous recommandons de sélectionner cette option, car elle devrait permettre de réduire le nombre de faux positifs (courrier valide classé comme courrier indésirable). 
    
4. Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie par défaut s'affiche dans le volet droit.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>Considérations concernant la configuration des listes vertes IP
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

Voici des considérations supplémentaires que vous pouvez envisager ou dont vous devez être informé lors de la configuration d'une liste verte IP.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>Spécification d'une plage de routage CIDR en dehors des plages recommandées

Pour spécifier une plage d'adresses IP CIDR s'étendant de /1 à /23, vous devez créer une règle de transport opérant sur cette plage d'adresses IP et qui définit le seuil de probabilité de courrier indésirable (SCL) sur **Contourner le filtrage du courrier indésirable** (ce qui signifie que tous les messages provenant d'adresses IP se trouvant sur cette plage sont définis comme « courrier légitime » et que le service n'effectue aucun filtrage supplémentaire). Toutefois, si l'une de ces adresses IP figure sur une liste rouge de Microsoft ou de ses fournisseurs de listes tiers, ces messages sont bloqués. Il est donc fortement recommandé d'utiliser la plage d'adresses de /32 à /24 IP. 
  
Pour créer cette règle de transport, procédez comme suit :
  
1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.png), puis sélectionnez **Créer une règle**.
    
3. Nommez la règle, puis cliquez sur **Plus d'options**.
    
4. Sous **Appliquer cette règle si**, sélectionnez **L'expéditeur**, puis **l'adresse IP se situe dans l'une de ces plages ou correspond exactement**.
    
5. Dans le champ **Spécifier des adresses IP**, spécifiez la plage d'adresses IP, cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.png), puis sur **OK**.
    
6. Sous **Faire ceci**, définissez l'action en sélectionnant **Modifier les propriétés des messages**, puis **Définir le seuil de probabilité de courrier indésirable (SCL)**. Dans le champ **spécifier la valeur SCL**, sélectionnez **Ignorer le filtrage du courrier indésirable**, puis cliquez sur **OK**.
    
7. Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer, tester et activer la règle sur une période spécifique, etc. Nous vous recommandons de tester la règle pendant un certain temps avant de l'appliquer. Pour plus d'informations sur ces sélections, voir [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx). 
    
8. Pour enregistrer la règle, cliquez sur **Enregistrer**. Elle apparaît dans votre liste de règles. 
    
Une fois la règle créée et appliquée, le filtrage du courrier indésirable est contourné pour la plage d'adresses IP spécifiée.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>Définition de l'étendue d'une exception de liste verte IP pour un domaine spécifique

En règle générale, nous vous recommandons d'ajouter les adresses IP (ou plages d'adresses IP) pour tous les domaines que vous jugez fiables à la liste verte IP. Toutefois, si vous ne voulez pas que votre liste verte IP s'applique à tous vos domaines, vous pouvez créer une règle de transport qui exclut des domaines spécifiques. 
  
Par exemple, supposons que vous disposez de trois domaines : ContosoA.com, ContosoB.com et ContosoC.com, et que vous souhaitez ajouter l'adresse IP (pour des raisons de simplicité, nous allons utiliser 1.2.3.4) et ignorer le filtrage uniquement pour le domaine ContosoB.com. Vous allez créer une liste verte IP pour 1.2.3.4, qui définit le seuil de probabilité de courrier indésirable (SCL) sur -1 (ce qui signifie qu'il est classé comme courrier non indésirable) pour tous les domaines. Vous pouvez ensuite créer une règle de transport qui définit le SCL pour tous les domaines sauf ContosoB.com sur 0. Le message est alors réanalysé pour tous les domaines associés à l'adresse IP, à l'exception de ContosoB.com qui est le domaine répertorié comme l'exception à la règle. Le SCL de ContosoB.com est toujours de -1, ce qui signifie que le filtrage est ignoré, tandis que celui de ContosoA.com et ContosoC.com est de 0, ce qui signifie qu'ils seront réanalysés par le filtre de contenu.
  
Pour ce faire, procédez comme suit :
  
1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.png), puis sélectionnez **Créer une règle**.
    
3. Nommez la règle, puis cliquez sur **Plus d'options**.
    
4. Sous **Appliquer cette règle si**, sélectionnez **L'expéditeur**, puis **l'adresse IP se situe dans l'une de ces plages ou correspond exactement**.
    
5. Dans le champ **Spécifier des adresses IP**, spécifiez l'adresse IP ou la plage d'adresses IP que vous avez entrée dans la liste d'adresses IP autorisées, cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.png), puis sur **OK**.
    
6. Sous **Faire ceci**, définissez l'action en sélectionnant **Modifier les propriétés des messages**, puis **définir le seuil de probabilité de courrier indésirable (SCL)**. Dans le champ **spécifier la valeur SCL**, sélectionnez **0**, puis cliquez sur **OK**.
    
7. Cliquez sur **Ajouter une exception**et sous **sauf si**, sélectionnez **l’expéditeur** et choisissez le **domaine est**. 
    
8. Dans le champ **Spécifier le domaine**, entrez le domaine pour lequel vous voulez contourner le filtrage du courrier indésirable, par exemple **contosob.com**. Cliquez sur **Ajouter**![Icône Ajouter](media/ITPro-EAC-AddIcon.png) pour le déplacer vers la liste d'expressions. Répétez cette étape pour ajouter d'autres domaines et exceptions, puis cliquez sur **OK** quand vous avez terminé. 
    
9. Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer, tester et activer la règle sur une période spécifique, etc. Nous vous recommandons de tester la règle pendant un certain temps avant de l'appliquer. Pour plus d'informations sur ces sélections, voir [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx). 
    
10. Pour enregistrer la règle, cliquez sur **Enregistrer**. Elle apparaît dans votre liste de règles. 
    
Après avoir créé et appliqué la règle, le filtrage du courrier indésirable de l'adresse IP ou de la plage d'adresses IP spécifiée est contourné uniquement pour l'exception de domaine que vous avez entrée.
  
## <a name="new-to-office-365"></a>Vous débutez avec Office 365 ?
<a name="sectionSection3"> </a>

||
|:-----|
|![Icône rapide pour LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Vous débutez avec Office 365 ?**         Découvrez les cours vidéo gratuits pour **Office 365 admins and IT pros** proposés par LinkedIn Learning. |
   
## <a name="for-more-information"></a>Pour plus d'informations
<a name="sectionSection4"> </a>

[Listes des expéditeurs autorisés et des expéditeurs bloqués dans Exchange Online](safe-sender-and-blocked-sender-lists-faq.md)
  
[Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md)
  
[Configurer la stratégie anti-courrier indésirable sortant](configure-the-outbound-spam-policy.md)
  
[Comment s'assurer qu'un message n'est pas marqué comme du courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=534224)
  
[Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225)
  

