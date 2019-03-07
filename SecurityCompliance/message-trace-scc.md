---
title: Suivi des messages dans le centre de sécurité & conformité
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: Les administrateurs peuvent utiliser le suivi des messages dans le centre de sécurité & Compliance Center pour déterminer ce qui s'est passé aux messages.
ms.openlocfilehash: 9c427328972fb9c8d64a2847368f5be022974744
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455346"
---
# <a name="message-trace-in-the-security--compliance-center"></a>Suivi des messages dans le centre de sécurité & conformité

Le suivi des messages dans le centre de sécurité & conformité suit les messages électroniques échangés via votre organisation Exchange Online. Vous pouvez déterminer si un message a été reçu, rejeté, différé ou remis par le service. Cela indique également les actions entamées par rapport au message avant qu'il atteigne son statut final.

Le suivi des messages dans le centre de sécurité & conformité améliore le suivi des messages qui était disponible dans le centre d'administration Exchange. Vous pouvez utiliser les informations du suivi des messages pour répondre efficacement aux questions des utilisateurs sur ce qui s'est passé à leurs messages, résoudre les problèmes de flux de messagerie et valider les modifications de stratégie.

## <a name="open-message-trace"></a>Ouvrir le suivi des messages

1. [Connectez-vous à Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) à l'aide de votre compte professionnel ou scolaire.

