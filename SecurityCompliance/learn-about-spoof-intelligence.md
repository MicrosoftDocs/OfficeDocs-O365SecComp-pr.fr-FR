---
title: En savoir plus sur l’usurpation d’identité
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 978c3173-3578-4286-aaf4-8a10951978bf
description: Utilisez aide à la décision usurpation d’identité de la sécurité &amp; centre de conformité dans la page Paramètres de blocage du courrier indésirable pour passer en revue tous les expéditeurs qui sont l’usurpation des domaines qui font partie de votre organisation ou l’usurpation des domaines externes. Aide à la décision usurpation d’identité n’est disponible dans le cadre d’Office 365 entreprise E5 ou séparément dans le cadre de la protection contre les menaces avancées et Exchange Online Protection.
ms.openlocfilehash: 3be606c05dde4a13d3a6a4a43ce927cf4f0ca53c
ms.sourcegitcommit: 176ce86e2b440c079414fe99d4b0b9e89ccebb40
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2018
ms.locfileid: "25496555"
---
# <a name="learn-more-about-spoof-intelligence"></a>En savoir plus sur l’usurpation d’identité

Utilisez aide à la décision usurpation d’identité de la sécurité &amp; centre de conformité dans la **page Paramètres de blocage du courrier indésirable** pour passer en revue tous les expéditeurs qui sont l’usurpation des domaines qui font partie de votre organisation ou l’usurpation des domaines externes. Aide à la décision usurpation d’identité n’est disponible dans le cadre d’Office 365 entreprise E5 ou séparément dans le cadre de Protection de menace avancées (DAV) et à compter d’octobre, 2018 Exchange Online Protection (EOP). 
  
## <a name="what-types-of-email-spoofing-can-i-review-and-which-should-i-protect-against-with-spoof-intelligence"></a>Quels types de messagerie usurpation puis-je consulter et qui dois-je protéger contre avec intelligence usurpation d’identité ?

Pour les domaines vous possédez, vous pouvez consulter les expéditeurs sont l’usurpation de votre domaine, puis cliquez sur Autoriser l’expéditeur continuer ou bloquer l’expéditeur. Pour les domaines externes, vous pouvez autoriser le domaine de l’expéditeur combiné à l’infrastructure d’envoi, mais pas une adresse électronique envoi individuelle.
  
Lorsqu’un expéditeur usurpe une adresse de messagerie, elles apparaissent à envoyer des messages au nom d’un ou plusieurs comptes d’utilisateur dans un des domaines de votre organisation ou un domaine externe, envoyez à votre organisation. Étonnamment, il existe quelques raisons légitime pour l’usurpation d’identité. Par exemple, dans ce cas, vous ne pas bloquer l’expéditeur de l’usurpation d’identité de votre domaine :
  
- Vous avez expéditeurs tiers qui utilisent votre domaine à envoyer du courrier électronique en masse à vos employés pour la société sondages.
    
- Vous avez embauchée une société externe à générer et envoyer des publicités ou des mises à votre place.
    
- Un assistant qui régulièrement doit envoyer un message électronique pour une autre personne de votre organisation.
    
- Une application qui est configurée pour usurper son propre organisation afin d’envoyer des notifications internes par courrier électronique.
    
Les domaines externes envoient fréquemment e-mail falsifié et un grand nombre de ces raisons sont légitimes. Par exemple, Voici certains cas légitimes lorsque les expéditeurs externes envoyer un message électronique usurpé :
  
- L’expéditeur figure dans une liste de distribution de discussion et la liste de distribution est relayer le courrier électronique de l’expéditeur d’origine à tous les participants dans la liste de distribution.
    
- Une société externe est envoyé au nom d’une autre société (par exemple, un rapport automatisé ou une société de logiciel en tant que service).
    
Vous avez besoin d’un moyen pour vous assurer que les messages envoyés par des questions légitimes n’obtenir intercepté dans les filtres anti-spam dans Office 365 ou des systèmes de messagerie externe. En règle générale, Office 365 traite les messages électroniques comme courrier indésirable. En tant qu’un administrateur Office 365, vous avez la possibilité d’éviter cela en définissant des filtres d’usurpation d’identité dans la sécurité &amp; centre de conformité. Si vous êtes propriétaire du domaine, vous pouvez configurer SPF DKIM et DMARC pour autoriser les expéditeurs.
  
