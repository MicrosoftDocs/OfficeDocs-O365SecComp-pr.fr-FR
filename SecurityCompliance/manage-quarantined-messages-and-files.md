---
title: Gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
ms.date: 09/05/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent apprendre à afficher et à gérer les messages mis en quarantaine dans le centre de sécurité & de la sécurité d’Office 365.
ms.openlocfilehash: 0b67abe3dbf21650925b53d2882bc40096d6a646
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822524"
---
# <a name="manage-quarantined-messages-and-files-as-an-admin-in-office-365"></a>Gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365

En tant qu’administrateur, vous pouvez afficher, publier et supprimer des messages mis en quarantaine, et signaler des messages en quarantaine faux positifs dans Office 365. Vous pouvez également afficher, télécharger et supprimer les fichiers mis en quarantaine capturés par Advance Threat Protection (ATP) pour SharePoint Online, OneDrive entreprise et Microsoft Teams. Vous pouvez configurer des stratégies pour qu’Office 365 filtre les messages et les envoie à la mise en quarantaine pour plusieurs raisons : ils ont été identifiés comme courrier indésirable, courrier en nombre, courrier de hameçonnage, contenant des programmes malveillants, ou parce qu’ils correspondent à une règle de flux de messagerie.

Par défaut, Office 365 envoie les messages de hameçonnage et les messages contenant des programmes malveillants directement en quarantaine. Les autres messages filtrés sont envoyés dans le dossier de courrier indésirable des utilisateurs, sauf si vous configurez une stratégie pour les envoyer en quarantaine.

Pour afficher et effectuer des actions sur les messages mis en quarantaine dans le centre de sécurité & conformité, votre compte a besoin de l’une des autorisations suivantes :

**Rôle destinataires en affichage seul**: Affichez la liste des messages mis en quarantaine.

**Rôle du lecteur de sécurité**: Affichez la liste des messages mis en quarantaine et les en-têtes de leurs messages.

**Rôle d’administrateur de sécurité**: afficher la liste des messages mis en quarantaine et les en-têtes de leurs messages ; Prévisualiser, publier, supprimer et télécharger les messages mis en quarantaine.

Par défaut, les groupes de rôles Administrateur de sécurité et gestion de l’organisation dans le centre de sécurité & conformité ont le rôle administrateur de sécurité qui leur est affecté (l’appartenance à l’un de ces groupes de rôles vous accorde les autorisations). Pour plus d’informations, consultez [la rubrique autorisations dans le centre de conformité & Office 365 Security](permissions-in-the-security-and-compliance-center.md).

