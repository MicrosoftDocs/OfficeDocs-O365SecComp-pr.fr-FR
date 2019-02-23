---
title: Utiliser DMARC pour valider les e-mails dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.custom: TN2DMC
ms.assetid: 4a05898c-b8e4-4eab-bd70-ee912e349737
description: Découvrez comment configurer l'authentification de message basée sur un domaine, la création de rapports et la conformité (DMARC) pour valider les messages envoyés à partir de votre organisation Office 365.
ms.openlocfilehash: f96fbe147a14087ee86bca2b9fae04d281ccdbec
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223723"
---
# <a name="use-dmarc-to-validate-email-in-office-365"></a>Utiliser DMARC pour valider les e-mails dans Office 365

L'authentification de message basée sur un domaine, la création de rapports et la conformité ([DMARC](https://dmarc.org)) fonctionne avec SPF (Sender Policy Framework) et DomainKeys Identified Identified Mail (DKIM) pour authentifier les expéditeurs de messages et s'assurer que les systèmes de messagerie de destination approuvent les messages envoyés à partir de votre domaine. L'implémentation de DMARC avec SPF et DKIM offre une protection supplémentaire contre l'usurpation et le courrier électronique de hameçonnage. DMARC permet de recevoir des systèmes de messagerie qui déterminent la marche à suivre pour les messages envoyés à partir de votre domaine et qui échouent aux contrôles SPF ou DKIM.
  
## <a name="how-do-spf-and-dmarc-work-together-to-protect-email-in-office-365"></a>Comment SPF et DMARC fonctionnent-ils ensemble pour protéger les messages électroniques dans Office 365 ?
<a name="SPFandDMARC"> </a>

 Un message électronique peut contenir plusieurs adresses d'origine (ou d'expéditeur). Ces adresses sont utilisées à des fins différentes. Par exemple, prenez les adresses suivantes : 
  
- **Adresse «mail from»**: identifie l'expéditeur et spécifie l'emplacement où envoyer des notifications de retour si un problème se produit avec la remise du message, comme des notifications d'échec de remise. Il apparaît dans la partie enveloppe d'un message électronique et n'est généralement pas affiché par votre application de messagerie. Il s'agit parfois de l'adresse 5321. MailFrom ou de l'adresse de chemin inverse.
    
- **Adresse**de l'expéditeur: adresse de l'expéditeur par votre application de messagerie. Cette adresse identifie l'auteur du message. C'est-à-dire, la boîte aux lettres de la personne ou du système responsable de l'écriture du message. Il s'agit parfois de l'adresse 5322. from.
    
SPF utilise un enregistrement TXT DNS pour fournir la liste des adresses IP d'envoi autorisées pour un domaine donné. En règle générale, les vérifications SPF sont uniquement effectuées pour l'adresse 5321.MailFrom. Cela signifie que l'adresse 5322.From n'est pas authentifiée lorsque vous utilisez uniquement SPF. Vous pouvez ainsi vous retrouver dans le cas de figure où un utilisateur reçoit un message qui a été accepté par la vérification SPF mais possède une adresse d'expéditeur 5322.From usurpée. Prenez par exemple, la transcription SMTP suivante :
  
```
S: Helo woodgrovebank.com
S: Mail from: phish@phishing.contoso.com
S: Rcpt to: astobes@tailspintoys.com
S: data
S: To: "Andrew Stobes" <astobes@tailspintoys.com>
S: From: "Woodgrove Bank Security" <security@woodgrovebank.com>
S: Subject: Woodgrove Bank - Action required
S:
S: Greetings User,
S: 
S: We need to verify your banking details.
S: Please click the following link to verify that we have the right information for your account.
S: 
S: http://short.url/woodgrovebank/updateaccount/12-121.aspx
S:
S: Thank you,
S: Woodgrove Bank
S: .
```

Dans cette transcription, les adresses de l'expéditeur sont les suivantes :
  
- Adresse « Mail from » (5321.MailFrom) : phish@phishing.contoso.com
    
