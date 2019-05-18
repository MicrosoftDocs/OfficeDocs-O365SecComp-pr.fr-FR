---
title: Règles de flux de messagerie (règles de transport) dans Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/29/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9c2cf227-eff7-48ef-87fb-487186e47363
description: Vous pouvez utiliser des règles de flux de messagerie (règles de transport) pour identifier et effectuer des actions sur les messages qui circulent dans votre organisation Office 365.
ms.openlocfilehash: 73f5668be76a20af7474f6de06d50e278057fd06
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153146"
---
# <a name="mail-flow-rules-transport-rules-in-exchange-online-protection"></a>Règles de flux de messagerie (règles de transport) dans Exchange Online Protection

Vous pouvez utiliser des règles de flux de messagerie (également appelées règles de transport) pour identifier les messages qui circulent dans votre organisation Office 365 et agir sur ceux-ci. Les règles de flux de messagerie sont semblables aux règles de boîte de réception disponibles dans Outlook et Outlook sur le web. La principale différence réside dans le fait que les règles de flux de messagerie agissent sur les messages pendant qu'ils sont en transit, et non une fois qu'ils ont été remis dans la boîte aux lettres. Les règles de flux de messagerie contiennent un plus vaste ensemble de conditions, d'exceptions et d'actions, ce qui vous permet de mettre en place facilement plusieurs types de stratégies de messagerie.
  
Cet article décrit les composants des règles de flux de messagerie et leur fonctionnement.
  
Pour connaître les étapes à suivre pour créer, copier et gérer les règles de flux de messagerie, consultez la rubrique **Manage mail Flow Rules**. Pour chaque règle, vous avez la possibilité de l'appliquer, de la tester ou bien de la tester et d'avertir l'expéditeur. Pour en savoir plus sur les options de test, voir **tester une règle de flux de messagerie** et **conseils de stratégie**.
  
Pour obtenir un résumé et des rapports détaillés concernant les messages qui correspondent aux règles de flux de messagerie, consultez la rubrique **Utilisation des rapports de protection de messagerie dans Office 365 pour afficher les données sur les programmes malveillants, le courrier électronique et les détections de règles**.
  
Pour mettre en œuvre des stratégies de messagerie spécifiques à l'aide de règles de flux de messagerie, consultez ces rubriques :
  
- [Utilisez des règles de flux de messagerie pour analyser les pièces jointes des messages dans Office 365.](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)
    
