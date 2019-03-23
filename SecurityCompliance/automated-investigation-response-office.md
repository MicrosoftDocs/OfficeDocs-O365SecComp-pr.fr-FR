---
title: Recherche et réponse automatisées (AIR) avec Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Découvrez les fonctionnalités d'analyse et de réponse automatisées dans Office 365 Advanced Threat Protection.
ms.openlocfilehash: c6cfc03588e580382f673b2e9be8543bfcaf9ac1
ms.sourcegitcommit: f6073deec39a18581ed12abef18728417a52cdf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2019
ms.locfileid: "30747560"
---
# <a name="automated-investigation-and-response-air-with-office-365"></a>Recherche et réponse automatisées (AIR) avec Office 365

AutoMated Investigation and Response (AIR) (bientôt disponible pour les [fonctionnalités d'enquête et de réponse aux menaces Office 365](office-365-ti.md)) vous permet d'effectuer des recherches et des corrections automatiques sur des menaces connues qui existent aujourd'hui. Lisez cet article pour obtenir une vue d'ensemble de l'AIR et comment il peut aider votre organisation et les équipes chargées de la sécurité à réduire les menaces de manière plus efficace. Pour en savoir plus sur la disponibilité de fonctionnalités supplémentaires dans AIR, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).

## <a name="alerts"></a>Alertes

Les [alertes](alert-policies.md#viewing-alerts) représentent des déclencheurs pour les flux de travail d'équipe des opérations de sécurité pour la réponse aux incidents. La définition de la priorité des alertes à droite pour l'enquête tout en s'assurant qu'aucune menace n'est sans adresse est complexe. Lorsque les enquêtes dans les alertes sont effectuées manuellement, les équipes des opérations de sécurité doivent rechercher et corréler les entités (par exemple, le contenu, les appareils et les utilisateurs) menacées. Ces tâches et les flux de travail sont très longs et impliquent plusieurs outils et systèmes. Avec AIR, l'analyse et la réponse sont automatisées dans les alertes de gestion de la sécurité et des menaces clés qui déclenchent automatiquement vos règles de réponse de sécurité. 

Dans la version initiale d'AIR en avril 2019, les alertes générées à partir des stratégies d'alerte d'événements Singel suivantes seront analysées automatiquement. 

1. Un clic d'URL potentiellement malveillant a été détecté
2. Courrier électronique signalé par l'utilisateur comme hameçonnage *
3. Messages électroniques contenant des programmes malveillants supprimés après la remise *
4. Messages électroniques contenant des URL d'hameçonnage supprimées après la remise *

* Remarque: ces alertes ont reçu une sévérité «inFormatif» dans les stratégies d'alerte respectives dans le centre de sécurité et de conformité et les notifications par courrier électronique sont désactivées. Ces éléments peuvent être activés par le biais de la configuration de la stratégie d'alerte.

pour afficher les alertes, dans le centre de sécurité & de sécurité Office 365, sélectionnez **alertes** > **afficher les alertes**. Sélectionnez une alerte pour afficher ses détails, puis, à partir de là, utilisez le lien **consulter l'enquête** pour accéder à l' [enquête](#investigation-graph)correspondante.

![Alertes liées à des enquêtes](media/air-alerts-page-details.png) 


## <a name="security-playbooks"></a>Règles de sécurité

Les règles de sécurité sont des stratégies principales qui sont au cœur de l'automatisation dans la protection contre les menaces Microsoft. Les règles de sécurité fournies dans AIR sont basées sur des scénarios de sécurité réels courants. Un manuel de sécurité est lancé automatiquement lorsqu'une alerte est déclenchée au sein de votre organisation. Une fois que l'alerte est déclenchée, le manuel associé est exécuté automatiquement. Le manuel exécute une enquête, en examinant toutes les métadonnées associées (y compris les messages électroniques, les utilisateurs, les objets, les expéditeurs, etc.) et, en fonction de ses conclusions, recommande une série d'actions que l'équipe de sécurité de votre organisation peut prendre pour contrôler et atténuer la menace. 

Les règles de sécurité que vous obtenez avec AIR sont conçues pour aborder les menaces les plus fréquentes auxquelles les entreprises sont confrontés aujourd'hui. Elles sont basées sur les opérations de sécurité et les équipes de réponse aux incidents, notamment celles qui permettent de défendre les ressources de Microsoft et de nos clients.

### <a name="security-playbooks-are-rolling-out-in-phases"></a>Les règles de sécurité sont déployées en plusieurs phases

Dans le cadre de l'AIR, les règles de sécurité sont déployées en phases.

- **Phase 1 (avril 2019)**: les règles incluent des recommandations pour les actions que les administrateurs de la sécurité examinent et approuvent. 

- **Phase 2 (juin 2019)**: les administrateurs de la sécurité auront la possibilité de configurer des règles de sécurité pour effectuer des actions automatiquement, sans interaction administrative.

La phase 1 inclut les règles suivantes:
- Message hameçon signalé par l'utilisateur
- URL cliquez sur modifier le verdict 
- Détection de programmes malveillants après la livraison (programmes malveillants ZAP)
- Hameçonnage détecté après la livraison ZAP (hameçon ZAP)
- Enquêtes manuelles par courrier électronique (à l'aide de l'Explorateur de menaces)

Plusieurs autres règles sont prévues pour la phase 2.

### <a name="playbooks-include-investigation-and-recommendations"></a>Les règles incluent une enquête et des recommandations

Chaque manuel inclut: 
- une enquête racine, 
- les étapes à suivre pour identifier et corréler les autres menaces potentielles, et 
- actions de correction des menaces recommandées.

Chaque étape de haut niveau inclut de nombreuses sous-étapes qui sont exécutées pour fournir une réponse approfondie, détaillée et exhaustive aux menaces.

## <a name="example-user-reported-phish-message"></a>Exemple: message hameçon signalé par l'utilisateur

Lorsqu'un utilisateur de votre organisation soumet un message électronique et le signale à Microsoft à l'aide du [complément de message de rapport pour Outlook ou Outlook Web Access](enable-the-report-message-add-in.md). Cela déclenche une alerte d'information basée sur le système qui lance automatiquement le manuel d'enquête.

Lors de la phase d'enquête de racine, différents aspects du courrier électronique sont évalués. Ces situations sont les suivantes :
- Détermination du type de menace susceptible de se présenter;
- Expéditeur;
- Emplacement d'envoi du courrier électronique (infrastructure émettrice);
- Si d'autres instances du courrier électronique ont été remises ou bloquées;
- Une évaluation de nos analystes;
- Si le courrier électronique est associé à des campagnes connues;
- et bien plus encore.

Une fois l'enquête terminée, le manuel fournit une liste d'actions recommandées à effectuer.
  
Ensuite, plusieurs étapes d'enquête sur les menaces et de chasse sont exécutées:

- Les messages électroniques similaires dans d'autres clusters de messagerie sont recherchés.
- Le signal est partagé avec d'autres plateformes, telles que [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).
- Une détermination est effectuée sur le fait que les utilisateurs aient cliqué sur les liens dans les messages électroniques suspects.
- Une vérification est effectuée dans Office 365 Exchange Online Protection ([EOP]) (EOP/Exchange-Online-Protection-EOP. MD) et Office 365 Advanced Therat protection ([ATP]) (Office-365-atp.md) pour voir s'il existe d'autres messages similaires signalés par les utilisateurs.
- Une vérification est exécutée pour déterminer si un utilisateur a été compromis. Cette vérification exploite les signaux de la sécurité de l' [application Cloud Microsoft](https://docs.microsoft.com/cloud-app-security) et d' [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), en mettant en corrélation les anomalies d'activité de l'utilisateur associées. 

Au cours de la phase de chasse, les risques et les menaces sont affectés à différentes étapes de la chasse.  

La correction est la phase finale du manuel. Pendant cette phase, les étapes de correction sont prises, en fonction des phases de theinvestigation et de chasse.  

## <a name="getting-started"></a>Prise en main

Pour accéder à vos enquêtes, en tant qu'administrateur général Office 365, administrateur de sécurité ou lecteur de sécurité, accédez au centre de sécurité & conformité[https://protection.office.com](https://protection.office.com)Office 365 () et connectez-vous. Effectuez ensuite l’une des opérations suivantes :

- Dans le volet de navigation de gauche, accédez à**recherches**de **gestion** > des menaces.

    ou

- Visitez le tableau de bord de gestion des menaces (dans le centre de sécurité & Compliance Center, accédez au**tableau de bord**de **gestion** > des menaces).

![Widgets d'AIR](media/air-widgets.png)

Vos widgets d'AIR s'affichent dans la partie supérieure du [tableau de bord de sécurité](security-dashboard.md). Sélectionnez un widget pour commencer.

Vous pouvez également accéder à une invesitgation directement à partir des alertes associées.

### <a name="automated-investigations"></a>Analyses automatisées

La page enquêtes automatiques indique les évaluations de votre organisation et leurs États actuels.

![Page d'enquête principale pour l'AIR](media/air-maininvestigationpage.png) 
  
Vous pouvez :
- Accédez directement à une enquête (sélectionnez un **ID d'enquête**).
- Appliquer des filtres. Choisissez entre **type**d'enquête ****, période, **État**ou une combinaison de ces éléments.
- ExPortez les données dans un fichier CSV.

### <a name="investigation-graph"></a>Graphique d'enquête

Lorsque vous ouvrez une enquête spécifique, vous voyez la page Graph de l'enquête. Cette page affiche toutes les entités différentes: les messages électroniques, les utilisateurs (ainsi que leurs activités) et les appareils qui ont été automatiquement analysés dans le cadre de l'alerte déclenchée.

![Page graphique d'enquête sur l'AIR](media/air-investigationgraphpage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle de l'enquête actuelle.
- Afficher un résumé du minutage de l'enquête.
- Sélectionnez un nœud dans la visualisation pour afficher les détails de ce nœud.
- Sélectionnez un onglet dans la partie supérieure pour afficher les détails de cet onglet.

### <a name="alert-investigation"></a>Enquête sur les alertes

Dans l'onglet **alertes** pour une enquête, vous pouvez voir des alertes relatives à l'enquête. Les détails incluent l'alerte qui a déclenché l'enquête et d'autres alertes, telles que la connexion à risque, le téléchargement en masse, etc., qui sont corrélées à l'enquête. À partir de cette page, un analyste de sécurité peut également afficher des détails supplémentaires sur des alertes individuelles.

![Page alertes AÉRIENNEs](media/air-investigationalertspage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle de l'alerte de déclenchement actuelle et de toutes les alertes associées.
- Sélectionnez une alerte dans la liste pour ouvrir une page de survol qui affiche les détails de l'alerte complète.

### <a name="email-investigation"></a>Enquête par courrier électronique

Dans l'onglet **e-mail** pour une enquête, vous pouvez voir tous les clusters de messagerie identifiés dans le cadre de l'enquête. 

Étant donné le volume de courrier électronique que les utilisateurs d'une organisation envoient et reçoivent, le processus de 
- mise en cluster de messages électroniques en fonction d'attributs similaires d'un en-tête, d'un corps, d'une URL et d'une pièce jointe de message; 
- séparation du courrier électronique malveillant du courrier électronique approprié; les 
- prendre des mesures sur les messages électroniques malveillants 

peut prendre plusieurs heures. AIR automatise ce processus en enregistrant le temps et les efforts de l'équipe de sécurité de votre organisation. 

À titre d'exemple, considérons le scénario suivant. Le premier cluster de trois messages électroniques était considéré comme un hameçonnage. Un autre cluster de messages similaires avec la même adresse IP et l'objet a été trouvé et considéré comme malveillant, car certains d'entre eux étaient identifiés comme des hameçons lors de la détection initiale. 

![Page d'enquête sur le courrier électronique aérien](media/air-investigationemailpage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des résultats de clustering actuels et des menaces détectées.
- Cliquez sur une entité de cluster ou une liste de menaces pour ouvrir une page de survol qui affiche les détails de l'alerte complète.

![Courrier électronique d'enquête aérienne avec détails du menu volant](media/air-investigationemailpageflyoutdetails.png)

* Remarque: dans le contexte de la messagerie électronique, vous pouvez voir une surface d'anomalie de volume dans le cadre de l'enquête. Une anomalie de volume indique un pic dans des courriers électroniques de même type pendant la durée de l'événement d'enquête par rapport aux délais précédents. Ce pic dans le trafic de messagerie avec des caractéristiques similaires (par exemple, domaine d'objet et de l'expéditeur, similitude entre le corps et IP de l'expéditeur) est typique du début des campagnes ou des attaques par courrier électronique. Toutefois, les campagnes de courrier électronique en bloc et SPOM partagent également ces caractéristiques. Les anomalies de volume représentent une menace potentielle et peuvent donc être moins sévères par rapport aux menaces de programmes malveillants ou hameçons identifiées à l'aide de moteurs antivirus, de détonation ou de réputation malveillante.

### <a name="user-investigation"></a>Enquête utilisateur

Sous l'onglet **utilisateurs** , vous pouvez voir tous les utilisateurs identifiés dans le cadre de l'enquête. 

Par exemple, dans l'image suivante, AIR a identifié des indicateurs de compromission et des anomalies en fonction d'une nouvelle règle de boîte de réception créée. Des détails supplémentaires (preuve) de l'enquête sont disponibles via des vues détaillées dans cet onglet. les indicateurs de compromis et d'anomalies peuvent également inclure des détections d'anomalies dans la [sécurité des applications Cloud de Microsoft](https://docs.microsoft.com/cloud-app-security).

![Page des utilisateurs de l'enquête aérienne](media/air-investigationuserspage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des résultats et des risques utilisateur identifiés.
- Sélectionnez un utilisateur pour ouvrir une page de survol qui affiche les détails de l'alerte complète.

### <a name="machine-investigation"></a>Enquête sur les machines

Sous l'onglet **ordinateurs** , vous pouvez voir tous les ordinateurs identifiés dans le cadre de l'enquête. 

![Page de l'ordinateur d'enquête aérien](media/air-investigationmachinepage.png)

Dans le cadre de l'enquête, AIR établit une corrélation entre les menaces de messagerie et les appareils. Par exemple, une enquête transmet un hachage de fichier à [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) pour enquêter. Cela permet l'analyse automatisée des ordinateurs pertinents pour vos utilisateurs et vous aide à vous assurer que les menaces sont résolues dans le Cloud et sur vos appareils. 

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des ordinateurs et menaces actuels détectés.
- Sélectionnez un ordinateur pour ouvrir une vue dans les [enquêtes Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection) associées dans le centre de sécurité Windows Defender ATP.

### <a name="entity-investigation"></a>Enquête d'entité

Sous l'onglet **entités** , vous pouvez voir tous les ordinateurs identifiés dans le cadre de l'enquête. 

Ici, vous pouvez voir les entités analysées. Vous pouvez afficher les détails des types d'entités, tels que les messages électroniques, les clusters, les adresses IP, les utilisateurs et bien plus encore. Vous pouvez également voir le nombre d'entités analysées et les menaces associées à chacune d'elles. 

![Page des entités d'enquête sur l'AIR](media/air-investigationentitiespage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des entités d'enquête et des menaces détectées.
- Sélectionnez une entité pour ouvrir une page de survol qui affiche le détail de l'entité associée.

![Détails des entités d'enquête aérienne](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>Journal des manifestes

Sous l'onglet **Journal** , vous pouvez voir toutes les étapes du manuel qui ont eu lieu lors de l'enquête. Le journal capture un inventaire complet de toutes les actions effectuées par les fonctionnalités d'enquête automatique d'Office 365 dans le cadre de l'AIR. Elle fournit une vue claire de toutes les étapes effectuées, y compris l'action elle-même, une description et la durée du début à la fin. 

![Page Journal d'enquête aérienne](media/air-investigationlogpage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des étapes du manuel.
- ExPortez les résultats dans un fichier CSV.
- Filtrer l'affichage.

### <a name="recommended-actions"></a>Actions recommandées

Sous l'onglet **actions** , vous pouvez voir toutes les actions de recherche qui sont recommandées pour la correction une fois l'enquête terminée. 

Actions Capturez les étapes que Microsoft vous recommande d'effectuer à la fin de l'enquête. Vous pouvez prendre des mesures de correction ici en sélectionnant une ou plusieurs actions. Si vous cliquez sur **approuver** , le début de la correction est autorisé. (Les autorisations appropriées seront requises. Par exemple, un lecteur de sécurité peut afficher les actions mais pas les approuver.)  

![Page action de l'enquête par avion](media/air-investigationactionspage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des actions recommandées.
- Sélectionnez une ou plusieurs actions.
- Approuver ou rejeter les actions recommandées avec les commentaires.
- ExPortez les résultats dans un fichier CSV.
- Filtrer l'affichage.

## <a name="how-to-get-air"></a>Comment obtenir de l'AIR

Actuellement, Office 365 AIR est en préversion. Office 365 AIR sera inclus dans les abonnements suivants:

- Microsoft 365 Entreprise E5
- Office 365 Entreprise E5
- Protection contre les menaces Microsoft
- Plan 2 de protection avancée contre les menaces Office 365

Pour en savoir plus sur la disponibilité des fonctionnalités, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).
