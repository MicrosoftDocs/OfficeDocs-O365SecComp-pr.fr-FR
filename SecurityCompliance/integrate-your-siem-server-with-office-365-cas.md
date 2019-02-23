---
title: Intégrer votre serveur SIEM à la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Vous pouvez intégrer votre serveur SIEM à la sécurité des applications Cloud Office 365. Lisez cet article pour obtenir une vue d'ensemble du fonctionnement et de la configuration.
ms.openlocfilehash: b4baeda3cb836c0b1aa528d29176bbf4321d1fe2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215874"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a>Intégrer votre serveur SIEM à la sécurité des applications cloud Office 365
  
|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étape suivante](utilization-activities-for-ocas.md) <br/> |[Commencer à utiliser](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a>Vue d'ensemble et conditions préalables

Vous pouvez intégrer la [sécurité des applications Cloud Office 365](get-ready-for-office-365-cas.md) avec votre serveur de gestion des événements et des informations de sécurité (Siem) pour permettre une surveillance centralisée des alertes. Cela est particulièrement utile pour les organisations qui utilisent les services Cloud et les applications serveur locales. L'intégration à un serveur SIEM permet à votre équipe de sécurité de mieux protéger vos applications Office 365 tout en conservant votre flux de travail de sécurité habituel, en automatisant certaines procédures de sécurité et en corrélées entre les événements sur site et en nuage.  
  
Lorsque vous intégrez votre serveur SIEM à la sécurité des applications Cloud Office 365, les alertes des deux derniers jours sont transmises au serveur SIEM, ainsi qu'à toutes les alertes en provenance de ces deux jours (en fonction de tous les filtres que vous sélectionnez). En outre, si vous désactivez cette fonctionnalité pendant une période prolongée, lorsque vous la réactivez, elle transférera les deux jours précédents d'alertes, puis toutes les alertes à partir de ce moment.

### <a name="siem-integration-architecture"></a>Architecture d'intégration SIEM

Un agent SIEM est configuré dans le réseau de votre organisation. Une fois déployée et configurée, l'agent SIEM extrait les types de données qui ont été configurés (alertes) à l'aide des API Microsoft Office 365 Cloud App Security RESTful. Le trafic est ensuite envoyé sur un canal HTTPs chiffré sur le port 443.
  
Lorsqu'un agent SIEM récupère des données à partir de la sécurité de l'application Cloud Office 365, il envoie les messages syslog à votre serveur SIEM local en utilisant les configurations réseau fournies lors de l'installation (TCP ou UDP avec un port personnalisé).

![Architecture de sécurité de l'application de SIEM et de Cloud](media/siem-architecture.png)

### <a name="supported-siem-servers"></a>Serveurs SIEM pris en charge

La sécurité des applications Cloud Office 365 prend actuellement en charge les serveurs SIEM suivants:
- Micro focus ArcSight
- CEF générique

### <a name="prerequisites"></a>Conditions préalables

- Vous devez être un administrateur général ou un administrateur de sécurité pour effectuer les tâches décrites dans cet article. Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md)

- La sécurité de l' [application Cloud d'Office 365](turn-on-office-365-cas.md) doit être activée pour votre organisation.

