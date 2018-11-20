---
title: En-têtes de messages anti-courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
description: Lorsque Exchange Online Protection analyse un message entrant, il insère l'en-tête **X-Forefront-Antispam-Report** dans chaque message.
ms.openlocfilehash: 39cac8e1406bd4f7505ae4bc626b8c7e78f88101
ms.sourcegitcommit: 75b985b2574f4be70cf352498ea300b3d99dd338
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/10/2018
ms.locfileid: "26255889"
---
# <a name="anti-spam-message-headers"></a>En-têtes de messages anti-courrier indésirable

Lorsque Exchange Online Protection analyse un message entrant, il insère l'en-tête **X-Forefront-Antispam-Report** dans chaque message. Les champs de cet en-tête permettent de fournir des informations aux administrateurs en ce qui concerne le message et sur la manière dont ce dernier a été traité. Les champs de l'en-tête **X-Microsoft-Antispam** fournissent des informations supplémentaires sur le courrier en nombre et le hameçonnage. En plus de ces deux en-têtes, Exchange Online Protection insère également les résultats de l'authentification d'e-mail pour chaque message qu'il traite dans l'en-tête **Authentication-results** (résultats de l'authentification).
  
> [!TIP]
> Pour plus d'informations sur le mode d'affichage de l'en-tête d'un message électronique dans divers clients de messagerie, voir [Analyseur d'en-têtes de message](https://go.microsoft.com/fwlink/p/?LinkId=306583). Vous pouvez copier et coller le contenu de l'en-tête du message dans l'[analyseur d'en-têtes de message](https://testconnectivity.microsoft.com/?tabid=mha). Lorsque vous sélectionnez un message dans la zone de quarantaine du centre d'administration Exchange, le lien **Afficher l'en-tête du message** vous permet également de copier le texte de l'en-tête en toute simplicité et de le coller dans l'outil. Une fois dans l'outil Analyseur d'en-tête de message, cliquez sur **Analyser les en-têtes** afin d'obtenir des informations sur l'en-tête.
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>Champs d'en-tête de message X-Forefront-Antispam-Report
<a name="sectionSection0"> </a>

Après avoir accédé aux informations d'un en-tête de message, recherchez **X-Forefront-Antispam-Report**, puis recherchez les champs ci-dessous. Les autres champs de cet en-tête sont exclusivement utilisés par l'équipe Microsoft de lutte contre les courriers indésirables à des fins de diagnostic.

|**Champ d'en-tête**|**Description**|
|:-----|:-----|
|CIP: [IP address]|Adresse IP de connexion. Vous pouvez spécifier cette adresse IP lors de la création d'une liste d'adresses IP autorisées ou d'une liste d'adresses IP bloquées dans le filtre de connexion. Pour plus d'informations, voir [Configuration de la stratégie de filtrage des connexions](configure-the-connection-filter-policy.md).  |
|CTRY|Pays depuis lequel le message s’est connecté au service. Cette valeur est déterminée par l'adresse IP de connexion, qui peut ne pas être la même que l'adresse IP d'envoi de provenance.|
|LANG|Langue dans laquelle le message a été rédigé, tel que spécifié par le code du pays (par exemple, ru_RU pour le russe).|
|SCL|Valeur du seuil de probabilité de courrier indésirable (SCL) du message. Pour plus d'informations sur l'interprétation de ces valeurs, consultez la rubrique [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).  |
|PCL|Valeur du seuil de probabilité de courrier d'hameçonnage (PCL) du message. Pour plus d'informations sur les valeurs PCL, voir [PCL](anti-spam-message-headers.md#PCL).  |
|SRV:BULK|Le message a été identifié comme un message électronique en masse. Si l' **option avancée de filtrage du courrier indésirable Bloquer tous les envois de messages électroniques en masse** est activée, le message sera marqué comme courrier indésirable. Si cette option est désactivée, le message sera uniquement marqué comme courrier indésirable si le reste des règles de filtrage déterminent que le message est un courrier indésirable.  |
|SFV:SFE|Le filtrage a été ignoré et le message a été autorisé à passer car il a été envoyé à partir d'une adresse figurant sur la liste des expéditeurs autorisés d'un utilisateur.|
|SFV:BLK|Le filtrage a été ignoré et le message a été bloqué car il a été envoyé à partir d'une adresse figurant sur la liste des expéditeurs bloqués d'un utilisateur.  <br/> **Conseil**: pour plus d’informations sur la façon dont les utilisateurs finaux peuvent créer des listes d’expéditeurs autorisés et bloqués, voir [bloquer ou autoriser (paramètres de courrier indésirable)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (Outlook sur le web) et [vue d’ensemble du filtre de courrier indésirable](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).|
|IPV:CAL|Le message n'a pas été bloqué par les filtres anti-spam car l'adresse IP se trouve dans une liste d'adresses IP autorisées du filtre des connexions.|
|IPV:NLI|L'adresse IP n'était répertoriée sur aucune liste de réputation d'adresses IP.|
|SFV:SPM|Le message a été marqué comme courrier indésirable par le filtre de contenu.|
|SFV:SKS|Le message a été marqué comme courrier indésirable avant d’être traité par le filtre de contenu. Cela inclut les messages pour lesquels une règle de transport les a marqués automatiquement comme étant des courriers indésirables et où toutes les étapes de filtrage supplémentaires ont été contournées.|
|SFV:SKA|Le message a ignoré le filtrage et a été remis à la boîte de réception, car il correspond à une liste verte dans la stratégie de filtrage du courrier indésirable, telle que la **liste d'expéditeurs autorisés**.|
|SFV:SKB|Le message a été marqué comme courrier indésirable, car il correspond à une liste rouge dans la stratégie de filtrage du courrier indésirable, telle que la **liste d'expéditeurs bloqués**.|
|SFV:SKN|Le message a été marqué comme courrier non indésirable avant d’être traité par le filtre de contenu. Il s’agit des messages qui ont été marqués automatiquement par une règle de transport comme étant des courriers non indésirables et pour lesquels toutes les étapes de filtrage supplémentaires ont été contournées.|
|SFV:SKI|Semblable à SFV:SKN. Le message a ignoré le filtrage pour une autre raison, par exemple, il s'agissait d'un message électronique intra-organisationnel au sein d'un client.|
|SFV:SKQ|Le message a été libéré de la quarantaine et a été envoyé aux destinataires appropriés.|
|SFV:NSPM|Le message a été marqué comme n'étant pas un courrier indésirable et a été envoyé aux destinataires appropriés.|
|H: [helostring]|Chaîne HELO ou EHLO du serveur de messagerie de connexion.|
|PTR: [ReverseDNS]|Enregistrement PTR, ou enregistrement de pointeur, de l'adresse IP d'envoi, également appelé adresse DNS inverse.|
|SFTY|Le message a été identifié comme hameçonnage et est également marqué avec une des valeurs suivantes : <br/>• 9.1 : valeur par défaut. Le message contient une URL hameçonnage, peut contenir des autres contenus phishing ou ont été marqué comme hameçonnage par un autre filtre de messagerie comme une version locale d’Exchange Server avant de relayer le message vers Office 365. <br/>• 9.11 : échec du message l’usurpation d’identité contre les contrôles où dans le domaine : en-tête est identique, ou s’aligne sur ou fait partie de la même organisation que le domaine de réception. <br/>• 9.21 : échec du message l’usurpation d’identité contre les vérifications et dans le domaine : en-tête n’authentifie pas. Utilisée conjointement avec CompAuth (voir les résultats de l’authentification). <br/>• 9.22 : identique à 9.21, sauf que l’utilisateur dispose d’un expéditeur fiable qui a été remplacé. <br/>• 9.23 : identique à 9.22, sauf que l’organisation a un expéditeur autorisé ou un domaine qui a été remplacé. <br/>• 9,24 : identique à 9.23, sauf que l’utilisateur dispose d’une règle de flux de messagerie Exchange qui a été remplacée.|
|X-CustomSpam: [ASFOption]|Le message correspondait à un option de filtrage avancé du courrier indésirable. Par exemple, **X-CustomSpam : liens vers des sites distants d’Image** indique que l’option **Image des liens vers des sites distants** ASF a été mis en correspondance. Pour savoir comment le texte d’en-tête X est ajouté pour chaque option ASF spécifique, voir [options de filtrage avancé du courrier indésirable](advanced-spam-filtering-asf-options.md).|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Champs d'en-tête de message X-Microsoft-Antispam
<a name="sectionSection1"> </a>

Le tableau suivant décrit certains champs utiles de l'en-tête **X-Microsoft-Antispam** des messages. Les autres champs de cet en-tête sont exclusivement utilisés par l'équipe Microsoft de lutte contre les courriers indésirables à des fins de diagnostic.
  
|**Champ d'en-tête**|**Description**|
|:-----|:-----|
|BCL|Niveau de réclamation en bloc (Bulk Complaint Level, BCL) du message. Pour plus d'informations, voir [Valeurs BCL](bulk-complaint-level-values.md).  |
|PCL|Au niveau de confiance hameçonnage (PCL) du message, ce qui indique s’il s’agit d’un message de phishing. Ce statut peut être retourné en tant qu’une des valeurs numériques suivantes :<br/>• **0-3**: le contenu du message n’est pas susceptible d’être hameçonnage. <br/>• **4 à 8**: le contenu du message est susceptible d’être hameçonnage. <br/>• **-9990**: (Exchange Online Protection uniquement) le contenu du message est susceptible d’être hameçonnage.  <br/>  Les valeurs sont utilisées pour déterminer les mesures de votre client de messagerie prend sur les messages. Par exemple, Outlook utilise le cachet PCL pour bloquer le contenu des messages suspects. Pour plus d’informations sur les attaques par hameçonnage et comment Outlook traite les messages de phishing, voir [Activer ou désactiver les liens dans les messages électroniques](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).|
   
## <a name="authentication-results-message-header"></a>En-tête de message Authentication-results
<a name="sectionSection2"> </a>

Les résultats des vérifications de SPF DKIM et DMARC sont enregistrés ou marqués par Office 365 dans l'en-tête **Authentication-results** des messages lorsque nos serveurs de messagerie reçoivent un e-mail.
  
### <a name="check-stamp-syntax-and-examples"></a>Syntaxe et exemples de marques de vérification
<a name="referenceSPFstamp"> </a>

L'exemple de syntaxe suivant présente une partie de la « marque » au format texte qu'Office 365 applique à l'en-tête du message pour chaque message qui fait l'objet d'une authentification lorsqu'il est reçu par nos serveurs de messagerie. Cette marque est ajoutée à l'en-tête **Authentication-Results**:
  
 **Syntaxe : marque de vérification SPF**
  
Pour SPF, la syntaxe suivante s'applique.
  
```
spf=<pass (IP address)|fail (IP address)|softfail (reason)|neutral|none|temperror|permerror> smtp.mailfrom=<domain>
```

 **Exemples : marque de vérification SPF**
  
```
spf=pass (sender IP is 192.168.0.1) smtp.mailfrom=contoso.com
spf=fail (sender IP is 127.0.0.1) smtp.mailfrom=contoso.com
```

 **Syntaxe : marque de vérification DKIM**
  
Pour DKIM, la syntaxe suivante s'applique.
  
```
dkim=<pass|fail (reason)|none> header.d=<domain>
```

 **Exemples : marque de vérification DKIM**
  
```
dkim=pass (signature was verified) header.d=contoso.com
dkim=fail (body hash did not verify) header.d=contoso.com
```

 **Syntaxe : marque de vérification DMARC**
  
Pour DMARC, la syntaxe suivante s'applique.
  
```
dmarc=<pass|fail|bestguesspass|none> action=<permerror|temperror|oreject|pct.quarantine|pct.reject> header.from=<domain>
```

 **Exemples : marque de vérification DMARC**
  
```
dmarc=pass action=none header.from=contoso.com
dmarc=bestguesspass action=none header.from=contoso.com
dmarc=fail action=none header.from=contoso.com
dmarc=fail action=oreject header.from=contoso.com
```

### <a name="authentication-results-message-header-fields-used-by-office-365-email-authentication"></a>Champs de l'en-tête Authentication-results utilisés par l'authentification de messagerie Office 365
<a name="referenceSPFstamp"> </a>

Le tableau ci-dessous décrit les champs et les valeurs possibles pour chaque vérification d'authentification de courrier électronique.
  
|**Champ d'en-tête**|**Description**|
|:-----|:-----|
|spf|Décrit les résultats de la vérification SPF pour le message. Les valeurs admises sont les suivantes :  <br/>• **transmettre (adresse IP)**: indique la vérification SPF pour le message est passé et inclut l’adresse IP de l’expéditeur. Le client est autorisé à envoyer ou relayer le courrier électronique au nom de domaine de l’expéditeur.<br/>• **Échec (adresse IP)**: indique la vérification SPF de l’échec du message et inclut l’adresse IP de l’expéditeur. Il est parfois appelée _Échec sévère_.<br/>• **softfail (raison)**: indique que l’enregistrement SPF a désigné l’hôte comme n’étant ne pas autorisés à envoyer mais est en transition. <br/>• **neutre**: indique que l’enregistrement SPF a déclaré explicitement qu’il confirme pas si l’adresse IP est autorisée. <br/>• **none**: indique que le domaine ne dispose pas d’un enregistrement SPF ou l’enregistrement SPF ne correspond pas à un résultat. <br/>• **temperror**: indique qu’une erreur s’est produite qui peut être temporaire de nature, par exemple, une erreur DNS. Tentative ultérieurement peut aboutir sans intervention de l’administrateur.<br/>• **permerror**: indique qu’une erreur permanente s’est produite. Cela se produit lorsque, par exemple, le domaine a un enregistrement SPF incorrect.|
|SMTP.MailFrom|Contient le domaine source à partir duquel le message a été envoyé. Les erreurs concernant cet e-mail sont envoyées à l'administrateur ou à l'entité responsable du domaine. Cet élément est parfois appelé adresse 5321.MailFrom ou adresse de chemin inverse sur l'enveloppe du message.|
|dkim|Décrit les résultats de la vérification DKIM du message. Les valeurs admises sont les suivantes :  <br/>• **transmettre**: indique la vérification DKIM pour le message est passé. <br/>• **Échec (raison)**: indique la vérification DKIM pour le message a échoué et pourquoi. Par exemple, si le message n’a pas été signé ou la signature n’a pas été vérifiée.<br/>• **none**: indique que le message n’a pas été signé. Cela peut ou ne peut pas indiquer que le domaine a un enregistrement DKIM ou l’enregistrement DKIM ne correspond pas à un résultat, uniquement que ce message n’a pas été signé.|
|Header.d|Domaine défini dans la signature DKIM, s'il y en a un. Il s'agit du domaine auquel la clé publique est demandée.|
|dmarc|Décrit les résultats de la vérification DMARC pour le message. Les valeurs admises sont les suivantes :  <br/>• **transmettre**: indique la vérification DMARC pour le message est passé. <br/>• **Échec**: indique la vérification DMARC pour le message a échoué. <br/>• **bestguesspass**: indique que n’existe aucun enregistrement TXT DMARC pour le domaine, mais si une existait, la vérification de DMARC pour le message serait se sont écoulées. Il s’agit, car le domaine de l’adresse 5321.MailFrom correspond au domaine de l’adresse 5322.From.<br/>• **none**: indique qu’il n’existe aucun enregistrement TXT DKIM pour le domaine dans DNS.|
|action|Indique l'action effectuée par le filtre de courrier indésirable en fonction des résultats de la vérification DMARC. Par exemple :  <br/>• **permerror**: une erreur permanente s’est produite lors de l’évaluation DMARC, par exemple un TXT DMARC correctement formé enregistrer dans le système DNS. Essayez de renvoyer ce message n’est pas susceptible de se terminer par un résultat différent. Au lieu de cela, vous devrez peut-être contacter le propriétaire du domaine afin de résoudre le problème.<br/>• **temperror**: une erreur temporaire s’est produite lors de l’évaluation DMARC. Vous ne pourrez pas demander à l’expéditeur de renvoyer le message ultérieurement afin de traiter le courrier électronique correctement.<br/>• **oreject** ou **o.reject**: correspond à remplacer le rejet. Dans ce utilise cas Office 365 cette action lorsqu’il reçoit un message qui échoue la DMARC vérifier à partir d’un domaine dont l’enregistrement TXT DMARC dispose d’une stratégie de p = rejeter. Au lieu de supprimer ou de rejeter le message, Office 365 marque le message comme courrier indésirable. Pour plus d’informations sur pourquoi Office 365 est configuré de cette manière, voir [poignées comment Office 365 entrant qui échoue DMARC de messagerie](use-dmarc-to-validate-email.md#inbounddmarcfail).<br/>• **pct.quarantine**: indique qu’un pourcentage inférieur à 100 % des messages qui ne passent pas DMARC est remis malgré tout. Cela signifie que le message d’échec de la DMARC et la stratégie a été définie pour mettre en quarantaine, mais le champ pourcentage n’a pas été défini sur 100 % et le système au hasard déterminée à ne pas appliquer l’action DMARC, selon la stratégie du domaine spécifié.<br/>• **pct.reject**: indique qu’un pourcentage inférieur à 100 % des messages qui ne passent pas DMARC est remis malgré tout. Cela signifie que le message d’échec de la DMARC et la stratégie a été définie pour rejeter, mais le champ pourcentage n’a pas été défini sur 100 % et le système au hasard déterminée à ne pas appliquer l’action DMARC, selon la stratégie du domaine spécifié.|
|Header.From|Le domaine de l’adresse dans l’en-tête du message électronique. Il est parfois appelée l’adresse _5322.From_ .|
|compauth|Résultat de l’authentification composite. Utilisé par Office 365 pour combiner plusieurs types d’authentification comme SPF, DKIM, DMARC ou toute autre partie du message pour déterminer si le message est authentifié. Utilise la provenance : domaine comme base d’évaluation.|
|motif|La raison pour laquelle l’authentification composite réussi ou échoué. La valeur de la raison se compose de trois chiffres :<br/>• **000**: Échec de l’authentification du message explicitement. Par exemple, le message reçu un message d’échec DMARC avec une action de mise en quarantaine ou rejeter.<br/>• **001**: Échec de l’authentification du message implicitement, et le domaine n’avez pas publié les stratégies d’authentification. Par exemple, une stratégie DMARC de p = none.<br/>• **1xx**: le message envoyé à l’authentification. Les deux chiffres sont les codes internes utilisés par Office 365.<br/>• **2xx**: l’authentification transmises récupérable message. Les deux chiffres sont les codes internes utilisés par Office 365.<br/>• **3xx**: le message n’a pas été activé pour l’authentification composite. <br/>• **4xx**: le message contourné authentification composite. Les deux chiffres sont les codes internes utilisés par Office 365.|
