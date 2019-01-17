---
title: Suivi des messages dans le centre de conformité de & sécurité
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: Administrateurs peuvent utiliser le suivi des messages dans le centre de conformité de & sécurité permettant de savoir qu’est-il advenu de messages.
ms.openlocfilehash: 9dfdab4adc5caba55664e93b49c8428791670ab3
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685431"
---
# <a name="message-trace-in-the-security--compliance-center"></a>Suivi des messages dans le centre de conformité de & sécurité

Suivi des messages dans le centre de conformité de & sécurité suit les messages électroniques pendant leur acheminement via votre organisation Exchange Online. Vous pouvez déterminer si un message a été reçu, rejeté, différé ou remis par le service. Il indique également les actions exécutées sur le message avant qu’elle atteint son état final.

Suivi des messages dans le centre de conformité de & sécurité améliore de suivi des messages qui était disponible dans le centre d’administration Exchange (CAE). Vous pouvez utiliser les informations de suivi des messages pour répondre aux questions d’utilisateur sur qu’est-il advenu de leurs messages efficacement, résoudre les problèmes de flux de messagerie et valider des modifications de la stratégie.

## <a name="open-message-trace"></a>Suivi des messages ouverts

1. [Connectez-vous à Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) à l'aide de votre compte professionnel ou scolaire.

