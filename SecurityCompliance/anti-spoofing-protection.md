---
title: "protection contre l'usurpation d'identité dans Office 365" ms. Author: krowley Author: kccross Manager: laurawi ms. Date: 12/06/2018 ms. audience: professionnel ms. topic: article ms. service: O365-seccomp localization_priority: normal Search. appverid:
- MET150 ms. AssetID: d24bb387-c65d-486e-93e7-06a4f1a436c0 ms. collection:
    - M365-Security-Description de la conformité: «cet article explique comment Office 365 réduit les attaques par hameçonnage qui utilisent des domaines d'expéditeurs falsifiés, c'est-à-dire les domaines qui sont falsifiés. Pour ce faire, il analyse les messages et bloque ceux qui peuvent être authentifiés neithe à l'aide de méthodes d'authentification de messagerie standard ou d'autres techniques de réputation de l'expéditeur. Cette modification est implémentée afin de réduire le nombre d'attaques par hameçonnage dans Office 365 sont exposées à.
---

# <a name="anti-spoofing-protection-in-office-365"></a>Protection anti-usurpation dans Office 365

Cet article explique comment Office 365 atténue les attaques par hameçonnage qui utilisent des domaines d'expéditeurs falsifiés, c'est-à-dire des domaines falsifiés. Pour ce faire, il analyse les messages et bloque ceux qui ne peuvent pas être authentifiés à l'aide de méthodes d'authentification de messagerie standard, ni d'autres techniques de réputation de l'expéditeur. Cette modification est implémentée pour réduire le nombre d'attaques de hameçonnage auxquelles les clients sont exposés.
  
Cet article décrit également la raison pour laquelle cette modification est effectuée, la façon dont les clients peuvent se préparer à ce changement, comment afficher les messages qui seront affectés, comment générer des rapports sur les messages, comment atténuer les faux positifs, ainsi que comment les expéditeurs à Microsoft doivent se préparer à ce problème. port.
  
La technologie de détection d'usurpation de Microsoft a été déployée à l'origine dans ses organisations disposant d'un abonnement Office 365 entreprise E5 ou a acheté le complément Office 365 Advanced Threat Protection (ATP) pour leur abonnement. Depuis octobre 2018, nous avons étendu la protection aux organisations qui possèdent également Exchange Online Protection (EOP). En outre, en raison de la façon dont tous nos filtres apprennent les uns des autres, les utilisateurs de Outlook.com peuvent également être affectés.
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a>Utilisation de l'usurpation dans les attaques par hameçonnage

Lorsqu'il s'agit de protéger ses utilisateurs, Microsoft prend la menace de hameçonnage. L'une des techniques couramment utilisées par les spammeurs et les auteurs de phishing est l'usurpation, c'est-à-dire lorsque l'expéditeur est falsifié et qu'un message semble provenir de quelqu'un ou d'un autre emplacement que la source réelle. Cette technique est souvent utilisée dans les campagnes de hameçonnage conçues pour obtenir des informations d'identification utilisateur. La technologie anti-usurpation de Microsoft examine spécifiquement la contrefaçon de l'en-tête «From:» qui est celle qui s'affiche dans un client de messagerie tel qu'Outlook. Lorsque Microsoft a un niveau de confiance élevé que l'en-tête From: est usurpé, il identifie le message comme une usurpation.
  
Les messages d'usurpation ont deux conséquences négatives pour les utilisateurs réels:
  
### <a name="1-spoofed-messages-deceive-users"></a>1. les messages falsifiés tromper les utilisateurs
  
Tout d'abord, un message usurpé peut inciter un utilisateur à cliquer sur un lien et à donner des informations d'identification, télécharger des programmes malveillants ou répondre à un message avec du contenu sensible (ce qui est connu sous le nom de compromission du courrier électronique professionnel). Par exemple, voici un message de hameçonnage avec un expéditeur usurpé d'msoutlook94@service.outlook.com:
  
