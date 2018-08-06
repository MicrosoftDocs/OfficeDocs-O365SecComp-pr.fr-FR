---
title: Comment Office 365 utilise SPF (Sender Policy Framework) pour éviter l’usurpation
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/15/2016
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 3aff33c5-1416-4867-a23b-e0c0c5b4d2be
description: "Résumé : Cet article décrit comment Office 365 utilise l'enregistrement TXT SPF (Sender Policy Framework) dans le système DNS pour s'assurer que les systèmes de messagerie de destination approuvent les messages envoyés à partir de votre domaine personnalisé. Cela s'applique aux messages sortants envoyés à partir d'Office 365. Les messages envoyés à partir d'Office 365 à un destinataire d'Office 365 passent toujours par SPF."
ms.openlocfilehash: aea7f740a67ce282424efc409d25f3f135546ada
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026461"
---
# <a name="how-office-365-uses-sender-policy-framework-spf-to-prevent-spoofing"></a>Comment Office 365 utilise SPF (Sender Policy Framework) pour éviter l’usurpation

 **Résumé :** Cet article décrit comment Office 365 utilise l'enregistrement TXT SPF (Sender Policy Framework) dans le système DNS pour s'assurer que les systèmes de messagerie de destination approuvent les messages envoyés à partir de votre domaine personnalisé. Cela s'applique aux messages sortants envoyés à partir d'Office 365. Les messages envoyés à partir d'Office 365 à un destinataire d'Office 365 passent toujours par SPF. 
  
Un enregistrement TXT SPF est un enregistrement DNS qui permet d'éviter l' usurpation et le hameçonnage en vérifiant le nom du domaine à partir duquel les messages électroniques sont envoyés. SPF valide l'origine des messages électroniques en vérifiant l'adresse IP de l'expéditeur par rapport à celle du prétendu propriétaire du domaine d'expédition. 
  
> [!NOTE]
> Les types d'enregistrement SPF ont été déconseillés par le groupe de travail IETF (Internet Engineering Task Force) en 2014. À la place, veillez à utiliser des enregistrements TXT dans le système DNS pour publier vos informations SPF. Le reste de cet article utilise le terme « enregistrement TXT SPF » pour plus de clarté. 
  
Les administrateurs de domaine publient des informations SPF dans les enregistrements TXT au sein du système DNS. Les informations SPF identifient les serveurs de messagerie sortants autorisés. Les systèmes de messagerie électronique de destination vérifient que les messages proviennent de serveurs de messagerie sortants autorisés. Si vous êtes déjà familiarisé avec SPF ou si vous disposez d’un déploiement simple et que vous avez simplement besoin de connaître les éléments à inclure dans votre enregistrement TXT SPF au sein du système DNS pour Office 365, vous pouvez accéder à [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md). Si vous ne disposez pas d’un déploiement entièrement hébergé par Office 365, ou que vous souhaitez obtenir plus d’informations sur le fonctionnement de SPF ou sur la façon de dépanner SPF pour Office 365, poursuivez votre lecture.
  
> [!NOTE]
> Auparavant, vous deviez ajouter un autre enregistrement TXT SPF à votre domaine personnalisé si vous utilisiez également SharePoint Online. Cela n'est plus nécessaire. Ce changement doit réduire le risque que les messages de notification SharePoint Online terminent dans le dossier Courrier indésirable. Vous n’avez pas besoin d’apporter des modifications immédiatement, mais si vous recevez l’erreur « Trop de recherches », modifiez votre enregistrement TXT SPF comme décrit dans l’article [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md). 
     
## <a name="how-spf-works-to-prevent-spoofing-and-phishing-in-office-365"></a>Fonctionnement de SPF pour éviter l'usurpation et le hameçonnage dans Office 365
<a name="HowSPFWorks"> </a>

