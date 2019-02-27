---
title: Utilisation des règles de flux de courrier pour définir le seuil de probabilité de courrier indésirable (SCL) dans les messages
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
ms.collection:
- M365-security-compliance
description: Vous pouvez créer une règle de transport qui définit le seuil de probabilité de courrier indésirable (SCL) d'un message électronique. Le SCL mesure la probabilité qu'un message soit un courrier indésirable. Le courrier indésirable représente les messages électroniques non sollicités (et généralement indésirables). Le service prend différentes mesures en ce qui concerne le message en fonction de la notation SCL. Par exemple, vous pouvez contourner le filtrage de contenu de courrier indésirable pour les messages envoyés par des membres de votre organisation, car vous pensez qu'un message envoyé en interne par un collègue n'est pas un courrier indésirable. L'utilisation des règles de transport pour définir la valeur SCL d'un message vous offre un contrôle accru en matière de gestion du courrier indésirable.
ms.openlocfilehash: dfce98aa9d4fec25a06674eb68d6e00ae2964e87
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275624"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a><span data-ttu-id="3107a-108">Utilisation des règles de flux de courrier pour définir le seuil de probabilité de courrier indésirable (SCL) dans les messages</span><span class="sxs-lookup"><span data-stu-id="3107a-108">Use mail flow rules to set the spam confidence level (SCL) in messages</span></span>

<span data-ttu-id="3107a-p102">Vous pouvez créer une règle de transport qui définit le seuil de probabilité de courrier indésirable (SCL) d'un message électronique. Le SCL mesure la probabilité qu'un message soit un courrier indésirable. Le courrier indésirable représente les messages électroniques non sollicités (et généralement indésirables). Le service prend différentes mesures en ce qui concerne le message en fonction de la notation SCL. Par exemple, vous pouvez contourner le filtrage de contenu de courrier indésirable pour les messages envoyés par des membres de votre organisation, car vous pensez qu'un message envoyé en interne par un collègue n'est pas un courrier indésirable. L'utilisation des règles de transport pour définir la valeur SCL d'un message vous offre un contrôle accru en matière de gestion du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="3107a-p102">You can create a transport rule that sets the spam confidence level (SCL) of an email message. The SCL is a measure of how likely a message is to be spam. Spam is unsolicited (and typically unwanted) email messages. The service takes different action on a message depending on its SCL rating. For example, you might want to bypass spam content filtering for messages that are sent from people inside your organization because you trust that a message sent internally from a colleague isn't spam. Using transport rules to set the SCL value of a message gives you increased control in handling spam.</span></span> 
  
 <span data-ttu-id="3107a-115">**Ce qu'il faut savoir avant de commencer**</span><span class="sxs-lookup"><span data-stu-id="3107a-115">**What do you need to know before you begin?**</span></span>
  
- <span data-ttu-id="3107a-116">Durée estimée de la procédure : 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="3107a-116">Estimated time to complete this procedure: 10 minutes.</span></span>
    
- <span data-ttu-id="3107a-p103">Des autorisations doivent vous être attribuées avant de pouvoir effectuer cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée «règles de transport» dans Feature perMissions [in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) ou permissions [in EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="3107a-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) or [Feature permissions in EOP](eop/feature-permissions-in-eop.md).</span></span> 
    
- <span data-ttu-id="3107a-119">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="3107a-119">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
### <a name="to-create-a-transport-rule-that-sets-the-scl-of-a-message"></a><span data-ttu-id="3107a-120">Pour créer une règle de transport définissant la valeur SCL d'un message</span><span class="sxs-lookup"><span data-stu-id="3107a-120">To create a transport rule that sets the SCL of a message</span></span>

1. <span data-ttu-id="3107a-121">Dans le Centre d'administration Exchange (CAE), choisissez **Flux de messagerie** \> **Règles**.</span><span class="sxs-lookup"><span data-stu-id="3107a-121">In the Exchange admin center (EAC), choose **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="3107a-122">Cliquez sur **Nouveau**![Icône Ajouter](media/ITPro-EAC-AddIcon.gif), puis sélectionnez **Créer une règle**.</span><span class="sxs-lookup"><span data-stu-id="3107a-122">Choose **New**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="3107a-123">Indiquez le nom de la règle.</span><span class="sxs-lookup"><span data-stu-id="3107a-123">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="3107a-124">Choisissez **Plus d'options** et, sous **Appliquer cette règle si**, indiquez une condition qui déclenchera l'action que vous allez définir pour cette règle (c'est-à-dire la valeur SCL).</span><span class="sxs-lookup"><span data-stu-id="3107a-124">Choose **More options**, and then under **Apply this rule if**, specify a condition that will trigger the action you'll be setting for this rule (which is to set the SCL value).</span></span>
    
    <span data-ttu-id="3107a-125">Par exemple, vous pouvez définir **L'expéditeur** \> **est interne/externe** et, dans la boîte de dialogue **Sélectionner l'emplacement de l'expéditeur**, choisir **À l'intérieur de l'organisation**, puis cliquer sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3107a-125">For example, you can set **The sender** \> **is internal/external**, and then in the **select sender location** dialog box, select **Inside the organization**, and choose **ok**.</span></span><br/>
    <span data-ttu-id="3107a-126">![Sélectionner l'emplacement de l'expéditeur](media/EOP-ETR-SetSCL-1.jpg)</span><span class="sxs-lookup"><span data-stu-id="3107a-126">![Select sender location](media/EOP-ETR-SetSCL-1.jpg)</span></span>
  