- La [journalIsation d'audit](turn-audit-log-search-on-or-off.md) doit être activée pour Office 365

- Vous devez disposer d'un serveur standard remplissant les conditions requises suivantes pour configurer l'intégration de serveur SIEM:
    - SYSTÈME d'exploitation: Windows ou Linux (il peut s'agir d'une machine virtuelle)
    - PROCESSEUR: 2
    - Espace disque: 20 Go
    - RAM: 2 GO
    - [Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installé
    - Pare-feu configuré comme indiqué dans [Network Requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)

- Vous devez disposer de détails sur votre **hôte syslog distant** et votre **numéro de port Syslot**. Un administrateur réseau ou un administrateur de la sécurité doit être en mesure de vous aider à localiser ces informations. 

- Vous devez accepter les termes du contrat de [licence logiciel](https://go.microsoft.com/fwlink/?linkid=862491) pour télécharger le [fichier jar](https://go.microsoft.com/fwlink/?linkid=838596) dont vous aurez besoin pour intégrer votre serveur Siem.
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a>Étape 1: configuration d'un agent SIEM dans Office 365 Cloud App Security

1. Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous.
  
2. Cliquez sur **extensions de sécurité**des **paramètres** \> , puis sur agents Siem.<br/>
![Choisir les paramètres > Security extensions](media/Settings-SecurityExtensions.png)

3. Sélectionnez **Ajouter un agent Siem**.<br/>![Sélectionnez Ajouter un agent SIEM.](media/SIEMAgents.png)
    
4. Sélectionnez **Démarrer l'Assistant**.<br/>![Obtenir de l'aide ou démarrer l'Assistant](media/HelpOrWizard.png) 
    
5. Dans l'étape **générale** , spécifiez un nom, **Sélectionnez votre format Siem** et définissez les **Paramètres avancés** qui sont pertinents pour ce format. Ensuite, cliquez sur **suivant**.<br/>![Spécifier un nom et un type](media/ChooseAgentTypeAndName.png)
    
6. Dans l'étape de **Journal système distant** , spécifiez l'adresse IP ou le nom d'hôte de l' **hôte syslog distant** et le **numéro de port syslog**. Sélectionnez TCP ou UDP comme protocole syslog distant. (Vous pouvez collaborer avec votre administrateur réseau ou administrateur de sécurité pour obtenir ces informations si vous ne les avez pas.) Ensuite, cliquez sur **suivant**.<br/>![Spécifier les détails du journal des accès à distance](media/ArcSightS1Syslog.png)
  
7. Dans l'étape **types de données** , effectuez l'une des opérations suivantes, puis cliquez sur **suivant**:
    - Conserver le paramètre par défaut de **toutes les alertes**<br/>OU
    - Cliquez sur **toutes les alertes**, puis choisissez **filtres spécifiques**. Définissez des filtres pour sélectionner les types d'alertes que vous souhaitez envoyer à votre serveur SIEM.<br/>![Étape types de données de l'Assistant](media/ArcSightS1ExportOptions.png)
  
8. Dans l'écran Félicitations, copiez le jeton et enregistrez-le pour une version ultérieure.<br/>![Écran créé par l'agent SIEM](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> À ce stade, vous avez configuré un agent SIEM dans Office 365 Cloud App Security, mais votre intégration de serveur SIEM n'est pas encore terminée. Passez à l'étape suivante pour continuer votre intégration de serveur SIEM.

Après avoir cliqué sur Fermer et quitté l'Assistant, dans l'écran extensions de sécurité, vous pouvez voir l'agent SIEM que vous avez ajouté dans le tableau. Il indique l'état **créé** jusqu'à ce qu'il soit connecté plus tard.

![Agent SIEM créé](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a>Étape 2: télécharger un fichier JAR et l'exécuter sur votre serveur SIEM

1. Téléchargez l' [agent Siem Microsoft Cloud App Security](https://go.microsoft.com/fwlink/?linkid=838596) et décompressez le dossier. (Vous devez accepter les [termes du contrat de licence logiciel](https://go.microsoft.com/fwlink/?linkid=862491) pour pouvoir continuer.) 
    
2. ExTrayez le fichier. jar du dossier zippé et exécutez-le sur votre serveur SIEM.
    
3. Après avoir exécuté le fichier, exécutez la commande suivante:<br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a>Remarques importantes

- Le nom de fichier peut varier en fonction de la version de l'agent SIEM. 

- Nous vous recommandons d'exécuter le fichier JAR sur votre serveur SIEM lors de la configuration du serveur.

    - **Windows**: exécuter en tant que tâche planifiée, en veillant à configurer la tâche pour **qu'elle s'exécute si l'utilisateur est connecté ou non** et désactivez l'option **arrêter la tâche si elle s'exécute plus longtemps que** .

    - **Linux**: ajoutez la commande Run avec un **&** dans le `rc.local` fichier. <br/>Exemple :<br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- Les paramètres entre crochets [] sont facultatifs et ne doivent être utilisés qu'en cas de pertinence. Utilisez les variables suivantes:

    - **DIRNAME** est le chemin d'accès au répertoire que vous souhaitez utiliser pour les journaux de débogage de l'agent local.

    - **Address [:P ORT]** est l'adresse et le port du serveur proxy utilisés par le serveur pour se connecter à Internet.

    - **Token** est le jeton d'agent Siem que vous avez copié dans la première procédure.

    - Pour obtenir de l'aide `-h`, tapez. 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a>Étape 3: valider le fonctionnement de l'agent SIEM

1. Assurez-vous que l'état de l'agent SIEM dans le portail de sécurité des applications Cloud Office 365 n'est pas affiché en tant qu' **erreur de connexion** ou **déconnecté** et qu'il n'y a pas de notifications d'agent.<br/>Par exemple, nous pouvons voir que le serveur SIEM est connecté:<br/>![Serveur SIEM connecté](media/siem-connected.png)<br/>Et ici, nous pouvons voir que le serveur SIEM est déconnecté:<br/>![Serveur SIEM non connecté](media/siem-not-connected.png) 
  
2. Sur votre serveur Syslog/SIEM, vérifiez que vous voyez que des alertes ont été émises par Office 365 Cloud App Security.
  
## <a name="what-the-logfiles-look-like"></a>À quoi ressemblent les fichiers journaux

Voici un exemple de fichier journal des alertes qui peut être envoyé à un serveur SIEM:

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

Et voici un autre exemple, cette fois au format CEF:


|Nom de champ CEF  | Description  |
|---------|---------|
|Démarrer     | horodatage de l'alerte        |
|fin     | horodatage de l'alerte        |
|transcriptase     | horodatage de l'alerte        |
|msg     | Description de l'alerte, comme illustré dans le portail de sécurité des applications Cloud Office 365        |
|suser     | utilisateur de l'objet d'alerte        |
|destinationServiceName     | alerte: application d'origine, telle qu'Office 365, SharePoint ou OneDrive        |
|csLabel     | Varie (les étiquettes ont des significations différentes). En règle générale, les étiquettes sont explicites, comme targetObjects.        |
|cs     | Informations correspondant à une étiquette (par exemple, l'utilisateur cible d'une alerte en fonction de l'exemple d'étiquette)        |

## <a name="additional-tasks-as-needed"></a>Tâches supplémentaires (si nécessaire)

Une fois que vous avez configuré votre serveur SIEM et que vous l'avez intégré à la sécurité des applications Cloud Office 365, vous devrez peut-être régénérer un jeton, modifier un agent SIEM ou supprimer un agent SIEM. Les sections suivantes décrivent comment effectuer ces tâches.

### <a name="regenerate-a-token"></a>Régénérer un jeton

Si vous perdez votre jeton, vous pouvez en régénérer un. 

1. dans le portail de sécurité des applications Cloud Office[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)365 (), sélectionnez paramètres de**sécurité**des **paramètres** > .

2. Dans le tableau, recherchez la ligne de l'agent SIEM. 

3. Cliquez sur les ellipses, puis choisissez **régénérer le jeton**.<br/>![Régénérer un jeton en cliquant sur les points de suspension de votre agent SIEM](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
### <a name="edit-a-siem-agent"></a>Modifier un agent SIEM

1. dans le portail de sécurité des applications Cloud Office[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)365 (), sélectionnez paramètres de**sécurité**des **paramètres** > .

2. Localisez la ligne pour l'agent SIEM. 

3. Cliquez sur les ellipses, puis choisissez **modifier**. (Si vous modifiez l'agent SIEM, vous n'avez pas besoin de réexécuter le fichier. jar; il est mis à jour automatiquement.)<br/>![Pour modifier votre agent SIEM, sélectionnez les ellipses, puis cliquez sur modifier.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
### <a name="delete-a-siem-agent"></a>Supprimer un agent SIEM

1. dans le portail de sécurité des applications Cloud Office[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)365 (), sélectionnez paramètres de**sécurité**des **paramètres** > .

2. Localisez la ligne pour l'agent SIEM. 

3. Cliquez sur les ellipses, puis choisissez **supprimer**.<br/>![Pour supprimer un agent SIEM, choisissez les ellipses, puis choisissez Supprimer.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

  
## <a name="next-steps"></a>Étapes suivantes

- [Activités d’utilisation après avoir déployé la sécurité des applications cloud Office 365](utilization-activities-for-ocas.md)
    
- [Passer en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [ReGroupez vos adresses IP pour simplifier la gestion](group-your-ip-addresses-in-ocas.md)
    

