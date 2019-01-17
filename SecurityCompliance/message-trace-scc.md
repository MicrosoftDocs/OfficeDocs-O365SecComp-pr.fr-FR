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
# <a name="message-trace-in-the-security--compliance-center"></a><span data-ttu-id="3b982-103">Suivi des messages dans le centre de conformité de & sécurité</span><span class="sxs-lookup"><span data-stu-id="3b982-103">Message trace in the Security & Compliance Center</span></span>

<span data-ttu-id="3b982-p101">Suivi des messages dans le centre de conformité de & sécurité suit les messages électroniques pendant leur acheminement via votre organisation Exchange Online. Vous pouvez déterminer si un message a été reçu, rejeté, différé ou remis par le service. Il indique également les actions exécutées sur le message avant qu’elle atteint son état final.</span><span class="sxs-lookup"><span data-stu-id="3b982-p101">Message trace in the Security & Compliance Center follows email messages as they travel through your Exchange Online organization. You can determine if a message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>

<span data-ttu-id="3b982-p102">Suivi des messages dans le centre de conformité de & sécurité améliore de suivi des messages qui était disponible dans le centre d’administration Exchange (CAE). Vous pouvez utiliser les informations de suivi des messages pour répondre aux questions d’utilisateur sur qu’est-il advenu de leurs messages efficacement, résoudre les problèmes de flux de messagerie et valider des modifications de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="3b982-p102">Message trace in the Security & Compliance Center improves upon message trace that was available in the Exchange admin center (EAC). You can use the information from message trace to efficiently answer user questions about what happened to their messages, troubleshoot mail flow issues, and validate policy changes.</span></span>

## <a name="open-message-trace"></a><span data-ttu-id="3b982-109">Suivi des messages ouverts</span><span class="sxs-lookup"><span data-stu-id="3b982-109">Open message trace</span></span>

1. <span data-ttu-id="3b982-110">[Connectez-vous à Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) à l'aide de votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="3b982-110">[Sign in to Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span>

