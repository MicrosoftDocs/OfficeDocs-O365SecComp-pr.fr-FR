---
title: Stratégies d'alerte dans le centre de &amp; sécurité conformité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: 8927b8b9-c5bc-45a8-a9f9-96c732e58264
description: Créez des stratégies d'alerte dans le centre &amp; de sécurité conformité Office 365 pour surveiller les menaces potentielles, les pertes de données et les autorisations. Ensuite, vous pouvez afficher et gérer les alertes générées lorsque les utilisateurs effectuent des activités qui répondent aux conditions d'une stratégie d'alerte.
ms.openlocfilehash: 562b5870fb866839382b46f3398051f8c63336fb
ms.sourcegitcommit: af69fbf152b03e69d36cb2d7d4593f9945eb8c5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2019
ms.locfileid: "30795699"
---
# <a name="alert-policies-in-the-office-365-security-amp-compliance-center"></a>Stratégies d'alerte dans le centre de &amp; sécurité conformité Office 365

Vous pouvez utiliser les nouveaux outils de tableau de bord d'alerte et d'alerte dans &amp; le centre de sécurité conformité Office 365 pour créer des stratégies d'alerte, puis afficher les alertes générées lorsque les utilisateurs effectuent des activités qui répondent aux conditions d'une stratégie d'alerte. Les stratégies d'alerte s'appuient sur et développent les fonctionnalités des alertes d'activité en vous permettant de catégoriser la stratégie d'alerte, d'appliquer la stratégie à tous les utilisateurs de votre organisation, de définir un niveau de seuil pour le déclenchement d'une alerte et de décider si vous souhaitez ou non recevoir des courriers électroniques. notifications. Il existe également une page **afficher les alertes** dans le &amp; Centre de sécurité conformité où vous pouvez afficher et filtrer des alertes, définir un état d'alerte pour vous aider à gérer les alertes, puis ignorer les alertes après avoir résolu ou résolu l'incident sous-jacent. Nous avons également développé le type d'événements pour lesquels vous pouvez créer des alertes. Par exemple, vous pouvez créer des stratégies d'alerte pour suivre les activités de programmes malveillants et les incidents de perte de données. Enfin, nous avons également inclus un certain nombre de stratégies d'alerte par défaut qui vous permettent de surveiller l'affectation des privilèges d'administrateur dans Exchange Online, les attaques de programmes malveillants et les niveaux inhabituels de suppressions de fichiers et de partage externe. 
  
> [!NOTE]
> Les stratégies d'alerte sont disponibles pour les organisations disposant d'un abonnement Office 365 Enterprise ou Office 365 Government E1/G1, E3/G3 ou E5/G5. Toutefois, certaines fonctionnalités avancées sont disponibles uniquement pour les organisations disposant d'un abonnement E5/G5 ou pour les organisations disposant d'un abonnement E1/G1 ou E3/G3 et d'un complément Office 365 Advanced Threat Protection (ATP) P2 ou Office 365 Advanced Compliance. abonnés. La fonctionnalité nécessitant un abonnement E5/G5 ou complément est mise en surbrillance dans cette rubrique. Notez également que les stratégies d'alerte sont disponibles dans les environnements Office 365 GCC, GCC High et DoD US Government.
  
## <a name="how-alert-policies-work"></a>Fonctionnement des stratégies d'alerte

Voici un aperçu rapide du fonctionnement des stratégies d'alerte et des alertes déclenchées lorsque l'activité de l'utilisateur ou de l'administrateur correspond aux conditions d'une stratégie d'alerte.
  
![Vue d'ensemble du fonctionnement des stratégies d'alerte](media/e02a622d-b429-448b-8107-dd1a4770b4e0.png)
  
1. Un administrateur de votre organisation crée, configure et active une stratégie d'alerte à l'aide de la page **stratégies d'alerte** du centre de sécurité _AMP_ Compliance Center. Vous pouvez également créer des stratégies d'alerte à l'aide de la cmdlet **New-protectionalert vous permet** dans PowerShell. Pour créer des stratégies d'alerte, vous devez disposer du rôle de configuration de l'organisation ou du rôle gérer les alertes dans le centre de sécurité & Compliance Center.
    
2. Un utilisateur effectue une activité qui correspond aux conditions d'une stratégie d'alerte. Dans le cas d'une attaque par programme malveillant, les messages électroniques infectés envoyés aux utilisateurs de votre organisation déclencheront une alerte.
    
