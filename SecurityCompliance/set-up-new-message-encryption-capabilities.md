---
title: Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Les nouvelles fonctionnalités de chiffrement de messages Office 365 basées sur Azure information protection, votre organisation peut utiliser la communication de messagerie protégée avec des personnes à l'intérieur et à l'extérieur de votre organisation. Les nouvelles fonctionnalités de OME fonctionnent avec d'autres organisations Office 365, Outlook.com, Gmail et d'autres services de messagerie.
ms.openlocfilehash: fd237e537aa1ff961d2d975b3b30f4a51744ba7c
ms.sourcegitcommit: e24f70699021c4f4ba56508ad0afb6f65010c357
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2019
ms.locfileid: "31479650"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="1b989-104">Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="1b989-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="1b989-105">Les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME) permettent aux organisations de partager des courriers électroniques protégés avec quiconque sur n'importe quel appareil.</span><span class="sxs-lookup"><span data-stu-id="1b989-105">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device.</span></span> <span data-ttu-id="1b989-106">Les utilisateurs peuvent échanger des messages protégés avec d'autres organisations Office 365, ainsi que des clients non-Office 365 à l'aide de Outlook.com, Gmail et d'autres services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1b989-106">Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>


>[!NOTE]
><span data-ttu-id="1b989-107">Cet article est destiné aux administrateurs et aux professionnels de l'informatique.</span><span class="sxs-lookup"><span data-stu-id="1b989-107">This article is intended for administrators and IT professionals.</span></span> <span data-ttu-id="1b989-108">Si vous êtes un utilisateur final, reportez-vous à la liste des articles dans [Office 365 message Encryption (OME)](ome.md) pour obtenir des solutions appropriées.</span><span class="sxs-lookup"><span data-stu-id="1b989-108">If you're an end-user, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) for appropriate solutions.</span></span>

<span data-ttu-id="1b989-109">Suivez les étapes ci-dessous pour vous assurer que les nouvelles fonctionnalités de OME sont disponibles dans votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="1b989-109">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 tenant.</span></span>

## <a name="verify-azure-rights-management-arm-is-active"></a><span data-ttu-id="1b989-110">Vérifier que la gestion des droits Azure (ARM) est active</span><span class="sxs-lookup"><span data-stu-id="1b989-110">Verify Azure Rights Management (ARM) is active</span></span>

>[!NOTE]
><span data-ttu-id="1b989-111">Les nouvelles fonctionnalités OME tirent parti des fonctionnalités de protection d' [Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), la technologie utilisée par [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).</span><span class="sxs-lookup"><span data-stu-id="1b989-111">The new OME capabilities leverage the protection features in [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).</span></span>

<span data-ttu-id="1b989-112">La seule condition requise pour l'utilisation des nouvelles fonctionnalités OME est que [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) doit être activé dans votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="1b989-112">The only prerequisite for using the new OME capabilities is that [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your Office 365 tenant.</span></span> <span data-ttu-id="1b989-113">Si c'est le cas, Office 365 active automatiquement les nouvelles fonctionnalités OME et vous n'avez rien à faire.</span><span class="sxs-lookup"><span data-stu-id="1b989-113">If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span>