2. Sélectionnez l'icône du lanceur d'applications ![Icône du lanceur d'applications Office 365](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) dans la partie supérieure gauche, puis **Administrateur**.

3. Dans le volet de navigation en bas à gauche, développez **centres d'administration** et sélectionnez **sécurité & conformité**.

4. Dans la page conformité du service de **sécurité &** qui s'ouvre, développez **flux de messagerie**, puis sélectionnez **suivi des messages**.

## <a name="message-trace-page"></a>Page de suivi des messages

À partir de là, vous pouvez démarrer un nouveau suivi par défaut en cliquant sur le bouton **Démarrer un suivi** . Cette opération recherche tous les messages pour tous les expéditeurs et destinataires au cours des deux derniers jours. Vous pouvez aussi utiliser l'une des requêtes stockées des catégories de requête disponibles et les exécuter telles quelles ou les utiliser comme points de départ pour vos propres requêtes:

- **Requêtes par défaut**: requêtes intégrées fournies par Office 365.

- **Requêtes personnalisées**: requêtes enregistrées par les administrateurs de votre organisation en vue d'une utilisation ultérieure.

- **Requêtes enregistrées automatiquement**: les dix dernières requêtes exécutées. Cette liste facilite la récupération là où vous vous étiez arrêté.

Cette page contient également une section **rapports** téléchargeable pour les demandes que vous avez envoyées, ainsi que les rapports eux-mêmes lorsqu'ils sont disponibles pour le téléchargement.

## <a name="options-for-a-new-message-trace"></a>Options pour un nouveau suivi des messages

### <a name="filter-by-senders-and-recipients"></a>Filtrer par expéditeurs et destinataires

Les valeurs par défaut sont **tous les expéditeurs** et **tous les destinataires**, mais vous pouvez utiliser les champs suivants pour filtrer les résultats:

- **Par ces personnes**: cliquez dans ce champ pour sélectionner un ou plusieurs expéditeurs de votre organisation. Vous pouvez également commencer à taper un nom et les éléments de la liste seront filtrés en fonction de ce que vous avez tapé, de la même manière qu'une page de recherche.

- **Pour les personnes**suivantes: cliquez dans ce champ pour sélectionner un ou plusieurs destinataires dans votre organisation.

Vous pouvez également taper les adresses de messagerie des expéditeurs et des destinataires externes. Les caractères génériques sont pris`*@contoso.com` en `scot?@contoso.com`charge (ou), mais vous ne pouvez pas utiliser plusieurs entrées génériques dans le même champ simultanément.

### <a name="time-range"></a>Plage horaire

La valeur par défaut est **2 jours**, mais vous pouvez spécifier des plages de date/heure allant jusqu'à 90 jours. Lorsque vous utilisez des plages date/heure, tenez compte des points suivants:

- Par défaut, vous sélectionnez la plage de temps dans le mode **curseur** à l'aide d'une ligne de temps. Vous pouvez uniquement sélectionner les paramètres de jour ou d'heure affichés. La tentative de sélection d'une valeur entre-entre va aligner la bulle de début/fin au paramètre affiché le plus proche.

   ![Un intervalle de temps de curseur dans un nouveau suivi des messages dans le centre de sécurité & Compliance Center](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   Toutefois, vous pouvez également passer en mode affichage **personnalisé** où vous pouvez spécifier les valeurs de date de **début** et de **Date de fin** (y compris les heures), et vous pouvez également sélectionner le **fuseau horaire** pour la plage date/heure. Notez que le paramètre **fuseau horaire** s'applique à la fois à vos entrées de requête et à vos résultats de requête.

   ![Une plage de temps personnalisée dans un nouveau suivi des messages dans le centre de sécurité & Compliance Center](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   Pendant 10 jours ou moins, les résultats sont disponibles instantanément sous la forme d'un rapport de **synthèse** . Si vous spécifiez un intervalle de temps qui est encore légèrement supérieur à 10 jours, les résultats seront retardés, car ils ne seront disponibles que sous forme de fichier CSV **** téléchargeable ( **Résumé amélioré** ou rapports étendus).

   Pour plus d'informations sur les différents types de rapport, reportez-vous à la section [choisir un type de rapport](#choose-report-type) dans cette rubrique.

   **Remarque**: le résumé amélioré et les rapports étendus sont préparés à l'aide des données de suivi des messages archivés, et peuvent prendre jusqu'à plusieurs heures avant que le rapport ne soit disponible pour téléchargement. En fonction du nombre d'autres administrateurs ayant également envoyé des demandes de rapports en même temps, vous pouvez également remarquer un délai avant le début du traitement de votre demande en file d'attente.

- L'enregistrement d'une requête en mode **curseur** enregistre la plage de temps relative (par exemple, 3 jours à partir d'aujourd'hui). L'enregistrement d'une requête en mode **personnalisé** enregistre la plage date/heure absolue (par exemple, 2018-05-06 13:00 à 2018-05-08 18:00).

### <a name="more-search-options"></a>Autres options de recherche

#### <a name="delivery-status"></a>État de remise

Vous pouvez laisser la valeur par défaut **tous** sélectionnée ou vous pouvez sélectionner l'une des valeurs suivantes pour filtrer les résultats:

- **Remis**: le message a bien été remis à la destination prévue.

- **En attente**: la remise du message est tentée ou retentée.

- **Étendu**: un destinataire de groupe de distribution a été étendu avant la remise aux membres individuels du groupe.

- **Échec**: le message n'a pas été remis.

- **Mis en quarantaine**: le message a été mis en quarantaine (en tant que courrier indésirable, courrier en nombre ou hameçonnage). Pour plus d'informations, consultez la rubrique [mise en quarantaine des messages électroniques dans Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).

- **Filtré en tant que courrier**indésirable: le message a été identifié comme courrier indésirable, et a été rejeté ou bloqué (non mis en quarantaine).

- **Obtention de l'État:** Le message a été récemment reçu par Office 365, mais aucune autre donnée d'État n'est encore disponible. Vérifiez de nouveau dans quelques minutes.

**Remarque**: les valeurs **en attente,** **mises en quarantaine**et **filtrées en tant que courrier** indésirable sont uniquement disponibles pour les recherches de moins de 10 jours. De plus, il peut y avoir un délai de 5 à 10 minutes entre l'état de remise réel et signalé.

#### <a name="message-id"></a>ID du message

Il s'agit de l'ID de message Internet (également appelé ID de client) qui se trouve dans le champ d'en-tête **message-ID:** dans l'en-tête du message. Les utilisateurs peuvent vous donner cette valeur pour examiner des messages spécifiques.

Cette valeur est constante pendant toute la durée de vie du message. Pour les messages créés dans Office 365 ou Exchange, la valeur est au format `<GUID@ServerFQDN>`, y compris les chevrons\< \>(). Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. D'autres systèmes de messagerie peuvent utiliser des valeurs ou une syntaxe différentes. Cette valeur est supposée unique, mais tous les systèmes de courrier ne respectent pas strictement cette exigence. Si le champ d'en-tête **message-ID:** n'existe pas ou est vide pour les messages entrants provenant de sources externes, une valeur arbitraire est assignée.

Lorsque vous utilisez l' **ID de message** pour filtrer les résultats, veillez à inclure la chaîne complète, y compris tous les chevrons.

#### <a name="direction"></a>Direction (Sens)

Vous pouvez laisser la valeur par défaut **tous** sélectionnée ou vous pouvez sélectionner **** les messages entrants (messages envoyés à des destinataires dans votre organisation) ou **sortants** (messages envoyés par les utilisateurs de votre organisation) pour filtrer les résultats.

#### <a name="original-client-ip-address"></a>Adresse IP du client d’origine

Vous pouvez échanger les résultats par adresse IP du client pour enquêter sur les ordinateurs piratés qui envoient de grandes quantités de courrier indésirable ou de programmes malveillants. Bien que les messages semblent provenir de plusieurs expéditeurs, il est probable que le même ordinateur génère tous les messages.

**Remarque**: les informations d'adresse IP du client sont disponibles uniquement pendant 10 jours et sont disponibles uniquement dans le **Résumé amélioré** ou les rapports **étendus** (fichiers CSV téléchargeables).

### <a name="choose-report-type"></a>Choisir le type de rapport

Les types de rapports disponibles sont les suivants:

- **Résumé**: disponible si l'intervalle de temps est inférieur à 10 jours et ne requiert aucune option de filtrage supplémentaire. Les résultats sont disponibles presque immédiatement après que vous avez cliqué sur **Rechercher**.

- **Résumé amélioré** ou **étendu**: ces rapports sont disponibles uniquement en tant que fichiers CSV téléchargeables et nécessitent une ou plusieurs des options de filtrage suivantes, quelle que soit la plage horaire: **par ces personnes**, **à ces personnes**, ou ** ID du message**. Vous pouvez utiliser des caractères génériques pour les expéditeurs ou les destinataires (par \*exemple, @contoso. com).

**Remarques** :

- Le résumé amélioré et les rapports étendus sont préparés à l'aide de données de suivi des messages archivés, et peuvent prendre jusqu'à plusieurs heures avant le téléchargement de votre rapport. En fonction du nombre d'autres administrateurs ayant également envoyé des demandes de rapports en même temps, vous pouvez également remarquer un délai avant le début du traitement de votre demande en file d'attente.

- Bien que vous puissiez sélectionner un rapport avancé ou étendu pour n'importe quelle plage date/heure, les quatre dernières heures de données archivées ne sont pas encore disponibles pour ces deux types de rapports.

Lorsque vous cliquez sur **suivant**, une page de résumé répertorie les options de filtrage que vous avez sélectionnées, un titre unique (modifiable) pour le rapport et l'adresse de messagerie qui reçoit la notification lorsque le suivi des messages est terminé (également modifiable, et doit se trouver dans l'un des domaines acceptés de votre organisation). Cliquez sur **préparer le rapport** pour envoyer le suivi des messages. Sur la page principale de **suivi des messages** , vous pouvez voir l'état du rapport dans la section **rapports** téléchargeables.

Pour plus d'informations sur les informations renvoyées dans les différents types de rapports, voir la section suivante.

## <a name="message-trace-results"></a>Résultats du suivi des messages

Les différents types de rapport renvoient différents niveaux d'informations. Les informations disponibles dans les différents rapports sont décrites dans les sections suivantes.

### <a name="summary-report-output"></a>Sortie du rapport de synthèse

Après avoir exécuté le suivi des messages, les résultats sont affichés, triés par ordre décroissant de date/heure (en premier lieu).

![Résultats du rapport de synthèse pour le suivi des messages dans le centre de sécurité & Compliance Center](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

Le rapport de synthèse contient les informations suivantes:

- **Date**: date et heure auxquelles le message a été reçu par le service, à l'aide du fuseau horaire UTC configuré.

- **Sender**: adresse de messagerie de l'expéditeur (*alias*@*Domain*).

- **Recipient**: adresse de messagerie du ou des destinataires. Pour un message envoyé à plusieurs destinataires, il y a une ligne par destinataire. Si le destinataire est un groupe de distribution, un groupe de distribution dynamique ou un groupe de sécurité à extension messagerie, le groupe sera le premier destinataire, puis chaque membre du groupe se trouve sur une ligne distincte.

- **Objet**: les premiers 256 caractères du champ objet du message **:**

- **État**: ces valeurs sont décrites dans la section [État de remise](#delivery-status) .

Par défaut, le premier résultat 250 est chargé et immédiatement disponible. Lorsque vous faites défiler vers le bas, il y a une légère pause lorsque le lot de résultats suivant est chargé. Au lieu de faire défiler, vous pouvez cliquer sur **charger tout** pour charger tous les résultats jusqu'à un maximum de 10 000.

Vous pouvez cliquer sur les en-têtes de colonne pour trier les résultats en fonction des valeurs de cette colonne dans l'ordre croissant ou décroissant.

Vous pouvez cliquer sur **Filtrer les résultats** pour filtrer les résultats par une ou plusieurs colonnes.

Vous pouvez exporter les résultats une fois que vous avez sélectionné une ou plusieurs lignes en cliquant sur **Exporter les résultats** , puis en sélectionnant **exporter tous les résultats**, **Exporter les résultats chargés**ou **Exporter la sélection**.

#### <a name="find-related-records-for-this-message"></a>Rechercher des enregistrements associés pour ce message

Les enregistrements de message associés sont des enregistrements qui ont partagé le même ID de message. N'oubliez pas qu'un seul message envoyé entre deux personnes peut générer plusieurs enregistrements. Le nombre d'enregistrements augmente lorsque le message est affecté par l'expansion du groupe de distribution, le transfert, les règles de flux de messagerie (également appelées règles de transport), etc.

Une fois que vous avez activé la case à cocher d'une ligne, vous pouvez trouver des enregistrements correspondants pour le message en cliquant sur le bouton **Rechercher connexe** qui s'affiche, ou en sélectionnant **plus d'options** ![](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **pour ce message**.

Pour plus d'informations sur l'ID de message, consultez la section ID de message plus haut dans cette rubrique.

#### <a name="message-trace-details"></a>Détails du suivi des messages

Dans le rapport de synthèse, vous pouvez afficher les détails relatifs à un message à l'aide de l'une des méthodes suivantes:

- Sélectionnez la ligne (cliquez n'importe où dans la ligne à l'exception de la case à cocher).

- Activez la case à cocher ligne, puis cliquez sur **autres options** ![plus](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **afficher les détails du message**.

   ![Détails après un double-clic sur une ligne dans le rapport de synthèse résultats du suivi des messages dans le centre de sécurité & Compliance Center](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

Les détails de suivi des messages contiennent les informations supplémentaires suivantes qui ne sont pas présentes dans le rapport récapitulatif:

- **Événements de message**: cette section contient des classifications qui permettent de classer les actions effectuées par le service sur les messages. Voici quelques-uns des événements les plus intéressants que vous pouvez rencontrer:

   - **Receive**: le message a été reçu par le service.

   - **Send**: le message a été envoyé par le service.

   - **Échec**: le message n'a pas pu être remis.

   - **Remettre**: le message a été remis à une boîte aux lettres.

   - **Expand**: le message a été envoyé à un groupe de distribution qui a été étendu.

   - **Transfert**: les destinataires ont été déplacés vers un message de bifurcation en raison de la conversion de contenu, de limites de destinataires de messages ou d'agents.

   - **Defer**: la remise du message a été différée et peut être retentée ultérieurement.

   - **Résolu**: le message a été redirigé vers une nouvelle adresse de destinataire en fonction d'une recherche Active Directory. Lorsque cela se produit, l'adresse du destinataire d'origine est répertoriée sur une ligne distincte dans le suivi des messages avec l'état de remise final du message.

   Notez que même un message qui n'a pas été correctement remis génère plusieurs entrées d' **événements** dans le suivi des messages.

- **Informations supplémentaires**: cette section contient les informations suivantes:

   - **ID du message**: cette valeur est décrite dans la section [ID du message](#message-id) , plus haut dans cette rubrique. Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

   - **Taille du message**

   - **IP from**: adresse IP de l'ordinateur qui a envoyé le message. Pour les messages sortants envoyés à partir d'Exchange Online, ce champ est vide.

   - **Vers IP**: adresse ou adresses IP où le service a tenté de livrer le message. Si le message contient plusieurs destinataires, ceux-ci sont affichés. Pour les messages entrants envoyés à Exchange Online, ce champ est vide.

### <a name="enhanced-summary-reports"></a>Rapports de synthèse améliorés

Les rapports de synthèse (terminé) disponibles sont disponibles dans la section **rapports** téléchargeables au début du suivi des messages. Les informations suivantes sont disponibles dans le rapport:

- **origin_timestamp**<sup>*</sup>: date et heure de réception initiale du message par le service, à l'aide du fuseau horaire UTC configuré.

- **sender_address**: adresse de messagerie de l'expéditeur (*alias*@de*domaine*).

- **Recipient_status**: état de la remise du message au destinataire. Si le message a été envoyé à plusieurs destinataires, il affiche tous les destinataires et l'état correspondant pour chacun, au format \<:*État*\>de l' *adresse*\>##\<de messagerie. Par exemple :

   - **# #Receive, envoyer** signifie que le message a été reçu par le service et qu'il a été envoyé à la destination prévue.

   - **# #Receive, Fail** signifie que le message a été reçu par le service, mais que la remise à la destination prévue a échoué.

   - **# #Receive, Deliver** signifie que le message a été reçu par le service et qu'il a été remis à la boîte aux lettres du destinataire.

- **message_subject**: les premiers 256 caractères du champ **Subject** du message.

- **total_bytes**: taille du message en octets, pièces jointes comprises.

- **message_id**: cette valeur est décrite dans la section [ID du message](#message-id) plus haut dans cette rubrique. Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

- **network_message_id**: valeur unique d'ID de message qui persiste sur toutes les copies du message qui peuvent être créées suite à une bifurcation ou à une expansion du groupe de distribution. Par exemple, la `1341ac7b13fb42ab4d4408cf7f55890f`valeur est.

- **original_client_ip**: adresse IP du client de l'expéditeur.

- **directionnel**: indique si le message a été envoyé (1) à votre organisation ou s'il a été envoyé (2) à partir de votre organisation.

- **connector_id**: nom du connecteur source ou de destination. Pour plus d'informations sur les connecteurs dans Exchange Online, consultez la rubrique [configure mail Flow using Connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).

- **delivery_priority**<sup>*</sup>: indique si le message a été envoyé avec **une priorité élevée**, **faible**ou **normale** .

<sup>*</sup>Ces propriétés sont disponibles uniquement dans les rapports de synthèse étendus.

### <a name="extended-reports"></a>Rapports étendus

Les rapports étendus disponibles (terminés) sont disponibles dans la section **rapports** téléchargeables au début du suivi des messages. Presque toutes les informations d'un rapport de synthèse amélioré sont disponibles dans un rapport étendu (à l'exception de **origin_timestamp** et **delivery_priority**). Les informations supplémentaires suivantes sont disponibles uniquement dans un rapport étendu:

- **client_IP**: adresse IP du serveur de messagerie ou du client de messagerie ayant envoyé le message.

- **client_hostname**: le nom d'hôte ou le nom de domaine complet (FQDN) du serveur de messagerie ou du client de messagerie qui a envoyé le message.

- **server_ip**: adresse IP du serveur source ou de destination.

- **server_hostname**: le nom d'hôte ou le nom de domaine complet du serveur de destination.

- **source_context**: informations supplémentaires associées au champ **source** . Par exemple :

   - `Protocol Filter Agent`

   - `3489061114359050000`

- **source**: composant Exchange Online responsable de l'événement. Par exemple :

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- **event_id**: ils correspondent aux valeurs d' **événement de message** qui sont expliquées dans la section [Rechercher des enregistrements liés pour ce message](#find-related-records-for-this-message) .

- **internal_message_id**: identificateur de message qui est affecté par le serveur Exchange Online qui traite actuellement le message.

- **recipient_address**: adresses de messagerie des destinataires du message. Les adresses de messagerie multiples sont séparées par des points-virgules (;).

- **recipient_count**: nombre total de destinataires dans le message.

- **related_recipient_address**: utilisé avec `EXPAND`, `REDIRECT`et `RESOLVE` les événements pour afficher d'autres adresses de messagerie de destinataires associées au message.

- **référence**: ce champ contient des informations supplémentaires pour des types d'événements spécifiques. Par exemple :

   - **DSN**: contient le lien de rapport, qui est la valeur **message_id** de la notification d'état de remise associée (également appelée DSN, notification d'échec de remise, notification d'échec de remise ou message de retour) si un DSN est généré suite à cet événement. S'il s'agit d'un message DSN, ce champ contient la valeur **message_id** du message d'origine pour lequel le DSN a été généré.

   - **Expand**: contient la valeur **related_recipient_address** des messages connexes.

   - **Receive**: peut contenir la valeur **message_id** du message connexe si le message a été généré par d'autres processus (par exemple, les règles de boîte de réception).

   - **Send**: contient la valeur **internal_message_id** de tous les messages DSN.

   - **Transfer**: contient la valeur **internal_message_id** du message en cours de bifurcation (par exemple, par conversion de contenu, limites de destinataires de message ou agents).

   - **MAILBOXRULE**: contient la valeur **internal_message_id** du message entrant qui a provoqué la génération du message sortant par la règle de boîte de réception.

   Pour les autres types d'événements, ce champ est généralement vide.

- **return_path**: adresse de messagerie de retour spécifiée par la commande **Mail from** qui a envoyé le message. Bien que ce champ ne soit jamais vide, il peut avoir la valeur de l'adresse de `<>`l'expéditeur null représentée par.

- **message_info**: informations supplémentaires sur le message. Par exemple :

   - Date et heure d'origine du message au format UTC `DELIVER` pour `SEND` les événements et. La date d'origine date-heure est l'heure à laquelle le message est entré pour la première fois dans l'organisation Exchange Online. L'heure UTC est représentée au format de date-heure ISO 8601: `yyyy-mm-ddThh:mm:ss.fffZ`, où `yyyy` = année, `mm` = mois, `dd` = jour, `T` indique le début du composant d'heure, `hh` = heure, `mm` = minute, `ss` = seconde, = `fff` les fractions de seconde, et `Z` signifient `Zulu`, qui est une autre façon de désigner UTC.

   - Erreurs d'authentification. Par exemple, vous pouvez voir la valeur `11a` et le type d'authentification utilisé lorsque l'erreur d'authentification s'est produite.

- **tenant_id**: valeur GUID qui représente l'organisation Exchange Online (par exemple, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).

- **original_server_ip**: adresse IP du serveur d'origine.

- **custom_data**: contient des données liées à des types d'événements spécifiques. Pour plus d'informations, consultez les sections suivantes.

#### <a name="customdata-values"></a>valeurs custom_data

Le champ **custom_data** d'un `AGENTINFO` événement est utilisé par divers agents Exchange Online pour enregistrer les détails de traitement des messages. Certains des agents les plus intéressants sont décrits dans les sections suivantes.

#### <a name="spam-filter-agent"></a>Agent de filtrage du courrier inDésirable

Une valeur **custom_data** qui commence par `S:SFA` est l'agent de filtrage du courrier indésirable. Les détails clés sont décrits dans le tableau suivant:

|**Valeur**|**Description**|
|:-----|:-----|
|`SFV=NSPM`|Le message a été marqué comme n'étant pas un courrier indésirable et a été envoyé aux destinataires appropriés.|
|`SFV=SPM`|Le message a été marqué comme courrier indésirable par le filtre de contenu.|
|`SFV=BLK`|Le filtrage a été ignoré et le message a été bloqué, car il provient d'un expéditeur bloqué.|
|`SFV=SKS`|Le message a été marqué comme courrier indésirable avant d'être traité par le filtre de contenu. Il s'agit des messages marqués automatiquement comme courrier indésirable par une règle de transport et qui n'ont donc pas fait l'objet d'un filtrage supplémentaire.|
|`SCL=<number>`|Pour plus d'informations sur les différentes valeurs de SCL et leur signification, voir [Seuils de probabilité de courrier indésirable](https://technet.microsoft.com/library/jj200686.aspx).|
|`PCL=<number>`|Valeur du seuil de probabilité de courrier d'hameçonnage (PCL) du message. Ces valeurs peuvent être interprétées de la même façon que les valeurs SCL répertoriées dans [Seuils de probabilité de courrier indésirable](https://technet.microsoft.com/library/jj200686.aspx).  |
|`DI=SB`|L'expéditeur du message a été bloqué.|
|`DI=SQ`|Le message a été mis en quarantaine.|
|`DI=SD`|Le message a été supprimé.|
|`DI=SJ`|Le message a été mis dans le dossier Courrier indésirable du destinataire.|
|`DI=SN`|Le message a été routé via le pool de remises à haut risque. Pour plus d'informations, consultez la rubrique [pool de remise à haut risque pour les messages sortants](https://technet.microsoft.com/library/jj200746.aspx).|
|`DI=SO`|Le message a été routé via le pool de remises normal pour les messages sortants.|
|«SFS = [a]|SFS = [b] '|Cela indique que des règles anti-spam ont été associées.|
|`IPV=CAL`|Le message n'a pas été bloqué par les filtres anti-spam car l'adresse IP se trouve dans une liste d'adresses IP autorisées du filtrage des connexions.|
|`H=<EHLOstring>`|La chaîne HELO ou EHLO du serveur de messagerie de connexion.|
|`PTR=<ReverseDNS>`|Enregistrement PTR de l'adresse IP d'envoi, également appelé adresse DNS inverse.|

Exemple de valeur **custom_data** pour un message qui est filtré pour le courrier indésirable comme suit:

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a>Agent de filtrage des programmes malveillants

Une valeur **custom_data** qui commence par `S:AMA` provient de l'agent de filtrage des programmes malveillants. Les détails clés sont décrits dans le tableau suivant:

|**Valeur**|**Description**|
|:-----|:-----|
|'AMA = SUM|v=1|` or `AMA=EV|v = 1 '|Un programme malveillant a été détecté dans le message. `SUM`indique que le programme malveillant a pu être détecté par n'importe quel nombre de moteurs. `EV`indique que le programme malveillant a été détecté par un moteur spécifique. Lorsqu'un programme malveillant est détecté par un moteur, les actions suivantes se produisent.|
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

Voici un exemple de valeur **custom_data** pour un message qui contient un programme malveillant:

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a>Agent de règle de transport

Une valeur **custom_data** qui commence par`S:TRA` provient de l'agent de règles de transport pour les règles de flux de messagerie (également appelées règles de transport). Les détails clés sont décrits dans le tableau suivant:

|**Valeur**|**Description**|
|:-----|:-----|
|'ETR|ruleId =<guid>`|ID de la règle qui s'applique.|
|`St=<datetime>`|Date et heure UTC de la correspondance de la règle.|
|`Action=<ActionDefinition>`|Action appliquée. Pour obtenir la liste des actions disponibles, consultez la rubrique [mail Flow Rule actions in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).|
|`Mode=<Mode>`|Mode de la règle. UserMailbox <br/>• **Appliquer**: toutes les actions de la règle seront appliquées. <br/>• **Test avec conseils de stratégie:**: toutes les actions de Conseil de stratégie seront envoyées, mais les autres actions d'application ne seront pas traitées. <br/>• **Test sans conseils de stratégie**: les actions seront consignées dans un fichier journal, mais les expéditeurs ne recevront aucune notification et les actions d'application ne seront pas effectuées.|

Voici un exemple de valeur **custom_data** pour les messages qui correspondent aux conditions d'une règle de flux de messagerie comme suit:

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`
