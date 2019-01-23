---
title: Stratégies de sécurité Office 365 d’alerte &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 8927b8b9-c5bc-45a8-a9f9-96c732e58264
description: Créer des stratégies de l’alerte de sécurité Office 365 &amp; centre de conformité à surveiller les menaces potentielles, la perte de données et problème d’autorisations. Ensuite, vous pouvez afficher et gérer les alertes sont générées lorsque les utilisateurs effectuent des activités qui correspondent aux conditions d’une stratégie de l’alerte.
ms.openlocfilehash: 28ea842c74f2d3d232218e582d3de31f3841284e
ms.sourcegitcommit: a1d8174240eb88b51af3a1ba26d715292fe08c53
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "29426029"
---
# <a name="alert-policies-in-the-office-365-security-amp-compliance-center"></a>Stratégies de sécurité Office 365 d’alerte &amp; centre de conformité

Vous pouvez utiliser la nouvelle stratégie de l’alerte et outils de tableau de bord de l’alerte de sécurité Office 365 &amp; centre de conformité pour créer des stratégies de l’alerte et puis afficher les alertes sont générées lorsque les utilisateurs effectuent des activités qui correspondent aux conditions d’une stratégie de l’alerte. Alerte de stratégies de créer et d’étendre les fonctionnalités d’alertes de l’activité en vous permettant de classer la stratégie de l’alerte, appliquer la stratégie à tous les utilisateurs de votre organisation, définir un seuil de déclenche d’une alerte et décider s’il faut recevoir du courrier électronique notifications. Il existe également une page **Afficher les alertes** de sécurité &amp; centre de conformité où vous pouvez afficher et filtrer des alertes, des alertes définir un état d’alerte pour vous aider à gérer les alertes, puis faire disparaître une fois que vous avez résolu ou résolu l’incident sous-jacent. Nous avons également étendu le type d’événements que vous pouvez créer des alertes pour. Par exemple, vous pouvez créer des stratégies de l’alerte pour effectuer le suivi des incidents de perte de données et de l’activité de programmes malveillants. Enfin, nous avons également inclus un certain nombre de stratégies de l’alerte par défaut qui vous permettent de surveiller l’attribution de privilèges d’administrateur dans Exchange Online, les attaques de programmes malveillants et les niveaux inhabituelles de suppressions de fichiers et de partage externe. 
  
> [!NOTE]
> Stratégies de l’alerte sont disponibles pour les organisations possédant un Office 365 pour entreprises ou Office 365 nous gouvernement E1/G1, E3/G3 ou abonnement E5/G5. Toutefois, certaines fonctionnalités avancées sont uniquement disponible pour les organisations avec un abonnement E5/G5, ou pour les organisations qui ont un E1/G1 ou abonnement E3/G3 et un abonnement à Office 365 menaces ou Office 365 avancées module complémentaire. La fonctionnalité qui requiert un abonnement E5/G5 ou un module complémentaire est mise en surbrillance dans cette rubrique. Notez également que les stratégies de l’alerte sont disponibles dans Office 365 GCC GCC haute et environnements DoD US.
  
## <a name="how-alert-policies-work"></a>Comment l’alerte travail stratégies

Voici une vue d’ensemble rapide de travail de stratégies comment l’alerte et les alertes qui sont des déclencheurs lors de l’activité utilisateur ou un administrateur correspondent aux conditions d’une stratégie de l’alerte.
  
![Vue d’ensemble du travail de stratégies comment l’alerte](media/e02a622d-b429-448b-8107-dd1a4770b4e0.png)
  
1. Un administrateur de votre organisation crée, configure et Active une stratégie de l’alerte à l’aide de la page de **stratégies de l’alerte** dans le centre de conformité de & sécurité. Vous pouvez également créer des stratégies des alertes à l’aide de l’applet de commande **New-ProtectionAlert** dans PowerShell. Pour créer des stratégies de l’alerte, vous devez affecter le rôle de gestion des alertes dans le centre de conformité de & sécurité ou de la Configuration de l’organisation.
    
2. Un utilisateur effectue une activité qui correspond aux conditions d’une stratégie de l’alerte. Dans le cas des attaques de programmes malveillants, messages électroniques infectés envoyés aux utilisateurs de votre organisation déclenche une alerte.
    