2. <span data-ttu-id="3b982-111">Sélectionnez l'icône du lanceur d'applications ![Icône du lanceur d'applications Office 365](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) dans la partie supérieure gauche, puis **Administrateur**.</span><span class="sxs-lookup"><span data-stu-id="3b982-111">Select the app launcher icon ![Office 365 app launcher icon](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in the upper-left and choose **Admin**.</span></span>

3. <span data-ttu-id="3b982-112">Dans le volet de navigation inférieur gauche, développez le **Centre d’administration** et sélectionnez **sécurité & conformité**.</span><span class="sxs-lookup"><span data-stu-id="3b982-112">In the lower-left navigation, expand **Admin centers** and select **Security & Compliance**.</span></span>

4. <span data-ttu-id="3b982-113">Dans la page **sécurité & conformité** qui s’ouvre, développez des **flux de messagerie**et sélectionnez le **suivi des messages**.</span><span class="sxs-lookup"><span data-stu-id="3b982-113">In the **Security & Compliance** page that opens, expand **Mail flow**, and select **Message trace**.</span></span>

## <a name="message-trace-page"></a><span data-ttu-id="3b982-114">Page de suivi de message</span><span class="sxs-lookup"><span data-stu-id="3b982-114">Message trace page</span></span>

<span data-ttu-id="3b982-p103">À partir de là, vous pouvez démarrer une nouvelle trace par défaut en cliquant sur le bouton **Démarrer un suivi** . Il recherche tous les messages pour tous les expéditeurs et destinataires pour les deux derniers jours. Ou vous pouvez utiliser une des requêtes stockées dans les catégories de requête disponibles et soit les exécuter en tant que-est ou de les utiliser comme point de départ pour vos propres requêtes :</span><span class="sxs-lookup"><span data-stu-id="3b982-p103">From here you can start a new default trace by clicking on the **Start a trace** button. This will search for all messages for all senders and recipients for the last two days. Or you can use one of the stored queries from the available query categories and either run them as-is or use them as starting points for your own queries:</span></span>

- <span data-ttu-id="3b982-118">**Par défaut des requêtes**: requêtes intégrés fournis par Office 365.</span><span class="sxs-lookup"><span data-stu-id="3b982-118">**Default queries**: Built-in queries provided by Office 365.</span></span>

- <span data-ttu-id="3b982-119">**Requêtes personnalisé**: requêtes enregistrées par les administrateurs de votre organisation pour une utilisation future.</span><span class="sxs-lookup"><span data-stu-id="3b982-119">**Custom queries**: Queries saved by admins in your organization for future use.</span></span>

- <span data-ttu-id="3b982-p104">**Requêtes enregistrée automatiquement**: les derniers dix récemment exécuter des requêtes. Cette liste facilite la décrochez où vous en étiez resté.</span><span class="sxs-lookup"><span data-stu-id="3b982-p104">**Autosaved queries**: The last ten most recently run queries. This list makes it simple to pick up where you left off.</span></span>

<span data-ttu-id="3b982-122">Également sur cette page est une section **Downloadable rapports** pour les requêtes que vous avez envoyée, ainsi que les rapports eux-mêmes lorsqu’il sont disponibles en téléchargement.</span><span class="sxs-lookup"><span data-stu-id="3b982-122">Also on this page is a **Downloadable reports** section for the requests you've submitted, as well as the reports themselves when they're are available for download.</span></span>

## <a name="options-for-a-new-message-trace"></a><span data-ttu-id="3b982-123">Options de suivi d’un nouveau message</span><span class="sxs-lookup"><span data-stu-id="3b982-123">Options for a new message trace</span></span>

### <a name="filter-by-senders-and-recipients"></a><span data-ttu-id="3b982-124">Filtrer par des expéditeurs et destinataires</span><span class="sxs-lookup"><span data-stu-id="3b982-124">Filter by senders and recipients</span></span>

<span data-ttu-id="3b982-125">Les valeurs par défaut sont **tous les expéditeurs** et **tous les destinataires**, mais vous pouvez utiliser les champs suivants pour filtrer les résultats :</span><span class="sxs-lookup"><span data-stu-id="3b982-125">The default values are **All senders** and **All recipients**, but you can use the following fields to filter the results:</span></span>

- <span data-ttu-id="3b982-p105">**Par ces personnes**: cliquez sur ce champ pour sélectionner un ou plusieurs des expéditeurs de votre organisation. Vous pouvez également démarrer à taper un nom et les éléments dans la liste seront filtrés par que vous avez tapé, beaucoup comme le comporte d’une page de recherche.</span><span class="sxs-lookup"><span data-stu-id="3b982-p105">**By these people**: Click in this field to select one or more senders from your organization. You can also start to type a name and the items in the list will be filtered by what you've typed, much like how a search page behaves.</span></span>

- <span data-ttu-id="3b982-128">**Pour ces personnes**: cliquez sur ce champ pour sélectionner un ou plusieurs destinataires de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3b982-128">**To these people**: Click in this field to select one or more recipients in your organization.</span></span>

<span data-ttu-id="3b982-p106">Vous pouvez également taper les adresses de messagerie de destinataires et les expéditeurs externes. Des caractères génériques sont pris en charge (`*@contoso.com` ou `scot?@contoso.com`), mais vous ne pouvez pas utiliser plusieurs entrées de caractères génériques dans le même champ en même temps.</span><span class="sxs-lookup"><span data-stu-id="3b982-p106">You can also type the email addresses of external senders and recipients. Wildcards are supported (`*@contoso.com` or `scot?@contoso.com`), but you can't use multiple wildcard entries in the same field at the same time.</span></span>

### <a name="time-range"></a><span data-ttu-id="3b982-131">Plage de temps</span><span class="sxs-lookup"><span data-stu-id="3b982-131">Time range</span></span>

<span data-ttu-id="3b982-p107">La valeur par défaut est **2 jours**, mais vous pouvez spécifier des plages de date/heure de 90 jours. Lorsque vous utilisez des plages de date/heure, prenez en compte ces problèmes :</span><span class="sxs-lookup"><span data-stu-id="3b982-p107">The default value is **2 days**, but you can specify date/time ranges of up to 90 days. When you use date/time ranges, consider these issues:</span></span>

- <span data-ttu-id="3b982-p108">Par défaut, vous sélectionnez la plage de temps dans l’affichage du **curseur** à l’aide d’une ligne du temps. Vous pouvez uniquement sélectionner le jour ou les paramètres qui sont affichés. Essayez de sélectionner une valeur intermédiaires s’alignent la bulle de début/fin pour le plus proche affiche le paramètre.</span><span class="sxs-lookup"><span data-stu-id="3b982-p108">By default, you select the time range in **Slider** view using a time line. You can only select the day or time settings that are displayed. Trying to select an in-between value will snap the start/end bubble to the nearest displayed setting.</span></span>

   ![Une période de curseur dans un nouveau suivi des messages dans le centre de conformité de & sécurité](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   <span data-ttu-id="3b982-p109">Toutefois, vous pouvez également passer à la vue **personnalisée** dans laquelle vous pouvez spécifier les valeurs de **date de début** et **date de fin** (y compris les heures), et vous pouvez également sélectionner le **fuseau horaire** pour la plage de date/heure. Notez que le paramètre de **fuseau horaire** s’applique à la fois vos entrées de requête et les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="3b982-p109">But, you can also switch to **Custom** view where you can specify the **Start date** and **End date** values (including times), and you can also select the **Time zone** for the date/time range. Note that the **Time zone** setting applies to both your query inputs and your query results.</span></span>

   ![Une plage de temps personnalisé dans un nouveau suivi des messages dans le centre de conformité de & sécurité](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   <span data-ttu-id="3b982-p110">Pour 10 jours ou moins, les résultats sont disponibles immédiatement en tant qu’un rapport de **synthèse** . Si vous spécifiez une plage de temps est légèrement supérieure à 10 jours, le résultat sera retardé comme ils ne sont disponibles dans un fichier CSV téléchargeable (rapports de **Synthèse améliorée** ou **étendue** ).</span><span class="sxs-lookup"><span data-stu-id="3b982-p110">For 10 days or less, the results are available instantly as a **Summary** report. If you specify a time range that's even slightly greater than 10 days, the results will be delayed as they are only available as a downloadable CSV file ( **Enhanced summary** or **Extended** reports).</span></span>

   <span data-ttu-id="3b982-143">Pour plus d’informations sur les différents types de rapport, voir la section [type de rapport choisir](#choose-report-type) dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="3b982-143">For more information about the different report types, see the [Choose report type](#choose-report-type) section in this topic.</span></span>

   <span data-ttu-id="3b982-p111">**Remarque**: rapports de synthèse et étendues améliorées sont établis à l’aide de données de suivi des messages archivés, et elle peut prendre quelques heures avant que votre état est disponible en téléchargement. Selon le nombre d’autres administrateurs ont soumis également les demandes de rapports en même temps, vous pouvez également remarquer un délai avant le début du traitement de votre demande en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="3b982-p111">**Note**: Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available for download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before processing starts for your queued request.</span></span>

- <span data-ttu-id="3b982-p112">Enregistrement d’une requête en mode de **curseur** enregistre la période relative (par exemple, 3 jours). Enregistrement d’une requête dans la vue **personnalisée** enregistre la plage de date/heure absolue (par exemple, 2018-05-06 13:00 et 05-2018-08 18:00).</span><span class="sxs-lookup"><span data-stu-id="3b982-p112">Saving a query in **Slider** view saves the relative time range (for example, 3 days from today). Saving a query in **Custom** view saves the absolute date/time range (for example, 2018-05-06 13:00 to 2018-05-08 18:00).</span></span>

### <a name="more-search-options"></a><span data-ttu-id="3b982-148">Plus d’options de recherche</span><span class="sxs-lookup"><span data-stu-id="3b982-148">More search options</span></span>

#### <a name="delivery-status"></a><span data-ttu-id="3b982-149">État de remise</span><span class="sxs-lookup"><span data-stu-id="3b982-149">Delivery status</span></span>

<span data-ttu-id="3b982-150">Vous pouvez laisser la valeur par défaut **toutes les** sélectionnée, ou vous pouvez sélectionner une des valeurs suivantes pour filtrer les résultats :</span><span class="sxs-lookup"><span data-stu-id="3b982-150">You can leave the default value **All** selected, or you can select one of the following values to filter the results:</span></span>

- <span data-ttu-id="3b982-151">**Remis**: le message a bien été remis à la destination prévue.</span><span class="sxs-lookup"><span data-stu-id="3b982-151">**Delivered**: The message was successfully delivered to the intended destination.</span></span>

- <span data-ttu-id="3b982-152">**En attente**: la remise du message est en cours de tentative de.</span><span class="sxs-lookup"><span data-stu-id="3b982-152">**Pending**: Delivery of the message is being attempted or re-attempted.</span></span>

- <span data-ttu-id="3b982-153">**Expanded**: un destinataire de groupe de distribution a été développé avant remise aux membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="3b982-153">**Expanded**: A distribution group recipient was expanded before delivery to the individual members of the group.</span></span>

- <span data-ttu-id="3b982-154">**Échec**: le message n’a pas été remis.</span><span class="sxs-lookup"><span data-stu-id="3b982-154">**Failed**: The message was not delivered.</span></span>

- <span data-ttu-id="3b982-p113">**Mis en quarantaine**: le message a été mis en quarantaine (en tant que courrier indésirable, courrier en nombre ou hameçonnage). Pour plus d’informations, voir les [messages électroniques de mise en quarantaine dans Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b982-p113">**Quarantined**: The message was quarantined (as spam, bulk mail, or phishing). For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).</span></span>

- <span data-ttu-id="3b982-157">**Filtré comme courrier indésirable**: le message a été identifié du courrier indésirable et a été rejeté ou bloqué (non mis en quarantaine).</span><span class="sxs-lookup"><span data-stu-id="3b982-157">**Filtered as spam**: The message was identified spam, and was rejected or blocked (not quarantined).</span></span>

- <span data-ttu-id="3b982-p114">**Obtention de l’état :** Le message a été reçu récemment par Office 365, mais aucune autre donnée d’état n’est encore disponible. Vérifiez de retour dans quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="3b982-p114">**Getting status:** The message was recently received by Office 365, but no other status data is yet available. Check back in a few minutes.</span></span>

<span data-ttu-id="3b982-p115">**Remarque**: les valeurs **en attente,** **mis en quarantaine**et **filtre de courrier indésirable** sont disponibles uniquement pour les recherches de moins de 10 jours. En outre, il peut y avoir un délai de 5 à 10 minutes entre l’état de remise réels et signalés.</span><span class="sxs-lookup"><span data-stu-id="3b982-p115">**Note**: The values **Pending,** **Quarantined**, and **Filter as spam** are only available for searches less than 10 days. Also, there might be a 5 to 10 minute delay between the actual and reported delivery status.</span></span>

#### <a name="message-id"></a><span data-ttu-id="3b982-162">Message ID</span><span class="sxs-lookup"><span data-stu-id="3b982-162">Message ID</span></span>

<span data-ttu-id="3b982-p116">Il s’agit de l’ID de message internet (également appelé ID de Client) qui se trouve dans le **Message-ID :** champ d’en-tête dans l’en-tête du message. Les utilisateurs peuvent vous fournir cette valeur pour rechercher des messages spécifiques.</span><span class="sxs-lookup"><span data-stu-id="3b982-p116">This is the internet message ID (also known as the Client ID) that's found in the **Message-ID:** header field in the message header. Users can give you this value to investigate specific messages.</span></span>

<span data-ttu-id="3b982-p117">Cette valeur est constante pour la durée de vie du message. Pour les messages créés dans Office 365 ou Exchange, la valeur est au format `<GUID@ServerFQDN>`, y compris les crochets pointus (\< \>). Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Autres systèmes de messagerie peuvent utiliser une syntaxe différente ou valeurs. Cette valeur est censée pour être uniques, mais pas tous les systèmes de messagerie électronique suivent strictement cette exigence. Si le **Message-ID :** champ d’en-tête n’existe pas ou est vide pour les messages entrants provenant de sources externes, une valeur arbitraire est affectée.</span><span class="sxs-lookup"><span data-stu-id="3b982-p117">This value is constant for the lifetime of the message. For messages created in Office 365 or Exchange, the value is in the format `<GUID@ServerFQDN>`, including the angle brackets (\< \>). For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Other messaging systems might use different syntax or values. This value is supposed to be unique, but not all email systems strictly follow this requirement. If the **Message-ID:** header field doesn't exist or is blank for incoming messages from external sources, an arbitrary value is assigned.</span></span>

<span data-ttu-id="3b982-171">Lorsque vous utilisez un **ID de Message** pour filtrer les résultats, veillez à inclure la chaîne complète, y compris les crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="3b982-171">When you use **Message ID** to filter the results, be sure to include the full string, including any angle brackets.</span></span>

#### <a name="direction"></a><span data-ttu-id="3b982-172">Direction (Sens)</span><span class="sxs-lookup"><span data-stu-id="3b982-172">Direction</span></span>

<span data-ttu-id="3b982-173">Vous pouvez laisser la valeur par défaut **toutes les** sélectionnée, ou vous pouvez sélectionner **entrants** (les messages envoyés aux destinataires de votre organisation) ou **sortant** (les messages envoyés par les utilisateurs dans votre organisation) pour filtrer les résultats.</span><span class="sxs-lookup"><span data-stu-id="3b982-173">You can leave the default value **All** selected, or you can select **Inbound** (messages sent to recipients in your organization) or **Outbound** (messages sent from users in your organization) to filter the results.</span></span>

#### <a name="original-client-ip-address"></a><span data-ttu-id="3b982-174">Adresse IP du client d’origine</span><span class="sxs-lookup"><span data-stu-id="3b982-174">Original client IP address</span></span>

<span data-ttu-id="3b982-p118">Vous pouvez fichiers les résultats à l’adresse IP du client pour examiner les ordinateurs piratés envoyant des grandes quantités de courrier indésirable ou un programme malveillant. Bien que les messages provenant de plusieurs expéditeurs peuvent sembler, il est probable que le même ordinateur génère tous les messages.</span><span class="sxs-lookup"><span data-stu-id="3b982-p118">You can filer the results by client IP address to investigate hacked computers that are sending large amounts of spam or malware. Although the messages might appear to come from multiple senders, it's likely that the same computer is generating all of the messages.</span></span>

<span data-ttu-id="3b982-177">**Remarque**: les informations d’adresse IP client est disponibles uniquement pour 10 jours et est disponibles uniquement dans les rapports de **Synthèse améliorée** ou **étendu** (fichiers CSV téléchargeables).</span><span class="sxs-lookup"><span data-stu-id="3b982-177">**Note**: The client IP address information is only available for 10 days, and is only available in the **Enhanced summary** or **Extended** reports (downloadable CSV files).</span></span>

### <a name="choose-report-type"></a><span data-ttu-id="3b982-178">Choisissez le type de rapport</span><span class="sxs-lookup"><span data-stu-id="3b982-178">Choose report type</span></span>

<span data-ttu-id="3b982-179">Les types de rapports disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3b982-179">The available report types are:</span></span>

- <span data-ttu-id="3b982-p119">**Résumé**: disponible si la plage de temps est inférieure à 10 jours et ne requiert aucune option de filtrage supplémentaires. Les résultats sont disponibles presque immédiatement après que vous cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="3b982-p119">**Summary**: Available if the time range is less than 10 days, and requires no additional filtering options. The results are available almost immediately after you click **Search**.</span></span>

- <span data-ttu-id="3b982-p120">**Synthèse améliorée** ou **étendue**: ces rapports sont uniquement disponibles en tant que fichiers CSV téléchargeables et nécessitent une ou plusieurs des options de filtrage suivants quelle que soit la plage de temps : **ces personnes**, **ces personnes**ou \*\* ID de message\*\*. Vous pouvez utiliser des caractères génériques pour les expéditeurs ou des destinataires (par exemple, \*@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="3b982-p120">**Enhanced summary** or **Extended**: These reports are only available as downloadable CSV files, and require one or more of the following filtering options regardless of the time range: **By these people**, **To these people**, or **Message ID**. You can use wildcards for the senders or the recipients (for example, \*@contoso.com).</span></span>

<span data-ttu-id="3b982-184">**Remarques** :</span><span class="sxs-lookup"><span data-stu-id="3b982-184">**Notes**:</span></span>

- <span data-ttu-id="3b982-p121">Rapports de synthèse et étendues améliorées sont établis à l’aide de données de suivi des messages archivés, et elle peut prendre quelques heures avant que votre état est disponible en téléchargement. Selon le nombre d’autres administrateurs ont soumis également les demandes de rapports en même temps, vous pouvez également remarquer un délai avant le début de votre demande en file d’attente de traitement.</span><span class="sxs-lookup"><span data-stu-id="3b982-p121">Enhanced summary and Extended reports are prepared using archived message trace data, and it can take up to several hours before your report is available to download. Depending on how many other admins have also submitted report requests around the same time, you might also notice a delay before your queued request starts to be processed.</span></span>

- <span data-ttu-id="3b982-187">Alors que vous pouvez sélectionner un rapport de synthèse ou étendues améliorée pour une plage de date/heure, couramment quatre dernières heures des données archivées ne le pourront pas encore disponible pour ces deux types de rapports.</span><span class="sxs-lookup"><span data-stu-id="3b982-187">While you can select an Enhanced summary or Extended report for any date/time range, commonly the last four hours of archived data will not yet be available for these two types of reports.</span></span>

<span data-ttu-id="3b982-p122">Lorsque vous cliquez sur **suivant**, que vous voyez une page de synthèse qui répertorie les options de filtrage que vous avez sélectionné, un titre unique (modifiable) pour le rapport et l’adresse de messagerie qui reçoit la notification lorsque le suivi des messages est terminée (également modifiable, et doit être l’un des domaines acceptés de votre organisation). Cliquez sur l' **état de préparation** pour soumettre le suivi des messages. Sur la principale page du **suivi des messages** , vous pouvez voir le statut de l’état dans la section **rapports téléchargeable** .</span><span class="sxs-lookup"><span data-stu-id="3b982-p122">When you click **Next**, you're presented with a summary page that lists the filtering options that you selected, a unique (editable) title for the report, and the email address that receives the notification when the message trace completes (also editable, and must be in one of your organization's accepted domains). Click **Prepare report** to submit the message trace. On the main **Message trace** page, you can see the status of the report in the **Downloadable reports** section.</span></span>

<span data-ttu-id="3b982-191">Pour plus d’informations sur les informations qui sont retournées dans les différents types de rapport, voir la section suivante.</span><span class="sxs-lookup"><span data-stu-id="3b982-191">For more information about the information that's returned in the different report types, see the next section.</span></span>

## <a name="message-trace-results"></a><span data-ttu-id="3b982-192">Résultats de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="3b982-192">Message trace results</span></span>

<span data-ttu-id="3b982-p123">Les types de rapports différents renvoyer différents niveaux d’informations. Les informations qui sont disponibles dans les différents rapports sont décrit dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b982-p123">The different report types return different levels of information. The information that's available in the different reports is described in the following sections.</span></span>

### <a name="summary-report-output"></a><span data-ttu-id="3b982-195">Sortie du rapport de synthèse</span><span class="sxs-lookup"><span data-stu-id="3b982-195">Summary report output</span></span>

<span data-ttu-id="3b982-196">Après avoir exécuté le suivi des messages, les résultats sont répertoriés, triées par ordre décroissant de date/heure (plus récente).</span><span class="sxs-lookup"><span data-stu-id="3b982-196">After running the message trace, the results will be listed, sorted by descending date/time (most recent first).</span></span>

![Résultats du rapport de synthèse pour le suivi des messages dans le centre de conformité de & sécurité](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

<span data-ttu-id="3b982-198">Le rapport de synthèse contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3b982-198">The summary report contains the following information:</span></span>

- <span data-ttu-id="3b982-199">**Date**: date et heure auxquelles le message a été reçu par le service en utilisant le temps universel coordonné.</span><span class="sxs-lookup"><span data-stu-id="3b982-199">**Date**: The date and time at which the message was received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="3b982-200">**Expéditeur**: l’adresse de messagerie de l’expéditeur (*alias*@*domaine*).</span><span class="sxs-lookup"><span data-stu-id="3b982-200">**Sender**: The email address of the sender (*alias*@*domain*).</span></span>

- <span data-ttu-id="3b982-p124">**Destinataire**: l’adresse de messagerie du destinataire ou des destinataires. Pour un message envoyé à plusieurs destinataires, il existe une ligne par destinataire. Si le destinataire est un groupe de distribution, un groupe de distribution dynamique ou un groupe de sécurité à extension messagerie, le groupe sera le premier destinataire, puis chaque membre du groupe est sur une ligne distincte.</span><span class="sxs-lookup"><span data-stu-id="3b982-p124">**Recipient**: The email address of the recipient or recipients. For a message sent to multiple recipients, there's one line per recipient. If the recipient is a distribution group, dynamic distribution group, or mail-enabled security group, the group will be the first recipient, and then each member of the group is on a separate line.</span></span>

- <span data-ttu-id="3b982-204">**Objet**: les 256 premiers caractères du message **Subject :** champ.</span><span class="sxs-lookup"><span data-stu-id="3b982-204">**Subject**: The first 256 characters of the message's **Subject:** field.</span></span>

- <span data-ttu-id="3b982-205">**État**: ces valeurs sont décrites dans la section [état de remise](#delivery-status) .</span><span class="sxs-lookup"><span data-stu-id="3b982-205">**Status**: These values are described in the [Delivery status](#delivery-status) section.</span></span>

<span data-ttu-id="3b982-p125">Par défaut, les 250 premiers résultats sont chargés et disponibles. Lorsque vous faites défiler vers le bas, a une pause léger le lot suivant de résultats sont chargés. Au lieu de défilement, vous pouvez cliquer sur **charger toutes** pour charger tous les résultats avec un maximum de 10 000.</span><span class="sxs-lookup"><span data-stu-id="3b982-p125">By default, the first 250 results are loaded and readily available. When you scroll down, there's a slight pause as the next batch of results are loaded. Instead of scrolling, you can click **Load all** to load all of the results up to a maximum of 10,000.</span></span>

<span data-ttu-id="3b982-209">Vous pouvez cliquer sur les en-têtes de colonne pour trier les résultats par les valeurs de cette colonne dans l’ordre croissant ou décroissant.</span><span class="sxs-lookup"><span data-stu-id="3b982-209">You can click on the column headers to sort the results by the values in that column in ascending or descending order.</span></span>

<span data-ttu-id="3b982-210">Vous pouvez cliquer sur **les résultats de filtre** pour filtrer les résultats par une ou plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="3b982-210">You can click **Filter results** to filter the results by one or more columns.</span></span>

<span data-ttu-id="3b982-211">Vous pouvez exporter les résultats une fois que vous avez sélectionné une ou plusieurs lignes en cliquant sur **Exporter les résultats** , puis cliquez sur **exporter tous les résultats**, **exportation chargé de résultats**ou **Exporter la sélection**.</span><span class="sxs-lookup"><span data-stu-id="3b982-211">You can export the results after you've selected one or more rows by clicking **Export results** and then selecting **Export all results**, **Export loaded results**, or **Export selected**.</span></span>

#### <a name="find-related-records-for-this-message"></a><span data-ttu-id="3b982-212">Rechercher des enregistrements connexes pour ce message</span><span class="sxs-lookup"><span data-stu-id="3b982-212">Find related records for this message</span></span>

<span data-ttu-id="3b982-p126">Enregistrements de messages associés sont les enregistrements partageant le même ID de Message. N’oubliez pas de même un message envoyé entre deux personnes peut générer plusieurs enregistrements. Le nombre d’enregistrements augmente lorsque le message est affecté par le développement de groupes de distribution, le transfert, règles de flux de messagerie (également connu sous les règles de transport), etc..</span><span class="sxs-lookup"><span data-stu-id="3b982-p126">Related message records are records that shared the same Message ID. Remember, even a single message sent between two people can generate multiple records. The number of records increases when the message is affected by distribution group expansion, forwarding, mail flow rules (also known as transport rules), etc.</span></span>

<span data-ttu-id="3b982-216">Une fois que vous sélectionnez la case à cocher d’une ligne, vous pouvez rechercher des enregistrements connexes pour le message en cliquant sur le bouton **Rechercher liées** qui s’affiche, ou en sélectionnant des **options plus** ![plus](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Rechercher les enregistrements associés à ce message**).</span><span class="sxs-lookup"><span data-stu-id="3b982-216">After you select a row's check box, you can find related records for the message by clicking the **Find related** button that appears, or by selecting **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Find related records for this message**).</span></span>

<span data-ttu-id="3b982-217">Pour plus d’informations sur l’ID de Message, consultez la section ID de Message plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="3b982-217">For more information about the Message ID, see the Message ID section earlier in this topic.</span></span>

#### <a name="message-trace-details"></a><span data-ttu-id="3b982-218">Détails de suivi des messages</span><span class="sxs-lookup"><span data-stu-id="3b982-218">Message trace details</span></span>

<span data-ttu-id="3b982-219">Dans la sortie du rapport de synthèse, vous pouvez afficher plus d’informations sur un message en utilisant l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3b982-219">In the summary report output, you can view details about a message by using either of the following methods:</span></span>

- <span data-ttu-id="3b982-220">Sélectionnez la ligne (cliquez n’importe où dans la ligne à l’exception de la case à cocher).</span><span class="sxs-lookup"><span data-stu-id="3b982-220">Select the row (click anywhere in the row except the check box).</span></span>

- <span data-ttu-id="3b982-221">Activez la case à cocher de la ligne et cliquez sur **autres options** ![plus](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Détails du message**.</span><span class="sxs-lookup"><span data-stu-id="3b982-221">Select the row's check box and click **More options** ![More](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **View message details**.</span></span>

   ![Détails après en double-cliquant sur une ligne dans les résultats de suivi de message de rapport de synthèse dans le centre de conformité de & sécurité](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

<span data-ttu-id="3b982-223">Détails de suivi des messages contiennent les informations supplémentaires suivantes qui ne sont pas présentes dans le rapport de synthèse :</span><span class="sxs-lookup"><span data-stu-id="3b982-223">The message trace details contain the following additional information that's not present in the summary report:</span></span>

- <span data-ttu-id="3b982-p127">**Événements de message**: cette section contient des classifications qui permettent de catégoriser les actions effectuées par le service sur les messages. Les événements plus intéressantes que vous pouvez rencontrer sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3b982-p127">**Message events**: This section contains classifications that help categorize the actions that the service takes on messages. Some of the more interesting events that you might encounter are:</span></span>

   - <span data-ttu-id="3b982-226">**Réception**: le message a été reçu par le service.</span><span class="sxs-lookup"><span data-stu-id="3b982-226">**Receive**: The message was received by the service.</span></span>

   - <span data-ttu-id="3b982-227">**Envoyer**: le message a été envoyé par le service.</span><span class="sxs-lookup"><span data-stu-id="3b982-227">**Send**: The message was sent by the service.</span></span>

   - <span data-ttu-id="3b982-228">**Échec**: le message d’échec de remise.</span><span class="sxs-lookup"><span data-stu-id="3b982-228">**Fail**: The message failed to be delivered.</span></span>

   - <span data-ttu-id="3b982-229">**Remettre**: le message a été remis à une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3b982-229">**Deliver**: The message was delivered to a mailbox.</span></span>

   - <span data-ttu-id="3b982-230">**Développer**: le message a été envoyé à un groupe de distribution qui a été étendu.</span><span class="sxs-lookup"><span data-stu-id="3b982-230">**Expand**: The message was sent to a distribution group that was expanded.</span></span>

   - <span data-ttu-id="3b982-231">**Transfert**: destinataires ont été déplacés vers un message BIFURQUÉ en raison de la conversion de contenu, les limites de destinataires de message ou d’agents.</span><span class="sxs-lookup"><span data-stu-id="3b982-231">**Transfer**: Recipients were moved to a bifurcated message because of content conversion, message recipient limits, or agents.</span></span>

   - <span data-ttu-id="3b982-232">**Defer**: la remise du message a été différée et peut être nouvelle tentative ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3b982-232">**Defer**: The message delivery was postponed and might be re-attempted later.</span></span>

   - <span data-ttu-id="3b982-p128">**Résolu**: le message a été redirigé vers une nouvelle adresse destinataire basée sur une recherche Active Directory. Dans ce cas, l’adresse du destinataire d’origine est répertorié dans une ligne distincte dans le suivi des messages ainsi que l’état de remise finale pour le message.</span><span class="sxs-lookup"><span data-stu-id="3b982-p128">**Resolved**: The message was redirected to a new recipient address based on an Active Directory look up. When this happens, the original recipient address is listed in a separate row in the message trace along with the final delivery status for the message.</span></span>

   <span data-ttu-id="3b982-235">Notez que même un message feront qui est envoyé avec succès génère plusieurs entrées **d’événements** dans le suivi des messages.</span><span class="sxs-lookup"><span data-stu-id="3b982-235">Note that even an uneventful message that's successfully delivered will generate multiple **Event** entries in the message trace.</span></span>

- <span data-ttu-id="3b982-236">**Plus d’informations**: cette section contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3b982-236">**More information**: This section contains the following details:</span></span>

   - <span data-ttu-id="3b982-p129">**ID de message**: cette valeur est décrit dans la section [ID de Message](#message-id) plus haut dans cette rubrique. Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span><span class="sxs-lookup"><span data-stu-id="3b982-p129">**Message ID**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

   - <span data-ttu-id="3b982-239">**Taille des messages**</span><span class="sxs-lookup"><span data-stu-id="3b982-239">**Message size**</span></span>

   - <span data-ttu-id="3b982-p130">**Adresse IP**: adresse IP de l’ordinateur qui a envoyé le message. Pour les messages sortants envoyés à partir d’Exchange Online, cette valeur est vide.</span><span class="sxs-lookup"><span data-stu-id="3b982-p130">**From IP**: The IP address of the computer that sent the message. For outbound messages sent from Exchange Online, this value is blank.</span></span>

   - <span data-ttu-id="3b982-p131">**Pour IP**: adresse IP ou adresses où le service a tenté de remettre le message. Si le message comporte plusieurs destinataires, elles sont affichées. Pour les messages entrants envoyés vers Exchange Online, cette valeur est vide.</span><span class="sxs-lookup"><span data-stu-id="3b982-p131">**To IP**: The IP address or addresses where the service attempted to deliver the message. If the message has multiple recipients, these are displayed. For inbound messages sent to Exchange Online, this value is blank.</span></span>

### <a name="enhanced-summary-reports"></a><span data-ttu-id="3b982-245">Rapports de synthèse améliorées</span><span class="sxs-lookup"><span data-stu-id="3b982-245">Enhanced summary reports</span></span>

<span data-ttu-id="3b982-p132">(Terminé) améliorée rapports de synthèse disponibles sont disponibles dans la section **rapports téléchargeables** sur le suivi des messages début. Les informations suivantes sont disponibles dans le rapport :</span><span class="sxs-lookup"><span data-stu-id="3b982-p132">Available (completed) Enhanced summary reports are available in the **Downloadable reports** section at the beginning message trace. The following information is available in the report:</span></span>

- <span data-ttu-id="3b982-248">**origin_timestamp**<sup>\*</sup>: la date et l’heure lorsque le message a été initialement reçu par le service en utilisant le temps universel coordonné.</span><span class="sxs-lookup"><span data-stu-id="3b982-248">**origin_timestamp**<sup>\*</sup>: The date and time when the message was initially received by the service, using the configured UTC time zone.</span></span>

- <span data-ttu-id="3b982-249">**sender_address**: adresse de messagerie de l’expéditeur (*alias*@*domaine*).</span><span class="sxs-lookup"><span data-stu-id="3b982-249">**sender_address**: The sender's email address (*alias*@*domain*).</span></span>

- <span data-ttu-id="3b982-p133">**Recipient_status**: l’état de la remise du message au destinataire. Si le message a été envoyé à plusieurs destinataires, elle affiche tous les destinataires et l’état correspondant pour chacun, au format : \< *adresse de messagerie*\>##\<*état*\>. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3b982-p133">**Recipient_status**: The status of the delivery of the message to the recipient. If the message was sent to multiple recipients, it will show all the recipients and the corresponding status for each, in the format: \<*email address*\>##\<*status*\>. For example:</span></span>

   - <span data-ttu-id="3b982-253">**##Receive, envoyer** signifie que le message a été reçu par le service et a été envoyé à la destination prévue.</span><span class="sxs-lookup"><span data-stu-id="3b982-253">**##Receive, Send** means the message was received by the service and was sent to the intended destination.</span></span>

   - <span data-ttu-id="3b982-254">**##Receive, échec** signifie que le message a été reçu par le service mais la remise vers la destination a échoué.</span><span class="sxs-lookup"><span data-stu-id="3b982-254">**##Receive, Fail** means the message was received by the service but delivery to the intended destination failed.</span></span>

   - <span data-ttu-id="3b982-255">**##Receive, remettre** signifie que le message a été reçu par le service et a été remis à la boîte aux lettres du destinataire.</span><span class="sxs-lookup"><span data-stu-id="3b982-255">**##Receive, Deliver** means the message was received by the service and was delivered to the recipient's mailbox.</span></span>

- <span data-ttu-id="3b982-256">**message_subject**: les 256 premiers caractères du champ **d’objet** du message.</span><span class="sxs-lookup"><span data-stu-id="3b982-256">**message_subject**: The first 256 characters of the message's **Subject** field.</span></span>

- <span data-ttu-id="3b982-257">**total_bytes**: la taille du message en octets, y compris les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="3b982-257">**total_bytes**: The size of the message in bytes, including attachments.</span></span>

- <span data-ttu-id="3b982-p134">**message_id**: cette valeur est décrit dans la section [ID de Message](#message-id) plus haut dans cette rubrique. Par exemple, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span><span class="sxs-lookup"><span data-stu-id="3b982-p134">**message_id**: This value is described in the [Message ID](#message-id) section earlier in this topic. For example, `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.</span></span>

- <span data-ttu-id="3b982-p135">**network_message_id**: une valeur d’ID de message unique sont conservées dans toutes les copies du message qui peut être créé en raison de l’expansion de groupe de distribution ou de bifurcation. Est un exemple de valeur `1341ac7b13fb42ab4d4408cf7f55890f`.</span><span class="sxs-lookup"><span data-stu-id="3b982-p135">**network_message_id**: A unique message ID value that persists across all copies of the message that might be created due to bifurcation or distribution group expansion. An example value is `1341ac7b13fb42ab4d4408cf7f55890f`.</span></span>

- <span data-ttu-id="3b982-262">**original_client_ip**: l’adresse IP du client de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="3b982-262">**original_client_ip**: The IP address of the sender's client.</span></span>

- <span data-ttu-id="3b982-263">**orientation**: indique si le message a été envoyé entrant (1) dans votre organisation, ou s’il a été envoyé sortant (2) à partir de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3b982-263">**directionality**: Indicates whether the message was sent inbound (1) to your organization, or whether it was sent outbound (2) from your organization.</span></span>

- <span data-ttu-id="3b982-p136">**connector_id**: le nom du connecteur source ou de destination. Pour plus d’informations sur les connecteurs dans Exchange Online, voir [configurer le flux de messagerie à l’aide de connecteurs dans Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span><span class="sxs-lookup"><span data-stu-id="3b982-p136">**connector_id**: The name of the source or destination connector. For more information about connectors in Exchange Online, see [Configure mail flow using connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).</span></span>

- <span data-ttu-id="3b982-266">**delivery_priority**<sup>\*</sup>: si le message a été envoyé avec une priorité **haute**, **faible**ou **Normal** .</span><span class="sxs-lookup"><span data-stu-id="3b982-266">**delivery_priority**<sup>\*</sup>: Whether the message was sent with **High**, **Low**, or **Normal** priority.</span></span>

<span data-ttu-id="3b982-267"><sup>\*</sup>Ces propriétés sont uniquement disponibles dans les rapports de synthèse améliorée.</span><span class="sxs-lookup"><span data-stu-id="3b982-267"><sup>\*</sup>These properties are only available in Enhanced summary reports.</span></span>

### <a name="extended-reports"></a><span data-ttu-id="3b982-268">Rapports étendus</span><span class="sxs-lookup"><span data-stu-id="3b982-268">Extended reports</span></span>

<span data-ttu-id="3b982-p137">Rapports d’étendue (terminés) disponibles sont disponibles dans la section **rapports Downloadable** au début du suivi des messages. Presque toutes les informations à partir d’un rapport de synthèse améliorée est disponible dans un rapport de l’étendue (à l’exception de **origin_timestamp** et **delivery_priority**). Les informations supplémentaires suivantes sont uniquement disponibles dans un rapport de l’étendue :</span><span class="sxs-lookup"><span data-stu-id="3b982-p137">Available (completed) Extended reports are available in the **Downloadable reports** section at the beginning of message trace. Virtually all of the information from an Enhanced summary report is available in an Extended report (with the exception of **origin_timestamp** and **delivery_priority**). The following additional information is only available in an Extended report:</span></span>

- <span data-ttu-id="3b982-272">**client_ip**: l’adresse IP du serveur de messagerie ou du client de messagerie qui a envoyé le message.</span><span class="sxs-lookup"><span data-stu-id="3b982-272">**client_ip**: The IP address of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="3b982-273">**client_hostname**: le nom d’hôte ou le nom de domaine complet du serveur de messagerie ou du client de messagerie qui a envoyé le message.</span><span class="sxs-lookup"><span data-stu-id="3b982-273">**client_hostname**: The host name or FQDN of the email server or messaging client that submitted the message.</span></span>

- <span data-ttu-id="3b982-274">**server_ip**: l’adresse IP du serveur source ou de destination.</span><span class="sxs-lookup"><span data-stu-id="3b982-274">**server_ip**: The IP address of the source or destination server.</span></span>

- <span data-ttu-id="3b982-275">**server_hostname**: le nom d’hôte ou le nom de domaine complet du serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="3b982-275">**server_hostname**: The host name or FQDN of the destination server.</span></span>

- <span data-ttu-id="3b982-p138">**source_context**: associées au champ de la **source** des informations supplémentaires. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3b982-p138">**source_context**: Extra information associated with the **source** field. For example:</span></span>

   - `Protocol Filter Agent`

   - `3489061114359050000`

- <span data-ttu-id="3b982-p139">**source**: composant The Exchange Online qui est responsable de l’événement. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3b982-p139">**source**: The Exchange Online component that's responsible for the event. For example:</span></span>

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- <span data-ttu-id="3b982-280">**ID_événement**: ils correspondent aux valeurs qui sont décrites dans la section [Rechercher les enregistrements associés à ce message](#find-related-records-for-this-message) **d’événement de Message** .</span><span class="sxs-lookup"><span data-stu-id="3b982-280">**event_id**: These correspond to the **Message event** values that are explained in the [Find related records for this message](#find-related-records-for-this-message) section.</span></span>

- <span data-ttu-id="3b982-281">**internal_message_id**: un identificateur de message qui est affecté par le serveur Exchange Online qui traite le message actuellement.</span><span class="sxs-lookup"><span data-stu-id="3b982-281">**internal_message_id**: A message identifier that's assigned by the Exchange Online server that's currently processing the message.</span></span>

- <span data-ttu-id="3b982-p140">**recipient_address**: les adresses de messagerie des destinataires du message. Plusieurs adresses de messagerie sont séparés par un point-virgule ( ;).</span><span class="sxs-lookup"><span data-stu-id="3b982-p140">**recipient_address**: The email addresses of the message's recipients. Multiple email addresses are separated by the semicolon character (;).</span></span>

- <span data-ttu-id="3b982-284">**recipient_count**: le nombre total de destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="3b982-284">**recipient_count**: The total number of recipients in the message.</span></span>

- <span data-ttu-id="3b982-285">**related_recipient_address**: utilisé avec `EXPAND`, `REDIRECT`, et `RESOLVE` événements pour afficher les autres destinataires de messagerie adresses qui sont associées au message.</span><span class="sxs-lookup"><span data-stu-id="3b982-285">**related_recipient_address**: Used with `EXPAND`, `REDIRECT`, and `RESOLVE` events to display other recipient email addresses that are associated with the message.</span></span>

- <span data-ttu-id="3b982-p141">**référence**: ce champ contient des informations supplémentaires pour des types spécifiques d’événements. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3b982-p141">**reference**: This field contains additional information for specific types of events. For example:</span></span>

   - <span data-ttu-id="3b982-p142">**DSN**: contient le lien de rapport, qui est la valeur de **message_id** de la notification d’état de remise associée (également appelé un DSN, rapport de non-remise, un rapport de non-remise ou message de retour) si une source de données est généré à la suite de cet événement. S’il s’agit d’un message DSN, ce champ contient la valeur de **message_id** du message d’origine qui a été généré pour la source de données.</span><span class="sxs-lookup"><span data-stu-id="3b982-p142">**DSN**: Contains the report link, which is the **message_id** value of the associated delivery status notification (also known as a DSN, non-delivery report, NDR, or bounce message) if a DSN is generated subsequent to this event. If this is a DSN message, this field contains the **message_id** value of the original message that the DSN was generated for.</span></span>

   - <span data-ttu-id="3b982-290">**Développer**: contient la valeur **related_recipient_address** des messages associés.</span><span class="sxs-lookup"><span data-stu-id="3b982-290">**EXPAND**: Contains the **related_recipient_address** value of the related messages.</span></span>

   - <span data-ttu-id="3b982-291">**Réception**: peut contenir la valeur de **message_id** du message connexe si le message a été généré par d’autres processus (par exemple, les règles de boîte de réception).</span><span class="sxs-lookup"><span data-stu-id="3b982-291">**RECEIVE**: Might contain the **message_id** value of the related message if the message was generated by other processes (for example, Inbox rules).</span></span>

   - <span data-ttu-id="3b982-292">**Envoyer**: contient la valeur **internal_message_id** de tous les messages DSN.</span><span class="sxs-lookup"><span data-stu-id="3b982-292">**SEND**: Contains the **internal_message_id** value of any DSN messages.</span></span>

   - <span data-ttu-id="3b982-293">**Transfert**: contient la valeur **internal_message_id** du message est en cours dirigé (par exemple, en la conversion de contenu, les limites de destinataires de message ou d’agents).</span><span class="sxs-lookup"><span data-stu-id="3b982-293">**TRANSFER**: Contains the **internal_message_id** value of the message that's being forked (for example, by content conversion, message recipient limits, or agents).</span></span>

   - <span data-ttu-id="3b982-294">**MAILBOXRULE**: contient la valeur **internal_message_id** du message entrant qui a provoqué la règle de boîte de réception générer le message sortant.</span><span class="sxs-lookup"><span data-stu-id="3b982-294">**MAILBOXRULE**: Contains the **internal_message_id** value of the inbound message that caused the Inbox rule to generate the outbound message.</span></span>

   <span data-ttu-id="3b982-295">Pour tous les autres types d’événements, ce champ est généralement vide.</span><span class="sxs-lookup"><span data-stu-id="3b982-295">For other types of events, this field is usually blank.</span></span>

- <span data-ttu-id="3b982-p143">**return_path**: l’adresse e-mail spécifiée par la commande **MAIL FROM** qui a envoyé le message. Bien que ce champ n’est jamais vide, il peut avoir la valeur d’adresse expéditeur null représentée sous forme de `<>`.</span><span class="sxs-lookup"><span data-stu-id="3b982-p143">**return_path**: The return email address specified by the **MAIL FROM** command that sent the message. Although this field is never empty, it can have the null sender address value represented as `<>`.</span></span>

- <span data-ttu-id="3b982-p144">**message_info**: plus d’informations sur le message. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3b982-p144">**message_info**: Additional information about the message. For example:</span></span>

   - <span data-ttu-id="3b982-p145">La message origine date-heure au format UTC pour `DELIVER` et `SEND` événements. L’heure-date d’origine est lorsque le message d’entrée tout d’abord l’organisation Exchange Online. L’heure UTC est représentée dans le format de date et d’heure ISO8601 : `yyyy-mm-ddThh:mm:ss.fffZ`, où `yyyy` = année, `mm` = mois, `dd` = jour, `T` indique le début du composant heure, `hh` = heure, `mm` = minute, `ss` = deuxième, `fff` = fractions de seconde, et `Z` signifie `Zulu`, qui est une autre façon d’indiquer au format UTC.</span><span class="sxs-lookup"><span data-stu-id="3b982-p145">The message origination date-time in UTC for `DELIVER` and `SEND` events. The origination date-time is the time when the message first entered the Exchange Online organization. The UTC date-time is represented in the ISO 8601 date-time format: `yyyy-mm-ddThh:mm:ss.fffZ`, where `yyyy` = year, `mm` = month, `dd` = day, `T` indicates the beginning of the time component, `hh` = hour, `mm` = minute, `ss` = second, `fff` = fractions of a second, and `Z` signifies `Zulu`, which is another way to denote UTC.</span></span>

   - <span data-ttu-id="3b982-p146">Erreurs d’authentification. Par exemple, vous pouvez voir la valeur `11a` et le type d’authentification utilisé lors de l’erreur d’authentification.</span><span class="sxs-lookup"><span data-stu-id="3b982-p146">Authentication errors. For example, you might see the value `11a` and the type of authentication that was used when the authentication error occurred.</span></span>

- <span data-ttu-id="3b982-305">**tenant_id**: une valeur GUID qui représente l’organisation Exchange Online (par exemple, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span><span class="sxs-lookup"><span data-stu-id="3b982-305">**tenant_id**: A GUID value that represents the Exchange Online organization (for example, `39238e87-b5ab-4ef6-a559-af54c6b07b42`).</span></span>

- <span data-ttu-id="3b982-306">**original_server_ip**: l’adresse IP du serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="3b982-306">**original_server_ip**: The IP address of the original server.</span></span>

- <span data-ttu-id="3b982-p147">**custom_data**: contient les données associées à des types d’événement spécifique. Pour plus d’informations, voir les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b982-p147">**custom_data**: Contains data related to specific event types. For more information, see the following sections.</span></span>

#### <a name="customdata-values"></a><span data-ttu-id="3b982-309">valeurs custom_data</span><span class="sxs-lookup"><span data-stu-id="3b982-309">custom_data values</span></span>

<span data-ttu-id="3b982-p148">Le champ **custom_data** pour un `AGENTINFO` événement est utilisé par un grand nombre d’agents Exchange Online pour journaliser les détails du traitement du message. Parmi les plus intéressantes agents sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b982-p148">The **custom_data** field for an `AGENTINFO` event is used by a variety of Exchange Online agents to log message processing details. Some of the more interesting agents are described in the following sections.</span></span>

#### <a name="spam-filter-agent"></a><span data-ttu-id="3b982-312">Agent de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="3b982-312">Spam filter agent</span></span>

<span data-ttu-id="3b982-p149">Une valeur **custom_data** qui commence par `S:SFA` est à partir de l’agent de filtrage du courrier indésirable. Les détails sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="3b982-p149">A **custom_data** value that starts with `S:SFA` is from the spam filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="3b982-315">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3b982-315">**Value**</span></span>|<span data-ttu-id="3b982-316">**Description**</span><span class="sxs-lookup"><span data-stu-id="3b982-316">**Description**</span></span>|
|:-----|:-----|
|`SFV=NSPM`|<span data-ttu-id="3b982-317">Le message a été marqué comme n'étant pas un courrier indésirable et a été envoyé aux destinataires appropriés.</span><span class="sxs-lookup"><span data-stu-id="3b982-317">The message was marked as non-spam and was sent to the intended recipients.</span></span>|
|`SFV=SPM`|<span data-ttu-id="3b982-318">Le message a été marqué comme courrier indésirable par le filtre de contenu.</span><span class="sxs-lookup"><span data-stu-id="3b982-318">The message was marked as spam by the content filter.</span></span>|
|`SFV=BLK`|<span data-ttu-id="3b982-319">Le filtrage a été ignoré et le message a été bloqué, car il provient d'un expéditeur bloqué.</span><span class="sxs-lookup"><span data-stu-id="3b982-319">Filtering was skipped and the message was blocked because it originated from a blocked sender.</span></span>|
|`SFV=SKS`|<span data-ttu-id="3b982-p150">Le message a été marqué comme courrier indésirable avant d'être traité par le filtre de contenu. Cela inclut les messages pour lesquels une règle de transport les a marqués automatiquement comme étant des courriers indésirables et où toutes les étapes de filtrage supplémentaires ont été contournées.</span><span class="sxs-lookup"><span data-stu-id="3b982-p150">The message was marked as spam prior to being processed by the content filter. This includes messages where the message matched a Transport rule to automatically mark it as spam and bypass all additional filtering.</span></span>|
|`SCL=<number>`|<span data-ttu-id="3b982-322">Pour plus d'informations sur les différentes valeurs de SCL et leur signification, voir [Seuils de probabilité de courrier indésirable](https://technet.microsoft.com/library/jj200686.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b982-322">For more information about the different SCL values and what they mean, see [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`PCL=<number>`|<span data-ttu-id="3b982-p151">Valeur du seuil de probabilité de courrier d'hameçonnage (PCL) du message. Ces valeurs peuvent être interprétées de la même façon que les valeurs SCL répertoriées dans [Seuils de probabilité de courrier indésirable](https://technet.microsoft.com/library/jj200686.aspx).  </span><span class="sxs-lookup"><span data-stu-id="3b982-p151">The Phishing Confidence Level (PCL) value of the message. These can be interpreted the same way as the SCL values documented in [Spam confidence levels](https://technet.microsoft.com/library/jj200686.aspx).</span></span>|
|`DI=SB`|<span data-ttu-id="3b982-325">L'expéditeur du message a été bloqué.</span><span class="sxs-lookup"><span data-stu-id="3b982-325">The sender of the message was blocked.</span></span>|
|`DI=SQ`|<span data-ttu-id="3b982-326">Le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="3b982-326">The message was quarantined.</span></span>|
|`DI=SD`|<span data-ttu-id="3b982-327">Le message a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="3b982-327">The message was deleted.</span></span>|
|`DI=SJ`|<span data-ttu-id="3b982-328">Le message a été mis dans le dossier Courrier indésirable du destinataire.</span><span class="sxs-lookup"><span data-stu-id="3b982-328">The message was sent to the recipient's Junk Email folder.</span></span>|
|`DI=SN`|<span data-ttu-id="3b982-p152">Le message a été routé via le pool de remise à risque plus élevé. Pour plus d’informations, voir [pool de remise à haut risque pour les messages sortants](https://technet.microsoft.com/library/jj200746.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b982-p152">The message was routed through the higher risk delivery pool. For more information, see [High-risk delivery pool for outbound messages](https://technet.microsoft.com/library/jj200746.aspx).</span></span>|
|`DI=SO`|<span data-ttu-id="3b982-331">Le message a été routé via le pool de remises normal pour les messages sortants.</span><span class="sxs-lookup"><span data-stu-id="3b982-331">The message was routed through the normal outbound delivery pool.</span></span>|
|<span data-ttu-id="3b982-332">' SFS = [a]</span><span class="sxs-lookup"><span data-stu-id="3b982-332">\`SFS=[a]</span></span>|<span data-ttu-id="3b982-333">SFS = [b]'</span><span class="sxs-lookup"><span data-stu-id="3b982-333">SFS=[b]\`</span></span>|<span data-ttu-id="3b982-334">Cela indique que des règles anti-spam ont été associées.</span><span class="sxs-lookup"><span data-stu-id="3b982-334">This denotes that spam rules were matched.</span></span>|
|`IPV=CAL`|<span data-ttu-id="3b982-335">Le message n'a pas été bloqué par les filtres anti-spam car l'adresse IP se trouve dans une liste d'adresses IP autorisées du filtre des connexions.</span><span class="sxs-lookup"><span data-stu-id="3b982-335">The message was allowed through the spam filters because the IP address was specified in an IP Allow list in the connection filter.</span></span>|
|`H=<EHLOstring>`|<span data-ttu-id="3b982-336">La chaîne HELO ou EHLO du serveur de messagerie qui se connecte.</span><span class="sxs-lookup"><span data-stu-id="3b982-336">The HELO or EHLO string of the connecting email server.</span></span>|
|`PTR=<ReverseDNS>`|<span data-ttu-id="3b982-337">Enregistrement PTR de l'adresse IP d'envoi, également appelé adresse DNS inverse.</span><span class="sxs-lookup"><span data-stu-id="3b982-337">The PTR record of the sending IP address, also known as the reverse DNS address.</span></span>|

<span data-ttu-id="3b982-338">Un exemple de valeur **custom_data** pour un message est filtré comme courrier indésirable similaire à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="3b982-338">An example **custom_data** value for a message that's filtered for spam like this:</span></span>

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a><span data-ttu-id="3b982-339">Agent de filtrage des programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="3b982-339">Malware filter agent</span></span>

<span data-ttu-id="3b982-p153">Une valeur **custom_data** qui commence par `S:AMA` est à partir de l’agent de filtrage des programmes malveillants. Les détails sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="3b982-p153">A **custom_data** value that starts with `S:AMA` is from the malware filter agent. The key details are described in the following table:</span></span>

|<span data-ttu-id="3b982-342">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3b982-342">**Value**</span></span>|<span data-ttu-id="3b982-343">**Description**</span><span class="sxs-lookup"><span data-stu-id="3b982-343">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b982-344">' AMA = SOMME</span><span class="sxs-lookup"><span data-stu-id="3b982-344">\`AMA=SUM</span></span>|<span data-ttu-id="3b982-345">v=1</span><span class="sxs-lookup"><span data-stu-id="3b982-345">v=1</span></span>|<span data-ttu-id="3b982-346">` or `AMA=EV</span><span class="sxs-lookup"><span data-stu-id="3b982-346">` or `AMA=EV</span></span>|<span data-ttu-id="3b982-347">v = 1'</span><span class="sxs-lookup"><span data-stu-id="3b982-347">v=1\`</span></span>|<span data-ttu-id="3b982-p154">Le message a été déterminé contenant des programmes malveillants. `SUM` indique le programme malveillant avoir été détecté par n’importe quel nombre de moteurs. `EV` indique le programme malveillant détecté par un moteur spécifique. Lorsque programme malveillant est détecté par un moteur que cela déclenche les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b982-p154">The message was determined to contain malware. `SUM` indicates the malware could've been detected by any number of engines. `EV` indicates the malware was detected by a specific engine. When malware is detected by an engine this triggers the subsequent actions.</span></span>|
|`Action=r`|<span data-ttu-id="3b982-352">Le message a été remplacé.</span><span class="sxs-lookup"><span data-stu-id="3b982-352">The message was replaced.</span></span>|
|`Action=p`|<span data-ttu-id="3b982-353">Le message a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="3b982-353">The message was bypassed.</span></span>|
|`Action=d`|<span data-ttu-id="3b982-354">Le message a été différé.</span><span class="sxs-lookup"><span data-stu-id="3b982-354">The message was deferred.</span></span>|
|`Action=s`|<span data-ttu-id="3b982-355">Le message a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="3b982-355">The message was deleted.</span></span>|
|`Action=st`|<span data-ttu-id="3b982-356">Le message a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="3b982-356">The message was bypassed.</span></span>|
|`Action=sy`|<span data-ttu-id="3b982-357">Le message a été ignoré.</span><span class="sxs-lookup"><span data-stu-id="3b982-357">The message was bypassed.</span></span>|
|`Action=ni`|<span data-ttu-id="3b982-358">Le message a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="3b982-358">The message was rejected.</span></span>|
|`Action=ne`|<span data-ttu-id="3b982-359">Le message a été rejeté.</span><span class="sxs-lookup"><span data-stu-id="3b982-359">The message was rejected.</span></span>|
|`Action=b`|<span data-ttu-id="3b982-360">Le message a été bloqué.</span><span class="sxs-lookup"><span data-stu-id="3b982-360">The message was blocked.</span></span>|
|`Name=<malware>`|<span data-ttu-id="3b982-361">Nom du programme malveillant détecté.</span><span class="sxs-lookup"><span data-stu-id="3b982-361">The name of the malware that was detected.</span></span>|
|`File=<filename>`|<span data-ttu-id="3b982-362">Nom du fichier qui contenait le programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="3b982-362">The name of the file that contained the malware.</span></span>|

<span data-ttu-id="3b982-363">Un exemple de valeur **custom_data** pour un message contenant des programmes malveillants ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="3b982-363">An example **custom_data** value for a message that contains malware looks like this:</span></span>

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a><span data-ttu-id="3b982-364">Agent de règle de transport</span><span class="sxs-lookup"><span data-stu-id="3b982-364">Transport rule agent</span></span>

<span data-ttu-id="3b982-p155">Une valeur **custom_data** qui commence par`S:TRA` est à partir de l’agent de règle de transport pour les règles de flux de messagerie (également connu sous les règles de transport). Les détails sont décrits dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="3b982-p155">A **custom_data** value that starts with`S:TRA` is from the transport rule agent for mail flow rules (also known as transport rules). The key details are described in the following table:</span></span>

|<span data-ttu-id="3b982-367">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3b982-367">**Value**</span></span>|<span data-ttu-id="3b982-368">**Description**</span><span class="sxs-lookup"><span data-stu-id="3b982-368">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b982-369">' ETR</span><span class="sxs-lookup"><span data-stu-id="3b982-369">\`ETR</span></span>|<span data-ttu-id="3b982-370">ruleId =<guid>\`</span><span class="sxs-lookup"><span data-stu-id="3b982-370">ruleId=<guid>\`</span></span>|<span data-ttu-id="3b982-371">ID de la règle qui s'applique.</span><span class="sxs-lookup"><span data-stu-id="3b982-371">The rule ID that was matched.</span></span>|
|`St=<datetime>`|<span data-ttu-id="3b982-372">La date et l’heure UTC lorsque la correspondance de règle.</span><span class="sxs-lookup"><span data-stu-id="3b982-372">The date and time in UTC when the rule match occurred.</span></span>|
|`Action=<ActionDefinition>`|<span data-ttu-id="3b982-p156">L’action qui a été appliquée. Pour obtenir la liste des actions disponibles, voir [flux de messagerie des actions de règle dans Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span><span class="sxs-lookup"><span data-stu-id="3b982-p156">The action that was applied. For a list of available actions, see [Mail flow rule actions in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).</span></span>|
|`Mode=<Mode>`|<span data-ttu-id="3b982-p157">Le mode de la règle. Les valeurs valides sont :</span><span class="sxs-lookup"><span data-stu-id="3b982-p157">The mode of the rule. Valid values are: </span></span><br/><span data-ttu-id="3b982-377">• **Appliquer**: toutes les actions de la règle seront appliquées.</span><span class="sxs-lookup"><span data-stu-id="3b982-377">• **Enforce**: All actions on the rule will be enforced.</span></span> <br/><span data-ttu-id="3b982-378">• **Test avec conseils de stratégie :**: tous les conseils de stratégie seront envoyés, mais les autres actions d’application ne seront pas effectuées.</span><span class="sxs-lookup"><span data-stu-id="3b982-378">• **Test with Policy Tips:**: Any Policy Tip actions will be sent, but other enforcement actions will not be acted on.</span></span> <br/><span data-ttu-id="3b982-379">• **Test sans conseils de stratégie**: Actions seront consignées dans un fichier journal, mais les expéditeurs ne seront pas informés de toute façon et actions d’application ne seront pas effectuées.</span><span class="sxs-lookup"><span data-stu-id="3b982-379">• **Test without Policy Tips**: Actions will be listed in a log file, but senders will not be notified in any way, and enforcement actions will not be acted on.</span></span>|

<span data-ttu-id="3b982-380">Une valeur **custom_data** d’exemple pour un message qui correspond aux conditions d’une règle de flux de messagerie ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="3b982-380">An example **custom_data** value for a messages that matches the conditions of a mail flow rule looks like this:</span></span>

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`
