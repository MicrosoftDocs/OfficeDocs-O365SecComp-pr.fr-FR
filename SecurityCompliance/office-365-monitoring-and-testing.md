---
title: Analyse d’Office 365 et le test des limites du client
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Surveille les Résumé : Une explication de la façon de Microsoft et les tests des limites des clients pour Office 365.'
ms.openlocfilehash: 4d57c7497bfe8bf9939f3ae785ab9fbc670bd0ae
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527836"
---
# <a name="monitoring-and-testing-tenant-boundaries"></a>Surveillance et test des limites de client
Microsoft surveille en permanence et teste explicitement pour les points faibles et les vulnérabilités dans les limites du client, y compris la surveillance des intrusions, les tentatives de violation d’autorisation et insuffisance de ressources. Nous utilisons également plusieurs systèmes internes à analyser en continu pour l’utilisation des ressources inapproprié, qui dans ce cas, déclenche la limitation intégrés.

Office 365 offre des systèmes de surveillance internes qui en permanence surveiller pour une défaillance et la récupération automatique du lecteur lors de l’échec est détecté. Les systèmes Office 365 analyser les différences de comportement de service et lancer des processus de réparation automatique qui sont intégrés au système. Office 365 utilise également en dehors de surveillance dans lequel l’analyse est effectuée à partir de plusieurs emplacements à la fois des services de tiers approuvés (pour la vérification de SLA indépendante) et nos propres centres de données pour générer des alertes. Pour les diagnostics, nous avons journalisation complète, l’audit et suivi. Suivi précis et vous aide à isoler les problèmes et effectuer racine rapide et efficace de surveillance entraînent l’analyse.

Lorsque Office 365 a automatisé des actions de récupération si possible, ingénieurs d’appel Microsoft sont disponibles 24 x 7 à étudier toutes les procédures d’escalade sécurité gravité 1 et bilan passe en revue de chaque incident service contribue à la formation continue et amélioration du produit. Cette équipe comprend les techniciens du support technique, les développeurs de produits, responsables de programme, les responsables de produits et direction. Nos professionnels sur appel fournissent une sauvegarde en temps voulu et souvent peuvent automatiser les actions de récupération, afin que la prochaine fois que cet événement se produit un événement, il peut être automatique cicatrisée.