- [Configurer le chiffrement dans Office 365 Entreprise](https://support.office.com/article/e86fc991-0161-4f01-9c1c-d25e87733d06)
    
- [Clauses d’exclusion de responsabilité, signatures, pieds de page ou en-têtes de message à l’échelle de l’organisation dans Office 365](http://technet.microsoft.com/library/29ac61c2-77f1-4071-b14e-8cc64e3e76ba.aspx)
    
- [Utilisation des règles de flux de courrier pour définir le seuil de probabilité de courrier indésirable (SCL) dans les messages](../use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)
    
- [Créer des listes d’expéditeurs bloqués et autorisés à l’échelle de l’organisation dans Office 365](../create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365.md)
    
- [Réduction des menaces de programmes malveillants par le biais du blocage des pièces jointes de fichier dans Exchange Online Protection](reducing-malware-threats-through-file-attachment-blocking-in-exchange-online-pro.md)
    
- [Définir des règles pour chiffrer ou déchiffrer des messages électroniques](https://go.microsoft.com/fwlink/p/?Linkid=402846)
    
La vidéo suivante fournit une démonstration de la configuration des règles de flux de messagerie dans Exchange Online Protection.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/7cdcd2cb-9382-4065-98e1-81257b32a189?autoplay=false]
  
## <a name="mail-flow-rule-components"></a>Composants de règle de flux de messagerie

Une règle de flux de messagerie est constituée de conditions, d'exceptions, d'actions et de propriétés :
  
- **Conditions** Identifient les messages auxquels que vous souhaitez appliquer les actions. Certaines conditions examinent les champs d'en-tête de message (par exemple, les champs À, De ou Cc). D'autres examinent les propriétés des messages (par exemple l'objet, le corps, les pièces jointes, la taille ou la classification du message). La plupart des conditions font appel à un opérateur de comparaison (par exemple, « égal à », « différent de » ou « contient ») ainsi qu'à une valeur de concordance que vous devez spécifier. S'il n'y a ni conditions ni d'exceptions, la règle s'applique à tous les messages. 
    
    Pour plus d’informations sur les conditions des règles de flux de messagerie dans Exchange Online Protection, consultez la rubrique [mail Flow Rule conditions and exceptions (prédicats) in Exchange Online.](https://docs.microsoft.com/en-us/exchange/security-and-compliance/mail-flow-rules/conditions-and-exceptions).
    
- **Exceptions** Identifient éventuellement les messages auxquels les actions ne doivent pas s'appliquer. Les identificateurs de message disponibles dans les conditions le sont également dans les exceptions. Les exceptions ont la priorité sur les conditions et empêchent l'application d'actions à un message, même s'il remplit toutes les conditions configurées. 
    
- **Actions** Spécifient que faire des messages qui remplissent les conditions de la règle et qui ne correspondent à aucune des exceptions. De nombreuses actions sont possibles, notamment le rejet, la suppression ou la redirection de messages, l'ajout de destinataires supplémentaires, l'ajout de préfixes à l'objet des messages ou l'insertion de clauses d'exclusion de responsabilité dans le corps des messages. 
    
    Pour plus d’informations sur les actions de règle de flux de messagerie disponibles dans Exchange Online Protection, consultez la rubrique [mail Flow Rule actions in Exchange Online Protection](http://technet.microsoft.com/library/f8621ecb-a177-4025-9011-a6569999746a.aspx).
    
- **Propriétés** Spécifient d'autres paramètres de règles qui ne sont pas des conditions, des exceptions ou des actions. Par exemple, lorsque la règle doit être appliquée, les propriétés indiquent s'il faut appliquer ou tester la règle, ainsi que la période de temps sur laquelle la règle reste active. 
    
     Pour plus d'informations, consultez la section [Propriétés de règle de flux de messagerie](mail-flow-rules-transport-rules-0.md#Properties) dans cette rubrique. 
    
### <a name="multiple-conditions-exceptions-and-actions"></a>Plusieurs conditions, exceptions et actions

Le tableau suivant explique comment plusieurs conditions, valeurs de condition, exceptions et actions sont traitées dans une règle.
  
|**Composant**|**Logique**|**Comments**|
|:-----|:-----|:-----|
|Commentaires  <br/> |AND  <br/> |Un message doit remplir toutes les conditions de la règle. Si vous souhaitez qu'une condition ou une autre s'applique, utilisez des règles distinctes pour chaque condition. Par exemple, si vous souhaitez ajouter la même clause d'exclusion de responsabilité aux messages comportant des pièces jointes et aux messages contenant un texte spécifique, créez une règle pour chaque condition. Vous pouvez facilement copier une règle dans le CAE.  <br/> |
|Un message doit remplir toutes les conditions de la règle. Si vous souhaitez qu’une condition ou une autre s’applique, utilisez des règles distinctes pour chaque condition. Par exemple, si vous souhaitez ajouter la même clause d’exclusion de responsabilité aux messages comportant des pièces jointes et aux messages dont le contenu correspond à un modèle, créez une règle pour chaque condition. Vous pouvez facilement copier une règle.  <br/> |OR  <br/> |Certaines conditions vous permettent de spécifier plusieurs valeurs. Le message doit correspondre à l'une des valeurs spécifiées (pas toutes). Par exemple, si l'objet d'un message électronique est Informations sur le cours des actions et que la condition **L'objet inclut l'un de ces mots** est configurée pour établir une correspondance avec le mot Contoso ou actions, la condition est remplie, car l'objet du message contient au moins l'une des valeurs spécifiées.  <br/> |
|Certaines conditions vous permettent de spécifier plusieurs valeurs. Si plusieurs valeurs peuvent être spécifiées pour une condition, le message doit correspondre à l’une des valeurs spécifiées pour cette condition. Par exemple, si l’objet d’un message électronique est Informations sur le cours des actions et que la condition L’objet inclut l’un de ces mots est configurée pour établir une correspondance avec le mot Contoso ou actions, la condition est remplie, car l’objet du message contient au moins l’une des valeurs de condition.  <br/> |OR  <br/> |Si un message établit une correspondance avec l'une des exceptions, les actions ne sont pas appliquées. Le message ne doit pas forcément correspondre à toutes les exceptions.  <br/> |
|Si un message établit une correspondance avec l’une des exceptions, les actions ne sont pas traitées. Le message ne doit pas forcément correspondre à toutes les exceptions.  <br/> |AND  <br/> |Les messages qui répondent aux conditions d'une règle permettent d'obtenir toutes les actions qui sont spécifiées dans la règle. Par exemple, si les actions **Ajouter à l'objet du message le préfixe** et **Ajouter des destinataires au champ Cci** sont sélectionnées, les deux actions sont appliquées au message.  <br/> Si un message remplit les conditions d’une règle, toutes les actions spécifiées dans la règle en question lui sont appliquées. Par exemple, si les actions Ajouter à l’objet du message le préfixe et Ajouter des destinataires au champ Cci sont sélectionnées, les deux actions sont appliquées au message. La chaîne spécifiée sera ajoutée en préfixe de l’objet du message et les destinataires indiqués seront ajoutés en tant que destinataires Cci.<br/> Vous pouvez également définir une action sur une règle de sorte que lorsque cette règle est appliquée, les règles suivantes ne sont pas appliquées au message.  <br/> |
   
### <a name="mail-flow-rule-properties"></a>Propriétés de règle de flux de messagerie
<a name="Properties"> </a>

Le tableau suivant décrit les propriétés de règle qui sont disponibles dans les règles de flux de messagerie.
  
|**Nom de la propriété dans le CAE**|**Nom du paramètre dans PowerShell**|**Description**|
|:-----|:-----|:-----|
|**Priorité** <br/> | _Priority_ <br/> |Indique l'ordre dans lequel les règles sont appliquées aux messages. La priorité par défaut est définie en fonction de la date de création de la règle (les règles plus anciennes ont une priorité plus élevée que les règles plus récentes et les règles haute priorité sont traitées avant les règles basse priorité).    <br/> Vous modifiez la priorité de la règle dans le CAE en la déplaçant vers le haut ou le bas de la liste des règles. Dans l'PowerShell, vous définissez le numéro de priorité (0 représente la priorité la plus élevée).    <br/> Par exemple, si vous disposez d'une règle qui rejette les messages dans lesquels figure un numéro de carte de crédit et d'une autre règle qui exige une approbation, vous voudrez certainement que la règle de rejet soit appliquée en premier et que les autres règles ne s'appliquent pas.  |
|**Mode** <br/> | _Mode_ <br/> |Vous pouvez spécifier si vous souhaitez que la règle commence immédiatement le traitement des messages ou si vous souhaitez tester les règles sans affecter la remise du message (avec ou sans prévention contre la perte de données ou conseils de stratégie DLP).  <br/> Les conseils de stratégie affichent une courte note dans Outlook ou Outlook sur le web afin d'avertir une personne créant un message de possibles violations de stratégie. Pour plus d'informations, consultez la rubrique **Conseils de stratégie**.  <br/> Pour plus d’informations sur les modes, voir **Test a mail flow rule**.  <br/> |
|**Activer cette règle à la date suivante** <br/> **Désactiver cette règle à la date suivante** <br/> | _ActivationDate_ <br/>  _ExpiryDate_ <br/> |Spécifie la plage de dates au cours de laquelle la règle est active.  <br/> |
|Case à cocher **Activé** sélectionnée ou non  <br/> |Nouvelles règles : paramètre  _Enabled_ avec la cmdlet **New-TransportRule**.  <br/> Règles existantes : Utilisez les cmdlets **Enable-TransportRule** ou **Disable-TransportRule**.  <br/> La valeur est affichée dans la propriété **State** de la règle.  <br/> |Vous pouvez créer une règle désactivée, puis l'activer lorsque vous êtes prêt à la tester. Vous pouvez également désactiver une règle sans la supprimer pour en conserver les paramètres.  <br/> |
|**Différer le message si le traitement de la règle ne se termine pas** <br/> | _RuleErrorAction_ <br/> |Vous pouvez spécifier la manière dont le message doit être pris en charge si le traitement des règles ne se termine pas. Par défaut, la règle est ignorée, mais vous pouvez choisir de renvoyer ce message en vue de son traitement.  <br/> |
|**Faire correspondre l'adresse de l'expéditeur dans le message** <br/> | _SenderAddressLocation_ <br/> |Si la règle utilise des conditions ou des exceptions qui examinent l'adresse de messagerie de l'expéditeur, vous pouvez rechercher la valeur dans l'en-tête du message, dans l'enveloppe du message ou dans les deux.  <br/> |
|**Ne plus traiter de règles** <br/> | _SenderAddressLocation_ <br/> |Il s'agit d'une action de la règle, mais celle-ci ressemble à une propriété dans le CAE. Vous pouvez décider d'arrêter d'appliquer des règles à un message après qu'il a été traité par une règle.  <br/> |
|**Commentaires** <br/> | _Comments_ <br/> |Vous pouvez entrer des commentaires descriptifs sur la règle.  <br/> |
   
## <a name="how-mail-flow-rules-are-applied-to-messages"></a>Application des règles de flux de messagerie au courrier électronique

Tous les messages qui transitent par votre organisation sont évalués par rapport aux règles de flux de messagerie activées de celle-ci. Les règles sont traitées dans l'ordre indiqué sur la page **Flux de messagerie** \> **Règles** du Centre d'administration Exchange ou selon la valeur du paramètre  _Priority_ correspondant dans l'PowerShell. 
  
Chaque règle offre également la possibilité d'arrêter le traitement des autres règles lorsqu'elle détecte une correspondance. Ce paramètre est important pour les messages qui répondent aux conditions de plusieurs règles de flux de messagerie (quelle règle souhaitez-vous appliquer au message ? Toutes ? Une seule ?).
  
### <a name="differences-in-processing-based-on-message-type"></a>Différences de traitement selon le type de message

Plusieurs types de messages transitent par une organisation. Le tableau suivant montre ceux qui peuvent être traités par les règles de flux de messagerie.
  
****

|**Type de message**|**Une règle peut-elle être appliquée ?**|
|:-----|:-----|
|**Messages ordinaires** Il s'agit soit de messages contenant un corps de message au format RTF, HTML ou texte brut, soit de messages en plusieurs parties ou composés d'autres ensembles de corps de message.  <br/> |Oui  <br/> |
|**Chiffrement de messages Office 365 ** Messages chiffrés par Chiffrement de messages Office 365 dans Office 365. Pour plus d'informations, consultez la rubrique [Chiffrement dans Office 365](https://go.microsoft.com/fwlink/p/?LinkId=392525).  <br/> |Les règles peuvent toujours accéder aux en-têtes des enveloppes contenus dans des messages protégés et traiter les messages en se basant sur les conditions qui analysent les en-têtes.  <br/> Pour qu'une règle examine ou modifie le contenu d'un message chiffré, vous devez vérifier que le déchiffrement du transport est activé (Obligatoire ou Facultatif ; la valeur par défaut est Facultatif). Pour plus d'informations, consultez la rubrique relative à l'[activation ou la désactivation du déchiffrement du transport](https://go.microsoft.com/fwlink/p/?linkid=848060).  <br/> Vous pouvez également créer une règle qui déchiffre automatiquement les messages chiffrés. Pour en savoir plus, consultez la rubrique [Définir des règles pour chiffrer ou déchiffrer des messages électroniques](https://go.microsoft.com/fwlink/p/?Linkid=402846).  <br/> |
|**Messages chiffrés S/MIME** <br/> |Les règles peuvent uniquement accéder aux en-têtes d'enveloppe et traiter les messages en fonction de conditions qui inspectent ces en-têtes.  <br/> Les règles avec conditions qui requièrent l'inspection du contenu des messages ou les actions qui modifient le contenu des messages ne peuvent pas être traitées.  <br/> |
|**Messages protégés par RMS** Messages auxquels était appliquée une stratégie Services AD RMS (Active Directory Rights Management Services) (AD RMS) ou Azure Rights Management (RMS).  <br/> |Les règles peuvent toujours accéder aux en-têtes des enveloppes contenus dans des messages protégés et traiter les messages en se basant sur les conditions qui analysent les en-têtes.  <br/> Pour qu'une règle examine ou modifie le contenu d'un message protégé par RMS, vous devez vérifier que le déchiffrement du transport est activé (Obligatoire ou Facultatif ; la valeur par défaut est Facultatif). Pour plus d'informations, consultez la rubrique relative à l'[activation ou la désactivation du déchiffrement du transport](https://go.microsoft.com/fwlink/p/?linkid=848060).  <br/> |
|**Messages signés en clair** Messages signés, mais non chiffrés.  <br/> |Oui  <br/> |
|**Messages de messagerie unifiée** Il s'agit de messages créés ou traités par le service de messagerie unifiée, tels que les messages vocaux, les télécopies, les notifications d'appels manqués et les messages créés ou transférés à l'aide de Microsoft Outlook Voice Access.  <br/> |Oui  <br/> |
|**Messages anonymes** Messages envoyés par des expéditeurs anonymes.  <br/> |Oui  <br/> |
|**Rapports de lecture** Il s'agit des rapports générés en réponse aux demandes de confirmation de lecture des expéditeurs. Les rapports de lecture sont associés à une classe de message  `IPM.Note*.MdnRead` ou  `IPM.Note*.MdnNotRead`.  <br/> |Oui  <br/> |
   
## <a name="what-else-should-i-know"></a>Que dois-je savoir d’autre ?

- La valeur de la propriété **version** ou **RuleVersion** d’une règle n’est pas importante dans Exchange Online Protection. 
    
- Une fois que vous avez créé ou modifié une règle de flux de messagerie, l’application de la nouvelle règle ou de la règle mise à jour au courrier électronique peut prendre jusqu’à 30 minutes.
    
## <a name="for-more-information"></a>Pour plus d'informations
  
[Utiliser des règles de flux de messagerie pour inspecter les pièces jointes des messages dans Exchange Online](http://technet.microsoft.com/library/874d1c78-a8ec-4938-b388-d3208c2fa971.aspx)
  
[Chiffrement du courrier électronique dans Office 365](https://support.office.com/article/c0d87cbe-6d65-4c03-88ad-5216ea5564e8)
  
[Limites concernant les règles de journal, de transport et de boîte de réception](https://go.microsoft.com/fwlink/p/?LinkId=324584)
