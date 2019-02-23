---
title: En savoir plus sur l’usurpation d’identité
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/22/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 978c3173-3578-4286-aaf4-8a10951978bf
description: Utilisez l'Assistant usurpation d'identité &amp; dans le centre de sécurité conformité de la page Paramètres anti-courrier indésirable pour examiner tous les expéditeurs qui usurpent l'identité des domaines qui font partie de votre organisation ou qui usurpent des domaines externes. L'intelligence d'usurpation d'identité est disponible dans le cadre d'Office 365 entreprise E5 ou séparément dans le cadre de la protection avancée contre les menaces et d'Exchange Online Protection.
ms.openlocfilehash: b8c791dc47198fa0da08dec1de6fdab8ebfbdb32
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214822"
---
# <a name="learn-more-about-spoof-intelligence"></a>En savoir plus sur l’usurpation d’identité

Utilisez l'Assistant usurpation d'identité &amp; dans le centre de sécurité conformité de la **page Paramètres anti-courrier** indésirable pour examiner tous les expéditeurs qui usurpent l'identité des domaines qui font partie de votre organisation ou qui usurpent des domaines externes. La fonctionnalité d'usurpation d'identité est disponible dans le cadre d'Office 365 entreprise E5 ou séparément dans le cadre de la protection avancée contre les menaces (ATP) et depuis octobre, 2018 Exchange Online Protection (EOP). 
  
## <a name="what-types-of-email-spoofing-can-i-review-and-which-should-i-protect-against-with-spoof-intelligence"></a>Quels types d'usurpation d'identité de courriers électroniques puis-je vérifier par rapport à l'aide d'usurpation d'identité?

Pour les domaines que vous possédez, vous pouvez vérifier les expéditeurs qui usurpent votre domaine, puis choisir d'autoriser l'expéditeur à continuer ou à bloquer l'expéditeur. Pour les domaines externes, vous pouvez autoriser le domaine de l'expéditeur associé à l'infrastructure d'envoi, bien qu'il ne s'agisse pas d'une adresse de messagerie d'envoi individuelle.
  
Lorsqu'un expéditeur usurpe une adresse de messagerie, il semble envoyer des courriers électroniques pour le compte d'un ou de plusieurs comptes d'utilisateur dans l'un des domaines de votre organisation ou un domaine externe qui envoie des messages à votre organisation. Étonnamment, il existe des raisons d'usurpation légitimes. Par exemple, dans ce cas, vous n'empêchez pas l'expéditeur d'usurper votre domaine:
  
- Vous avez des expéditeurs tiers qui utilisent votre domaine pour envoyer du courrier en nombre à vos employés pour les sondages de la société.
    
- Vous avez embauché une société externe pour générer et envoyer des mises à jour de publicités ou de produits en votre nom.
    
- Assistant qui doit régulièrement envoyer un courrier électronique à une autre personne au sein de votre organisation.
    
- Application configurée pour usurper sa propre organisation afin d'envoyer des notifications internes par courrier électronique.
    
Les domaines externes envoient fréquemment des courriers falsifiés, et bon nombre de ces raisons sont légitimes. Par exemple, voici quelques cas légitimes où les expéditeurs externes envoient des messages falsifiés:
  
- L'expéditeur figure dans une liste de distribution de discussion et la liste de publipostage relaie le courrier électronique de l'expéditeur d'origine à tous les participants de la liste de distribution.
    
- Une société externe envoie des courriers électroniques au nom d'une autre société (par exemple, un rapport automatisé, ou une société de logiciels en tant que service).
    
Vous avez besoin d'un moyen pour vous assurer que le courrier électronique envoyé par des usurpateurs légitimes ne se trouve pas dans des filtres de courrier indésirable dans Office 365 ou des systèmes de messagerie externes. Normalement, Office 365 traite ces messages électroniques comme du courrier indésirable. En tant qu'administrateur Office 365, vous pouvez éviter cela en configurant des filtres d'usurpation dans le centre &amp; de sécurité conformité. Si vous êtes propriétaire du domaine, vous pouvez configurer SPF, DKIM et DMARC pour autoriser ces expéditeurs.
  
