---
title: Intégrer votre serveur SIEM à la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Vous pouvez intégrer votre serveur SIEM avec Office 365 Cloud Application Security. Lisez cet article pour obtenir une vue d’ensemble de son fonctionnement et comment la configurer.
ms.openlocfilehash: a2bd75e73ddccef9359ace304faa3c8b1dd4a728
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972326"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="9992c-104">Intégrer votre serveur SIEM à la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="9992c-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="9992c-105">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="9992c-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="9992c-106">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="9992c-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="9992c-107">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="9992c-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="9992c-108">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="9992c-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="9992c-109">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="9992c-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="9992c-110">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="9992c-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="9992c-111">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="9992c-111">You are here!</span></span>  <br/> [<span data-ttu-id="9992c-112">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9992c-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="9992c-113">Commencer à utiliser</span><span class="sxs-lookup"><span data-stu-id="9992c-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="9992c-p102">Vous pouvez intégrer [Office 365 Cloud application sécurité](get-ready-for-office-365-cas.md) avec le serveur sécurité des informations et des événements SIEM (gestion) pour activer la surveillance centralisée des alertes. Cela est particulièrement utile pour les organisations qui utilisent des services en nuage et des applications serveur local. Intégration avec un serveur SIEM permet à votre équipe de sécurité pour mieux protéger vos applications Office 365 tout en conservant votre flux de travail habituelles de sécurité, en automatisant certaines procédures de sécurité et de corrélation entre en nuage et événements locale.</span><span class="sxs-lookup"><span data-stu-id="9992c-p102">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts. This is especially beneficial for organizations who are using cloud services and on-premises server applications. Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="9992c-p103">Lorsque vous intégrez tout d’abord votre serveur SIEM avec Office 365 Cloud application sécurité, alertes à partir des deux derniers jours sont transférés vers le serveur SIEM, ainsi que toutes les alertes à partir de puis sur (basé sur des filtres que vous sélectionnez). En outre, si vous désactivez cette fonctionnalité pour une période prolongée, lorsque vous le réactiviez, elle transmet les deux derniers jours d’alertes et de toutes les alertes puis par la suite.</span><span class="sxs-lookup"><span data-stu-id="9992c-p103">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select). Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>
 
## <a name="siem-integration-architecture"></a><span data-ttu-id="9992c-119">Architecture de l’intégration SIEM</span><span class="sxs-lookup"><span data-stu-id="9992c-119">SIEM integration architecture</span></span>

<span data-ttu-id="9992c-p104">Un agent SIEM est défini dans le réseau de votre organisation. Déployée et configurée, l’agent SIEM extrait les types de données qui ont été configurées (alertes) à l’aide des API RESTful sécurité d’application dans le nuage Office 365. Le trafic est ensuite envoyé via un canal HTTPS chiffré sur le port 443.</span><span class="sxs-lookup"><span data-stu-id="9992c-p104">A SIEM agent is set up in your organization's network. When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs. The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="9992c-123">Lorsqu’un agent SIEM récupère des données à partir de la sécurité d’application Office 365 dans le nuage, il envoie les messages de journal système à votre serveur SIEM local en utilisant les configurations de réseau sont fournies lors de l’installation (TCP ou UDP avec un port personnalisé).</span><span class="sxs-lookup"><span data-stu-id="9992c-123">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![Architecture SIEM et de sécurité d’application dans le nuage](media/siem-architecture.png)

## <a name="supported-siem-servers"></a><span data-ttu-id="9992c-125">Serveurs SIEM pris en charge</span><span class="sxs-lookup"><span data-stu-id="9992c-125">Supported SIEM servers</span></span>

<span data-ttu-id="9992c-126">Sécurité d’application Office 365 Cloud prend actuellement en charge les serveurs SIEM suivants :</span><span class="sxs-lookup"><span data-stu-id="9992c-126">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="9992c-127">ArcSight Micro Focus</span><span class="sxs-lookup"><span data-stu-id="9992c-127">Micro Focus ArcSight</span></span>
- <span data-ttu-id="9992c-128">Format CEF générique</span><span class="sxs-lookup"><span data-stu-id="9992c-128">Generic CEF</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9992c-129">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="9992c-129">Prerequisites</span></span>

- <span data-ttu-id="9992c-p105">Vous devez être un administrateur global ou un administrateur de sécurité pour effectuer les tâches décrites dans cet article. Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="9992c-p105">You must be a global administrator or security administrator to perform the tasks described in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="9992c-132">Vous devez avoir [activé de sécurité d’application Office 365 dans le nuage](turn-on-office-365-cas.md) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9992c-132">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="9992c-133">[L’enregistrement d’audit](turn-audit-log-search-on-or-off.md) doit être activé pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9992c-133">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="9992c-134">Vous devez disposer d’un serveur standard qui remplit les conditions suivantes afin de configurer l’intégration du serveur SIEM :</span><span class="sxs-lookup"><span data-stu-id="9992c-134">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="9992c-135">Système d’exploitation : Windows ou Linux (Cela peut être un ordinateur virtuel)</span><span class="sxs-lookup"><span data-stu-id="9992c-135">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="9992c-136">PROCESSEUR : 2</span><span class="sxs-lookup"><span data-stu-id="9992c-136">CPU: 2</span></span>
    - <span data-ttu-id="9992c-137">Espace disque : 20 Go</span><span class="sxs-lookup"><span data-stu-id="9992c-137">Disk space: 20 GB</span></span>
    - <span data-ttu-id="9992c-138">RAM : 2 GO</span><span class="sxs-lookup"><span data-stu-id="9992c-138">RAM: 2 GB</span></span>
    - <span data-ttu-id="9992c-139">Installé de [Java Oracle 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html)</span><span class="sxs-lookup"><span data-stu-id="9992c-139">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="9992c-140">Pare-feu configuré comme indiqué dans la [configuration réseau requise](https://docs.microsoft.com/cloud-app-security/network-requirements)</span><span class="sxs-lookup"><span data-stu-id="9992c-140">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="9992c-p106">Vous devez avoir plus d’informations sur votre **hôte de journal système distant** et du **numéro de port Syslot**. Un administrateur réseau ou un administrateur de sécurité doit être en mesure de vous aider à trouver ces informations.</span><span class="sxs-lookup"><span data-stu-id="9992c-p106">You must have details about your **Remote syslog host** and **Syslot port number**. A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="9992c-143">Vous devez accepter les termes du contrat de [licence logiciel](https://go.microsoft.com/fwlink/?linkid=862491) télécharger le [fichier JAR de](https://go.microsoft.com/fwlink/?linkid=838596) vous devrez intégrer votre serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="9992c-143">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="integrate-office-365-cloud-app-security"></a><span data-ttu-id="9992c-144">Intégrer la sécurité d’application Office 365 dans le nuage</span><span class="sxs-lookup"><span data-stu-id="9992c-144">Integrate Office 365 Cloud App Security</span></span>
    
### <a name="step-1-set-it-up-in-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="9992c-145">Étape 1 : Configurer dans le portail Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="9992c-145">Step 1: Set it up in the Office 365 Cloud App Security portal</span></span>

1. <span data-ttu-id="9992c-p107">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.)</span><span class="sxs-lookup"><span data-stu-id="9992c-p107">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="9992c-148">Accédez à des **alertes** \> **Gestion avancée des alertes**.</span><span class="sxs-lookup"><span data-stu-id="9992c-148">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="9992c-p108">Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="9992c-p108">Choose **Go to Office 365 Cloud App Security**. </span></span><br/>
    <span data-ttu-id="9992c-150">![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-150">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="9992c-151">Cliquez sur **paramètres** \> **extensions de sécurité**.</span><span class="sxs-lookup"><span data-stu-id="9992c-151">Click **Settings** \> **Security extensions**.</span></span><br/>
<span data-ttu-id="9992c-152">![Choisissez Paramètres > extensions de sécurité](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-152">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

5. <span data-ttu-id="9992c-153">Choisissez **SIEM ajouter des agents**.</span><span class="sxs-lookup"><span data-stu-id="9992c-153">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="9992c-154">![Choisissez agent SIEM ajouter.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-154">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
6. <span data-ttu-id="9992c-155">Cliquez sur **Démarrer l’Assistant**.</span><span class="sxs-lookup"><span data-stu-id="9992c-155">Choose **Start wizard**.</span></span><br/><span data-ttu-id="9992c-156">![Obtenir de l’aide ou de démarrer l’Assistant](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-156">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
7. <span data-ttu-id="9992c-p109">Dans l’étape **Général** , spécifiez un nom et **Sélectionnez votre format SIEM** et définir des **Paramètres avancés** qui sont pertinents pour ce format. Puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9992c-p109">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format. Then choose **Next**.</span></span><br/><span data-ttu-id="9992c-159">![Spécifiez le nom et type](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-159">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
8. <span data-ttu-id="9992c-p110">Dans l’étape de **Journal système distant** , spécifiez l’adresse IP ou le nom d’hôte de l' **hôte de journal système distant** et le **numéro de port de journal système**. Sélectionnez TCP ou UDP comme protocole de journal système distant. (Vous pouvez travailler avec votre administrateur réseau ou à un administrateur de sécurité pour obtenir ces informations si vous ne les avez). Puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="9992c-p110">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**. Select TCP or UDP as the Remote Syslog protocol. (You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="9992c-163">![Spécifier les détails du journal système distant](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-163">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
9. <span data-ttu-id="9992c-164">Dans l’étape de **Types de données** , effectuez l’une des opérations suivantes, puis cliquez sur **suivant**:</span><span class="sxs-lookup"><span data-stu-id="9992c-164">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="9992c-165">Conservez la valeur par défaut de **Toutes les alertes**</span><span class="sxs-lookup"><span data-stu-id="9992c-165">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="9992c-166">OU</span><span class="sxs-lookup"><span data-stu-id="9992c-166">OR</span></span>
    - <span data-ttu-id="9992c-p111">Cliquez sur **toutes les alertes**, puis cliquez sur **filtres spécifiques**. Définir des filtres pour sélectionner les types d’alertes que vous voulez envoyer à votre serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="9992c-p111">Click **All alerts**, and then choose **Specific filters**. Define filters to select the kinds of alerts you want to send to your SIEM server. </span></span><br/><span data-ttu-id="9992c-169">![Étape de Types de données de l’Assistant](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-169">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
10. <span data-ttu-id="9992c-170">Dans l’écran Félicitations, copiez le jeton et enregistrer pour plus tard.</span><span class="sxs-lookup"><span data-stu-id="9992c-170">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![Écran de l’agent créé SIEM](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="9992c-p112">À ce stade, vous avez configuré un agent SIEM dans Office 365 Cloud application sécurité, mais votre intégration du serveur SIEM n’est pas encore terminée. Passez à l’étape suivante pour continuer votre intégration du serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="9992c-p112">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished. Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="9992c-p113">Une fois que vous cliquez sur Fermer et quitter l’Assistant, dans l’écran d’extensions de sécurité, vous pouvez voir l’agent SIEM ajouté au cours de la table. Il affiche un état **créé** tant qu’il est connecté ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="9992c-p113">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table. It will show a status of **Created** until it's connected later.</span></span>

![Agent SIEM créé](media/SIEMAgentCreated.png)
    
### <a name="step-2-download-the-jar-file-and-run-it-on-your-server"></a><span data-ttu-id="9992c-177">Étape 2 : Téléchargez le fichier JAR et exécutez-le sur votre serveur</span><span class="sxs-lookup"><span data-stu-id="9992c-177">Step 2: Download the JAR file and run it on your server</span></span>

1. <span data-ttu-id="9992c-p114">Télécharger [Microsoft Cloud application sécurité SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) et décompressez le dossier. (Vous devez accepter [le contrat de licence](https://go.microsoft.com/fwlink/?linkid=862491) pour continuer.)</span><span class="sxs-lookup"><span data-stu-id="9992c-p114">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder. (You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="9992c-180">Extrayez le fichier JAR à partir du dossier compressé et exécutez-le sur votre serveur.</span><span class="sxs-lookup"><span data-stu-id="9992c-180">Extract the .jar file from the zipped folder and run it on your server.</span></span>
    
3. <span data-ttu-id="9992c-181">Après avoir exécuté le fichier, exécutez la commande suivante : commande :</span><span class="sxs-lookup"><span data-stu-id="9992c-181">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
#### <a name="important-notes"></a><span data-ttu-id="9992c-182">Remarques importantes</span><span class="sxs-lookup"><span data-stu-id="9992c-182">Important notes</span></span>

- <span data-ttu-id="9992c-183">Le nom de fichier peut varier en fonction de la version de l’agent SIEM.</span><span class="sxs-lookup"><span data-stu-id="9992c-183">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="9992c-184">Nous vous conseillons d’exécuter le remplissage JAR sur votre serveur lors de l’installation du serveur.</span><span class="sxs-lookup"><span data-stu-id="9992c-184">We recommend that you run the JAR fill on your server during server setup.</span></span>
    - <span data-ttu-id="9992c-185">**Windows**: exécuter en tant qu’une tâche planifiée, en veillant à la configuration de la tâche à **exécuter si l’utilisateur est connecté ou non** et désactivez l’option **Arrêter la tâche si elle s’exécute plu** .</span><span class="sxs-lookup"><span data-stu-id="9992c-185">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="9992c-186">**Linux**: ajouter la commande Exécuter avec un **&** à la `rc.local` fichier.</span><span class="sxs-lookup"><span data-stu-id="9992c-186">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="9992c-187">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9992c-187">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="9992c-p115">Paramètres entre crochets [] sont facultatives et doivent être utilisés uniquement si nécessaire. Utilisez les variables suivantes :</span><span class="sxs-lookup"><span data-stu-id="9992c-p115">Parameters in brackets [] are optional, and should be used only if relevant. Use the following variables:</span></span>
    - <span data-ttu-id="9992c-190">**DIRNAME** est le chemin d’accès au répertoire à utiliser pour les journaux de débogage de l’agent local.</span><span class="sxs-lookup"><span data-stu-id="9992c-190">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>
    - <span data-ttu-id="9992c-191">**Adresse [ : PORT]** est l’adresse du serveur proxy et le port que le serveur utilise pour se connecter à Internet.</span><span class="sxs-lookup"><span data-stu-id="9992c-191">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>
    - <span data-ttu-id="9992c-192">**Jeton** est le jeton de l’agent SIEM que vous avez copié dans la première procédure.</span><span class="sxs-lookup"><span data-stu-id="9992c-192">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>
    - <span data-ttu-id="9992c-193">Pour obtenir de l’aide, tapez `-h`.</span><span class="sxs-lookup"><span data-stu-id="9992c-193">To get help, type `-h`.</span></span> 
  
### <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="9992c-194">Étape 3 : Valider l’utilisation de l’agent SIEM</span><span class="sxs-lookup"><span data-stu-id="9992c-194">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="9992c-195">Assurez-vous que l’état de l’agent SIEM dans le portail Office 365 Cloud application sécurité n’est pas affiché en tant que **message erreur de connexion** ou **déconnecté** et qu’il n’existe aucune notification de l’agent.</span><span class="sxs-lookup"><span data-stu-id="9992c-195">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="9992c-196">Par exemple, nous voyons ici qu'est connecté le serveur SIEM :</span><span class="sxs-lookup"><span data-stu-id="9992c-196">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="9992c-197">![Serveur SIEM connecté](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-197">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="9992c-198">Et nous pouvons voir ici, que le serveur SIEM est déconnecté :</span><span class="sxs-lookup"><span data-stu-id="9992c-198">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="9992c-199">![Serveur SIEM ne sont ne pas connecté](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="9992c-199">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="9992c-200">Dans votre serveur/SIEM journal système, vérifiez que les alertes sont arrivées à partir de la sécurité d’application Office 365 dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="9992c-200">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="regenerating-your-token"></a><span data-ttu-id="9992c-201">Régénération votre jeton</span><span class="sxs-lookup"><span data-stu-id="9992c-201">Regenerating your token</span></span>

<span data-ttu-id="9992c-p116">Si vous perdez votre jeton, vous pouvez toujours le restaurer. Dans le tableau, recherchez la ligne pour l’agent SIEM. Cliquez sur le bouton de sélection, puis cliquez sur **Régénérer le jeton**.</span><span class="sxs-lookup"><span data-stu-id="9992c-p116">If you lose your token, you can always regenerate it. In the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Regenerate token**.</span></span>

![Régénérer un jeton en cliquant sur le bouton de sélection de l’agent SIEM](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
## <a name="editing-your-siem-agent"></a><span data-ttu-id="9992c-206">Modification de votre agent SIEM</span><span class="sxs-lookup"><span data-stu-id="9992c-206">Editing your SIEM agent</span></span>

<span data-ttu-id="9992c-p117">Pour modifier votre SIEM agent, dans le tableau, recherchez la ligne pour l’agent SIEM. Cliquez sur le bouton de sélection, puis cliquez sur **Modifier**. Si vous modifiez l’agent SIEM, il est inutile réexécuter le fichier .jar ; Il met à jour automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9992c-p117">To edit your SIEM agent, in the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Edit**. If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.</span></span>

![Pour modifier votre agent SIEM, choisissez le bouton de sélection, puis cliquez sur Modifier.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
## <a name="deleting-your-siem-agent"></a><span data-ttu-id="9992c-211">Suppression de l’agent SIEM</span><span class="sxs-lookup"><span data-stu-id="9992c-211">Deleting your SIEM agent</span></span>

<span data-ttu-id="9992c-p118">Pour supprimer votre SIEM agent, dans le tableau, recherchez la ligne pour l’agent SIEM. Cliquez sur le bouton de sélection, puis cliquez sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="9992c-p118">To delete your SIEM agent, in the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Delete**.</span></span>

![Pour supprimer un agent SIEM, choisissez le bouton de sélection, puis choisissez Supprimer.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

## <a name="sample-logfiles"></a><span data-ttu-id="9992c-215">Fichiers journaux d’exemple</span><span class="sxs-lookup"><span data-stu-id="9992c-215">Sample logfiles</span></span>

<span data-ttu-id="9992c-216">Voici un exemple de fichier journal d’alertes pouvant être envoyées à un serveur SIEM :</span><span class="sxs-lookup"><span data-stu-id="9992c-216">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="9992c-217">Et Voici un exemple de format format CEF</span><span class="sxs-lookup"><span data-stu-id="9992c-217">And here's a sample in CEF format</span></span>


|<span data-ttu-id="9992c-218">Nom du champ Format CEF</span><span class="sxs-lookup"><span data-stu-id="9992c-218">CEF field name</span></span>  | <span data-ttu-id="9992c-219">Description</span><span class="sxs-lookup"><span data-stu-id="9992c-219">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="9992c-220">Démarrer</span><span class="sxs-lookup"><span data-stu-id="9992c-220">start</span></span>     | <span data-ttu-id="9992c-221">horodatage de l’alerte</span><span class="sxs-lookup"><span data-stu-id="9992c-221">alert timestamp</span></span>        |
|<span data-ttu-id="9992c-222">fin</span><span class="sxs-lookup"><span data-stu-id="9992c-222">end</span></span>     | <span data-ttu-id="9992c-223">horodatage de l’alerte</span><span class="sxs-lookup"><span data-stu-id="9992c-223">alert timestamp</span></span>        |
|<span data-ttu-id="9992c-224">RT</span><span class="sxs-lookup"><span data-stu-id="9992c-224">rt</span></span>     | <span data-ttu-id="9992c-225">horodatage de l’alerte</span><span class="sxs-lookup"><span data-stu-id="9992c-225">alert timestamp</span></span>        |
|<span data-ttu-id="9992c-226">msg</span><span class="sxs-lookup"><span data-stu-id="9992c-226">msg</span></span>     | <span data-ttu-id="9992c-227">description de l’alerte, comme indiqué dans le portail Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="9992c-227">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="9992c-228">sUser</span><span class="sxs-lookup"><span data-stu-id="9992c-228">suser</span></span>     | <span data-ttu-id="9992c-229">utilisateur de l’objet de l’alerte</span><span class="sxs-lookup"><span data-stu-id="9992c-229">alert subject user</span></span>        |
|<span data-ttu-id="9992c-230">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="9992c-230">destinationServiceName</span></span>     | <span data-ttu-id="9992c-231">alerte d’application, telles que Office 365, SharePoint ou OneDrive d’origine</span><span class="sxs-lookup"><span data-stu-id="9992c-231">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="9992c-232">csLabel</span><span class="sxs-lookup"><span data-stu-id="9992c-232">csLabel</span></span>     | <span data-ttu-id="9992c-p119">Varie (étiquettes ont des significations différentes). En règle générale, les étiquettes sont explicites, comme targetObjects.</span><span class="sxs-lookup"><span data-stu-id="9992c-p119">Varies (labels have different meanings). Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="9992c-235">cs</span><span class="sxs-lookup"><span data-stu-id="9992c-235">cs</span></span>     | <span data-ttu-id="9992c-236">Informations correspondant à une étiquette (par exemple, l’utilisateur cible d’une alerte en fonction de l’exemple d’étiquette)</span><span class="sxs-lookup"><span data-stu-id="9992c-236">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |
  
## <a name="next-steps"></a><span data-ttu-id="9992c-237">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9992c-237">Next steps</span></span>

- [<span data-ttu-id="9992c-238">Activités d’utilisation après avoir déployé la sécurité des applications cloud Office 365</span><span class="sxs-lookup"><span data-stu-id="9992c-238">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="9992c-239">Passez en revue et effectuer une action sur les alertes</span><span class="sxs-lookup"><span data-stu-id="9992c-239">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="9992c-240">Vos adresses IP pour simplifier la gestion de groupe</span><span class="sxs-lookup"><span data-stu-id="9992c-240">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