3. Office 365 génère une alerte qui s’affiche dans la page **Afficher les alertes** de sécurité &amp; centre de conformité. En outre, si les notifications par courrier électronique sont activées pour la stratégie de l’alerte, Office 365 envoie une notification à une liste de destinataires. Les alertes que l’administrateur ou autres utilisateurs peuvent voir dans la page **Afficher les alertes** est déterminée par les rôles attribués à l’utilisateur. Pour plus d’informations, consultez la section [autorisations RBAC requises pour afficher les alertes](#rbac-permissions-required-to-view-alerts) .
    
4. Un administrateur qui gère les alertes de sécurité &amp; centre de conformité. Gestion des alertes se compose de l’affectation d’un état d’alerte pour aider à suivre et gérer toute enquête.
    

  
## <a name="alert-policy-settings"></a>Paramètres de stratégie de l’alerte

Une stratégie d’alerte se compose d’un ensemble de règles et conditions qui définissent les activités d’administration qui génèrent une alerte, une liste d’utilisateurs qui déclenchera l’alerte exercez l’activité, et seuil qui définit la fréquence à laquelle l’activité doit se produire avant un alerte n est déclenchée. Classer la stratégie de vous assigner un niveau de gravité. Ces deux paramètres permettent de gérer les stratégies des alertes (et les alertes qui sont déclenchées lorsque les conditions de stratégie sont mis en correspondance), car vous pouvez filtrer ces paramètres lors de la gestion des stratégies et affichage des alertes de sécurité &amp; centre de conformité. Par exemple, vous pouvez afficher les alertes qui correspondent aux conditions de la même catégorie ou afficher les alertes avec le même niveau de gravité.
  
Pour afficher et créer des stratégies de l’alerte, accédez à des **alertes** \> **stratégies des alertes** de sécurité &amp; centre de conformité. 
  
![Dans la sécurité &amp; Complinace centre de solutions, cliquez sur alertes, puis cliquez sur alerte stratégies pour afficher et créer des stratégies d’alerte](media/09ebd451-8e84-44e1-aefc-63e70bba4d97.png)
  
Une stratégie d’alerte comprend les conditions et les paramètres suivants.
  
- **Effectue le suivi des activités de l’alerte** : vous créez une stratégie pour effectuer le suivi d’une activité ou dans certains cas, quelques activités associées, tel un partage un fichier avec un utilisateur externe par le partage, l’affectation des autorisations d’accès ou création d’un lien anonyme. Lorsqu’un utilisateur effectue l’activité définie par la stratégie, une alerte est déclenchée en fonction des paramètres de seuil d’alerte.
    
    > [!NOTE]
    > Les activités que vous pouvez suivre dépendent de votre organisation Office 365 pour entreprises ou Office 365 nous pour le plan. En règle générale, les activités relatives aux campagnes de programmes malveillants et attaques par hameçonnage nécessitent un abonnement E5/G5 ou un abonnement/G1 E1 ou E3/G3 avec un abonnement à un module complémentaire sur les menaces. 
  
- **Conditions d’activité** - pour la plupart des activités, vous pouvez définir des conditions supplémentaires qui doivent être remplies pour une alerte doit être déclenchée. Conditions courantes incluent IP addresses (de sorte qu’une alerte est déclenchée lorsque l’utilisateur effectue l’activité sur un ordinateur avec une adresse IP spécifique ou au sein d’une plage d’adresses IP), si une alerte est déclenchée si un ou plusieurs utilisateurs effectuer cette activité et, si l’activité est effectuée sur une URL ou le nom de fichier spécifique. Vous pouvez également configurer une condition qui déclenche une alerte lorsque l’activité est effectuée par les utilisateurs dans votre organisation. Notez que les conditions disponibles dépendent de l’activité sélectionnée.
    
- **Lors du déclenche de l’alerte** - vous pouvez configurer un paramètre qui définit la fréquence à laquelle une activité peut se produire avant le déclenche d’une alerte. Permet de définir une stratégie pour générer une alerte chaque fois qu’une activité remplit les conditions de la stratégie, lorsqu’un certain seuil est dépassé, ou lorsque l’occurrence de l’activité de que l’alerte effectue le suivi est inhabituelle de votre organisation. 
    
    ![Configurer la façon dont les alertes sont déclenchées, en fonction quand l’activité se produit, un seuil ou une activité inhabituelle pour votre organisation](media/97ee1ed2-e7a9-47a2-a980-5f9f63872c65.png)
  
    Si vous sélectionnez le paramètre basé sur l’activité inhabituelle, Office 365 établit une valeur de base qui définit la fréquence normale pour l’activité sélectionnée ; nécessaire pour établir une relation de cette ligne de base, au cours de laquelle des alertes ne sont pas générées jusqu'à sept jours. Une fois établie la ligne de base, une alerte sera déclenchée lorsque la fréquence de l’activité de suivi de la stratégie de l’alerte considérablement dépasse la valeur de la ligne de base. Pour les activités liées aux audit (par exemple, les activités de fichiers et de dossiers), vous pouvez définir une planification basée sur un seul utilisateur ou sur tous les utilisateurs de votre organisation ; pour les activités liées aux programmes malveillants, vous pouvez établir une planification basée sur une famille de programmes malveillants unique, un seul destinataire ou tous les messages dans votre organisation.
    
    > [!NOTE]
    > La possibilité de configurer alerte stratégies basée sur un seuil ou sur une activité inhabituelle requiert un abonnement E5/G5, un/G1 E1 ou E3/G3 abonnement avec une aide à la décision Threat ou abonnement de module complémentaire de conformité avancées. Les organisations avec un abonnement E1/G1 et E3/G3 peuvent uniquement créer une stratégie d’alerte où une alerte est déclenchée chaque fois que cet événement se produit une activité. 
  
- **Catégorie d’alerte** - pour aider à suivre et à gérer les alertes générées par une stratégie, vous pouvez attribuer une des catégories suivantes à une stratégie.
    
  - Gouvernance des données
    
  - Protection contre la perte de données

  - Flux de messagerie
    
  - Autorisations
    
  - Gestion des menaces
    
  - Autres
    
  Lorsqu’une activité se produit qui correspond aux conditions de la stratégie de l’alerte, l’alerte qui est généré est marqué avec la catégorie définie dans ce paramètre. Cela vous permet de suivre et gérer les alertes qui ont la même catégorie définition dans la page **Afficher les alertes** dans le centre de conformité de & sécurité car vous pouvez trier et filtrer les alertes selon la catégorie. 
    
- **Gravité d’alerte** : similaire à la catégorie de l’alerte, vous assignez un attribut severity ( **faible**, **moyen**ou **élevé**) à des stratégies de l’alerte. Comme la catégorie de l’alerte, lorsqu’une activité se produit qui correspond aux conditions de la stratégie de l’alerte, l’alerte qui est généré est marqué avec le même niveau de gravité est défini pour la stratégie de l’alerte. Là encore, cela vous permet suivre et gérer les alertes qui ont le même paramètre gravité sur la page **Afficher les alertes** . Par exemple, vous pouvez filtrer la liste des alertes afin que seules les alertes de gravité **élevée** soient affichées. 
    
    > [!TIP]
    > Lorsque vous configurez une stratégie de l’alerte, envisagez l’affectation d’un niveau de gravité supérieure aux activités peuvent avoir des conséquences sérieusement négatifs, telles que la détection de programmes malveillants après remise aux utilisateurs, affichage des données sensibles ou confidentielles, partage de données avec des utilisateurs externes, ou d’autres activités qui peuvent entraîner des menaces de sécurité ou de perte de données. Vous pouvez définir la priorité des alertes et les actions à étudier et à résoudre les causes sous-jacentes. 
  
- **Notifications par courrier électronique** : vous pouvez configurer la stratégie de sorte que les notifications par courrier électronique sont envoyées (ou pas envoyées) à une liste d’utilisateurs lorsqu’une alerte est déclenchée. Vous pouvez également définir une limite quotidienne de notification afin qu’une fois que le nombre maximal de notifications a été atteinte, aucuns plus de notifications ne sont envoyées pour l’alerte pendant ce jour. Dans supplémentaires aux notifications, des messages, les autres administrateurs peuvent afficher les alertes qui sont déclenchées par une stratégie dans la page **Afficher les alertes** . Envisagez d’activer les notifications par courrier électronique pour les stratégies de l’alerte d’une catégorie spécifique ou qui ont un paramètre de gravité supérieure. 
  
## <a name="default-alert-policies"></a>Stratégies d’alerte par défaut

Office 365 fournit les stratégies de l’alerte intégrés qui permettent d’identifier l’abus d’autorisations Exchange admin, activité de programmes malveillants et les risques de la gouvernance de données. Dans la page **stratégies des alertes** , le nom de ces stratégies intégrées sont en gras et le type de stratégie est défini en tant que **système**. Ces stratégies sont activées par défaut. Vous pouvez désactiver ces stratégies (ou reconnecter), configurez une liste de destinataires pour envoyer des notifications par courrier électronique à et définir une limite quotidienne de notification. Les autres paramètres de ces stratégies ne peuvent pas être modifiés.
  
Le tableau suivant répertorie et décrit les règles d’alerte par défaut disponibles et indique les plans Office 365 pour entreprises et Office 365 américains requis pour chacun d’eux. Notez que certaines stratégies d’alerte par défaut ne sont disponibles que si votre organisation dispose de l’abonnement au module complémentaire appropriée en plus d’un abonnement/G1 E1 ou E3/G3. 
  
|**Stratégie de l’alerte par défaut**|**Description**|**Abonnement à Office 365 entreprise**|
|:-----|:-----|:-----|
|**Création de règles de transfert/redirection** <br/> |Génère une alerte lorsqu’une personne de votre organisation crée une règle de boîte de réception pour leur boîte aux lettres qui transfère ou redirige les messages vers un autre compte de messagerie. Cette stratégie suit uniquement les règles de boîte de réception sont créés à l’aide d’Outlook Web App ou Exchange Online PowerShell. Cette stratégie possède un paramètre de niveau de gravité **faible** . Pour plus d’informations à l’aide de règles de boîte de réception pour transférer et rediriger les messages électroniques dans Outlook Web App, voir [utiliser les règles dans Outlook Web App pour transférer automatiquement les messages vers un autre compte](https://support.office.com/article/1433e3a0-7fb0-4999-b536-50e05cb67fed).<br/> |/ G1 E1, E3/G3 ou E5/G5  <br/> |
|**recherche de découverte électronique démarré ou exportés** <br/> |Génère une alerte lorsqu’une personne utilise l’outil de recherche de contenu dans le centre de conformité de & sécurité. Une alerte est déclenchée lorsque les activités de recherche de contenu suivantes sont effectuées :<br/><br/>• Une recherche de contenu est démarré.<br/>• Les résultats d’une recherche de contenu sont exportées.<br/>• Exportation d’un rapport de recherche de contenu<br/><br/>Alertes sont déclenchées également lorsque les activités de recherche de contenu précédente sont effectuées en association avec un cas eDiscovery. Cette stratégie possède un paramètre de gravité **moyenne** . Pour plus d’informations sur les activités de recherche de contenu, voir [recherche d’activités de découverte électronique dans Office 365 journal d’audit](search-for-ediscovery-activities-in-the-audit-log.md#ediscovery-activities).<br/> |/ G1 E1, E3/G3 ou E5/G5  <br/> |
|**Élévation de privilèges d’administrateur Exchange** <br/> |Génère une alerte lorsqu’une personne est attribuée des autorisations d’administration dans votre organisation Exchange Online ; par exemple, si un utilisateur est ajouté au rôle de gestion de l’organisation de groupe dans Exchange Online. Cette stratégie possède un paramètre de niveau de gravité **faible** .<br/> |/ G1 E1, E3/G3 ou E5/G5  <br/> |
|**Les messages qui ont été retardées** <br/> |Génère une alerte lorsque Office 365 ne peut pas remettre les messages électroniques à votre organisation locale ou à un partenaire de serveurs à l’aide d’un connecteur. Lorsque cela se produit, le message est en file d’attente dans Office 365. Cette alerte se déclenche quand il y a 2 000 messages ou plus qui ont été mis en attente pour plus d’une heure. Cette stratégie possède un paramètre de gravité **élevée** .<br/> |/ G1 E1, E3/G3 ou E5/G5  <br/> |
|**Campagne de programme malveillant détecté après la remise** <br/> |Génère une alerte lorsqu’un nombre excessif de messages contenant des programmes malveillants est remis aux boîtes aux lettres dans votre organisation. Si cet événement se produit, Office 365 supprime les messages infectés de boîtes aux lettres Exchange Online. Cette stratégie possède un paramètre de gravité **élevée** .<br/> |Abonnement de module complémentaire E5/G5 ou menaces Office 365  <br/> |
|**Campagne de programme malveillant détecté et bloqué** <br/> |Génère une alerte lorsqu’une personne a tenté d’envoyer un nombre excessif de messages électroniques contenant un certain type de programmes malveillants pour les utilisateurs de votre organisation. Si cet événement se produit, les messages infectés sont bloquées par Office 365 et non remis aux boîtes aux lettres. Cette stratégie possède un paramètre de niveau de gravité **faible** .<br/> |Abonnement de module complémentaire E5/G5 ou menaces Office 365  <br/> |
|**Campagne de programme malveillant détecté dans SharePoint et OneDrive** <br/> |Génère une alerte lorsqu’un volume anormalement élevé de programmes malveillants ou de virus détectés dans les fichiers situés dans des sites SharePoint ou de comptes OneDrive dans votre organisation. Cette stratégie possède un paramètre de gravité **élevée** .<br/> |Abonnement de module complémentaire E5/G5 ou menaces Office 365  <br/> |
|**Activité du fichier d’utilisateurs externes inhabituelle** <br/> |Génère une alerte lorsqu’un nombre élevé généralement des activités est effectué sur des fichiers dans SharePoint ou OneDrive par les utilisateurs extérieurs à votre organisation. Cela inclut les activités telles que l’accès aux fichiers de téléchargement de fichiers et suppression des fichiers. Cette stratégie possède un paramètre de gravité **élevée** .<br/> |E5/G5 ou abonnement de module complémentaire Office 365 menaces ou de conformité avancées  <br/> |
|**Volume inhabituel de partage de fichiers externes** <br/> |Génère une alerte lorsqu’un généralement grand nombre de fichiers dans SharePoint ou OneDrive est partagé avec les utilisateurs extérieurs à votre organisation. Cette stratégie possède un paramètre de gravité **moyenne** .<br/> |E5/G5 ou abonnement de module complémentaire Office 365 menaces ou de conformité avancées  <br/> |
|**Volume inhabituel de suppression de fichiers** <br/> |Génère une alerte lorsqu’un nombre excessif de fichiers est supprimé dans SharePoint ou OneDrive dans un délai court. Cette stratégie possède un paramètre de gravité **moyenne** .<br/> |E5/G5 ou abonnement de module complémentaire Office 365 menaces ou de conformité avancées  <br/> |
|**Augmentation inhabituelle de messagerie signalée comme hameçonnage** <br/> |Génère une alerte lorsqu’il existe une augmentation significative du nombre de personnes dans votre organisation à l’aide du complément de Message d’état dans Outlook aux messages de rapport en tant que courrier hameçonnage. Cette stratégie possède un paramètre de gravité **élevée** . Pour plus d’informations sur ce complément, reportez-vous à [utiliser le complément de Message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).<br/> |Abonnement de module complémentaire E5/G5 ou menaces Office 365  <br/> |
   
Notez que l’activité inhabituelle surveillée par certaines stratégies intégrées est basée sur le même processus que le seuil d’alerte qui a été précédemment décrits. Office 365 établit une valeur de base qui définit la fréquence normale pour l’activité « normal ». Alertes sont déclenchées puis lorsque la fréquence des activités suivies par la stratégie de l’alerte intégrée considérablement dépasse la valeur de la ligne de base.
 
## <a name="viewing-alerts"></a>Affichage des alertes

Lorsqu’une activité effectuée par les utilisateurs de votre organisation correspondent aux paramètres d’une stratégie de l’alerte, une alerte est générée et affichée dans la page **Afficher les alertes** de sécurité &amp; centre de conformité. En fonction des paramètres d’une stratégie de l’alerte, une notification par courrier électronique est également envoyée à une liste d’utilisateurs spécifiés lors du déclenche d’une alerte. Pour chaque alerte, le tableau de bord dans la page **Afficher les alertes** affiche le nom de la stratégie de l’alerte correspondante, la catégorie et la gravité de l’alerte (défini dans la stratégie de l’alerte) et le nombre de fois qu’une activité s’est produite qui a provoqué l’alerte en cours généré ; Cette valeur est basée sur le paramètre de seuil de la stratégie de l’alerte. Le tableau de bord affiche également l’état pour chaque alerte. Consultez la section [Gestion des alertes](#managing-alerts) pour plus d’informations sur l’utilisation de la propriété status pour gérer les alertes. 
  
Pour afficher les alertes, accédez à des **alertes** \> **Afficher les alertes** de sécurité &amp; centre de conformité. 
  
![Dans la sécurité &amp; Complinace centre de solutions, cliquez sur alertes, puis cliquez sur Afficher les alertes pour afficher des alertes](media/ec5ea59b-bf61-459f-8b65-970ab4bb8bcc.png)
  
Vous pouvez utiliser les filtres suivants pour afficher un sous-ensemble de toutes les alertes dans la page **Afficher les alertes** . 
  
- **État** - Utilisez ce filtre pour afficher les alertes qui sont affectés à un état particulier ; l’état par défaut est **Active**. Autres administrateurs ou vous pouvant modifier la valeur d’état.
    
- **Stratégie** - Utilisez ce filtre pour afficher les alertes qui correspondent à la valeur d’une ou plusieurs stratégies de l’alerte. Ou bien, vous pouvez uniquement afficher toutes les alertes pour toutes les stratégies de l’alerte.
    
- **Période** - Utilisez ce filtre pour afficher les alertes qui ont été générés au sein d’une date spécifique et une plage de temps.
    
- **Gravité** - Utilisez ce filtre pour afficher les alertes qui sont affectés à un niveau de gravité spécifique.
    
- **Catégorie** - Utilisez ce filtre pour afficher les alertes à partir d’une ou plusieurs catégories de l’alerte.

- **Source** - Utilisez ce filtre pour afficher les alertes déclenchées par des stratégies de l’alerte dans le centre de conformité de & sécurité ou les alertes déclenchées par les stratégies de sécurité d’application Office 365 dans le nuage, ou les deux. Pour plus d’informations sur les alertes de sécurité pour application Cloud Microsoft Office 365, voir la section [affichage du nuage application sécurité alertes](#viewing-cloud-app-security-alerts) .

### <a name="rbac-permissions-required-to-view-alerts"></a>Autorisations RBAC requises pour afficher les alertes

> [!NOTE]
> La fonctionnalité décrite dans cette section mettra en place pour les organisations commençant sur 20 février 2019 et sera effectuée dans le monde entier à la fin de mars 2019.

Les autorisations de contrôle d’accès des Bases de rôle (RBAC) affectées aux utilisateurs dans votre organisation détermine les alertes, les utilisateurs peuvent voir dans la page **Afficher les alertes** . Comment est effectué ? Les rôles de gestion affectées aux utilisateurs (en fonction de leur appartenance à des groupes de rôles dans le centre de conformité de & sécurité) déterminent les catégories d’alerte un utilisateur peut voir dans la page **Afficher les alertes** . Voici quelques exemples :

- Les membres du groupe de rôles de gestion des enregistrements peuvent afficher uniquement les alertes qui sont générés par les stratégies de l’alerte qui sont affectés à la catégorie de **la gouvernance des données** .
- Les membres du groupe de rôles d’administrateur de la conformité ne peut pas afficher les alertes qui sont générées par des stratégies de l’alerte qui sont affectés à la catégorie de **Gestion des menaces** . 
- Membres du groupe de rôles de gestionnaire de découverte ne peut pas afficher les alertes, car aucun des rôles affectés accordent des autorisations pour afficher les alertes à partir de n’importe quelle catégorie de l’alerte.

Ce modèle (en fonction des autorisations RBAC) vous permet de déterminer les alertes qui peuvent être visualisés (et gérées) par les utilisateurs dans des rôles spécifiques dans votre organisation. 

Le tableau suivant répertorie les rôles qui sont nécessaires pour afficher les alertes de 6 différentes catégories de l’alerte. La première colonne dans les tableaux répertorie tous les rôles de centre de conformité & sécurité.  Une coche indique qu’un utilisateur qui est affecté à ce rôle peut afficher des alertes à partir de la catégorie d’alerte correspondante répertorié dans la ligne supérieure.

|<br/>|Gouvernance des données|Protection contre la perte de données|Flux de messagerie|Autorisations|Gestion des menaces|Autres | 
|:---------|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|
|Journaux d’audit <br/> |         ||         |         |         |         |
|Gestion des incidents <br/>|         |         |         |         |         |         |
|Administrateur de conformité<br/>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Recherche de conformité<br/>|         |         |         |         |         |         |
|Gestion des appareils<br/>|         |         |         |         |         |         |
|Gestion de destruction<br/>|         |         |         |         |         |         |
|Gestion de la conformité DLP<br/>|         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |
|Exporter<br/>|         |         |         |         |         |         |
|Conservation<br/>|         |         |         |         |         |         |
|Gérer les alertes<br/>|         |         |         |         |         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Configuration de l’organisation|         |         |         |         |         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Aperçu <br/>|         |         |         |         |         |         |
|Gestion des enregistrements <br/>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Gestion de la rétention <br/>| ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Révision  <br/>|         |         |         |         |         |         |
|Déchiffrement RMS<br/>|         |         |         |         |         |         |
|Gestion des rôles<br/>|         |         |         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |
|Recherche et Purge<br/>|         |         |         |         |         |         |
|Administrateur de sécurité<br/>||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| | ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Lecteur de sécurité<br/>|         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| | ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)
|Affichage d’Assurance de service<br/>|         |         |         |         |         |         |
|Surveillance administrateur de révision<br/>|         |         |         |         |         |         |
|Journaux d’Audit affichage seul<br/>|         |         |         |         |         |         |
|Gestion des périphériques affichage seul<br/>|         |         |         |         |         |         |
|Gestion de la conformité DLP affichage seul<br/>|         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |
|Affichage seul gérer les alertes<br/>|         |         |         |         |         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Afficher uniquement les destinataires<br/>|         |         |  ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       |         ||         |
|Gestion des enregistrements affichage seul<br/>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Gestion de la rétention d’affichage seul<br/>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|         |         |         |         |         |         |

**Conseil :** Pour afficher les rôles qui sont assignés à chacun des groupes de rôles par défaut, exécutez les commandes suivantes dans la sécurité & PowerShell du centre de conformité : 

```
$RoleGroups = Get-RoleGroup

$RoleGroups | foreach {Write-Output -InputObject `r`n,$_.Name,"-----------------------"; Get-RoleGroup $_.Identity | Select-Object -ExpandProperty Roles}
```
Vous pouvez également afficher les rôles attribués à un groupe de rôles dans le centre de conformité de & sécurité. Accédez à la page **autorisations** , cliquez sur un groupe de rôles. Les rôles attribués sont répertoriés dans la page mobile.


## <a name="managing-alerts"></a>Gestion des alertes

Une fois que les alertes ont été générés et affichés sur la page **Afficher les alertes** de sécurité &amp; centre de conformité, vous pouvez trier, examiner et les résoudre. Voici certaines tâches que vous pouvez effectuer pour gérer les alertes. 
  
- **Affecter un statut aux alertes** : vous pouvez affecter un des statuts suivants aux alertes : **Active** (la valeur par défaut), **Investigating**, **résolu**ou **Dismissed**. Ensuite, vous pouvez filtrer ce paramètre pour afficher les alertes avec le même paramètre de statut. Ce paramètre de statut peut aider à suivre le processus de gestion des alertes.
    
- **Afficher les détails de l’alerte** : vous pouvez cliquer sur une alerte pour afficher une page mobile avec plus d’informations sur l’alerte. Les informations détaillées dépendent de la stratégie de l’alerte correspondante, mais il inclut généralement les éléments suivants : nom de l’opération réelle qui a déclenché l’alerte (par exemple, une applet de commande), une description de l’activité qui a déclenché l’alerte, l’utilisateur (ou la liste d’utilisateurs) qui a déclenché l’alerte, et le nom (et le lier) du correspondant de stratégie de l’alerte.
    
  - Nom de l’opération réelle qui a déclenché l’alerte, par exemple une applet de commande ou d’une opération de journal d’audit.
    
  - Description de l’activité qui a déclenché l’alerte.
    
  - L’utilisateur qui a déclenché l’alerte. Il est inclus uniquement pour les stratégies des alertes qui sont configurés pour effectuer le suivi d’un utilisateur unique ou une activité unique.
    
  - Le nombre de fois que l’activité de suivi de l’alerte a été effectué. Notez que ce numéro peut correspondre pas à ce nombre d’alertes associées répertoriées sur la page alertes d’affichage, car des alertes supplémentaires ont été déclenchés.
    
  - Un lien vers une liste d’activités qui inclut un élément pour chaque activité qui a été effectué qui a déclenché l’alerte. Chaque entrée dans cette liste identifie lors de l’activité, le nom de l’opération en cours, (par exemple, « FileDeleted ») et l’utilisateur qui a effectué l’activité, l’objet (comme un fichier, un cas de découverte électronique ou une boîte aux lettres) exécutée sur l’activité et l’adresse IP adresse de l’ordinateur de l’utilisateur. Les logiciels malveillants associés alertes, présente des liens vers une liste de messages.
    
  - Le nom (et le lier) de la stratégie de l’alerte correspondante.
    
- **Supprimer les notifications de messagerie** : vous pouvez désactiver (ou supprimer) les notifications par courrier électronique à partir de la page flottant pour une alerte. Lorsque vous supprimez des notifications par courrier électronique, Office 365 n’envoyer des notifications lorsque les activités ou les événements qui correspondent aux conditions de la stratégie de l’alerte. Toutefois, les alertes continuera à être déclencheur lors d’opérations effectuées par les utilisateurs remplissent les conditions de la stratégie de l’alerte. Vous pouvez également désactiver les notifications par courrier électronique en modifiant la stratégie de l’alerte.
    
- **Résoudre les alertes** - vous pouvez marquer une alerte comme résolu dans la page mobile d’une alerte (qui définit l’état de l’alerte **résolu**). Sauf si vous modifiez le filtre, alertes résolues ne sont pas affichés dans la page **Afficher les alertes** . 
    
## <a name="viewing-cloud-app-security-alerts"></a>Affichage des alertes de sécurité des applications dans le nuage
  
Les alertes qui sont déclenchées par les stratégies de sécurité d’application Office 365 dans le Cloud sont affichent dans la page **Afficher les alertes** dans le centre de conformité de & sécurité. Cela inclut les alertes qui sont déclenchées par les stratégies d’activité et les alertes qui sont déclenchées par des stratégies de détection des anomalies dans Office 365 Cloud Application Security. Cela signifie que vous pouvez afficher toutes les alertes dans le centre de conformité de & sécurité. Notez que Office 365 Cloud application sécurité n’est disponible pour les organisations avec un abonnement à Office 365 entreprise E5 ou Office 365 des G5 des administrations US. Pour plus d’informations, voir [Vue d’ensemble d’Office 365 Cloud Application Security](office-365-cas-overview.md).

En outre, les organisations qui ont Microsoft Cloud Application Security dans le cadre d’une mobilité d’entreprise + l’abonnement E5 de sécurité ou en tant que service autonome peuvent également afficher les alertes de sécurité d’application Cloud liés aux applications Office 365 et les services dans le & de sécurité Centre de conformité.

Pour afficher uniquement les alertes de sécurité des applications dans le nuage dans le centre de conformité de & sécurité, utilisez le filtre de la **Source** et sélectionnez **Sécurité d’application dans le nuage**.

![Utilisez le filtre de la Source pour afficher uniquement les alertes de sécurité des applications dans le nuage](media/FilterCASAlerts.png)

Semblable à une alerte déclenchée par un & de sécurité Stratégie de l’alerte de centre de conformité, vous pouvez cliquer sur une alerte de sécurité des applications dans le nuage pour afficher une page mobile avec plus d’informations sur l’alerte. Le message d’alerte inclut un lien pour afficher les détails et gérer l’alerte dans le portail de sécurité des applications dans le nuage et un lien vers la stratégie de sécurité des applications dans le nuage correspondante qui a déclenché l’alerte. Consultez la rubrique [révision et effectuer une opération sur les alertes de sécurité d’application Office 365 dans le nuage](review-office-365-cas-alerts.md).

![Détails de l’alerte contiennent des liens vers le portail de sécurité des applications dans le nuage](media/CASAlertDetail.png)

> [!IMPORTANT]
> Modification de l’état d’une alerte de sécurité d’application Cloud dans le centre de conformité de & sécurité ne sont pas mettre à jour l’état de résolution de l’alerte même dans le portail de sécurité des applications dans le nuage. Par exemple, si vous activez l’état de l’alerte comme **résolu** dans le centre de conformité de & sécurité, l’état de l’alerte dans le portail de sécurité des applications dans le nuage est inchangée. Pour résoudre ou faire disparaître une alerte de sécurité des applications dans le nuage, gérer l’alerte dans le portail de sécurité des applications dans le nuage.