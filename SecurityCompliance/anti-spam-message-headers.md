---
title: En-têtes de messages anti-courrier indésirable
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
ms.collection:
- M365-security-compliance
description: Lorsque Exchange Online Protection analyse un message entrant, il insère l'en-tête **X-Forefront-Antispam-Report** dans chaque message.
ms.openlocfilehash: 13bcb3598552bbb63bd50b50963b9806c3f34844
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276194"
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
|PCL|Valeur du seuil de probabilité de courrier d'hameçonnage (PCL) du message. |
|SRV:BULK|Le message a été identifié comme un message électronique en masse. Si l' **option avancée de filtrage du courrier indésirable Bloquer tous les envois de messages électroniques en masse** est activée, le message sera marqué comme courrier indésirable. Si cette option est désactivée, le message sera uniquement marqué comme courrier indésirable si le reste des règles de filtrage déterminent que le message est un courrier indésirable.  |
|SFV:SFE|Le filtrage a été ignoré et le message a été autorisé à passer car il a été envoyé à partir d'une adresse figurant sur la liste des expéditeurs autorisés d'un utilisateur.|
|SFV:BLK|Le filtrage a été ignoré et le message a été bloqué car il a été envoyé à partir d'une adresse figurant sur la liste des expéditeurs bloqués d'un utilisateur.  <br/> **Conseil**: pour plus d'informations sur la façon dont les utilisateurs finaux peuvent créer des listes d'expéditeurs autorisés et bloqués, consultez la rubrique [bloquer ou autoriser (paramètres](https://go.microsoft.com/fwlink/p/?LinkId=294862) du courrier indésirable) (Outlook sur le Web) et [vue d'ensemble du filtre de](https://go.microsoft.com/fwlink/p/?LinkId=270065) courrier indésirable (Outlook).|
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
|SFTY|Le message a été identifié comme hameçonnage et sera marqué avec l'une des valeurs suivantes: <br/>• 9,1: valeur par défaut. Le message contient une URL de hameçonnage, peut contenir un autre contenu de hameçonnage ou a été marqué comme hameçonnage par un autre filtre de messagerie, par exemple une version locale d'Exchange Server avant de transmettre le message à Office 365. <br/>• 9,11: échec du message échec de la détection d'usurpation d'identité lorsque le domaine d'envoi dans l'en-tête From: est identique à ou s'aligne avec ou fait partie de la même organisation que le domaine de réception. Cela indique qu'un Conseil de sécurité d'usurpation intra-organisationnel est ajouté au message. <br/>• 9,19: échec du message vérifications d'usurpation d'identité de domaine lorsque le domaine d'envoi tente d'emprunter l'identité d'un domaine détenu par le récepteur ou d'un domaine personnalisé protégé par la stratégie anti-hameçonnage. Cela indique qu'un Conseil de sécurité d'emprunt d'identité est ajouté au message, s'il est activé par le biais de la stratégie anti-hameçonnage. <br/>• 9,20: échec du message échec de la vérification de l'emprunt d'identité lorsque l'utilisateur expéditeur tente d'emprunter l'identité d'un utilisateur au sein de l'Organisation des récepteurs ou d'un utilisateur personnalisé protégé par la stratégie anti-hameçonnage. Cela indique qu'un Conseil de sécurité d'emprunt d'identité est ajouté au message, s'il est activé par le biais de la stratégie anti-hameçonnage. <br/>• 9,21: le message a échoué les vérifications d'usurpation d'identité et le domaine d'envoi dans l'en-tête From: ne s'authentifient pas et proviennent d'un domaine externe. Utilisé en association avec CompAuth (voir Authentication-Results). <br/>• 9,22: identique à 9,21, sauf que l'utilisateur a un expéditeur approuvé qui a été remplacé. <br/>• 9,23: identique à 9,22, sauf que l'organisation a un expéditeur ou un domaine qui a été remplacé. <br/>• 9,24: identique à 9,23, sauf que l'utilisateur a une règle de flux de messagerie Exchange qui a été remplacée.|
|X-CustomSpam: [ASFOption]|Le message correspond à une option de filtrage avancé du courrier indésirable. Par exemple, **X-CustomSpam: les liens d'image vers des sites** distants indiquent que l'option **liens de l'image vers des sites distants en** ASF a été mise en correspondance. Pour savoir quel texte d'en-tête X est ajouté pour chaque option ASF spécifique, consultez la rubrique [options de filtrage avancé du courrier](advanced-spam-filtering-asf-options.md)indésirable.|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Champs d'en-tête de message X-Microsoft-Antispam
<a name="sectionSection1"> </a>

Le tableau suivant décrit certains champs utiles de l'en-tête **X-Microsoft-Antispam** des messages. Les autres champs de cet en-tête sont exclusivement utilisés par l'équipe Microsoft de lutte contre les courriers indésirables à des fins de diagnostic.
  
|**Champ d'en-tête**|**Description**|
|:-----|:-----|
|BCL|Niveau de réclamation en bloc (Bulk Complaint Level, BCL) du message. Pour plus d'informations, voir [Valeurs BCL](bulk-complaint-level-values.md).  |
|PCL|Niveau de probabilité de courrier d'hameçonnage (PCL) du message, qui indique s'il s'agit d'un message de hameçonnage. Cet État peut être renvoyé sous la forme d'une des valeurs numériques suivantes:<br/>• **0-3**: le contenu du message n'est pas susceptible d'être un hameçonnage. <br/>• **4-8**: le contenu du message est susceptible d'être un hameçonnage. <br/>• **-9990**: (Exchange Online Protection uniquement) le contenu du message est susceptible d'être un hameçonnage.  <br/>  Les valeurs sont utilisées pour déterminer l'action que votre client de messagerie effectue sur les messages. Par exemple, Outlook utilise le cachet PCL pour bloquer le contenu des messages suspects. Pour plus d'informations sur le hameçonnage et la façon dont Outlook traite les messages de hameçonnage, voir [activer ou désactiver les liens dans les messages électroniques](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).|
   
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
|spf|Décrit les résultats de la vérification SPF pour le message. Les valeurs admises sont les suivantes :  <br/>• **passe (adresse IP)**: indique la vérification SPF pour le message transmis et inclut l'adresse IP de l'expéditeur. Le client est autorisé à envoyer ou à relayer le courrier électronique de la part du domaine de l'expéditeur.<br/>• **Fail (adresse IP)**: indique que la vérification SPF pour le message a échoué et inclut l'adresse IP de l'expéditeur. Cela est parfois appelé _échec matériel_.<br/>• **SoftFail (raison)**: indique que l'enregistrement SPF a désigné l'hôte comme n'étant pas autorisé à envoyer mais qu'il est en transition. <br/>• **Neutral**: indique que l'enregistrement SPF a explicitement déclaré qu'il ne déclare pas si l'adresse IP est autorisée. <br/>• **None**: indique que le domaine n'a pas d'enregistrement SPF ou que l'enregistrement SPF n'évalue pas un résultat. <br/>• **TempError**: indique qu'une erreur qui peut être temporaire, par exemple une erreur DNS, s'est produite. Toute tentative ultérieure peut aboutir sans aucune action de l'administrateur.<br/>• **PermError**: indique qu'une erreur permanente s'est produite. Cela se produit lorsque, par exemple, le domaine a un enregistrement SPF mal formaté.|
|SMTP. Mailfrom|Contient le domaine source à partir duquel le message a été envoyé. Les erreurs concernant cet e-mail sont envoyées à l'administrateur ou à l'entité responsable du domaine. Cet élément est parfois appelé adresse 5321.MailFrom ou adresse de chemin inverse sur l'enveloppe du message.|
|dkim|Décrit les résultats de la vérification DKIM du message. Les valeurs admises sont les suivantes :  <br/>• **passe**: indique que la vérification DKIM du message a réussi. <br/>• **Fail (Reason)**: indique que la vérification DKIM du message a échoué et pourquoi. Par exemple, si le message n'a pas été signé ou si la signature n'a pas été vérifiée.<br/>• **None**: indique que le message n'a pas été signé. Cela peut indiquer ou non que le domaine a un enregistrement DKIM ou que l'enregistrement DKIM ne correspond pas à un résultat, uniquement que ce message n'a pas été signé.|
|en-tête. d|Domaine défini dans la signature DKIM, s'il y en a un. Il s'agit du domaine auquel la clé publique est demandée.|
|dmarc|Décrit les résultats de la vérification DMARC pour le message. Les valeurs admises sont les suivantes :  <br/>• **passe**: indique que la vérification DMARC pour le message a réussi. <br/>• **Fail**: indique que la vérification DMARC pour le message a échoué. <br/>• **bestguesspass**: indique qu'aucun enregistrement txt DMARC pour le domaine n'existe, mais si l'un d'entre eux existait, la vérification DMARC pour le message aurait réussi. Cela est dû au fait que le domaine de l'adresse 5321. MailFrom correspond au domaine dans l'adresse 5322. from.<br/>• **None**: indique qu'il n'existe aucun enregistrement txt DKIM pour le domaine expéditeur dans le système DNS.|
|action|Indique l'action effectuée par le filtre de courrier indésirable en fonction des résultats de la vérification DMARC. Par exemple :  <br/>• **PermError**: une erreur permanente s'est produite lors de l'évaluation d'DMARC, telle qu'un enregistrement txt DMARC incorrect dans le système DNS. La tentative de renvoi de ce message ne peut pas se terminer par un autre résultat. Au lieu de cela, vous devrez peut-être contacter le propriétaire du domaine afin de résoudre le problème.<br/>• **TempError**: une erreur temporaire s'est produite lors de l'évaluation d'DMARC. Vous pouvez demander à l'expéditeur de renvoyer le message ultérieurement afin de traiter correctement le courrier.<br/>• **oreject** ou **o. Reject**: signifie remplacer le rejet. Dans ce cas, Office 365 utilise cette action lorsqu'il reçoit un message qui fait échouer la vérification DMARC à partir d'un domaine dont l'enregistrement TXT DMARC possède la stratégie p = refuser. Au lieu de supprimer ou de rejeter le message, Office 365 marque le message comme courrier indésirable. Pour plus d'informations sur la façon dont Office 365 est configuré de cette façon, voir [How office 365 handle le courrier électronique entrant qui échoue DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).<br/>• **PCT. Quarantine**: indique qu'un pourcentage inférieur à 100% des messages qui ne transmettent pas de DMARC sera quand même remis. Cela signifie que le message a échoué DMARC et que la stratégie a été définie sur Quarantine, mais que le champ PCT n'a pas la valeur 100% et que le système a déterminé de façon aléatoire de ne pas appliquer l'action DMARC, conformément à la stratégie du domaine spécifié.<br/>• **PCT. Reject**: indique qu'un pourcentage inférieur à 100% des messages qui ne transmettent pas de DMARC sera quand même remis. Cela signifie que le message a échoué DMARC et que la stratégie a été définie sur refuser, mais que le champ PCT n'a pas la valeur 100% et que le système a déterminé de façon aléatoire de ne pas appliquer l'action DMARC, conformément à la stratégie du domaine spécifié.|
|en-tête. from|Domaine de l'adresse de l'adresse de l'en-tête du message électronique. Il s'agit parfois de l'adresse _5322. from_ .|
|compauth|Résultat de l'authentification composite. Utilisé par Office 365 pour combiner plusieurs types d'authentification, tels que SPF, DKIM, DMARC ou toute autre partie du message afin de déterminer si le message est authentifié ou non. Utilise le domaine from: comme base de l'évaluation.|
|origine|Raison pour laquelle l'authentification composite a réussi ou échoué. La valeur du motif est composée de trois chiffres:<br/>• **000**: l'authentification du message a échoué explicitement. Par exemple, le message reçu une DMARC échoue avec une action de mise en quarantaine ou rejet.<br/>• **001**: l'authentification du message a échoué implicitement et le domaine d'envoi n'a pas publié les stratégies d'authentification. Par exemple, une stratégie DMARC de p = None.<br/>• **1xx**: l'authentification du message a réussi. Les deux chiffres sont des codes internes utilisés par Office 365.<br/>• **2xx**: l'authentification à transmission logicielle. Les deux chiffres sont des codes internes utilisés par Office 365.<br/>• **3xx**: le message n'a pas été vérifié pour l'authentification composite. <br/>• **4xx**: le message a contourné l'authentification composite. Les deux chiffres sont des codes internes utilisés par Office 365.|
