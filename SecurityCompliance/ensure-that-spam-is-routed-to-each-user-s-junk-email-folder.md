---
title: Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: L'action anti-courrier indésirable par défaut pour les clients EOP consiste à déplacer les messages identifiés comme tels vers le dossier Courrier indésirable des destinataires. Afin que cette action fonctionne sur des boîtes aux lettres locales, vous devez configurer des règles de transport Exchange sur vos serveurs Edge ou Hub locaux de manière à détecter les en-têtes de courrier indésirable ajoutés par EOP. Ces règles de transport définissent le seuil de probabilité de courrier indésirable (SCL) utilisé par la propriété SclJunkThreshold (de la cmdlet Set-OrganizationConfig) pour déplacer le courrier indésirable dans le dossier Courrier indésirable de chaque boîte aux lettres.
ms.openlocfilehash: f712e66934956bcf46215e4016501003ce9b1725
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222883"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a><span data-ttu-id="93a5b-105">Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur</span><span class="sxs-lookup"><span data-stu-id="93a5b-105">Ensure that spam is routed to each user's Junk Email folder</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93a5b-p102">Cette rubrique s'applique uniquement aux clients Exchange Online Protection (EOP) qui hébergent des boîtes aux lettres localement dans un déploiement hybride. Les clients Exchange Online dont les boîtes aux lettres sont entièrement hébergées dans Office 365 n'ont pas besoin d'exécuter ces commandes.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p102">This topic only applies to Exchange Online Protection (EOP) customers who host mailboxes on-premises in a hybrid deployment. Exchange Online customers whose mailboxes are fully-hosted in Office 365 do not need to run these commands.</span></span> 
  
<span data-ttu-id="93a5b-p103">L'action anti-courrier indésirable par défaut pour les clients EOP consiste à déplacer les messages identifiés comme tels vers le dossier Courrier indésirable des destinataires. Afin que cette action fonctionne sur des boîtes aux lettres locales, vous devez configurer des règles de transport Exchange sur vos serveurs Edge ou Hub locaux de manière à détecter les en-têtes de courrier indésirable ajoutés par EOP. Ces règles de transport définissent le seuil de probabilité de courrier indésirable (SCL) utilisé par la propriété SclJunkThreshold (de la cmdlet Set-OrganizationConfig) pour déplacer le courrier indésirable dans le dossier Courrier indésirable de chaque boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p103">The default anti-spam action for EOP customers is to move spam messages to the recipients' Junk Email folder. In order for this action to work with on-premises mailboxes, you must configure Exchange Transport rules on your on-premises Edge or Hub servers to detect spam headers added by EOP. These Transport rules set the spam confidence level (SCL) used by the SclJunkThreshold property of the Set-OrganizationConfig cmdlet to move spam into the Junk Email folder of each mailbox.</span></span> 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a><span data-ttu-id="93a5b-111">Pour ajouter des règles de transport afin d'assurer le déplacement du courrier indésirable vers le dossier Courrier indésirable à l'aide de Windows PowerShell, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="93a5b-111">To add transport rules to ensure spam is moved to the Junk Email folder by using Windows PowerShell</span></span>

1. <span data-ttu-id="93a5b-p104">Accédez au Environnement de ligne de commande Exchange Management Shell de votre serveur Exchange local. Pour apprendre à ouvrir l'environnement de ligne de commande Environnement de ligne de commande Exchange Management Shell dans votre organisation Exchange locale, reportez-vous à **Open the Shell**.</span><span class="sxs-lookup"><span data-stu-id="93a5b-p104">Access the Exchange Management Shell for your on-premises Exchange server. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**.</span></span>
    
2. <span data-ttu-id="93a5b-114">Exécutez la commande suivante pour router le courrier indésirable filtré sur le contenu dans le dossier Courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="93a5b-114">Run the following command to route content-filtered spam messages to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    <span data-ttu-id="93a5b-115">Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkContentFilteredMail.</span><span class="sxs-lookup"><span data-stu-id="93a5b-115">Where  _NameForRule_ is the name for the new rule, for example, JunkContentFilteredMail.</span></span> 
    
3. <span data-ttu-id="93a5b-116">Exécutez la commande suivante pour router les messages marqués en tant que courrier indésirable avant qu'ils atteignent le filtre de contenu dans le dossier Courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="93a5b-116">Run the following command to route messages marked as spam prior to reaching the content filter to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    <span data-ttu-id="93a5b-117">Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkMailBeforeReachingContentFilter.</span><span class="sxs-lookup"><span data-stu-id="93a5b-117">Where  _NameForRule_ is the name for the new rule, for example, JunkMailBeforeReachingContentFilter.</span></span> 
    
4. <span data-ttu-id="93a5b-118">Exécutez la commande suivante pour vous assurer que les messages provenant des expéditeurs d'une liste rouge dans la stratégie de filtre de courrier indésirable, telle que la liste d' **expéditeurs bloqués**, sont acheminés vers le dossier Courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="93a5b-118">Run the following command to ensure that messages from senders in a block list in the spam filter policy, such as the **Sender block** list, are routed to the Junk Email folder:</span></span> 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    <span data-ttu-id="93a5b-119">Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkMailInSenderBlockList.</span><span class="sxs-lookup"><span data-stu-id="93a5b-119">Where  _NameForRule_ is the name for the new rule, for example, JunkMailInSenderBlockList.</span></span> 
    
<span data-ttu-id="93a5b-p105">Si vous ne souhaitez pas utiliser l'action **Déplacer le message dans le dossier Courrier indésirable**, vous pouvez choisir une autre action parmi vos stratégies de filtrage de contenu dans le Centre d'administration Exchange. Pour plus d'informations, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Pour plus d'informations sur ces champs dans l'en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="93a5b-p105">If you do not want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93a5b-123">See also</span><span class="sxs-lookup"><span data-stu-id="93a5b-123">See also</span></span>

[<span data-ttu-id="93a5b-124">Cmdlet New-TransportRule</span><span class="sxs-lookup"><span data-stu-id="93a5b-124">New-TransportRule cmdlet</span></span>](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