![Message d'hameçonnage empruntant une identité service.outlook.com](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
Les éléments ci-dessus ne proviennent pas réellement de service.outlook.com, mais ont été falsifiés par le hameçonnage pour lui donner l'apparence souhaitée. Elle tente de tromper un utilisateur en cliquant sur le lien dans le message.
  
L'exemple suivant est l'usurpation d'contoso.com:
  
![Message de hameçonnage-compromission de la messagerie professionnelle](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
Le message semble légitime, mais en réalité il s'agit d'une usurpation. Ce message de hameçonnage est un type de compromission de la messagerie professionnelle qui est une sous-catégorie du hameçonnage.
    
### <a name="2-users-confuse-real-messages-for-fake-ones"></a>2. les utilisateurs confondent les messages réels pour les fausses
  
Deuxièmement, les messages usurpés créent une incertitude pour les utilisateurs qui connaissent les messages d'hameçonnage, mais ils ne peuvent pas distinguer la différence entre un message réel et un message falsifié. Par exemple, voici un exemple de réinitialisation effective du mot de passe à partir de l'adresse de messagerie du compte de sécurité Microsoft:
  
![Réinitialisation de mot de passe légitime Microsoft](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
Le message ci-dessus provient de Microsoft, mais en même temps, les utilisateurs sont utilisés pour obtenir des messages de hameçonnage susceptibles de tromper un utilisateur en cliquant sur un lien et en donnant ses informations d'identification, en téléchargeant des programmes malveillants ou en répondant à un message avec du contenu sensible. Étant donné qu'il est difficile d'indiquer la différence entre une réinitialisation de mot de passe réelle et une fausse tentative, de nombreux utilisateurs ignorent ces messages, les signalent comme courrier indésirable ou signalent inutilement les messages à Microsoft comme étant des arnaques de hameçonnage manquées.
    
Pour arrêter l'usurpation d'identité, l'industrie de filtrage du courrier électronique a développé des protocoles d'authentification de messagerie, tels que [SPF](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)et [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email). DMARC empêche l'usurpation d'identité de l'expéditeur d'un message, celle que l'utilisateur voit dans son client de messagerie (dans les exemples ci-dessus, il s'agit de service.outlook.com, outlook.com et accountprotection.microsoft.com)-avec le domaine qui a réussi ou DKIM. Autrement dit, le domaine que l'utilisateur voit a été authentifié et n'est donc pas usurpé. Pour une discussion plus complète, consultez la section «*comprendre pourquoi l'authentification de messagerie n'est pas toujours suffisante pour arrêter l'usurpation»* , plus loin dans ce document. 
  
Toutefois, le problème est que les enregistrements d'authentification de messagerie sont facultatifs, et non pas obligatoires. Par conséquent, tandis que les domaines avec des stratégies d'authentification fortes telles que microsoft.com et skype.com sont protégés contre l'usurpation, les domaines qui publient des stratégies d'authentification plus faibles ou aucune stratégie ne sont des cibles à usurper. Depuis le 2018 mars, seuls 9% des domaines des sociétés du Fortune 500 publient des stratégies d'authentification de messagerie fiables. Les 91% restants peuvent être usurpés par un hameçonnage et, sauf si le filtre de courrier électronique les détecte à l'aide d'une autre stratégie, peut être remis à un utilisateur final et le tromper:
  
![Stratégies DMARC des sociétés Fortune 500](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
La proportion des petites et moyennes entreprises qui ne figurent pas dans le Fortune 500 qui publient des stratégies d'authentification de messagerie forte est plus petite et encore plus petite pour les domaines situés en dehors de l'Amérique du Nord et de l'Europe occidentale.
  
Il s'agit d'un problème majeur, car les entreprises n'ont peut-être pas conscience du fonctionnement de l'authentification de messagerie, les auteurs de phishing comprennent et tirent parti de l'absence de service.
  
Pour plus d'informations sur la configuration de SPF, DKIM et DMARC, consultez la section «*clients d'Office 365»* plus loin dans ce document. 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a>Arrêt de l'usurpation avec l'authentification de messagerie implicite

Étant donné que le hameçonnage et le Spear Phishing sont un problème, et en raison de l'adoption limitée de stratégies d'authentification de messagerie fortes, Microsoft continue d'investir dans des fonctionnalités pour protéger ses clients. Par conséquent, Microsoft se déplace vers *l'avant avec l'authentification de messagerie implicite* : si un domaine n'est pas authentifié, Microsoft le traitera comme s'il avait publié des enregistrements d'authentification de messagerie et le traitera en conséquence s'il ne réussit pas. 
  
Pour ce faire, Microsoft a créé de nombreuses extensions à l'authentification de messagerie normale, notamment la réputation de l'expéditeur, l'historique des expéditeurs/destinataires, l'analyse comportementale et d'autres techniques avancées. Un message envoyé à partir d'un domaine qui ne publie pas d'authentification de messagerie sera marqué comme falsifié, sauf s'il contient d'autres signaux pour indiquer qu'il est légitime.
  
En procédant ainsi, les utilisateurs finaux peuvent avoir la certitude qu'un courrier électronique qui leur est envoyé n'a pas été usurpé, mais les expéditeurs peuvent être assurés que personne n'emprunte l'identité de leur domaine, et les clients d'Office 365 peuvent offrir une meilleure protection, comme la protection contre l'emprunt d'identité.
  
Pour consulter l'annonce générale de Microsoft, reportez-vous à [la section Sea of phishing part 2-Enhanced anti-spoofing in Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a>Identification d'un message considéré comme falsifié

### <a name="composite-authentication"></a>Authentification composite

Bien que SPF, DKIM et DMARC soient tout à fait utiles, ils ne communiquent pas suffisamment d'état d'authentification dans l'éventualité où un message n'a pas d'enregistrement d'authentification explicite. Par conséquent, Microsoft a développé un algorithme qui combine plusieurs signaux en une seule valeur appelée authentification composite ou compauth pour Short. Les clients dans Office 365 ont des valeurs compauth indiquées dans l'en-tête *Authentication-Results* dans les en-têtes de message. 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|**Résultat CompAuth**|**Description**|
|:-----|:-----|
|fonctionner|Échec de l'authentification explicite du message (envoi explicite d'enregistrements publiés dans le DNS) ou authentification implicite (le domaine d'envoi n'a pas publié les enregistrements dans le système DNS, de sorte qu'Office 365 interpole le résultat comme s'il avait publié des enregistrements).|
|acceptation|Message passé l'authentification explicite (message passé DMARC, ou [meilleure estimation passée DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) ou authentification implicite avec un niveau de confiance élevé (le domaine d'envoi ne publie pas les enregistrements d'authentification de messagerie, mais Office 365 a des signaux principaux forts vers indiquer que le message est vraisemblablement légitime.|
|softpass|Message passé authentification implicite avec un niveau de confiance faible à moyen (le domaine d'envoi ne publie pas l'authentification de messagerie, mais Office 365 a des signaux principaux pour indiquer que le message est légitime, mais que la force du signal est plus faible).|
|aucune|Le message ne s'est pas authentifié (ou s'il s'est authentifié mais ne s'est pas aligné), mais l'authentification composite n'a pas été appliquée en raison de la réputation de l'expéditeur ou d'autres facteurs.|
   
|||
|:-----|:-----|
|**Reason**|**Description**|
|0XX|Échec de l'authentification composite du message.<br/>**000** signifie que le message a échoué DMARC avec une action de refus ou de mise en quarantaine.  <br/>**001** signifie que le message a échoué à l'authentification de messagerie implicite. Cela signifie que le domaine d'envoi n'a pas publié des enregistrements d'authentification de messagerie électronique, ou si c'est le cas, ils avaient une stratégie d'échec plus faible (échec logiciel SPF ou stratégie neutre DMARC de p = None).<br/>**002** signifie que l'organisation a une stratégie pour la paire d'expéditeurs/domaines qui est explicitement interdite à l'envoi d'un message électronique falsifié, ce paramètre est défini manuellement par un administrateur.  <br/>**010** signifie que le message a échoué DMARC avec une action de refus ou de mise en quarantaine et que le domaine d'envoi est l'un des domaines acceptés de votre organisation (faisant partie de self-to-Self, ou intra-org, l'usurpation).  <br/>le **011** signifie que le message a échoué à l'authentification de messagerie implicite et que le domaine d'envoi est l'un des domaines acceptés de votre organisation (faisant partie de self-to-Self, ou intra-org, l'usurpation).|
|Tous les autres codes (1xx, 2xx, 3xx, 4xx, 5xx)|Correspond à divers codes internes indiquant pourquoi un message a passé l'authentification implicite ou qu'aucune authentification n'a été appliquée.|
   
En examinant les en-têtes d'un message, un administrateur ou un utilisateur final peut déterminer comment Office 365 arrive en conclusion que l'expéditeur peut être usurpé.
  
### <a name="differentiating-between-different-types-of-spoofing"></a>Différenciation entre différents types d'usurpation d'identité

Microsoft différencie deux types différents de messages d'usurpation d'identité:
  
 **Usurpation inter-organisationnelle**
  
Également appelé «usurpation automatique», cela se produit lorsque le domaine de l'adresse de: est le même que le domaine du destinataire ou s'aligne avec celui-ci (lorsque le domaine du destinataire est l'un des [domaines acceptés](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)de votre organisation); ou, lorsque le domaine de l'adresse de: fait partie de la même organisation.
  
Par exemple, l'expéditeur et le destinataire du même domaine (contoso.com) sont les suivants: Des espaces sont insérés dans l'adresse de messagerie pour empêcher spambots récolte sur cette page):
  
From: sender @ contoso.com
  
À: destinataire @ contoso.com
  
Les domaines de l'expéditeur et du destinataire sont alignés sur le domaine de l'organisation (fabrikam.com) de la façon suivante:
  
From: sender @ foo.fabrikam.com
  
À: destinataire @ bar.fabrikam.com
  
Les domaines des expéditeurs et des destinataires suivants sont différents (microsoft.com et bing.com), mais ils appartiennent à la même organisation (c'est-à-dire, tous deux font partie des domaines acceptés de l'organisation):
  
From: sender @ microsoft.com
  
À: destinataire @ bing.com
  
Les messages qui échouent à l'usurpation d'organisation interne contiennent les valeurs suivantes dans les en-têtes:
  
X-Forefront-antispam-Report:... CAT: SPM/HSPM/PHSH;... SFTY: 9.11
  
Le Tao est la catégorie du message, et il est normalement marqué comme SPM (courrier indésirable), mais il peut parfois être HSPM (courrier indésirable à haute fiabilité) ou hameçon (phishing) en fonction des autres types de modèles qui se produisent dans le message.
  
Le SFTY est le niveau de sécurité du message, le premier chiffre (9) signifie que le message est un hameçonnage et un deuxième jeu de chiffres après le point (11) signifie qu'il s'agit d'une usurpation intra-organisation.
  
Il n'existe pas de code de raison spécifique pour l'authentification composite pour l'usurpation intra-organisation, qui sera marqué ultérieurement dans 2018 (chronologie pas encore définie).
  
 **Usurpation d'identité entre domaines**
  
Cela se produit lorsque le domaine d'envoi de l'adresse de: est un domaine externe pour l'organisation destinataire. Les messages dont l'authentification composite échoue en raison d'une usurpation entre domaines contiennent les valeurs suivantes dans les en-têtes:
  
Authentication-Results:... compauth = cause de l'échec = 000/001
  
X-Forefront-antispam-Report:... CAT: USURPATION;... SFTY: 9.22
  
