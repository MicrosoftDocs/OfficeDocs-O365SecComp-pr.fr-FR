---
title: Recherche et réponse automatiques dans Office 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/04/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Découvrez les fonctionnalités d’analyse et de réponse automatisées dans Office 365 Advanced Threat Protection.
ms.openlocfilehash: a62714adb0682d3faf27e25fff365bb1ba6d4fc5
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2019
ms.locfileid: "36761700"
---
# <a name="automated-investigation-and-response-air-in-office-365"></a>Recherche et réponse automatiques dans Office 365

Les fonctionnalités d’analyse et de réponse automatisées (incluses dans [Office 365 Advanced Threat Protection](office-365-atp.md) plan 2) vous permettent d’exécuter des processus d’enquête automatisés en réponse à des menaces connues qui existent aujourd’hui. Lisez cet article pour obtenir une vue d’ensemble de l’AIR et comment il peut aider votre organisation et les équipes chargées de la sécurité à réduire les menaces de manière plus efficace. Pour commencer à utiliser AIR, consultez la rubrique [enquêter et répondre aux menaces dans Office 365](office-365-air.md).

> [!NOTE]
> Vous devez être un administrateur général, un administrateur de sécurité, un opérateur de sécurité ou un lecteur de sécurité pour effectuer les tâches décrites dans cet article. Pour plus d’informations, consultez la rubrique [Microsoft 365 Security Center : Roles and Permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).

## <a name="the-overall-flow-of-air"></a>Flux d’AIR global

À un niveau élevé, le flux d’AIR fonctionne comme ceci :