- Adresse From (5322.From) : security@woodgrovebank.com
    
Si vous avez configuré SPF, le serveur de réception effectue une vérification sur l’adresse Mail from phish@phishing.contoso.com. Si l’e-mail provenait d’une source valide pour le domaine phishing.contoso.com, le contrôle SPF accepte le message. Étant donné que le client de messagerie affiche uniquement l’adresse From, l’utilisateur voit que ce message provenait de security@woodgrovebank.com. Avec SPF seul, la validité de l’adresse woodgrovebank.com n’a jamais été authentifiée.
  
Lorsque vous utilisez DMARC, le serveur de réception effectue aussi une vérification sur l’adresse From. Dans l’exemple ci-dessus, s’il existe un enregistrement TXT DMARC pour woodgrovebank.com, la vérification de l’adresse de provenance rejette celle-ci.
  
## <a name="what-is-a-dmarc-txt-record"></a>Qu'est-ce qu'un enregistrement TXT DMARC ?
<a name="WhatisDMARC"> </a>

À l'instar des enregistrements DNS pour SPF, l'enregistrement pour DMARC est un enregistrement DNS au format texte (TXT) qui empêche l'usurpation d'identité et le hameçonnage. Vous publiez les enregistrements TXT DMARC dans le système DNS. Les enregistrements TXT DMARC valident l'origine des messages électroniques en comparant l'adresse IP de l'auteur de l'e-mail à celle du prétendu propriétaire du domaine d'expédition. L'enregistrement TXT DMARC identifie les serveurs de messagerie sortants autorisés. Les systèmes de messagerie électronique de destination peuvent alors vérifier si les messages reçus proviennent de serveurs de messagerie sortants autorisés.
  
Un enregistrement TXT DMARC de Microsoft se présente comme suit :
  
```
_dmarc.microsoft.com.   3600    IN      TXT     "v=DMARC1; p=none; pct=100; rua=mailto:d@rua.agari.com; ruf=mailto:d@ruf.agari.com; fo=1" 
```