Dans les deux cas, le Conseil de sécurité rouge suivant est marqué dans le message ou un équivalent adapté à la langue de la boîte aux lettres du destinataire:
  
![Conseil de sécurité rouge-détection de fraude](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
Il s'agit uniquement de l'adresse de provenance et de la connaissance de l'adresse de messagerie du destinataire ou de l'examen des en-têtes des messages, que vous pouvez différencier de l'usurpation intra-org et inter-domaines.
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a>Comment les clients d'Office 365 peuvent se préparer à la nouvelle protection contre l'usurpation d'identité

### <a name="information-for-administrators"></a>Informations pour les administrateurs

En tant qu'administrateur d'une organisation dans Office 365, il existe plusieurs informations clés que vous devez connaître.
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a>Comprendre pourquoi l'authentification de messagerie n'est pas toujours suffisante pour arrêter l'usurpation d'identité

La nouvelle protection contre l'usurpation d'identité s'appuie sur l'authentification de messagerie (SPF, DKIM et DMARC) pour ne pas marquer un message comme falsifié. Un exemple courant est le fait lorsqu'un domaine d'envoi n'a jamais publié d'enregistrements SPF. S'il n'y a pas d'enregistrements SPF ou s'ils sont configurés de manière incorrecte, un message envoyé est marqué comme falsifié à moins que Microsoft n'ait une intelligence dorsale indiquant que le message est légitime.
  
Par exemple, avant le déploiement de la fonction de détection d'usurpation d'identité, un message peut s'afficher comme suit sans enregistrement SPF, sans enregistrement DKIM et sans enregistrement DMARC: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
Après la détection d'usurpation d'identité, si vous disposez d'Office 365 entreprise E5, EOP ou ATP, la valeur compauth est marquée:
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

Si example.com le corrige en configurant un enregistrement SPF mais pas un enregistrement DKIM, l'authentification composite est transmise, car le domaine qui a passé SPF s'est aligné sur le domaine dans l'adresse de: 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Ou bien, s'ils configurent un enregistrement DKIM mais pas un enregistrement SPF, l'authentification composite est également transmise, car le domaine dans la signature DKIM qui s'est passé avec le domaine dans l'adresse de:: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Toutefois, un hameçonnage peut également configurer SPF et DKIM et signer le message avec son propre domaine, mais spécifier un domaine différent dans l'adresse de:. Ni SPF, ni DKIM ne requièrent que le domaine s'aligne sur le domaine dans l'adresse de l'expéditeur, de sorte que, sauf si example.com a publié des enregistrements DMARC, il n'est pas marqué comme étant une usurpation à l'aide de DMARC: 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

Dans le client de messagerie (Outlook, Outlook sur le Web ou tout autre client de messagerie), seul le domaine de: est affiché, et non le domaine dans SPF ou DKIM, et cela peut induire l'utilisateur à penser que le message provenait d'example.com, mais provient en réalité de maliciousDomain.com .
  
![Message authentifié, mais de: le domaine ne s'aligne pas sur ce qui a réussi ou sur le DKIM](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
Pour cette raison, Office 365 nécessite que le domaine de l'adresse de: s'aligne sur le domaine dans la signature SPF ou DKIM et, si ce n'est pas le cas, contient d'autres signaux internes indiquant que le message est légitime. Dans le cas contraire, le message est un compauth Fail. 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

Par conséquent, l'usurpation d'identité Office 365 protège contre les domaines sans authentification et par les domaines qui configurent l'authentification mais qui ne correspondent pas au domaine de l'adresse de: comme celle que l'utilisateur voit et pense être l'expéditeur du message. Il s'agit des deux domaines à l'extérieur de votre organisation, ainsi que des domaines au sein de votre organisation.
  
Par conséquent, si vous recevez un message indiquant que l'authentification composite a échoué et qu'elle est usurpée, même si le message a passé SPF et DKIM, c'est que le domaine qui a passé SPF et DKIM n'est pas aligné sur le domaine dans l'adresse de:.
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a>Présentation des modifications apportées au traitement des courriers falsifiés

Actuellement, pour toutes les organisations dans Office 365-ATP et les messages non ATP qui échouent DMARC avec une stratégie de rejet ou de mise en quarantaine sont marqués comme courrier indésirable et prennent généralement l'action de courrier indésirable à niveau de confiance élevé, ou parfois l'action de courrier indésirable normal (selon que d'autres courriers indésirants ou non). les règles les identifient en tant que courrier indésirable). Les détections d'usurpation intra-org prennent l'action de courrier indésirable normale. Il n'est pas nécessaire d'activer ce comportement, ni de le désactiver.
  
Toutefois, pour les messages d'usurpation de domaine, avant que cette modification ne se produise, les vérifications de courrier indésirable, de hameçonnage et de programmes malveillants, et si d'autres parties du filtre les ont identifiées comme suspectes, les marquent comme courrier indésirable, hameçon ou programme malveillant. Avec la nouvelle protection contre l'usurpation d'identité d'un domaine, les messages qui ne peuvent pas être authentifiés effectuent, par défaut, l'action définie dans \> la stratégie anti-usurpation d'identité anti-hameçonnage. Si aucune n'est définie, elle est déplacée vers le dossier courrier inDésirable des utilisateurs. Dans certains cas, le Conseil de sécurité rouge est également ajouté aux messages plus suspects dans le message.
  
Par conséquent, certains messages précédemment marqués comme courrier indésirable sont toujours marqués comme courrier indésirable, mais ils sont également dotés d'un Conseil de sécurité rouge. dans les autres cas, les messages précédemment marqués comme courrier non indésirable commencent à être marqués comme courrier indésirable (CAT: usurpation) avec un Conseil de sécurité rouge ajouté. Dans d'autres cas, les clients qui déplacent l'ensemble du courrier indésirable et du hameçonnage vers la mise en quarantaine verraient le dossier courrier inDésirable (ce comportement peut être modifié, voir [modification de vos paramètres anti-usurpation d'identité](#changing-your-anti-spoofing-settings)).
  
Il existe plusieurs façons d'usurper un message (consultez la rubrique [différenciation entre différents types d'usurpations d'identité](#differentiating-between-different-types-of-spoofing) plus haut dans cet article) mais, depuis mars 2018, la façon dont Office 365 traite ces messages n'est pas encore unifié. Le tableau suivant est un résumé rapide: la protection contre l'usurpation d'identité de domaine est un nouveau comportement: 
  
|**Type d'usurpation d'identité**|**Catégorie**|**Conseil de sécurité ajouté?**|**S'applique à**|
|:-----|:-----|:-----|:-----|
|Échec de DMARC (mise en quarantaine ou rejet)  <br/> |HSPM (valeur par défaut) peut également être défini sur SPM ou PHSH  <br/> |Non (pas encore)  <br/> |Tous les clients Office 365, Outlook.com  <br/> |
|Self-to-Self  <br/> |MONITEUR  <br/> |Oui  <br/> |Toutes les organisations Office 365, Outlook.com  <br/> |
|Entre domaines  <br/> |Tromp  <br/> |Oui  <br/> |Clients Office 365 Advanced Threat Protection et E5  <br/> |
   
### <a name="changing-your-anti-spoofing-settings"></a>Modification de vos paramètres de détection d'usurpation d'identité

Pour créer ou mettre à jour vos paramètres de protection contre l'usurpation d'identité (entre domaines), accédez aux paramètres \> de détection d'usurpation d'identité sous l'onglet \> stratégie de gestion des menaces &amp; dans le centre de sécurité et de conformité. Si vous n'avez jamais créé de paramètres anti-hameçonnage, vous devrez en créer un:
  
![Antiphishing-créer une stratégie](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
Si vous en avez déjà créé un, vous pouvez le sélectionner pour le modifier:
  
![Anti-hameçonnage-modifier la stratégie existante](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
Sélectionnez la stratégie que vous venez de créer et suivez les étapes décrites dans la section [en savoir plus sur les informations d'usurpation d'identité.](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)
  
![Activer ou désactiver l'espionnage](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![Activer ou désactiver les conseils de sécurité contre l'usurpation d'identité](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
Pour créer une nouvelle stratégie via PowerShell, procédez comme suit: 
  
```
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

Vous pouvez ensuite modifier les paramètres de la stratégie anti-hameçonnage à l'aide de PowerShell, en suivant la documentation sur [Set-antiphishpolicy permet](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps). Vous pouvez spécifier le $name en tant que paramètre:
  
```
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

Plus tard dans 2018, au lieu de créer une stratégie par défaut, il est créé pour vous, dont l'étendue est limitée à tous les destinataires de votre organisation, vous n'avez pas à le spécifier manuellement (les captures d'écran ci-dessous peuvent être modifiées avant la mise en œuvre finale).
  
![Stratégie par défaut pour le hameçonnage](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
Contrairement à une stratégie que vous créez, vous ne pouvez pas supprimer la stratégie par défaut, modifier sa priorité ou choisir les utilisateurs, domaines ou groupes auxquels elle doit s'étendre.
  
![Détails de la stratégie anti-hameçonnage par défaut](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
Pour configurer votre protection par défaut via PowerShell, procédez comme suit:
  
```
$defaultAntiphishPolicy = Get-AntiphishPolicy | ? {$_.IsDefault -eq $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

Vous ne devez désactiver la protection contre l'usurpation d'identité que si vous disposez d'un ou de plusieurs serveurs de messagerie devant Office 365 (pour plus de détails, voir scénarios légitimes de désactivation de la détection d'usurpation d'identité). 
  
```
$defaultAntiphishPolicy = Get-AntiphishiPolicy | ? {$_.IsDefault $true}
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> Si le premier tronçon dans le chemin d'accès de votre courrier électronique est Office 365 et que vous recevez trop de courriers électroniques légitimes marqués comme falsifiés, vous devez d'abord configurer vos expéditeurs autorisés à envoyer des messages falsifiés à votre domaine (voir la section *«gestion des expéditeurs légitimes qui envoient des u nauthenticated email»* ). Si vous obtenez toujours trop de faux positifs (par exemple, des messages légitimes marqués comme frauduleux), nous vous déconseillons de désactiver totalement la protection contre l'usurpation d'identité. Au lieu de cela, nous vous recommandons de choisir de base au lieu de protection élevée.                    Il est préférable d'utiliser des faux positifs plutôt que d'exposer votre organisation à des e-mails usurpés, ce qui pourrait entraîner des coûts nettement plus élevés à long terme.

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a>Gestion des expéditeurs légitimes qui envoient des messages électroniques non authentifiés

Office 365 effectue le suivi des personnes qui envoient des messages électroniques non authentifiés à votre organisation. Si le service pense que l'expéditeur n'est pas légitime, il le marque comme une erreur *compauth* . Elle sera classée comme USURPée, même si elle dépend de votre stratégie d'usurpation d'identité appliquée au message. 
  
Toutefois, en tant qu'administrateur, vous pouvez spécifier quels expéditeurs sont autorisés à envoyer des messages falsifiés, en remplaçant la décision d'Office 365.
  
**Méthode 1: Si votre organisation est propriétaire du domaine, configurez l'authentification de messagerie.**
  
Cette méthode peut être utilisée pour résoudre l'usurpation d'identité intra-organisationnelle et l'usurpation inter-domaines dans les cas où vous êtes propriétaire ou interagissez avec plusieurs clients. Il permet également de résoudre l'usurpation d'identité entre les domaines lorsque vous envoyez des e-mails à d'autres clients dans Office 365, ainsi qu'à des tiers hébergés par d'autres fournisseurs.
  
Pour plus d'informations, consultez la rubrique [Customers of Office 365](#customers-of-office-365). 
 
**Méthode 2-utiliser l'intelligence d'usurpation d'identité pour configurer les expéditeurs autorisés d'un message électronique non authentifié**
  
Vous pouvez également utiliser l' [intelligence usurpée](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) pour permettre aux expéditeurs de transmettre des messages non authentifiés à votre organisation. 
  
Pour les domaines externes, l'utilisateur usurpé est le domaine dans l'adresse de l'expéditeur, tandis que l'infrastructure d'envoi est l'adresse IP d'envoi (divisée au/24 plages CIDR) ou le domaine de l'organisation de l'enregistrement PTR (dans la capture d'écran ci-dessous, l'adresse IP d'envoi peut être 131.107.18.4 dont l'enregistrement PTR est outbound.mail.protection.outlook.com, et cela apparaîtra comme outlook.com pour l'infrastructure d'envoi).
  
Pour autoriser cet expéditeur à envoyer des messages électroniques non authentifiés, attribuez la **valeur Oui**à l'option **non** .
  
![Configuration des expéditeurs autorisés de l'antiusurpation d'identité](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
Vous pouvez également utiliser PowerShell pour permettre à un expéditeur spécifique d'usurper votre domaine: 
  
```
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Obtention d'expéditeurs usurpés via PowerShell](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
Dans l'image précédente, des sauts de ligne supplémentaires ont été ajoutés pour que cette capture d'écran s'ajuste, mais en réalité, toutes les valeurs apparaissent sur une seule ligne.
  
Modifiez le fichier et recherchez la ligne correspondant à outlook.com et bing.com, et remplacez l'entrée AllowedToSpoof par oui:
  
![Définition du paramètre autoriser la falsification sur Oui via PowerShell](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
Enregistrez le fichier, puis exécutez: 
  
```
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

Cela permettra à bing.com d'envoyer des messages électroniques non authentifiés \*à partir de. Outlook.com.

**Méthode 3-créer une entrée d'autorisation pour la paire expéditeur/destinataire**
  
Vous pouvez également choisir de contourner tout le filtrage du courrier indésirable pour un expéditeur particulier. Pour plus d'informations, consultez la rubrique relative [à l'ajout sécurisé d'un expéditeur à une liste verte dans Office 365](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/).
  
Si vous utilisez cette méthode, elle ignore le courrier indésirable et certains des filtrages de hameçonnage, mais pas le filtrage des programmes malveillants.
  
**Méthode 4: contactez l'expéditeur et demandez-lui de configurer l'authentification de messagerie**
  
En raison du problème de courrier indésirable et de hameçonnage, Microsoft recommande à tous les expéditeurs de configurer l'authentification de messagerie. Si vous êtes un administrateur du domaine d'envoi, contactez-le et demandez-lui de configurer les enregistrements d'authentification de messagerie de sorte que vous n'ayez pas à ajouter de remplacements. Pour plus d'informations, consultez la section [administrateurs de domaines qui ne sont pas des clients Office 365](#administrators-of-domains-that-are-not-office-365-customers), plus loin dans cet article. 
  
Bien qu'il puisse s'avérer difficile d'obtenir des domaines d'envoi pour l'authentification, au fil du temps, lorsque de plus en plus de filtres de courrier indésirent ou refusent leur courrier, les enregistrements appropriés sont configurés pour garantir une meilleure remise.
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a>Affichage des rapports sur le nombre de messages marqués comme falsifiés

Une fois que votre stratégie d'usurpation d'identité est activée, vous pouvez utiliser Threat Intelligence pour obtenir des chiffres indiquant le nombre de messages marqués comme hameçonnage. Pour ce faire, accédez au centre de &amp; sécurité conformité dans l'Explorateur de gestion \> des menaces, définissez l'affichage sur hameçonnage, et regroupez par domaine de l'expéditeur ou état de protection:
  
![Affichage du nombre de messages marqués comme hameçonnage](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
Vous pouvez interagir avec les différents rapports pour connaître le nombre d'hameçons marqués comme courriers inactifs, y compris les messages marqués comme frauduleux. Pour plus d'informations, reportez-vous à la rubrique [prise en main d'Office 365 Threat Intelligence](https://support.office.com/article/get-started-with-office-365-threat-intelligence-38e9b67f-d188-490f-bc91-a1ae4b270441).
  
Vous ne pouvez pas encore séparer les messages qui ont été marqués en raison d'une usurpation et d'autres types de phishing (hameçonnage général, emprunt d'identité de domaine ou d'utilisateur, etc.). Toutefois, plus loin dans le 2018, vous serez en mesure de le faire via &amp; le centre de sécurité conformité. Une fois que vous avez effectué cette opération, vous pouvez utiliser ce rapport comme emplacement de départ pour identifier les domaines qui peuvent être légitimes et marqués comme des falsifications en raison de l'échec de l'authentification.
  
La capture d'écran suivante est une proposition de l'apparence de ces données, mais peut changer lorsqu'elle est publiée:
  
![Affichage des rapports d'hameçonnage par type de détection](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
Pour les clients non-ATP et E5, ces rapports seront disponibles plus tard dans 2018 sous les rapports sur le statut de protection contre les menaces (TPS), mais seront retardés d'au moins 24 heures. Cette page sera mise à jour au fur et à mesure de &amp; son intégration dans le centre de sécurité conformité.
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a>PréDiction du nombre de messages qui seront marqués comme frauduleux

Plus tard dans 2018, une fois qu'Office 365 a mis à jour ses paramètres pour vous permettre de désactiver l'application d'usurpation d'identité ou en utilisant une application de base ou une contrainte élevée, vous aurez la possibilité de voir le mode de modification de la disposition des messages aux différents paramètres. Autrement dit, si l'anti-usurpation d'identité est désActivée, vous pouvez voir le nombre de messages qui seront détectés comme usurpés si vous activez la fonctionnalité de base; Si elle est de base, vous pourrez voir le nombre d'autres messages à détecter en tant qu'usurpateur si vous le transformez en haute.
  
Cette fonctionnalité est actuellement en cours de développement. À mesure que des détails supplémentaires sont définis, cette page sera mise à jour à la fois avec des captures d'écran du centre de sécurité et de conformité, et avec des exemples PowerShell.
  
![Rapport «What If» pour l'activation de l'antiusurpation](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![EXPÉRIENCE utilisateur possible pour autoriser un expéditeur usurpé](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="understanding-how-spam-phishing-and-advanced-phishing-detections-are-combined"></a>Comprendre le mode de combinaison du courrier indésirable, du hameçonnage et des détections d'hameçonnage avancées

Les organisations qui utilisent Exchange Online, avec ou sans la protection avancée contre les menaces, peuvent spécifier les actions à effectuer lorsque le service identifie les messages comme des programmes malveillants, du courrier indésirable, du courrier indésirable à fiabilité élevée, du hameçonnage et en bloc. Avec les stratégies anti-hameçonnage ATP pour les clients ATP, ainsi que les stratégies anti-hameçonnage pour les clients EOP, et le fait qu'un message peut atteindre plusieurs types de détection (par exemple, les programmes malveillants, le hameçonnage et l'emprunt d'identité de l'utilisateur), il peut y avoir une certaine confusion quant à ce qui la stratégie s'applique. 
  
En règle générale, la stratégie appliquée à un message est identifiée dans l'en-tête X-Forefront-antispam-report de la propriété CAT (Category). 
  
|**Priority (Priorité)**|**Renvoi**|**Catégorie**|**Où géré?**|**S'applique à**|
|:-----|:-----|:-----|:-----|:-----|
|0,1  <br/> |Malware :   <br/> |MALW  <br/> |[Stratégie de programmes malveillants](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|2   <br/> |Hameçonnage  <br/> |PHSH  <br/> |[Stratégie de filtrage de contenu hébergé](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|3   <br/> |Courrier indésirable à probabilité élevée  <br/> |HSPM  <br/> |[Stratégie de filtrage de contenu hébergé](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|4   <br/> |L'usurpation  <br/> |Tromp  <br/> |[Stratégie anti-hameçonnage](https://go.microsoft.com/fwlink/?linkid=864553), aide à l' [usurpation d'identité](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) <br/> |Toutes les organisations  <br/> |
|5   <br/> |Courrier indésirable  <br/> |MONITEUR  <br/> |[Stratégie de filtrage de contenu hébergé](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|6   <br/> |E-mails  <br/> |E-mails  <br/> |[Stratégie de filtrage de contenu hébergé](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|7   <br/> |Emprunt d'identité de domaine  <br/> |DIMP  <br/> |[Stratégie anti-hameçonnage](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |Organisations avec ATP uniquement  <br/> |
|8   <br/> |Emprunt d'identité de l'utilisateur  <br/> |UIMP  <br/> |[Stratégie anti-hameçonnage](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |Organisations avec ATP uniquement <br/> |
   
Si vous disposez de plusieurs stratégies de protection contre le hameçonnage, la priorité la plus élevée s'applique. Par exemple, supposons que vous avez deux stratégies:
  
|**Renvoi**|**Priority (Priorité)**|**Emprunt d'identité d'utilisateur/domaine**|**Protection contre l'usurpation d'identité**|
|:-----|:-----|:-----|:-----|
|A  <br/> |0,1  <br/> |On  <br/> |Off  <br/> |
|B  <br/> |2   <br/> |Off  <br/> |On  <br/> |
   
Si un message arrive et est identifié comme une usurpation et l'emprunt d'identité de l'utilisateur, et que le même ensemble d'utilisateurs est inclus dans la stratégie A et la stratégie B, le message est traité comme une usurpation, mais aucune action n'est appliquée, étant donné que l'anti-usurpation d'identité est désactivée et l'usurpation s'exécute avec une priorité plus élevée (4) que l'emprunt d'identité d'utilisateur (8).
  
Pour appliquer d'autres types de stratégies de hameçonnage, vous devrez ajuster les paramètres d'application des différentes stratégies.
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a>Scénarios légitimes pour désactiver la détection d'usurpation d'identité

La protection contre l'usurpation d'identité protège les clients contre les attaques par hameçonnage et, par conséquent, la désactivation de la protection contre l'usurpation d'identité est fortement déconseillée. En le désactivant, vous pouvez résoudre certains faux positifs à court terme, mais à long terme, vous serez exposé à davantage de risques. Le coût de configuration de l'authentification côté expéditeur ou d'ajustements dans les stratégies de hameçonnage est généralement un événement unique ou nécessite uniquement une maintenance périodique minimale. Toutefois, le coût de récupération d'une attaque par hameçonnage dans laquelle les données ont été exposées ou les ressources ont été compromis est bien plus élevé.
  
Pour cette raison, il est préférable d'utiliser des faux positifs d'usurpation d'identité plutôt que de désactiver la protection contre l'usurpation d'identité.
  
Toutefois, il existe un scénario légitime où l'anti-usurpation d'identité doit être désactivée, et c'est le cas lorsqu'il y a des produits de filtrage du courrier supplémentaires dans le routage des messages, et Office 365 n'est pas le premier tronçon dans le chemin d'accès du courrier électronique:
  
![L'enregistrement MX du client ne pointe pas vers Office 365](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
L'autre serveur peut être un serveur de messagerie Exchange local, un périphérique de filtrage de messagerie tel qu'IronPort ou un autre service hébergé sur le Cloud.
  
Si l'enregistrement MX du domaine du destinataire ne pointe pas vers Office 365, il n'est pas nécessaire de désactiver l'usurpation d'identité, car Office 365 recherche l'enregistrement MX de votre domaine de réception et supprime l'usurpation d'identité s'il pointe vers un autre service. Si vous ne le faites pas si votre domaine dispose d'un autre serveur, vous pouvez utiliser un site Web comme MX boîte à outils pour Rechercher l'enregistrement MX. Cela peut dire ce qui suit:
  
![L'enregistrement MX indique que le domaine ne pointe pas vers Office 365](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
Ce domaine a un enregistrement MX qui ne pointe pas vers Office 365, de sorte qu'Office 365 n'applique pas l'application d'usurpation d'identité.
  
Toutefois, si l'enregistrement MX du domaine du destinataire ** pointe vers Office 365, même s'il existe un autre service devant Office 365, vous devez désactiver la détection d'usurpation d'identité. L'exemple le plus courant consiste à utiliser la réécriture d'un destinataire: 
  
![Diagramme de routage pour la réécriture de destinataires](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
L'enregistrement MX du domaine contoso. com pointe vers le serveur local, tandis que l'enregistrement MX du domaine @office365. contoso. net pointe vers Office 365 car il contient \*. protection.Outlook.com ou \*. eo.Outlook.com dans l'enregistrement MX:
  
![L'enregistrement MX pointe vers Office 365, par conséquent probablement la réécriture des destinataires](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
N'oubliez pas de distinguer lorsque l'enregistrement MX d'un domaine du destinataire ne pointe pas vers Office 365 et lorsqu'il a subi une réécriture de destinataire. Il est important de déterminer la différence entre ces deux cas.
  
Si vous ne savez pas si votre domaine de réception a subi une réécriture de destinataire, vous pouvez parfois en examiner les en-têtes.
  
a) d'abord, examinez les en-têtes du message pour le domaine du destinataire dans l'en-tête Authentication-Results: 
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

Le domaine du destinataire est indiqué en gras en gras au-dessus, dans ce cas office365.contoso.net. Cela peut être différent pour le destinataire de l'en-tête to::
  
Vers: exemple de \<destinataire de destinataire @ contoso.com\>
  
Effectuer une recherche de l'enregistrement MX du domaine du destinataire réel. S'il contient \*. protection.outlook.com, mail.Messaging.Microsoft.com, \*. eo.Outlook.com ou mail.global.FrontBridge.com, le MX pointe vers Office 365.
  
S'il ne contient pas ces valeurs, cela signifie que MX ne pointe pas vers Office 365. Vous pouvez utiliser un outil pour vérifier qu'il s'agit de la boîte à outils MX.
  
Pour cet exemple particulier, le code suivant indique que contoso.com, le domaine qui ressemble au destinataire, étant donné qu'il s'agissait de l'en-tête to:, qu'il pointe vers un serveur sur local:
  
![L'enregistrement MX pointe vers le serveur local](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
Toutefois, le destinataire réel est office365.contoso.net dont l'enregistrement MX pointe vers Office 365:
  
![MX pointe vers Office 365, doit être réécrite pour le destinataire](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
Par conséquent, ce message a probablement subi une réécriture de destinataire.
  
b) Deuxièmement, veillez à bien faire la distinction entre les cas d'utilisation courants des réécrits de destinataires. Si vous envisagez de réécrire le domaine du \*destinataire dans. onmicrosoft.com, vous devez le \*réécrire dans. mail.onmicrosoft.com.
  
Une fois que vous avez identifié le domaine de destinataire final qui est acheminé derrière un autre serveur et que l'enregistrement MX du domaine du destinataire pointe en fait vers Office 365 (tel que publié dans ses enregistrements DNS), vous pouvez désactiver la détection d'usurpation d'identité.
  
N'oubliez pas de désactiver l'usurpation d'identité si le premier tronçon du domaine dans le chemin de routage est Office 365, uniquement lorsqu'il est derrière un ou plusieurs services.
  
### <a name="how-to-disable-anti-spoofing"></a>Procédure de désactivation de l'usurpation d'identité

Si vous avez déjà créé une stratégie anti-hameçonnage, définissez le paramètre EnableAntispoofEnforcement sur $false: 
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false 

```

Si vous ne connaissiez pas le nom de la ou des stratégies à désactiver, vous pouvez les afficher: 
  
```
Get-AntiphishPolicy | fl Name
```

Si vous n'avez pas de stratégies anti-hameçonnage existantes, vous pouvez en créer une, puis la désactiver (même si vous n'avez pas de stratégie, la détection d'usurpation d'identité est toujours appliquée; ensuite, une stratégie par défaut sera créée pour vous, puis désactivez-la au lieu d'en créer une). . Vous devrez effectuer cette opération en plusieurs étapes: 
  
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
# Finally, scope the antiphishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false 

```

La désActivation de la détection d'usurpation d'identité est uniquement disponible via la cmdlet (plus loin dans le 2ème trimestre &amp; 2018, elle sera disponible dans le centre de sécurité conformité). Si vous n'avez pas accès à PowerShell, créez un ticket de support.
  
N'oubliez pas que cette application doit être appliquée uniquement aux domaines qui subissent un routage indirect lors de l'envoi vers Office 365. Résistez à la tentation de désactiver la détection d'usurpation d'identité en raison de certains faux positifs, il sera préférable de le faire à long terme.
  
### <a name="information-for-individual-users"></a>Informations pour les utilisateurs individuels

Les utilisateurs individuels sont limités dans la façon dont ils peuvent interagir avec le Conseil de sécurité d'usurpation d'identité. Toutefois, il existe plusieurs choses que vous pouvez faire pour résoudre des scénarios courants.
  
### <a name="common-scenario-1---mailbox-forwarding"></a>#1 de scénario courant-transfert de boîte aux lettres

Si vous utilisez un autre service de messagerie et transférez votre courrier électronique vers Office 365 ou Outlook.com, votre courrier peut être marqué comme une usurpation d'identité et recevoir un Conseil de sécurité rouge. Office 365 et Outlook.com plan pour résoudre ce cas automatiquement lorsque le redirecteur est l'un des Outlook.com, Office 365, Gmail ou tout autre service qui utilise le [protocole arc](https://arc-spec.org). Toutefois, jusqu'à ce que ce correctif soit déployé, les utilisateurs doivent utiliser la fonctionnalité comptes connectés pour importer leurs messages directement au lieu d'utiliser l'option de transfert.
  
Pour configurer des comptes connectés dans Office 365, sélectionnez l'icône d'engrenage dans le coin supérieur droit \> des comptes de \> messagerie \> \> de messagerie de l'interface Web Office 365.
  
![Office 365-option de comptes connectés](media/e8e841ca-8861-4d83-8506-2a0858c51010.jpg)
  
Dans Outlook.com \> , le processus est l'icône d'engrenages comptes de \> messagerie \> \> connectés.
  
### <a name="common-scenario-2---discussion-lists"></a>#2 de scénario courants-listes de discussion

Les listes de discussion sont connues pour rencontrer des problèmes avec la détection d'usurpation d'identité en raison de la façon dont elles transfèrent le message et modifient son contenu mais conserve l'adresse de provenance:.
  
Par exemple, supposons que votre adresse e-mail est user @ contoso.com et que vous êtes intéressé par les oiseaux et que vous joignez la liste de discussion birdwatchers @ example.com. Lorsque vous envoyez un message à la liste de discussion, vous pouvez l'envoyer de la manière suivante:
  
**À partir de:** John Doe \<user @ contoso.com\> 
  
**À:** Liste \<de discussion de Birdwatcher birdwatchers @ example.com\> 
  
**Objet:** Affichage parfait de Jays bleus en haut de Mt. Rainier cette semaine 
  
Quiconque souhaite consulter cette semaine à partir de Mt. Rainier?
  
Lorsque la liste de messages électroniques reçoit le message, il met en forme le message, modifie son contenu et le rejoue sur le reste des membres de la liste de discussion qui est composé de participants provenant de nombreux récepteurs de messagerie différents.
  
**À partir de:** John Doe \<user @ contoso.com\> 
  
**À:** Liste \<de discussion de Birdwatcher birdwatchers @ example.com\> 
  
**Objet:** [BIRDWATCHERS] Affichage parfait de Jays bleus en haut de Mt. Rainier cette semaine 
  
Quiconque souhaite consulter cette semaine à partir de Mt. Rainier?
  
---
  
Ce message a été envoyé à la liste de discussion birdwatchers. Vous pouvez annuler votre abonnement à tout moment.
  
Dans ce qui précède, le message rediffusé a la même adresse que: Address (user @ contoso.com), mais le message d'origine a été modifié en ajoutant une balise à la ligne d'objet et un pied de page en bas du message. Ce type de modification de message est courant dans les listes de publipostage et peut entraîner des faux positifs.
  
Si vous ou une personne de votre organisation est un administrateur de la liste de distribution, vous pouvez peut-être la configurer pour qu'elle transmette des contrôles d'usurpation d'identité.
  
- Consultez le Forum aux questions sur DMARC.org: [j'utilise une liste de publipostage et je souhaite interagir avec DMARC, que dois-je faire?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)
    
- Lisez les instructions de ce billet de blog: [Conseil pour les opérateurs de liste de publipostage pour interagir avec DMARC afin d'éviter les défaillances](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)
    
- EnVisagez d'installer des mises à jour sur votre serveur de listes de distribution pour prendre en charge ARC, consultez[https://arc-spec.org](https://arc-spec.org/)
    
Si vous n'êtes pas propriétaire de la liste de publipostage:
  
- Vous pouvez demander au responsable de la liste de publipostage d'implémenter l'une des options ci-dessus (elles doivent également configurer l'authentification de messagerie pour le domaine à partir duquel la liste de publipostage rerelaie).
    
- Vous pouvez créer des règles de boîte aux lettres dans votre client de messagerie pour déplacer des messages vers la boîte de réception. Vous pouvez également demander aux administrateurs de votre organisation de configurer des règles d'autorisation ou des remplacements comme décrit dans la section gestion des expéditeurs légitimes qui envoient des messages électroniques non authentifiés.
    
- Vous pouvez créer un ticket de support avec Office 365 pour créer un remplacement pour la liste de publipostage afin de la traiter comme légitime
    
### <a name="other-scenarios"></a>Autres scénarios

1. Si aucun des scénarios courants ci-dessus ne s'applique à votre situation, signalez le message comme faux positif à Microsoft. Pour plus d'informations, reportez-vous à la section Comment puis-je signaler des courriers indésirables [ou des messages non indésirables à Microsoft?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) plus loin dans cet article. 
    
2. Vous pouvez également contacter votre administrateur de messagerie qui peut le déclencher en tant que ticket de support avec Microsoft. L'équipe d'ingénierie Microsoft examinera pourquoi le message a été marqué comme falsifié.
    
3. De plus, si vous savez qui est l'expéditeur et qu'il est sûr qu'il n'est pas usurpé par malveillance, vous pouvez répondre à l'expéditeur indiquant qu'il envoie des messages à partir d'un serveur de messagerie qui ne s'authentifie pas. Il en résulte parfois que l'expéditeur d'origine contacte son administrateur informatique qui configurera les enregistrements d'authentification de messagerie requis.
  
Lorsque suffisamment d'expéditeurs répondent à des propriétaires de domaine pour configurer des enregistrements d'authentification de messagerie, il les Spurs en cours d'exécution. Bien que Microsoft travaille également avec les propriétaires de domaine pour publier les enregistrements requis, il est encore plus utile lorsque des utilisateurs individuels le demandent.
    
4. Vous pouvez également ajouter l'expéditeur à votre liste des expéditeurs approuvés. Toutefois, sachez que si un hameçonnage usurpe ce compte, il sera remis à votre boîte aux lettres. Par conséquent, cette option doit être utilisée avec modération.
    
## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a>Comment les expéditeurs de Microsoft doivent se préparer à la protection contre l'usurpation d'identité

Si vous êtes un administrateur qui envoie des messages à Microsoft, qu'il s'agisse d'Office 365 ou Outlook.com, vous devez vous assurer que votre courrier électronique est correctement authentifié, sinon il peut être marqué comme courrier indésirable ou hameçon. 
  
### <a name="customers-of-office-365"></a>Clients d'Office 365

Si vous êtes un client Office 365 et que vous utilisez Office 365 pour envoyer des e-mails sortants:
  
- Pour vos domaines, [configurez SPF dans Office 365 pour éviter l'usurpation](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing)
    
- Pour vos domaines principaux, [Utilisez DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email)
    
- EnVisagez de [configurer des enregistrements DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email) pour votre domaine afin de déterminer les personnes qui sont vos expéditeurs légitimes 
    
Microsoft ne fournit pas d'instructions d'implémentation détaillées pour chaque SPF, DKIM et DMARC. Toutefois, il existe un grand nombre d'informations publiées en ligne. Il existe également des sociétés tierces dédiées pour aider votre organisation à configurer les enregistrements d'authentification de messagerie.
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a>Administrateurs de domaines qui ne sont pas des clients Office 365

Si vous êtes un administrateur de domaine, mais qu'il ne s'agit pas d'un client Office 365:
  
- Vous devez configurer SPF pour publier les adresses IP d'envoi de votre domaine et configurer DKIM (le cas échéant) pour signer numériquement les messages. Vous pouvez également configurer des enregistrements DMARC.
    
- Si vous avez des expéditeurs en bloc qui transmettent des courriers électroniques à votre place, vous devez les utiliser pour envoyer des courriers électroniques de sorte que le domaine d'envoi de l'adresse de: (s'il vous appartient) s'aligne sur le domaine qui transmet SPF ou DMARC.
    
- Si vous avez des serveurs de messagerie locaux ou que vous envoyez des messages à partir d'un fournisseur de logiciels en tant que service ou d'un service d'hébergement de Cloud tel que Microsoft Azure, GoDaddy, Rackspace, Amazon Web services ou similaire, vous devez vous assurer qu'ils sont ajoutés à votre enregistrement SPF.
    
- Si vous êtes un petit domaine hébergé par un fournisseur de services Internet, vous devez configurer votre enregistrement SPF conformément aux instructions fournies par votre fournisseur de services Internet. La plupart des fournisseurs de service Internet fournissent ces types d'instructions et sont accessibles sur les pages de support de l'entreprise.
    
- Même si vous n'avez pas dû publier des enregistrements d'authentification de courrier électronique avant et que cela fonctionnait correctement, vous devez toujours publier des enregistrements d'authentification de courrier électronique à envoyer à Microsoft. En procédant ainsi, vous participez à la lutte contre le hameçonnage et vous réduisez la possibilité que vous ou les organisations vers lesquelles vous envoyez des e-mails soient hameçons.
    
### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a>Que faire si vous ne connaissez pas les personnes qui envoient des messages électroniques en tant que votre domaine?

De nombreux domaines ne publient pas d'enregistrements SPF, car ils ne connaissent pas tous leurs expéditeurs. C'est possible, vous n'avez pas besoin de vous en informer. Au lieu de cela, vous devez commencer par publier un enregistrement SPF pour ceux que vous savez, en particulier où se trouve votre trafic d'entreprise, et publier une stratégie SPF neutre? All:
  
example.com dans TXT "v = spf1 include include. example. com? All"
  
La stratégie SPF neutre signifie que tout courrier électronique qui sort de votre infrastructure d'entreprise passera l'authentification de courrier électronique à tous les autres destinataires. Les messages électroniques provenant d'expéditeurs dont vous n'êtes pas informé seront redirigés vers le système de messagerie neutre, qui est quasiment identique à la publication d'aucun enregistrement SPF.
  
Lors de l'envoi à Office 365, les messages électroniques provenant de votre trafic d'entreprise seront marqués comme étant authentifiés, mais les messages provenant de sources que vous ne connaissiez pas peuvent toujours être marqués comme frauduleux (selon que Office 365 peut ou non l'authentifier de manière implicite). Toutefois, il s'agit toujours d'une amélioration de tous les messages électroniques marqués comme usurpés par Office 365.
  
Une fois que vous avez commencé à utiliser un enregistrement SPF avec une stratégie de secours de? tout, vous pouvez inclure progressivement de plus en plus d'infrastructure d'envoi, puis publier une stratégie plus stricte. 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a>Que faire si vous êtes le propriétaire d'une liste de publipostage?

Consultez la section [scénario courant #2-listes de discussion](#common-scenario-2---discussion-lists). 
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a>Que se passe-t-il si vous êtes un fournisseur d'infrastructure tel qu'un fournisseur de services Internet, un fournisseur de services de messagerie (ESP) ou un service d'hébergement de Cloud?

Si vous hébergez le courrier électronique d'un domaine, qu'il envoie des courriers électroniques ou une infrastructure d'hébergement pouvant envoyer des courriers électroniques, vous devez effectuer les opérations suivantes:
  
- Vérifier que vos clients disposent d'une documentation décrivant les éléments à publier dans leurs enregistrements SPF
    
- EnVisagez de signer les signatures DKIM sur les messages sortants même si le client ne le configure pas explicitement (signez-le à l'aide d'un domaine par défaut). Vous pouvez même signer le courrier électronique à l'aide de signatures DKIM (une seule fois avec le domaine du client s'il l'a configurée, puis une deuxième fois avec la signature DKIM de votre entreprise).
    
La remise à Microsoft n'est pas garantie même si vous authentifiez le courrier électronique provenant de votre plateforme, mais qu'il garantit au moins que Microsoft ne peut pas légitimer votre courrier électronique, car il n'est pas authentifié. Pour plus d'informations sur la façon dont Outlook.com filtre les messages électroniques, consultez la [page Outlook.com postmaster](https://postmaster.live.com/pm/postmaster.aspx).
  
Pour plus d'informations sur les meilleures pratiques en matière de fournisseurs de services, consultez la rubrique [M3AAWG mobile messagIng Best Practices for Service](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf)Providers.
  
## <a name="frequently-asked-questions"></a>Forum Aux Questions

### <a name="why-is-microsoft-making-this-change"></a>Pourquoi Microsoft apporte-t-il cette modification?

En raison de l'impact des attaques par hameçonnage et de l'authentification de messagerie depuis plus de 15 ans, Microsoft pense que le risque de continuer à autoriser le courrier non authentifié est plus élevé que le risque de perdre des messages légitimes.
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a>Cette modification entraîne-t-elle le marquage du courrier légitime comme courrier indésirable?

Dans un premier temps, certains messages seront marqués comme courrier indésirable. Toutefois, au fil du temps, les expéditeurs ajusteront, puis la quantité de messages ayant été labellisés comme falsifiés sera négligeable pour la plupart des chemins d'accès.
  
Microsoft a d'abord adopté cette fonctionnalité plusieurs semaines avant de la déployer sur le reste de ses clients. Bien qu'il y ait une interruption en premier, il a progressivement baissé.
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a>Est-ce que Microsoft mettra cette fonctionnalité à Outlook.com et aux clients de protection contre les menaces de Microsoft Office 365?

La technologie de détection d'usurpation de Microsoft a été déployée à l'origine dans ses organisations disposant d'un abonnement Office 365 entreprise E5 ou a acheté le complément Office 365 Advanced Threat Protection (ATP) pour leur abonnement. Depuis octobre 2018, nous avons étendu la protection aux organisations qui possèdent également Exchange Online Protection (EOP). À l'avenir, nous pouvons le publier pour Outlook.com. Toutefois, dans ce cas, certaines fonctionnalités ne sont pas appliquées, telles que la création de rapports et les substitutions personnalisées.
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a>Comment puis-je signaler des courriers indésirables ou des messages non indésirables à Microsoft?

Vous pouvez utiliser le [complément de message de rapport pour Outlook](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2), ou s'il n'est pas installé, soumettre des messages de courrier indésirable, de courrier [non indésirable et de hameçonnage à Microsoft pour analyse](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx).
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a>Je suis un administrateur de domaine qui ne connaît pas tous mes expéditeurs!

Veuillez consulter [les administrateurs de domaines qui ne sont pas des clients Office 365](#administrators-of-domains-that-are-not-office-365-customers).
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a>Que se passe-t-il si je désactive la protection contre l'usurpation d'identité pour mon organisation, même si Office 365 est mon filtre principal?

Nous vous déconseillons de le faire car vous serez exposé à d'autres messages de hameçonnage et de courrier indésirable. Tout le hameçonnage n'est pas usurpé, et toutes les usurpations ne seront pas manquées. Toutefois, votre risque est supérieur à celui d'un client qui active la détection d'usurpation d'identité.
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a>Est-ce que l'activation de la protection contre l'usurpation d'identité signifie que je suis protégé contre tous les tentatives de hameçonnage?

Malheureusement, non, car les auteurs de phishing s'adaptent à d'autres techniques telles que les comptes compromis ou à la configuration des comptes de services gratuits. Toutefois, la protection anti-hameçonnage est bien plus efficace pour détecter ces autres types de méthodes de hameçonnage car les couches de protection d'Office 365 sont conçues conjointement et s'imbriquent les unes sur les autres.
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a>D'autres récepteurs de courrier volumineux bloquent-ils le courrier électronique non authentifié?

Presque tous les grands récepteurs de courrier électronique mettent en œuvre SPF, DKIM et DMARC. Certains récepteurs ont d'autres vérifications qui sont plus strictes que les seules normes, mais il n'est pas nécessaire d'utiliser Office 365 pour bloquer les messages électroniques non authentifiés et les traiter comme une usurpation. Toutefois, la plupart du secteur d'activité est de plus en plus strict sur ce type particulier de courrier électronique, en particulier en raison du problème de hameçonnage.
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a>Est-ce que j'ai toujours besoin de l'option avancée de filtrage du courrier inDésirable pour «échec matériel SPF» si j'active la détection d'usurpation d'identité?

Non, cette option n'est plus nécessaire, car la fonctionnalité de détection d'usurpation d'identité ne prend pas en compte le blocage de SPF, mais un ensemble plus large de critères. Si la détection d'usurpation d'identité est activée et que l'option SPF non activable est activée, vous obtiendrez probablement plus de faux positifs. Nous vous recommandons de désactiver cette fonctionnalité, car elle ne fournirait presque aucune capture supplémentaire pour le courrier indésirable ou le hameçonnage et générera plutôt des faux positifs.
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a>Est-ce que le modèle de réécriture d'expéditeur (SRS) permet de réparer le courrier transféré?

Le service SRS corrige partiellement le problème de la transmission du courrier électronique. En réécrivant le courrier SMTP à partir de, le service SRS peut s'assurer que le message transféré passe par SPF à la destination suivante. Toutefois, étant donné que la détection d'usurpation d'identité est basée sur l'adresse de l'expéditeur en combinaison avec le domaine de messagerie ou le domaine de signature DKIM (ou d'autres signaux), il n'est pas suffisant d'empêcher le marquage du courrier transféré comme falsifié.
  

