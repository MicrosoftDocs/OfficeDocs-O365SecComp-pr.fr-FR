---
title: Protection contre l’usurpation d’identité dans Office 365
ms.author: tracyp
author: MSFTtracyp
manager: laurawi
ms.date: 03/29/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
ms.collection:
- M365-security-compliance
- Strat_O365_IP
ms.custom: TopSMBIssues
localization_priority: Priority
description: Cet article explique comment Office 365 prévient les attaques par hameçonnage utilisant des domaines d’expéditeur falsifiés, ou usurpés. Pour ce faire, Microsoft analyse les messages et bloque ceux qui ne peuvent être authentifiés ni à l’aide de méthodes d’authentification standard du courrier, ni à l’aide d’autres techniques basées sur la réputation des expéditeurs. Cette modification a été apportée afin de réduire le nombre d’attaques par hameçonnage auxquelles sont exposées les organisations utilisant Office 365.
ms.openlocfilehash: 533444d323728d2f238da409256f6547a5c8d209
ms.sourcegitcommit: 1261a37c414111f869df5791548a768d853fda60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2019
ms.locfileid: "31004261"
---
# <a name="anti-spoofing-protection-in-office-365"></a>Protection contre l’usurpation d’identité dans Office 365

Cet article explique comment Office 365 prévient les attaques par hameçonnage utilisant des domaines d’expéditeur falsifiés, ou usurpés. Pour ce faire, Microsoft analyse les messages et bloque ceux qui ne peuvent être authentifiés ni à l’aide de méthodes d’authentification standard du courrier, ni à l’aide d’autres techniques basées sur la réputation des expéditeurs. Cette modification a été apportée afin de réduire le nombre d’attaques par hameçonnage auxquelles sont exposées les organisations utilisant Office 365.
  
Cet article explique également pourquoi cette modification a été introduite, comment les clients peuvent s’y préparer, comment afficher les messages qui seront affectés, comment générer des rapports sur les messages, comment limiter le nombre de faux positifs, et comment les expéditeurs à Microsoft doivent se préparer.
  
La technologie de détection d’usurpation d’identité de Microsoft a été initialement déployée vers des organisations qui disposaient d’un abonnement Office 365 Entreprise E5 ou avaient acheté le module complémentaire Office 365 - Protection avancée contre les menaces pour leur abonnement. Depuis octobre 2018, nous avons étendu la protection aux organisations disposant d’Exchange Online Protection. De plus, en raison de la façon dont tous nos filtres apprennent les uns des autres, les utilisateurs d’Outlook.com peuvent également être concernés.
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a>Comment l’usurpation est utilisée dans les attaques par hameçonnage

Pour protéger ses utilisateurs, Microsoft prend la menace du hameçonnage au sérieux. L’usurpation d’identité est l’une des techniques que les hameçonneurs et les expéditeurs de courrier indésirable utilisent couramment. Cette technique consiste à falsifier l’identité de l’expéditeur de telle sorte qu’un message semble provenir d’un personne ou d’un endroit autre que la source réelle. Cette technique est souvent utilisée dans des campagnes de hameçonnage visant à dérober des informations d’identification d’utilisateur. La technologie de détection d’usurpation d’identité de Microsoft examine spécifiquement la falsification de l’en-tête « De : » qui apparaît dans un client de courrier tel qu’Outlook. Quand Microsoft est convaincu que l’en-tête De : est usurpé, il identifie le message comme une usurpation d’identité.
  
Les messages usurpant une identité ont deux conséquences négatives pour les utilisateurs réels :
  
### <a name="1-spoofed-messages-deceive-users"></a>1. Ils trompent les utilisateurs
  
Premièrement, un message usurpant une identité peut leurrer un utilisateur en l’incitant à cliquer sur un lien l’amenant à révéler ses identifiants, à télécharger un programme malveillant ou à répondre en révélant du contenu sensible (compromission de courrier professionnel). Par exemple, voici un message de hameçonnage dont l’expéditeur a usurpé l’adresse msoutlook94@service.outlook.com :
  
