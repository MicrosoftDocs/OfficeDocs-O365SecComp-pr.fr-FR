---
title: Recherche et réponse automatisées (AIR) avec Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Découvrez les fonctionnalités d'analyse et de réponse automatisées dans Office 365 Advanced Threat Protection.
ms.openlocfilehash: c2d5acd0bf26dc28b30f26488adf47de2c834fb6
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30736301"
---
# <a name="automated-investigation-and-response-air-with-office-365-threat-intelligence"></a>Recherche et réponse automatisées (AIR) avec Office 365 Threat Intelligence

AutoMated Investigation and Response (AIR) (bientôt disponible pour les [fonctionnalités d'enquête et de réponse aux menaces Office 365](office-365-ti.md)) vous permet d'effectuer des recherches et des corrections automatiques sur des menaces connues qui existent aujourd'hui. Lisez cet article pour obtenir une vue d'ensemble de l'AIR et la façon dont il peut aider votre organisation à réduire les menaces de manière plus efficace. Tolearn en savoir plus sur la disponibilité de l'AIR, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).

## <a name="alerts"></a>Alertes

Les [alertes](alert-policies.md#viewing-alerts) représentent des déclencheurs pour les flux de travail d'équipe des opérations de sécurité pour la réponse aux incidents. La définition de la priorité des alertes à droite pour l'enquête tout en s'assurant qu'aucune menace n'est sans adresse est complexe. Lorsque les enquêtes dans les alertes sont effectuées manuellement, les équipes des opérations de sécurité doivent rechercher et corréler les entités (par exemple, le contenu, les appareils et les utilisateurs) menacées. Ces tâches et les flux de travail sont très longs et impliquent plusieurs outils et systèmes. Avec AIR, l'analyse et la réponse sont automatisées dans les alertes de gestion de la sécurité et des menaces clés qui déclenchent automatiquement vos règles de réponse de sécurité. 

pour afficher les alertes, dans le centre de sécurité & de sécurité Office 365, sélectionnez **alertes** > **afficher les alertes**.

![Alertes liées à des enquêtes](media/air-alerts-page-details.png) 

Sélectionnez une alerte pour afficher ses détails, puis, à partir de là, utilisez le lien **consulter l'enquête** pour accéder à l' [enquête](#investigation-graph)correspondante.

## <a name="security-playbooks"></a>Règles de sécurité

Les règles de sécurité sont des stratégies principales qui sont au cœur de l'automatisation dans la protection contre les menaces Microsoft. Les règles de sécurité fournies dans AIR sont basées sur des scénarios de sécurité réels courants. Un manuel de sécurité est lancé automatiquement lorsqu'une alerte est déclenchée au sein de votre organisation. Une fois que l'alerte est déclenchée, le manuel associé est exécuté automatiquement. Le manuel exécute une enquête, en examinant toutes les métadonnées associées (y compris les messages électroniques, les utilisateurs, les objets, les expéditeurs, etc.) et, en fonction de ses conclusions, recommande une série d'actions que l'équipe de sécurité de votre organisation peut prendre pour contrôler et atténuer la menace. 

Les règles de sécurité que vous obtenez avec AIR sont conçues pour aborder les menaces les plus fréquentes auxquelles les entreprises sont confrontés aujourd'hui. Elles sont basées sur les opérations de sécurité et les équipes de réponse aux incidents, notamment celles qui permettent de défendre les biens Microsoft.

### <a name="security-playbooks-are-rolling-out-in-phases"></a>Les règles de sécurité sont déployées en plusieurs phases

Dans le cadre de l'AIR, les règles de sécurité sont déployées en phases.

- **Phase 1 (avril 2019)**: les règles incluent des recommandations que les administrateurs de la sécurité examinent et approuvent. 

- **Phase 2 (juin 2019)**: les administrateurs de la sécurité auront la possibilité d'autoriser les règles de sécurité à agir automatiquement, sans interaction administrative.

La phase 1 inclut les règles suivantes:
- Message hameçon signalé par l'utilisateur
- URL cliquez sur modifier le verdict et remplacer le bloc liens de sécurité ATP
- Programme malveillant ZAP
- Hameçon ZAP
- Analyses manuelles (à l'aide de l'Explorateur)

Plusieurs autres règles sont prévues pour la phase 2.

### <a name="playbooks-include-investigation-and-recommendations"></a>Les règles incluent une enquête et des recommandations

Chaque manuel inclut: 
- une enquête racine, 
- étapes de la recherche d'autres menaces potentielles et 
- correction des menaces recommandées.

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
  
Ensuite, plusieurs étapes de la chasse sont exécutées:

- Les messages électroniques similaires dans d'autres clusters de messagerie sont recherchés.
- Le signal est partagé avec d'autres plateformes, telles que [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).
- Une détermination est effectuée sur le fait que les utilisateurs aient cliqué sur le message suspect.
- Une vérification est effectuée dans Office 365 [EOP](eop/exchange-online-protection-eop.md) et [](office-365-atp.md) la protection avancée contre les menaces pour voir s'il existe d'autres messages similaires signalés par les utilisateurs.
- Une vérification est exécutée pour déterminer si un utilisateur a été compromis. Cette vérification s'appuie sur les signaux de la sécurité de l' [application Cloud Microsoft](https://docs.microsoft.com/cloud-app-security) et d' [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), ce qui met en corrélation les événements ou alertes connexes. 

Au cours de la phase de chasse, les risques et les menaces sont affectés à différentes étapes de la chasse.  

La correction est la phase finale du manuel. Pendant cette phase, les étapes de correction sont prises, en fonction des phases de theinvestigation et de chasse.  

## <a name="getting-started"></a>Prise en main

Pour accéder à vos enquêtes, en tant qu'administrateur général ou administrateur de sécurité Office 365, accédez au centre de sécurité & conformité[https://protection.office.com](https://protection.office.com)Office 365 () et connectez-vous. Effectuez ensuite l’une des opérations suivantes :

- Dans le volet de navigation de gauche, accédez à**recherches**de **gestion** > des menaces.

    ou

- Visitez le tableau de bord de gestion des menaces (dans le centre de sécurité & Compliance Center, accédez au**tableau de bord**de **gestion** > des menaces).

![Widgets d'AIR](media/air-widgets.png)

Vos widgets d'AIR s'affichent dans la partie supérieure du [tableau de bord de sécurité](security-dashboard.md). Sélectionnez un widget pour commencer.

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

Dans l'onglet **alertes** pour une enquête, vous pouvez voir toutes les alertes relatives à l'enquête. Les détails incluent l'alerte qui a déclenché l'enquête et d'autres alertes, telles que la connexion à risque, le téléchargement en masse, etc., qui sont corrélées à l'enquête. À partir de cette page, un analyste de sécurité peut également afficher des détails supplémentaires sur des alertes individuelles.

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

À titre d'exemple, considérez l'image suivante. Le premier cluster de trois messages électroniques était considéré comme un hameçonnage. Un autre cluster de messages similaires avec le même IP et le même objet a été trouvé et considéré comme malveillant, car certains d'entre eux ont été identifiés comme des hameçons lors de la détection initiale. 

![Page d'enquête sur le courrier électronique aérien](media/air-investigationemailpage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des résultats de clustering actuels et des menaces détectées.
- Cliquez sur une entité de cluster ou une liste de menaces pour ouvrir une page de survol qui affiche les détails de l'alerte complète.

![Courrier électronique d'enquête aérienne avec détails du menu volant](media/air-investigationemailpageflyoutdetails.png)

### <a name="user-investigation"></a>Enquête utilisateur

Sous l'onglet **utilisateurs** , vous pouvez voir tous les utilisateurs identifiés dans le cadre de l'enquête. 

Par exemple, dans l'image suivante, AIR a identifié des indicateurs de compromission et des anomalies en fonction d'une nouvelle règle de boîte de réception créée. Des détails supplémentaires (preuve) de l'enquête sont disponibles par le biais d'affichages détaillés au sein de cet onglet.

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
- Sélectionnez un ordinateur pour ouvrir une vue dans les [recherches Windows Defender](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection)connexes connexes.

### <a name="entity-investigation"></a>Enquête d'entité

Sous l'onglet **entités** , vous pouvez voir tous les ordinateurs identifiés dans le cadre de l'enquête. 

Ici, vous pouvez voir les entités analysées. Vous pouvez afficher les détails des types d'entités, tels que les messages électroniques, les clusters, les adresses IP, les utilisateurs et bien plus encore. Vous pouvez également voir le nombre d'entités analysées et les menaces associées à chacune d'elles. 

![Page des entités d'enquête sur l'AIR](media/air-investigationentitiespage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des entités d'enquête et des menaces détectées.
- Sélectionnez une entité pour ouvrir une page de survol qui affiche le détail de l'entité associée.

![Détails des entités d'enquête aérienne](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>Journal des manifestes

Sous l'onglet **Journal** , vous pouvez voir toutes les étapes du manuel qui ont eu lieu lors de l'enquête. Le journal capture un inventaire complet de toutes les actions effectuées par les fonctionnalités d'aide à la décision Office 365 dans le cadre de l'AIR. Elle fournit une vue claire de toutes les étapes effectuées, y compris l'action elle-même, une description et la durée du début à la fin. 

![Page Journal d'enquête aérienne](media/air-investigationlogpage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des étapes du manuel.
- ExPortez les résultats dans un fichier CSV.
- Filtrer l'affichage.

### <a name="recommended-actions"></a>Actions recommandées

Sous l'onglet **actions** , vous pouvez voir toutes les actions de recherche qui sont recommandées pour la correction une fois l'enquête terminée. 

Actions capturez la liste complète de toutes les étapes que Microsoft vous recommande d'effectuer à la fin de l'enquête. Vous pouvez prendre des mesures de correction ici en sélectionnant une ou plusieurs actions. Si vous cliquez sur **approuver** , le début de la correction est autorisé. (Des autorisations appropriées peuvent être requises. Par exemple, un lecteur de sécurité peut afficher les actions mais pas les approuver.)  

![Page action de l'enquête par avion](media/air-investigationactionspage.png)

Vous pouvez :
- Obtenir une vue d'ensemble visuelle des actions recommandées.
- Sélectionnez une ou plusieurs actions.
- Approuver les actions recommandées. (Ceux-ci sont démarrés immédiatement avec les commentaires.)
- ExPortez les résultats dans un fichier CSV.
- Filtrer l'affichage.

## <a name="how-to-get-air"></a>Comment obtenir de l'AIR

Actuellement, AIR est en préversion. Une fois diffusé, AIR est inclus dans les abonnements suivants:

- Microsoft 365 Entreprise E5
- Office 365 Entreprise E5
- Protection contre les menaces Microsoft
- Plan 2 de protection avancée contre les menaces Office 365

Pour en savoir plus sur la disponibilité des fonctionnalités, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).