Microsoft effectue un examen approfondi de post-incident chaque fois qu’un incident de sécurité Office 365 se produit quel que soit l’ampleur de l’impact. Un examen après incident se compose d’une analyse des événements, comment nous a répondu et comment nous empêcher incidents similaires à l’avenir. Pour des raisons de transparence et la responsabilisation, nous partager révision post-incident pour les incidents principaux de service avec les clients concernés. Pour plus d’informations, voir [Gestion des incidents de sécurité Office 365](http://aka.ms/Office365SIM).

## <a name="assume-breach-methodology"></a>Supposons que la méthodologie de violation
En fonction de l’analyse détaillée des tendances de sécurité, Microsoft préconise et met en évidence la nécessité d’investissements supplémentaires de sécurité réactive processus et technologies qui se concentrer sur la détection et la réponse aux nouvelles menaces, plutôt qu’uniquement la prévention de ces menaces. En raison des modifications dans le paysage des menaces et l’analyse approfondie, Microsoft affiné sa stratégie de sécurité au-delà des violations de sécurité simplement empêcher un mieux est conçu pour gérer les problèmes liés aux violations de lorsqu’elles se produisent, une stratégie qui prend en compte ne principale pas les événements de sécurité en tant qu’if, mais lorsque.

Alors que les pratiques de [Supposent une violation](https://www.microsoft.com/en-us/TrustCenter/Security/default.aspx) de Microsoft ont été en place de nombreuses années, de nombreux clients ne savent pas le travail effectué en arrière-plan pour renforcer la sécurité du nuage de Microsoft. Supposons que violation est une approche qui guide les investissements de sécurité, les décisions de conception et les pratiques de sécurité opérationnelle. Supposons limites violation l’approbation placée dans les applications, les services, les identités et les réseaux par traiter tous les — internes et externes, comme non sécurisés et déjà compromis. Bien que la stratégie supposent une violation a été pas pris en charge à partir d’une violation effective de tous les services Microsoft enterprise ou dans le cloud, il était une que bon nombre d’organisations, dans l’industrie, était en cours compromise en dépit de toutes les tentatives d’empêcher la reconnaissance. Lorsque la prévention des violations est un rôle essentiel des opérations d’une organisation, ces pratiques doivent être en permanence testées et augmentés pour relever adversaires modernes et avancées permanentes contre les menaces. Pour une organisation préparer une violation, ils doivent tout d’abord créer et maintenir des procédures de réponse de sécurité fiable, reproductible et minutieusement testé.

Pendant le processus de sécurité empêcher une violation, tels que de la modélisation des menaces, les révisions de code et les tests de sécurité sont très utiles dans le cadre du cycle de [Vie de développement de sécurité](http://www.microsoft.com/security/sdl/default.aspx), violation supposent fournit les nombreux avantages permettant de compte pour la sécurité globale par exercice et fonctionnalités réactives en cas de violation de mesure.

Chez Microsoft, nous définissons la sortie pour ce faire, en cours war-games exercices et le site actif simulations de nos plans de réponse de sécurité dans le but d’améliorer notre capacité de détection et de réponse. Microsoft simule les violations concrètes régulièrement, possède une surveillance continue de la sécurité et la gestion des incidents sécurité pratiques pour valider et améliorer la sécurité d’Office 365 et autres services de cloud Microsoft Azure.

Microsoft exécute sa stratégie de sécurité violation supposent que l’aide de deux principaux groupes :
- Équipes rouge (pirates)
- Équipes bleus (défenses)

Microsoft Azure et Office 365 personnel séparez des équipes rouge à plein temps et des équipes bleus.

Dénommé «[Agrégation rouge](http://go.microsoft.com/fwlink/?linkid=518599)», l’approche est pour tester les systèmes Azure et Office 365 et les opérations à l’aide de la même tactiques, techniques et des procédures comme adversaires réels, par rapport à l’infrastructure d’environnement de production, sans la connaissance préalable du Ingénierie ou les équipes opérationnelles. Cette commande teste la détection de la sécurité et les capacités de réponse de Microsoft, et permet d’identifier les vulnérabilités de production, les erreurs de configuration, hypothèses non valides et autres problèmes de sécurité de manière contrôlée. Violation de chaque équipe rouge est suivie de divulgation complète entre les deux équipes pour identifier les lacunes, résoudre les résultats et améliorer violation de la réponse.

**Remarque**: aucune donnée client délibérément ne ciblée au cours de collaboration rouge ou simulations de site actif. Les tests sont par rapport à l’infrastructure d’Office 365 et Azure et plateformes, ainsi que de Microsoft clients, des applications et données. Les clients de client, des applications et le contenu hébergé dans Office 365 ou Azure jamais ciblés.

## <a name="red-teams"></a>Équipes rouge
L’équipe rouge est un groupe de personnel à temps plein au sein de Microsoft qui se concentre sur l’infrastructure de Microsoft violation, plateforme et clients de Microsoft et applications. Ils sont l’adversaire dédié (un groupe de pirates éthiques) effectue les attaques ciblées et permanentes par rapport à des Services en ligne (infrastructure Microsoft, plates-formes et applications mais pas fin clients applications ou du contenu).

Le rôle de l’équipe rouge consiste à attaquer et traverser les environnements à l’aide de la même procédure comme un adversaire :
 
![Étapes de violation](media/office-365-isolation-breach-stages.png)

Parmi d’autres fonctions, les équipes rouge tentent spécifiquement violer des limites d’isolation de client pour trouver des bogues ou des espaces dans notre conception d’isolation.

## <a name="blue-teams"></a>Équipes bleus
L’équipe blue est composé de soit un ensemble dédié de répondeurs de sécurité ou des membres dans la réponse aux incidents de sécurité, d’ingénierie et opérations organisations. Quelle que soit leur tri, ils sont indépendants et gérée séparément à partir de l’équipe de rouge. L’équipe blue suit établie sécurité traite et utilise les outils et les technologies les plus récents pour détecter et répondre aux attaques et intrusions. À l’instar des attaques du monde réel, l’équipe blue ne sait pas quand et comment les attaques de l’équipe rouge seront produit ou les méthodes peuvent être utilisées. Leur travail, qu’il s’agisse d’une attaque de l’équipe rouge ou d’une attaque réelle, consiste à détecter et répondre à tous les incidents de sécurité. Pour cette raison, l’équipe blue sur appel en continu et doit réagir violations de l’équipe rouge la même manière qu’ils le feriez pour toute autre violation.

Lorsqu’un adversaire, par exemple une équipe rouge, a franchi un environnement, l’équipe blue doit :
- Recueillir les preuves laissées par l’adversaire
- Détecter les signes comme une indication de compromis
- Les équipes Engineering et le fonctionnement appropriés d’alerte
- Triez les alertes pour déterminer si elles nécessitent une étude approfondie
- Recueillir contexte de l’environnement à la violation d’étendue
- Un plan de mise à jour pour contenir ou supprimer l’adversaire de formulaire
- Exécuter le plan de mise à jour et récupérer à partir de violation

Ces étapes écran incidents de sécurité qui s’exécute en parallèle à l’adversaire, comme indiqué ci-dessous :
 
![Étapes de réponse violation](media/office-365-isolation-breach-response-stages.png)

Autorisent les violations de l’équipe rouge de la capacité de l’équipe blue pour détecter et répondre aux attaques concrètes au bout en bout. Plus important, il permet d’incidents de sécurité pratiques avant une violation authentique. En outre, en raison de violations de l’équipe rouge, l’équipe blue améliore leur connaissance de la situation qui peut être utile lorsque vous travaillez avec des violations futures (que ce soit à partir de l’équipe rouge ou un autre adversaire). Tout au long de la détection et le processus de réponse, l’équipe blue produit intelligents et gains de visibilité sur les conditions réelles du ou les milieux qu’ils tentent de protéger. Cette opération s’effectue souvent via l’analyse des données et investigation, effectuée par l’équipe blue, lors de la réponse aux attaques de l’équipe rouge et en créant des indicateurs de menace, telles que les indicateurs de compromis. Beaucoup comme comment l’équipe rouge identifie des intervalles dans l’article de la sécurité, des équipes bleus identifient les lacunes dans capables de détecter et y répondre. En outre, étant donné que les équipes rouge concrètes attaques du modèle, l’équipe blue peut être évaluée avec précision sur leur capacité ou incapacité, faire des adversaires déterminés et permanentes. Enfin, violations de l’équipe rouge mesurent la préparation et l’impact de notre réponse violation.