<span data-ttu-id="1b989-114">ARM est également activé automatiquement pour la plupart des plans éligibles, de sorte que vous n'avez probablement pas à faire quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="1b989-114">ARM is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either.</span></span> <span data-ttu-id="1b989-115">Pour plus d'informations, consultez la rubrique [activation d'Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .</span><span class="sxs-lookup"><span data-stu-id="1b989-115">See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more.</span></span>

>[!IMPORTANT]
><span data-ttu-id="1b989-116">Si vous utilisez le service AD RMS (Active Directory Rights Management) avec Exchange Online, vous devez [migrer vers Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) avant de pouvoir utiliser les nouvelles fonctionnalités de ome.</span><span class="sxs-lookup"><span data-stu-id="1b989-116">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities.</span></span> <span data-ttu-id="1b989-117">AD RMS n'est pas compatible avec ARM.</span><span class="sxs-lookup"><span data-stu-id="1b989-117">AD RMS is not compatible with ARM.</span></span>  

<span data-ttu-id="1b989-118">Pour plus d'informations, consultez la rubrique suivante:</span><span class="sxs-lookup"><span data-stu-id="1b989-118">For more, see:</span></span>

- <span data-ttu-id="1b989-119">[Quels sont les abonnements nécessaires pour utiliser les nouvelles fonctionnalités d'ome?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) pour vérifier si votre plan d'abonnement inclut Azure information protection (qui inclut ARM).</span><span class="sxs-lookup"><span data-stu-id="1b989-119">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes ARM).</span></span>
- <span data-ttu-id="1b989-120">[Azure information protection](https://azure.microsoft.com/en-us/services/information-protection/) pour plus d'informations sur l'achat d'un abonnement éligible.</span><span class="sxs-lookup"><span data-stu-id="1b989-120">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-arm"></a><span data-ttu-id="1b989-121">Activation manuelle du bras</span><span class="sxs-lookup"><span data-stu-id="1b989-121">Manually activating ARM</span></span>

<span data-ttu-id="1b989-122">Si vous avez désactivé ARM ou s'il n'a pas été activé automatiquement pour une raison quelconque, vous pouvez l'activer manuellement dans:</span><span class="sxs-lookup"><span data-stu-id="1b989-122">If you disabled ARM, or if it was not automatically activated for any reason, you can activated it manually in the:</span></span>

- <span data-ttu-id="1b989-123">**Centre d'administration office 365**: Découvrez [Comment activer Azure Rights Management à partir du centre d'administration Office 365](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="1b989-123">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions.</span></span>
- <span data-ttu-id="1b989-124">**Portail Azure**: Découvrez [Comment activer Azure Rights Management à partir du portail Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="1b989-124">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span>

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="1b989-125">Configurer la gestion de votre clé de client Azure information protection</span><span class="sxs-lookup"><span data-stu-id="1b989-125">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="1b989-126">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="1b989-126">This is an optional step.</span></span> <span data-ttu-id="1b989-127">Autoriser Microsoft à gérer la clé racine pour Azure information protection est le paramètre par défaut et meilleure pratique recommandée pour la plupart des clients Office 365.</span><span class="sxs-lookup"><span data-stu-id="1b989-127">Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants.</span></span> <span data-ttu-id="1b989-128">Si c'est le cas, aucune action n'est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1b989-128">If this is the case, you don't need to do anything.</span></span>

<span data-ttu-id="1b989-129">Il existe de nombreuses raisons, telles que les exigences de conformité, qui peuvent nécessiter la génération et la gestion de votre propre clé racine (également appelée créer votre propre clé (BYOK)).</span><span class="sxs-lookup"><span data-stu-id="1b989-129">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)).</span></span> <span data-ttu-id="1b989-130">Dans ce cas, nous vous recommandons d'effectuer les étapes requises avant de configurer les nouvelles fonctionnalités de OME.</span><span class="sxs-lookup"><span data-stu-id="1b989-130">If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities.</span></span> <span data-ttu-id="1b989-131">Pour plus d'informations, consultez [la rubrique planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .</span><span class="sxs-lookup"><span data-stu-id="1b989-131">See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span>

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="1b989-132">Vérifier la nouvelle configuration de OME dans Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="1b989-132">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="1b989-133">Vous pouvez vérifier que votre client Office 365 est correctement configuré pour utiliser les nouvelles fonctionnalités de OME dans [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="1b989-133">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="1b989-134">[Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) à l'aide d'un compte disposant d'autorisations d'administrateur général dans votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="1b989-134">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="1b989-135">Exécutez la cmdlet Test-IRMConfiguration à l'aide de la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="1b989-135">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="1b989-136">**Exemple**:</span><span class="sxs-lookup"><span data-stu-id="1b989-136">**Example**:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - <span data-ttu-id="1b989-137">L'envoi d'un message électronique est facultatif, mais force le système à effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1b989-137">Providing a sender email is optional, but forces the system to perform additional checks.</span></span> <span data-ttu-id="1b989-138">Utilisez l'adresse de messagerie de n'importe quel utilisateur de votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="1b989-138">Use the email address of any user in your Office 365 tenant.</span></span> 

     <span data-ttu-id="1b989-139">Vos résultats doivent ressembler à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="1b989-139">Your results should be similar to:</span></span>

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not 
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

   - <span data-ttu-id="1b989-140">Le nom de votre organisation Office 365 remplacera *contoso*.</span><span class="sxs-lookup"><span data-stu-id="1b989-140">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="1b989-141">Les noms de modèle par défaut peuvent être différents de ceux affichés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1b989-141">The default template names may be different from those displayed above.</span></span> <span data-ttu-id="1b989-142">Pour plus d'informations, rePortez-vous à la rubrique [Configuring and Managing Templates for Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .</span><span class="sxs-lookup"><span data-stu-id="1b989-142">See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

3. <span data-ttu-id="1b989-143">Exécutez la cmdlet Remove-PSSession pour vous déconnecter du service gestion des droits.</span><span class="sxs-lookup"><span data-stu-id="1b989-143">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>

     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="1b989-144">Mettre à jour les règles de flux de messagerie pour utiliser les nouvelles fonctionnalités OME</span><span class="sxs-lookup"><span data-stu-id="1b989-144">Update mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="1b989-145">S'il existe des [règles de flux de messagerie](define-mail-flow-rules-to-encrypt-email.md) précédemment configurées pour chiffrer les messages électroniques dans votre client Office 365, vous devez mettre à jour ces règles existantes pour utiliser les nouvelles fonctionnalités de ome.</span><span class="sxs-lookup"><span data-stu-id="1b989-145">If there are previously configured [mail flow rules to encrypt email](define-mail-flow-rules-to-encrypt-email.md) in your Office 365 tenant, you need to update these existing rules to use the new OME capabilities.</span></span> <span data-ttu-id="1b989-146">Pour les nouveaux déploiements, cette étape n'est pas nécessaire à ce stade.</span><span class="sxs-lookup"><span data-stu-id="1b989-146">For new deployments, this step is unnecessary at this stage.</span></span>   

>[!Note]
><span data-ttu-id="1b989-147">Les règles de flux de messagerie définissent les conditions dans lesquelles les messages électroniques sont chiffrés, ainsi que le moment où le chiffrement doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="1b989-147">Mail flow rules define the conditions under which email messages are encrypted, and when encryption should be removed.</span></span> <span data-ttu-id="1b989-148">Pour plus d'informations, consultez la rubrique [définir des règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md) .</span><span class="sxs-lookup"><span data-stu-id="1b989-148">See [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md) for more.</span></span>

<span data-ttu-id="1b989-149">Pour mettre à jour les règles existantes afin d'utiliser les nouvelles fonctionnalités OME:</span><span class="sxs-lookup"><span data-stu-id="1b989-149">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="1b989-150">Dans le centre d'administration Office 365, accédez à centre d'administration **_GT_ Exchange**.</span><span class="sxs-lookup"><span data-stu-id="1b989-150">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>

2. <span data-ttu-id="1b989-151">Dans le centre d'administration Exchange, accédez à **_GT_ mail Flow Rules**.</span><span class="sxs-lookup"><span data-stu-id="1b989-151">In the Exchange admin center, go to **Mail flow > Rules**.</span></span> 
3. <span data-ttu-id="1b989-152">Pour chaque règle, dans **effectuer les opérations suivantes**:</span><span class="sxs-lookup"><span data-stu-id="1b989-152">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="1b989-153">Sélectionnez **modifier la sécurité des messages**.</span><span class="sxs-lookup"><span data-stu-id="1b989-153">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="1b989-154">Sélectionnez **appliquer le chiffrement de messages Office 365 et protection des droits**.</span><span class="sxs-lookup"><span data-stu-id="1b989-154">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="1b989-155">Sélectionnez un modèle RMS dans la liste.</span><span class="sxs-lookup"><span data-stu-id="1b989-155">Select an RMS template from the list.</span></span>
    - <span data-ttu-id="1b989-156">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1b989-156">Select **Save**.</span></span>
    - <span data-ttu-id="1b989-157">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b989-157">Select **OK**.</span></span>
  
>[!IMPORTANT]
><span data-ttu-id="1b989-158">Si vous ne mettez pas à jour les règles de flux de messagerie existantes, vos utilisateurs continueront à recevoir des messages chiffrés qui utilisent le format de pièce jointe HTML précédent au lieu des nouvelles fonctionnalités OME.</span><span class="sxs-lookup"><span data-stu-id="1b989-158">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new OME capabilities.</span></span>