En revanche, les usurpateurs malveillants, ceux qui usurpent votre domaine ou des domaines externes, d'envoyer du courrier indésirable ou du hameçonnage, doivent être bloqués. L'usurpation est également un moyen courant pour les auteurs de phishing d'obtenir des informations d'identification de l'utilisateur. Office 365 offre une protection contre les falsifications intégrée pour vous aider à protéger votre organisation contre les expéditeurs de ces messages malveillants. La protection contre les usurpations pour les domaines de votre organisation est toujours active pour tous les clients Office 365, et la protection contre les attaques par usurpation de domaine externe est activée par défaut pour les clients de protection avancée contre les menaces et depuis octobre, les clients EOP de 2018. Pour renforcer encore cette protection, dites aux expéditeurs d'être autorisés à usurper les domaines de votre organisation et à envoyer des courriers électroniques en votre nom, et si des domaines externes sont autorisés à usurper. Tout message électronique envoyé par un expéditeur que vous n'autorisez pas est traité comme du courrier indésirable ou une usurpation d'identité par Office 365. Gardez un oeil sur les expéditeurs qui usurpent votre domaine et aidez-nous à améliorer l'aide aux &amp; usurpations à l'aide du centre de sécurité conformité.
  
## <a name="managing-spoof-intelligence-in-the-security-amp-compliance-center"></a>Gestion des usurpations d'identité &amp; dans le centre de sécurité conformité
<a name="Managespooflist"> </a>

La stratégie d'aide à la décision que vous configurez est toujours appliquée par Office 365. Vous ne pouvez pas le désactiver, mais vous pouvez choisir le niveau de gestion de votre choix.
  
Vous pouvez vérifier les expéditeurs qui usurpent votre domaine, ou des domaines externes, puis décider si chaque expéditeur doit être autorisé à le faire à l'aide du centre de &amp; sécurité conformité. Pour chaque compte d'utilisateur usurpé qu'un expéditeur usurpe à partir de votre domaine ou d'un domaine externe, vous pouvez afficher les informations dans le tableau suivant.
  
|**Paramètre**|**Description**|
|:-----|:-----|
|Expéditeur  <br/> |Également appelé véritable expéditeur. Il s'agit généralement du domaine à l'origine de l'usurpation du courrier électronique. Office 365 détermine le domaine de l'enregistrement DNS du pointeur (PTR) de l'adresse IP d'envoi qui usurpe l'identité de votre organisation. Si aucun domaine n'est trouvé, le rapport affiche à la place l'adresse IP de l'expéditeur.  <br/> |
|Utilisateur usurpé  <br/> |Le compte d'utilisateur qui est usurpé par l'expéditeur.  <br/> Onglet **interne** uniquement. Ce champ contient une adresse de messagerie unique, ou si l'expéditeur usurpe plusieurs comptes d'utilisateur, il en contient **plusieurs**.<br/> Onglet **externe** uniquement. Les domaines externes contiennent uniquement un domaine d'envoi et ne contiennent pas d'adresse de messagerie complète.<br/> **Conseil! Pour les administrateurs avancés.** L'utilisateur usurpé est l'adresse de (5322. from) qui est également l'adresse de l'expéditeur par le client de messagerie. Il s'agit parfois de l'adresse d'en-tête. from. La validité de cette adresse n'est pas vérifiée par SPF.           |
|Nombre de messages  <br/> |Nombre de messages électroniques envoyés par l'expéditeur à votre organisation pour le compte de l'expéditeur ou des expéditeurs usurpés identifiés au cours des 30 derniers jours.  <br/> |
|Nombre de plaintes de l'utilisateur  <br/> |Plaintes envoyées par des utilisateurs à l'expéditeur par vos utilisateurs au cours des 30 derniers jours. Les plaintes se présentent généralement sous la forme d'envois de courrier indésirable à Microsoft.  <br/> |
|Résultat de l'authentification  <br/> |Cette valeur est **transmise** si les vérifications d'authentification d'expéditeurs Exchange Online Protection (EoP) transmises par l'expéditeur, comme SPF ou DKIM, **ont échoué** si l'expéditeur a échoué à la vérification de l'authentification de l'expéditeur EOP, ou Unknown si le résultat de ces contrôles n'est pas **** connus.  <br/> |
|Décision définie par  <br/> |Indique si l'administrateur d'Office 365 ou la stratégie d'aide à la décision a déterminé si l'expéditeur est autorisé ou non à usurper l'identité de l'utilisateur.  <br/> |
|Dernière vue  <br/> |Dernière date à laquelle un message a été reçu par cet expéditeur au nom de cet utilisateur usurpé.  <br/> |
|Autorisé à usurper?  <br/> | Indique si cet expéditeur est autorisé à envoyer des courriers électroniques au nom de l'utilisateur usurpé. Les valeurs possibles sont les suivantes:<br/> **Valeur Oui** Toutes les adresses usurpées de cet expéditeur d'usurpation d'identité seront autorisées à usurper votre organisation.  <br/> **Non** Les adresses usurpées de cet expéditeur d'usurpation d'identité ne seront pas autorisées à usurper votre organisation. Au lieu de cela, les messages provenant de cet expéditeur seront marqués comme courrier indésirable par Office 365.<br/> **Certains utilisateurs** Si un expéditeur usurpe l'identité de plusieurs utilisateurs, certaines adresses usurpées de cet expéditeur seront autorisées à usurper votre organisation, le reste sera marqué comme courrier indésirable. Utilisez l'onglet **détaillé** pour afficher les adresses spécifiques.<br/> |
|Type d'usurpation  <br/> |Cette valeur est **interne** si le domaine est l'un des domaines configurés de votre organisation, sinon la valeur est **externe**.  <br/> |
   
 **Pour gérer les expéditeurs qui usurpent votre domaine à l'aide du &amp; Centre de sécurité conformité**
  
