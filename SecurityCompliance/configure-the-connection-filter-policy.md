---
title: Configuration de la stratégie de filtrage des connexions
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6ae78c12-7bbe-44fa-ab13-c3768387d0e3
ms.collection:
- M365-security-compliance
description: Pour vous assurer que le courrier électronique envoyé à partir de personnes que vous approuvez n'est pas bloqué, vous pouvez utiliser la stratégie de filtrage des connexions pour créer une liste verte, également appelée liste d'expéditeurs approuvés, des adresses IP que vous approuvez. Vous pouvez également créer une liste des expéditeurs bloqués.
ms.openlocfilehash: d7c99f8fb6b9b05efb800804927ccb26f7dd9f40
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216904"
---
# <a name="configure-the-connection-filter-policy"></a>Configuration de la stratégie de filtrage des connexions
 
Nous avons tous des amis et des partenaires professionnels en qui nous avons confiance. Cela peut être frustrant de retrouver leurs messages électroniques dans votre dossier de courrier indésirable, ou même complètement bloqués par un filtre de blocage du courrier indésirable. Si vous voulez vous assurer que les messages envoyés par des personnes de confiance ne sont pas bloqués, vous pouvez utiliser la stratégie de filtrage des connexions pour créer une liste d'adresses IP approuvées (également appelée liste d'expéditeurs autorisés) en lesquelles vous avez confiance. Vous pouvez également créer une liste d'expéditeurs bloqués, qui est une liste d'adresses IP, généralement d'expéditeurs de courrier indésirable connus, desquels vous ne voulez jamais recevoir de messages électroniques.
  
 Pour plus d'informations sur d'autres paramètres de courrier indésirable applicables à l'ensemble de l'organisation, consultez les rubriques relatives aux procédures permettant de [s'assurer qu'un message n'est pas marqué comme courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=534224) et de [bloquer le courrier indésirable avec le filtre anti-courrier indésirable d'Office 365 pour éviter les problèmes de faux négatifs](https://go.microsoft.com/fwlink/p/?LinkId=534225). Ces procédures sont utiles si vous disposez d'un contrôle de niveau administrateur et que vous souhaitez éviter les faux positifs ou les faux négatifs.
  
La vidéo suivante montre les étapes de configuration de la stratégie de filtrage des connexions :
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/b2f5bea3-e1a7-44b3-b7e2-07fac0d0ca40?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Ce qu'il faut savoir avant de commencer ?
<a name="sectionSection0"> </a>

- Durée estimée de l'opération : 15 minutes
    
- Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée «blocage du courrier indésirable» dans la rubrique [autorisations des fonctionnalités dans Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) . 
    
- Pour obtenir l'adresse IP de l'expéditeur dont vous souhaitez autoriser ou bloquer les messages, vous pouvez vérifier l'en-tête Internet du message. Recherchez l'en-tête CIP comme décrit dans en [-têtes de message anti-courrier](anti-spam-message-headers.md)indésirable. Pour plus d'informations sur l'affichage de l'en-tête d'un message dans divers clients de messagerie, voir Analyseur d' [en-têtes de message](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
    
- Les courriers électroniques envoyés depuis une adresse IP dans la liste d'adresses IP bloquées sont rejetés, ne sont pas marqués comme courriers indésirables et aucun filtrage supplémentaire n'est appliqué.
    
- La procédure de filtrage des connexions suivante peut également être effectuée via PowerShell à distance. Utilisez la cmdlet [Get-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/bd751db2-3f26-495b-8e5a-4fcab53b17fd.aspx) pour vérifier vos paramètres, et [Set-HostedConnectionFilterPolicy](http://technet.microsoft.com/library/ccb5731b-3fca-4d69-a91f-5049ea963fac.aspx) pour modifier vos paramètres de stratégie de filtrage des connexions. Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online Protection, consultez la rubrique [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). Pour savoir comment utiliser Windows PowerShell pour se connecter à Exchange Online, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
## <a name="use-the-eac-to-edit-the-default-connection-filter-policy"></a>Utilisation du Centre d'administration Exchange (CAE) pour modifier la stratégie par défaut de filtrage des connexions
<a name="sectionSection1"> </a>

Créez une liste d'adresses IP approuvées ou bloquées en modifiant la stratégie de filtrage des connexions dans le Centre d'administration Exchange (CAE). Les paramètres de stratégie de filtrage des connexions sont appliqués uniquement aux messages entrants.
  
1. Dans le Centre d'administration Exchange (CAE), accédez à **Protection** \> **Filtre des connexions**, puis double-cliquez sur la stratégie par défaut.
    
2. Cliquez sur l'option de menu **Filtrage des connexions**, puis créez les listes nécessaires : une liste d'adresses IP approuvées, une liste d'adresses IP bloquées ou les deux. 
    
    Pour créer ces listes, cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.gif). Dans la boîte de dialogue qui s'affiche, spécifiez l'adresse ou la plage d'adresses IP, puis cliquez sur **OK**. Pour ajouter d'autres adresses, répétez ce processus (vous pouvez également modifier ou supprimer des adresses IP après les avoir ajoutées).
    
    > [!NOTE]
    >  Si vous ajoutez une adresse IP aux deux listes, les messages envoyés à partir de cette adresse IP sont autorisés. 

    Spécifiez les adresses IP IPV4 au format nnn. nnn. nnn. nnn où NNN est un nombre compris entre 0 et 255. Vous pouvez également spécifier des plages CIDR (CLASSLESS Inter-Domain Routing) au format nnn. nnn. nnn. nnn/rr où RR est un nombre compris entre 24 et 32. Pour spécifier des plages en dehors de la plage de 24 à 32, consultez la rubrique [autres considérations à prendre en compte lors de la configuration des listes d'adresses IP autorisées](configure-the-connection-filter-policy.md#bkmk_addtionalconsiderationswhenconfiguringipallowlists). 

    Vous pouvez spécifier un maximum de 1273 entrées, où une entrée est une adresse IP unique ou une plage CIDR d'adresses IP comprise entre/24 et/32. > si vous envoyez des messages chiffrés via TLS, les adresses IPv6 et les plages d'adresses ne sont pas prises en charge. 
  
3. Éventuellement, activez la case à cocher **activer la liste verte** pour empêcher les messages électroniques manquants de certains expéditeurs bien connus. Manière? Microsoft s'abonne à des sources tierces d'expéditeurs approuvés. Cette liste verte signifie que ces expéditeurs approuvés ne sont pas marqués par erreur comme courrier indésirable. Nous vous recommandons de sélectionner cette option car elle doit réduire le nombre de faux positifs (courrier classé comme courrier indésirable) que vous recevez. 
    
4. Cliquez sur **Enregistrer**. Un résumé de vos paramètres de stratégie par défaut s'affiche dans le volet droit.
    
## <a name="additional-considerations-when-configuring-ip-allow-lists"></a>Considérations concernant la configuration des listes vertes IP
<a name="bkmk_addtionalconsiderationswhenconfiguringipallowlists"> </a>

Voici des considérations supplémentaires que vous pouvez envisager ou dont vous devez être informé lors de la configuration d'une liste verte IP.
  
### <a name="specifying-a-cidr-range-that-falls-outside-of-the-recommended-range"></a>Spécification d'une plage de routage CIDR en dehors des plages recommandées

Pour spécifier une plage d'adresses IP CIDR comprise entre/1 et/23, vous devez créer une règle de flux de messagerie qui fonctionne sur la plage d'adresses IP qui définit le seuil de probabilité de courrier indésirable (SCL) qui conTourne le **filtrage du courrier** indésirable (ce qui signifie que tous les messages reçus depuis cette plage d'adresses IP sont défini sur «pas de courrier indésirable») et aucun filtrage supplémentaire n'est effectué par le service). Toutefois, si l'une de ces adresses IP apparaît sur une liste rouge propriétaire de Microsoft ou sur l'une de nos listes de blocage tierces, ces messages seront toujours bloqués. Il est donc vivement recommandé d'utiliser la plage d'adresses IP/24 vers/32. 
  
Pour créer cette règle de flux de messagerie, procédez comme suit.
  
1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une règle**.
    
3. Nommez la règle, puis cliquez sur **Plus d'options**.
    
4. Sous **Appliquer cette règle si**, sélectionnez **L'expéditeur**, puis **l'adresse IP se situe dans l'une de ces plages ou correspond exactement**.
    
5. Dans la **zone spécifier des adresses IP**, spécifiez la plage d'adresses IP,](media/ITPro-EAC-AddIcon.gif)cliquez sur **Ajouter** ![une icône, puis cliquez sur **OK**.
    
6. Sous **Faire ceci**, définissez l'action en sélectionnant **Modifier les propriétés des messages**, puis **Définir le seuil de probabilité de courrier indésirable (SCL)**. Dans le champ **spécifier la valeur SCL**, sélectionnez **Ignorer le filtrage du courrier indésirable**, puis cliquez sur **OK**.
    
7. Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer la règle, tester la règle, activer la règle pendant une période spécifique, ainsi que d'autres sélections. Nous vous recommandons de tester la règle pendant une période avant de l'appliquer. [Procédures pour les règles de flux de messagerie dans Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contient plus d'informations sur ces sélections. 
    
8. Cliquez sur **Enregistrer** pour enregistrer la règle. La règle apparaît dans votre liste de règles. 
    
Une fois que vous avez créé et appliqué la règle, le service contourne le filtrage du courrier indésirable pour la plage d'adresses IP que vous avez spécifiée.
  
### <a name="scoping-an-ip-allow-list-exception-for-a-specific-domain"></a>Définition de l'étendue d'une exception de liste verte IP pour un domaine spécifique

En règle générale, nous vous recommandons d'ajouter les adresses IP (ou plages d'adresses IP) pour tous les domaines que vous jugez fiables à la liste verte IP. Toutefois, si vous ne voulez pas que votre liste verte IP s'applique à tous vos domaines, vous pouvez créer une règle de transport qui exclut des domaines spécifiques. 
  
Par exemple, supposons que vous disposez de trois domaines : ContosoA.com, ContosoB.com et ContosoC.com, et que vous souhaitez ajouter l'adresse IP (pour des raisons de simplicité, nous allons utiliser 1.2.3.4) et ignorer le filtrage uniquement pour le domaine ContosoB.com. Vous allez créer une liste verte IP pour 1.2.3.4, qui définit le seuil de probabilité de courrier indésirable (SCL) sur -1 (ce qui signifie qu'il est classé comme courrier non indésirable) pour tous les domaines. Vous pouvez ensuite créer une règle de transport qui définit le SCL pour tous les domaines sauf ContosoB.com sur 0. Le message est alors réanalysé pour tous les domaines associés à l'adresse IP, à l'exception de ContosoB.com qui est le domaine répertorié comme l'exception à la règle. Le SCL de ContosoB.com est toujours de -1, ce qui signifie que le filtrage est ignoré, tandis que celui de ContosoA.com et ContosoC.com est de 0, ce qui signifie qu'ils seront réanalysés par le filtre de contenu.
  
Pour ce faire, procédez comme suit :
  
1. Dans le CAE, accédez à **Flux de messagerie** \> **Règles**.
    
2. Cliquez sur ![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une règle**.
    
3. Nommez la règle, puis cliquez sur **Plus d'options**.
    
4. Sous **Appliquer cette règle si**, sélectionnez **L'expéditeur**, puis **l'adresse IP se situe dans l'une de ces plages ou correspond exactement**.
    
5. Dans la zone **spécifier des adresses IP** , spécifiez l'adresse IP ou la plage d'adresses IP que vous avez entrée dans la liste d'](media/ITPro-EAC-AddIcon.gif)adresses IP autorisées, cliquez sur **Ajouter** ![une icône, puis cliquez sur **OK**.
    
6. Sous **Faire ceci**, définissez l'action en sélectionnant **Modifier les propriétés des messages**, puis **définir le seuil de probabilité de courrier indésirable (SCL)**. Dans le champ **spécifier la valeur SCL**, sélectionnez **0**, puis cliquez sur **OK**.
    
7. Cliquez sur **Ajouter une exception**, puis sous **sauf si**, sélectionnez **l'expéditeur** et choisissez **domaine**. 
    
8. Dans la zone **spécifier un domaine** , entrez le domaine pour lequel vous souhaitez contourner le filtrage du courrier indésirable, tel que **contosob.com**. Cliquez sur **Ajouter** ![une](media/ITPro-EAC-AddIcon.gif) icône pour le déplacer vers la liste des expressions. Répétez cette étape pour ajouter d'autres domaines en tant qu'exceptions, puis cliquez sur **OK** lorsque vous avez terminé. 
    
9. Si vous le souhaitez, vous pouvez effectuer des sélections pour auditer la règle, tester la règle, activer la règle pendant une période spécifique, ainsi que d'autres sélections. Nous vous recommandons de tester la règle pendant une période avant de l'appliquer. [Procédures pour les règles de flux de messagerie dans Exchange Server](https://docs.microsoft.com/en-us/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures) contient plus d'informations sur ces sélections. 
    
10. Cliquez sur **Enregistrer** pour enregistrer la règle. La règle apparaît dans votre liste de règles. 
    
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
  

