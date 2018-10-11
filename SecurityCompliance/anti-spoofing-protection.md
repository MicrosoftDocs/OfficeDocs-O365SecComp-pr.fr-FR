---
title: Protection anti-usurpation dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/11/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
description: Cet article explique comment Office 365 atténue contre les attaques par hameçonnage qu’utilise falsifié expéditeur domaines, c'est-à-dire, qui sont usurpés. Pour ce faire, il analyse les messages et le blocage de celles qui peuvent être authentifiés neithe à l’aide des méthodes d’authentification standard de courrier électronique, ni les autres techniques de réputation de l’expéditeur. Cette modification est en cours implémentée pour réduire le nombre d’organisations dans Office 365 sont affichent dans les attaques par phishing.
ms.openlocfilehash: 37eddfcad9bc5e412f62dd857178eafa8cac9355
ms.sourcegitcommit: ba2175e394d0cb9f8ede9206aabb44b5b677fa0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/11/2018
ms.locfileid: "25496898"
---
# <a name="anti-spoofing-protection-in-office-365"></a>Protection anti-usurpation dans Office 365

Cet article explique comment Office 365 atténue contre les attaques par hameçonnage qu’utilise falsifié expéditeur domaines, c'est-à-dire, qui sont usurpés. Il y parvient en analysant les messages et de blocage de ceux qui ne peuvent pas être authentifiés à l’aide des méthodes d’authentification standard de courrier électronique, ni les autres techniques de réputation de l’expéditeur. Cette modification est en cours implémentée pour réduire le nombre de clients sont exposés à des attaques de phishing.
  
Cet article décrit également pourquoi ce changement est effectué, comment les clients peuvent préparer à cette modification, comment afficher les messages qui seront affectés, comment créer des rapports sur les messages, comment limiter le nombre de faux positifs, ainsi que comment expéditeurs à Microsoft doivent préparer modifier.
  
La technologie anti-usurpation de Microsoft a été initialement déployée à ses organisations qui avaient un abonnement à Office 365 entreprise E5 ou avaient acheté module complémentaire de leur abonnement Office 365 Advanced Threat Protection (DAV). À compter d’octobre, 2018, nous avons étendu la protection pour les organisations ayant ainsi que Exchange Online Protection (EOP). En outre, en raison de la manière que tous nos filtres Découvrez chacun des autres utilisateurs Outlook.com peuvent également être affectées.
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a>Utilisation de l’usurpation d’identité dans les attaques par hameçonnage

Lorsqu’il s’agit de protéger ses utilisateurs, Microsoft prend les menaces de phishing sérieusement. Une des techniques qui spam et phishing utilisent couramment usurpation, lorsque l’expéditeur est falsifié et un message s’affiche pour provenir d’une personne ou un endroit autre que la source réelle. Cette technique est souvent utilisée dans les campagnes de phishing conçus pour obtenir des informations d’identification de l’utilisateur. Technologie de blocage usurpation d’identité de Microsoft examine spécifiquement contrefaçon de la « à partir de : en-tête » qui est celui qui s’affiche dans le client de messagerie électronique comme Outlook. Lorsque Microsoft a le niveau de confiance élevé qui From : en-tête est faux, il identifie le message comme une usurpation d’identité.
  
Messages d’usurpation des deux répercussions utilisateurs réels :
  
### <a name="1-spoofed-messages-deceive-users"></a>1. messages usurpés intercepter les utilisateurs
  
Tout d’abord, un message usurpé peut-être amener un utilisateur en cliquant sur un lien et abandonner leurs informations d’identification, le téléchargement de logiciels malveillants ou répondre à un message avec contenu sensible (la dernière est appelée Business messagerie compromis). Par exemple, Voici un message de phishing avec un expéditeur usurpé de msoutlook94@service.outlook.com :
  