2. Sélectionnez l'icône du lanceur d'applications ![Icône du lanceur d'applications Office 365](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) dans la partie supérieure gauche, puis **Administrateur**.

3. Dans le volet de navigation inférieur gauche, développez le **Centre d’administration** et sélectionnez **sécurité & conformité**.

4. Dans la page **sécurité & conformité** qui s’ouvre, développez des **flux de messagerie**et sélectionnez le **suivi des messages**.

## <a name="message-trace-page"></a>Page de suivi de message

À partir de là, vous pouvez démarrer une nouvelle trace par défaut en cliquant sur le bouton **Démarrer un suivi** . Il recherche tous les messages pour tous les expéditeurs et destinataires pour les deux derniers jours. Ou vous pouvez utiliser une des requêtes stockées dans les catégories de requête disponibles et soit les exécuter en tant que-est ou de les utiliser comme point de départ pour vos propres requêtes :

- **Par défaut des requêtes**: requêtes intégrés fournis par Office 365.

- **Requêtes personnalisé**: requêtes enregistrées par les administrateurs de votre organisation pour une utilisation future.

- **Requêtes enregistrée automatiquement**: les derniers dix récemment exécuter des requêtes. Cette liste facilite la décrochez où vous en étiez resté.

Également sur cette page est une section **Downloadable rapports** pour les requêtes que vous avez envoyée, ainsi que les rapports eux-mêmes lorsqu’il sont disponibles en téléchargement.

## <a name="options-for-a-new-message-trace"></a>Options de suivi d’un nouveau message

### <a name="filter-by-senders-and-recipients"></a>Filtrer par des expéditeurs et destinataires

Les valeurs par défaut sont **tous les expéditeurs** et **tous les destinataires**, mais vous pouvez utiliser les champs suivants pour filtrer les résultats :

- **Par ces personnes**: cliquez sur ce champ pour sélectionner un ou plusieurs des expéditeurs de votre organisation. Vous pouvez également démarrer à taper un nom et les éléments dans la liste seront filtrés par que vous avez tapé, beaucoup comme le comporte d’une page de recherche.

- **Pour ces personnes**: cliquez sur ce champ pour sélectionner un ou plusieurs destinataires de votre organisation.

Vous pouvez également taper les adresses de messagerie de destinataires et les expéditeurs externes. Des caractères génériques sont pris en charge (`*@contoso.com` ou `scot?@contoso.com`), mais vous ne pouvez pas utiliser plusieurs entrées de caractères génériques dans le même champ en même temps.

### <a name="time-range"></a>Plage de temps

La valeur par défaut est **2 jours**, mais vous pouvez spécifier des plages de date/heure de 90 jours. Lorsque vous utilisez des plages de date/heure, prenez en compte ces problèmes :

- Par défaut, vous sélectionnez la plage de temps dans l’affichage du **curseur** à l’aide d’une ligne du temps. Vous pouvez uniquement sélectionner le jour ou les paramètres qui sont affichés. Essayez de sélectionner une valeur intermédiaires s’alignent la bulle de début/fin pour le plus proche affiche le paramètre.

   ![Une période de curseur dans un nouveau suivi des messages dans le centre de conformité de & sécurité](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   Toutefois, vous pouvez également passer à la vue **personnalisée** dans laquelle vous pouvez spécifier les valeurs de **date de début** et **date de fin** (y compris les heures), et vous pouvez également sélectionner le **fuseau horaire** pour la plage de date/heure. Notez que le paramètre de **fuseau horaire** s’applique à la fois vos entrées de requête et les résultats de la requête.

   ![Une plage de temps personnalisé dans un nouveau suivi des messages dans le centre de conformité de & sécurité](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   Pour 10 jours ou moins, les résultats sont disponibles immédiatement en tant qu’un rapport de **synthèse** . Si vous spécifiez une plage de temps est légèrement supérieure à 10 jours, le résultat sera retardé comme ils ne sont disponibles dans un fichier CSV téléchargeable (rapports de **Synthèse améliorée** ou **étendue** ).

   Pour plus d’informations sur les différents types de rapport, voir la section [type de rapport choisir](#choose-report-type) dans cette rubrique.

   **Remarque**: rapports de synthèse et étendues améliorées sont établis à l’aide de données de suivi des messages archivés, et elle peut prendre quelques heures avant que votre état est disponible en téléchargement. Selon le nombre d’autres administrateurs ont soumis également les demandes de rapports en même temps, vous pouvez également remarquer un délai avant le début du traitement de votre demande en file d’attente.

- Enregistrement d’une requête en mode de **curseur** enregistre la période relative (par exemple, 3 jours). Enregistrement d’une requête dans la vue **personnalisée** enregistre la plage de date/heure absolue (par exemple, 2018-05-06 13:00 et 05-2018-08 18:00).

### <a name="more-search-options"></a>Plus d’options de recherche

#### <a name="delivery-status"></a>État de remise

Vous pouvez laisser la valeur par défaut **toutes les** sélectionnée, ou vous pouvez sélectionner une des valeurs suivantes pour filtrer les résultats :

- **Remis**: le message a bien été remis à la destination prévue.

- **En attente**: la remise du message est en cours de tentative de.

- **Expanded**: un destinataire de groupe de distribution a été développé avant remise aux membres du groupe.

- **Échec**: le message n’a pas été remis.

- **Mis en quarantaine**: le message a été mis en quarantaine (en tant que courrier indésirable, courrier en nombre ou hameçonnage). Pour plus d’informations, voir les [messages électroniques de mise en quarantaine dans Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).

- **Filtré comme courrier indésirable**: le message a été identifié du courrier indésirable et a été rejeté ou bloqué (non mis en quarantaine).

- **Obtention de l’état :** Le message a été reçu récemment par Office 365, mais aucune autre donnée d’état n’est encore disponible. Vérifiez de retour dans quelques minutes.

**Remarque**: les valeurs **en attente,** **mis en quarantaine**et **filtre de courrier indésirable** sont disponibles uniquement pour les recherches de moins de 10 jours. En outre, il peut y avoir un délai de 5 à 10 minutes entre l’état de remise réels et signalés.

#### <a name="message-id"></a>Message ID

Il s’agit de l’ID de message internet (également appelé ID de Client) qui se trouve dans le **Message-ID :** champ d’en-tête dans l’en-tête du message. Les utilisateurs peuvent vous fournir cette valeur pour rechercher des messages spécifiques.

Cette valeur est constante pour la durée de vie du message. Pour les messages créés dans Office 365 ou Exchange, la valeur est au format `<GUID@ServerFQDN>`, y compris les crochets pointus (\< \>). Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Autres systèmes de messagerie peuvent utiliser une syntaxe différente ou valeurs. Cette valeur est censée pour être uniques, mais pas tous les systèmes de messagerie électronique suivent strictement cette exigence. Si le **Message-ID :** champ d’en-tête n’existe pas ou est vide pour les messages entrants provenant de sources externes, une valeur arbitraire est affectée.

Lorsque vous utilisez un **ID de Message** pour filtrer les résultats, veillez à inclure la chaîne complète, y compris les crochets pointus.

#### <a name="direction"></a>Direction (Sens)

Vous pouvez laisser la valeur par défaut **toutes les** sélectionnée, ou vous pouvez sélectionner **entrants** (les messages envoyés aux destinataires de votre organisation) ou **sortant** (les messages envoyés par les utilisateurs dans votre organisation) pour filtrer les résultats.

#### <a name="original-client-ip-address"></a>Adresse IP du client d’origine

Vous pouvez fichiers les résultats à l’adresse IP du client pour examiner les ordinateurs piratés envoyant des grandes quantités de courrier indésirable ou un programme malveillant. Bien que les messages provenant de plusieurs expéditeurs peuvent sembler, il est probable que le même ordinateur génère tous les messages.

**Remarque**: les informations d’adresse IP client est disponibles uniquement pour 10 jours et est disponibles uniquement dans les rapports de **Synthèse améliorée** ou **étendu** (fichiers CSV téléchargeables).

### <a name="choose-report-type"></a>Choisissez le type de rapport

Les types de rapports disponibles sont les suivants :

- **Résumé**: disponible si la plage de temps est inférieure à 10 jours et ne requiert aucune option de filtrage supplémentaires. Les résultats sont disponibles presque immédiatement après que vous cliquez sur **Rechercher**.

- **Synthèse améliorée** ou **étendue**: ces rapports sont uniquement disponibles en tant que fichiers CSV téléchargeables et nécessitent une ou plusieurs des options de filtrage suivants quelle que soit la plage de temps : **ces personnes**, **ces personnes**ou ** ID de message**. Vous pouvez utiliser des caractères génériques pour les expéditeurs ou des destinataires (par exemple, \*@contoso.com).

**Remarques** :

- Rapports de synthèse et étendues améliorées sont établis à l’aide de données de suivi des messages archivés, et elle peut prendre quelques heures avant que votre état est disponible en téléchargement. Selon le nombre d’autres administrateurs ont soumis également les demandes de rapports en même temps, vous pouvez également remarquer un délai avant le début de votre demande en file d’attente de traitement.

- Alors que vous pouvez sélectionner un rapport de synthèse ou étendues améliorée pour une plage de date/heure, couramment quatre dernières heures des données archivées ne le pourront pas encore disponible pour ces deux types de rapports.

Lorsque vous cliquez sur **suivant**, que vous voyez une page de synthèse qui répertorie les options de filtrage que vous avez sélectionné, un titre unique (modifiable) pour le rapport et l’adresse de messagerie qui reçoit la notification lorsque le suivi des messages est terminée (également modifiable, et doit être l’un des domaines acceptés de votre organisation). Cliquez sur l' **état de préparation** pour soumettre le suivi des messages. Sur la principale page du **suivi des messages** , vous pouvez voir le statut de l’état dans la section **rapports téléchargeable** .

Pour plus d’informations sur les informations qui sont retournées dans les différents types de rapport, voir la section suivante.

## <a name="message-trace-results"></a>Résultats de suivi des messages

Les types de rapports différents renvoyer différents niveaux d’informations. Les informations qui sont disponibles dans les différents rapports sont décrit dans les sections suivantes.

### <a name="summary-report-output"></a>Sortie du rapport de synthèse

Après avoir exécuté le suivi des messages, les résultats sont répertoriés, triées par ordre décroissant de date/heure (plus récente).

![Résultats du rapport de synthèse pour le suivi des messages dans le centre de conformité de & sécurité](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

Le rapport de synthèse contient les informations suivantes :

- **Date**: date et heure auxquelles le message a été reçu par le service en utilisant le temps universel coordonné.

- **Expéditeur**: l’adresse de messagerie de l’expéditeur (*alias*@*domaine*).

- **Destinataire**: l’adresse de messagerie du destinataire ou des destinataires. Pour un message envoyé à plusieurs destinataires, il existe une ligne par destinataire. Si le destinataire est un groupe de distribution, un groupe de distribution dynamique ou un groupe de sécurité à extension messagerie, le groupe sera le premier destinataire, puis chaque membre du groupe est sur une ligne distincte.

- **Objet**: les 256 premiers caractères du message **Subject :** champ.

- **État**: ces valeurs sont décrites dans la section [état de remise](#delivery-status) .

Par défaut, les 250 premiers résultats sont chargés et disponibles. Lorsque vous faites défiler vers le bas, a une pause léger le lot suivant de résultats sont chargés. Au lieu de défilement, vous pouvez cliquer sur **charger toutes** pour charger tous les résultats avec un maximum de 10 000.

Vous pouvez cliquer sur les en-têtes de colonne pour trier les résultats par les valeurs de cette colonne dans l’ordre croissant ou décroissant.

Vous pouvez cliquer sur **les résultats de filtre** pour filtrer les résultats par une ou plusieurs colonnes.

Vous pouvez exporter les résultats une fois que vous avez sélectionné une ou plusieurs lignes en cliquant sur **Exporter les résultats** , puis cliquez sur **exporter tous les résultats**, **exportation chargé de résultats**ou **Exporter la sélection**.

#### <a name="find-related-records-for-this-message"></a>Rechercher des enregistrements connexes pour ce message

Enregistrements de messages associés sont les enregistrements partageant le même ID de Message. N’oubliez pas de même un message envoyé entre deux personnes peut générer plusieurs enregistrements. Le nombre d’enregistrements augmente lorsque le message est affecté par le développement de groupes de distribution, le transfert, règles de flux de messagerie (également connu sous les règles de transport), etc..

Une fois que vous sélectionnez la case à cocher d’une ligne, vous pouvez rechercher des enregistrements connexes pour le message en cliquant sur le bouton **Rechercher liées** qui s’affiche, ou en sélectionnant des **options plus** ![plus](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Rechercher les enregistrements associés à ce message**).

Pour plus d’informations sur l’ID de Message, consultez la section ID de Message plus haut dans cette rubrique.

#### <a name="message-trace-details"></a>Détails de suivi des messages

Dans la sortie du rapport de synthèse, vous pouvez afficher plus d’informations sur un message en utilisant l’une des méthodes suivantes :

- Sélectionnez la ligne (cliquez n’importe où dans la ligne à l’exception de la case à cocher).

- Activez la case à cocher de la ligne et cliquez sur **autres options** ![plus](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Détails du message**.

   ![Détails après en double-cliquant sur une ligne dans les résultats de suivi de message de rapport de synthèse dans le centre de conformité de & sécurité](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

Détails de suivi des messages contiennent les informations supplémentaires suivantes qui ne sont pas présentes dans le rapport de synthèse :

- **Événements de message**: cette section contient des classifications qui permettent de catégoriser les actions effectuées par le service sur les messages. Les événements plus intéressantes que vous pouvez rencontrer sont les suivants :

   - **Réception**: le message a été reçu par le service.

   - **Envoyer**: le message a été envoyé par le service.

   - **Échec**: le message d’échec de remise.

   - **Remettre**: le message a été remis à une boîte aux lettres.

   - **Développer**: le message a été envoyé à un groupe de distribution qui a été étendu.

   - **Transfert**: destinataires ont été déplacés vers un message BIFURQUÉ en raison de la conversion de contenu, les limites de destinataires de message ou d’agents.

   - **Defer**: la remise du message a été différée et peut être nouvelle tentative ultérieurement.

   - **Résolu**: le message a été redirigé vers une nouvelle adresse destinataire basée sur une recherche Active Directory. Dans ce cas, l’adresse du destinataire d’origine est répertorié dans une ligne distincte dans le suivi des messages ainsi que l’état de remise finale pour le message.

   Notez que même un message feront qui est envoyé avec succès génère plusieurs entrées **d’événements** dans le suivi des messages.

- **Plus d’informations**: cette section contient les informations suivantes :

   - **ID de message**: cette valeur est décrit dans la section [ID de Message](#message-id) plus haut dans cette rubrique. Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

   - **Taille des messages**

   - **Adresse IP**: adresse IP de l’ordinateur qui a envoyé le message. Pour les messages sortants envoyés à partir d’Exchange Online, cette valeur est vide.

   - **Pour IP**: adresse IP ou adresses où le service a tenté de remettre le message. Si le message comporte plusieurs destinataires, elles sont affichées. Pour les messages entrants envoyés vers Exchange Online, cette valeur est vide.

### <a name="enhanced-summary-reports"></a>Rapports de synthèse améliorées

(Terminé) améliorée rapports de synthèse disponibles sont disponibles dans la section **rapports téléchargeables** sur le suivi des messages début. Les informations suivantes sont disponibles dans le rapport :

- **origin_timestamp**<sup>*</sup>: la date et l’heure lorsque le message a été initialement reçu par le service en utilisant le temps universel coordonné.

- **sender_address**: adresse de messagerie de l’expéditeur (*alias*@*domaine*).

- **Recipient_status**: l’état de la remise du message au destinataire. Si le message a été envoyé à plusieurs destinataires, elle affiche tous les destinataires et l’état correspondant pour chacun, au format : \< *adresse de messagerie*\>##\<*état*\>. Par exemple :

   - **##Receive, envoyer** signifie que le message a été reçu par le service et a été envoyé à la destination prévue.

   - **##Receive, échec** signifie que le message a été reçu par le service mais la remise vers la destination a échoué.

   - **##Receive, remettre** signifie que le message a été reçu par le service et a été remis à la boîte aux lettres du destinataire.

- **message_subject**: les 256 premiers caractères du champ **d’objet** du message.

- **total_bytes**: la taille du message en octets, y compris les pièces jointes.

- **message_id**: cette valeur est décrit dans la section [ID de Message](#message-id) plus haut dans cette rubrique. Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

- **network_message_id**: une valeur d’ID de message unique sont conservées dans toutes les copies du message qui peut être créé en raison de l’expansion de groupe de distribution ou de bifurcation. Est un exemple de valeur `1341ac7b13fb42ab4d4408cf7f55890f`.

- **original_client_ip**: l’adresse IP du client de l’expéditeur.

- **orientation**: indique si le message a été envoyé entrant (1) dans votre organisation, ou s’il a été envoyé sortant (2) à partir de votre organisation.

- **connector_id**: le nom du connecteur source ou de destination. Pour plus d’informations sur les connecteurs dans Exchange Online, voir [configurer le flux de messagerie à l’aide de connecteurs dans Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).

- **delivery_priority**<sup>*</sup>: si le message a été envoyé avec une priorité **haute**, **faible**ou **Normal** .

<sup>*</sup>Ces propriétés sont uniquement disponibles dans les rapports de synthèse améliorée.

### <a name="extended-reports"></a>Rapports étendus

Rapports d’étendue (terminés) disponibles sont disponibles dans la section **rapports Downloadable** au début du suivi des messages. Presque toutes les informations à partir d’un rapport de synthèse améliorée est disponible dans un rapport de l’étendue (à l’exception de **origin_timestamp** et **delivery_priority**). Les informations supplémentaires suivantes sont uniquement disponibles dans un rapport de l’étendue :

- **client_ip**: l’adresse IP du serveur de messagerie ou du client de messagerie qui a envoyé le message.

- **client_hostname**: le nom d’hôte ou le nom de domaine complet du serveur de messagerie ou du client de messagerie qui a envoyé le message.

- **server_ip**: l’adresse IP du serveur source ou de destination.

- **server_hostname**: le nom d’hôte ou le nom de domaine complet du serveur de destination.

- **source_context**: associées au champ de la **source** des informations supplémentaires. Par exemple :

   - `Protocol Filter Agent`

   - `3489061114359050000`

- **source**: composant The Exchange Online qui est responsable de l’événement. Par exemple :

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- **ID_événement**: ils correspondent aux valeurs qui sont décrites dans la section [Rechercher les enregistrements associés à ce message](#find-related-records-for-this-message) **d’événement de Message** .

- **internal_message_id**: un identificateur de message qui est affecté par le serveur Exchange Online qui traite le message actuellement.

- **recipient_address**: les adresses de messagerie des destinataires du message. Plusieurs adresses de messagerie sont séparés par un point-virgule ( ;).

- **recipient_count**: le nombre total de destinataires du message.

- **related_recipient_address**: utilisé avec `EXPAND`, `REDIRECT`, et `RESOLVE` événements pour afficher les autres destinataires de messagerie adresses qui sont associées au message.

- **référence**: ce champ contient des informations supplémentaires pour des types spécifiques d’événements. Par exemple :

   - **DSN**: contient le lien de rapport, qui est la valeur de **message_id** de la notification d’état de remise associée (également appelé un DSN, rapport de non-remise, un rapport de non-remise ou message de retour) si une source de données est généré à la suite de cet événement. S’il s’agit d’un message DSN, ce champ contient la valeur de **message_id** du message d’origine qui a été généré pour la source de données.

   - **Développer**: contient la valeur **related_recipient_address** des messages associés.

   - **Réception**: peut contenir la valeur de **message_id** du message connexe si le message a été généré par d’autres processus (par exemple, les règles de boîte de réception).

   - **Envoyer**: contient la valeur **internal_message_id** de tous les messages DSN.

   - **Transfert**: contient la valeur **internal_message_id** du message est en cours dirigé (par exemple, en la conversion de contenu, les limites de destinataires de message ou d’agents).

   - **MAILBOXRULE**: contient la valeur **internal_message_id** du message entrant qui a provoqué la règle de boîte de réception générer le message sortant.

   Pour tous les autres types d’événements, ce champ est généralement vide.

- **return_path**: l’adresse e-mail spécifiée par la commande **MAIL FROM** qui a envoyé le message. Bien que ce champ n’est jamais vide, il peut avoir la valeur d’adresse expéditeur null représentée sous forme de `<>`.

- **message_info**: plus d’informations sur le message. Par exemple :

   - La message origine date-heure au format UTC pour `DELIVER` et `SEND` événements. L’heure-date d’origine est lorsque le message d’entrée tout d’abord l’organisation Exchange Online. L’heure UTC est représentée dans le format de date et d’heure ISO8601 : `yyyy-mm-ddThh:mm:ss.fffZ`, où `yyyy` = année, `mm` = mois, `dd` = jour, `T` indique le début du composant heure, `hh` = heure, `mm` = minute, `ss` = deuxième, `fff` = fractions de seconde, et `Z` signifie `Zulu`, qui est une autre façon d’indiquer au format UTC.

   - Erreurs d’authentification. Par exemple, vous pouvez voir la valeur `11a` et le type d’authentification utilisé lors de l’erreur d’authentification.

- **tenant_id**: une valeur GUID qui représente l’organisation Exchange Online (par exemple, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).

- **original_server_ip**: l’adresse IP du serveur d’origine.

- **custom_data**: contient les données associées à des types d’événement spécifique. Pour plus d’informations, voir les sections suivantes.

#### <a name="customdata-values"></a>valeurs custom_data

Le champ **custom_data** pour un `AGENTINFO` événement est utilisé par un grand nombre d’agents Exchange Online pour journaliser les détails du traitement du message. Parmi les plus intéressantes agents sont décrites dans les sections suivantes.

#### <a name="spam-filter-agent"></a>Agent de filtrage du courrier indésirable

Une valeur **custom_data** qui commence par `S:SFA` est à partir de l’agent de filtrage du courrier indésirable. Les détails sont décrits dans le tableau suivant :

|**Valeur**|**Description**|
|:-----|:-----|
|`SFV=NSPM`|Le message a été marqué comme n'étant pas un courrier indésirable et a été envoyé aux destinataires appropriés.|
|`SFV=SPM`|Le message a été marqué comme courrier indésirable par le filtre de contenu.|
|`SFV=BLK`|Le filtrage a été ignoré et le message a été bloqué, car il provient d'un expéditeur bloqué.|
|`SFV=SKS`|Le message a été marqué comme courrier indésirable avant d'être traité par le filtre de contenu. Cela inclut les messages pour lesquels une règle de transport les a marqués automatiquement comme étant des courriers indésirables et où toutes les étapes de filtrage supplémentaires ont été contournées.|
|`SCL=<number>`|Pour plus d'informations sur les différentes valeurs de SCL et leur signification, voir [Seuils de probabilité de courrier indésirable](https://technet.microsoft.com/library/jj200686.aspx).|
|`PCL=<number>`|Valeur du seuil de probabilité de courrier d'hameçonnage (PCL) du message. Ces valeurs peuvent être interprétées de la même façon que les valeurs SCL répertoriées dans [Seuils de probabilité de courrier indésirable](https://technet.microsoft.com/library/jj200686.aspx).  |
|`DI=SB`|L'expéditeur du message a été bloqué.|
|`DI=SQ`|Le message a été mis en quarantaine.|
|`DI=SD`|Le message a été supprimé.|
|`DI=SJ`|Le message a été mis dans le dossier Courrier indésirable du destinataire.|
|`DI=SN`|Le message a été routé via le pool de remise à risque plus élevé. Pour plus d’informations, voir [pool de remise à haut risque pour les messages sortants](https://technet.microsoft.com/library/jj200746.aspx).|
|`DI=SO`|Le message a été routé via le pool de remises normal pour les messages sortants.|
|' SFS = [a]|SFS = [b]'|Cela indique que des règles anti-spam ont été associées.|
|`IPV=CAL`|Le message n'a pas été bloqué par les filtres anti-spam car l'adresse IP se trouve dans une liste d'adresses IP autorisées du filtre des connexions.|
|`H=<EHLOstring>`|La chaîne HELO ou EHLO du serveur de messagerie qui se connecte.|
|`PTR=<ReverseDNS>`|Enregistrement PTR de l'adresse IP d'envoi, également appelé adresse DNS inverse.|

Un exemple de valeur **custom_data** pour un message est filtré comme courrier indésirable similaire à celle-ci :

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a>Agent de filtrage des programmes malveillants

Une valeur **custom_data** qui commence par `S:AMA` est à partir de l’agent de filtrage des programmes malveillants. Les détails sont décrits dans le tableau suivant :

|**Valeur**|**Description**|
|:-----|:-----|
|' AMA = SOMME|v=1|` or `AMA=EV|v = 1'|Le message a été déterminé contenant des programmes malveillants. `SUM` indique le programme malveillant avoir été détecté par n’importe quel nombre de moteurs. `EV` indique le programme malveillant détecté par un moteur spécifique. Lorsque programme malveillant est détecté par un moteur que cela déclenche les actions suivantes.|
|`Action=r`|Le message a été remplacé.|
|`Action=p`|Le message a été ignoré.|
|`Action=d`|Le message a été différé.|
|`Action=s`|Le message a été supprimé.|
|`Action=st`|Le message a été ignoré.|
|`Action=sy`|Le message a été ignoré.|
|`Action=ni`|Le message a été rejeté.|
|`Action=ne`|Le message a été rejeté.|
|`Action=b`|Le message a été bloqué.|
|`Name=<malware>`|Nom du programme malveillant détecté.|
|`File=<filename>`|Nom du fichier qui contenait le programme malveillant.|

Un exemple de valeur **custom_data** pour un message contenant des programmes malveillants ressemble à ceci :

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a>Agent de règle de transport

Une valeur **custom_data** qui commence par`S:TRA` est à partir de l’agent de règle de transport pour les règles de flux de messagerie (également connu sous les règles de transport). Les détails sont décrits dans le tableau suivant :

|**Valeur**|**Description**|
|:-----|:-----|
|' ETR|ruleId =<guid>`|ID de la règle qui s'applique.|
|`St=<datetime>`|La date et l’heure UTC lorsque la correspondance de règle.|
|`Action=<ActionDefinition>`|L’action qui a été appliquée. Pour obtenir la liste des actions disponibles, voir [flux de messagerie des actions de règle dans Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).|
|`Mode=<Mode>`|Le mode de la règle. Les valeurs valides sont :<br/>• **Appliquer**: toutes les actions de la règle seront appliquées. <br/>• **Test avec conseils de stratégie :**: tous les conseils de stratégie seront envoyés, mais les autres actions d’application ne seront pas effectuées. <br/>• **Test sans conseils de stratégie**: Actions seront consignées dans un fichier journal, mais les expéditeurs ne seront pas informés de toute façon et actions d’application ne seront pas effectuées.|

Une valeur **custom_data** d’exemple pour un message qui correspond aux conditions d’une règle de flux de messagerie ressemble à ceci :

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`