En revanche, questions malveillantes, l’usurpation d’identité votre domaine ou des domaines externes à envoyer un courrier électronique indésirable ou hameçonnage, les expéditeurs doivent doit être bloquée. L’usurpation d’identité est également un moyen commun de phishing obtenir des informations d’identification de l’utilisateur. Office 365 offre une protection intégrée usurpation d’identité pour aider à protéger votre organisation des expéditeurs de ces messages. Protection contre l’usurpation des domaines de votre organisation est toujours active pour tous les clients Office 365 et protection d’usurpation d’identité de domaine externe est activée par défaut pour les clients de protection contre les menaces avancées et à compter d’octobre, 2018 EOP ainsi que les clients. Pour renforcer cette protection, nous indiquer les expéditeurs sont autorisés à usurper des domaines de votre organisation et envoyer un message électronique en votre nom, et si tous les domaines externes sont autorisés à usurper. Tout le courrier envoyé par un expéditeur que vous n’autorisez est considéré comme du courrier indésirable ou usurpation d’identité par Office 365. Surveillez les expéditeurs l’usurpation d’identité de votre domaine et nous aider à améliorer l’aide à la décision usurpation d’identité à l’aide de la sécurité &amp; centre de conformité.
  
## <a name="managing-spoof-intelligence-in-the-security-amp-compliance-center"></a>Aide à la décision usurpation d’identité dans la sécurité de la gestion des &amp; centre de conformité
<a name="Managespooflist"> </a>

La stratégie d’aide à la décision usurpation d’identité que vous configurer est toujours appliquée par Office 365. Vous ne pouvez pas la désactiver, mais vous pouvez choisir comment que vous voulez gérer activement.
  
Vous pouvez consulter les expéditeurs qui l’usurpation d’identité votre domaine ou des domaines externes, puis décider si chaque expéditeur doit être autorisé à le faire à l’aide de la sécurité &amp; centre de conformité. Pour chaque compte d’utilisateur usurpés et d’un expéditeur usurpe à partir de votre domaine ou un domaine externe, vous pouvez afficher les informations dans le tableau suivant.
  
|**Paramètre**|**Description**|
|:-----|:-----|
|Expéditeur  <br/> |Également appelée l’expéditeur la valeur true. Il s’agit généralement du domaine dont provient l’e-mail usurpation d’identité. Office 365 détermine le domaine du pointeur d’enregistrement DNS (PTR) de l’adresse IP d’envoi qui est l’usurpation de votre organisation. Si aucun domaine n’est trouvée, le rapport affiche adresse IP de l’expéditeur à la place.  <br/> |
|Utilisateur usurpé  <br/> |Le compte d’utilisateur qui est falsifié par l’expéditeur.  <br/> Onglet **interne** uniquement. Ce champ contient une adresse de messagerie unique, ou si l’expéditeur est l’usurpation de plusieurs comptes d’utilisateurs, il contient **plusieurs**.<br/> Onglet **externe** . Les domaines externes uniquement contient un domaine et ne contiennent pas une adresse de messagerie complète.<br/> > [!TIP]> **Pour les administrateurs avancés.** L’utilisateur usurpé est l’adresse (5322.From) qui est également l’adresse affiché comme adresse par le client de messagerie. Il est parfois appelée l’adresse header.from. La validité de cette adresse n’est pas vérifiée par le service SPF.           |
|Nombre de messages  <br/> |Le nombre de messages électroniques envoyés par l’expéditeur à votre organisation au nom de l’expéditeur usurpé identifié ou aux expéditeurs au sein au cours des 30 derniers jours.  <br/> |
|Nombre de réclamations d’utilisateur  <br/> |Réclamations signalées par les utilisateurs par rapport à cet expéditeur par vos utilisateurs dans au cours des 30 derniers jours. Réclamations sont généralement sous la forme d’envoi de courriers indésirables à Microsoft.  <br/> |
|Résultat de l’authentification  <br/> |Cette valeur est **transmise** si l’expéditeur passé expéditeur Exchange Online Protection (EOP) des contrôles d’authentification, tels que SPF ou DKIM, **Échec** en cas d’échec de l’expéditeur vérifications d’authentification de l’expéditeur EOP ou **inconnu** si le résultat de ces contrôles n’est pas connus.  <br/> |
|Décision  <br/> |Indique si l’administrateur Office 365 ou la stratégie d’aide à la décision usurpation d’identité déterminée ou non l’expéditeur est autorisé à usurper l’identité de l’utilisateur.  <br/> |
|Dernière détection  <br/> |Dernière date à laquelle un message a été reçu par cet expéditeur au nom de cet utilisateur usurpé.  <br/> |
|Autorisé à usurper ?  <br/> | Indique si cet expéditeur est autorisé à envoyer un message électronique au nom de l’utilisateur usurpé ou non. Les valeurs possibles sont les suivantes :<br/> **Oui** Toutes les adresses usurpés de cet expéditeur usurpation d’identité seront autorisés à usurper votre organisation.  <br/> **No** Usurpation d’adresses de cet expéditeur usurpation d’identité ne sont pas autorisés à usurper votre organisation. Au lieu de cela, les messages provenant de cet expéditeur seront marqués comme courrier indésirable par Office 365.<br/> **Certains utilisateurs** Si un expéditeur est l’usurpation de plusieurs utilisateurs, certaines adresses usurpés de cet expéditeur seront autorisés à usurper votre organisation, le reste sera marqué comme courrier indésirable. Utilisez l’onglet **Détails** pour afficher les adresses spécifiques.<br/> |
|Type d’usurpation d’identité  <br/> |Cette valeur est **interne** , si le domaine est l’un des domaines mis en service de votre organisation, dans le cas contraire, la valeur est **externe**.  <br/> |
   
 **Pour gérer les expéditeurs qui l’usurpation d’identité votre domaine à l’aide de la sécurité &amp; centre de conformité**
  