![Hameçonnage service.outlook.com à emprunt d’identité](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
La commande ci-dessus ne provient pas réellement de service.outlook.com, mais au lieu de cela, a été falsifiés par l’auteur du phishing à lui donner comme. Il tente d’amener un utilisateur en cliquant sur le lien dans le message.
  
L’exemple suivant est l’usurpation d’identité contoso.com :
  
![Hameçonnage - business messagerie compromis](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
Le message semble fiable, mais est en fait une usurpation d’identité. Ce message d’hameçonnage est un type de compromission de messagerie entreprise qui est une sous-catégorie de hameçonnage.
    
### <a name="2-users-confuse-real-messages-for-fake-ones"></a>2. messages réels pour ceux faux confondez pas utilisateurs
  
Deuxième messages usurpés créer incertitude pour les utilisateurs qui savoir à propos de hameçonnage, mais ne peut pas faire la différence entre un message réel et usurpés. Par exemple, Voici un exemple d’un mot de passe réinitialisé à partir de l’adresse de messagerie du compte Microsoft Security :
  
![Réinitialisation du mot de passe légitimes Microsoft](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
Le message ci-dessus provient de Microsoft, mais en même temps, les utilisateurs sont utilisés pour l’obtention de messages de phishing qui peut-être amener un utilisateur en cliquant sur un lien et abandonner leurs informations d’identification, le téléchargement de logiciels malveillants ou répondre à un message avec du contenu sensible. Comme il est difficile de déterminer la différence entre une réinitialisation du mot de passe réel et un substitut un grand nombre d’utilisateurs ignore ces messages, les signaler comme courrier indésirable ou inutilement compte-rendu les messages à Microsoft en tant que hameçonnage manqués.
    
Pour arrêter l’usurpation d’identité, le courrier électronique du secteur de filtrage a développé des protocoles d’authentification électronique comme [SPF](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx), [DKIM](https://technet.microsoft.com/en-us/library/mt695945%28v=exchg.150%29.aspx)et [DMARC](https://technet.microsoft.com/en-us/library/mt734386%28v=exchg.150%29.aspx). DMARC empêche l’usurpation examinant l’expéditeur d’un message - celle que l’utilisateur voit dans leur client de messagerie (dans l’exemple ci-dessus, il s’agit service.outlook.com, outlook.com et accountprotection.microsoft.com) - avec le domaine transmis SPF ou DKIM. Autrement dit, le domaine que voit l’utilisateur a été authentifié et n’est donc pas usurpé. Pour une description plus complète, consultez la section « *comprendre pourquoi l’authentification du courrier électronique n’est pas toujours suffisant pour empêcher l’usurpation d’identité «* plus loin dans ce document. 
  
Toutefois, le problème est que l’authentification de courrier électronique enregistrements sont facultatives, non requis. Par conséquent, tandis que les domaines avec les stratégies de l’authentification forte comme microsoft.com et skype.com sont protégés contre l’usurpation d’identité, domaines que publier tout les stratégies d’authentification plus faibles ou aucune stratégie, sont les objectifs de l’usurpation. À compter de mars 2018, uniquement 9 % des domaines de sociétés dans le classement Fortune 500 publier des stratégies de messagerie fort d’authentification. Le 91 % restants peuvent être usurpés par un auteur de phishing, et à moins que le filtre de courrier détecte à l’aide d’une autre stratégie, peuvent être remis à un utilisateur final et les inciter :
  
![Stratégies DMARC des entreprises du classement Fortune 500](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
La proportion de petites et moyennes entreprises qui se trouvent pas dans le classement Fortune 500 qui publient des stratégies de messagerie fort d’authentification est, en toujours plus petits pour les domaines qui sont en dehors de l’Amérique du Nord et en Europe.
  
Il s’agit d’un problème très grand car alors que les entreprises ne connaissent pas forcément de fonctionnement de l’authentification du courrier électronique, phishing comprendre et tirer parti de l’absence de celle-ci.
  
Pour plus d’informations sur la configuration de SPF, DKIM et DMARC, consultez la section « *clients d’Office 365"* plus loin dans ce document. 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a>Arrêt de l’usurpation d’identité avec l’authentification implicite de courrier électronique

Hameçonnage phishing et sonde étant ce type de problème et en raison de l’adoption de stratégies d’authentification du courrier électronique fort limitée, Microsoft continue à investir dans des fonctionnalités pour protéger ses clients. Par conséquent, Microsoft avancer avec *authentification implicite de courrier électronique* - si un domaine n’authentifie, Microsoft traiter comme s’il a publié des enregistrements de messagerie d’authentification et traite en conséquence si elle ne passe pas. 
  
Pour ce faire, Microsoft a créé de nombreuses extensions vers l’authentification régulièrement du courrier, y compris la réputation de l’expéditeur, l’historique des expéditeurs/destinataires, comportement et d’autres techniques avancées. Un message envoyé à partir d’un domaine qui ne publie pas l’authentification du courrier électronique sera marqué comme usurpation d’identité, sauf si elle contient d’autres signaux pour indiquer qu’il est légitime.
  
Ce faisant, fin, les utilisateurs peuvent avoir confiance qu’un message électronique envoyé n’a pas été falsifié, expéditeurs peuvent être sûres que personne emprunte l’identité de leur domaine, et les clients d’Office 365 offre une protection mieux encore telles que la protection de l’emprunt d’identité.
  
Pour voir le lancement de Microsoft, voir [A marin de hameçonnage partie 2 - Anti amélioré l’usurpation d’identité dans Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a>Identification qu’un message est classé comme étant usurpés

### <a name="composite-authentication"></a>Authentification composite

Alors que SPF, DKIM et DMARC sont tous utiles par eux-mêmes, ils ne communiquent suffisamment l’état d’authentification dans les événements un message n’a aucun enregistrement explicite de l’authentification. Par conséquent, Microsoft a développé un algorithme qui combine les signaux multiples en une seule valeur appelée authentification Composite ou compauth pour short. Clients dans Office 365 ont des valeurs de compauth en l’en-tête des *Résultats de l’authentification* dans les en-têtes des messages. 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|**Résultat CompAuth**|**Description**|
|:-----|:-----|
|Échec|Message d’échec d’authentification explicites (domaine expéditeur paru enregistrements explicitement DNS) ou authentification implicite (envoi de domaine n’avez pas publié des enregistrements dans DNS, pour Office 365 interpolées le résultat comme s’il a publié des enregistrements).|
|passer|Message transmis d’authentification explicites (message transmis DMARC ou [Meilleures DMARC transmis deviner](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) ou l’authentification implicite avec un niveau de confiance élevé (envoi de domaine ne publie pas les enregistrements de messagerie d’authentification, mais Office 365 a fort principal des signaux indiquer le message est probablement légitimes).|
|softpass|Message transmis authentification implicite en toute confiance faible à moyen (envoi de domaine ne publie pas l’authentification du courrier électronique, mais Office 365 a signaux principal pour indiquer le message est légitime, mais la puissance du signal est la plus faible).|
|aucune|Message ne s’est pas authentifié (ou il s’est authentifié, mais ne pas aligner), mais l’authentification composite ne pas appliquée en raison de la réputation de l’expéditeur ou d’autres facteurs.|
   
|||
|:-----|:-----|
|**Reason**|**Description**|
|0XX|Message d’échec de l’authentification composite.<br/>**000** signifie que le message d’échec de DMARC avec une action de rejet ou mise en quarantaine.                    -001 signifie que le message d’échec de l’authentification de courrier électronique implicite. Cela signifie que le domaine ne dispose pas d’enregistrements d’authentification e-mail publiés, ou si c’était le cas, il était une stratégie de défaillance plus faible (échec logicielle SPF ou neutre, stratégie DMARC de p = none).<br/>**002** signifie que de l’organisation dispose d’une stratégie pour la paire de l’expéditeur ou du domaine qui est interdite explicitement d’envoyer l’e-mail falsifié, ce paramètre est défini manuellement par un administrateur.  <br/>**010** signifie que le message a échoué DMARC avec une action de rejet ou mise en quarantaine, et le domaine est un des domaines acceptés de votre organisation (Cela fait partie de self-à-self ou interne à l’organisation, l’usurpation d’identité).  <br/>**011** signifie que le message d’échec de l’authentification de courrier électronique implicite et le domaine est un des domaines acceptés de votre organisation (Cela fait partie de self-à-self ou interne à l’organisation, l’usurpation d’identité).|
|Tous les autres codes (1xx, 2xx, 3xx, 4xx, 5xx)|Correspond à différents codes internes pour la raison pour laquelle un message authentification implicite ou n’eu aucune authentification mais aucune action n’a été appliquée.|
   
En examinant les en-têtes d’un message, un administrateur ou même un utilisateur final peut déterminer comment Office 365 arrive à la conclusion que l’expéditeur peut être usurpé.
  
### <a name="differentiating-between-different-types-of-spoofing"></a>Différencier les différents types de l’usurpation d’identité

Microsoft fait la distinction entre les deux types de messages de l’usurpation d’identité :
  
 **Interne à l’organisation l’usurpation d’identité**
  
Également appelé self-à-self l’usurpation d’identité, cela se produit lorsque le domaine dans le champ : adresse est identique ou s’aligne sur le domaine du destinataire (lorsque le domaine du destinataire est un des [Domaines acceptés](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)les de votre organisation) ; ou, si le domaine dans le champ : adresse fait partie de la même organisation.
  
Par exemple, les éléments suivants a expéditeur et destinataire du même domaine (contoso.com). Les espaces sont insérés dans l’adresse de messagerie pour empêcher spambot capture sur cette page) :
  
De : expéditeur @ contoso.com
  
À : destinataire @ contoso.com
  
Les domaines de l’expéditeur et destinataire alignant sur le domaine d’organisation (fabrikam.com) comprend les suivantes :
  
De : expéditeur @ foo.fabrikam.com
  
À : destinataire @ bar.fabrikam.com
  
Les domaines suivants de l’expéditeur et destinataire sont différents (microsoft.com et bing.com), mais ils appartiennent à la même organisation (autrement dit, les deux font partie des domaines l’organisation acceptés) :
  
De : expéditeur @ microsoft.com
  
À : destinataire @ bing.com
  
Les messages qui échouent interne à l’organisation usurpation contient les valeurs suivantes dans les en-têtes :
  
X-Forefront-Antispam-Report :... CAT:SPM/HSPM/PHSH ;... SFTY:9.11
  
Le Chat est la catégorie du message et il est généralement marqué comme moniteur de port standard (spam), mais peuvent être HSPM (spam niveau de confiance élevé) ou hameçonnage (phishing), selon les autres types de modèles de se produire occasionnellement dans le message.
  
Le SFTY est le niveau de sécurité du message, le premier chiffre (9) signifie le message est hameçonnage et deuxième ensemble de chiffres après que le point (11) signifie qu’il est interne à l’organisation l’usurpation d’identité.
  
Il n’existe aucun code raison spécifique pour l’authentification Composite pour interne à l’organisation l’usurpation d’identité, qui portent plus loin dans 2018 (chronologie n’est pas encore défini).
  
 **Usurpation d’autres domaines**
  
Cela se produit lorsque le domaine dans l’envoi : adresse est un domaine externe à l’organisation de réception. Les messages que l’authentification Composite a échoué en raison de l’usurpation d’identité inter-domaines contient les valeurs suivantes dans les en-têtes :
  
Résultats de l’authentification :... compauth = échec raison 001 de 000
  
X-Forefront-Antispam-Report :... CAT:SPOOF ;... SFTY:9.22
  
Dans les deux cas, l’info-bulle de sécurité rouge suivant est marqué dans le message ou un équivalent à la langue de la boîte aux lettres destinataire personnalisé :
  
![Conseil de sécurité rouge - détection de fraude](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
Il est uniquement à partir de : adresse et savoir quel est votre messagerie du destinataire ou en examinant les en-têtes de courrier électronique, vous pouvez différencier interne à l’organisation et l’usurpation d’identité inter-domaines.
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a>Comment les clients d’Office 365 peuvent se préparer pour la nouvelle protection anti-l’usurpation d’identité

### <a name="information-for-administrators"></a>Informations pour les administrateurs

En tant qu’administrateur d’une organisation dans Office 365, il existe plusieurs éléments clés d’informations, que vous devez connaître.
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a>Comprendre pourquoi l’authentification du courrier électronique n’est pas toujours suffisant pour empêcher l’usurpation d’identité

La nouvelle protection anti-usurpation repose sur l’authentification de courrier électronique (SPF, DKIM et DMARC) ne pas marquer un message comme l’usurpation d’identité. Un exemple courant est lorsqu’un domaine d’envoi a publié jamais les enregistrements SPF. Si aucun enregistrement SPF ou qu’ils sont correctement configurés, un message envoyé sera marqué comme étant usurpés, sauf si Microsoft a aide à la décision principale indiquant que le message est légitime.
  
Par exemple, avant anti-usurpation déployé, un message peut pouvaient ressembler à ce qui suit avec aucun enregistrement SPF, aucun enregistrement DKIM et aucun enregistrement DMARC : 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
Après avoir anti-usurpation, si vous avez Office 365 entreprise E5, EOP ou DAV, la valeur compauth est marquée :
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

Si example.com fixe cela en configurant un enregistrement SPF mais pas un enregistrement DKIM, afin de passer composite d’authentification car le domaine qui a passé SPF aligné sur le domaine dans le champ : adresse : 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Ou, si elles configuré un enregistrement DKIM, mais pas un enregistrement SPF, également passer composite d’authentification car le domaine de la Signature DKIM transmis aligné sur le domaine dans le champ de : adresse : 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Toutefois, un auteur de phishing peut également configurer SPF et DKIM et signer le message avec leur propre domaine, mais spécifier un domaine différent du : adresse. SPF ni DKIM nécessite aligner avec le domaine dans le domaine : adresse, sauf si example.com publié enregistrements DMARC, ce ne serait pas marquées comme une usurpation d’identité à l’aide de DMARC : 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

Dans le client de messagerie (Outlook, Outlook sur le web, ou tout autre client de messagerie), d’uniquement : domaine est affiché, pas sur le domaine dans le SPF ou DKIM et qui peut croire l’utilisateur le message provenance example.com, mais c’est bien maliciousDomain.com .
  
![Message authentifié mais : domaine n’aligne pas avec ce que transmis SPF ou DKIM](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
Pour cette raison, Office 365 requiert que le domaine du : adresse s’aligne sur le domaine dans la signature SPF ou DKIM, et si elle ne, contient certains autres signaux interne qui indique que le message est légitime. Dans le cas contraire, le message est un message d’échec compauth. 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

Par conséquent, Office 365 anti-l’usurpation d’identité protège contre les domaines sans authentification et les domaines qui a configuré l’authentification, mais incompatibilité par rapport au domaine dans la : adresse comme celle que l’utilisateur voit et considère sont l’expéditeur du message. Cela est vrai à la fois des domaines externes à votre organisation, ainsi que les domaines dans votre organisation.
  
Par conséquent, si vous recevez toujours un message d’échec de l’authentification composite et est marqué comme étant usurpés, même si le message passé SPF et DKIM, il est, car le domaine qui a passé SPF et DKIM ne sont pas alignés avec le domaine du : adresse.
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a>Présentation des modifications dans les messages électroniques usurpés comment sont traitées.

Actuellement, pour toutes les organisations dans Office 365 - DAV et non-DAV - messages échoue DMARC avec une stratégie de rejet ou mise en quarantaine sont marquées comme du courrier indésirable et prennent généralement l’action de courrier indésirable de niveau de confiance élevé, ou parfois l’action du courrier indésirable régulière (selon qu’autres du courrier indésirable règles d’abord identifient comme courrier indésirable). Détections d’usurpation d’identité interne à l’organisation effectuer l’action de courrier indésirable régulière. Ce problème n’a pas besoin d’être activé, ni peut être désactivée.
  
Toutefois, pour les messages d’usurpation inter-domaines, avant cette modification elles, exécutez régulièrement des contrôles spam, hameçonnage et les logiciels malveillants et si d’autres composants du filtre identifiés comme suspects, seraient marquer comme courrier indésirable, hameçonnage ou un programme malveillant respectivement. Avec la nouvelle protection usurpation d’identité inter-domaines, tout message ne peut pas être authentifié, par défaut, exécute l’action définie dans le Anti-hameçonnage \> stratégie anti-usurpation d’identité. Si celle-ci n’est pas définie, il sera déplacé dans un dossier de courrier indésirable des utilisateurs. Dans certains cas, les messages plus suspects aura également ajouté au message info-bulle de sécurité rouge.
  
Cela peut entraîner des messages qui ont été marqués comme courrier indésirable toujours marqués comme du courrier indésirable mais maintenant aussi une info-bulle rouge de sécurité ; dans les autres cas, les messages qui ont été marqués comme légitimes démarrera marqués comme courrier indésirable (CAT:SPOOF) avec une info-bulle de sécurité rouge est ajouté. Dans d’autres cas encore, les clients qui ont été déplacer tous les courriers indésirables et phishing à la mise en quarantaine maintenant verront les accédant au dossier courrier indésirable (ce comportement peut être modifié, voir [modification de vos paramètres anti-usurpation](#changing-your-anti-spoofing-settings)).
  
Il existe plusieurs façons qu'un message peut être usurpé (voir [Differentiating entre les différents types de l’usurpation d’identité](#differentiating-between-different-types-of-spoofing) plus haut dans cet article), mais à compter de mars 2018 la façon dont Office 365 traite ces messages n’est pas encore unifiée. Le tableau suivant est un résumé rapide, avec protection usurpation d’identité inter-domaines est nouveau comportement : 
  
|**Type d’usurpation d’identité**|**Catégorie**|**Conseil de sécurité ajouté ?**|**S'applique à**|
|:-----|:-----|:-----|:-----|
|Échec DMARC (mise en quarantaine ou rejeter)  <br/> |HSPM (valeur par défaut), peut également être Moniteur de port standard ou PHSH  <br/> |No (non)  <br/> |Tous les clients Office 365, Outlook.com  <br/> |
|Self-à-self  <br/> |MONITEUR DE PORT STANDARD  <br/> |Oui  <br/> |Toutes les organisations Office 365, Outlook.com  <br/> |
|Inter-domaines  <br/> |USURPATION D’IDENTITÉ  <br/> |Oui  <br/> |Protection contre les menaces avancées Office 365 et E5 clients  <br/> |
   
### <a name="changing-your-anti-spoofing-settings"></a>Modification de vos paramètres anti-l’usurpation d’identité

Pour créer ou mettre à jour vos paramètres anti-usurpation (domaines), accédez à l’hameçonnage \> usurpation Anti paramètres de la gestion des menaces \> onglet Stratégie de la sécurité &amp; centre de conformité. Si vous n’avez jamais créé des paramètres anti-hameçonnage, vous devrez créer un :
  
![Anti-hameçonnage - créer une nouvelle stratégie](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
Si vous avez déjà créé un, vous pouvez le sélectionner pour le modifier :
  
![Anti-hameçonnage - modifier une stratégie existante](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
Sélectionnez la stratégie que vous venez de créer et passez en revue les étapes comme décrit dans [pour en savoir plus sur l’aide à la décision usurpation.](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)
  
![Activer ou désactiver antispoofing](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![Activer ou désactiver les conseils de sécurité antispoofing](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
Pour créer une nouvelle stratégie via PowerShell : 
  
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

Vous pouvez modifier ensuite les paramètres de stratégie anti-hameçonnage à l’aide de PowerShell, [Set-AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps)de la documentation. Vous pouvez spécifier le $name en tant que paramètre :
  
```
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

Plus loin dans 2018, au lieu d’avoir à créer une stratégie par défaut, un sera créé qui porte sur tous les destinataires de votre organisation afin que vous n’êtes pas obligé de spécifier manuellement (les captures d’écran ci-dessous sont sujettes à modification avant l’implémentation finale).
  
![Stratégie par défaut pour anti-hameçonnage](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
Contrairement à la stratégie que vous créez, vous ne peut pas supprimer la stratégie par défaut, modifier sa priorité ou choisissez quels utilisateurs, les domaines ou les groupes à étendue.
  
![Détails de la stratégie par défaut anti-hameçonnage](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
Plus loin dans 2018, pour configurer la protection par défaut via PowerShell :
  
```
$defaultAntiphishPolicy = Get-AntiphishingPolicy -IsDefault $true
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

Ne désactivez protection anti-usurpation si vous disposez d’un autre serveur de messagerie ou serveurs devant Office 365 (voir scénarios légitimes pour désactiver contre l’usurpation d’identité pour plus d’informations). 
  
```
$defaultAntiphishPolicy = Get-AntiphishingPolicy -IsDefault $true
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> Si le premier tronçon dans votre chemin d’accès du courrier électronique est Office 365, et vous obtenez un trop grand nombre de messages électroniques légitimes marqués comme usurpation d’identité, vous devez tout d’abord configurer votre expéditeurs autorisés à envoyer un courrier électronique usurpé à votre domaine (voir la section *« Gestion des expéditeurs légitimes qui envoient u messagerie nauthenticated »* ). Si vous obtenez toujours trop de faux positifs (par exemple, les messages marqués comme usurpation d’identité de légitimes), nous ne recommandons pas la désactivation de protection anti-usurpation entièrement. Au lieu de cela, nous vous recommandons de choisissant de base au lieu d’une protection élevée.                    Il est préférable de travailler par le biais de faux positifs qu’à exposer votre organisation pour les courriers électroniques usurpés qui pourrait finir imposant des coûts considérablement plus élevés à long terme.

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a>Gestion des expéditeurs légitimes qui sont envoyant du courrier non authentifié

Office 365 effectue le suivi des personnes sont envoyant du courrier non authentifié à votre organisation. Si le service pense que l’expéditeur n’est pas légitime, il marque comme un échec *compauth* . Il sera classé comme usurpation d’identité bien que cela dépend de votre stratégie anti-l’usurpation d’identité qui a été appliquée au message. 
  
Toutefois, en tant qu’administrateur, vous pouvez spécifier les expéditeurs autorisés à envoyer un message électronique usurpé, substitution de décision d’Office 365.
  
**Méthode 1 : Si votre organisation possède le domaine configuré l’authentification du courrier électronique**
  
Cette méthode peut être utilisée pour résoudre l’usurpation interne à l’organisation et l’usurpation d’autres domaines dans les cas où vous possédez ou interagissez avec plusieurs clients. Il permet également de résoudre l’usurpation d’identité de domaines où vous envoyez aux autres clients dans Office 365, ainsi que les tierces parties qui sont hébergées dans les autres fournisseurs.
  
Pour plus d’informations, voir [clients d’Office 365](#customers-of-office-365). 
 
**Méthode 2 : aide à la décision usurpation d’identité utiliser pour configurer les expéditeurs autorisés de courriers électroniques non authentifiés**
  
Vous pouvez également utiliser [l’Usurpation d’identité aide à la décision](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) d’autoriser les expéditeurs pour transmettre des messages non authentifiés à votre organisation. 
  
Pour les domaines externes, l’utilisateur usurpé est le domaine de l’adresse de provenance, tandis que l’infrastructure d’envoi est l’adresse IP envoi (divisé en /24 plages CIDR), ou le domaine d’organisation de l’enregistrement PTR (dans la capture d’écran ci-dessous, l’envoi IP peut-être être 131.107.18.4 dont l’enregistrement PTR est outbound.mail.protection.outlook.com, et il doit s’afficher en tant que outlook.com pour l’infrastructure d’envoi).
  
Pour permettre à cet expéditeur pour envoyer un message électronique non authentifié, remplacez le **No** **Oui**.
  
![Configuration d’antispoofing expéditeurs autorisé](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
Vous pouvez également utiliser PowerShell pour autoriser l’expéditeur spécifique d’usurper votre domaine : 
  
```
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Obtention des expéditeurs usurpés via Powershell](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
Dans l’image précédente, les sauts de ligne supplémentaires ont été ajoutées pour rendre cette capture d’écran présents, mais en réalité, toutes les valeurs apparaîtraient sur une seule ligne.
  
Modifier le fichier et recherchez la ligne qui correspond à outlook.com et bing.com et modifiez l’entrée AllowedToSpoof non Oui :
  
![Usurpation d’identité paramètre Autoriser Oui via Powershell](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
Enregistrez le fichier, puis exécutez : 
  
```
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

Cela permettra maintenant bing.com envoyer un message électronique non authentifié à partir de \*. outlook.com.

**Méthode 3 : créer une entrée d’autoriser pour la paire de l’expéditeur/destinataire**
  
Vous pouvez également choisir d’ignorer toutes les de filtrage pour un expéditeur particulier. Pour plus d’informations, voir [comment ajouter en toute sécurité un expéditeur à une liste verte dans Office 365](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/).
  
Si vous utilisez cette méthode, elle ignore le courrier indésirable et le filtrage de hameçonnage, certains, mais pas le filtrage anti-programme malveillant.
  
**Méthode 4 - contactez l’expéditeur et demandez-lui de configurer l’authentification du courrier électronique**
  
En raison de problème de courrier indésirable et l’hameçonnage, Microsoft vous recommande de configurer l’authentification du courrier électronique de tous les expéditeurs. Si vous connaissez un administrateur de domaine, contactez les et demande qu’ils enregistrent des enregistrements de messagerie d’authentification pour ne pas avoir à ajouter les substitutions. Pour plus d’informations, voir [les administrateurs des domaines qui ne sont pas des clients Office 365](#administrators-of-domains-that-are-not-office-365-customers)« plus loin dans cet article. 
  
S’il peut être difficile à tout d’abord obtenir l’envoi des domaines d’authentification, au fil du temps, en plus des filtres de courrier électronique démarrer junking ou rejet même leur messagerie électronique, entraîne leur configurer les enregistrements appropriés afin d’améliorer la fourniture.
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a>Affichage des rapports de nombre de messages marqué comme étant usurpés

Une fois votre stratégie anti-l’usurpation d’identité est activé, vous pouvez utiliser des menaces pour contourner le nombre de messages est marqué comme étant de hameçonnage les numéros. Pour ce faire, accédez à la sécurité &amp; centre de conformité (SCC) sous gestion des menaces \> Explorateur de solutions, affectez l’affichage hameçonnage et groupe par domaine de l’expéditeur ou l’état de Protection :
  
![Afficher le nombre de messages est marqué comme étant de hameçonnage](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
Vous pouvez interagir avec les différents rapports combien ont été marqués en tant que l’hameçonnage, y compris les messages marqués comme usurpation d’identité. Pour plus d’informations, voir [en route avec Office 365 menaces](https://support.office.com/article/get-started-with-office-365-threat-intelligence-38e9b67f-d188-490f-bc91-a1ae4b270441).
  
Vous ne pouvez pas encore répartir les messages marqués en raison de l’usurpation d’identité et d’autres types de hameçonnage (phishing général, l’emprunt d’identité de domaine ou un utilisateur et ainsi de suite). Toutefois, plus loin dans 2018, vous pourrez faire par le biais de la sécurité &amp; centre de conformité. Une fois que vous le faites, vous pouvez utiliser ce rapport comme point de départ pour identifier les domaines d’envoi peuvent être légitimes qui sont marqués comme usurpation d’identité en raison de l’échec d’authentification.
  
La capture d’écran suivante est une proposition de la façon dont ces données recherchera, mais peuvent modifier lorsque l’utilisateur relâche :
  
![Affichage des rapports d’hameçonnage par type de détection](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
Pour obtenir et clients E5 non DAV, ces rapports seront disponibles plus tard 2018 dans les rapports d’état de Protection de menace (support), mais seront retardés d’au moins 24 heures. Cette page sera mise à jour comme elles sont intégrées à la sécurité &amp; centre de conformité.
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a>Prévoir le nombre de messages sera signalée comme usurpation d’identité

Plus loin dans 2018, une fois Office 365 met à jour ses paramètres qui vous permet de désactiver la mise en œuvre l’usurpation d’identité contre ou sur la mise en application Basic ou élevé, vous aurez la possibilité de quoi destruction message va changer les paramètres différents. Autrement dit, si l’usurpation d’identité anti est désactivée, vous serez en mesure de voir le nombre de messages sera détecté comme usurpation d’identité si vous activez Basic ; ou, si elle est Basic, vous serez en mesure de voir le nombre de messages plus sera détecté comme usurpation d’identité si vous l’activez à haut niveau.
  
Cette fonctionnalité est actuellement en cours de développement. Lorsque plus de détails sont définis, cette page sera mise à jour avec captures d’écran de la sécurité et le centre de conformité et avec des exemples de PowerShell.
  
![« Que se passe-t-il si » état d’activation antispoofing](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![Expérience utilisateur possible pour permettre un expéditeur usurpé](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="understanding-how-spam-phishing-and-advanced-phishing-detections-are-combined"></a>Comprendre comment spam, hameçonnage et l’hameçonnage avancée détections sont combinées

Les organisations qui utilisent Exchange Online, avec ou sans DAV, pouvant spécifier les actions à entreprendre lorsque le service identifie les messages comme des programmes malveillants, le courrier indésirable, du courrier indésirable de niveau de confiance élevé, l’hameçonnage et en bloc. Avec les stratégies Anti-hameçonnage ATP pour les clients DAV et les stratégies Anti-hameçonnage pour les clients EOP et le fait qu’un message peut-être atteint plusieurs types de détection (par exemple, les logiciels malveillants, phishing et emprunt d’identité utilisateur), il peut y avoir une certaine confusion quant à laquelle stratégie s’applique. 
  
En règle générale, la stratégie appliquée à un message est identifiée dans l’en-tête X-Forefront-Antispam-Report dans la propriété CAT (catégorie). 
  
|**Priority (Priorité)**|**Stratégie**|**Catégorie**|**Où gérée ?**|**S'applique à**|
|:-----|:-----|:-----|:-----|:-----|
|1  <br/> |Malware :   <br/> |MALW  <br/> |[Stratégie de programmes malveillants](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|2  <br/> |Hameçonnage  <br/> |PHSH  <br/> |[Stratégie de filtrage de contenu hébergé](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|3  <br/> |Courrier indésirable à probabilité élevée  <br/> |HSPM  <br/> |[Stratégie de filtrage de contenu hébergé](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|4  <br/> |L’usurpation d’identité  <br/> |USURPATION D’IDENTITÉ  <br/> |[Stratégie anti-hameçonnage](https://go.microsoft.com/fwlink/?linkid=864553), [aide à la décision usurpation d’identité](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) <br/> |Toutes les organisations  <br/> |
|5   <br/> |Courrier indésirable  <br/> |MONITEUR DE PORT STANDARD  <br/> |[Stratégie de filtrage de contenu hébergé](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|6   <br/> |En bloc  <br/> |EN BLOC  <br/> |[Stratégie de filtrage de contenu hébergé](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Toutes les organisations  <br/> |
|7   <br/> |Emprunt d’identité de domaine  <br/> |DIMP  <br/> |[Stratégie anti-hameçonnage](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |Organisations avec DAV  <br/> |
|8   <br/> |Emprunt d’identité de l’utilisateur  <br/> |UIMP  <br/> |[Stratégie anti-hameçonnage](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |Organisations avec DAV <br/> |
   
Si vous disposez de plusieurs stratégies Anti-hameçonnage différents, celui dont la priorité la plus élevée s’appliquera. Par exemple, supposons que vous avez deux stratégies :
  
|**Stratégie**|**Priority (Priorité)**|**Emprunt d’identité de l’utilisateur ou du domaine**|**Anti-l’usurpation d’identité**|
|:-----|:-----|:-----|:-----|
|A  <br/> |1  <br/> |On  <br/> |Off  <br/> |
|B  <br/> |2  <br/> |Off  <br/> |On  <br/> |
   
Si un message est proposé sous et est identifié en tant que l’emprunt d’identité à la fois l’usurpation d’identité et l’utilisateur et le même ensemble d’utilisateurs porte sur la stratégie A et B de la stratégie, puis le message est traité comme une usurpation d’identité mais aucune action n’est appliquée depuis anti-usurpation d’identité est désactivé , et l’usurpation d’identité s’exécute à une priorité plus élevée (4) à l’utilisateur d’emprunt d’identité (8).
  
Pour effectuer d’autres types de hameçonnage stratégie s’applique, vous devrez ajuster les paramètres de qui différentes stratégies sont appliquées.
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a>Scénarios légitimes pour désactiver l’usurpation d’identité contre

L’usurpation d’identité contre améliore la protection des clients contre les attaques par hameçonnage, et par conséquent, la désactivation de protection anti-usurpation est fortement déconseillée. En le désactivant, vous pouvez résoudre certains faux positifs à court terme, mais à long terme que vous seront exposés à plus de risques. Le coût de configuration de l’authentification sur le côté de l’expéditeur ou la réalisation d’ajustements dans les stratégies anti-hameçonnage, sont généralement uniques événements ou nécessitent une maintenance périodique minime. Toutefois, le coût de récupération à partir d’une attaque par hameçonnage où les données a été exposées ou d’éléments ont été compromise est beaucoup plus élevé.
  
Pour cette raison, il est préférable de travailler par le biais de l’usurpation d’identité contre faux positifs que pour désactiver la protection anti-courrier usurpation d’identité.
  
Toutefois, il existe un scénario authentique où l’usurpation d’identité anti doit être désactivée et qui est quand il y a plus de filtrage de courrier produits dans le routage des messages et Office 365 n’est pas le premier tronçon dans le chemin d’accès du courrier électronique :
  
![Enregistrement MX ne pointe pas vers Office 365](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
L’autre serveur peut être un serveur de messagerie sur site Exchange, un dispositif tel que Ironport, de filtrage de messagerie ou un autre dans le nuage hébergé par service.
  
Si l’enregistrement MX du domaine destinataire ne pointe pas vers Office 365, il n’est pas nécessaire de désactiver l’usurpation d’identité contre, car Office 365 recherche un enregistrement MX de votre domaine de réception et supprime l’usurpation d’identité contre qu’il pointe vers un autre service. Si vous ignorez si votre domaine possède un autre serveur au premier plan, vous pouvez utiliser un site Web à la boîte à outils MX pour rechercher l’enregistrement MX. Elle peut indiquer ce qui suit :
  
![Enregistrement MX indique le domaine ne pointe pas vers Office 365](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
Ce domaine a un enregistrement MX qui ne pointe pas vers Office 365, afin que Office 365 ne s’appliquent pas anti-l’usurpation d’identité de l’application.
  
Toutefois, si l’enregistrement MX du domaine du destinataire *est* pointe vers Office 365, même s’il existe un autre service devant Office 365, puis vous devez désactiver anti-l’usurpation d’identité. L’exemple le plus courant consiste à utiliser d’une réécriture de destinataire : 
  
![Diagramme de routage pour la réécriture de destinataire](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
Un enregistrement MX du domaine contoso.com pointe vers le serveur sur site, tandis que l’enregistrement MX de domaine @office365.contoso .Web .UI pointe vers Office 365, car il contient \*. protection.outlook.com, ou \*. eo.outlook.com dans l’enregistrement MX :
  
![Points d’enregistrement MX vers Office 365, par conséquent probablement destinataire réécrire](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
N’oubliez pas de différencier les lors de l’enregistrement MX de destinataire d’un domaine ne pointe pas vers Office 365 et lorsqu’il a subi une réécriture destinataire. Il est important de faire la différence entre ces deux cas.
  
Si vous ne savez pas si votre domaine de réception ayant subi une réécriture de destinataire, vous pouvez parfois indiquer en examinant les en-têtes des messages.
  
un) tout d’abord, examinez les en-têtes dans le message pour le domaine du destinataire dans l’en-tête des résultats de l’authentification : 
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

Le domaine du destinataire se trouve dans le texte en gras en rouge ci-dessus, dans ce cas office365.contoso.net. Il peut être différent que le destinataire dans le champ à : en-tête :
  
À : Exemple destinataire \<destinataire @ contoso.com\>
  
Effectuer une recherche d’enregistrement MX du domaine destinataire réel. S’il contient \*. protection.outlook.com, mail.messaging.microsoft.com, \*. eo.outlook.com ou mail.global.frontbridge.com, ce qui signifie que la MX pointe vers Office 365.
  
Si elle ne contient pas ces valeurs, cela signifie que la MX ne pointe pas vers Office 365. Un outil que vous pouvez utiliser pour vérifier cela est boîte à outils MX.
  
Pour cet exemple, ce qui suit indique contoso.com, le domaine qui se présente comme le destinataire, car elle était à : en-tête, a des points d’enregistrement MX sur un serveur sur prem :
  
![Enregistrement MX pointe vers le serveur sous prem](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
Toutefois, le destinataire réel est office365.contoso.net dont l’enregistrement MX pointe vers Office 365 :
  
![MX pointe vers Office 365, doit être réécriture destinataire](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
Par conséquent, ce message a subi probablement une réécriture de destinataire.
  
b) en second lieu, n’oubliez pas de faire la distinction entre les cas d’utilisation courants de réécritures destinataires. Si vous souhaitez réécrire le domaine du destinataire à \*. onmicrosoft.com, au lieu de cela réécrire pour qu’il \*. mail.onmicrosoft.com.
  
Une fois que vous avez identifié le domaine du destinataire final qui est routé derrière un autre serveur et un enregistrement MX du domaine destinataire réellement pointe vers Office 365 (tel qu’il est publié dans ses enregistrements DNS), vous pouvez continuer à désactiver anti-l’usurpation d’identité.
  
N’oubliez pas, vous ne souhaitez pas désactiver anti-usurpation si tronçon premier du domaine dans le chemin de routage est Office 365, uniquement lorsqu’il est derrière un ou plusieurs services.
  
### <a name="how-to-disable-anti-spoofing"></a>Comment faire pour désactiver l’usurpation d’identité contre

Si vous avez déjà une stratégie Anti-hameçonnage créée, définissez le paramètre EnableAntispoofEnforcement sur $false : 
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false 

```

Si vous ne connaissez pas le nom de la stratégie (ou plusieurs) pour désactiver, vous pouvez afficher les : 
  
```
Get-AntiphishPolicy | fl Name
```

Si vous ne disposez pas des stratégies anti-hameçonnage existantes, vous pouvez en créer un et ensuite la désactiver (même si vous n’avez pas une stratégie, l’usurpation d’identité contre est toujours appliqué ; ultérieurement dans 2018, une stratégie par défaut est créée pour vous et vous pouvez ensuite désactiver qui au lieu de créer un) . Vous devez procéder ainsi dans plusieurs étapes : 
  
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

Désactivation de l’usurpation d’identité contre est disponible uniquement via l’applet de commande (plus loin dans 2018 Q2, il sera disponible dans la sécurité &amp; centre de conformité). Si vous n’avez pas accès à PowerShell, créez un ticket de support.
  
N’oubliez pas, il doit être appliqué uniquement à des domaines qui subissent routage indirect lorsque envoyées à Office 365. Pour désactiver l’usurpation d’identité contre en raison de certains faux positifs tentant de réserve, il sera préférable à long terme de travailler à leur.
  
### <a name="information-for-individual-users"></a>Informations pour les utilisateurs individuels

Les utilisateurs individuels sont limitées à comment ils peuvent interagir avec l’info-bulle de sécurité anti-l’usurpation d’identité. Toutefois, il existe plusieurs choses que vous pouvez faire pour résoudre des scénarios courants.
  
### <a name="common-scenario-1---mailbox-forwarding"></a>Scénario courant #1 - transfert de boîte aux lettres

Si vous utilisez un autre service de messagerie et transférez votre courrier électronique vers Office 365 ou Outlook.com, votre courrier électronique peut être marqué comme l’usurpation d’identité et recevoir une info-bulle de sécurité rouge. Office 365 et Outlook.com planifier adresses automatiquement lorsque le redirecteur est un des Outlook.com, Office 365, Gmail ou tout autre service qui utilise le [protocole de l’ARC](https://arc-spec.org). Toutefois, jusqu'à ce que ce correctif est déployé, les utilisateurs doivent utiliser la fonctionnalité de comptes connectés à importer leurs messages directement, au lieu d’utiliser l’option de transfert.
  
Pour configurer les comptes connectés dans Office 365, sélectionnez l’icône représentant un engrenage dans le coin supérieur droit de l’interface web de Office 365 \> messagerie \> messagerie \> comptes \> comptes connectés.
  
![Option de comptes Office 365 - connecté](media/e8e841ca-8861-4d83-8506-2a0858c51010.jpg)
  
Dans Outlook.com, le processus est l’icône d’engrenage \> Options \> messagerie \> comptes \> comptes connectés.
  
### <a name="common-scenario-2---discussion-lists"></a>Listes de Discussion fréquent #2 :

Listes de discussion connus pour avoir des problèmes avec anti-usurpation en raison de la façon dont ils transférer le message et modifier son contenu encore conserver le d’origine à partir de : adresse.
  
Par exemple, supposons que votre adresse e-mail est utilisateur @ contoso.com, et que vous intéressez observation d’oiseaux et joindre les amoureux de la nature liste discussion @ exemple.com. Lorsque vous envoyez un message à la liste de discussion, vous pouvez l’envoyer ainsi :
  
**à partir de :** John Doe \<utilisateur @ contoso.com\> 
  
**À :** Liste de Discussion de birdwatcher \<amoureux de la nature @ exemple.com\> 
  
**Objet :** Une visualisation de jays bleu dans la partie supérieure de Rainier MT. cette semaine 
  
Tout le monde souhaitez extraire l’affichage cette semaine de Rainier MT. ?
  
Lorsque la liste de messagerie reçoit le message, ils mettre en forme le message, de modifier son contenu et relire au reste des membres dans la liste de discussion constituée de participants à partir de nombreux récepteurs de messagerie différents.
  
**à partir de :** John Doe \<utilisateur @ contoso.com\> 
  
**À :** Liste de Discussion de birdwatcher \<amoureux de la nature @ exemple.com\> 
  
**Objet :** [AMOUREUX DE LA NATURE] Une visualisation de jays bleu dans la partie supérieure de Rainier MT. cette semaine 
  
Tout le monde souhaitez extraire l’affichage cette semaine de Rainier MT. ?
  
---
  
Ce message a été envoyé à la liste de Discussion amoureux de la nature. Vous pouvez annuler l’abonnement à tout moment.
  
Dans l’exemple ci-dessus, le message relu possède la même : adresse (utilisateur @ contoso.com), mais le message d’origine a été modifié en ajoutant une balise à la ligne d’objet et un pied de page au bas du message. Ce type de modification du message est souvent dans des listes de distribution et risque de faux positifs.
  
Si vous ou une personne de votre organisation est un administrateur de la liste de distribution, vous pourrez peut-être le configurer pour passer les vérifications de l’usurpation d’identité contre.
  
- Consultez le Forum aux questions à DMARC.org : [puis-je utiliser une liste de publipostage et je souhaite interagir avec DMARC, que dois-je faire ?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)
    
- Consulter les instructions à ce billet de blog : [une info-bulle pour les opérateurs de liste de distribution interagir avec DMARC pour éviter tout problème](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)
    
- Envisagez l’installation de mises à jour sur votre serveur de liste de distribution à prendre en charge d’ARC, voir[https://arc-spec.org](https://arc-spec.org/)
    
Si vous n’avez pas de propriété de la liste de distribution :
  
- Vous pouvez demander du chargé de maintenance de la liste de distribution pour implémenter une des options ci-dessus (ils doivent également avoir authentification électronique configuré pour le domaine de de que la liste de distribution est le relais à partir)
    
- Vous pouvez créer des règles de boîte aux lettres dans votre client de messagerie pour déplacer des messages vers la boîte de réception. Vous pouvez également demander aux administrateurs de votre organisation pour configurer des règles d’autorisation ou substitutions comme indiqué dans la section Gestion des expéditeurs légitimes qui sont envoyant du courrier non authentifié
    
- Vous pouvez créer un ticket d’assistance avec Office 365 pour créer une substitution pour la liste de distribution à traiter comme légitime
    
### <a name="other-scenarios"></a>Autres scénarios

1. Si aucun des scénarios courants ci-dessus s’applique à votre situation, signaler le message comme faux positif arrière à Microsoft. Pour plus d’informations, consultez la section [comment signaler les messages de courrier indésirable ou non-spam retour à Microsoft ?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) plus loin dans cet article. 
    
2. Vous pouvez également contacter votre administrateur, qui peut déclencher comme un ticket de support Microsoft. L’équipe d’ingénierie Microsoft va étudier la raison pour laquelle le message a été marqué comme une usurpation d’identité.
    
3. En outre, si vous connaissez l’expéditeur et êtes certain qu’ils ne sont pas à des fins malveillantes usurpés, vous pouvez répondre à l’expéditeur indiquant que leur envoyer des messages à partir d’un serveur de messagerie qui n’authentifie pas. Cela entraîne parfois l’expéditeur d’origine contacter leur administrateur informatique qui définira les enregistrements d’authentification requis de courrier électronique.
  
Lorsque suffisamment expéditeurs de répondre à des propriétaires de domaine qu’ils doivent configurer des enregistrements de messagerie d’authentification, il les incite à prendre d’action. Microsoft fonctionne également avec les propriétaires de domaine pour publier les enregistrements requis, mais elle permet encore plus lorsque des utilisateurs individuels demandent.
    
4. Si vous le souhaitez, ajouter l’expéditeur à votre liste des expéditeurs approuvés. Cependant, gardez à l’esprit que si un auteur de phishing usurpe ce compte, il est remis à votre boîte aux lettres. Par conséquent, cette option doit être utilisée avec modération.
    
## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a>Comment les expéditeurs à Microsoft doivent préparer pour la protection anti-l’usurpation d’identité

Si vous êtes un administrateur ayant actuellement envoie des messages à Microsoft Office 365 ou Outlook.com, vous devez vous assurer que votre courrier électronique est correctement authentifié sinon il peut être marqué comme du courrier indésirable ou hameçonnage. 
  
### <a name="customers-of-office-365"></a>Clients d’Office 365

Si vous êtes un client Office 365 et Office 365 vous permet d’envoyer des messages électroniques sortants :
  
- Pour vos domaines, [configurer SPF dans Office 365 afin d’empêcher l’usurpation d’identité](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx)
    
- Pour vos domaines principaux, [DKIM utilisés pour valider le courrier sortant envoyé à partir de votre domaine personnalisé dans Office 365](https://technet.microsoft.com/en-us/library/mt695945%28v=exchg.150%29.aspx)
    
- [Envisager la création d’enregistrements DMARC](https://technet.microsoft.com/en-us/library/mt734386%28v=exchg.150%29.aspx) pour votre domaine pour déterminer quels sont vos expéditeurs légitimes 
    
Microsoft ne fournit pas d’instructions d’implémentation détaillées pour chacune des SPF, DKIM et DMARC. Toutefois, il est beaucoup d’informations de publication en ligne. 3e entreprises tierces sont également dédié pour aider votre organisation à configurer des enregistrements de messagerie d’authentification.
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a>Administrateurs de domaines qui ne sont pas des clients Office 365

Si vous êtes un administrateur de domaine, mais ne sont pas un client Office 365 :
  
- Vous devez configurer SPF pour publier les adresses IP d’envoi de votre domaine et également configurer DKIM (le cas échéant) pour signer numériquement les messages. Vous pouvez également envisager la configuration d’enregistrements DMARC.
    
- Si vous avez les expéditeurs qui transmettent courrier à votre place, vous devez travailler avec leur envoyer un message électronique d’une manière telle que dans le domaine : adresse (si elle appartient à vous) s’aligne sur le domaine qui transmet SPF ou DMARC.
    
- Si vous avez sur site, les serveurs de messagerie ou envoyer à partir d’un fournisseur de logiciel en tant que service, ou d’un service d’hébergement cloud Microsoft Azure, GoDaddy, rack, Amazon Web Services, ou similaire, vous devez vous assurer que qu’ils sont ajoutés à votre enregistrement SPF.
    
- Si vous êtes un domaine de petite taille qui est hébergé par un fournisseur de services Internet, vous devez configurer votre enregistrement SPF conformément aux instructions qui est fournie par votre fournisseur de services Internet. La plupart des fournisseurs de services Internet fournissent ces types d’instructions et se trouvent sur des pages de prise en charge de l’entreprise.
    
- Même si vous n’avez pas à publier des enregistrements d’authentification e-mail avant, et il fonctionne correctement, vous devez toujours publier les enregistrements d’authentification de courrier électronique à envoyer à Microsoft. En procédant ainsi, vous êtes à vous aider dans la lutte contre le hameçonnage et réduire le risque que vous, ou organisations que vous envoyez, obtenez récoltées.
    
### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a>Que se passe-t-il si vous ne connaissez pas qui envoie un courrier électronique en tant que votre domaine ?

Nombre de domaines ne pas publie les enregistrements SPF, car ils ne savent pas tous les expéditeurs sont. OK, vous n’avez pas besoin de savoir qui toutes ne soient. Au lieu de cela, doit commencer par la publication d’un enregistrement SPF pour celles que vous connaissez, en particulier où le trafic d’entreprise se trouve et publier une stratégie SPF neutre, ? tous les :
  
example.com TXT dans « v = spf1 include:spf.example.com ? tous les »
  
La stratégie SPF neutre signifie que tous les messages envoyés fourni en dehors de votre infrastructure d’entreprise transmettra l’authentification du courrier électronique à tous les autres destinataires de courrier électronique. Courrier provenant d’expéditeurs que vous ne connaissez revient à neutre, qui est presque identique à celle aucun enregistrement SPF tout.
  
Lors de l’envoi vers Office 365, courrier électronique provenant de votre entreprise trafic sera marqué comme authentifié, mais le courrier électronique provenant de sources que vous ne connaissez peut toujours être marqué comme étant usurpation d’identité (en fonction ou non Office 365 peut authentifier implicitement il). Toutefois, il s’agit toujours une amélioration à partir de tout le courrier est marqué comme usurpation d’identité par Office 365.
  
Une fois que vous avez obtenu en route avec un enregistrement SPF avec une stratégie de secours ? tous, vous pouvez inclure progressivement infrastructure d’envoi plus et puis publier une stratégie plus stricte. 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a>Que se passe-t-il si vous êtes le propriétaire d’une liste de distribution ?

Voir la section [listes de scénario courant #2 - Discussion](#common-scenario-2---discussion-lists). 
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a>Que se passe-t-il si vous êtes un fournisseur d’infrastructure comme un fournisseur de services (Internet), fournisseur de Service de messagerie (ESP) ou dans le cloud hébergeant le service ?

Si vous hébergez messagerie d’un domaine, et il envoie un courrier électronique, ou fournir une infrastructure d’hébergement qui permettre envoyer un message électronique, vous devez procédez comme suit :
  
- Vérifiez vos clients documentation décrivant comment publier dans leurs enregistrements SPF
    
- Tenez compte des signatures DKIM de signature de courrier électronique sortant même si le client ne définie explicitement (connexion avec un domaine par défaut). Vous pouvez même double-signer le courrier électronique avec les signatures DKIM (une seule fois avec le domaine du client si elles ont le configurées et une deuxième fois avec la signature de votre société DKIM)
    
Remise des messages à Microsoft ne sont pas garanti même si vous authentifier provenant de votre plateforme de messagerie, mais au moins garantit que Microsoft légitime votre courrier électronique, car il n’est pas authentifié. Pour plus de détails autour comment Outlook.com filtres de courrier électronique, consultez la [page administrateur Outlook.com](https://postmaster.live.com/pm/postmaster.aspx).
  
Pour plus d’informations sur les recommandations de fournisseurs de service, voir [M3AAWG Mobile Messaging meilleures pratiques pour les fournisseurs de services](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).
  
## <a name="frequently-asked-questions"></a>Forum Aux Questions

### <a name="why-is-microsoft-making-this-change"></a>Pourquoi est-ce que Microsoft effectuer cette modification ?

En raison des attaques de l’impact de l’hameçonnage et étant donné que l’authentification du courrier électronique a été autour de plus de 15 ans, Microsoft estime que le risque de continue à autoriser la messagerie non authentifié est plus élevée que les risques de perte de courrier légitime.
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a>Cette modification entraînera électroniques légitimes doit être marqué comme courrier indésirable ?

Dans un premier temps, il y aura des messages qui sont marqués comme courrier indésirable. Toutefois, au fil du temps, ajustent expéditeurs et ensuite la quantité de messages mal étiquetées en tant qu’usurpés sera négligeable pour la plupart des chemins d’accès du courrier électronique.
  
Microsoft lui-même adopté tout d’abord cette fonctionnalité plusieurs semaines avant le déploiement sur le reste de ses clients. Alors que les interruptions en premier lieu, elle progressivement refusée.
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a>Microsoft apportera cette fonctionnalité pour les clients Outlook.com et non - avancée contre les menaces d’Office 365 ?

La technologie anti-usurpation de Microsoft a été initialement déployée à ses organisations qui avaient un abonnement à Office 365 entreprise E5 ou avaient acheté module complémentaire de leur abonnement Office 365 Advanced Threat Protection (DAV). À compter d’octobre, 2018, nous avons étendu la protection pour les organisations ayant ainsi que Exchange Online Protection (EOP). À l’avenir, nous pouvons diffuser Outlook.com. Toutefois, dans ce cas, il peut y avoir des fonctions qui ne sont pas appliquées telles que la création de rapports et des remplacements personnalisés.
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a>Comment signaler les messages de courrier indésirable ou non-spam retour à Microsoft ?

Vous pouvez utiliser le [complément de Message de rapport pour Outlook](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2), ou si elle n’est pas installé, [Envoyer du courrier indésirable, non-, messages indésirables et phishing anti-spam à Microsoft pour analyse](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx).
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a>Je suis un administrateur de domaine ne sait pas qui sont tous les expéditeurs mon !

Consultez [les administrateurs des domaines qui ne sont pas des clients Office 365](#administrators-of-domains-that-are-not-office-365-customers).
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a>Que se passe-t-il si je désactiver protection anti-l’usurpation d’identité pour mon organisation, même si Office 365 est mon filtre primaire ?

Nous ne recommandons pas cette opération, car vous disposerez plus manqué hameçonnage et les messages de courrier indésirable. Usurpation d’hameçonnage pas tous, et seront manquer falsifiés pas tous. Toutefois, les risques sera supérieure à un client qui permet l’usurpation d’identité contre.
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a>Activation de la protection anti-usurpation signifie de que s’être protégé contre le hameçonnage tous les ?

Malheureusement, non, étant donné que les auteurs de phishing s’adapte pour utiliser d’autres techniques telles que compromise des comptes ou des comptes de services gratuits. Toutefois, la protection anti-hameçonnage fonctionne mieux détecter ces autres types de méthodes de hameçonnage, car la protection d’Office 365 calques sont conçus travail ensemble et créer les uns sur les autres.
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a>Autres récepteurs de grande taille ne bloquent des courrier non authentifié ?

Presque tous les récepteurs de grande taille implémentent traditionnel SPF DKIM et DMARC. Des récepteurs d’ont autres contrôles qui se trouvent plus stricts qu’uniquement les standards, mais peu accédez comme non authentifié Office 365 pour bloquer la messagerie et les traiter comme une usurpation d’identité. Toutefois, la plupart de l’industrie devient plus strict sur ce type particulier de courriers électroniques, notamment en raison du problème de hameçonnage.
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a>Dois-je toujours l’option Advanced Spam Filtering activée pour « Échec dur SPF » si l’usurpation d’identité anti activer ?

Non, cette option n’est plus nécessaire, car la fonctionnalité anti-usurpation considère comme non seulement échoue dur SPF, mais un ensemble de critères beaucoup plus large. Si vous avez activé l’usurpation anti et l’option SPF dur échouent est activée, vous obtiendrez probablement plus de faux positifs. Nous vous recommandons de désactiver cette fonctionnalité, car il serait fournissent presque sans conditions supplémentaires pour le courrier indésirable ou hameçonnage et à la place générer principalement de faux positifs.
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a>Schéma de réécriture d’expéditeur (SRS) permet-elle de résoudre électroniques transférés ?

SRS ne résout que partiellement le problème de courriers électroniques transférés. Par la réécriture le SMTP MAIL FROM, SRS peut faire en sorte que SPF passes message transféré à l’emplacement suivant. Toutefois, étant donné que l’usurpation d’identité anti est en fonction de : adresse en combinaison avec le domaine de la messagerie à partir d’ou signature DKIM (ou autres signaux), il n’est pas suffisant empêcher électroniques transférés d’être marqué comme étant usurpés.
  