|Phase  |Ce qui est impliqué  |
|---------|---------|
|0,1     |[Alerte](#alerts) déclenchée et un [manifeste de sécurité](#security-playbooks) est initié.         |
|n°2     |En fonction du manuel d’alerte et de sécurité en particulier, l' [enquête automatisée commence immédiatement](#example-a-user-reported-phish-message-launches-an-investigation-playbook). (Alternativement, un analyste de sécurité peut [lancer une enquête automatisée manuellement](#example-a-security-administrator-triggers-an-investigation-from-threat-explorer), à partir d’une valeur dans un rapport, tel qu' [Explorer](threat-explorer.md).)         |
|3     |Lorsqu’une enquête automatisée s’exécute, son étendue peut augmenter en tant que nouvelles alertes associées.         |
|4     |Pendant et après une enquête automatisée, des [Détails et des résultats](#investigation-graph) peuvent être consultés. Les résultats incluent les [actions recommandées](#recommended-actions) qui peuvent être prises pour répondre et corriger les menaces détectées. De plus, un [Journal des manifestes](#playbook-log) est disponible pour suivre toutes les activités d’enquête.<br/>Si votre organisation utilise une solution de création de rapports personnalisée ou une solution tierce, vous pouvez [utiliser l’API activité de gestion d’Office 365](office-365-air.md#use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions) pour afficher des informations sur les analyses et les menaces automatisées.         |
|disque     |Votre équipe de gestion des opérations de sécurité examine les résultats et les recommandations, et approuve les actions de correction. Dans Office 365, les actions de correction ne sont prises qu’après approbation de l’équipe de sécurité de votre organisation.         |

Les sections suivantes fournissent plus d’informations sur AIR, notamment des informations sur les alertes, les règles de sécurité et les détails de l’enquête. De plus, deux exemples de fonctionnement de l’AIR sont inclus dans cet article. Pour commencer à utiliser AIR, consultez la rubrique [enquêter et répondre aux menaces dans Office 365](office-365-air.md).

## <a name="alerts"></a>Alertes

Les [alertes](alert-policies.md#viewing-alerts) représentent des déclencheurs pour les flux de travail d’équipe des opérations de sécurité pour la réponse aux incidents. La définition de la priorité des alertes à droite pour l’enquête, tout en s’assurant qu’aucune menace n’est sans adresse est complexe. Lorsque les enquêtes dans les alertes sont effectuées manuellement, les équipes des opérations de sécurité doivent rechercher et corréler les entités (par exemple, le contenu, les appareils et les utilisateurs) menacées. Ces tâches et les flux de travail sont très longs et impliquent plusieurs outils et systèmes. Avec AIR, l’analyse et la réponse sont automatisées dans les alertes de gestion de la sécurité et des menaces clés qui déclenchent automatiquement vos règles de réponse de sécurité. 

Dans la version initiale d’AIR (début du 2019 avril), les alertes générées à partir des stratégies d’alerte d’événements uniques suivantes sont automatiquement analysées. 

- Un clic d’URL potentiellement malveillant a été détecté

- Courrier électronique signalé par l’utilisateur comme hameçonnage *

- Messages électroniques contenant des programmes malveillants supprimés après la remise *

- Messages électroniques contenant des URL d’hameçonnage supprimées après la remise *

> [!NOTE]
> Ces alertes ont reçu une sévérité « informatif » dans les stratégies d’alerte respectives dans le centre de sécurité & conformité avec notifications par courrier électronique désactivées. Ces éléments peuvent être activés par le biais de la configuration de la stratégie d’alerte.

Pour afficher les alertes, dans le centre de sécurité & conformité, sélectionnez **alertes** > **afficher les alertes**. Sélectionnez une alerte pour afficher ses détails, puis, à partir de là, utilisez le lien **consulter l’enquête** pour accéder à l' [enquête](#investigation-graph)correspondante. Notez que les alertes d’information sont masquées par défaut dans l’affichage des alertes. Pour les afficher, vous devez modifier le filtrage des alertes de manière à inclure des alertes d’information.

Si votre organisation gère vos alertes de sécurité par le biais d’un système de gestion des alertes, d’un système de gestion des services ou d’un système de gestion des événements et des informations de sécurité (SIEM), vous pouvez envoyer des alertes Office 365 à ce système via une notification par courrier électronique ou via le [ API d’activité de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). Les notifications d’alerte d’enquête via le courrier électronique ou l’API incluent des liens permettant d’accéder aux alertes dans le centre de sécurité & conformité, ce qui permet à l’administrateur de sécurité affecté de naviguer rapidement dans l’enquête.

![Alertes liées à des enquêtes](media/air-alerts-page-details.png) 

## <a name="security-playbooks"></a>Règles de sécurité

Les règles de sécurité sont des stratégies principales qui sont au cœur de l’automatisation dans la protection contre les menaces Microsoft. Les règles de sécurité fournies dans AIR sont basées sur des scénarios de sécurité réels courants. Un manuel de sécurité est lancé automatiquement lorsqu’une alerte est déclenchée au sein de votre organisation. Une fois que l’alerte est déclenchée, le manuel associé est exécuté automatiquement. Le manuel exécute une enquête, en examinant toutes les métadonnées associées (notamment les messages électroniques, les utilisateurs, les sujets, les expéditeurs, etc.). En fonction des conclusions du manuel, AIR recommande un ensemble d’actions que l’équipe de sécurité de votre organisation peut prendre pour contrôler et atténuer la menace. 

Les règles de sécurité que vous obtenez avec AIR sont conçues pour aborder les menaces les plus fréquentes auxquelles les entreprises sont confrontés aujourd’hui. Elles sont basées sur les opérations de sécurité et les équipes de réponse aux incidents, notamment celles qui permettent de défendre les ressources de Microsoft et de nos clients.

### <a name="security-playbooks-are-rolling-out-in-phases"></a>Les règles de sécurité sont déployées en plusieurs phases

Dans le cadre de l’AIR, les règles de sécurité sont déployées en plusieurs phases. Lors de la phase 1 (l’aperçu a commencé en avril 2019), plusieurs règles ont été publiées, qui incluent des recommandations pour les actions que les administrateurs de la sécurité examinent et approuvent :
- Message hameçon signalé par l’utilisateur
- URL cliquez sur modifier le verdict 
- Détection de programmes malveillants après la livraison (programmes malveillants ZAP)
- Hameçonnage détecté après la livraison ZAP (hameçon ZAP)

La phase 1 inclut également des enquêtes manuelles par courrier électronique (à l’aide de l' [Explorateur de menaces](threat-explorer.md)).

La phase 2 est maintenant en cours. Consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) pour voir les autres éléments planifiés et bientôt disponibles.

### <a name="playbooks-include-investigation-and-recommendations"></a>Les règles incluent une enquête et des recommandations

Dans AIR, chaque manuel de sécurité inclut les éléments suivants : 
- une enquête racine, 
- les étapes à suivre pour identifier et corréler les autres menaces potentielles, et 
- actions de correction des menaces recommandées.

Chaque étape de haut niveau inclut de nombreuses sous-étapes qui sont exécutées pour fournir une réponse approfondie, détaillée et exhaustive aux menaces.

## <a name="automated-investigations"></a>Analyses automatisées

La page enquêtes automatiques indique les évaluations de votre organisation et leurs États actuels.

![Page d’enquête principale pour l’AIR](media/air-maininvestigationpage.png) 
  
Vous pouvez :
- Accédez directement à une enquête (sélectionnez un **ID d’enquête**).
- Appliquer des filtres. Choisissez entre **type**d’enquête **, période**, **État**ou une combinaison de ces éléments.
- Exportez les données dans un fichier. csv.

L’état d’enquête indique la progression de l’analyse et des actions. Lors de l’exécution de l’enquête, les États changent pour indiquer si des menaces ont été détectées et si des actions ont été approuvées. 
- **Début**: l’enquête est mise en file d’attente pour commencer bientôt.
- **En cours d’exécution**: l’enquête a commencé et mène son analyse
- **Aucune menace détectée**: l’enquête a terminé son analyse et aucune menace n’a été détectée.
- **Terminé par le système**: l’enquête n’a pas été fermée et a expiré après 7 jours
- **Action en attente**: l’enquête a détecté des menaces avec des actions recommandées
- **Menaces détectées**: l’enquête a détecté des menaces, mais les menaces n’ont pas d’actions disponibles dans l’air
- **Corrigé**: l’enquête s’est terminée et a été entièrement corrigée (toutes les actions ont été approuvées)
- **Partiellement résolue**: l’enquête terminée et certaines des actions recommandées ont été approuvées
- **Terminé par l’utilisateur**: un administrateur a mis fin à l’enquête.
- **Échec**: une erreur s’est produite lors de l’enquête qui l’empêche d’atteindre une conclusion sur les menaces
- Mise **en file d’attente par limitation**: l’enquête attend une analyse en raison de limitations de traitement du système (pour protéger les performances du service)
- **Interruption par la limitation**: l’enquête n’a pas pu être terminée en temps suffisant en raison des limitations de traitement du volume et du système. Vous pouvez déclencher à nouveau l’enquête en sélectionnant l’e-mail dans l’Explorateur et en sélectionnant l’action examiner.

### <a name="investigation-graph"></a>Graphique d’enquête

Lorsque vous ouvrez une enquête spécifique, vous voyez la page Graph de l’enquête. Cette page affiche toutes les entités différentes : les messages électroniques, les utilisateurs (ainsi que leurs activités) et les appareils qui ont été automatiquement analysés dans le cadre de l’alerte déclenchée.

![Page graphique d’enquête sur l’AIR](media/air-investigationgraphpage.png)

Vous pouvez :
- Obtenir une vue d’ensemble visuelle de l’enquête actuelle.
- Afficher un résumé de la durée de l’enquête.
- Sélectionnez un nœud dans la visualisation pour afficher les détails de ce nœud.
- Sélectionnez un onglet dans la partie supérieure pour afficher les détails de cet onglet.

### <a name="alert-investigation"></a>Enquête sur les alertes

Dans l’onglet **alertes** pour une enquête, vous pouvez voir des alertes relatives à l’enquête. Les détails incluent l’alerte qui a déclenché l’enquête et d’autres alertes, telles que la connexion à risque, le téléchargement en masse, etc., qui sont corrélées à l’enquête. À partir de cette page, un analyste de sécurité peut également afficher des détails supplémentaires sur des alertes individuelles.

![Page alertes AÉRIENNEs](media/air-investigationalertspage.png)

Vous pouvez :
- Obtenir une vue d’ensemble visuelle de l’alerte de déclenchement actuelle et de toutes les alertes associées.
- Sélectionnez une alerte dans la liste pour ouvrir une page de survol qui affiche les détails de l’alerte complète.

### <a name="email-investigation"></a>Enquête par courrier électronique

Dans l’onglet **e-mail** pour une enquête, vous pouvez voir tous les clusters de courrier électronique identifiés dans le cadre de l’enquête. 

Étant donné le volume de courrier électronique que les utilisateurs d’une organisation envoient et reçoivent, le processus de 
- mise en cluster de messages électroniques en fonction d’attributs similaires provenant d’un en-tête, d’un corps, d’une URL et de pièces jointes de message ; 
- séparation du courrier électronique malveillant du courrier électronique approprié ; les 
- prendre des mesures sur les messages électroniques malveillants 

peut prendre plusieurs heures. AIR automatise ce processus en enregistrant le temps et les efforts de l’équipe de sécurité de votre organisation. 

Il est possible d’identifier deux types différents de clusters de messagerie lors de l’analyse du courrier : les clusters de similitudes et les clusters d’indicateurs. 
- Les clusters de similarité sont des messages électroniques contenant des attributs d’expéditeur et de contenu similaires. Ces clusters sont évalués pour le contenu malveillant en fonction des résultats de la détection d’origine. Les clusters de messagerie qui contiennent suffisamment de détections malveillantes sont considérés comme malveillants.
- Les clusters d’indicateurs sont des messages électroniques qui contiennent la même entité d’indicateur (hachage de fichier ou URL) que le courrier électronique d’origine. Lorsque l’entité fichier/URL d’origine est identifiée comme malveillante, AIR applique le verdict de l’indicateur à l’ensemble du cluster de messages contenant cette entité. En tant que fichier identifié comme un programme malveillant, le cluster de messages électroniques contenant ce fichier est traité comme un message électronique de programme malveillant.

L’objectif du clustering est de trouver d’autres messages électroniques associés envoyés par le même expéditeur dans le cadre d’une attaque ou d’une campagne.

L’onglet **courrier** électronique affiche également les éléments de courrier liés à l’enquête, tels que les détails du message électronique, le courrier électronique d’origine signalé, le ou les messages électroniques zapped en raison de programmes malveillants/hameçons, etc.

Le nombre de messages identifiés dans l’onglet e-mail représente actuellement la somme totale de tous les messages électroniques affichés dans l’onglet **e-mail** . Étant donné que les messages électroniques sont présents dans plusieurs clusters, le nombre total réel de messages électroniques identifiés (et affectés par les actions de correction) est le nombre de messages électroniques uniques présents sur tous les clusters et les messages électroniques des destinataires d’origine. 

L’Explorateur et l’AIR envoient les messages électroniques par destinataire, étant donné que les verdicts de sécurité, les actions et les emplacements de remise varient selon les destinataires. Par conséquent, un message électronique d’origine envoyé à trois utilisateurs est compté comme un total de trois messages électroniques au lieu d’un seul. Remarque dans certains cas, un courrier électronique est compté deux ou plusieurs fois, car le courrier électronique peut avoir plusieurs actions et il peut y avoir plusieurs copies de l’e-mail une fois toutes les actions effectuées. Par exemple, un courrier indésirable détecté lors de la remise peut entraîner le blocage du courrier électronique (mis en quarantaine) et le remplacement du courrier électronique (fichier de menace remplacé par un fichier d’avertissement, puis remis à la boîte aux lettres de l’utilisateur). Étant donné qu’il y a littéralement deux copies du courrier électronique dans le système, celles-ci peuvent être comptées dans le compte du cluster. 

Le nombre de messages est calculé lors de l’enquête et certains comptes sont recalculés lorsque vous ouvrez des lanceurs d’investigation (sur la base d’une requête sous-jacente). Le nombre de messages affichés pour les clusters de courrier électronique sous l’onglet e-mail et la valeur de quantité de courrier électronique affichée dans la fenêtre mobile du cluster sont calculés lors de l’enquête. Nombre de messages électroniques affiché en bas de l’onglet e-mail de la fenêtre mobile du cluster, et le nombre de messages électroniques affichés dans l’Explorateur reflètent les messages électroniques reçus après l’analyse initiale de l’enquête. Par conséquent, un cluster de messagerie qui affiche une quantité initiale de 10 messages électroniques affiche une liste de courriers au total 15 lorsque 5 autres messages électroniques arrivent entre la phase d’analyse de l’enquête et lorsque l’administrateur révise l’enquête. L’affichage des deux comptes dans différentes vues permet d’indiquer l’impact du courrier électronique au moment de l’examen et l’impact actuel jusqu’à l’exécution de la correction.

À titre d’exemple, considérons le scénario suivant. Le premier cluster de trois messages électroniques était considéré comme un hameçonnage. Un autre cluster de messages similaires avec la même adresse IP et l’objet a été trouvé et considéré comme malveillant, car certains d’entre eux étaient identifiés comme des hameçons lors de la détection initiale. 

![Page d’enquête sur le courrier électronique aérien](media/air-investigationemailpage.png)

Vous pouvez :
- Obtenir une vue d’ensemble visuelle des résultats de clustering actuels et des menaces détectées.
- Cliquez sur une entité de cluster ou une liste de menaces pour ouvrir une page de survol qui affiche les détails de l’alerte complète.
- Pour approfondir le cluster de messagerie, cliquez sur le lien « ouvrir dans l’Explorateur » en haut de l’onglet « Détails du cluster de messagerie ».

![Courrier électronique d’enquête aérienne avec détails du menu volant](media/air-investigationemailpageflyoutdetails.png)

* Remarque : dans le contexte de la messagerie électronique, vous pouvez voir une surface d’anomalie de volume dans le cadre de l’enquête. Une anomalie de volume indique un pic dans les messages électroniques similaires de la durée de l’événement d’enquête par rapport aux délais précédents. Ce pic dans le trafic de messagerie avec des caractéristiques similaires (par exemple, domaine d’objet et de l’expéditeur, similitude entre le corps et IP de l’expéditeur) est typique du début des campagnes ou des attaques par courrier électronique. Toutefois, les campagnes de courrier électronique, de courrier indésirable et légitimes partagent généralement ces caractéristiques. Les anomalies de volume représentent une menace potentielle et peuvent donc être moins sévères par rapport aux menaces de programmes malveillants ou hameçons identifiées à l’aide de moteurs antivirus, de détonation ou de réputation malveillante.

### <a name="user-investigation"></a>Enquête utilisateur

Sous l’onglet **utilisateurs** , vous pouvez voir tous les utilisateurs identifiés dans le cadre de l’enquête. Les comptes d’utilisateur apparaissent dans l’enquête lorsqu’il existe un événement ou une indication que ces comptes d’utilisateur peuvent être affectés ou compromis.

Par exemple, dans l’image suivante, AIR a identifié des indicateurs de compromission et des anomalies en fonction d’une nouvelle règle de boîte de réception créée. Des détails supplémentaires (preuve) de l’enquête sont disponibles via des vues détaillées dans cet onglet. les indicateurs de compromis et d’anomalies peuvent également inclure des détections d’anomalies dans la [sécurité des applications Cloud de Microsoft](https://docs.microsoft.com/cloud-app-security).

![Page des utilisateurs de l’enquête aérienne](media/air-investigationuserspage.png)

Vous pouvez :
- Obtenir une vue d’ensemble visuelle des résultats et des risques utilisateur identifiés.
- Sélectionnez un utilisateur pour ouvrir une page de survol qui affiche les détails de l’alerte complète.

### <a name="machine-investigation"></a>Enquête sur les machines

Sous l’onglet **ordinateurs** , vous pouvez voir tous les ordinateurs identifiés dans le cadre de l’enquête. 

![Page de l’ordinateur d’enquête aérien](media/air-investigationmachinepage.png)

Dans le cadre de l’enquête, AIR établit une corrélation entre les menaces de messagerie et les appareils. Par exemple, une enquête transmet un hachage de fichier malveillant à [Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection
) pour enquêter. Cela permet l’analyse automatisée des ordinateurs pertinents pour vos utilisateurs, afin de garantir que les menaces sont résolues à la fois dans le nuage et sur vos points de terminaison. 

Vous pouvez :
- Obtenir une vue d’ensemble visuelle des ordinateurs et menaces actuels détectés.
- Sélectionnez un ordinateur pour ouvrir une vue dans les [recherches Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations) associées dans le centre de sécurité Microsoft Defender.

### <a name="entity-investigation"></a>Enquête d’entité

Sous l’onglet **entités** , vous pouvez voir toutes les entités identifiées dans le cadre de l’enquête. 

Ici, vous pouvez voir les entités analysées et les détails des types d’entités, tels que les messages électroniques, les clusters, les adresses IP, les utilisateurs, et bien plus encore. Vous pouvez également voir le nombre d’entités analysées et les menaces associées à chacune d’elles. 

![Page des entités d’enquête sur l’AIR](media/air-investigationentitiespage.png)

Vous pouvez :
- Obtenir une vue d’ensemble visuelle des entités d’enquête et des menaces détectées.
- Sélectionnez une entité pour ouvrir une page de survol qui affiche les détails de l’entité associée.

![Détails des entités d’enquête aérienne](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>Journal des manifestes

Sous l’onglet **Journal** , vous pouvez voir toutes les étapes du manuel qui ont eu lieu lors de l’enquête. Le journal capture un inventaire complet de toutes les actions effectuées par les fonctionnalités d’enquête automatique d’Office 365 dans le cadre de l’AIR. Elle offre une vue claire de toutes les étapes effectuées, y compris l’action elle-même, une description et la durée du début à la fin. 

![Page Journal d’enquête aérienne](media/air-investigationlogpage.png)

Vous pouvez :
- Obtenir une vue d’ensemble visuelle des étapes du manuel.
- Exportez les résultats dans un fichier CSV.
- Filtrer l’affichage.

### <a name="recommended-actions"></a>Actions recommandées

Sous l’onglet **actions** , vous pouvez voir toutes les actions de recherche qui sont recommandées pour la correction une fois l’enquête terminée. 

Actions Capturez les étapes que Microsoft vous recommande d’effectuer à la fin de l’enquête. Vous pouvez prendre des mesures de correction ici en sélectionnant une ou plusieurs actions. Si vous cliquez sur **approuver** , le début de la correction est possible. (Les autorisations appropriées sont nécessaires : le rôle « recherche et purge » est requis pour exécuter des actions à partir de l’Explorateur et de l’AIR). Par exemple, un lecteur de sécurité peut afficher les actions mais pas les approuver. Remarque : vous n’avez pas besoin d’approuver toutes les actions. Si vous n’acceptez pas l’action recommandée ou si votre organisation ne choisit pas certains types d’actions, vous pouvez choisir de **refuser** les actions ou simplement les ignorer et n’effectuer aucune action. L’approbation et/ou le rejet de toutes les actions permettent à l’enquête de se fermer complètement, tout en laissant certaines actions incomplètes dans l’état de l’enquête en passant à un état partiellement résolu.

![Page action de l’enquête par avion](media/air-investigationactionspage.png)

Vous pouvez :
- Obtenir une vue d’ensemble visuelle des actions recommandées.
- Sélectionnez une ou plusieurs actions.
- Approuver ou rejeter les actions recommandées avec les commentaires.
- Exportez les résultats dans un fichier CSV.
- Filtrer l’affichage.

## <a name="example-a-user-reported-phish-message-launches-an-investigation-playbook"></a>Exemple : un message hameçon signalé par un utilisateur lance un manuel d’enquête.

Lorsqu’un utilisateur de votre organisation soumet un message électronique et le signale à Microsoft à l’aide du [complément de message de rapport pour Outlook ou Outlook Web Access](enable-the-report-message-add-in.md), le rapport est également envoyé à votre système et est visible dans l’Explorateur dans la vue signalée par l’utilisateur. Ce message signalée par l’utilisateur déclenche désormais une alerte d’information basée sur le système, qui lance automatiquement le manuel d’enquête.

Lors de la phase d’enquête de racine, différents aspects du courrier électronique sont évalués. Ces approches sont les suivantes :
- Détermination du type de menace susceptible de se présenter ;
- Expéditeur ;
- Emplacement d’envoi du courrier électronique (infrastructure émettrice);
- Si d’autres instances du courrier électronique ont été remises ou bloquées ;
- Une évaluation de nos analystes ;
- Si le courrier électronique est associé à des campagnes connues ;
- et bien plus encore.

Une fois l’enquête terminée, le manuel fournit une liste des actions recommandées à effectuer sur le courrier électronique d’origine et les entités qui lui sont associées.
  
Ensuite, plusieurs étapes d’enquête sur les menaces et de chasse sont exécutées :

- Les messages électroniques similaires dans d’autres clusters de messagerie sont recherchés.
- Le signal est partagé avec d’autres plateformes, telles que [Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection).
- Une détermination est effectuée sur le fait que les utilisateurs aient cliqué sur les liens malveillants dans les messages électroniques suspects.
- Une vérification est effectuée dans Office 365 Exchange Online Protection ([EOP](eop/exchange-online-protection-eop.md)) et Office 365 Advanced Threat Protection ([ATP](office-365-atp.md)) pour voir s’il existe d’autres messages similaires signalés par les utilisateurs.
- Une vérification est exécutée pour déterminer si un utilisateur a été compromis. Cette vérification exploite les signaux de la sécurité de l' [application Cloud Microsoft](https://docs.microsoft.com/cloud-app-security) et d' [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), en mettant en corrélation les anomalies d’activité de l’utilisateur associées. 

Au cours de la phase de chasse, les risques et les menaces sont affectés à différentes étapes de la chasse. 

La correction est la phase finale du manuel. Pendant cette phase, les étapes de correction sont prises, en fonction des phases d’enquête et de chasse. 

## <a name="example-a-security-administrator-triggers-an-investigation-from-threat-explorer"></a>Exemple : un administrateur de sécurité déclenche une enquête à partir de l’Explorateur de menaces

En plus des recherches automatiques déclenchées par une alerte, l’équipe des opérations de sécurité de votre organisation peut déclencher une enquête automatique à partir d’une vue dans l' [Explorateur de menaces](use-explorer-in-security-and-compliance.md).

Par exemple, supposons que vous affichiez des données dans l’Explorateur à propos des messages signalés par l’utilisateur. Vous pouvez sélectionner un élément dans la liste des résultats, puis cliquer sur **examiner**.

![Messages signalés par l’utilisateur dans l’Explorateur avec le bouton Rechercher](media/Explorer-UserReported-Investigate.png)

Autre exemple : Supposons que vous affichiez des données sur les messages électroniques détectés comme contenant des programmes malveillants, et que plusieurs messages électroniques soient détectés comme contenant des programmes malveillants. Vous pouvez sélectionner l’onglet **courrier électronique** , sélectionner un ou plusieurs messages, puis, dans le menu **actions** , sélectionner **examiner**. 

![Démarrage d’une enquête pour les programmes malveillants dans l’Explorateur](media/Explorer-Malware-Email-ActionsInvestigate.png)

À l’instar des règles déclenchées par une alerte, les recherches automatiques déclenchées à partir d’une vue dans l’Explorateur incluent une enquête de racine, des étapes permettant d’identifier et de corréler les menaces, ainsi que les actions recommandées pour atténuer ces menaces.

## <a name="how-to-get-air"></a>Comment obtenir de l’AIR

Office 365 AIR sont inclus dans les abonnements suivants :

- Microsoft 365 Entreprise E5
- Office 365 Entreprise E5
- Protection Microsoft contre les menaces
- Plan 2 de protection avancée contre les menaces Office 365

Si vous n’avez pas l’un de ces abonnements, [Démarrez une version d’évaluation gratuite](https://go.microsoft.com/fwlink/p/?LinkID=698279&culture=en-US&country=US).

Pour en savoir plus sur la disponibilité des fonctionnalités, consultez la rubrique [disponibilité des fonctionnalités dans les plans de protection avancée contre les menaces](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).

## <a name="next-steps"></a>Étapes suivantes

[Prise en main de l’utilisation de l’AIR dans Office 365](office-365-air.md)

[En savoir plus sur AIR dans Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations) 

[Consultez la feuille de route Microsoft 365 pour découvrir les éléments bientôt disponibles et à déployer](https://www.microsoft.com/microsoft-365/roadmap?filters=)