1. Accédez au [Centre de &amp; sécurité conformité](https://protection.office.com).
    
2. Connectez-vous à Office 365 avec votre compte professionnel ou scolaire. Votre compte doit disposer d'informations d'identification d'administrateur dans votre organisation Office 365.
    
3. Dans le centre &amp; de sécurité conformité, développez **protection contre le courrier**indésirable de la **stratégie** \> de **gestion** \> des menaces.  
  
    ![Capture d'écran illustrant l'accès à la page de blocage du courrier indésirable](media/0a098e68-5ecf-40d7-984f-d15fcc1f958d.jpg)
  
4. Sur la page **paramètres de blocage du courrier** indésirable dans le volet droit, sélectionnez l'onglet **personnalisé** , puis faites défiler la liste vers le bas et développez stratégie d'aide à la **décision**.  
  
    ![Capture d'écran illustrant l'accès aux paramètres personnalisés de blocage du courrier indésirable](media/a5112100-0b37-460f-932d-5b2f98157871.jpg)
  
5. Pour afficher la liste des expéditeurs qui usurpent votre domaine, choisissez **examiner les nouveaux expéditeurs** , puis sélectionnez l'onglet **vos domaines** . 
    
    Si vous avez déjà vérifié les expéditeurs et que vous souhaitez modifier certains de vos choix précédents, vous pouvez choisir **afficher les expéditeurs que j'ai déjà examinés** . Dans les deux cas, le panneau suivant s'affiche.  
  
    ![Capture d'écran illustrant l'accès à l'onglet des expéditeurs usurpés](media/c0c062fd-f4a4-4d78-96f7-2c22009052bb.jpg)
  
    Chaque utilisateur usurpé est affiché sur une ligne distincte de sorte que vous pouvez choisir d'autoriser ou d'empêcher l'expéditeur d'usurper chaque utilisateur individuellement.  
  
    Pour ajouter un expéditeur à la liste verte pour un utilisateur, sélectionnez **Oui** dans la colonne **autorisé à usurper** . Pour ajouter un expéditeur à la liste rouge pour un utilisateur, choisissez **non**.
     
    Pour définir la stratégie pour les domaines dont vous n'êtes pas propriétaire, sélectionnez l'onglet **domaines externes** . Remplacez un expéditeur par **Oui** dans la colonne **autorisé à usurper** pour autoriser cet expéditeur à envoyer un message électronique non authentifié à votre organisation. Par ailleurs, si vous pensez qu'Office 365 a commis une erreur en autorisant l'expéditeur à envoyer un message électronique usurpé, définissez la colonne **autorisé à usurper** sur **non**.  
  
    ![Capture d'écran indiquant si un expéditeur est autorisé à usurper](media/5dbef9cf-103f-49cd-9638-4b0083d6baa7.jpg)
  
6. Sélectionnez **Enregistrer** pour enregistrer les modifications. 

Si vous disposez d'un abonnement Office 365 entreprise E5 ou si la protection avancée contre les menaces est achetée séparément en tant que module complémentaire, vous pouvez également gérer les expéditeurs qui usurpent votre domaine via la fonction d'aide à la [décision](https://docs.microsoft.com/en-us/office365/securitycompliance/walkthrough-spoof-intelligence-insight).
    
## <a name="configuring-the-anti-spoofing-policy"></a>Configuration de la stratégie d'usurpation d'identité
<a name="Managespooflist"> </a>

En plus d'autoriser ou de bloquer l'envoi de courrier falsifié à un expéditeur particulier dans votre organisation, vous pouvez également configurer le degré de rigueur souhaité pour le filtre et l'action à effectuer lorsqu'un message d'usurpation est trouvé.
  
La protection contre l'usurpation d'identité est appliquée aux messages provenant d'expéditeurs provenant de domaines externes à votre organisation Office 365. Vous pouvez appliquer la stratégie aux destinataires dont les boîtes aux lettres sont détenteurs d'une licence pour Office 365 entreprise E5, protection avancée contre les menaces et depuis octobre, 2018 clients EOP. Vous gérez la stratégie d'usurpation d'identité, ainsi que les autres paramètres anti-hameçonnage. Pour plus d'informations sur les paramètres anti-hameçonnage, consultez [la rubrique Configurer les stratégies anti-hameçonnage Office 365](https://support.office.com/article/set-up-office-365-atp-anti-phishing-policies-5a6f2d7f-d998-4f31-b4f5-f7cbf6f38578?ui=en-US&amp;rs=en-US&amp;ad=US#phishpolicyoptions).
  
Office 365 inclut une protection contre l'usurpation d'identité par défaut qui est toujours en cours d'exécution. Cette protection par défaut n'est pas visible dans &amp; le centre de sécurité conformité ou des applets de commande Windows PowerShell. Vous ne pouvez pas modifier la protection contre l'usurpation d'identité par défaut. Au lieu de cela, vous pouvez configurer la façon dont Office 365 applique la protection contre l'usurpation d'identité dans chaque stratégie anti-hameçonnage que vous créez. 
  
Même si la stratégie d'usurpation d'identité apparaît sous la stratégie anti-hameçonnage dans le centre de &amp; sécurité conformité, elle n'hérite pas du comportement par défaut du paramètre d'hameçonnage existant dans la configuration anti-courrier indésirable. Si vous avez des paramètres sous **hameçonnage** de **blocage du courrier** \> indésirable que vous souhaitez répliquer contre l'usurpation d'identité, vous devez créer une stratégie anti-hameçonnage, puis modifier la partie d'usurpation de la stratégie anti-hameçonnage en fonction de vos paramètres d'usurpation d'identité décrit dans la section suivante, au lieu d'accepter les paramètres par défaut qui s'exécutent en arrière-plan. 
  
 **Pour configurer la protection contre l'usurpation d'identité dans une stratégie anti-hameçonnage à l'aide &amp; du centre de sécurité conformité**
  
1. Accédez au [Centre de &amp; sécurité conformité](https://protection.office.com).
    
2. Connectez-vous à Office 365 avec votre compte professionnel ou scolaire. Votre compte doit disposer d'informations d'identification d'administrateur dans votre organisation Office 365.
    
3. Dans le centre &amp; de sécurité conformité, développez **protection contre le hameçonnage**de la **stratégie** \> de **gestion** \> des menaces. 
    
4. Sur la page **anti-hameçonnage** dans le volet droit, sélectionnez la stratégie anti-hameçonnage que vous souhaitez configurer. 
    
5. Sur la page qui s'affiche, dans la ligne **frauduleux** , sélectionnez **modifier**. 
    
6. Ensuite, configurez les actions à effectuer lorsqu'un message est détecté comme usurpateur de domaine. Le comportement par défaut consiste à déplacer le message vers le dossier de courrier indésirable du destinataire. L'autre option consiste à envoyer le message en quarantaine. Pour plus d'informations sur la gestion des messages envoyés en quarantaine, consultez la rubrique [mise en quarantaine des messages électroniques dans Office 365](quarantine-email-messages.md).  
  
    ![Capture d'écran montrant les options d'édition d'une stratégie d'usurpation d'identité](media/7a868dff-2c4b-46b9-88ca-f2d523ca2307.jpg)
  
7. Faites votre choix, puis cliquez sur **Enregistrer**. 
    
## <a name="other-ways-to-manage-spoofing-and-phishing-with-office-365"></a>Autres façons de gérer l'usurpation d'identité et le hameçonnage avec Office 365
<a name="Managespooflist"> </a>

Soyez très à la protection contre l'usurpation d'identité et la protection antiphishing. Voici des méthodes relatives pour vérifier les expéditeurs qui usurpent votre domaine et les empêcher d'endommager votre organisation:
  
- Consultez le rapport usurpation de courrier Exchange Online protection dans le cadre de votre routine. Vous pouvez utiliser ce rapport fréquemment pour afficher et gérer les expéditeurs usurpés. Pour plus d'informations, reportez-vous à la rubrique **usurpation de courrier électronique** dans [use mail protection reports in Office 365 pour afficher les données sur les programmes malveillants, le courrier indésirable et les menaces](https://technet.microsoft.com/library/dn500744%28v=exchg.150%29.aspx)
    
Pour les administrateurs Office 365 plus avancés, vous pouvez également effectuer les vérifications suivantes:
    
    
- Passez en revue votre configuration SPF (Sender Policy Framework). Pour une présentation rapide de SPF et pour qu'il soit configuré rapidement, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l'usurpation](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Pour mieux comprendre comment Office 365 utilise SPF, ou pour résoudre des problèmes ou des déploiements non standard tels que des déploiements hybrides, commencez par [Comment office 365 utilise SPF (Sender Policy Framework) pour éviter l'usurpation](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).
    
- Passez en revue votre configuration DKIM (DomainKeys Identified Identified Mail). Vous devez utiliser DKIM en plus de SPF et de DMARC pour empêcher les usurpateurs d'envoyer des messages qui semblent provenir de votre domaine. DKIM vous permet d'ajouter une signature numérique aux messages électroniques dans l'en-tête du message. Pour plus d'informations, consultez [la rubrique use DKIM pour valider les messages sortants envoyés à partir de votre domaine dans Office 365](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).
    
- Passez en revue votre configuration d'authentification de message basée sur un domaine, de création de rapports et de conformité (DMARC). L'implémentation de DMARC avec SPF et DKIM offre une protection supplémentaire contre l'usurpation et le courrier électronique de hameçonnage. DMARC permet de recevoir des systèmes de messagerie qui déterminent la marche à suivre pour les messages envoyés à partir de votre domaine et qui échouent aux contrôles SPF ou DKIM. Pour plus d'informations, consultez la rubrique [utiliser DMARC pour valider le courrier électronique dans Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
- Utilisez l'applet de commande Windows PowerShell [Get-PhishFilterPolicy](https://technet.microsoft.com/en-us/library/mt735158%28v=exchg.160%29.aspx) pour collecter des données détaillées sur des expéditeurs usurpés, générer des listes verte et rouge et vous aider à déterminer comment générer des enregistrements DNS SPF, DKIM et DMARC plus complets sans avoir besoin de votre courrier légitime les filtres de courrier indésirable externes sont détectés. Pour plus d'informations, consultez la rubrique fonctionnement [de la protection contre l'usurpation d'identité dans Office 365](https://blogs.msdn.microsoft.com/tzink/2016/02/23/how-antispoofing-protection-works-in-office-365/).
    