![Message de hameçonnage usurpant le domaine service.outlook.com](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
Le courrier qui précède ne provient pas de service.outlook.com, mais le hameçonneur à l’origine de l’usurpation a fait en sorte qu’il semble provenir de ce domaine. Il tente de duper le destinataire en l’incitant à cliquer sur le lien contenu dans le message.
  
L’exemple suivant usurpe le domaine contoso.com :
  
![Message de hameçonnage – compromission de courrier professionnel](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
Le message semble légitime, mais est en réalité une usurpation. Ce message de hameçonnage est du type compromission de courrier professionnel qui est une sous-catégorie du hameçonnage.

### <a name="2-users-confuse-real-messages-for-fake-ones"></a>2. Certains utilisateurs prennent de vrais messages pour des faux
  
Deuxièmement, les messages usurpant des identités créent une incertitude dans le chef des utilisateurs informés de l’existence de messages de hameçonnage mais incapables de faire la différence entre un message authentique et un message falsifié. Par exemple, voici un exemple de demande de réinitialisation de mot de passe authentique provenant de l’adresse e-mail du compte Microsoft Security :
  
![Réinitialisation de mot de passe légitime de Microsoft](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
Si le message ci-dessus provient effectivement de Microsoft, les utilisateurs sont habitués à recevoir des messages de hameçonnage susceptibles de les inciter à cliquer sur un lien les amenant à révéler leurs identifiants, à télécharger un programme malveillant ou à répondre en révélant du contenu sensible. En raison de la difficulté de faire la distinction entre une demande de réinitialisation de mot de passe authentique et une fausse demande, bon nombre d’utilisateurs ignorent ces messages, les marquent comme du courrier indésirable, ou les signalent à Microsoft comme des tentatives de hameçonnage.

Pour mettre fin aux usurpations d’identité, les experts en filtrage du courrier ont développé des protocoles d’authentification tels que [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email) et [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email). DMARC empêche l’usurpation d’identité en examinant l’expéditeur d’un message que l’utilisateur voit dans son client de courrier (dans les exemples ci-dessus, service.outlook.com, outlook.com et accountprotection.microsoft.com), avec le domaine qui a traversé les filtres SPF ou DKIM. Autrement dit, le domaine que l’utilisateur voit a été authentifié et n’est donc pas usurpé. Pour une présentation plus complète, voir la section « *Pourquoi l’authentification du courrier ne suffit pas toujours pour empêcher l’usurpation* », plus loin dans cet article.
  
Cependant, le problème est que les enregistrements d’authentification de courrier sont facultatifs et non obligatoires. Dès lors, si les domaines dotés de stratégies d’authentification fortes, tels que microsoft.com et skype.com, sont protégés contre l’usurpation d’identité, des domaines dont les stratégies d’authentification sont plus faibles, voire inexistantes, constituent des cibles idéales pour de telles usurpations. En mars 2018, seul 9% des domaines des sociétés répertoriées dans Fortune 500 affichent de fortes stratégies d’authentification d’email. Ainsi, un hameçonneur peut usurper le domaine des 91 % de domaines restants de sorte que, si le filtre de courrier ne détecte pas l’usurpation à l’aide d’une autre stratégie, le courrier peut être délivré à un utilisateur final et le tromper :
  
![Stratégies DMARC des entreprises du Fortune 500](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
La proportion de petites et moyennes entreprises non reprises au classement Fortune 500 et qui publient des stratégies d’authentification de courrier fortes est plus faible, et plus faible encore pour les domaines situés en dehors de l’Amérique du Nord et de l’Europe occidentale.
  
Le problème est de taille car, si les entreprises ne sont peut-être pas informées des mécanismes d’authentification du courrier, les rançonneurs les maîtrisent parfaitement et profitent de ces lacunes.
  
Pour plus d’informations sur la configuration de SPF, DKIM et DMARC, voir la section « *Clients d’Office 365* » plus loin dans ce document. 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a>Blocage de l’usurpation d’identité avec une authentification de courrier implicite

Le hameçonnage et le harponnage sont si problématiques et l’adoption de stratégies d’authentification de courrier fortes si limitée que Microsoft continue d’investir dans des fonctionnalités capables de protéger ses clients. C’est pourquoi Microsoft va de l’avant avec l’*authentification de courrier implicite*. Si un domaine ne s’authentifie pas, Microsoft le traite comme s’il avait publié des enregistrements d’authentification de courrier et avait échoué. 
  
Pour ce faire, Microsoft a ajouté de nombreuses extensions à l’authentification de courrier ordinaire, dont la réputation de l’expéditeur, l’historique de l’expéditeur et du destinataire, l’analyse comportementale et d’autres techniques avancées. Un message provenant d’un domaine ne publiant pas d’authentification de courrier est marqué comme une usurpation d’identité, sauf s’il contient d’autres signaux indiquant sa légitimité.
  
Ainsi, les destinataires ont la certitude qu’un courrier qui leur est envoyé n’a pas été usurpé, et les expéditeurs sont assurés que personne n’usurpe leur domaine. Par ailleurs, les clients d’Office 365 bénéficient d’une protection encore supérieure, par exemple, contre l’emprunt d’identité.
  
Pour lire l’annonce générale de Microsoft, voir [A Sea of Phish Part 2 – Enhanced Anti-spoofing in Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a>Identification de la classification d’un message comme usurpé

### <a name="composite-authentication"></a>Authentification composite

Si les filtrages SPF, DKIM et DMARC sont utiles en soi, ils ne communiquent pas suffisamment l’état d’authentification quand un message n’a pas d’enregistrement d’authentification explicite. C’est pourquoi Microsoft a développé un algorithme combinant plusieurs signaux en une valeur unique appelée Authentification composite, abrégée en Compauth. Les clients d’Office 365 ont des valeurs compauth estampillées dans l’en-tête *Authentication-Results*, à l’intérieur des en-têtes de message. 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|**Résultat CompAuth**|**Description**|
|:-----|:-----|
|fail|Authentification explicite de message ayant échoué (le domaine d’envoi a publié des enregistrements de façon explicite dans DNS), ou authentification implicite (le domaine d’envoi n’ayant pas publié d’enregistrement dans DNS, Office 365 a interpolé le résultat comme s’il en avait publié).|
|pass|Authentification explicite de message transmis (le message a franchi le filtrage DMARC ou [Best Guess Passed DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)), ou authentification implicite à niveau de confiance élevé (le domaine n’a pas publié d’enregistrement d’authentification de courrier mais Office 365 a des signaux forts indiquant que le message est probablement légitime).|
|softpass|Le message a passé l’authentification implicite avec un niveau de confiance faible à moyen (si le domaine d’envoi ne publie pas d’authentification de courrier, Office 365 a des signaux indiquant que le message est légitime mais que la force du signal est plus faible).|
|none|Le message ne s’est pas authentifié (ou s’est authentifié mais ne s’alignait pas), mais l’authentification composite n’a pas été appliquée en raison de la réputation de l’expéditeur ou d’autres facteurs.|
   
|||
|:-----|:-----|
|**Raison**|**Description**|
|0xx|Le message a échoué à l’authentification composite.<br/>**000** signifie que le message a échoué au filtrage DMARC, et déclenché une action de rejet ou de mise en quarantaine.  <br/>**001** signifie que le message a échoué à l’authentification de courrier implicite. Cela signifie que le domaine d’envoi n’a pas publié d’enregistrement d’authentification de courrier ou, s’il la fait, que sa stratégie en cas d’échec était plus faible (erreur SPF récupérable ou neutre, stratégie DMARC p=aucune).  <br/>**002** signifie que l’organisation a une stratégie pour la paire expéditeur/domaine qui interdit explicitement l’envoi d’e-mails usurpés, ce paramètre étant défini manuellement par un administrateur.  <br/>**010** signifie que le message a échoué au filtrage DMARC, et déclenché une action de rejet ou de mise en quarantaine, et que le domaine d’envoi est l’un des domaines acceptés de l’organisation (cela fait partie de l’usurpation self-to-self, ou intra-organisationnelle).  <br/>**011** signifie que le message a échoué à l’authentification de courrier implicite et que le domaine d’envoi est l’un des domaines acceptés de l’organisation (cela fait partie de l’usurpation self-to-self, ou intra-organisationnelle).|
|Tous les autres codes (1xx, 2xx, 3xx, 4xx, 5xx)|Correspond à divers codes internes expliquant pourquoi un message ayant passé l’authentification implicite ou n’ayant fait l’objet d’aucune authentification n’a pas déclenché d’action.|
   
En examinant les en-têtes d’un message, un administrateur, voire un destinataire, peut déterminer comment Office 365 en arrive à la conclusion que l’identité de l’expéditeur peut être usurpée.
  
### <a name="differentiating-between-different-types-of-spoofing"></a>Différenciation des différents types d’usurpations

Microsoft distingue deux types de messages d’usurpation d’identité :
  
 **Usurpation intra-organisationnelle**
  
Également appelée usurpation self-to-self, elle se produit lorsque le domaine figurant dans l’adresse De : est identique au domaine du destinataire ou aligné sur celui-ci (lorsque le domaine du destinataire est l’un des [Domaines acceptés](https://technet.microsoft.com/fr-FR/library/jj945194%28v=exchg.150%29.aspx) par l’organisation), ou lorsque le domaine figurant dans l’adresse De : fait partie de la même organisation.
  
Par exemple, l’expéditeur et le destinataire du message suivant appartiennent au même domaine (contoso.com). (Des espaces sont insérées dans les adresses de courrier pour empêcher d’éventuels bots de spam de prélever celles-ci sur cette page) :
  
De: expéditeur @ contoso.com
  
À : destinataire @ contoso.com
  
Dans l’exemple suivant, les domaines de l’expéditeur et du destinataire sont alignés sur le domaine de l’organisation (fabrikam.com) :
  
De : expéditeur @ foo.fabrikam.com
  
À : destinataire @ bar.fabrikam.com
  
Dans l’exemple suivant, les domaines de l’expéditeur et du destinataire sont différents (microsoft.com et bing.com), mais ils appartiennent à la même organisation (ce qui signifie que tous deux font partie des domaines acceptés de l’organisation) :
  
De: expéditeur @ microsoft.com
  
À : destinataire @ bing.com
  
Les messages qui échouent au filtrage d’usurpation intra-organisationnelle contiennent les valeurs suivantes dans les en-têtes :
  
X-Forefront-Antispam-Report: ...CAT:SPM/HSPM/PHSH;...SFTY:9.11
  
CAT correspond à la catégorie du message qui est normalement SPM (courrier indésirable), mais peut parfois être HSPM (courrier fortement suspecté d’être indésirable) ou de PHSH (hameçonnage), en fonction des autres types de structures présents dans le message.
  
SFTY indique le niveau de sécurité du message. Le premier chiffre (9) signifie que le message est du hameçonnage, et les deux chiffres après le point (11) qu’il s’agit d’une usurpation d’identité intra-organisationnelle.
  
Il n’y a pas de code de motif spécifique en lien avec l’authentification composite pour l’usurpation d’identité intra-organisationnelle. Un tel code sera estampillé plus tard en 2018 (calendrier non encore défini).
  
 **Usurpation inter-domaines**
  
Cela se produit lorsque le domaine d’envoi figurant dans l’adresse De : est un domaine externe à l’organisation destinataire. Les en-têtes des messages qui échouent à l’authentification composite en raison d’une usurpation inter-domaines contiennent les valeurs suivantes :
  
Authentication-Results: … compauth=fail reason=000/001
  
X-Forefront-Antispam-Report: ...CAT:SPOOF;...SFTY:9.22
  
Dans les deux cas, le conseil de sécurité rouge suivant est estampillé dans le message, ou un conseil équivalent personnalisé en fonction de la langue de la boîte aux lettres du destinataire :
  
![Conseil de sécurité rouge – détection de fraude](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
Il n’est possible de faire la différence entre une usurpation intra-organisationnelle et une usurpation inter-domaines qu’en regardant l’adresse De : et en connaissant l’adresse e-mail du destinataire, ou en inspectant les en-têtes de l’e-mail.
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a>Comment les clients d’Office 365 peuvent se préparer à la nouvelle protection contre l’usurpation d’identité

### <a name="information-for-administrators"></a>Informations pour les administrateurs

En tant qu’administrateur d’une organisation dans Office 365, vous devez connaître plusieurs informations essentielles.
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a>Pourquoi l’authentification du courrier ne suffit pas toujours pour empêcher l’usurpation

La nouvelle protection contre l’usurpation d’identité s’appuie sur l’authentification de courrier (SPF, DKIM et DMARC) pour ne pas marquer un message comme usurpant une identité. Un exemple courant est quand un domaine d’envoi n’a jamais publié d’enregistrements SPF. À défaut d’enregistrements SPF ou si les enregistrements ne sont pas correctement configurés, un message envoyé est marqué comme usurpé, sauf si Microsoft dispose de renseignement indiquant que le message est légitime.
  
Par exemple, avant le déploiement de la détection d’usurpation d’identité, un message pouvait ressembler à ce qui suit sans enregistrement SPF, DKIM ou DMARC : 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
Après déploiement de la détection d’usurpation d’identité, si vous disposez d’Office 365 Entreprise E5, d’Exchange Online Protection ou d’Advanced Threat Protection, la valeur compauth est estampillée :
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

Si example.com corrigeait cela en configurant un enregistrement SPF mais pas d’enregistrement DKIM, l’authentification composite était transmise, car le domaine transmettant SPF correspondait au domaine figurant dans l’adresse De :. 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Ou bien, s’ils configuraient un enregistrement DKIM mais pas d’enregistrement SPF, l’authentification composite était également transmise parce que le domaine dans la signature DKIM qui transmettait correspondait au domaine dans l’adresse De :. 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Cependant, un hameçonneur peut également configurer SPF et DKIM, et signer le message avec son propre domaine, mais spécifier un autre domaine dans l’adresse De :. Ni SPF, ni DKIM n’exigeant que le domaine corresponde au domaine indiqué dans l’adresse De:, si example.com n’a pas publié d’enregistrements DMARC, les messages ne sont pas marqués comme usurpés à l’aide de DMARC : 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

Dans le client de courrier (Outlook, Outlook sur le web ou tout autre client), seul le domaine De : est affiché, pas le domaine dans SPF ou DKIM, ce qui peut induire l’utilisateur en erreur en lui faisant croire que le message provient d’example. com, alors qu’il provient en réalité de DomaineMalveillant.com.
  
![Message authentifié mais le domaine De : ne correspond pas à ce qu’ont transmis SPF ou DKIM](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
Pour cette raison, Office 365 requiert que le domaine dans l’adresse De : corresponde à celui figurant dans la signature SPF ou DKIM et, dans le cas contraire, que le message contienne d’autres signaux internes indiquant qu’il est légitime. Autrement, le message constitue un échec compauth. 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

Ainsi, le dispositif de détection d’usurpation d’identité d’Office 365 protège contre les domaines sans authentification ainsi que contre les domaines qui configurent une authentification mais ne correspondent pas au domaine figurant dans l’adresse d’expédition, puisqu’il s’agit de l’adresse que l’utilisateur voit et considère comme étant celle de l’expéditeur du message. Cela vaut tant pour les domaines externes à votre organisation que pour les domaines internes.
  
Par conséquent, si vous recevez un message qui a échoué à l’authentification composite et est marqué comme usurpant une identité, même si le message a franchi les filtrages SPF et DKIM, c’est parce que le domaine de ce message ne correspond pas au domaine indiqué dans l’adresse De:.
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a>Compréhension des modifications apportées à la manière dont les e-mails usurpant une identité sont traités

Actuellement, pour toutes les organisations utilisant Office 365, avec ou sans Advanced Threat Protection, les messages qui échouent au filtrage DMARC avec une stratégie de rejet ou de mise en quarantaine sont considérés comme du courrier indésirable et déclenchent généralement l’action anti-courrier fortement suspecté d’être indésirable, ou parfois l’action anti-courrier indésirable ordinaire (selon que d’autres règles de courrier indésirable ont identifié ou non les messages comme étant du courrier indésirable). Les détections d’usurpation intra-organisationnelle déclenchent l’action anti-courrier indésirable ordinaire. Ce comportement n’a pas besoin d’être activé, car il ne peut pas être désactivé.
  
En revanche, pour les messages d’usurpation inter-domaines, avant cette modification, ils étaient soumis à des contrôles réguliers en lien avec le courrier indésirable, le hameçonnage et les programmes malveillants et, si d’autres parties du filtre les identifiaient comme suspects, ils étaient marqués respectivement comme courrier indésirable, hameçonnage ou programme malveillant. Avec la nouvelle détection d’usurpation d’identité inter-domaines, tout message qui ne peut pas être authentifié déclenche par défaut l’action définie dans la stratégie Anti-hameçonnage \> Détection d’usurpation d’identité. Si un message n’est pas défini, il est déplacé vers le dossier de courrier indésirable de l’utilisateur. Dans certains cas, le conseil de sécurité rouge est également ajouté à d’autres messages suspects.
  
Cela peut avoir pour conséquence que certains messages qui étaient précédemment marqués comme courrier indésirable le soient toujours, mais reçoivent désormais un conseil de sécurité rouge. Dans d’autres cas, les messages précédemment marqués comme n’étant pas du courrier indésirable commencent à être marqués comme courrier indésirable (CAT:SPOOF) avec ajout d’un conseil de sécurité rouge. Dans d’autres cas encore, des clients qui mettaient tous les courriers indésirables et hameçonnages en quarantaine les verront désormais placés dans le dossier Courrier indésirable (ce comportement peut être modifié ; voir [Modification de vos paramètres de détection d’usurpation d’identité](#changing-your-anti-spoofing-settings)).
  
Un message peut usurper une identité de différentes façons (voir [Différenciation des différents types d’usurpations](#differentiating-between-different-types-of-spoofing) plus haut dans cet article) mais, depuis mars 2018, la manière dont Office 365 traite ces messages n’est pas encore unifiée. Le tableau suivant résume brièvement la situation avec la protection contre l’usurpation d’identité inter-domaines en tant que nouveau comportement : 
  
|**Type d’usurpation**|**Catégorie**|**Conseil de sécurité ajouté ?**|**S’applique à**|
|:-----|:-----|:-----|:-----|
|Échec DMARC (mise en quarantaine ou rejet)  <br/> |HSPM (par défaut), peut également être SPM ou PHSH  <br/> |Non (pas encore)  <br/> |Tous les clients d’Office 365, Outlook.com  <br/> |
|Self-to-self  <br/> |SPM  <br/> |Oui  <br/> |Toutes les organisations Office 365, Outlook.com  <br/> |
|Inter-domaines  <br/> |SPOOF  <br/> |Oui  <br/> |Clients d’Office 365 - Protection avancée contre les menaces et d’E5  <br/> |

### <a name="changing-your-anti-spoofing-settings"></a>Modification de vos paramètres de détection d’usurpation d’identité

Pour créer ou mettre à jour vos paramètres de détection d’usurpation d’identité (inter-domaines), dans le Centre de sécurité et de conformité, sous l’onglet Gestion des menaces \> Stratégie, accédez aux paramètres Anti-hameçonnage \> Détection d’usurpation d’identité. Si vous n’avez jamais créé de paramètres anti-hameçonnage, vous devez en créer un :
  
![Anti-hameçonnage – Créer une stratégie](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
Si vous avez déjà créé une stratégie, vous pouvez la sélectionner pour la modifier :
  
![Anti-hameçonnage – Modifier une stratégie existante](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
Sélectionnez la stratégie que vous venez de créer, puis suivez les étapes décrites dans la section [En savoir plus sur l’usurpation d’identité](learn-about-spoof-intelligence.md).
  
![Activer ou désactiver la détection d’usurpation d’identité](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![Activer ou désactiver les conseils de sécurité de la détection d’usurpation d’identité](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
Pour créer une nouvelle stratégie à l’aide de PowerShell : 
  
```powershell
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: The name should not exclude 64 characters, including spaces.
# If it does, you will need to pick a smaller name.
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy $name -RecipientDomainIs $domains
```

Vous pouvez ensuite modifier les paramètres de stratégie anti-hameçonnage à l’aide de PowerShell, en suivant la documentation sur la cmdlet [Set-AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps). Vous pouvez spécifier le $name en tant que paramètre :
  
```powershell
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

Depuis 2018, au lieu que vous ayez à créer une stratégie par défaut, une stratégie est créée pour vous et étendue à tous les destinataires au sein de votre organisation. Vous n’avez donc pas besoin de la spécifier manuellement (les captures d’écran peuvent différer légèrement de l’implémentation finale).
  
![Stratégie de anti-hameçonnage par défaut](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
À la différence d’une stratégie que vous créez, vous ne pouvez pas supprimer la stratégie par défaut, modifier sa priorité ou choisir les utilisateurs, domaines ou groupes auxquels l’étendre.
  
![Détails de la stratégie de anti-hameçonnage par défaut](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
Pour configurer votre protection par défaut à l’aide de PowerShell :
  
```powershell
$defaultAntiphishPolicy = Get-AntiphishPolicy | ? {$_.IsDefault -eq $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

Vous ne devez désactiver la protection contre l’usurpation d’identité que si vous avez un ou plusieurs autres serveurs de messagerie devant Office 365 (pour plus de détails, voir Scénarios légitimes pour désactiver la protection contre l’usurpation d’identité).
  
```powershell
$defaultAntiphishPolicy = Get-AntiphishiPolicy | ? {$_.IsDefault $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> Si Office 365 est en première ligne dans le chemin d’accès au courrier et que vous recevez trop d’e-mails légitimes marqués comme usurpant une identité, vous devez commencer par définir les expéditeurs autorisés à envoyer ce type de courrier à votre domaine (voir la section « *Gestion des expéditeurs légitimes qui envoient du courrier non authentifié* »). Si vous recevez encore trop de faux positifs (c’est-à-dire des messages légitimes marqués comme usurpant une identité), nous ne recommandons PAS de désactiver complètement la protection contre l’usurpation d’identité. Au lieu de cela, nous vous recommandons de choisir une protection De base plutôt que Haute. Mieux vaut s’accommoder de faux positifs que d’exposer votre organisation à du courrier usurpant des identités, ce qui pourrait finir par occasionner des coûts beaucoup plus élevés à long terme.

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a>Gestion des expéditeurs légitimes qui envoient du courrier non authentifié

Office 365 conserve la trace des personnes qui envoient du courrier non authentifié à votre organisation. Si le service considère que l’expéditeur n’est pas légitime, il le marque en tant qu’échec *compauth*. Ce courrier est classé comme usurpation (SPOOF), bien que cela dépende de votre stratégie de détection d’usurpation d’identité appliquée au message.
  
Toutefois, en tant qu’administrateur, vous pouvez spécifier les expéditeurs autorisés à envoyer du courrier usurpant une identité en infirmant la décision d’Office 365.
  
**Méthode 1 : si votre organisation est propriétaire du domaine, configurez l’authentification du courrier**
  
Cette méthode permet de résoudre l’usurpation d’identité intra-organisationnelle et inter-domaines dans les cas où vous interagissez avec plusieurs locataires. Cela aide également à résoudre l’usurpation inter-domaines lorsque vous envoyez du courrier à d’autres clients au sein d’Office 365, ainsi qu’à des tiers hébergés chez d’autres fournisseurs.
  
Pour plus d’informations, voir [Clients d’Office 365 ](#customers-of-office-365).

**Méthode 2 : utiliser la veille contre l’usurpation d’identité pour configurer les expéditeurs autorisés de courrier non authentifié**.
  
Vous pouvez également utiliser la [Veille contre l’usurpation d’identité](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) pour autoriser des expéditeurs à transmettre des messages non authentifiés à votre organisation. 
  
Pour des domaines externes, l’utilisateur usurpé est le domaine dans l’adresse de l’expéditeur, tandis que l’infrastructure d’envoi est soit l’adresse IP d’envoi (divisée en 24 plages CIDR), soit le domaine organisationnel de l’enregistrement PTR (dans la capture d’écran ci-dessous, l’adresse IP d’envoi pourrait être 131.107.18.4 dont l’enregistrement PTR est outbound.mail.protection.outlook.com, qui apparaîtrait comme outlook.com pour l’infrastructure d’envoi).
  
Pour autoriser cet expéditeur à envoyer un courrier non authentifié, remplacez **Non** par **Oui**.
  
![Définition des expéditeurs autorisés par la paramètre](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
Vous pouvez également utiliser PowerShell pour autoriser un expéditeur spécifique à usurper l’identité de votre domaine :
  
```powershell
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```powershell
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Obtention d’expéditeurs usurpés de Powershell](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
Dans l’image précédente, des sauts de ligne supplémentaires ont été ajoutés pour faciliter la lisibilité de cette capture d’écran. Normalement, toutes les valeurs apparaissent sur une seule ligne.
  
Editez le fichier et recherchez la ligne correspondant à outlook.com et bing.com, puis modifiez l’entrée AllowedToSpoof de Non à Oui :
  
![Définition de l’autorisation d’usurpation sur Oui dans Powershell](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
Enregistrez le fichier, puis exécutez la cmdlet suivante :
  
```powershell
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

Cela permettra désormais à bing.com d’envoyer du courrier non authentifié à partir de \*.outlook.com.

**Méthode 3 : créer une entrée d’autorisation pour la paire expéditeur/destinataire**
  
Vous pouvez également choisir d’ignorer tout filtrage du courrier indésirable pour un expéditeur particulier. Pour plus d’informations, voir [Comment ajouter en toute sécurité un expéditeur à une liste d’autorisation dans Office 365](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/).
  
Si vous utilisez cette méthode, le courrier indésirable et une partie du filtrage du hameçonnage sont ignorés, mais pas le filtrage des programmes malveillants.
  
**Méthode 4 : contacter l’expéditeur pour lui demander de configurer l’authentification du courrier**
  
En raison du problème de courrier indésirable et de hameçonnage, Microsoft recommande à tous les expéditeurs de configurer l’authentification du courrier. Si vous connaissez un administrateur du domaine d’envoi, contactez-le pour lui demander de configurer des enregistrements d’authentification du courrier afin que vous n’ayez pas à ajouter un contournement. Pour plus d’informations, voir [Administrateurs de domaines qui ne sont pas des clients d’Office 365](#administrators-of-domains-that-are-not-office-365-customers) plus loin dans cet article. 
  
S’il peut être difficile au début d’obtenir des domaines d’envoi qu’ils s’authentifient, avec le temps, à mesure que de plus en plus de filtres de courrier considéreront leurs e-mails comme indésirables, voire les rejetteront, ils seront amenés à configurer les enregistrements appropriés pour améliorer la remise.
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a>Affichage de rapports sur le nombre de messages marqués comme usurpés

Une fois votre stratégie de détection d’usurpation d’identité activée, vous pouvez utiliser l’enquête relative aux menaces pour obtenir des chiffres indiquant le nombre de messages marqués comme tentatives de hameçonnage. Pour ce faire, sous l’Explorateur&amp;du Centre de Sécurité et de Conformité (CSC) relatif à la Gestion des Menaces\>, définissez l’Affichage sur Hameçonnage, puis groupez par Domaine de l’expéditeur ou État de la protection :
  
![Affichage du nombre de messages marqués comme hameçonnage](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
Vous pouvez interagir avec les différents rapports pour voir combien de messages ont été marqués comme hameçonnage, y compris les messages marqués comme SPOOF. Pour en savoir plus, voir [Prise en main d’Office 365 Enquête relative aux Menaces et réponse](get-started-with-ti.md).
  
Vous ne pouvez pas encore discriminer des messages marqués en raison d’une usurpation par opposition à d’autres types de hameçonnages (hameçonnage général, emprunt d’identité de domaine ou d’utilisateur, etc.). En revanche, vous pourrez le faire ultérieurement via le Centre de sécurité et de conformité. Lorsque vous le ferez, vous pourrez utiliser ce rapport comme point de départ pour identifier les domaines d’envoi susceptibles d’être légitimes mais signalés comme usurpant une identité en raison d’un échec d’authentification.
  
La capture d’écran suivante pourrait différer de la version publiée :
  
![Affichage des rapports de hameçonnage par type de détection](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
Pour les clients autres qu’Advanced Threat Protection et E5, ces rapports seront disponibles ultérieurement sous les rapports d’État de la protection contre les menaces, mais seront retardés d’au moins 24 heures. Cette page sera mise à jour au fur et à mesure de leur intégration dans le Centre de sécurité et de conformité.
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a>Prédiction du nombre de messages qui seront marqués comme usurpant une identité

Quand Office 365 aura mis à jour ses paramètres pour vous permettre de désactiver la détection d’usurpation d’identité ou de l’activer avec l’application De base ou Élevée, vous aurez la possibilité de voir comment la disposition des messages changera en fonction des différents paramètres. Cela signifie que, si la détection d’usurpation d’identité est désactivée, vous pourrez voir combien de messages seront détectés comme Usurpation si vous passez à l’application De base. Ou bien, si l’application De base est activée, vous pourrez voir combien de messages supplémentaires seront détectés comme Usurpation si vous la réglez sur Elevée.
  
Cette fonctionnalité est en cours de développement. À mesure que davantage de détails seront définis, cette page sera mise à jour avec des captures d’écran du Centre de sécurité et conformité ainsi qu’avec des exemples PowerShell.
  
![Rapport « What If » pour activer la détection d’usurpation d’identité](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![Expérience utilisateur possible pour autoriser un expéditeur usurpé](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a>Scénarios légitimes pour désactiver la détection d’usurpation d’identité

La détection d’usurpation d’identité protégeant mieux les clients contre les attaques par hameçonnage, il est fortement déconseillé de la désactiver. Sa désactivation peut résoudre certains faux positifs à court terme, mais à long terme, vous serez exposé à davantage de risques. Le coût de la configuration de l’authentification côté expéditeur, ou de l’apport d’ajustements aux stratégies anti-hameçonnage, est généralement de quelques événements ponctuels ou ne requiert qu’une maintenance périodique minimale. Par contre, le coût de récupération après une attaque par hameçonnage dans le cadre de laquelle des données ont été exposées ou des ressources compromises est beaucoup plus élevé.
  
C’est pourquoi, il est préférable de s’accommoder de faux positifs de détection d’usurpation d’identité plutôt que de désactiver la protection contre l’usurpation d’identité.
  
Cependant, il existe un scénario légitime dans lequel la détection d’usurpation d’identité devrait être désactivée, à savoir quand il existe des produits de filtrage du courrier supplémentaires dans le routage des messages et qu’Office 365 n’est pas en première ligne dans le chemin d’accès au courrier :
  
![L’enregistrement MX du client ne pointe pas vers Office 365](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
L’autre serveur peut être un serveur de courrier Exchange local, un périphérique de filtrage du courrier tel qu’Ironport ou un autre service hébergé dans le cloud.
  
Si l’enregistrement MX du domaine de destinataire ne pointe pas vers Office 365, il n’est pas nécessaire de désactiver la détection d’usurpation d’identité car Office 365 recherche l’enregistrement MX de votre domaine de destination et supprime la détection d’usurpation d’identité s’il pointe vers un autre service. Si vous ignorez si votre domaine dispose d’un autre serveur frontal, vous pouvez utiliser un site web tel que MX Toolbox pour rechercher l’enregistrement MX. Le résultat pourrait ressembler à ceci :
  
![L’enregistrement MX indique que le domaine ne pointe pas vers Office 365](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
Ce domaine possédant un enregistrement MX qui ne pointe pas vers Office 365, Office 365 n’appliquerait pas la détection d’usurpation d’identité.
  
Toutefois, si l’enregistrement MX du domaine destinataire *pointe* vers Office 365, même s’il existe un autre service devant Office 365, vous devez désactiver la détection d’usurpation d’identité. L’exemple le plus courant est l’utilisation d’une réécriture de destinataire : 
  
![Diagramme de routage pour la réécriture de destinataire](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
L’enregistrement MX du domaine contoso.com pointe vers le serveur local, tandis que l’enregistrement MX du domaine @office365.contoso.net pointe vers Office 365 parce qu’il contient \*.protection.outlook.com ou \*.eo. outlook.com dans l’enregistrement MX :
  
![L’enregistrement MX pointe vers Office 365, donc probablement réécriture de destinataire](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
Veillez à bien distinguer quand un enregistrement MX de domaine de destinataire ne pointe pas vers Office 365 et quand il a subi une réécriture de destinataire. Il est important de faire la différence entre ces deux cas.
  
Si vous ignorez si votre domaine de destination a subi une réécriture de destinataire, vous pouvez parfois le déterminer en examinant les en-têtes dans le message.
  
a) Premièrement, examinez les en-têtes dans le message pour déterminer le domaine du destinataire dans l’en-tête Authentication-Results :
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

Le domaine du destinataire se trouve dans le texte rouge en gras ci-dessus. Il s’agit en l’occurrence d’office365.contoso.net. Cela peut différer du destinataire dans l’en-tête À:.
  
À: Exemple de destinataire \<destinataire @ contoso.com\>
  
Effectuez une recherche dans l’enregistrement MX du domaine de destinataire réel. Si l’enregistrement MX contient \*.protection.outlook.com, mail.messaging.microsoft.com, \*.eo.outlook.com ou mail.global.frontbridge.com, cela signifie qu’il pointe vers Office 365.
  
Si l’enregistrement MX ne contient aucune de ces valeurs, cela signifie qu’il ne pointe pas vers Office 365. Un outil que vous pouvez utiliser pour vérifier ceci est MX Toolbox.
  
Pour cet exemple particulier, ce qui suit indique que contoso.com, le domaine qui ressemble au destinataire puisqu’il s’agit de l’en-tête À:, a un enregistrement MX pointant vers un serveur local :
  
![L’enregistrement MX pointe vers un serveur local](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
Cependant, le destinataire réel est office365.contoso.net dont l’enregistrement MX ne pointe pas vers Office 365 :
  
![L’enregistrement MX pointe vers Office 365, doit être une réécriture de destinataire](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
Par conséquent, ce message a probablement subi une réécriture de destinataire.
  
b) Deuxièmement, veillez à distinguer les cas d’utilisation courants de réécritures de destinataire. Si vous voulez réécrire le domaine du destinataire en \*.onmicrosoft.com, réécrivez-le plutôt en \*.mail.onmicrosoft.com.
  
Une fois que vous avez identifié le domaine du destinataire final qui est routé derrière un autre serveur et si l’enregistrement MX du domaine du destinataire pointe réellement vers Office 365 (comme publié dans ses enregistrements DNS), vous pouvez désactiver la détection d’usurpation d’identité.
  
N’oubliez pas que vous ne souhaitez pas désactiver la détection d’usurpation d’identité si la première ligne du domaine dans le chemin de routage est Office 365, mais uniquement s’il se trouve derrière un ou plusieurs services.
  
### <a name="how-to-disable-anti-spoofing"></a>Comment désactiver la détection d’usurpation d’identité

Si vous avez déjà créé une stratégie anti-hameçonnage, définissez le paramètre EnableAntispoofEnforcement sur $ false :
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false

```

Si vous ne connaissez pas le nom de la stratégie (ou des stratégies) à désactiver, vous pouvez les afficher :
  
```
Get-AntiphishPolicy | fl Name
```

Si vous n’avez pas de stratégie anti-hameçonnage existante, vous pouvez en créer une, puis la désactiver (même si vous n’avez pas de stratégie, la détection d’usurpation d’identité est toujours appliquée; depuis 2018, une stratégie par défaut est créée pour vous, et vous pouvez la désactiver au lieu d’en créer une). Vous devez faire cela en plusieurs étapes :
  
```
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: If the name is more than 64 characters, you will need to choose a smaller one
```

```
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy -RecipientDomainIs $domains
# Finally, scope the anti-phishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false

```

La désactivation de la détection d’usurpation d’identité n’est disponible que via une cmdlet (elle sera disponible ultérieurement dans le Centre de conformité de la sécurité). Si vous n’avez pas accès à PowerShell, créez un ticket de support.
  
N’oubliez pas que cela ne doit s’appliquer qu’à des domaines soumis à un routage indirect lors de l’envoi à Office 365. Résistez à la tentation de désactiver la détection d’usurpation d’identité à cause de certains faux positifs. Il est préférable à long terme de vous en accommoder.
  
### <a name="information-for-individual-users"></a>Informations pour les utilisateurs individuels

Les utilisateurs individuels sont limités dans leurs modes d’interaction avec le conseil de sécurité de détection d’usurpation d’identité. Toutefois, vous disposez de plusieurs options pour résoudre les problèmes rencontrés dans les scénarios courants.
 
### <a name="common-scenario-1---discussion-lists"></a>Scénario courant n°1 - Listes de discussion

Les listes de discussion présentent des problèmes de détection d’usurpation d’identité en raison de la manière dont elles transmettent le message et en modifient le contenu tout en conservant l’adresse De : d’origine.
  
Par exemple, supposez que votre adresse électronique est utilisateur @ contoso.com. L’observation des oiseaux vous intéresse et vous rejoignez la liste de discussion ornithologues @ example.com. Lorsque vous envoyez un message à cette liste de discussion, vous pouvez l’adresser comme suit :
  
**De :** Alexandre Chauvin \<utilisateur @ contoso.com\> 
  
**À :** Liste de discussion des ornithologues \<ornithologues @ example.com\> 
  
**Objet :** Superbe observation de geais bleus au sommet du Mont Rainier. Rainier cette semaine 
  
Quelqu’un veut-il voir l’observation de cette semaine au Mont Rainier. Rainier ?
  
Lorsque la liste des courriers reçoit le message, elle le met en forme, en modifie le contenu et le rediffuse au reste des membres de la liste de discussion composée de nombreux destinataires de courrier différents.
  
**De :** Alexandre Chauvin \<utilisateur @ contoso.com\> 
  
**À :** Liste de discussion des ornithologues \<ornithologues @ example.com\> 
  
**Objet :** [ORNITHOLOGUES] Superbe observation de geais bleus au sommet du Mont Rainier cette semaine. Rainier cette semaine 
  
Quelqu’un veut-il voir l’observation de cette semaine au Mont Rainier. Rainier ?
  
---
  
Ce message a été envoyé à la liste de discussion Ornithologues. Vous pouvez vous désabonner à tout moment.
  
Dans ce qui précède, le message rediffusé a la même adresse De : (utilisateur @ contoso.com), mais le message d’origine a été modifié en ajoutant une balise à la ligne Objet et un pied de page au bas du message. Ce type de modification de message est courant dans les listes de diffusion et peut entraîner des faux positifs.
  
Si vous ou un membre de votre organisation êtes administrateur de la liste de diffusion, vous pouvez peut-être la configurer pour qu’elle passe avec succès les contrôles de détection d’usurpation d’identité.
  
- Consultez le FAQ sur DMARC.org : [I operate a mailing list and I want to interoperate with DMARC, what should I do?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)

- Lisez les instructions de ce billet de blog : [A tip for mailing list operators to interoperate with DMARC to avoid failures](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)

- Songez à installer des mises à jour sur votre serveur de liste de diffusion pour prendre en charge ARC. Pour ce faire, voir [https://arc-spec.org](https://arc-spec.org/).

Si vous n’êtes pas propriétaire de la liste de diffusion :
  
- Vous pouvez demander au responsable de la liste de diffusion d’implémenter l’une des options ci-dessus (l’authentification du courrier doit également être configurée pour le domaine à partir duquel la liste de diffusion est relayée).

- Vous pouvez créer des règles de boîte aux lettres dans votre client de courrier pour déplacer les messages vers la Boîte de réception. Vous pouvez également demander aux administrateurs de votre organisation de configurer des règles d’autorisation ou des contournements, comme décrit dans la section Gestion des expéditeurs légitimes qui envoient du courrier non authentifié.

- Vous pouvez ouvrir un ticket de support auprès d’Office 365 pour créer un contournement afin que la liste de diffusion traite les messages comme légitimes.

### <a name="other-scenarios"></a>Autres scénarios

1. Si aucun des scénarios courants ci-dessus ne s’applique à votre situation, signalez le message comme faux positif à Microsoft. Pour plus d’informations, voir la section [Comment signaler des messages comme étant ou n’étant pas du courrier indésirable à Microsoft ?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) plus loin dans cet article. 

2. Vous pouvez également contacter votre administrateur de courrier qui pourra ouvrir un ticket de support auprès de Microsoft. L’équipe d’ingénierie de Microsoft examinera pourquoi le message a été marqué comme usurpation d’identité.

3. De plus, si vous connaissez l’expéditeur et êtes certain qu’il ne s’agit pas d’une usurpation d’identité malveillante, vous pouvez lui répondre en indiquant qu’il envoie des messages à partir d’un serveur de courrier qui ne s’authentifie pas. Cela a parfois pour conséquence que l’expéditeur d’origine contacte son administrateur informatique pour lui demander de configurer les enregistrements d’authentification de courrier requis.
  
Lorsque suffisamment d’expéditeurs répondent aux propriétaires de domaine qu’ils devraient configurer des enregistrements d’authentification de courrier, cela les incite à agir. Bien que Microsoft collabore avec les propriétaires de domaine pour les inciter à publier les enregistrements requis, c’est encore plus efficace lorsque des utilisateurs individuels le demandent.

4. Ajoutez éventuellement l’expéditeur à votre liste des expéditeurs approuvés. Toutefois, sachez que si un hameçonneur usurpe l’identité ce compte, le courrier sera remis à votre boîte aux lettres. Par conséquent, cette option doit être utilisée avec parcimonie.

## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a>Comment les expéditeurs de Microsoft doivent se préparer à la protection contre l’usurpation d’identité

Si vous êtes un administrateur qui envoie des messages à Microsoft, Office 365 ou Outlook.com, vous devez vous assurer que votre courrier est correctement authentifié, sans quoi il risque d’être marqué comme courrier indésirable ou hameçonnage.
  
### <a name="customers-of-office-365"></a>Clients d’Office 365

Si vous êtes un client Office 365 utilisant Office 365 pour envoyer du courrier :
  
- Pour vos domaines, [configurez SPF dans Office 365 pour empêcher l’usurpation d’identité](set-up-spf-in-office-365-to-help-prevent-spoofing.md).

- Pour vos domaines principaux, [utilisez DKIM pour valider les e-mails sortants envoyés depuis votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).

- [Songez à configurer des enregistrements DMARC](use-dmarc-to-validate-email.md) pour votre domaine afin de déterminer qui sont vos expéditeurs légitimes.

Microsoft ne fournit pas de directives d’implémentation détaillées pour SPF, DKIM et DMARC. Cependant, beaucoup d’informations sont publiées en ligne. Il existe également des sociétés tierces spécialisées dans l’aide à la configuration d’enregistrements d’authentification de courrier.
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a>Administrateurs de domaines qui ne sont pas des clients d’Office 365

Si vous êtes un administrateur de domaine mais n’êtes pas un client d’Office 365 :
  
- Vous devez configurer SPF pour publier les adresses IP d’envoi de votre domaine et configurer DKIM (si disponible) pour signer numériquement les messages. Vous pouvez également envisager de configurer des enregistrements DMARC.

- Si vous avez des expéditeurs de courrier en nombre qui transmettent du courrier pour votre compte, vous devez leur demander d’envoyer le courrier de manière à ce que le domaine d’envoi figurant dans l’adresse De: (s’il vous appartient) corresponde au domaine qui passe le filtrage SPF ou DMARC.

- Si vous avez des serveurs de courrier locaux, ou expédiez du courrier via un fournisseur de logiciel en tant que service, ou via un service d’hébergement dans le cloud tel que Microsoft Azure, GoDaddy, Rackspace, Amazon Web Services ou autre service similaire, vous devez vous assurer que ceux-ci sont ajoutés à votre enregistrement SPF.

- Si vous êtes un petit domaine hébergé par un fournisseur de services Internet, vous devez configurer votre enregistrement SPF conformément aux instructions que celui-ci vous fournit. La plupart des fournisseurs de services Internet donnent ces types d’instructions qui sont disponibles sur leurs pages de support.

- Même si vous n’avez jamais eu à publier d’enregistrements d’authentification de courrier et que tout a toujours bien fonctionné, vous devez impérativement publier des enregistrements d’authentification de courrier pour envoyer à Microsoft. En agissant de la sorte, vous contribuez à la lutte contre le hameçonnage et à la réduction des risques auxquels vous-même et les organisations auxquelles vous envoyez des messages êtes exposés.

### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a>Que faire si vous ignorez qui envoie du courrier au nom de votre domaine ?

De nombreux domaines ne publient pas d’enregistrements SPF car ils ne connaissent pas tous leurs expéditeurs. Pas de souci. Vous n’avez pas besoin de les connaître tous. Au lieu de cela, vous devriez commencer par publier un enregistrement SPF pour ceux que vous connaissez, en spécifiant l’endroit où se trouve votre trafic d’entreprise, et publier une stratégie SPF neutre ?all :
  
example.com IN TXT "v=spf1 include:spf.example.com ?all"
  
La stratégie SPF neutre signifie que tout courrier sortant de votre infrastructure d’entreprise passe par une authentification du courrier chez tous les autres destinataires. Le courrier provenant d’expéditeurs que vous ne connaissez pas est considéré comme neutre, ce qui revient presque à ne publier aucun enregistrement SPF.
  
Lors de l’envoi à Office 365, le courrier provenant du trafic de votre entreprise est marqué comme authentifié, mais celui provenant de sources que vous ne connaissez pas peut être marqué usurpation d’identité (selon qu’Office 365 peut ou non l’authentifier implicitement). Cela constitue cependant toujours une amélioration par rapport à tout le courrier qu’Office 365 marque comme usurpant une identité.
  
Une fois que vous avez démarré avec un enregistrement SPF comprenant une stratégie neutre ?all, vous pouvez progressivement inclure de plus en plus d’infrastructures d’envoi, puis publier une stratégie plus stricte. 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a>Que se passe-t-il si vous êtes le propriétaire d’une liste de diffusion ?

Voir la section [Scénario courant n°1 - Listes de discussion](#common-scenario-1---discussion-lists).
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a>Que se passe-t-il si vous êtes un fournisseur d’infrastructure tel qu’un fournisseur de services Internet (ISP), un fournisseur de services de courrier (ESP) ou un service d’hébergement dans le cloud ?

Si vous hébergez le courrier d’un domaine qui envoie du courrier, ou si vous fournissez une infrastructure d’hébergement capable d’envoyer du courrier, procédez comme suit :
  
- Assurez-vous que vos clients disposent d’une documentation détaillant ce qu’ils doivent publier dans leurs enregistrements SPF.

- Pensez à apposer des signatures DKIM sur le courrier sortant, même si le client ne les a pas explicitement configurées (signature avec un domaine par défaut). Vous pouvez même signer deux fois le courrier avec des signatures DKIM (une fois avec le domaine du client s’il l’a configuré, et une seconde fois avec la signature DKIM de votre organisation).

La remise à Microsoft n’est nullement garantie, même si vous authentifiez le courrier provenant de votre plateforme, mais cela garantit au moins que Microsoft ne considèrera pas votre envoi comme du courrier indésirable parce qu’il n’est pas authentifié. Pour plus d’informations sur la manière dont Outlook.com filtre le courrier, voir la page [Outlook.com Postmaster](https://postmaster.live.com/pm/postmaster.aspx).
  
Pour plus d’informations sur les meilleures pratiques des fournisseurs de services, voir le document [M3AAWG Mobile Messaging Best Practices for Service Providers](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).
  
## <a name="frequently-asked-questions"></a>Forum Aux Questions

### <a name="why-is-microsoft-making-this-change"></a>Pourquoi Microsoft apporte-t-il ce changement ?

En raison de l’impact des attaques par hameçonnage et du fait que l’authentification du courrier existe depuis plus de 15 ans, Microsoft estime que le risque de continuer à autoriser du courrier non authentifié est supérieur au risque de perdre du courrier légitime.
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a>Ce changement aura-t-il pour effet que du courrier légitime sera marqué comme courrier indésirable ?

Au début, certains messages seront marqués comme courrier indésirable. Toutefois, au fil du temps, les expéditeurs s’adapteront et la quantité de messages étiquetés comme usurpation d’identité sera négligeable pour la plupart des chemins de courrier.
  
Microsoft a adopté cette fonctionnalité pour la première fois plusieurs semaines avant de la déployer vers le reste de ses clients. S’il y a eu des perturbations au début, elles ont progressivement diminué.
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a>Microsoft proposera-t-elle cette fonctionnalité aux clients d’Outlook.com et d’Office 365 sans Advanced Threat Protection ?

La technologie de détection d’usurpation d’identité de Microsoft a été initialement déployée vers des organisations qui disposaient d’un abonnement Office 365 Entreprise E5 ou avaient acheté le module complémentaire Office 365 - Protection avancée contre les menaces pour leur abonnement. Depuis octobre 2018, nous avons étendu la protection aux organisations disposant d’Exchange Online Protection. À l’avenir, nous pourrions la publier pour Outlook.com. Cependant, si nous le faisons, il se peut que certaines fonctionnalités ne soient pas appliquées, telles que la génération de rapports et les contournements personnalisés.
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a>Comment signaler des messages comme étant ou n’étant pas du courrier indésirable à Microsoft ?

Vous pouvez utiliser le [complément Signaler un message pour Outlook](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2) ou, s’il n’est pas installé, [envoyer les messages indésirables, légitimes ou de hameçonnage à Microsoft pour analyse](https://technet.microsoft.com/fr-FR/library/jj200769%28v=exchg.150%29.aspx).
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a>Je suis un administrateur de domaine qui ne connaît pas tous ses expéditeurs...

Veuillez consulter [Administrateurs de domaines qui ne sont pas des clients d’Office 365](#administrators-of-domains-that-are-not-office-365-customers).
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a>Que se passe-t-il si je désactive la protection contre l’usurpation d’identité pour mon organisation, même si Office 365 est mon filtre principal ?

Nous vous le déconseillons car vous manquerez davantage de messages de hameçonnage et de courrier indésirable. Tout hameçonnage n’est pas de l’usurpation d’identité, et toutes les usurpations d’identité ne seront pas manquées. Cependant, vous courrez un risque supérieur à celui auquel s’expose un client qui active la détection d’usurpation d’identité.
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a>Activer la protection contre l’usurpation d’identité signifie-t-il que je serai protégé contre tout hameçonnage ?

Malheureusement, non, car les hameçonneurs s’adaptent en recourant à d’autres techniques, telles que la compromission de comptes ou la création de comptes de services gratuits. Cependant, la protection anti-hameçonnage fonctionne beaucoup mieux pour détecter ces autres types de méthodes de hameçonnage, car les couches de protection d’Office 365 sont conçues pour fonctionner ensemble et s’appuyer les unes sur les autres.
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a>Est-ce que d’autres grands destinataires de courrier bloquent le courrier non authentifié ?

Presque tous les grands destinataires de courrier implémentent les filtrages SPF, DKIM et DMARC traditionnels. Certains destinataires disposent d’autres contrôles plus stricts que ces normes, mais rares sont ceux qui vont aussi loin qu’Office 365 pour bloquer le courrier non authentifié et le traiter comme une usurpation d’identité. Cependant, la plupart des entreprises du secteur deviennent de plus en plus strictes avec ce type particulier de courrier, en raison notamment du problème de hameçonnage.
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a>Ai-je toujours besoin d’activer l’option Filtrage avancé du courrier indésirable pour « Enregistrement SPF : échec sévère » si j’active la détection d’usurpation d’identité?

Non, cette option n’est plus requise car la fonction de détection d’usurpation d’identité considère non seulement les échecs sévères SPF, mais aussi un ensemble de critères beaucoup plus large. Si vous avez activé la détection d’usurpation d’identité et l’option Enregistrement SPF : échec sévère, vous obtiendrez probablement davantage de faux positifs. Nous vous recommandons de désactiver cette fonctionnalité car elle ne produirait pratiquement aucune capture supplémentaire de courrier indésirable ou de hameçonnage et générerait plutôt essentiellement des faux positifs.
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a>Est-ce que le Schéma de réécriture de l’expéditeur aide à corriger le problème de courrier transféré ?

Schéma de réécriture de l’expéditeur ne résout que partiellement le problème du courrier transféré. En réécrivant l’en-tête SMTP MAIL FROM, le Schéma de réécriture de l’expéditeur peut s’assurer que le message transféré passe le filtrage SPF à la destination suivante. Cependant, comme la détection d’usurpation d’identité est basée sur l’adresse De : combinée au domaine de signature MAIL FROM ou DKIM (ou à d’autres signaux), cela ne suffit pas pour empêcher le marquage du courrier transféré comme usurpant une identité.
