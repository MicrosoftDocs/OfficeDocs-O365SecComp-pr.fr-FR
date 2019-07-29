---
title: En-têtes de messages anti-courrier indésirable
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
ms.collection:
- M365-security-compliance
description: Lorsque Exchange Online Protection analyse un message entrant, il insère l’en-tête **X-Forefront-Antispam-Report** dans chaque message.
ms.openlocfilehash: b83cba8240ff27b9d6e872ad09bf23c2755478c5
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854618"
---
# <a name="anti-spam-message-headers"></a>En-têtes de messages anti-courrier indésirable

Lorsque Exchange Online Protection analyse un message entrant, il insère l'en-tête **X-Forefront-Antispam-Report** dans chaque message. Les champs de cet en-tête permettent de fournir des informations aux administrateurs en ce qui concerne le message et sur la manière dont ce dernier a été traité. Les champs de l'en-tête **X-Microsoft-Antispam** fournissent des informations supplémentaires sur le courrier en nombre et le hameçonnage. En plus de ces deux en-têtes, Exchange Online Protection insère également les résultats de l'authentification d'e-mail pour chaque message qu'il traite dans l'en-tête **Authentication-results** (résultats de l'authentification).

Pour plus d’informations sur le mode d’affichage de l’en-tête d’un message électronique dans divers clients de messagerie, consultez la rubrique [Analyseur d’en-têtes de message](https://go.microsoft.com/fwlink/p/?LinkId=306583). 
  
> [!TIP]
>  Vous pouvez copier et coller le contenu de l’en-tête du message dans l’[Analyseur de message](https://testconnectivity.microsoft.com/?tabid=mha). Cet outil aide à analyser les en-têtes et à les afficher dans un format plus lisible.
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>Champs d’en-tête de message X-Forefront-Antispam-Report

Après avoir accédé aux informations d’un en-tête de message, recherchez **X-Forefront-Antispam-Report**, puis recherchez les champs ci-dessous. Les autres champs de cet en-tête sont exclusivement utilisés par l’équipe Microsoft de lutte contre les courriers indésirables à des fins de diagnostic.

|**Champ d’en-tête**|**Description**|
|:-----|:-----|
|CIP: [IP address]|Adresse IP de connexion. Vous pouvez spécifier cette adresse IP lors de la création d'une liste d'adresses IP autorisées ou d'une liste d'adresses IP bloquées dans le filtre de connexion. Pour plus d'informations, voir [Configuration de la stratégie de filtrage des connexions](configure-the-connection-filter-policy.md).  |
|CTRY|Pays depuis lequel le message s’est connecté au service. Cette valeur est déterminée par l'adresse IP de connexion, qui peut ne pas être la même que l'adresse IP d'envoi de provenance.|
|LANG|Langue dans laquelle le message a été rédigé, tel que spécifié par le code du pays (par exemple, ru_RU pour le russe).|
|SCL|Valeur du seuil de probabilité de courrier indésirable (SCL) du message. Pour plus d'informations sur l'interprétation de ces valeurs, consultez la rubrique [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).  |
|PCL|Valeur du seuil de probabilité de courrier d’hameçonnage (PCL) du message.|
|SRV:BULK|Le message a été identifié comme un message électronique en masse. Si l’**option avancée de filtrage du courrier indésirable Bloquer tous les envois de messages électroniques en masse** est activée, le message sera marqué comme courrier indésirable. Si cette option est désactivée, le message sera uniquement marqué comme courrier indésirable si le reste des règles de filtrage déterminent que le message est un courrier indésirable.|
|SFV:SFE|Le filtrage a été ignoré et le message a été autorisé à passer car il a été envoyé à partir d'une adresse figurant sur la liste des expéditeurs autorisés d'un utilisateur.|
|SFV:BLK|Le filtrage a été ignoré et le message a été bloqué car il a été envoyé à partir d'une adresse figurant sur la liste des expéditeurs bloqués d'un utilisateur.  <br/> **Conseil** : pour plus d’informations sur la façon dont les utilisateurs finals peuvent créer des listes d’expéditeurs autorisés et bloqués, voir [Bloquer ou autoriser (paramètres du courrier indésirable)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (Outlook sur le web) et [À propos du filtre Courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).|
|IPV:CAL|Le message n’a pas été bloqué par les filtres anti-spam car l’adresse IP se trouve dans une liste d’adresses IP autorisées du filtre des connexions.|
|IPV:NLI|L’adresse IP n’était répertoriée sur aucune liste de réputation d’adresses IP.|
|SFV:SPM|Le message a été marqué comme courrier indésirable par le filtre de contenu.|
|SFV:SKS|Le message a été marqué comme courrier indésirable avant d’être traité par le filtre de contenu. Cela inclut les messages qui ont été marqués automatiquement comme étant des courriers indésirables par une règle de flux de courrier (également appelée règle de transport) et pour lesquels toutes les étapes de filtrage supplémentaires ont été contournées.|
|SFV:SKA|Le message a ignoré le filtrage et a été remis à la boîte de réception, car il correspond à une liste verte dans la stratégie de filtrage du courrier indésirable, telle que la **liste d’expéditeurs autorisés**.|
|SFV:SKB|Le message a été marqué comme courrier indésirable, car il correspond à une liste rouge dans la stratégie de filtrage du courrier indésirable, telle que la **liste d’expéditeurs bloqués**.|
|SFV:SKN|Le message a été marqué comme courrier non indésirable avant d’être traité par le filtre de contenu. Il s’agit des messages qui ont été marqués automatiquement par une règle de flux de courrier comme étant des courriers non indésirables et pour lesquels toutes les étapes de filtrage supplémentaires ont été contournées.|
|SFV:SKI|Semblable à SFV:SKN. Le message a ignoré le filtrage pour une autre raison, par exemple, il s’agissait d’un message électronique intra-organisationnel au sein d’un client.|
|SFV:SKQ|Le message a été libéré de la quarantaine et a été envoyé aux destinataires appropriés.|
|SFV:NSPM|Le message a été marqué comme n’étant pas un courrier indésirable et a été envoyé aux destinataires appropriés.|
|H: [helostring]|Chaîne HELO ou EHLO du serveur de messagerie de connexion.|
|PTR: [ReverseDNS]|Enregistrement PTR, ou enregistrement de pointeur, de l’adresse IP d’envoi, également appelé adresse DNS inverse.|
|SFTY|Le message a été identifié en tant que hameçonnage et il est marqué avec l’une des valeurs suivantes : <br/>• 9.1 : valeur par défaut. Le message contient une URL de hameçonnage, peut contenir d’autres contenus de hameçonnage ou peut avoir été marqué comme un message de hameçonnage par un autre filtre de messagerie, comme une version locale d’Exchange Server avant de relayer le message à Office 365. <br/>• 9.11 : le message a échoué aux vérifications anti-falsification, et le domaine d’envoi figurant dans l'en-tête From: est le même que, correspond à ou fait partie de la même organisation que le domaine de réception. Cela indique qu’une astuce d’emprunt d’identité intra-organisationnelle sera ajoutée au message. <br/>• 9.19 : l’emprunt d’identité d’un message échoue lorsque le domaine expéditeur tente d’emprunter l’identité d’un domaine appartenant au destinataire, ou l’identité d’un domaine personnalisé protégé par la stratégie anti-hameçonnage. Cela indique qu’une astuce d’emprunt d’identité sera ajoutée au message si elle est activée via la stratégie anti-hameçonnage. <br/>• 9.20 : l’emprunt d’identité d’un message échoue lorsque l’utilisateur expéditeur tente d’emprunter l’identité d’un utilisateur dans l’organisation des destinataires ou l’identité d’un utilisateur protégé par la stratégie anti-hameçonnage. Cela indique qu’une astuce d’emprunt d’identité sera ajoutée au message si elle est activée via la stratégie anti-hameçonnage. <br/>• 9.21 : le message a échoué aux vérifications anti-falsification, et le domaine d’envoi figurant dans l'en-tête From: ne s’authentifie pas et provient d'un domaine externe. Utilisé en association avec CompAuth (voir Authentication-Results). <br/>• 9.22 : similaire au point 9.21 hormis que l’utilisateur possède un expéditeur approuvé qui a été remplacé. <br/>• 9.23 : similaire au point 9.22 hormis que l’organisation possède un expéditeur ou un domaine autorisé qui a été remplacé. <br/>• 9.24 : similaire au point 9.23 hormis que l’utilisateur possède une règle de flux de courrier Exchange qui a été remplacée.|
|X-CustomSpam: [ASFOption]|Le message établit une correspondance avec une option avancée de filtrage de courrier indésirable. Par exemple, **Liens d’image vers des sites distants** indique que l’option ASF **Liens d’image vers des sites distants** a établi une correspondance. Pour connaître le texte d’en-tête X ajouté à chaque option ASF spécifique, voir [Options de filtrage avancé du courrier indésirable](advanced-spam-filtering-asf-options.md).|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Champs d’en-tête de message X-Microsoft-Antispam

Le tableau suivant décrit certains champs utiles de l’en-tête **X-Microsoft-Antispam** des messages. Les autres champs de cet en-tête sont exclusivement utilisés par l’équipe Microsoft de lutte contre les courriers indésirables à des fins de diagnostic.
  
|**Champ d’en-tête**|**Description**|
|:-----|:-----|
|BCL|Niveau de réclamation en bloc (Bulk Complaint Level, BCL) du message. Pour plus d'informations, voir [Valeurs BCL](bulk-complaint-level-values.md).  |
|PCL|Seuil de probabilité de courrier d'hameçonnage du message, qui indique s'il s'agit d'un message de hameçonnage. Le statut est renvoyé avec l’une des valeurs numériques suivantes : <br/>• **0-3** : le contenu du message ne correspond probablement pas à du hameçonnage. <br/>• **4-8** : le contenu du message correspond probablement à du hameçonnage. <br/>• **-9990** : (Exchange Online Protection uniquement) le contenu du message correspond probablement à du hameçonnage.  <br/>  Ces valeurs permettent de déterminer les mesures prises par votre client de messagerie vis-à-vis des messages. Par exemple, Outlook utilise le marquage PCL pour bloquer le contenu des messages suspects. Pour plus d’informations sur le hameçonnage et la façon dont Outlook traite les messages de hameçonnage, voir [Activer ou désactiver les liens dans les courriers électroniques](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).|
   
## <a name="authentication-results-message-header"></a>En-tête de message Authentication-results

Les résultats des vérifications de SPF DKIM et DMARC sont enregistrés ou marqués par Office 365 dans l’en-tête **Authentication-results** des messages lorsque nos serveurs de messagerie reçoivent un e-mail.
  
### <a name="check-stamp-syntax-and-examples"></a>Syntaxe et exemples de marques de vérification

L’exemple de syntaxe suivant présente une partie de la « marque » au format texte qu’Office 365 applique à l’en-tête du message pour chaque message qui fait l’objet d’une authentification lorsqu’il est reçu par nos serveurs de messagerie. Cette marque est ajoutée à l’en-tête **Authentication-Results** :
  
**Syntaxe : marque de vérification SPF**
  
Pour SPF, la syntaxe suivante s’applique.
  
```
spf=<pass (IP address)|fail (IP address)|softfail (reason)|neutral|none|temperror|permerror> smtp.mailfrom=<domain>
```

**Exemples : marque de vérification SPF**
  
```
spf=pass (sender IP is 192.168.0.1) smtp.mailfrom=contoso.com
spf=fail (sender IP is 127.0.0.1) smtp.mailfrom=contoso.com
```

**Syntaxe : marque de vérification DKIM**
  
Pour DKIM, la syntaxe suivante s’applique.
  
```
dkim=<pass|fail (reason)|none> header.d=<domain>
```

**Exemples : marque de vérification DKIM**
  
```
dkim=pass (signature was verified) header.d=contoso.com
dkim=fail (body hash did not verify) header.d=contoso.com
```

**Syntaxe : marque de vérification DMARC**
  
Pour DMARC, la syntaxe suivante s’applique.
  
```
dmarc=<pass|fail|bestguesspass|none> action=<permerror|temperror|oreject|pct.quarantine|pct.reject> header.from=<domain>
```

**Exemples : marque de vérification DMARC**
  
```
dmarc=pass action=none header.from=contoso.com
dmarc=bestguesspass action=none header.from=contoso.com
dmarc=fail action=none header.from=contoso.com
dmarc=fail action=oreject header.from=contoso.com
```

### <a name="authentication-results-message-header-fields-used-by-office-365-email-authentication"></a>Champs de l’en-tête Authentication-results utilisés par l’authentification de messagerie Office 365

Le tableau ci-dessous décrit les champs et les valeurs possibles pour chaque vérification d’authentification de courrier électronique.
  
|**Champ d’en-tête**|**Description**|
|:-----|:-----|
|spf|Décrit les résultats de la vérification SPF pour le message. Les valeurs admises sont les suivantes : <br/>• **pass (adresse IP)**  : indique que le message a réussi la vérification SPF et fournit l’adresse IP de l’expéditeur. Le client est autorisé à envoyer ou à relayer l’e-mail avec le domaine de l’expéditeur. <br/>• **fail (adresse IP)**  : indique que le message a échoué à la vérification SPF et fournit l’adresse IP de l’expéditeur. Dans ce cas, on parle parfois d’_échec sévère_. <br/>• **softfail (raison)**  : indique que l’enregistrement SPF a désigné l’hôte comme n’étant pas autorisé à envoyer mais qu’il est en transition. <br/>• **neutral** : indique que l’enregistrement SPF déclare explicitement qu’il ne peut pas confirmer si l’adresse IP est autorisée. <br/>• **none** : indique que le domaine n’a pas d’enregistrement SPF ou que l’évaluation de l’enregistrement SPF ne donne aucun résultat. <br/>• **temperror** : indique qu’une erreur pouvant être de nature temporaire s’est produite ; il s’agit, par exemple, d’une erreur DNS. L’opération est susceptible de réussir sans intervention de l’administrateur si vous réessayez ultérieurement. <br/>• **permerror** : indique qu’une erreur permanente s’est produite. Cela peut se produire, par exemple, si l’enregistrement SPF du domaine est mal formaté.|
|smtp.mailfrom|Contient le domaine source à partir duquel le message a été envoyé. Les erreurs concernant cet e-mail sont envoyées à l'administrateur ou à l'entité responsable du domaine. Cet élément est parfois appelé adresse 5321.MailFrom ou adresse de chemin inverse sur l'enveloppe du message.|
|dkim|Décrit les résultats de la vérification DKIM du message. Les valeurs admises sont les suivantes : <br/>• **pass** : indique que le message a satisfait à la vérification DKIM. <br/>• **fail (raison)**  : indique que le message ne satisfait pas à la vérification DKIM et pourquoi. Par exemple, parce que le message n’a pas été signé ou que la signature n’a pas été vérifiée. <br/>• **none** : indique que le message n’a pas été signé. Cela n’indique pas forcément que le domaine a un enregistrement DKIM ou que l’évaluation de l’enregistrement DKIM ne donne pas de résultat, mais simplement que ce message n’a pas été signé.|
|header.d|Domaine défini dans la signature DKIM, s'il y en a un. Il s'agit du domaine auquel la clé publique est demandée.|
|dmarc|Décrit les résultats de la vérification DMARC pour le message. Les valeurs admises sont les suivantes : <br/>• **pass** : indique que le message a satisfait à la vérification de DMARC. <br/>• **fail** : indique que le message a échoué à la vérification DMARC. <br/>**bestguesspass** : indique qu’il n’existe aucun enregistrement TXT DMARC pour le domaine, mais que s’il en existait un, la vérification DMARC aurait accepté le message. En effet, le domaine est le même dans l’adresse 5321.MailFrom et dans l’adresse 5322.From. <br/>• **none** : indique qu’il n’existe aucun enregistrement TXT DKIM pour le domaine expéditeur dans le système DNS.|
|action|Indique l’action effectuée par le filtre de courrier indésirable en fonction des résultats de la vérification DMARC. Par exemple : <br/>• **permerror** : indique qu’une erreur permanente s’est produite lors de l'évaluation DMARC, par exemple, qu’un enregistrement TXT DMARC mal formé a été détecté dans le système DNS. Toute tentative de renvoyer le message produira sans doute le même résultat. Essayez plutôt de contacter le propriétaire du domaine pour résoudre le problème. <br/>• **temperror** : indique qu’une erreur temporaire s’est produite lors de l’évaluation DMARC. Vous pouvez demander à l’expéditeur de renvoyer son message plus tard pour qu’il soit traité correctement. <br/>• **oreject** ou **o.reject** : signifie « override reject » (ignorer le rejet). Office 365 utilise cette action lorsqu’il reçoit un message qui échoue aux vérifications de DMARC et qui sont issus d’un domaine dont l’enregistrement TXT DMARC a pour stratégie p=reject (rejet). Au lieu de supprimer ou de rejeter le message, Office 365 le marque comme courrier indésirable. Pour obtenir des explications sur cette configuration d’Office 365, reportez-vous à la section [Gestion des messages électroniques entrants qui échouent aux vérifications de DMARC dans Office 365](use-dmarc-to-validate-email.md#inbounddmarcfail). <br/>• **pct.quarantine** : indique qu’un pourcentage inférieur à 100 % des messages n’ayant pas satisfait aux vérifications DMARC seront remis malgré tout. Cela signifie que le message n'a pas satisfait les vérifications DMARC et que la stratégie a été définie de manière à mettre les messages en quarantaine, mais que le champ pct n'a pas été défini sur 100 % et que le système a déterminé aléatoirement de ne pas appliquer l'action DMARC conformément à la stratégie du domaine spécifié. <br/>• **pct.reject** : indique qu’un pourcentage inférieur à 100 % des messages n'ayant pas satisfait aux vérifications DMARC seront remis malgré tout. Cela signifie que le message n'a pas satisfait les vérifications DMARC et que la stratégie a été définie de manière à rejeter les messages, mais que le champ pct n'a pas été défini sur 100 % et que le système a déterminé aléatoirement de ne pas appliquer l'action DMARC conformément à la stratégie du domaine spécifié.|
|header.from|Domaine de l’adresse From (5322.From) dans l’en-tête de l’e-mail. Elle est parfois appelée _adresse 5322.From_.|
|compauth|Résultat de l’authentification composite. Utilisé par Office 365 pour combiner plusieurs types d’authentification tels que SPF, DKIM, DMARC ou toute autre partie du message pour déterminer si le message est authentifié ou non. Utilise le domaine From: comme base d’évaluation.|
|reason (Raison)|Raison pour laquelle l’authentification composite a réussi ou échoué. La valeur de la raison est constituée de trois chiffres : <br/>• **000** : le message a échoué de façon explicite. Par exemple, le message a reçu un échec DMARC et déclenché une action de mise en quarantaine. <br/>• **001** : l’authentification du message a implicitement échoué, et le domaine d’envoi n’a pas publié de stratégies d’authentification. Par exemple, une stratégie DMARC avec p=none. <br/>• **1xx** : il s’agit de l’authentification réussie du message. Les deux autres chiffres sont des codes internes utilisés par Office 365. <br/>• **2xx** : il s’agit de l’authentification avec transfert logiciel. Les deux autres chiffres sont des codes internes utilisés par Office 365. <br/>• **3xx** : le message n’a pas été vérifié pour l’authentification composite. <br/>• **4xx** : le message a contourné l’authentification composite. Les deux autres chiffres sont des codes internes utilisés par Office 365.|