Microsoft envoie ses rapports DMARC à [Agari](https://agari.com), un système tiers. Agari collecte et analyse les rapports DMARC.
  
## <a name="implement-dmarc-for-inbound-mail"></a>Mettre en œuvre DMARC pour les messages entrants
<a name="implementDMARCinbound"> </a>

Vous n'avez rien à faire pour configurer DMARC pour les messages que vous recevez dans Office 365. Nous nous sommes occupés de tout. Si vous voulez découvrir ce qui se passe pour le courrier électronique rejeté par nos vérifications DMARC, reportez-vous à la section [Gestion des messages électroniques entrants qui échouent aux vérifications de DMARC dans Office 365](use-dmarc-to-validate-email.md#inbounddmarcfail).
  
## <a name="implement-dmarc-for-outbound-mail-from-office-365"></a>Mettre en œuvre DMARC pour les messages sortants d'Office 365
<a name="implementDMARCoutbound"> </a>

Si vous utilisez Office 365, mais pas un domaine personnalisé, c'est-à-dire que vous utilisez onmicrosoft.com, il vous suffit de configurer ou de mettre en œuvre DMARC pour votre organisation. SPF est déjà configuré pour vous et Office 365 génère automatiquement une signature DKIM pour vos messages sortants. Pour plus d'informations sur cette signature, voir [Comportement par défaut pour DKIM et Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).
  
 Si vous avez un domaine personnalisé ou utilisez des serveurs Exchange locaux en plus d'Office 365, vous devez implémenter manuellement DMARC pour vos messages sortants. La mise en œuvre de DMARC pour votre domaine personnalisé comporte les étapes suivantes : 
  
- [Étape 1 : déterminer les sources de messagerie valides pour votre domaine](use-dmarc-to-validate-email.md#IdentifyValidSources)
    
- [Étape 2 : configurer SPF pour votre domaine dans Office 365](use-dmarc-to-validate-email.md#ConfigSPF)
    
- [Étape 3 : configurer DKIM pour votre domaine personnalisé dans Office 365](use-dmarc-to-validate-email.md#ConfigDKIM)
    
- [Étape 4 : créer l'enregistrement TXT DMARC pour votre domaine dans Office 365](use-dmarc-to-validate-email.md#CreateDMARCRecord)
    
### <a name="step-1-identify-valid-sources-of-mail-for-your-domain"></a>Étape 1 : déterminer les sources de messagerie valides pour votre domaine
<a name="IdentifyValidSources"> </a>

Si vous avez déjà configuré SPF, vous connaissez déjà la procédure. Toutefois, il existe des considérations supplémentaires pour DMARC. Lorsque vous déterminez les sources de messagerie pour votre domaine, il existe deux questions auxquelles vous devez répondre :
  
- Quelles adresses IP envoient des messages à partir de mon domaine ?
    
- Pour les messages envoyés par des tiers de ma part, les domaines 5321.MailFrom et 5322.From correspondront-ils ?
    
### <a name="step-2-set-up-spf-for-your-domain-in-office-365"></a>Étape 2 : configurer SPF pour votre domaine dans Office 365
<a name="ConfigSPF"> </a>

Maintenant que vous avez une liste de tous vos expéditeurs valides, vous pouvez suivre les étapes pour [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).
  
Par exemple, en supposant que contoso.com envoie du courrier depuis Exchange Online, un serveur Exchange local dont l'adresse IP est 192.168.0.1 et une application web dont l'adresse IP est 192.168.100.100, l'enregistrement TXT SPF ressemblerait à ceci :
  
```
contoso.com  IN  TXT  " v=spf1 ip4:192.168.0.1 ip4:192.168.100.100 include:spf.protection.outlook.com -all"
```

Pour obtenir les meilleurs résultats, vérifiez que votre enregistrement TXT SPF tienne compte des expéditeurs tiers.
  
### <a name="step-3-set-up-dkim-for-your-custom-domain-in-office-365"></a>Étape 3 : configurer DKIM pour votre domaine personnalisé dans Office 365
<a name="ConfigDKIM"> </a>

Une fois que vous avez configuré SPF, vous devez configurer DKIM. DKIM vous permet d'ajouter une signature numérique aux messages électroniques dans l'en-tête du message. Si vous ne configurez pas DKIM et que vous autorisez Office 365 à utiliser la configuration par défaut pour votre domaine à la place, DMARC risque de rejeter les messages. En effet, la configuration par défaut de DKIM utilise votre domaine onmicrosoft.com en tant qu'adresse 5322.From, et non votre domaine personnalisé. Cela crée de fait une différence entre les adresses 5321.MailFrom et 5322.From dans tous les messages envoyés à partir de votre domaine.
  
Si des expéditeurs tiers envoient des messages en votre nom et que les adresses 5321.MailFrom et 5322.From de ces messages ne correspondent pas, DMARC rejettera ce message électronique. Pour éviter ce problème, vous devez configurer DKIM en définissant spécifiquement cet expéditeur tiers pour votre domaine. Cela permet à Office 365 d'authentifier les messages envoyés par ce service tiers. Toutefois, cela autorise également d'autres entités, par exemple, Yahoo, Gmail et Comcast, à vérifier le courrier électronique qui leur est envoyé par le tiers comme s'il s'agissait de messages envoyés par vous-même. C'est un avantage, car, d'un côté, cela renforce la confiance que les clients peuvent avoir en votre domaine, quel que soit l'endroit où se trouvent leurs boîtes aux lettres et, de l'autre, Office 365 ne marquera pas un message comme spam pour cause d'usurpation d'identité, car cet e-mail aura été accepté par les vérifications d'authentification pour votre domaine.
  
Pour obtenir des instructions sur la configuration de DKIM pour votre domaine, y compris sur la façon de configurer DKIM pour les expéditeurs tiers pour leur permettre d'usurper votre domaine, voir [Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).
  
### <a name="step-4-form-the-dmarc-txt-record-for-your-domain-in-office-365"></a>Étape 4 : créer l'enregistrement TXT DMARC pour votre domaine dans Office 365
<a name="CreateDMARCRecord"> </a>

Bien qu'il existe des options de syntaxe qui ne sont pas mentionnées ici, voici les options les plus fréquemment utilisées pour Office 365. Créez l'enregistrement TXT DMARC pour votre domaine au format suivant :
  
```
_dmarc.domain  TTL  IN  TXT  "v=DMARC1; pct=100; p=policy"
```

où :
  
- *domaine* est le domaine que vous souhaitez protéger. Par défaut, l'enregistrement protège les messages provenant du domaine et de tous les sous-domaines. Par exemple, si vous spécifiez \_DMARC.contoso.com, dMarc protège le courrier électronique à partir du domaine et de tous les sous-domaines, tels que housewares.contoso.com ou Plumbing.contoso.com. 
    
- La valeur *TTL* doit toujours être équivalente à une heure. L'unité utilisée pour la valeur TTL, qu'il s'agisse des heures (1 heure), des minutes (60 minutes) ou des secondes (3600 secondes), varie en fonction du Bureau d'enregistrement de votre domaine. 
    
- *PCT = 100* indique que cette règle doit être utilisée pour 100% du courrier électronique.
    
- *Policy* spécifie la stratégie que le serveur de réception doit suivre si DMARC échoue. Vous pouvez définir la stratégie sur aucune, mise en quarantaine ou rejeter. 
    
Pour plus d'informations sur les options à utiliser, familiarisez-vous avec les concepts de la section [Meilleures pratiques pour la mise en œuvre de DMARC dans Office 365](use-dmarc-to-validate-email.md#DMARCbestpractices).
  
Exemples :
  
- Stratégie définie sur none (Aucune)
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=none"
    ```

- Stratégie définie sur quarantine (Mettre en quarantaine)
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=quarantine"
    ```

- Stratégie définie sur reject (Rejeter)
  
    ```
    _dmarc.contoso.com  3600 IN  TXT  "v=DMARC1; p=reject"
    ```

Une fois que vous avez créé votre enregistrement, vous devez le mettre à jour auprès de votre bureau d'enregistrement de domaine. Pour obtenir des instructions sur l'ajout de l'enregistrement TXT DMARC à vos enregistrements DNS pour Office 365, voir [Créer des enregistrements DNS pour Office 365 lorsque vous gérez vos enregistrements DNS](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).
  
## <a name="best-practices-for-implementing-dmarc-in-office-365"></a>Meilleures pratiques pour la mise en œuvre de DMARC dans Office 365
<a name="DMARCbestpractices"> </a>

Vous pouvez implémenter DMARC progressivement sans que cela n'ait de répercussions sur le reste de votre flux de messagerie. Créez et mettez en œuvre un plan de déploiement qui suit la procédure ci-dessous. Effectuez d'abord chaque étape avec un sous-domaine, puis avec d'autres, et enfin avec le domaine de niveau supérieur de votre organisation avant de passer à l'étape suivante.
  
1. Contrôlez les effets de l'implémentation DMARC
    
    Commencez avec un simple enregistrement en mode surveillance pour un sous-domaine ou un domaine qui requiert que les récepteurs DMARC vous envoient des statistiques sur les messages qu'ils voient pour ce domaine. Un enregistrement en mode surveillance est un enregistrement TXT DMARC dont la stratégie est définie sur Aucune (p=none). De nombreuses sociétés publient un enregistrement TXT DMARC avec p=none, car elles ne savent pas exactement la quantité de messages qu'elles risquent de perdre en publiant une stratégie DMARC plus restrictive. 
    
    Vous pouvez effectuer cette opération avant même d'avoir mis en œuvre SPF ou DKIM dans votre infrastructure de messagerie. Toutefois, vous ne pourrez pas mettre en quarantaine ou refuser des messages à l'aide de DMARC jusqu'à ce que vous implémentiez également SPF et DKIM. Lorsque vous mettrez en place SPF et DKIM, les rapports générés via DMARC fourniront le nombre et la source des messages qui sont acceptés par ces contrôles, ainsi que de ceux qui sont refusés. Vous pouvez facilement déterminer la part de votre trafic légitime qui est ou non couverte par ces catégories et résoudre les problèmes. Vous commencerez aussi à voir le nombre de messages frauduleux envoyés, ainsi que leur source.
    
2. Demandez que les systèmes de messagerie externes mettent en quarantaine le courrier qui échoue aux vérifications de DMARC
    
    Lorsque vous pensez que tout ou partie de votre trafic légitime est protégé par SPF et DKIM, et que vous connaissez les répercussions de l'implémentation de DMARC, vous pouvez implémenter une stratégie de mise en quarantaine. Une stratégie de mise en quarantaine est un enregistrement TXT DMARC dont la stratégie est définie de manière à effectuer une mise en quarantaine (p=quarantine). Ce faisant, vous demandez aux récepteurs DMARC de placer les messages issus de votre domaine qui sont refusés par DMARC dans l'équivalent local d'un dossier de courrier indésirable plutôt que dans la boîte de réception de vos clients.
    
3. Demandez que les systèmes de messagerie externes n'acceptent pas les messages qui échouent aux vérifications de DMARC
    
    L'étape finale consiste à mettre en œuvre une stratégie de rejet. Une stratégie de rejet est un enregistrement TXT DMARC dont la stratégie est définie de manière à effectuer un rejet (p=reject). Lorsque vous effectuez cette opération, vous demandez aux récepteurs DMARC ne pas accepter les messages qui échouent aux tests DMARC. 
    
## <a name="how-office-365-handles-outbound-email-that-fails-dmarc"></a>Gestion des messages électroniques sortants qui échouent aux vérifications de DMARC dans Office 365
<a name="outbounddmarcfail"> </a>

Si un message est sortant d'Office 365 et échoue DMARC et que vous avez défini la stratégie sur p = Quarantine ou p = Reject, le message est routé via le [pool de remise à haut risque pour les messages sortants](high-risk-delivery-pool-for-outbound-messages.md). Il n'y a pas de remplacement pour le courrier électronique sortant.
  
Si vous publiez une stratégie de rejet DMARC (p=reject), aucun autre client dans Office 365 ne peut usurper votre domaine, car les messages ne seront pas en mesure de passer les vérifications SPF ou DKIM pour votre domaine lorsqu'un message sortant sera relayé via le service. En revanche, si vous publiez une stratégie de rejet DMARC mais que tous vos messages électroniques ne sont pas authentifiés via Office 365, une partie de ceux-ci peuvent être marqués comme courrier indésirable pour les e-mails entrants (comme décrit ci-dessus), ou ils seront refusés si vous ne publiez pas SPF et que vous essayez de les relayer dans le sens sortant via le service. Cela peut se produire, par exemple, si vous avez oublié d'inclure les adresses IP de certains serveurs et de certaines applications qui envoient des messages au nom de votre domaine lorsque vous avez créé votre enregistrement TXT DMARC.
  
## <a name="how-office-365-handles-inbound-email-that-fails-dmarc"></a>Gestion des messages électroniques entrants qui échouent aux vérifications de DMARC dans Office 365
<a name="inbounddmarcfail"> </a>

Si la stratégie DMARC du serveur expéditeur est p=reject (rejet), EOP marque le message comme du courrier indésirable au lieu de le rejeter. En d'autres termes, pour les messages entrants, Office 365 traite les stratégies p=reject (rejet) et p=quarantine (mise en quarantaine) de la même manière.
  
Office 365 est configuré de cette façon, car certains messages légitimes peuvent échouer aux vérifications de DMARC. Cela peut être le cas, par exemple, si un message est envoyé à une liste de diffusion qui le relaie ensuite à tous ses participants. Si Office 365 rejette ces e-mails, les destinataires peuvent perdre des messages légitimes sans avoir aucun moyen de les récupérer. C'est pourquoi, avec cette configuration, ces messages sont toujours refusés par DMARC, mais, au lieu d'être rejetés, ils sont marqués comme courrier indésirable. Si nécessaire, les utilisateurs peuvent toujours accéder à ces messages dans leur boîte de réception via les méthodes suivantes :
  
- Les utilisateurs ajoutent individuellement des expéditeurs approuvés à l'aide de leur client de messagerie
    
- Les administrateurs créent une règle de transport Exchange pour tous les utilisateurs qui autorise la transmission des messages de ces expéditeurs particuliers. 
    
## <a name="troubleshooting-your-dmarc-implementation"></a>Résolution des problèmes d'implémentation de DMARC
<a name="dmarctroubleshoot"> </a>

Si EOP n'est pas la première entrée des enregistrements MX de votre domaine, les stratégies de DMARC en cas d'échec aux vérifications ne seront pas appliquées pour votre domaine. 
  
Si vous êtes un client Office 365 et que l'enregistrement MX principal de votre domaine ne pointe pas vers EOP, vous ne bénéficiez pas de la protection de DMARC. Par exemple, DMARC ne fonctionne pas si l'enregistrement MX pointe vers votre serveur de messagerie local et que les e-mails sont ensuite acheminés vers EOP à l'aide d'un connecteur. Dans ce cas de figure, le domaine de réception est l'un de vos domaines d'accepté, mais EOP n'est pas l'enregistrement MX principal. Par exemple, supposons que l'enregistrement MX de contoso.com pointe vers contoso.com lui-même et que EOP soit utilisé comme enregistrement MX secondaire. L'enregistrement MX de contoso.com se présente alors comme suit :
  
```
contoso.com     3600   IN  MX  0  mail.contoso.com
contoso.com     3600   IN  MX  10 contoso-com.mail.protection.outlook.com
```

Tout ou la plupart, le courrier électronique est d'abord routé vers mail.contoso.com étant donné qu'il s'agit du MX principal, puis le courrier est acheminé vers EOP. Dans certains cas, vous ne pouvez même pas répertorier EOP comme un enregistrement MX et simplement raccorder des connecteurs pour acheminer votre courrier électronique. EOP ne doit pas nécessairement être la première entrée pour que la validation DMARC soit réalisée. Elle garantit simplement la validation, car il est impossible de s'assurer que tous les serveurs locaux/non-O365s effectuent des vérifications DMARC.  DMARC est éligible pour être appliqué au domaine d'un client (et non au serveur) lorsque vous configurez l'enregistrement TXT DMARC, mais il revient au serveur de réception de procéder à la mise en œuvre effective.  Si vous configurez EOP en tant que serveur de réception, EOP effectue l'application DMARC.
  
## <a name="for-more-information"></a>Pour plus d'informations
<a name="sectionSection8"> </a>

Vous voulez plus d'informations sur DMARC ? Ces ressources peuvent vous aider.
  
- [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md) comprend la syntaxe et les champs d'en-tête utilisés par Office 365 pour les vérifications DMARC. 
    
- Consultez la [série de formations sur DMARC](https://www.m3aawg.org/activities/training/dmarc-training-series) de M <sup>3</sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group).
    
- Utilisez la liste de vérification proposée par [dmarcian](https://space.dmarcian.com/deployment/).
    
- Accédez directement à la source à l'adresse [DMARC.org](https://dmarc.org).
    
## <a name="see-also"></a>See also
<a name="sectionSection8"> </a>

[Comment Office 365 utilise SPF (Sender Policy Framework) pour éviter l’usurpation](how-office-365-uses-spf-to-prevent-spoofing.md)
  
[Configurer SPF dans Office 365 pour empêcher l’usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
  
[Utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md)

