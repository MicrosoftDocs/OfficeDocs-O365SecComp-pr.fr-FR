---
title: Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Les nouvelles fonctionnalités de chiffrement de messages Office 365 basées sur Azure information protection, votre organisation peut utiliser la communication de messagerie protégée avec des personnes à l'intérieur et à l'extérieur de votre organisation. Les nouvelles fonctionnalités de OME fonctionnent avec d'autres organisations Office 365, Outlook.com, Gmail et d'autres services de messagerie.
ms.openlocfilehash: ea8756d08b1c172c433d6cd8ad1752c4c7ad64e9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260752"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="ead24-104">Configurer les nouvelles fonctionnalités de chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="ead24-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="ead24-105">Les nouvelles fonctionnalités de chiffrement de messages Office 365 (OME) permettent aux organisations de partager des courriers électroniques protégés avec quiconque sur n'importe quel appareil.</span><span class="sxs-lookup"><span data-stu-id="ead24-105">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device.</span></span> <span data-ttu-id="ead24-106">Les utilisateurs peuvent échanger des messages protégés avec d'autres organisations Office 365, ainsi que des clients non-Office 365 à l'aide de Outlook.com, Gmail et d'autres services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ead24-106">Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>

||
|:-----|
|<span data-ttu-id="ead24-107">Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="ead24-107">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="ead24-108">Cet article est destiné aux administrateurs et aux professionnels de l'informatique.</span><span class="sxs-lookup"><span data-stu-id="ead24-108">This article is intended for administrators and IT Pros.</span></span> <span data-ttu-id="ead24-109">Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ead24-109">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

<span data-ttu-id="ead24-110">Suivez les étapes ci-dessous pour vous assurer que les nouvelles fonctionnalités de OME sont disponibles dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="ead24-110">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 organization.</span></span>

## <a name="verify-that-azure-rights-management-is-active"></a><span data-ttu-id="ead24-111">Vérifier que la gestion des droits Azure est active</span><span class="sxs-lookup"><span data-stu-id="ead24-111">Verify that Azure Rights Management is active</span></span>

<span data-ttu-id="ead24-112">Les nouvelles fonctionnalités OME tirent parti des fonctionnalités de protection d'Azure [Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), la technologie utilisée par [Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) pour protéger les messages électroniques et les documents via le chiffrement et les contrôles d'accès.</span><span class="sxs-lookup"><span data-stu-id="ead24-112">The new OME capabilities leverage the protection features in [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) to protect emails and documents via encryption and access controls.</span></span>

<span data-ttu-id="ead24-113">La seule condition requise pour l'utilisation des nouvelles fonctionnalités OME est que la [gestion des droits Azure](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) doit être activée dans le client de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ead24-113">The only prerequisite for using the new OME capabilities is that [Azure Rights Management](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your organization's tenant.</span></span> <span data-ttu-id="ead24-114">Si c'est le cas, Office 365 active automatiquement les nouvelles fonctionnalités OME et vous n'avez rien à faire.</span><span class="sxs-lookup"><span data-stu-id="ead24-114">If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span>