3. Office 365 génère une alerte qui s'affiche sur la page **afficher les alertes** dans le &amp; Centre de sécurité et de conformité. De plus, si les notifications par courrier électronique sont activées pour la stratégie d'alerte, Office 365 envoie une notification à des destinataires de liste. Les alertes qu'un administrateur ou d'autres utilisateurs peuvent voir sur la page **afficher les alertes** sont déterminées par les rôles attribués à l'utilisateur. Pour plus d'informations, consultez la section [autorisations RBAC requises pour afficher les alertes](#rbac-permissions-required-to-view-alerts) .
    
4. Un administrateur gère les alertes dans le &amp; Centre de sécurité conformité. La gestion des alertes consiste à affecter un statut d'alerte pour faciliter le suivi et la gestion de toute enquête.
    
## <a name="alert-policy-settings"></a>Paramètres de stratégie d'alerte

Une stratégie d'alerte se compose d'un ensemble de règles et de conditions qui définissent l'activité de l'utilisateur ou de l'administrateur qui générera une alerte, d'une liste des utilisateurs qui déclencheront l'alerte s'ils effectuent l'activité, ainsi que le seuil qui définit le nombre de fois que l'activité doit avoir lieu avant qu'une n l'alerte est déclenchée. Vous pouvez également catégoriser la stratégie et lui attribuer un niveau de gravité. Ces deux paramètres vous aident à gérer les stratégies d'alerte (et les alertes déclenchées lorsque les conditions de la stratégie sont respectées) car vous pouvez filtrer ces paramètres lors de la gestion des stratégies et &amp; de l'affichage des alertes dans le centre de sécurité et de conformité. Par exemple, vous pouvez afficher les alertes qui répondent aux conditions de la même catégorie ou afficher les alertes ayant le même niveau de gravité.
  
Pour afficher et créer des stratégies d'alerte, **** \> accédez à alerts **Alert Policies** dans le centre de sécurité &amp; conformité. 
  
![Dans le centre &amp; de sécurité des Complinace, cliquez sur alertes, puis sur stratégies d'alerte pour afficher et créer des stratégies d'alerte.](media/09ebd451-8e84-44e1-aefc-63e70bba4d97.png)
  
Une stratégie d'alerte se compose des paramètres et conditions suivants.
  
- **Activité suivie par l'alerte** : vous créez une stratégie pour suivre une activité ou, dans certains cas, des activités associées, ce qui permet de partager un fichier avec un utilisateur externe en le partageant, en affectant des autorisations d'accès ou en créant un lien anonyme. Lorsqu'un utilisateur effectue l'activité définie par la stratégie, une alerte est déclenchée en fonction des paramètres de seuil d'alerte.
    
    > [!NOTE]
    > Les activités que vous pouvez suivre dépendent de la planification Office 365 Enterprise ou Office 365 pour le gouvernement américain de votre organisation. En règle générale, les activités liées aux campagnes de programmes malveillants et aux attaques de hameçonnage requièrent un abonnement E5/G5 ou un abonnement E1/G1 ou E3/G3 avec un abonnement de module complémentaire Threat Intelligence. 
  
- **Conditions d'activité** : pour la plupart des activités, vous pouvez définir des conditions supplémentaires qui doivent être remplies pour qu'une alerte soit déclenchée. Les conditions communes incluent des adresses IP (de sorte qu'une alerte est déclenchée lorsque l'utilisateur effectue l'activité sur un ordinateur avec une adresse IP spécifique ou dans une plage d'adresses IP), si une alerte est déclenchée si un utilisateur ou des utilisateurs spécifiques effectuent cette activité, et si l'activité est effectuée sur un nom de fichier ou une URL spécifique. Vous pouvez également configurer une condition qui déclenche une alerte lorsque l'activité est effectuée par un utilisateur de votre organisation. Notez que les conditions disponibles dépendent de l'activité sélectionnée.
    
- **Lorsque l'alerte est déclenchée** , vous pouvez configurer un paramètre qui définit la fréquence à laquelle une activité peut se produire avant le déclenchement d'une alerte. Cela vous permet de configurer une stratégie pour générer une alerte chaque fois qu'une activité correspond aux conditions de la stratégie, lorsqu'un certain seuil est dépassé, ou lorsque l'activité de l'alerte suivi de l'alerte devient inhabituelle pour notre organisation. 
    
    ![Configurer la façon dont les alertes sont déclenchées, en fonction de la date d'activité, d'un seuil ou d'une activité inhabituelle pour votre organisation](media/97ee1ed2-e7a9-47a2-a980-5f9f63872c65.png)
  
    Si vous sélectionnez le paramètre basé sur une activité inhabituelle, Office 365 établit une valeur de base qui définit la fréquence normale de l'activité sélectionnée; Il faut au maximum 7 jours pour établir cette ligne de base, pendant laquelle les alertes ne seront pas générées. Une fois la configuration de référence établie, une alerte est déclenchée lorsque la fréquence de l'activité suivie par la stratégie d'alerte dépasse largement la valeur de base. Pour les activités liées à l'audit (telles que les activités de fichiers et de dossiers), vous pouvez établir une ligne de base basée sur un seul utilisateur ou sur tous les utilisateurs de votre organisation; pour les activités liées aux programmes malveillants, vous pouvez établir une ligne de base basée sur une seule famille de programmes malveillants, un destinataire unique ou tous les messages de votre organisation.
    
    > [!NOTE]
    > La possibilité de configurer des stratégies d'alerte en fonction d'un seuil ou d'une activité inhabituelle nécessite un abonnement E5/G5 ou un abonnement E1/G1 ou E3/G3 avec un abonnement Office 365 ATP P2 ou un complément de conformité avancé. Les organisations disposant d'un abonnement E1/G1 et E3/G3 ne peuvent créer une stratégie d'alerte que lorsqu'une alerte est déclenchée à chaque fois qu'une activité se produit. 
  
- **Catégorie d'alerte** : pour faciliter le suivi et la gestion des alertes générées par une stratégie, vous pouvez affecter l'une des catégories suivantes à une stratégie.
    
  - Gouvernance des données
    
  - Protection contre la perte de données

  - Flux de messagerie
    
  - Autorisations
    
  - Gestion des menaces
    
  - Autres
    
  Lorsqu'une activité correspond aux conditions de la stratégie d'alerte, l'alerte générée est marquée avec la catégorie définie dans ce paramètre. Cela vous permet de suivre et de gérer les alertes qui ont le même paramètre de catégorie sur la page **afficher les alertes** dans le centre de sécurité _AMP_ Compliance Center, car vous pouvez trier et filtrer les alertes en fonction de la catégorie. 
    
- **Gravité d'alerte** : similaire à la catégorie d'alerte, vous affectez un attribut de gravité ( **faible**, **moyenne**, **haute**ou informatif) pour les stratégies d'alerte. **** Comme la catégorie d'alerte, lorsqu'une activité correspond aux conditions de la stratégie d'alerte, l'alerte générée est marquée avec le même niveau de gravité que celui défini pour la stratégie d'alerte. De nouveau, cela vous permet de suivre et de gérer les alertes qui ont le même paramètre de gravité sur la page **afficher les alertes** . Par exemple, vous pouvez filtrer la liste des alertes afin d'afficher uniquement les alertes dont la gravité est **élevée** . 
    
    > [!TIP]
    > Lors de la configuration d'une stratégie d'alerte, envisagez d'affecter une sévérité supérieure aux activités susceptibles d'avoir des conséquences négatives, telles que la détection de programmes malveillants après livraison aux utilisateurs, l'affichage de données sensibles ou classifiées, le partage de données avec des utilisateurs externes, ou d'autres activités susceptibles de provoquer une perte de données ou des menaces de sécurité. Cela peut vous aider à hiérarchiser les alertes et les actions que vous effectuez pour examiner et résoudre les causes sous-jacentes. 
  
- **Notifications par courrier électronique** : vous pouvez configurer la stratégie de sorte que les notifications par courrier électronique soient envoyées (ou non envoyées) à une liste d'utilisateurs lorsqu'une alerte est déclenchée. Vous pouvez également définir une limite de notification quotidienne de sorte qu'une fois le nombre maximal de notifications atteint, aucune notification supplémentaire n'est envoyée pour l'alerte au cours de ce jour. En plus des notifications par courrier électronique, vous ou d'autres administrateurs pouvez afficher les alertes déclenchées par une stratégie sur la page **afficher les alertes** . EnVisagez d'activer les notifications par courrier électronique pour les stratégies d'alerte d'une catégorie spécifique ou dont le paramètre de gravité est plus élevé. 
  
## <a name="default-alert-policies"></a>Stratégies d'alerte par défaut

Office 365 fournit des stratégies d'alerte intégrées qui permettent d'identifier les risques liés aux autorisations d'administrateur Exchange en matière d'abus, d'activité de programmes malveillants et de gouvernance des données. Sur la page **stratégies d'alerte** , le nom de ces stratégies intégrées est en gras et le type de stratégie est défini sur **système**. Ces stratégies sont activées par défaut. Vous pouvez désactiver ces stratégies (ou de nouveau), configurer une liste de destinataires vers lesquels envoyer des notifications par courrier électronique et définir une limite de notification quotidienne. Les autres paramètres de ces stratégies ne peuvent pas être modifiés.
  
Le tableau suivant répertorie et décrit les stratégies d'alerte par défaut disponibles, ainsi que la catégorie à laquelle chaque stratégie est affectée. Notez que cette catégorie est utilisée pour déterminer les alertes qu'un utilisateur peut afficher sur la page afficher les alertes. Pour plus d'informations, consultez la section [autorisations RBAC requises pour afficher les alertes](#rbac-permissions-required-to-view-alerts) .  

Le tableau indique également les plans Office 365 entreprise et Office 365 pour le gouvernement américain requis pour chacune d'entre elles. Notez que certaines stratégies d'alerte par défaut sont disponibles si votre organisation dispose de l'abonnement de module complémentaire approprié en plus d'un abonnement E1/G1 ou E3/G3. 
  
|**Stratégie d'alerte par défaut**|**Description**|**Category**|**Abonnement entreprise Office 365**|
|:-----|:-----|:-----|:-----|
|**Un clic d'URL potentiellement malveillant a été détecté** <br/> |Génère une alerte lorsqu'un utilisateur protégé par [Office 365 les liens approuvés ATP](https://docs.microsoft.com/office365/securitycompliance/atp-safe-links) dans votre organisation clique sur un lien malveillant. Cet événement est déclenché lorsque les modifications de verdict d'URL sont identifiées par Office 365 ATP ou lorsque les utilisateurs remplacent les pages de liens approuvés Office 365 ATP (en fonction de la stratégie de liens approuvés Office 365 ATP). Cette stratégie d'alerte a un paramètre de gravité **élevée** . Pour les clients Office 365 ATP P2, E5, G5, cette alerte déclenche automatiquement une [enquête et une réponse automatiséEs d'office 365](https://go.microsoft.com/fwlink/?linkid=2084737).  Pour plus d'informations sur les événements qui déclenchent cette alerte, consultez la rubrique [set up Office 365 ATP Safe Links Policies](https://docs.microsoft.com/office365/securitycompliance/set-up-atp-safe-links-policies).  <br/> |Gestion des menaces <br/> |Ajout d'un abonnement de complément P2 à l'ATP P2/G5 ou à Office 365  <br/> |
|**Création d'une règle de transfert/redirection** <br/> |Génère une alerte lorsqu'une personne de votre organisation crée une règle de boîte de réception pour sa boîte aux lettres qui transfère ou redirige les messages vers un autre compte de messagerie. Cette stratégie effectue uniquement le suivi des règles de boîte de réception créées à l'aide d'Outlook sur le Web (anciennement Outlook Web App) ou Exchange Online PowerShell. Cette stratégie a un paramètre de gravité **faible** . Pour plus d'informations sur l'utilisation des règles de boîte de réception pour transférer et rediriger le courrier électronique dans Outlook sur le Web, consultez [la rubrique utiliser des règles dans Outlook sur le Web pour transférer automatiquement des messages vers un autre compte](https://support.office.com/article/1433e3a0-7fb0-4999-b536-50e05cb67fed).  <br/> |Gestion des menaces <br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**recherche de découverte électronique démarrée ou exportée** <br/> |Génère une alerte lorsqu'un utilisateur utilise l'outil de recherche de contenu dans le centre de sécurité & Compliance Center. Une alerte est déclenchée lorsque les activités de recherche de contenu suivantes sont effectuées: <br/><br/>• Une recherche de contenu est démarrée.<br/>• Les résultats d'une recherche de contenu sont exportés<br/>• Un rapport de recherche de contenu est exporté<br/><br/>Les alertes sont également déclenchée lorsque les activités de recherche de contenu précédentes sont effectuées en association avec un cas de découverte électronique. Cette stratégie a un paramètre de gravité **moyenne** . Pour plus d'informations sur les activités de recherche de contenu, voir [Search for eDiscovery Activities dans le journal d'audit Office 365](search-for-ediscovery-activities-in-the-audit-log.md#ediscovery-activities). <br/> |Gestion des menaces<br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**Élévation des privilèges d'administrateur Exchange** <br/> |Génère une alerte lorsqu'un utilisateur se voit attribuer des autorisations d'administration dans votre organisation Exchange Online; par exemple, si un utilisateur est ajouté au groupe de rôles gestion de l'organisation dans Exchange Online. Cette stratégie a un paramètre de gravité **faible** .  <br/> |Autorisations <br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**Messages électroniques contenant des programmes malveillants supprimés après la remise** <br/> |Génère une alerte lorsque des messages contenant des programmes malveillants sont remis à des boîtes aux lettres de votre organisation. Si cet événement se produit, Office 365 supprime les messages infectés des boîtes aux lettres Exchange Online à l'aide de la [purge automatique avec zéro heure](https://docs.microsoft.com/en-us/office365/securitycompliance/zero-hour-auto-purge). Cette stratégie a un paramètre de gravité d' **information** et déclenche automatiquement l'analyse [et la réponse automatisées d'Office 365](https://go.microsoft.com/fwlink/?linkid=2084737).<br/> |Gestion des menaces <br/> |Ajout d'un abonnement de complément P2 à l'ATP P2/G5 ou à Office 365  <br/> |
|**Messages électroniques contenant des URL d'hameçonnage supprimées après la remise** <br/> |Génère une alerte lorsque des messages contenant des hameçons sont remis à des boîtes aux lettres de votre organisation. Si cet événement se produit, Office 365 supprime les messages infectés des boîtes aux lettres Exchange Online à l'aide de la [purge automatique avec zéro heure](https://docs.microsoft.com/en-us/office365/securitycompliance/zero-hour-auto-purge). Cette stratégie a un paramètre de gravité d' **information** et déclenche automatiquement l'analyse [et la réponse automatisées d'Office 365](https://go.microsoft.com/fwlink/?linkid=2084737).<br/> |Gestion des menaces <br/> |Ajout d'un abonnement de complément P2 à l'ATP P2/G5 ou à Office 365  <br/> |
|**Courrier électronique signalé par l'utilisateur comme programme malveillant ou hameçonnage** <br/> |Génère une alerte lorsque les utilisateurs de votre organisation signalent des messages en tant que courrier électronique de hameçonnage à l'aide du complément de message de rapport. Cette stratégie a un paramètre de gravité d' **information** . Pour plus d'informations sur ce complément, reportez-vous à [la rubrique utiliser le complément de message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Pour les clients Office 365 ATP P2, E5, G5, cette alerte déclenche automatiquement une [enquête et une réponse automatiséEs d'office 365](https://go.microsoft.com/fwlink/?linkid=2084737).  <br/> |Gestion des menaces <br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**Les messages ont été retardés** <br/> |Génère une alerte quand Office 365 ne peut pas envoyer de messages électroniques à votre organisation locale ou à un serveur partenaire à l'aide d'un connecteur. Lorsque cela se produit, le message est mis en file d'attente dans Office 365. Cette alerte est déclenchée lorsqu'il y a 2 000 messages ou plus qui ont été mis en file d'attente pendant plus d'une heure. Cette stratégie a un paramètre de gravité **élevée** .  <br/> |Flux de messagerie<br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|**Campagne anti-programme malveillant détectée après la remise** <br/> |Génère une alerte lorsqu'un nombre anormalement élevé de messages contenant des programmes malveillants est remis aux boîtes aux lettres de votre organisation. Si cet événement se produit, Office 365 supprime les messages infectés des boîtes aux lettres Exchange Online. Cette stratégie a un paramètre de gravité **élevée** .  <br/> |Gestion des menaces<br/> |Ajout d'un abonnement de complément P2 à l'ATP P2/G5 ou à Office 365  <br/> |
|**Campagne anti-programme malveillant détectée et bloquée** <br/> |Génère une alerte lorsqu'un utilisateur a tenté d'envoyer un nombre anormalement élevé de messages électroniques contenant un certain type de programme malveillant aux utilisateurs de votre organisation. Si cet événement se produit, les messages infectés sont bloqués par Office 365 et ne sont pas remis aux boîtes aux lettres. Cette stratégie a un paramètre de gravité **faible** .  <br/> |Gestion des menaces<br/> |Ajout d'un abonnement de complément P2 à l'ATP P2/G5 ou à Office 365  <br/> |
|**Campagne anti-programme malveillant détectée dans SharePoint et OneDrive** <br/> |Génère une alerte lorsqu'un volume inhabituellement élevé de programmes malveillants ou de virus est détecté dans des fichiers situés dans des sites SharePoint ou des comptes OneDrive de votre organisation. Cette stratégie a un paramètre de gravité **élevée** .  <br/> |Gestion des menaces<br/> |Ajout d'un abonnement de complément P2 à l'ATP P2/G5 ou à Office 365  <br/> |
|**Activité inHabituelle de fichier utilisateur externe** <br/> |Génère une alerte lorsqu'un grand nombre d'activités est généralement effectué sur des fichiers dans SharePoint ou OneDrive par des utilisateurs externes à votre organisation. Cela inclut des activités telles que l'accès aux fichiers, le téléchargement de fichiers et la suppression de fichiers. Cette stratégie a un paramètre de gravité **élevée** .  <br/> |Gouvernance des données<br/> |E5/G5, Office 365 DAV P2 ou abonnement au complément de conformité avancé  <br/> |
|**Volume inHabituel de partage de fichiers externes** <br/> |Génère une alerte lorsqu'un nombre généralement important de fichiers dans SharePoint ou OneDrive est partagé avec des utilisateurs extérieurs à votre organisation. Cette stratégie a un paramètre de gravité **moyenne** .  <br/> |Gouvernance des données<br/> |E5/G5, Office 365 DAV P2 ou abonnement au complément de conformité avancé  <br/> |
|**Volume inHabituel de suppression de fichiers** <br/> |Génère une alerte lorsqu'un nombre anormalement élevé de fichiers est supprimé dans SharePoint ou OneDrive pendant une période courte. Cette stratégie a un paramètre de gravité **moyenne** .  <br/> |Gouvernance des données <br/> |E5/G5, Office 365 DAV P2 ou abonnement au complément de conformité avancé  <br/> |
|**Augmentation inHabituelle d'e-mails signalés comme hameçons** <br/> |Génère une alerte lorsqu'il y a une augmentation significative du nombre de personnes dans votre organisation à l'aide du complément Report message dans Outlook pour signaler les messages sous forme de courriers électroniques de hameçonnage. Cette stratégie a un paramètre de gravité **élevée** . Pour plus d'informations sur ce complément, reportez-vous à [la rubrique utiliser le complément de message de rapport](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).  <br/> |Gestion des menaces<br/> |Ajout d'un abonnement de complément P2 à l'ATP P2/G5 ou à Office 365  <br/> |
|**Utilisateur non autorisé à envoyer un message électronique** <br/> |Génère une alerte lorsqu'une personne de votre organisation est restreinte d'envoyer des messages sortants. Cela se produit généralement lorsqu'un compte est compromis, et que l'utilisateur est affiché sur la page **utilisateurs restreints** dans le centre de sécurité _AMP_ Compliance Center. (Pour accéder à cette page, accédez à **> de gestion des menaces _GT_ utilisateurs restreints**). Cette stratégie a un paramètre de gravité **élevée** . Pour plus d'informations sur les utilisateurs avec accès restreint, consultez [la rubrique Suppression d'un utilisateur, d'un domaine ou d'une adresse IP d'une liste rouge après l'envoi de courrier](https://docs.microsoft.com/office365/securitycompliance/removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email)indésirable.  <br/> |Gestion des menaces<br/> |E1/G1, E3/G3 ou E5/G5  <br/> |
|||||
   
Notez que l'activité inhabituelle surveillée par certaines stratégies intégrées est basée sur le même processus que le paramètre de seuil d'alerte précédemment décrit. Office 365 établit une valeur de base qui définit la fréquence normale pour l'activité «usuelle». Les alertes sont ensuite déclenchées lorsque la fréquence des activités suivies par la stratégie d'alerte intégrée dépasse largement la valeur de la base.
 
## <a name="viewing-alerts"></a>Affichage des alertes

Lorsqu'une activité effectuée par les utilisateurs de votre organisation correspond aux paramètres d'une stratégie d'alerte, une alerte est générée et affichée sur la page **Afficher** les alertes &amp; dans le centre de sécurité et de conformité. En fonction des paramètres d'une stratégie d'alerte, une notification par courrier électronique est également envoyée à une liste d'utilisateurs spécifiés lorsqu'une alerte est déclenchée. Pour chaque alerte, le tableau de bord de la page **afficher les alertes** affiche le nom de la stratégie d'alerte correspondante, la gravité et la catégorie de l'alerte (définies dans la stratégie d'alerte), ainsi que le nombre de fois qu'une activité a eu lieu et que l'alerte a été générée. créés Cette valeur est basée sur le paramètre seuil de la stratégie d'alerte. Le tableau de bord affiche également l'état de chaque alerte. Pour plus d'informations sur l'utilisation de la propriété Status pour gérer les alertes, voir la section [gestion des alertes](#managing-alerts) . 
  
Pour afficher les alertes, accédez **** \> à alertes **Afficher** les alertes dans &amp; le centre de sécurité conformité. 
  
![Dans le centre &amp; de sécurité des Complinace, cliquez sur alertes, puis sur Afficher les alertes pour afficher les alertes.](media/ec5ea59b-bf61-459f-8b65-970ab4bb8bcc.png)
  
Vous pouvez utiliser les filtres suivants pour afficher un sous-ensemble de toutes les alertes sur la page **afficher les alertes** . 
  
- **État** : utilisez ce filtre pour afficher les alertes affectées à un statut particulier; l'État par défaut est **actif**. Vous ou d'autres administrateurs pouvez modifier la valeur d'État.
    
- **Stratégie** : utilisez ce filtre pour afficher les alertes correspondant au paramètre d'une ou de plusieurs stratégies d'alerte. Vous pouvez également afficher toutes les alertes pour toutes les stratégies d'alerte.
    
- **Plage horaire** : utilisez ce filtre pour afficher les alertes générées dans une plage de dates et d'heures spécifique.
    
- **Gravité** : utilisez ce filtre pour afficher les alertes auxquelles une gravité spécifique a été attribuée.
    
- **Catégorie** : utilisez ce filtre pour afficher les alertes d'une ou de plusieurs catégories d'alerte.

- **Source** : utilisez ce filtre pour afficher les alertes déclenchées par les stratégies d'alerte dans le centre de sécurité _AMP_ Compliance Center ou les alertes déclenchées par les stratégies de sécurité d'application Cloud d'Office 365, ou les deux. Pour plus d'informations sur les alertes de sécurité d'application Cloud Office 365, consultez la section [affichage des alertes de sécurité des applications Cloud](#viewing-cloud-app-security-alerts) .

## <a name="rbac-permissions-required-to-view-alerts"></a>Autorisations RBAC requises pour afficher les alertes

> [!NOTE]
> Les fonctionnalités décrites dans cette section seront déployées dans les organisations commençant le 20 février 2019 et seront réalisées dans le monde entier à la fin du 2019 mars.

Les autorisations de contrôle d'accès des bases de rôles (RBAC) affectées aux utilisateurs de votre organisation déterminent les alertes qu'un utilisateur peut afficher sur la page **afficher les alertes** . Comment cela est-il accompli? Les rôles de gestion attribués aux utilisateurs (en fonction de leur appartenance à des groupes de rôles dans le centre de sécurité & Compliance Center) déterminent les catégories d'alertes qu'un utilisateur peut afficher sur la page **afficher les alertes** . Voici quelques exemples :

- Les membres du groupe de rôles Gestion des enregistrements peuvent afficher uniquement les alertes générées par les stratégies d'alerte auxquelles la catégorie de **gouvernance des données** est attribuée.

- Les membres du groupe de rôles Administrateur de conformité ne peuvent pas afficher les alertes générées par les stratégies d'alerte auxquelles la catégorie de **gestion des menaces** est attribuée. 

- Les membres du groupe de rôles gestionnaire de découverte électronique ne peuvent pas afficher les alertes car aucun des rôles attribués ne donne l'autorisation d'afficher les alertes à partir de n'importe quelle catégorie d'alerte.

Cette conception (basée sur les autorisations RBAC) vous permet de déterminer les alertes pouvant être affichées (et gérées) par les utilisateurs en fonction de rôles de travail spécifiques dans votre organisation. 

Le tableau suivant répertorie les rôles requis pour afficher les alertes à partir des six catégories d'alertes différentes. La première colonne dans les tableaux répertorie tous les rôles dans le centre de sécurité & Compliance Center.  Une coche indique qu'un utilisateur auquel ce rôle est attribué peut afficher des alertes à partir de la catégorie d'alerte correspondante indiquée dans la ligne supérieure.

Pour voir la catégorie affectée à une stratégie d'alerte par défaut, consultez le tableau de la section [stratégies d'alerte par défaut](#default-alert-policies) .

|<br/>|Gouvernance des données|Protection contre la perte de données|Flux de messagerie|Autorisations|Gestion des menaces|Autres | 
|:---------|:---------:|:---------:|:---------:|:---------:|:---------:|:---------:|
|Journaux d’audit <br/> |         ||         |         |         |         |
|Gestion des cas <br/>|         |         |         |         |         |         |
|Administrateur de conformité<br/>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Recherche de conformité<br/>|         |         |         |         |         |         |
|Gestion des appareils<br/>|         |         |         |         |         |         |
|Gestion des destructions<br/>|         |         |         |         |         |         |
|Gestion de la conformité DLP<br/>|         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |
|Exporter<br/>|         |         |         |         |         |         |
|Placer<br/>|         |         |         |         |         |         |
|Gérer les alertes<br/>|         |         |         |         |         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Configuration de l'Organisation|         |         |         |         |         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Aperçu <br/>|         |         |         |         |         |         |
|Gestion des enregistrements <br/>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Gestion de la réTention <br/>| ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Révision <br/>|         |         |         |         |         |         |
|DéChiffrement RMS<br/>|         |         |         |         |         |         |
|Gestion des rôles<br/>|         |         |         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |
|Recherche et purge<br/>|         |         |         |         |         |         |
|Administrateur de sécurité<br/>||![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| | ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Lecteur de sécurité<br/>|         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| | ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)| ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)
|Vue de service assurance<br/>|         |         |         |         |         |         |
|Administrateur de la vérification de surveillance<br/>|         |         |         |         |         |         |
|Journaux d'audit en affichage seul<br/>|         |         |         |         |         |         |
|Gestion des appareils en affichage seul<br/>|         |         |         |         |         |         |
|Gestion de la conformité DLP en affichage seul<br/>|         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |
|Vue gérer uniquement les alertes<br/>|         |         |         |         |         |![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|
|Afficher uniquement les destinataires<br/>|         |         |  ![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       |         ||         |
|Gestion des enregistrements en affichage seul<br/>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|Gestion de la réTention en affichage seul<br/>|![Coche](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)|         |         |         |         |         |
|         |         |         |         |         |         |

**Conseil:** Pour afficher les rôles affectés à chacun des groupes de rôles par défaut, exécutez les commandes suivantes dans Security & Compliance Center PowerShell: 

```
$RoleGroups = Get-RoleGroup

$RoleGroups | foreach {Write-Output -InputObject `r`n,$_.Name,"-----------------------"; Get-RoleGroup $_.Identity | Select-Object -ExpandProperty Roles}
```
Vous pouvez également afficher les rôles attribués à un groupe de rôles dans le centre de sécurité & Compliance Center. Accédez à la page **autorisations** , puis cliquez sur un groupe de rôles. Les rôles attribués sont répertoriés sur la page de menu volant.


## <a name="managing-alerts"></a>Gestion des alertes

Une fois les alertes générées et affichées sur la page **afficher les alertes** dans &amp; le centre de sécurité et de conformité, vous pouvez les trier, les examiner et les résoudre. Voici quelques tâches que vous pouvez effectuer pour gérer les alertes. 
  
- **Attribuer un État aux alertes** : vous pouvez attribuer l'un des statuts suivants aux alertes: **actif** (valeur par défaut), analyse ****, **résolu**ou **fermé**. Ensuite, vous pouvez filtrer ce paramètre pour afficher les alertes ayant le même paramètre d'État. Ce paramètre d'état permet de suivre le processus de gestion des alertes.
    
- **Afficher les détails** de l'alerte: vous pouvez cliquer sur une alerte pour afficher une page de menu volant avec des détails sur l'alerte. Les informations détaillées dépendent de la stratégie d'alerte correspondante, mais elle inclut généralement les éléments suivants: nom de l'opération réelle qui a déclenché l'alerte (par exemple, une cmdlet), une description de l'activité qui a déclenché l'alerte, l'utilisateur (ou la liste des utilisateurs) qui a déclenché l'alerte, ainsi que le nom (et le lien) de la stratégie d'alerte correspondante.
    
  - Nom de l'opération réelle qui a déclenché l'alerte, telle qu'une applet de commande ou une opération de journal d'audit.
    
  - Description de l'activité qui A déclenché l'alerte.
    
  - Utilisateur qui a déclenché l'alerte; Cette option est incluse uniquement pour les stratégies d'alerte configurées pour suivre un seul utilisateur ou une seule activité.
    
  - Nombre de fois que l'activité suivie par l'alerte a été effectuée. Notez que ce nombre peut ne pas correspondre au nombre réel d'alertes associées indiquées sur la page afficher les alertes, car d'autres alertes ont pu être déclenchées.
    
  - Lien vers une liste d'activités qui inclut un élément pour chaque activité effectuée qui a déclenché l'alerte. Chaque entrée de cette liste identifie le moment où l'activité s'est produite, le nom de l'opération réelle (par exemple, «FileDeleted») et l'utilisateur qui a effectué l'activité, l'objet (tel qu'un fichier, un cas eDiscovery ou une boîte aux lettres) sur lequel l'activité a été exécutée, et l'adresse IP adresse de l'ordinateur de l'utilisateur. Pour les alertes liées aux programmes malveillants, cette fonction renvoie à une liste de messages.
    
  - Nom (et lien) de la stratégie d'alerte correspondante.
    
- **Supprimer les notifications par courrier électronique** : vous pouvez désactiver (ou supprimer) les notifications par courrier électronique à partir de la page de menu volant pour une alerte. Lorsque vous supprimez des notifications par courrier électronique, Office 365 n'envoie pas de notifications lorsque des activités ou des événements répondent aux conditions de la stratégie d'alerte. Toutefois, les alertes continuent d'être déclenchées lorsque les activités effectuées par les utilisateurs correspondent aux conditions de la stratégie d'alerte. Vous pouvez également désactiver les notifications par courrier électronique en modifiant la stratégie d'alerte.
    
- **Résoudre les alertes** : vous pouvez marquer une alerte comme étant résolue sur la page de menu volant pour une alerte (qui définit l'état de l'alerte sur **résolu**). Sauf si vous modifiez le filtre, les alertes résolues ne s'affichent pas sur la page **afficher les alertes** . 
    
## <a name="viewing-cloud-app-security-alerts"></a>Affichage des alertes de sécurité des applications Cloud
  
Les alertes déclenchées par les stratégies de sécurité des applications Cloud d'Office 365 s'affichent désormais sur la page **afficher les alertes** dans le centre de sécurité _AMP_ Compliance Center. Cela inclut les alertes déclenchées par les stratégies d'activité et les alertes déclenchées par des stratégies de détection des anomalies dans Office 365 Cloud App Security. Cela signifie que vous pouvez afficher toutes les alertes dans le centre de sécurité & Compliance Center. Notez que la sécurité des applications Cloud Office 365 est uniquement disponible pour les organisations disposant d'un abonnement Office 365 Enterprise E5 ou Office 365 pour le gouvernement G5. Pour plus d'informations, consultez la rubrique [vue d'ensemble de la sécurité des applications Cloud Office 365](office-365-cas-overview.md).

En outre, les organisations qui disposent d'un abonnement Enterprise Mobility + Security E5 ou en tant que service autonome peuvent également afficher les alertes de sécurité des applications Cloud liées aux applications et services Office 365 dans le & de sécurité. Centre de conformité.

Pour afficher uniquement les alertes de sécurité des applications Cloud dans le centre de sécurité & conformité, utilisez le filtre **source** et sélectionnez **sécurité des applications Cloud**.

![Utiliser le filtre source pour afficher uniquement les alertes de sécurité des applications Cloud](media/FilterCASAlerts.png)

À l'inStar d'une alerte déclenchée par une stratégie d'alerte du centre de sécurité & conformité, vous pouvez cliquer sur une alerte de sécurité d'application Cloud pour afficher une page de menu volant avec des détails sur l'alerte. L'alerte comprend un lien permettant d'afficher les détails et de gérer l'alerte dans le portail de sécurité de l'application Cloud, ainsi qu'un lien vers la stratégie de sécurité de l'application Cloud correspondante qui a déclenché l'alerte. Consultez la rubrique [Review and take action on alerts in Office 365 Cloud App Security](review-office-365-cas-alerts.md).

![Les détails de l'alerte contiennent des liens vers le portail de sécurité des applications Cloud](media/CASAlertDetail.png)

> [!IMPORTANT]
> La modification de l'état d'une alerte de sécurité d'application Cloud dans le centre de sécurité & Compliance Center ne met pas à jour l'état de résolution de la même alerte dans le portail de sécurité des applications Cloud. Par exemple, si vous marquez le statut de l'alerte comme **résolu** dans le centre de sécurité _AMP_ Compliance Center, l'état de l'alerte dans le portail de sécurité des applications Cloud est inchangé. Pour résoudre ou faire disparaître une alerte de sécurité d'application Cloud, gérez l'alerte dans le portail de sécurité des applications Cloud.