SPF détermine si un expéditeur est autorisé à envoyer des messages au nom d'un domaine. Si l'expéditeur n'y est pas autorisé, autrement dit, si la vérification SPF du message électronique échoue sur le serveur de réception, la stratégie de courrier indésirable configurée sur ce serveur détermine l'action à entreprendre avec le message.
  
Chaque enregistrement TXT SPF contient trois parties : la déclaration indiquant qu'il s'agit d'un enregistrement TXT SPF, les adresses IP qui sont autorisées à envoyer des messages à partir de votre domaine et les domaines externes pouvant envoyer des messages au nom de votre domaine, ainsi qu'une règle de mise en œuvre. Ces trois éléments sont obligatoires pour un enregistrement TXT SPF valide. Cet article décrit la façon dont vous devez créer votre enregistrement TXT SPF et fournit les meilleures pratiques pour utiliser ces services dans Office 365. Des liens vers des instructions sur l'utilisation de votre bureau d'enregistrement de domaine pour publier votre enregistrement dans DNS sont également disponibles.
  
### <a name="spf-basics-ip-addresses-allowed-to-send-from-your-custom-domain"></a>Concepts de base SPF : adresses IP autorisées à envoyer des messages à partir de votre domaine personnalisé
<a name="SPFBasicsIPaddresses"> </a>

Examinez la syntaxe de base pour une règle SPF :
  
v=spf1 \<IP\> \<règle de mise en œuvre\>
  
Par exemple, supposons que la règle SPF suivante existe pour contoso.com :
  
v=spf1 \<adresse IP 1\> \<adresse IP 2\> \<adresse IP 3\> \<règle de mise en œuvre\>
  
Dans cet exemple, la règle SPF demande au serveur de messagerie de réception d'accepter uniquement les messages provenant de ces adresses IP pour le domaine contoso.com :
  
- Adresse IP 1
    
- Adresse IP 2
    
- Adresse IP 3
    
Cette règle SPF indique au serveur de messagerie de réception que si un message provient de contoso.com, mais pas de l'une de ces trois adresses IP, le serveur de réception doit appliquer la règle de mise en œuvre au message. La règle de mise en œuvre est généralement l'une des options suivantes :
  
- **Échec sévère.** Marquez « échec sévère » dans l'enveloppe du message, puis suivez la stratégie de courrier indésirable configurée du serveur de réception pour ce type de message. 
    
- **Échec partiel.** Marquez « échec partiel » dans l'enveloppe du message. En règle générale, les serveurs de messagerie sont configurés pour remettre ce type de message. La plupart des utilisateurs finaux ne voient pas cette marque. 
    
- **Neutre.** Ne faites rien, autrement dit, ne marquez pas l'enveloppe du message. Cette marque est généralement réservée à des fins de test et est rarement utilisée. 
    
Les exemples suivants montrent comment SPF fonctionne dans plusieurs situations différentes. Dans ces exemples, contoso.com est l’expéditeur et woodgrovebank.com est le destinataire.
  
### <a name="example-1-email-authentication-of-a-message-sent-directly-from-sender-to-receiver"></a>Exemple 1 : authentification de messagerie d'un message envoyé directement de l'expéditeur au destinataire
<a name="spfExample1"> </a>

SPF fonctionne de manière optimale lorsque le chemin entre l'expéditeur et le destinataire est direct, par exemple :
  