<span data-ttu-id="ead24-115">Azure RMS est également activé automatiquement pour la plupart des plans éligibles, de sorte que vous n'avez probablement pas à faire quoi que ce soit.</span><span class="sxs-lookup"><span data-stu-id="ead24-115">Azure RMS is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either.</span></span> <span data-ttu-id="ead24-116">Pour plus d'informations, rePortez-vous à la rubrique [activation d'Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .</span><span class="sxs-lookup"><span data-stu-id="ead24-116">See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more information.</span></span>

>[!IMPORTANT]
><span data-ttu-id="ead24-117">Si vous utilisez le service AD RMS (Active Directory Rights Management) avec Exchange Online, vous devez [migrer vers Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) avant de pouvoir utiliser les nouvelles fonctionnalités de ome.</span><span class="sxs-lookup"><span data-stu-id="ead24-117">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities.</span></span> <span data-ttu-id="ead24-118">OME n'est pas compatible avec AD RMS.</span><span class="sxs-lookup"><span data-stu-id="ead24-118">OME is not compatible with AD RMS.</span></span>  

<span data-ttu-id="ead24-119">Pour plus d'informations, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ead24-119">For more information, see:</span></span>

- <span data-ttu-id="ead24-120">[Quels sont les abonnements nécessaires pour utiliser les nouvelles fonctionnalités d'ome?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) pour vérifier si votre plan d'abonnement inclut Azure information protection (qui inclut la fonctionnalité AD RMS).</span><span class="sxs-lookup"><span data-stu-id="ead24-120">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes Azure RMS functionality).</span></span>
- <span data-ttu-id="ead24-121">[Azure information protection](https://azure.microsoft.com/en-us/services/information-protection/) pour plus d'informations sur l'achat d'un abonnement éligible.</span><span class="sxs-lookup"><span data-stu-id="ead24-121">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-azure-rights-management"></a><span data-ttu-id="ead24-122">Activation manuelle de la gestion des droits Azure</span><span class="sxs-lookup"><span data-stu-id="ead24-122">Manually activating Azure Rights Management</span></span>

<span data-ttu-id="ead24-123">Si vous avez désactivé Azure RMS, ou s'il n'a pas été activé automatiquement pour une raison quelconque, vous pouvez l'activer manuellement dans:</span><span class="sxs-lookup"><span data-stu-id="ead24-123">If you disabled Azure RMS, or if it was not automatically activated for any reason, you can activate it manually in the:</span></span>

- <span data-ttu-id="ead24-124">**Centre d'administration office 365**: Découvrez [Comment activer Azure Rights Management à partir du centre d'administration Office 365](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="ead24-124">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions.</span></span>
- <span data-ttu-id="ead24-125">**Portail Azure**: Découvrez [Comment activer Azure Rights Management à partir du portail Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="ead24-125">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span>

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="ead24-126">Configurer la gestion de votre clé de client Azure information protection</span><span class="sxs-lookup"><span data-stu-id="ead24-126">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="ead24-127">Cette étape est facultative.</span><span class="sxs-lookup"><span data-stu-id="ead24-127">This is an optional step.</span></span> <span data-ttu-id="ead24-128">Autoriser Microsoft à gérer la clé racine pour Azure information protection est le paramètre par défaut et meilleure pratique recommandée pour la plupart des clients Office 365.</span><span class="sxs-lookup"><span data-stu-id="ead24-128">Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants.</span></span> <span data-ttu-id="ead24-129">Si c'est le cas, aucune action n'est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ead24-129">If this is the case, you don't need to do anything.</span></span>

<span data-ttu-id="ead24-130">Il existe de nombreuses raisons, telles que les exigences de conformité, qui peuvent nécessiter la génération et la gestion de votre propre clé racine (également appelée créer votre propre clé (BYOK)).</span><span class="sxs-lookup"><span data-stu-id="ead24-130">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)).</span></span> <span data-ttu-id="ead24-131">Dans ce cas, nous vous recommandons d'effectuer les étapes requises avant de configurer les nouvelles fonctionnalités de OME.</span><span class="sxs-lookup"><span data-stu-id="ead24-131">If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities.</span></span> <span data-ttu-id="ead24-132">Pour plus d'informations, consultez [la rubrique planification et implémentation de votre clé de client Azure information protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .</span><span class="sxs-lookup"><span data-stu-id="ead24-132">See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span>

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="ead24-133">Vérifier la nouvelle configuration de OME dans Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="ead24-133">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="ead24-134">Vous pouvez vérifier que votre client Office 365 est correctement configuré pour utiliser les nouvelles fonctionnalités de OME dans [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="ead24-134">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="ead24-135">[Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) à l'aide d'un compte disposant d'autorisations d'administrateur général dans votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="ead24-135">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="ead24-136">Exécutez la cmdlet Get-IRMConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ead24-136">Run the Get-IRMConfiguration cmdlet.</span></span>

     <span data-ttu-id="ead24-137">Vous devriez voir une valeur de $True pour le paramètre AzureRMSEnabled, qui indique que OME est configuré dans votre client.</span><span class="sxs-lookup"><span data-stu-id="ead24-137">You should see a value of $True for the AzureRMSEnabled parameter, which indicates that OME is configured in your tenant.</span></span> <span data-ttu-id="ead24-138">Si ce n'est pas le cas, utilisez Set-IRMConfiguration pour définir la valeur de AzureRMSEnabled sur $True afin d'activer OME.</span><span class="sxs-lookup"><span data-stu-id="ead24-138">If it is not, use Set-IRMConfiguration to set the value of AzureRMSEnabled to $True to enable OME.</span></span>

3. <span data-ttu-id="ead24-139">Exécutez la cmdlet Test-IRMConfiguration à l'aide de la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="ead24-139">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="ead24-140">**Exemple** :</span><span class="sxs-lookup"><span data-stu-id="ead24-140">**Example**:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - <span data-ttu-id="ead24-141">L'envoi d'un message électronique est facultatif, mais force le système à effectuer des vérifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ead24-141">Providing a sender email is optional, but forces the system to perform additional checks.</span></span> <span data-ttu-id="ead24-142">Utilisez l'adresse de messagerie de n'importe quel utilisateur de votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="ead24-142">Use the email address of any user in your Office 365 tenant.</span></span>

     <span data-ttu-id="ead24-143">Vos résultats doivent ressembler à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="ead24-143">Your results should be similar to:</span></span>

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

   - <span data-ttu-id="ead24-144">Le nom de votre organisation Office 365 remplacera *contoso*.</span><span class="sxs-lookup"><span data-stu-id="ead24-144">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="ead24-145">Les noms de modèle par défaut peuvent être différents de ceux affichés ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ead24-145">The default template names may be different from those displayed above.</span></span> <span data-ttu-id="ead24-146">Pour plus d'informations, rePortez-vous à la rubrique [Configuring and Managing Templates for Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .</span><span class="sxs-lookup"><span data-stu-id="ead24-146">See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

4. <span data-ttu-id="ead24-147">Exécutez la cmdlet Remove-PSSession pour vous déconnecter du service gestion des droits.</span><span class="sxs-lookup"><span data-stu-id="ead24-147">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="ead24-148">Étapes suivantes: définir des règles de flux de messagerie pour utiliser les nouvelles fonctionnalités de OME</span><span class="sxs-lookup"><span data-stu-id="ead24-148">Next steps: Define mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="ead24-149">S'il existe des règles de flux de messagerie précédemment configurées pour chiffrer les messages électroniques dans votre organisation Office 365, vous devez mettre à jour les règles existantes pour utiliser les nouvelles fonctionnalités de OME.</span><span class="sxs-lookup"><span data-stu-id="ead24-149">If there are previously configured mail flow rules to encrypt email in your Office 365 organization, you need to update the existing rules to use the new OME capabilities.</span></span> <span data-ttu-id="ead24-150">Pour les nouveaux déploiements, vous devez créer des règles de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ead24-150">For new deployments, you need to create new mail flow rules.</span></span>

>[!IMPORTANT]
><span data-ttu-id="ead24-151">Si vous ne mettez pas à jour les règles de flux de messagerie existantes, vos utilisateurs continueront à recevoir des messages chiffrés qui utilisent le format de pièce jointe HTML précédent au lieu de la nouvelle expérience OME transparente.</span><span class="sxs-lookup"><span data-stu-id="ead24-151">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new seamless OME experience.</span></span>

<span data-ttu-id="ead24-152">Les règles de flux de messagerie déterminent les conditions dans lesquelles les messages électroniques doivent être chiffrés, ainsi que les conditions de suppression de ce chiffrement.</span><span class="sxs-lookup"><span data-stu-id="ead24-152">Mail flow rules determine under what conditions email messages should be encrypted, as well as conditions for removing that encryption.</span></span> <span data-ttu-id="ead24-153">Lorsque vous définissez une action pour une règle, tous les messages qui correspondent aux conditions de la règle sont chiffrés lorsqu'ils sont envoyés.</span><span class="sxs-lookup"><span data-stu-id="ead24-153">When you set an action for a rule, any messages that match the rule conditions are encrypted when they're sent.</span></span>
  
<span data-ttu-id="ead24-154">Pour obtenir la procédure de création des règles de flux de messagerie pour OME, consultez la rubrique [define mail Flow Rules to Encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="ead24-154">For steps on creating mail flow rules for OME, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>

<span data-ttu-id="ead24-155">Pour mettre à jour les règles existantes afin d'utiliser les nouvelles fonctionnalités OME:</span><span class="sxs-lookup"><span data-stu-id="ead24-155">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="ead24-156">Dans le centre d'administration Office 365, accédez à centre d'administration **_GT_ Exchange**.</span><span class="sxs-lookup"><span data-stu-id="ead24-156">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>
2. <span data-ttu-id="ead24-157">Dans le centre d'administration Exchange, accédez à **_GT_ mail Flow Rules**.</span><span class="sxs-lookup"><span data-stu-id="ead24-157">In the Exchange admin center, go to **Mail flow > Rules**.</span></span>
3. <span data-ttu-id="ead24-158">Pour chaque règle, dans **effectuer les opérations suivantes**:</span><span class="sxs-lookup"><span data-stu-id="ead24-158">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="ead24-159">Sélectionnez **modifier la sécurité des messages**.</span><span class="sxs-lookup"><span data-stu-id="ead24-159">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="ead24-160">Sélectionnez **appliquer le chiffrement de messages Office 365 et protection des droits**.</span><span class="sxs-lookup"><span data-stu-id="ead24-160">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="ead24-161">Sélectionnez un modèle RMS dans la liste.</span><span class="sxs-lookup"><span data-stu-id="ead24-161">Select an RMS template from the list.</span></span>
    - <span data-ttu-id="ead24-162">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ead24-162">Select **Save**.</span></span>
    - <span data-ttu-id="ead24-163">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="ead24-163">Select **OK**.</span></span>