5. <span data-ttu-id="3107a-127">Sous **Effectuer les opérations suivantes**, sélectionnez **Modifier les propriétés des messages** \> **Définir le seuil de probabilité de courrier indésirable (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="3107a-127">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
  
6. <span data-ttu-id="3107a-128">Dans la boîte de dialogue **spécifier la valeur SCL**, sélectionnez l'une des valeurs suivantes, puis cliquez sur **OK**:</span><span class="sxs-lookup"><span data-stu-id="3107a-128">In the **specify SCL** dialog box, select one of the following values, and choose **ok**:</span></span>
    
  - <span data-ttu-id="3107a-129">**Contourner le filtrage du courrier indésirable**: cette option définit la valeur SCL sur -1, ce qui signifie qu'aucun filtrage de contenu ne sera effectué.</span><span class="sxs-lookup"><span data-stu-id="3107a-129">**Bypass spam filtering** - This sets the SCL to -1, which means that content filtering won't be performed.</span></span> 
    
  - <span data-ttu-id="3107a-130">**0-4**: lorsque vous définissez la valeur SCL sur l'une de ces valeurs, le message est transmis au filtre de contenu en vue d'un traitement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="3107a-130">**0-4** - When you set the SCL to one of these values, the message will be passed along to the content filter for additional processing.</span></span> 
    
  - <span data-ttu-id="3107a-p104">**5, 6**: lorsque vous définissez la valeur SCL sur l'une de ces valeurs, l'action spécifiée pour **Courrier indésirable** dans les stratégies de filtre de contenu applicables est appliquée. Par défaut, l'action consiste à envoyer le message vers le dossier Courrier indésirable du destinataire.</span><span class="sxs-lookup"><span data-stu-id="3107a-p104">**5, 6** - When you set the SCL to one of these values, the action specified for **Spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
  - <span data-ttu-id="3107a-p105">**7-9**: lorsque vous définissez la valeur SCL sur l'une de ces valeurs, l'action spécifiée pour **Probabilité élevée de courrier indésirable** dans les stratégies de filtre de contenu applicables est appliquée. Par défaut, l'action consiste à envoyer le message vers le dossier Courrier indésirable du destinataire.</span><span class="sxs-lookup"><span data-stu-id="3107a-p105">**7-9** - When you set the SCL to one of these values, the action specified for **High confidence spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
    <span data-ttu-id="3107a-p106">Pour plus d'informations sur la configuration des stratégies de filtre de contenu, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Pour plus d'informations sur les valeurs SCL du service, voir [Seuils de probabilité de courrier indésirable](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="3107a-p106">For more information about configuring your content filter policies, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
7. <span data-ttu-id="3107a-137">Spécifiez des propriétés supplémentaires pour la règle, puis choisissez **enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3107a-137">Specify additional properties for the rule, and choose **save**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="3107a-138">Pour plus d'informations sur les propriétés supplémentaires que vous pouvez sélectionner ou spécifier pour cette règle, voir [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span><span class="sxs-lookup"><span data-stu-id="3107a-138">For more information about the additional properties you can select or specify for this rule, see [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span></span> 
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="3107a-139">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="3107a-139">How do you know this worked?</span></span>

<span data-ttu-id="3107a-p107">Pour vous assurer que cette procédure fonctionne correctement, envoyez un message électronique à un membre de votre organisation et vérifiez que l'action effectuée sur le message correspond à celle prévue. Par exemple, si vous avez **défini le seuil de probabilité de courrier indésirable (SCL)** sur **Contourner le filtrage du courrier indésirable**, le message doit être envoyé vers la boîte de réception du destinataire spécifié. Cependant, si vous avez **défini le seuil de probabilité de courrier indésirable (SCL)** sur **9** et que l'action **Probabilité élevée de courrier indésirable** pour les stratégies de filtre de contenu applicables consiste à déplacer le message vers le dossier Courrier indésirable, le message doit être envoyé vers le dossier Courrier indésirable du destinataire spécifié.</span><span class="sxs-lookup"><span data-stu-id="3107a-p107">To verify that this procedure is working correctly, send an email message to someone inside your organization, and verify that the action performed on the message is as expected. For example, if you **set the spam confidence level (SCL)** to **Bypass spam filtering**, then the message should be sent to the specified recipient's inbox. However, if you **set the spam confidence level (SCL)** to **9**, and the **High confidence spam** action for your applicable content filter policies is to move the message to the Junk Email folder, then the message should be sent to the specified recipient's Junk Email folder.</span></span> 
  