> [!IMPORTANT]
> Par défaut, les messages de courrier indésirable et de phishing sont conservés en quarantaine pendant 30 jours. Les messages mis en quarantaine en raison d’une correspondance avec une règle de flux de messagerie sont conservés en quarantaine pendant 7 jours. Les messages malveillants sont maintenus en quarantaine pendant 15 jours. Vous pouvez personnaliser la durée de mise en quarantaine du courrier indésirable dans les paramètres de blocage du courrier indésirable dans le centre de sécurité & Compliance Center. Lorsque Office 365 supprime un message de la mise en quarantaine, vous ne pouvez pas le récupérer. Si vous le souhaitez, vous pouvez modifier la période de rétention des messages mis en quarantaine dans vos stratégies de filtrage du courrier indésirable. Pour plus d’informations, reportez-vous à la section [définir la période de rétention de quarantaine](#set-the-quarantine-retention-period) de cette rubrique.

## <a name="view-your-organizations-quarantined-messages"></a>Afficher les messages mis en quarantaine de votre organisation

1. [Ouvrez le centre de sécurité & conformité](go-to-the-securitycompliance-center.md) et accédez à la **mise en quarantaine**de la **vérification** \> de la **gestion** \> des menaces.

   > [!TIP]
   > Pour accéder directement à la page de **mise en quarantaine** , utilisez l' [https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)URL suivante :.

   Par défaut, le centre de sécurité & conformité affiche tous les messages électroniques mis en quarantaine en tant que courrier indésirable. Les messages sont triés du plus récent au plus ancien en fonction de la **Date** de réception du message. L' **expéditeur**, l' **objet**et la date d’expiration (sous **expire**) sont également affichés pour chaque message. Vous pouvez effectuer un tri sur un champ en cliquant sur l’en-tête de colonne correspondant ; Cliquez une deuxième fois sur un en-tête de colonne pour inverser l’ordre de tri.

2. Vous pouvez afficher la liste de tous les messages mis en quarantaine ou réduire le jeu de résultats en filtrant. Vous pouvez uniquement effectuer des opérations en bloc sur un maximum de 100 éléments, de sorte que le filtrage peut également contribuer à réduire votre jeu de résultats si vous avez plus de. Vous pouvez rapidement filtrer les messages pour une seule raison de mise en quarantaine en choisissant une option dans le filtre en haut de la page. Les options sont les suivantes :

   - Courrier identifié comme courrier indésirable

   - Courrier en quarantaine, car il correspond à une stratégie définie par une règle de flux de messagerie (également appelée règle de transport).

   - Courrier électronique identifié comme courrier en nombre

   - Courrier électronique identifié comme courrier de hameçonnage

   - Courrier en quarantaine, car il contient des programmes malveillants

En tant qu’administrateur, vous pouvez également choisir de filtrer tous les messages pour votre organisation ou uniquement les messages qui vous sont envoyés. Les utilisateurs finaux peuvent uniquement afficher et utiliser les messages qui leur ont été envoyés.

Vous pouvez également filtrer vos résultats pour rechercher des messages spécifiques. Pour obtenir des conseils, reportez-vous à la section [Filtrer les résultats pour rechercher les messages et les fichiers mis en quarantaine](#filter-the-results-to-find-quarantined-messages-and-files) dans cette rubrique.

Une fois que vous avez trouvé un message en quarantaine spécifique, cliquez sur le message pour en afficher les détails et effectuer des actions, comme la publication du message dans la boîte aux lettres d’un utilisateur.

## <a name="view-your-organizations-quarantined-files"></a>Afficher les fichiers mis en quarantaine de votre organisation

1. [Ouvrez le centre de sécurité & conformité](go-to-the-securitycompliance-center.md) et accédez à la **mise en quarantaine**de la **vérification** \> de la **gestion** \> des menaces.

   > [!TIP]
   > Pour accéder directement à la page de **mise en quarantaine** dans le centre de sécurité & conformité, utilisez l’URL suivante : >[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)

   Par défaut, la page affiche les messages électroniques mis en quarantaine. Pour afficher les fichiers mis en quarantaine, définissez les filtres en haut de la page pour afficher les **fichiers**mis en quarantaine en raison de **programmes malveillants**.

   Les fichiers sont triés du plus récent au plus ancien en fonction de la date à laquelle le fichier a été mis en quarantaine. Le dernier **utilisateur** qui a modifié le fichier, le **service** auquel le fichier a été publié, le **nom de fichier**, l' **emplacement**, la **taille de fichier**et la date d’expiration ( **expire**) sont également répertoriés pour chaque fichier. Vous pouvez effectuer un tri sur un champ en cliquant sur un en-tête ; Cliquez une deuxième fois sur un en-tête de colonne pour inverser l’ordre de tri.

2. Vous pouvez afficher la liste de tous les fichiers mis en quarantaine ou Rechercher des fichiers spécifiques en les filtrant. Tout comme les messages, vous pouvez uniquement effectuer des opérations en bloc sur un maximum de 100 éléments. Actuellement, le centre de sécurité & conformité vous permet d’afficher et de gérer les fichiers en quarantaine car ils ont été identifiés comme contenant des programmes malveillants. Pour obtenir des conseils, consultez la section suivante.

## <a name="filter-the-results-to-find-quarantined-messages-and-files"></a>Filtrer les résultats pour rechercher les messages et les fichiers mis en quarantaine

En fonction de vos paramètres, il peut y avoir un grand nombre de messages et de fichiers mis en quarantaine. Pour rechercher un message ou un fichier spécifique ou un ensemble de messages ou de fichiers, vous pouvez filtrer les éléments mis en quarantaine en fonction d’une variété d’informations supplémentaires.

1. Sur la page **mise en quarantaine** , vérifiez que la ligne supérieure de filtres est définie pour afficher les messages ou les fichiers selon vos besoins :

   - Pour rechercher des fichiers, définissez les filtres sur Afficher les **fichiers** mis en quarantaine en raison d’un **programme malveillant**.

     Pour les fichiers mis en quarantaine, la page affiche tous les fichiers mis en quarantaine, et pas seulement le vôtre, indépendamment de ce que vous lui indiquez.

   - Pour rechercher des messages mis en quarantaine, définissez des filtres sur afficher **tout** ou **seulement mon** **courrier électronique**. Pour le dernier filtre, choisissez le type de message en quarantaine que vous recherchez. Vous pouvez rechercher les messages mis en quarantaine identifiés comme **courrier indésirable**, les messages qui correspondent à une règle de flux de messagerie (**règle de transport**), le courrier **en nombre** , le courrier de **hameçonnage** ou le courrier contenant des **programmes malveillants**.

2. Sous **Trier les résultats par**, sélectionnez le filtre ou les filtres que vous souhaitez utiliser pour la recherche dans les listes déroulantes. Les options varient selon que vous recherchez des fichiers ou des messages. Les caractères génériques ne sont pas pris en charge dans les champs de recherche pour le moment.

   Pour les fichiers et les messages, vous pouvez choisir de filtrer selon la date à laquelle le message ou le fichier a été envoyé en quarantaine. Vous pouvez spécifier la date ou une plage de dates, y compris l’heure. Vous pouvez également filtrer vos résultats de recherche en fonction de la date d’expiration à laquelle le fichier ou le message sera supprimé de la quarantaine, ou vous pouvez utiliser une combinaison de filtres. Pour effectuer une recherche par date d’expiration, choisissez **filtre avancé**. Sous **expire**, vous pouvez sélectionner les messages qui seront supprimés de la quarantaine au cours des prochaines 24 heures **(aujourd’hui**), au cours des prochaines 48 heures ( **2 prochains jours**), au cours de la semaine suivante (7 prochains **jours**) ou vous pouvez sélectionner un intervalle de temps personnalisé.

   Pour les messages, vous disposez des options supplémentaires suivantes :

   - **ID du message**: utilisez cette information pour identifier un message spécifique lorsque vous êtes informé de l’ID du message.

     Par exemple, si un message spécifique est envoyé par un utilisateur de votre organisation ou s’il est destiné à celui-ci, mais qu’il n’a jamais atteint sa destination, vous pouvez rechercher le message à l’aide d’un [suivi des messages](message-trace-scc.md). Si vous découvrez que le message a été envoyé en quarantaine, peut-être parce qu’il correspond à une règle de flux de messagerie ou qu’il a été identifié comme courrier indésirable, vous pouvez facilement trouver ce message en quarantaine en spécifiant son ID de message. Veillez à inclure la chaîne d’ID de message complète. Cela peut inclure des chevrons\<\>(), par exemple `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`:.

   - **Adresse de messagerie**de l’expéditeur : choisissez de filtrer par une adresse de messagerie d’expéditeur unique.

   - **Adresse de messagerie du destinataire**: choisissez de filtrer par une seule adresse de courrier de destinataire.

   - **Objet**. Entrez l’objet de l’adresse de messagerie que vous souhaitez trouver. Étant donné que la recherche par caractères génériques n’est pas prise en charge, vous devez utiliser tout l’objet du message afin que la recherche renvoie le message dans les résultats. La recherche ne respecte pas la casse.

## <a name="view-details-about-quarantined-messages-and-files"></a>Afficher les détails des messages et des fichiers mis en quarantaine

Lorsque vous sélectionnez un élément affiché dans la liste de mise en quarantaine, vous voyez un résumé de ses propriétés dans le volet d' **informations** sur le côté droit du centre de sécurité & conformité.

### <a name="details-displayed-for-quarantined-messages"></a>Détails affichés pour les messages mis en quarantaine

- **ID du message**: identificateur unique du message.

- **Adresse**de l’expéditeur : qui a envoyé le message.

- **Received**: date et heure de réception du message.

- **Objet**: texte de la ligne d’objet du message.

- **Type**: indique si un message a été identifié comme **courrier indésirable**, **Bulk**, **hameçon**, correspond à une règle de flux de messagerie (**règle de transport**) ou a été identifié comme contenant un **programme malveillant**.

- **Expire**: date et heure auxquelles le message est automatiquement supprimé de la mise en quarantaine.

- **Publié à**: toutes les adresses de messagerie (le cas échéant) vers lesquelles le message a été publié.

- **Pas encore publié à**: toutes les adresses de messagerie (le cas échéant) auxquelles le message n’a pas encore été publié.

### <a name="details-displayed-for-quarantined-files"></a>Détails affichés pour les fichiers mis en quarantaine

- **Nom de fichier**: nom du fichier en quarantaine.

- **Chemin d’accès au site**: URL qui définit l’emplacement du fichier dans Office 365.

- **Date/heure détectée**: date et heure de mise en quarantaine du fichier.

- **Expire**: date à laquelle le message sera supprimé de la quarantaine.

- **Détecté par**: méthode utilisée pour détecter le programme malveillant dans le fichier. Il peut s’agir de la valeur ATP (protection avancée contre les menaces) ou du moteur anti-programme malveillant de Microsoft.

- **Publié**: indique si le fichier a été publié ou non.

- **Nom du programme malveillant**: famille et nom du programme malveillant détecté dans le fichier.

- **ID de document**: identificateur unique pour le document.

- **Taille du fichier**: taille du fichier en Ko.

- **Organisation**: ID unique de votre organisation dans Office 365.

- **Modifié par**: compte professionnel ou scolaire de l’utilisateur qui a modifié le fichier pour la dernière fois.

- **Taille du fichier**: taille du fichier en Ko.

- **Hachage SHA256**: hachage du fichier. Vous pouvez l’utiliser pour rechercher d’autres magasins de réputation que vous pouvez avoir ou examiner où se trouve le fichier dans votre environnement.

## <a name="manage-messages-and-files-in-quarantine"></a>Gestion des messages et des fichiers en quarantaine

Une fois que vous avez sélectionné un message ou un groupe de messages en quarantaine, vous disposez de plusieurs options pour effectuer les opérations suivantes :

- Ne rien faire : Si vous choisissez de ne rien faire, le message sera automatiquement supprimé par Office 365 lors de son expiration. Par défaut, le courrier indésirable, le courrier indésirable, les programmes malveillants, le hameçonnage et les messages mis en quarantaine, car ils correspondent à une règle de flux de messagerie sont maintenus en quarantaine pendant 30 jours. Lorsque Office 365 supprime un message de la mise en quarantaine, vous ne pouvez pas le récupérer. Si vous le souhaitez, vous pouvez modifier la période de rétention des messages mis en quarantaine en configurant le paramètre **conserver le courrier indésirable pendant (jours)** dans vos stratégies anti-courrier indésirable. Pour plus d’informations, reportez-vous à la section [définir la période de rétention de quarantaine](#set-the-quarantine-retention-period) de cette rubrique.

- **Afficher l’en-tête**du message : cliquez sur ce lien pour afficher le texte d’en-tête du message. Pour analyser l’en-tête en profondeur, copiez le texte d’en-tête de message dans votre presse-papiers, puis choisissez **analyseur d’en-têtes de message Microsoft** pour accéder à l’analyseur de connectivité à distance (cliquez avec le bouton droit et choisissez **ouvrir dans un nouvel onglet** si vous ne souhaitez pas quitter Office 365 pour effectuer cette tâche). Collez l’en-tête du message sur la page dans la section analyseur d’en-têtes de message, puis choisissez **analyser les en-têtes**.

- **Afficher un aperçu du message**: vous permet d’afficher les versions brutes ou HTML du texte du corps du message. En mode HTML, les liens sont désactivés.

- **Télécharger un message** ou un **fichier de téléchargement**: choisissez cette option pour télécharger une copie du message ou du fichier sur votre appareil local. Vous devrez confirmer que vous comprenez les risques associés au téléchargement des éléments à partir de la mise en quarantaine avant d’être autorisés à le faire. Les messages sont enregistrés au format. eml dans un dossier que vous spécifiez. Les fichiers mis en quarantaine sont enregistrés dans leur format d’origine.

- **Supprimer**: Si vous le souhaitez, vous pouvez supprimer immédiatement un élément mis en quarantaine (ou un ensemble d’éléments) au lieu d’attendre la date d’expiration définie par Office 365. Pour supprimer un message ou un fichier, dans la liste de mise en quarantaine, sélectionnez l’élément, puis cliquez sur **supprimer**. Pour supprimer plusieurs éléments à la fois, activez la case à cocher à gauche des éléments dans la liste de mise en quarantaine, puis, dans la page **actions en bloc** qui s’affiche, choisissez **Supprimer les messages sélectionnés** ou **Supprimer les fichiers sélectionnés**.

- **Publication**: Libérez un élément mis en quarantaine (ou un ensemble d’éléments) et signalez les éléments comme étant en quarantaine (faux positifs) à Microsoft.

  Pour publier et signaler un seul message ou fichier, dans la liste de mise en quarantaine, sélectionnez l’élément, choisissez **libérer le fichier** ou **diffuser le message**. Sur la page suivante, vérifiez que l’option **signaler les messages à Microsoft pour analyse** ou **fichiers de rapports à Microsoft pour analyse** est sélectionnée.

  Pour libérer plusieurs éléments à la fois, activez la case à cocher à gauche des éléments dans la liste de mise en quarantaine, puis, dans la page **actions en bloc** qui s’affiche, choisissez **libérer les fichiers** ou les **messages de publication**. Sur la page suivante, vérifiez que l’option **signaler les messages à Microsoft pour analyse** ou **fichiers de rapports à Microsoft pour analyse** est sélectionnée.

Lorsque vous publiez des messages, gardez à l’esprit les points suivants :

- Lorsque vous effectuez une dissémination en bloc de plusieurs messages à la fois, les messages sont publiés vers tous les destinataires identifiés à l’origine. Si vous souhaitez uniquement diffuser les messages à des destinataires spécifiques, vous devez les libérer un à la fois et identifier les destinataires individuellement.

- Un message ne peut pas être publié plus d’une fois au même destinataire.

- Lorsque vous publiez un message pour plusieurs destinataires, seuls les destinataires qui n’ont pas reçu le message ont été affichés dans la liste des destinataires potentiels.

- Lorsque vous choisissez de signaler les faux positifs, si le ou les messages que vous exportez ont été mis en quarantaine en tant que courrier indésirable, Bulk, phishing ou en tant que contenant des programmes malveillants, le message sera également signalé à l’équipe d’analyse du courrier indésirable de Microsoft. L’équipe évalue et analyse le message et, en fonction des résultats de l’analyse, les règles de filtrage de contenu de courrier indésirable à l’échelle du service peuvent être ajustées pour autoriser le message.

## <a name="set-the-quarantine-retention-period"></a>Définir la période de rétention de quarantaine

Vous pouvez configurer la durée de mise en quarantaine des messages et des fichiers avant leur expiration. Par défaut, les éléments mis en quarantaine sont conservés pendant 30 jours. Vous configurez ce paramètre pour chaque stratégie que vous créez. Vous pouvez également modifier la valeur de la stratégie par défaut comme décrit dans cet article.

### <a name="modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security--compliance-center"></a>Modifier la période de rétention de quarantaine pour la stratégie de filtrage du courrier indésirable par défaut dans le centre de sécurité & conformité

1. [Ouvrez le centre de sécurité & conformité](go-to-the-securitycompliance-center.md) et accédez à **protection contre le courrier indésirable**de la **stratégie** \> de **gestion** \> des menaces.

   > [!TIP]
   > Pour accéder directement à la page **blocage du courrier indésirable** , utilisez l’URL suivante :[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)

2. Choisissez **personnalisée** pour afficher l’onglet **paramètres personnalisés** .

3. Développez la ligne **stratégie de filtrage du courrier indésirable par défaut (toujours active)** .

4. Choisissez **modifier la stratégie**. Les paramètres de la stratégie de filtrage du courrier indésirable par défaut apparaissent dans une nouvelle page.

5. Développez **les actions de courrier indésirable et en bloc**.

6. Sous **quarantaine**, dans la zone de texte **conserver les courriers indésirables pendant (jours)** , entrez la durée pendant laquelle vous souhaitez qu’Office 365 conserve les messages et les fichiers en quarantaine. La valeur par défaut est 30 jours. Il s’agit également de la valeur maximale.

7. Choisissez **Enregistrer**.