![Diagramme illustrant comment SPF authentifie le courrier électronique lorsqu'il est envoyé directement d'un serveur à l'autre.](media/835c20a7-ed4c-49c4-91fe-b8ebb3e452a1.jpg)
  
Quand woodgrovebank.com reçoit le message, si l'adresse IP 1 se trouve dans l'enregistrement TXT SPF pour contoso.com, le message passe la vérification SPF et est authentifié.
  
### <a name="example-2-spoofed-sender-address-fails-the-spf-check"></a>Exemple 2 : l'adresse d'expéditeur falsifiée ne passe pas la vérification SPF
<a name="spfExample2"> </a>

Supposons qu'un auteur de hameçonnage trouve un moyen d'usurper contoso.com :
  
![Diagramme illustrant la façon dont SPF authentifie le courrier électronique envoyé à partir d'un serveur falsifié.](media/235dac3d-cdc5-466e-86e0-37b5979de198.jpg)
  
Étant donné que l'adresse IP 12 n'est pas dans l'enregistrement TXT SPF de contoso.com, le message ne passe pas la vérification SPF et le destinataire peut choisir de le marquer comme courrier indésirable.
  
### <a name="example-3-spf-and-forwarded-messages"></a>Exemple 3 : messages transférés et SPF
<a name="spfExample3"> </a>

SPF présente un désavantage qui réside dans le fait qu'il ne fonctionne pas lorsqu'un message électronique a été transféré. Par exemple, supposons que l'utilisateur woodgrovebank.com a défini une règle de transfert pour envoyer tous les messages électroniques vers un compte outlook.com :
  
![Diagramme indiquant comment SPF ne peut pas authentifier le courrier électronique lorsque le message est transféré.](media/6e92acd6-463e-4a1b-8327-fb1cf861f356.jpg)
  
Le message passe d'abord la vérification SPF sur woodgrovebank.com mais il échoue lors de la vérification SPF sur outlook.com, car l'adresse IP 25 ne figure pas dans l'enregistrement TXT SPF de contoso.com. Outlook.com peut ensuite marquer le message comme courrier indésirable. Pour contourner ce problème, utilisez SPF avec d'autres méthodes d'authentification de courrier électronique, comme DKIM et DMARC.
  
### <a name="spf-basics-including-third-party-domains-that-can-send-mail-on-behalf-of-your-domain"></a>Concepts de base SPF : intégration de domaines tiers pouvant envoyer des messages au nom de votre domaine
<a name="SPFBasicsIncludes"> </a>

En plus des adresses IP, vous pouvez également configurer votre enregistrement TXT SPF pour inclure des domaines en tant qu'expéditeurs. Ces domaines sont ajoutés à l'enregistrement TXT SPF comme des instructions « Include ». Par exemple, contoso.com souhaite peut-être inclure toutes les adresses IP des serveurs de messagerie à partir de contoso.net et de contoso.org qu'il possède également. Pour ce faire, contoso.com publie un enregistrement TXT SPF qui ressemble à ceci :
  
```
IN TXT "v=spf1 include:contoso.net include:contoso.org -all"
```

Lorsque le serveur de réception voit cet enregistrement dans le système DNS, il effectue également une recherche DNS sur l'enregistrement TXT SPF pour contoso.net, puis pour contoso.org. S'il trouve une instruction Include supplémentaire au sein des enregistrements pour contoso.net ou contoso.org, il la suivra également. Afin d'empêcher le refus d'attaque de service, le nombre maximal de recherches DNS pour un seul message est de 10. Chaque instruction Include représente une recherche DNS supplémentaire. Si un message dépasse la limite de 10, le message échoue lors de la vérification SPF. Une fois qu'un message atteint cette limite, selon la manière dont le serveur de réception est configuré, l'expéditeur peut recevoir un message indiquant que le message a généré « trop de recherches » ou que le « nombre maximal de sauts pour le message a été dépassé ». Pour savoir comment éviter cette situation, voir [Résolution des problèmes : Meilleures pratiques pour SPF dans Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).
  
## <a name="requirements-for-your-spf-txt-record-and-office-365"></a>Configuration requise pour votre enregistrement TXT SPF et Office 365
<a name="SPFReqsinO365"> </a>

Si vous avez configuré la messagerie lors de la configuration d'Office 365, vous avez déjà créé un enregistrement TXT SPF qui identifie les serveurs de messagerie Microsoft en tant que source légitime de messagerie pour votre domaine. Cet enregistrement ressemble probablement à ce qui suit :
  
```
v=spf1 include:spf.protection.outlook.com -all
```

Si vous êtes un client Office 365 entièrement hébergé, autrement dit, si vous n'avez aucun serveur de messagerie local qui envoie du courrier sortant, il s'agit du seul enregistrement TXT SPF que vous devez publier pour Office 365.
  
Si vous disposez d'un déploiement hybride (autrement dit, avec quelques boîtes aux lettres locales et d'autres hébergées dans Office 365), ou que vous êtes un client autonome Exchange Online Protection (EOP) (autrement dit, votre organisation utilise EOP pour protéger vos boîtes aux lettres locales), vous devez ajouter l'adresse IP sortante pour tous vos serveurs de messagerie Edge locaux à l'enregistrement TXT SPF dans DNS.
  
## <a name="form-your-spf-txt-record-for-office-365"></a>Formuler votre enregistrement TXT SPF pour Office 365
<a name="FormYourSPF"> </a>

Utilisez les informations de syntaxe de cet article afin de formuler l'enregistrement TXT SPF pour votre domaine personnalisé. Bien qu'il existe des options de syntaxe qui ne sont pas mentionnées ici, il s'agit des options les plus fréquemment utilisées. Une fois que vous avez formulé votre enregistrement, vous devez le mettre à jour auprès de votre bureau d'enregistrement de domaine.
  
Pour plus d'informations sur les domaines que vous devez inclure pour Office 365, voir [Enregistrements DNS externes pour Office 365](https://support.office.com/en-us/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US). Utilisez les [instructions pas à pas](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) pour mettre à jour les enregistrements SPF (TXT) dans votre bureau d'enregistrement de domaines. Si votre bureau d'enregistrement n'est pas répertorié, vous devez le contacter séparément pour savoir comment mettre à jour votre enregistrement. 
  
### <a name="spf-txt-record-syntax-for-office-365"></a>Syntaxe d'enregistrement TXT SPF pour Office 365
<a name="SPFSyntaxO365"> </a>

Un enregistrement TXT SPF standard pour Office 365 comporte la syntaxe suivante :
  
```
v=spf1 [<ip4>|<ip6>:<IP address>] [include:<domain name>] <enforcement rule>
```

Par exemple :
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 include:spf.protection.outlook.com -all
```

où :
  
- **v=spf1** est obligatoire. Cet élément définit l'enregistrement TXT en tant qu'enregistrement TXT SPF. 
    
- **IP4** indique que vous utilisez des adresses IP de version 4. **ip6** indique que vous utilisez des adresses IP de version 6. Si vous utilisez des adresses IP IPv6, remplacez **ip4** par **ip6** dans les exemples de cet article. Vous pouvez également spécifier des plages d'adresses IP à l'aide de la notation CIDR, par exemple **ip4:192.168.0.1/26**.
    
-  _IP address_ est l'adresse IP à ajouter à l'enregistrement TXT SPF. En règle générale, il s'agit de l'adresse IP du serveur de messagerie sortant pour votre organisation. Vous pouvez répertorier plusieurs serveurs de messagerie sortants. Pour plus d'informations, consultez la section [Exemple : enregistrement TXT SPF pour plusieurs serveurs de messagerie locaux sortants et Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#ExampleSPFMultipleMailServerO365).
    
-  _domain name_ est le domaine que vous souhaitez ajouter en tant qu'expéditeur légitime. Pour obtenir la liste de noms de domaine que vous devez inclure pour Office 365, voir [Enregistrements DNS externes pour Office 365](https://support.office.com/en-us/article/External-Domain-Name-System-records-for-Office-365-c0531a6f-9e25-4f2d-ad0e-a70bfef09ac0?ui=en-US&amp;rs=en-US&amp;ad=US).
    
- La règle de mise en œuvre est généralement l'une des règles suivantes :
    
  - -all
    
    Indique un échec sévère. Si vous connaissez toutes les adresses IP autorisées pour votre domaine, répertoriez-les dans l’enregistrement TXT SPF et utilisez le qualificateur -all (échec sévère). En outre, si vous utilisez uniquement SPF, c’est-à-dire que vous n’utilisez pas DMARC ou DKIM, vous devez utiliser le qualificateur -all. Nous vous recommandons de toujours utiliser ce qualificateur.
    
  - ~all
    
    Indique un échec partiel. Si vous n'êtes pas sûr de disposer de la liste complète des adresses IP, utilisez le qualificateur ~all (échec partiel). En outre, si vous utilisez DMARC avec p=quarantine ou p=reject, vous pouvez utiliser ~all. Dans le cas contraire, utilisez -all.
    
  - ?all
    
    Indique un résultat neutre. Il est utilisé lors des essais SPF. Nous vous déconseillons d’utiliser ce qualificatif dans votre déploiement.
    
### <a name="example-spf-txt-record-to-use-when-all-of-your-mail-is-sent-by-office-365"></a>Exemple : enregistrement TXT SPF à utiliser quand tous vos messages sont envoyés par Office 365
<a name="ExampleSPFNoSP"> </a>

Si tous vos messages sont envoyés par Office 365, utilisez les indications suivantes dans votre enregistrement TXT SPF :
  
```
v=spf1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-a-hybrid-scenario-with-one-on-premises-exchange-server-and-office-365"></a>Exemple : enregistrement TXT SPF pour un scénario hybride avec un serveur Exchange local et Office 365
<a name="ExampleSPFHybridOneExchangeServer"> </a>

Dans un environnement hybride, si l'adresse IP du serveur Exchange local est 192.168.0.1, afin de définir la règle de mise en œuvre SPF sur échec sévère, formez l'enregistrement TXT SPF comme suit :
  
```
v=spf1 ip4:192.168.0.1 include:spf.protection.outlook.com -all
```

### <a name="example-spf-txt-record-for-multiple-outbound-on-premises-mail-servers-and-office-365"></a>Exemple : enregistrement TXT SPF pour plusieurs serveurs de messagerie locaux sortants et Office 365
<a name="ExampleSPFMultipleMailServerO365"> </a>

Si vous avez plusieurs serveurs de messagerie sortants, ajoutez l'adresse IP de chaque serveur de messagerie dans l'enregistrement TXT SPF et séparez chaque adresse IP par un espace suivi par une instruction « ip4: ». Par exemple :
  
```
v=spf1 ip4:192.168.0.1 ip4:192.168.0.2 ip4:192.168.0.3 include:spf.protection.outlook.com -all
```

## <a name="next-steps-set-up-spf-for-office-365"></a>Étapes suivantes : configurer SPF pour Office 365
<a name="SPFNextSteps"> </a>

Une fois que vous avez formulé votre enregistrement TXT SPF, suivez la procédure décrite dans l’article [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) pour l’ajouter à votre domaine. 
  
Bien que SPF soit conçu pour éviter l'usurpation, il existe des techniques d'usurpation contre lesquelles SPF ne peut pas vous protéger. Afin de vous protéger contre ces techniques, une fois que vous avez configuré SPF, vous devez également configurer DKIM et DMARC pour Office 365. Consultez [Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md) pour commencer. Ensuite, consultez la rubrique [Utiliser DMARC pour valider les e-mails dans Office 365](use-dmarc-to-validate-email.md).
  
## <a name="troubleshooting-best-practices-for-spf-in-office-365"></a>Résolution des problèmes : Meilleures pratiques pour SPF dans Office 365
<a name="SPFTroubleshoot"> </a>

Vous ne pouvez créer qu'un seul enregistrement TXT SPF pour votre domaine personnalisé. La création de plusieurs enregistrements entraîne une situation alternée et l'échec de SPF. Pour éviter cela, vous pouvez créer des enregistrements distincts pour chaque sous-domaine. Par exemple, créez un enregistrement pour contoso.com et un autre enregistrement pour bulkmail.contoso.com.
  
Si un message électronique provoque plus de 10 recherches DNS avant sa livraison, le serveur de messagerie de réception répond avec une erreur permanente, également appelée  _permerror_, et génère l'échec du message lors de la vérification SPF. Le serveur de réception peut également répondre avec une notification d'échec de remise qui contient une erreur semblable à celles-ci :
  
- Le message a dépassé le nombre de sauts.
    
- Le message a demandé trop de recherches.
    
## <a name="avoiding-the-too-many-lookups-error-when-you-use-third-party-domains-with-office-365"></a>Éviter l'erreur « Trop de recherches » lorsque vous utilisez des domaines tiers avec Office 365
<a name="SPFTroubleshoot"> </a>

Certains enregistrements TXT SPF pour les domaines tiers indiquent au serveur de réception d'effectuer un nombre élevé de recherches DNS. Par exemple, au moment de la rédaction, Salesforce.com contient 5 instructions Include dans son enregistrement :
  
```
v=spf1 include:_spf.google.com
include:_spfblock.salesforce.com
include:_qa.salesforce.com
include:_spfblock1.salesforce.com
include:spf.mandrillapp.com mx ~all
```

Pour éviter l’erreur, vous pouvez implémenter une stratégie selon laquelle toute personne envoyant des messages électroniques en bloc, par exemple, doit utiliser un sous-domaine spécialement à cette fin. Ensuite, définissez un autre enregistrement TXT SPF pour le sous-domaine comprenant la messagerie électronique en bloc.
  
 Dans certains cas, comme dans l'exemple salesforce.com, vous devez utiliser le domaine dans votre enregistrement TXT SPF, mais dans d'autres cas, le domaine tiers a peut-être déjà créé un sous-domaine pour votre utilisation. Par exemple, exacttarget.com a créé un sous-domaine que vous devez utiliser pour votre enregistrement TXT SPF : 
  
```
cust-spf.exacttarget.com
```

Lorsque vous incluez des domaines tiers dans votre enregistrement TXT SPF, vous devez vérifier auprès du tiers le domaine ou le sous-domaine à utiliser pour éviter d'atteindre la limite de 10 recherches.
  
## <a name="how-to-view-your-current-spf-txt-record-and-determine-the-number-of-lookups-that-it-requires"></a>Comment afficher votre enregistrement TXT SPF et déterminer le nombre de recherches nécessaires
<a name="SPFTroubleshoot"> </a>

Vous pouvez utiliser nslookup pour afficher vos enregistrements DNS, y compris votre enregistrement TXT SPF. Sinon, si vous préférez, il existe plusieurs outils gratuits en ligne que vous pouvez utiliser pour afficher le contenu de votre enregistrement TXT SPF. En consultant votre enregistrement TXT SPF et en suivant la chaîne d'instructions Include et de redirections, vous pouvez déterminer le nombre de recherches DNS dont l'enregistrement a besoin. Certains outils en ligne peuvent même compter et afficher ces recherches pour vous. Le fait d'assurer le suivi de cette donnée permettra d'éviter que les messages envoyés depuis votre organisation ne déclenchent une erreur permanente, appelée permerror, sur le serveur de réception.
  
## <a name="for-more-information"></a>Pour plus d'informations
<a name="SPFTroubleshoot"> </a>

Besoin d'aide pour ajouter l'enregistrement TXT SPF ? Des [instructions pas à pas](https://office.microsoft.com/en-us/office365-suite-help/create-dns-records-for-office-365-HA102851099.aspx?CTT=5&amp;origin=HA102818404) sont disponibles pour mettre à jour les enregistrements SPF (TXT) dans divers bureaux d'enregistrement de domaines courants. Les [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md) incluent la syntaxe et les champs d'en-tête utilisés par Office 365 pour les vérifications SPF. 
  