1. Accédez à la [sécurité &amp; centre de conformité](https://protection.office.com).
    
2. Connectez-vous à Office 365 avec votre compte professionnel ou de l’école. Votre compte doit disposer des informations d’identification d’administrateur de votre organisation Office 365.
    
3. Dans la sécurité &amp; centre de conformité, développez **Threat Management** \> **stratégie** \> **contre le courrier indésirable**.
  
![](media/0a098e68-5ecf-40d7-984f-d15fcc1f958d.jpg)
  
4. Dans la page **paramètres de blocage du courrier indésirable** dans le volet droit, sélectionnez l’onglet **personnalisé** et puis faites défiler vers le bas et développez **stratégie d’aide à la décision usurpation d’identité**. 
  
![](media/a5112100-0b37-460f-932d-5b2f98157871.jpg)
  
5. Pour afficher la liste des expéditeurs l’usurpation d’identité de votre domaine, cliquez sur **nouveaux expéditeurs de révision** et sélectionnez le ** vos domaines ** onglet. 
    
    Si vous avez déjà passé en revue les expéditeurs et que vous souhaitez modifier certains de vos choix précédents, vous pouvez choisir **me faire apparaître les expéditeurs que j’ai déjà révisé** . Dans les deux cas, le panneau suivant s’affiche. 
  
![](media/c0c062fd-f4a4-4d78-96f7-2c22009052bb.jpg)
  
Chaque utilisateur usurpé est affiché dans une ligne distincte afin que vous puissiez choisir s’il faut autoriser ou bloquer l’expéditeur de l’usurpation d’identité chaque utilisateur individuellement.
  
Pour ajouter un expéditeur à la liste verte d’un utilisateur, sélectionnez **Oui** dans la colonne **autorisé d’usurper** . Pour ajouter un expéditeur à la liste de blocage d’un utilisateur, cliquez sur **non**.
  
Pour définir la stratégie pour les domaines vous ne possédez pas, sélectionnez l’onglet **Domaines externes** modifier n’importe quel expéditeur sur **Oui** dans la colonne **autorisés à l’usurpation d’identité** pour autoriser que l’expéditeur pour envoyer un courrier électronique non authentifié dans votre organisation. Autrement, si vous pensez que Office 365 a effectué une erreur dans l’autorisation de l’expéditeur pour envoyer un message électronique usurpé, modifier la colonne **autorisé d’usurper** **non**. 
  
![](media/5dbef9cf-103f-49cd-9638-4b0083d6baa7.jpg)
  
6. Cliquez sur **Enregistrer** pour enregistrer les modifications. 

Si vous êtes un client E5 ou DAV, vous pouvez également gérer les expéditeurs sont l’usurpation de votre domaine par le biais de l' [Usurpation d’identité présente les aide à la décision](https://docs.microsoft.com/en-us/office365/securitycompliance/walkthrough-spoof-intelligence-insight)
    
## <a name="configuring-the-anti-spoofing-policy"></a>Configuration de la stratégie anti-l’usurpation d’identité
<a name="Managespooflist"> </a>

Outre l’autorisation ou le blocage d’un expéditeur particulier d’envoyer l’e-mail falsifié dans votre organisation, vous pouvez également configurer strict comment vous souhaitez le filtre à l’action à effectuer lorsqu’un message usurpation d’identité est trouvé et s’il faut activer les conseils de sécurité pour anti-usurpation d’identité.
  
Protection anti-usurpation est appliquée aux messages provenant d’expéditeurs de domaines qui sont externes à votre organisation Office 365. Vous pouvez appliquer la stratégie aux destinataires dont les boîtes aux lettres sont une licence pour Office 365 entreprise E5, protection contre les menaces avancées et à compter d’octobre, ainsi que les clients EOP 2018. Vous gérer la stratégie de l’usurpation d’identité anti ainsi que les autres paramètres anti-hameçonnage. Pour plus d’informations sur les paramètres anti-hameçonnage, voir [configurer les stratégies anti-hameçonnage d’Office 365](https://support.office.com/article/set-up-office-365-atp-anti-phishing-policies-5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578?ui=en-US&amp;rs=en-US&amp;ad=US#phishpolicyoptions).
  
Office 365 inclut la protection anti-usurpation par défaut qui est toujours en cours d’exécution. Cette protection par défaut n’est pas visible dans la sécurité &amp; centre de conformité ou récupérable par le biais des applets de commande Windows PowerShell. Vous ne pouvez pas modifier la protection anti-l’usurpation d’identité par défaut. Au lieu de cela, vous pouvez configurer la façon dont Office 365 applique la protection anti-l’usurpation d’identité de chaque stratégie anti-hameçonnage que vous créez. 
  
Même si la stratégie de l’usurpation d’identité contre apparaît sous la stratégie anti-hameçonnage dans la sécurité &amp; centre de conformité, il n’hérite pas son comportement par défaut de l’hameçonnage existante sous la configuration de blocage du courrier indésirable. Si vous avez des paramètres de **blocage du courrier indésirable** \> **hameçonnage** que vous souhaitez répliquer anti-l’usurpation d’identité, vous devez créer une stratégie anti-hameçonnage, puis sur Modifier la partie de l’usurpation d’identité de la stratégie anti-hameçonnage pour refléter vos paramètres d’usurpation d’identité décrit dans la section suivante, au lieu d’accepter les paramètres par défaut qui s’exécutent en arrière-plan. 
  
 **Pour configurer l’usurpation d’identité contre la protection d’une stratégie anti-hameçonnage à l’aide de la sécurité &amp; centre de conformité**
  
1. Accédez à la [sécurité &amp; centre de conformité](https://protection.office.com).
    
2. Connectez-vous à Office 365 avec votre compte professionnel ou de l’école. Votre compte doit disposer des informations d’identification d’administrateur de votre organisation Office 365.
    
3. Dans la sécurité &amp; centre de conformité, développez **Threat Management** \> **stratégie** \> **Anti-hameçonnage**. 
    
4. Dans la page **Anti-hameçonnage** dans le volet droit, sélectionnez la stratégie anti-hameçonnage que vous souhaitez configurer. 
    
5. Dans la page qui s’affiche, dans la ligne de **l’usurpation d’identité** , choisissez **Modifier**. 
    
6. Ensuite, configurez les actions à effectuer lorsqu’un message est identifié comme une usurpation d’identité inter-domaines. Le comportement par défaut consiste à déplacer le message vers le dossier de courrier indésirable du destinataire. L’autre option consiste à envoyer le message en quarantaine. Pour plus d’informations sur la gestion des messages mis en quarantaine, voir les [messages électroniques de mise en quarantaine dans Office 365](quarantine-email-messages.md).
  
![](media/7a868dff-2c4b-46b9-88ca-f2d523ca2307.jpg)(
  
7. Indiquez si vous souhaitez activer ou désactiver l’usurpation d’identité contre les conseils de sécurité. Office 365 recommande l’activation de la pointe de sécurité de **l’authentification échoue** pour avertir les utilisateurs lorsqu’ils interagissent avec un expéditeur dont l’identité n’a pas pu être vérifiée. Office 365 recommande également d’activer l’info-bulle de sécurité pour une **authentification récupérable passes** les petits groupes d’utilisateurs, car ce Conseil de sécurité peut générer un grand nombre d’avertissements si l’utilisateur reçoit un courrier électronique provenant de sources légitimes, mais non authentifiés. 
  
![](media/1ed675c0-48c2-4587-a957-60eb68dc9628.jpg)
  
Faites votre choix, puis sélectionnez **Enregistrer**. 
    
## <a name="other-ways-to-manage-spoofing-and-phishing-with-office-365"></a>Autres méthodes pour gérer l’usurpation d’identité et l’hameçonnage avec Office 365
<a name="Managespooflist"> </a>

Être attentif à l’usurpation d’identité et l’hameçonnage protection. Voici les méthodes associées pour vérifier les expéditeurs l’usurpation d’identité de votre domaine et les empêcher d’endommager votre organisation :
  
- Vérifier l’état de la messagerie Exchange Online Protection usurpation d’identité dans le cadre de votre routine. Vous pouvez utiliser ce rapport souvent d’afficher et de gérer les expéditeurs usurpés. Pour plus d’informations, voir **rapport de messagerie usurpation d’identité** dans les [rapports de protection de messagerie utilisés dans Office 365 pour afficher les données sur les logiciels malveillants, le courrier indésirable et les détections de règle](https://technet.microsoft.com/library/dn500744%28v=exchg.150%29.aspx).
    
- Pour les administrateurs Office 365 plus avancées :
    
  - Passez en revue la configuration de votre infrastructure SPF (Sender Policy). Pour une présentation rapide pour SPF et pour obtenir une configuration rapidement, voir [Set up SPF dans Office 365 afin d’empêcher l’usurpation d’identité](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Pour une présentation plus approfondie de la façon dont Office 365 utilise SPF, ou pour les déploiements de résolution des problèmes ou non standard telles que les déploiements hybrides, démarrez avec la [façon dont Office 365 utilise Framework SPF (Sender Policy) pour empêcher l’usurpation d’identité](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).
    
  - Passez en revue votre configuration DomainKeys identifié DKIM (Mail). Vous devez utiliser DKIM outre SPF et DMARC pour éviter les questions d’envoyer des messages qui semblent provenir votre domaine. DKIM vous permet d’ajouter une signature numérique aux messages électroniques dans l’en-tête du message. Pour plus d’informations, voir [Utilisation DKIM pour valider le courrier sortant envoyé à partir de votre domaine dans Office 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).
    
  - Passez en revue votre configuration basée sur le domaine d’authentification de Message, de rapports et de conformité (DMARC). L’implémentation DMARC avec SPF et DKIM fournit une protection supplémentaire contre l’usurpation d’identité et l’hameçonnage de courrier électronique. Aide à DMARC les systèmes de messagerie destinataire déterminent comment traiter les messages envoyés à partir de votre domaine SPF échoue ou DKIM vérifie. Pour plus d’informations, voir [Utiliser DMARC pour valider le courrier dans Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
  - Utilisez l’applet de commande [Get-PhishFilterPolicy](https://technet.microsoft.com/en-us/library/mt735158%28v=exchg.160%29.aspx) Windows PowerShell pour recueillir des données détaillées sur les expéditeurs usurpés, générer autoriser, bloquer des listes et vous aident à déterminer comment générer des enregistrements SPF, DKIM et DMARC DNS plus complètes sans avoir votre courrier légitime obtenir capturés dans les filtres anti-spam externe. Pour plus d’informations, voir [comment fonctionne la protection antispoofing dans Office 365](https://blogs.msdn.microsoft.com/tzink/2016/02/23/how-antispoofing-protection-works-in-office-365/).
    

