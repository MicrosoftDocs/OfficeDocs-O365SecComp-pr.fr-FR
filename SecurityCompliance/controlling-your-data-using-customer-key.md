---
title: Contrôle de vos données dans Office 365 à l'aide de la Clé client.
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
ms.collection:
- M365-security-compliance
description: Découvrez comment configurer la clé client pour Office 365 pour Exchange Online, Skype entreprise, SharePoint Online et OneDrive entreprise. Avec la clé client, vous contrôlez les clés de chiffrement de votre organisation, puis vous configurez Office 365 afin de les utiliser pour chiffrer vos données au repos dans les centres de données de Microsoft.
ms.openlocfilehash: a14a213951bc87e4106e150c88c6b1461a5e685e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218754"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="9ec2e-104">Contrôle de vos données dans Office 365 à l'aide de la Clé client.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="9ec2e-p102">Avec la clé client, vous contrôlez les clés de chiffrement de votre organisation, puis vous configurez Office 365 afin de les utiliser pour chiffrer vos données au repos dans les centres de données de Microsoft. Les données de Rest incluent des données à partir d'Exchange Online et de Skype entreprise, qui sont stockées dans des boîtes aux lettres et des fichiers stockés dans SharePoint Online et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="9ec2e-p103">Vous devez configurer Azure avant de pouvoir utiliser la clé client pour Office 365. Cette rubrique décrit les étapes à suivre pour créer et configurer les ressources Azure requises, puis fournit la procédure de configuration de la clé client dans Office 365. Une fois que vous avez terminé la configuration d'Azure, vous déterminez la stratégie et, par conséquent, les clés, à affecter aux boîtes aux lettres et aux fichiers de votre organisation. Les boîtes aux lettres et les fichiers pour lesquels vous n'affectez pas de stratégie utilisent des stratégies de chiffrement qui sont contrôlées et gérées par Microsoft. Pour plus d'informations sur la clé client ou pour obtenir une vue d'ensemble, consultez la rubrique [customEr Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9ec2e-p104">Nous vous recommandons vivement de suivre les meilleures pratiques de cette rubrique. Ces éléments sont appelés « **Conseil** » et « **important**». La clé client vous permet de contrôler les clés de chiffrement racines dont l'étendue peut être aussi importante que l'ensemble de votre organisation. Cela signifie que les erreurs comprises avec ces clés peuvent avoir un impact général et peuvent entraîner des interruptions de service ou une perte irrévocable de vos données.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="9ec2e-116">Avant de commencer la configuration de la clé client</span><span class="sxs-lookup"><span data-stu-id="9ec2e-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="9ec2e-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-117"></span></span>

<span data-ttu-id="9ec2e-p105">Avant de commencer, assurez-vous que vous disposez de la licence appropriée pour votre organisation. La clé client dans Office 365 est proposée dans Office 365 E5 ou le SKU de conformité avancée.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="9ec2e-p106">Ensuite, pour comprendre les concepts et les procédures présentés dans cette rubrique, consultez la documentation sur le [coffre de stockage de clés Azure](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . De même, familiarisez-vous avec les termes utilisés dans Azure, par exemple, [client](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="9ec2e-122">Pour fournir des commentaires sur la clé client, y compris la documentation, envoyez vos idées, suggestions et perspectives à customerkeyfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="9ec2e-123">Vue d'ensemble de la configuration de la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9ec2e-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="9ec2e-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-124"></span></span>

<span data-ttu-id="9ec2e-p107">Pour configurer la clé client, vous devez effectuer ces tâches. Le reste de cette rubrique fournit des instructions détaillées pour chaque tâche, ou des liens vers des informations supplémentaires pour chaque étape du processus.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="9ec2e-127">**Dans Azure et Microsoft FastTrack:**</span><span class="sxs-lookup"><span data-stu-id="9ec2e-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="9ec2e-p108">Vous effectuerez la plupart de ces tâches en vous connectant à distance à Azure PowerShell. Pour obtenir de meilleurs résultats, utilisez la version 4.4.0 ou une version ultérieure d'Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="9ec2e-130">Créer deux nouveaux abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="9ec2e-131">Enregistrer des abonnements Azure pour utiliser une période de rétention obligatoire</span><span class="sxs-lookup"><span data-stu-id="9ec2e-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="9ec2e-132">L'inscription peut prendre entre un et cinq jours ouvrés.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="9ec2e-133">Soumettre une demande d'activation de la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9ec2e-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="9ec2e-p109">Une fois que vous avez créé les deux nouveaux abonnements Azure, vous devez soumettre la demande d'offre de clé client appropriée en remplissant un formulaire Web hébergé dans le portail Microsoft FastTrack. **L'équipe FastTrack ne fournit pas d'assistance pour la clé client. Office utilise simplement le portail FastTrack pour vous permettre d'envoyer le formulaire et de nous aider à suivre les offres pertinentes pour la clé client**.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. **The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key**.</span></span>
  
<span data-ttu-id="9ec2e-p110">Une fois que vous avez soumis une offre de clé de client, Microsoft révise votre demande et vous avertit lorsque vous pouvez effectuer les autres tâches de configuration. Ce processus peut prendre jusqu'à cinq jours ouvrés.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="9ec2e-138">Créer un coffre-fort de clés Azure pour chaque abonnement</span><span class="sxs-lookup"><span data-stu-id="9ec2e-138">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="9ec2e-139">Attribuer des autorisations à chaque coffre-fort de clés</span><span class="sxs-lookup"><span data-stu-id="9ec2e-139">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="9ec2e-140">Activer, puis confirmer la suppression logicielle de vos coffres-forts principaux</span><span class="sxs-lookup"><span data-stu-id="9ec2e-140">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="9ec2e-141">Ajouter une clé à chaque coffre-fort de clés en créant ou en important une clé</span><span class="sxs-lookup"><span data-stu-id="9ec2e-141">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="9ec2e-142">Vérifier le niveau de récupération de vos clés</span><span class="sxs-lookup"><span data-stu-id="9ec2e-142">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="9ec2e-143">Sauvegarder le coffre de clés Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-143">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="9ec2e-144">Valider les paramètres de configuration de coffre-fort de clés Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-144">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="9ec2e-145">Obtenir l'URI de chaque clé Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="9ec2e-145">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="9ec2e-146">**Dans Office 365:**</span><span class="sxs-lookup"><span data-stu-id="9ec2e-146">**In Office 365:**</span></span>
  
<span data-ttu-id="9ec2e-147">Exchange Online et Skype entreprise:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-147">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="9ec2e-148">Créer une stratégie de chiffrement de données (DEP) à utiliser avec Exchange Online et Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-148">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="9ec2e-149">Affecter une DEP à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="9ec2e-149">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="9ec2e-150">Valider le chiffrement de boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="9ec2e-150">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="9ec2e-151">SharePoint Online et OneDrive entreprise:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-151">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="9ec2e-152">Créer une stratégie de chiffrement de données (DEP) pour chaque région de SharePoint Online et OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-152">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="9ec2e-153">Valider le chiffrement des sites de groupe, des sites d'équipe et de OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-153">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="9ec2e-154">Effectuer des tâches dans Azure Key Vault et Microsoft FastTrack pour la clé client</span><span class="sxs-lookup"><span data-stu-id="9ec2e-154">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="9ec2e-155"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-155"></span></span>

<span data-ttu-id="9ec2e-p111">Effectuez ces tâches dans Azure Key Vault afin de configurer la clé client pour Office 365. Vous devrez effectuer ces étapes, que vous souhaitiez configurer la clé client pour Exchange Online et Skype entreprise ou SharePoint Online et OneDrive entreprise ou pour tous les services pris en charge dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="9ec2e-158">Créer deux nouveaux abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-158">Create two new Azure subscriptions</span></span>
<span data-ttu-id="9ec2e-159"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-159"></span></span>

<span data-ttu-id="9ec2e-p112">Deux abonnements Azure sont requis pour la clé client. Pour une meilleure pratique, Microsoft vous recommande de créer de nouveaux abonnements Azure à utiliser avec la clé client. Les clés Azure Key Vault peuvent uniquement être autorisées pour les applications dans le même client Azure Active Directory (AAD), vous devez créer les nouveaux abonnements à l'aide du même client Azure AD utilisé avec votre organisation Office 365 où les DEPs seront attribués. Par exemple, à l'aide de votre compte professionnel ou scolaire disposant de privilèges d'administrateur général dans votre organisation Office 365. Pour obtenir la procédure détaillée, consultez la rubrique [Inscrivez-vous à Azure en tant qu'organisation](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9ec2e-p113">La clé client nécessite deux clés pour chaque stratégie de chiffrement de données (DEP). Pour ce faire, vous devez créer deux abonnements Azure. En guise de meilleure pratique, Microsoft recommande que les membres distincts de votre organisation configurent une clé dans chaque abonnement. En outre, ces abonnements Azure ne doivent être utilisés que pour administrer les clés de chiffrement pour Office 365. Cela protège votre organisation si l'un de vos opérateurs supprime accidentellement, intentionnellement ou de manière malveillante ou non des clés dont il est responsable.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="9ec2e-p114">Nous vous recommandons de configurer de nouveaux abonnements Azure uniquement utilisés pour gérer les ressources Azure Key Vault à utiliser avec la clé client. Il n'existe pas de limite pratique au nombre d'abonnements Azure que vous pouvez créer pour votre organisation. Le suivi de ces meilleures pratiques réduira l'impact de l'erreur humaine tout en aidant à gérer les ressources utilisées par la clé client.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="9ec2e-173">Soumettre une demande d'activation de la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9ec2e-173">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="9ec2e-174"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-174"></span></span>

<span data-ttu-id="9ec2e-p115">Une fois que vous avez terminé les étapes Azure, vous devrez soumettre une demande d'offre dans le [portail Microsoft FastTrack](https://fasttrack.microsoft.com/). Une fois que vous avez soumis une demande via le portail Web FastTrack, Microsoft vérifie les données de configuration du coffre de clés Azure et les informations de contact que vous avez fournies. Les sélections effectuées dans le formulaire d'offre concernant les responsables autorisés de votre organisation sont essentielles et nécessaires à la réalisation de l'enregistrement de la clé client. Les responsables de votre organisation sélectionnés dans le formulaire seront utilisés pour garantir l'authenticité de toute demande de révocation et de destruction de toutes les clés utilisées avec une stratégie de chiffrement des données de clé client. Vous devrez effectuer cette étape une fois pour activer la clé client pour la couverture Exchange Online et Skype entreprise et une deuxième fois pour activer la clé client pour SharePoint Online et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="9ec2e-180">Pour soumettre une offre d'activation de la clé client, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-180">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="9ec2e-181">À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, connectez-vous au [portail Microsoft FastTrack](https://fasttrack.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-181">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="9ec2e-182">Une fois que vous êtes connecté, accédez au **tableau de bord**.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-182">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="9ec2e-183">Choisissez **offres**, puis passez en revue la liste des offres actuelles.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-183">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="9ec2e-184">Choisissez **en savoir plus** pour l'offre qui vous concerne:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-184">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="9ec2e-185">**Exchange Online et Skype entreprise:** Sélectionnez **en savoir plus** sur la **clé client pour** l'offre Exchange.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-185">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="9ec2e-186">**SharePoint Online et OneDrive entreprise:** Choisissez **en savoir plus** sur la **clé client pour SharePoint et OneDrive entreprise** .</span><span class="sxs-lookup"><span data-stu-id="9ec2e-186">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="9ec2e-187">Sur la page Détails de l' **offre** , sélectionnez **créer une demande**.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-187">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="9ec2e-p116">Renseignez toutes les informations pertinentes et les informations demandées dans le formulaire d'offre. Prêtez particulièrement attention à vos choix pour les responsables de votre organisation autorisés à approuver la destruction permanente et irréversible des clés et des données de chiffrement. Une fois que vous avez terminé le formulaire, sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="9ec2e-191">Ce processus peut prendre jusqu'à cinq jours ouvrés une fois que Microsoft a été informé de votre demande.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-191">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="9ec2e-192">Passez à la section période de rétention obligatoire ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-192">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="9ec2e-193">Enregistrer des abonnements Azure pour utiliser une période de rétention obligatoire</span><span class="sxs-lookup"><span data-stu-id="9ec2e-193">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="9ec2e-194"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-194"></span></span>

<span data-ttu-id="9ec2e-p117">La perte temporaire ou définitive de clés de chiffrement racine peut être très perturbatrice ou même catastrophique pour les opérations de service et peut entraîner une perte de données. Pour cette raison, les ressources utilisées avec la clé client nécessitent une protection renforcée. Toutes les ressources Azure utilisées avec les mécanismes de protection de l'offre de clé client au-delà de la configuration par défaut. Les abonnements Azure peuvent être balisés ou enregistrés de manière à empêcher toute annulation immédiate et irrévocable. Il s'agit de l'enregistrement pour une période de rétention obligatoire. Les étapes requises pour enregistrer les abonnements Azure pour une période de rétention obligatoire nécessitent une collaboration avec l'équipe Office 365. Ce processus peut prendre entre un et cinq jours ouvrés. Auparavant, il était parfois appelé «ne pas annuler».</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="9ec2e-203">Avant de contacter l'équipe Office 365, vous devez effectuer les étapes suivantes pour chaque abonnement Azure que vous utilisez avec la clé client:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-203">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="9ec2e-p118">Connectez-vous à votre abonnement Azure avec Azure PowerShell. Pour obtenir des instructions, consultez la rubrique [se connecter avec Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="9ec2e-206">Exécutez la cmdlet Register-AzureRmProviderFeature pour enregistrer vos abonnements afin d'utiliser une période de rétention obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-206">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="9ec2e-p119">Contactez Microsoft pour finaliser le processus. Pour l'équipe SharePoint et OneDrive entreprise, contactez [Spock@microsoft.com](mailto:spock@microsoft.com). Pour Exchange Online et Skype entreprise, contactez [exock@microsoft.com](mailto:exock@microsoft.com). Le contrat de niveau de service (SLA) pour la fin de ce processus est de cinq jours ouvrés une fois que Microsoft a été informé (et vérifié) que vous avez enregistré vos abonnements afin d'utiliser une période de rétention obligatoire. Incluez les éléments suivants dans votre courrier:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="9ec2e-212">**Subject**: clé client pour \< *le nom de domaine complet de votre client*\></span><span class="sxs-lookup"><span data-stu-id="9ec2e-212">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="9ec2e-213">**Body**: ID d'abonnement pour lesquels vous souhaitez que la période de rétention obligatoire soit finalisée.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-213">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="9ec2e-214">Une fois que vous recevez une notification de Microsoft que l'enregistrement est terminé, vérifiez l'état de votre inscription en exécutant la cmdlet Get-AzureRmProviderFeature comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-214">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="9ec2e-215">Après avoir vérifié que la propriété **d'État** de l'inscription de la cmdlet Get-AzureRmProviderFeature renvoie la valeur **Registered**, exécutez la commande suivante pour terminer le processus:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-215">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="9ec2e-216">Créer un coffre-fort de clés Azure pour chaque abonnement</span><span class="sxs-lookup"><span data-stu-id="9ec2e-216">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="9ec2e-217"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-217"></span></span>

<span data-ttu-id="9ec2e-218">Les étapes de création d'un coffre-fort clé sont documentées dans [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), qui vous guide tout au long de l'installation et du lancement d'Azure PowerShell, de la connexion à votre abonnement Azure, de la création d'un groupe de ressources et de la création d'un coffre-fort de clés dans ce Groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-218">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="9ec2e-p120">Lorsque vous créez un coffre-fort de clés, vous devez choisir un SKU: standard ou Premium. La référence SKU standard permet de protéger les clés du coffre-fort de clés Azure avec le logiciel: il n'existe pas de protection de clé HSM (Hardware Security Module) et la référence Premium permet d'utiliser des HSM pour la protection des clés de coffre-fort. La clé client accepte les coffres clés qui utilisent l'un des deux SKU, bien que Microsoft recommande vivement d'utiliser uniquement le SKU Premium. Le coût des opérations avec des clés de l'un des deux types est le même, de sorte que la seule différence de coût est le coût par mois pour chaque clé protégée par HSM. Pour plus d'informations, consultez la rubrique [prix clé du coffre](https://azure.microsoft.com/pricing/details/key-vault/) .</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9ec2e-224">Utilisez les coffres-forts de clés SKU Premium et les clés protégées par HSM pour les données de production, et utilisez uniquement les clés et coffres-forts de clé SKU standard à des fins de test et de validation.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-224">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="9ec2e-p121">Pour chaque service Office 365 avec lequel vous utiliserez la clé client, créez un coffre-fort de clés dans chacun des deux abonnements Azure que vous avez créés. Par exemple, pour Exchange Online et Skype entreprise uniquement ou SharePoint Online et OneDrive entreprise uniquement, vous ne devez créer qu'une seule paire de coffres-forts. Pour activer la clé client pour Exchange Online et SharePoint Online, vous devez créer deux paires de coffres-forts clés.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="9ec2e-p122">Utilisez une convention d'affectation de noms pour les coffres-forts de clés reflétant l'utilisation prévue de la DEP avec laquelle vous allez associer les coffres-forts. Consultez la section Méthodes conseillées ci-dessous pour connaître les recommandations de convention d'affectation de noms.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="9ec2e-p123">Créez un ensemble distinct de coffres couplés pour chaque stratégie de chiffrement de données. Pour Exchange Online, l'étendue d'une stratégie de chiffrement de données est choisie par vous lorsque vous affectez la stratégie à la boîte aux lettres. Une boîte aux lettres ne peut avoir qu'une seule stratégie affectée, et vous pouvez créer jusqu'à 50 stratégies. Pour SharePoint Online, l'étendue d'une stratégie est l'ensemble des données d'une organisation se trouvant dans un emplacement géographique ou dans une région géographique.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="9ec2e-p124">La création de coffre-fort de clés nécessite également la création de groupes de ressources Azure, car les coffres clés nécessitent une capacité de stockage (bien que très petite) et la journalisation de coffre de clés, si elle est activée, génère également des données stockées. Pour une meilleure pratique, Microsoft recommande d'utiliser des administrateurs distincts pour gérer chaque groupe de ressources, avec l'administration alignée sur l'ensemble des administrateurs qui géreront toutes les ressources liées à la clé client correspondante.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9ec2e-p125">Pour optimiser la disponibilité, vos coffres-forts principaux doivent se trouver dans des régions proches de votre service Office 365. Par exemple, si votre organisation Exchange Online est en Amérique du Nord, placez vos coffres clés en Amérique du Nord. Si votre organisation Exchange Online est en Europe, placez vos coffres clés en Europe.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="9ec2e-p126">Utiliser un préfixe commun pour les coffres clés, et inclure une abréviation de l'utilisation et de l'étendue du coffre-fort de clés et des clés (par exemple, pour le service Contoso SharePoint où les coffres seront situés en Amérique du Nord, une paire possible de noms est contoso-O365SP-NA-VaultA1 et Contoso-O365SP-NA-VaultA2. Les noms de coffre-fort sont des chaînes uniques au sein d'Azure, de sorte que vous devrez peut-être essayer des variantes des noms souhaités au cas où les noms souhaités seraient déjà réclamés par d'autres clients Azure. Depuis juillet 2017, les noms de coffre-fort ne peuvent pas être modifiés, c'est pourquoi il est recommandé de disposer d'un plan écrit pour la configuration et d'utiliser une deuxième personne pour vérifier que le plan est exécuté correctement.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="9ec2e-p127">Si possible, créez vos coffres dans des régions non couplées. Les régions Azure couplées fournissent une haute disponibilité entre les domaines ayant échoué. Par conséquent, les paires régionales peuvent être considérées comme la région de sauvegarde de chacune d'elles. Cela signifie qu'une ressource Azure placée dans une région bénéficie automatiquement de la tolérance de panne par le biais de la région couplée. Pour cette raison, le choix des régions pour deux coffres utilisés dans une DEP lorsque les régions sont couplées signifie que seul un total de deux régions de disponibilité est en cours d'utilisation. La plupart des régions géographiques n'ont que deux régions, de sorte qu'il n'est pas encore possible de sélectionner des régions non couplées. Si possible, choisissez deux régions non couplées pour les deux coffres utilisés avec une DEP. Cette opération bénéficie d'un total de quatre régions de disponibilité. Pour plus d'informations, consultez la rubrique [services de continuité d'activité et de récupération d'urgence (BCDR): régions coupléEs Azure](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) pour obtenir la liste actuelle des paires régionales.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="9ec2e-251">Attribuer des autorisations à chaque coffre-fort de clés</span><span class="sxs-lookup"><span data-stu-id="9ec2e-251">Assign permissions to each key vault</span></span>
<span data-ttu-id="9ec2e-252"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-252"></span></span>

<span data-ttu-id="9ec2e-p128">Pour chaque coffre-fort de clés, vous devez définir trois ensembles distincts d'autorisations pour la clé client, en fonction de votre implémentation. Par exemple, vous devez définir un ensemble d'autorisations pour chacun des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="9ec2e-p129">**Administrateurs de coffre-fort principal** qui effectueront la gestion quotidienne de votre coffre-fort pour votre organisation. Ces tâches incluent Backup, Create, Get, Import, List et Restore.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="9ec2e-p130">Le jeu d'autorisations affectées aux administrateurs de coffre-fort n'inclut pas l'autorisation de suppression de clés. Cette procédure est intentionnelle et pratique importante. La suppression de clés de chiffrement n'est généralement pas effectuée, car cette opération détruit définitivement les données. Nous vous recommandons de ne pas accorder cette autorisation aux administrateurs de coffre-fort par défaut. Au lieu de cela, réservez ceci pour les contributeurs de coffre-fort principal et ne l'attribuez à un administrateur de manière courte qu'une fois qu'une bonne compréhension des conséquences est comprise.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="9ec2e-p131">Pour attribuer ces autorisations à un utilisateur dans votre organisation Office 365, connectez-vous à votre abonnement Azure avec Azure PowerShell. Pour obtenir des instructions, consultez la rubrique [se connecter avec Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="9ec2e-264">Exécutez la cmdlet Set-AzureRmKeyVaultAccessPolicy pour attribuer les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-264">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="9ec2e-265">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-265">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="9ec2e-p132">Les contributeurs de **coffre-fort de clé** qui peuvent modifier les autorisations sur le coffre-fort des clés Azure. Vous devrez modifier ces autorisations lorsque les employés quittent ou rejoignent votre équipe, ou dans la situation extrêmement rare que les administrateurs clés de coffre-fort ont besoin de l'autorisation de supprimer ou de restaurer une clé. Cet ensemble de contributeurs de coffre-fort doit recevoir le rôle de **contributeur** sur votre coffre-fort de clés. Vous pouvez attribuer ce rôle à l'aide d'Azure Resource Manager. Pour obtenir la procédure détaillée, consultez [la rubrique utiliser le contrôle d'accès basé sur un rôle pour gérer l'accès à vos ressources d'abonnement Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). L'administrateur qui crée un abonnement bénéficie implicitement de cet accès, ainsi que de la possibilité d'affecter d'autres administrateurs au rôle contributeur.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="9ec2e-p133">Si vous envisagez d'utiliser la clé client avec Exchange Online et Skype entreprise, vous devez accorder à Office 365 l'autorisation d'utiliser le coffre-fort de clés pour Exchange Online et Skype entreprise. De même, si vous avez l'intention d'utiliser la clé client avec SharePoint Online et OneDrive entreprise, vous devez ajouter des autorisations pour l'Office 365 afin d'utiliser le coffre-fort de clés pour SharePoint Online et OneDrive entreprise. Pour accorder l'autorisation à Office 365, exécutez la cmdlet **Set-AzureRmKeyVaultAccessPolicy** à l'aide de la syntaxe suivante:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="9ec2e-275">Où :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-275">Where:</span></span>
    
  - <span data-ttu-id="9ec2e-276">*VAULTNAME* est le nom du coffre-fort de clés que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-276">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="9ec2e-277">Pour Exchange Online et Skype entreprise, remplacez *Office 365 AppID* par`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="9ec2e-277">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="9ec2e-278">Pour SharePoint Online et OneDrive entreprise, remplacez *Office 365 AppID* par`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="9ec2e-278">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="9ec2e-279">Exemple: définition des autorisations pour Exchange Online et Skype entreprise:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-279">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="9ec2e-280">Exemple: définition des autorisations pour SharePoint Online et OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-280">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="9ec2e-281">Activer, puis confirmer la suppression logicielle de vos coffres-forts principaux</span><span class="sxs-lookup"><span data-stu-id="9ec2e-281">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="9ec2e-282"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-282"></span></span>

<span data-ttu-id="9ec2e-p134">Lorsque vous pouvez rapidement récupérer vos clés, il est moins probable que vous rencontriez une panne de service étendue en raison de la suppression accidentelle ou malveillante de clés. Vous devez activer cette configuration, appelée suppression récupérable, avant de pouvoir utiliser vos clés avec la clé client. L'activation de la suppression douce vous permet de récupérer des clés ou des coffres dans les 90 jours suivant la suppression sans avoir à les restaurer à partir d'une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="9ec2e-286">Pour activer la suppression logicielle sur vos coffres-forts principaux, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-286">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="9ec2e-p135">Connectez-vous à votre abonnement Azure avec Windows PowerShell. Pour obtenir des instructions, consultez la rubrique [se connecter avec Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="9ec2e-p136">Exécutez la cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . Dans cet exemple, *VAULTNAME* est le nom du coffre-fort de clés pour lequel vous activez la suppression douce:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="9ec2e-p137">Vérifiez que la suppression logicielle est configurée pour le coffre-fort de clés en exécutant la cmdlet **Get-AzureRmKeyVault** . Si la suppression logicielle est correctement configurée pour le coffre-fort de clés, la suppression logicielle est-elle activée? la propriété renvoie la valeur **true**:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="9ec2e-293">Ajouter une clé à chaque coffre-fort de clés en créant ou en important une clé</span><span class="sxs-lookup"><span data-stu-id="9ec2e-293">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="9ec2e-294"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-294"></span></span>

<span data-ttu-id="9ec2e-p138">Il existe deux façons d'ajouter des clés à un coffre-fort de clés Azure; vous pouvez créer une clé directement dans le coffre-fort de clés ou importer une clé. La création d'une clé directement dans le coffre-fort est la méthode moins compliquée, tandis que l'importation d'une clé fournit un contrôle total sur la génération de la clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="9ec2e-297">Pour créer une clé directement dans votre coffre-fort de clés, exécutez la cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-297">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="9ec2e-298">Où :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-298">Where:</span></span>
  
-  <span data-ttu-id="9ec2e-299">*VAULTNAME* est le nom du coffre-fort de clés dans lequel vous souhaitez créer la clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-299">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="9ec2e-300">*keyName* est le nom que vous souhaitez donner à la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-300">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="9ec2e-p139">Clés de nom à l'aide d'une convention d'affectation de noms similaire à celle décrite ci-dessus pour les coffres clés. De cette manière, dans les outils qui affichent uniquement le nom de la clé, la chaîne est auto-descriptive.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="9ec2e-303">Si vous avez l'intention de protéger la clé avec un HSM, vérifiez que vous spécifiez **HSM** comme valeur du paramètre _destination_ , sinon, spécifiez **Software**.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-303">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="9ec2e-304">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="9ec2e-304">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="9ec2e-305">Pour importer directement une clé dans votre coffre-fort de clés, vous devez disposer d'un module de sécurité matérielle Thales nShield.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-305">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="9ec2e-306">Certaines organisations préfèrent établir la provenance de leurs clés, et la méthode this fournit également les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-306">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="9ec2e-307">L'ensemble d'outils utilisé pour l'importation comprend l'attestation de Thales indiquant que la clé d'échange Key (KEK) utilisée pour chiffrer la clé que vous générez n'est pas exportable et qu'elle est générée à l'intérieur d'un HSM authentique fabriqué par Thales.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-307">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="9ec2e-p140">L'ensemble d'outils inclut l'attestation de Thales qui a également été générée par le World Key Vault Security sur un autoHSM authentique fabriqué par Thales. Cette attestation prouve que Microsoft utilise également du matériel Thales authentique.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="9ec2e-p141">Vérifiez auprès de votre groupe de sécurité si les attestations ci-dessus sont requises. Pour obtenir la procédure détaillée de création d'une clé locale et de son importation dans votre coffre-fort de clés, consultez [la rubrique How to Generate and Transfer My protected Keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Utilisez les instructions Azure pour créer une clé dans chaque coffre-fort de clés.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="9ec2e-313">Vérifier le niveau de récupération de vos clés</span><span class="sxs-lookup"><span data-stu-id="9ec2e-313">Check the recovery level of your keys</span></span>
<span data-ttu-id="9ec2e-314"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-314"></span></span>

<span data-ttu-id="9ec2e-p142">Office 365 nécessite que le abonnement Azure Key Vault soit défini sur do not Cancel et que les clés utilisées par la clé client aient activé la suppression douce. Vous pouvez vérifier cela en examinant le niveau de récupération de vos clés.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="9ec2e-317">Pour vérifier le niveau de récupération d'une clé, dans Azure PowerShell, exécutez la cmdlet Get-AzureKeyVaultKey comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-317">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="9ec2e-318">Si la propriété de _niveau de récupération_ renvoie une valeur autre que **récupérable + ProtectedSubscription**, vous devez consulter cette rubrique et vous assurer que vous avez suivi toutes les étapes de mise en place de l'abonnement dans la liste ne pas annuler et que vous avez activé la suppression douce sur chaque coffre-fort de votre clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-318">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="9ec2e-319">Sauvegarder le coffre de clés Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-319">Backup Azure Key Vault</span></span>
<span data-ttu-id="9ec2e-320"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-320"></span></span>

<span data-ttu-id="9ec2e-p143">Immédiatement après la création ou la modification d'une clé, effectuez une sauvegarde et stockez des copies de la sauvegarde, en ligne et hors connexion. Les copies hors connexion ne doivent pas être connectées à un réseau, par exemple dans une installation de stockage sécurisé physique ou commerciale. Au moins une copie de la sauvegarde doit être stockée à un emplacement accessible en cas de sinistre. Les objets BLOB de sauvegarde constituent le seul moyen de restaurer le matériel de clé si une clé de coffre-fort de clé est détruite définitivement ou s'il est inopérable. Les clés externes au coffre-fort Azure et qui ont été importées vers le coffre-fort Azure ne sont pas qualifiées de sauvegarde car les métadonnées nécessaires à l'utilisation de la clé par le client n'existent pas avec la clé externe. Seule une sauvegarde effectuée à partir du coffre-fort de clés Azure peut être utilisée pour les opérations de restauration avec la clé client. Par conséquent, il est essentiel qu'une sauvegarde du coffre de clés Azure soit effectuée une fois qu'une clé est chargée ou créée.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="9ec2e-328">Pour créer une sauvegarde d'une clé Azure Key Vault, exécutez la cmdlet [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-328">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="9ec2e-329">Assurez-vous que votre fichier de `.backup`sortie utilise le suffixe.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-329">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="9ec2e-p144">Le fichier de sortie résultant de cette cmdlet est chiffré et ne peut pas être utilisé en dehors du coffre-fort de clés Azure. La sauvegarde ne peut être restaurée qu'à partir de l'abonnement Azure à partir duquel la sauvegarde a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="9ec2e-p145">Pour le fichier de sortie, choisissez une combinaison de votre nom de coffre-fort et de votre nom de clé. Cela fera en sorte que le nom de fichier soit auto-descriptif. Elle garantit également que les noms de fichier de sauvegarde n'entrent pas en conflit.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="9ec2e-335">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-335">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="9ec2e-336">Valider les paramètres de configuration de coffre-fort de clés Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-336">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="9ec2e-337"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-337"></span></span>

<span data-ttu-id="9ec2e-p146">Effectuer la validation avant d'utiliser des clés dans une DEP est facultatif, mais fortement recommandé. En particulier, si vous utilisez les étapes pour configurer vos clés et coffres-forts autres que ceux décrits dans cette rubrique, vous devez valider l'intégrité de vos ressources Azure Key Vault avant de configurer la clé client.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="9ec2e-340">Pour vérifier que les opérations Get, wrapKey et unwrapKey sont activées sur vos clés, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-340">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="9ec2e-341">Exécutez la cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-341">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="9ec2e-p147">Dans la sortie, recherchez la stratégie d'accès et l'identité Exchange Online (GUID) ou l'identité SharePoint Online (GUID), selon le cas. Les trois autorisations ci-dessus doivent être affichées sous autorisations sur clés.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="9ec2e-344">Si la configuration de la stratégie d'accès est incorrecte, exécutez la cmdlet Set-AzureRmKeyVaultAccessPolicy comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-344">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="9ec2e-345">Par exemple, pour Exchange Online et Skype entreprise:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-345">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="9ec2e-346">Par exemple, pour SharePoint Online et OneDrive entreprise:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-346">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="9ec2e-347">Pour vérifier qu'une date d'expiration n'est pas définie pour vos clés, exécutez la cmdlet [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-347">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="9ec2e-p148">Une clé expirée ne peut pas être utilisée par la clé client et les opérations tentées avec une clé expirée échoueront, ce qui peut entraîner une panne de service. Il est vivement recommandé que les clés utilisées avec la clé client n'aient pas de date d'expiration. Une date d'expiration, une fois définie, ne peut pas être supprimée, mais peut être remplacée par une date différente. Si une clé doit être utilisée avec une date d'expiration définie, modifiez la valeur d'expiration sur 12/31/9999. Les clés dont la date d'expiration est définie sur une date autre que 12/31/9999 ne réussiront pas la validation d'Office 365.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="9ec2e-353">Pour modifier une date d'expiration qui a été définie sur une valeur autre que 12/31/9999, exécutez la cmdlet [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-353">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="9ec2e-354">Ne définissez pas de date d'expiration sur les clés de chiffrement que vous utilisez avec la clé client.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-354">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="9ec2e-355">Obtenir l'URI de chaque clé Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="9ec2e-355">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="9ec2e-356"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-356"></span></span>

<span data-ttu-id="9ec2e-p149">Une fois que vous avez effectué toutes les étapes dans Azure pour configurer votre coffre-fort de clés et ajouté vos clés, exécutez la commande suivante pour obtenir l'URI de la clé dans chaque coffre-fort de clés. Vous devrez utiliser ces URI lorsque vous créerez et affecterez chaque DEP plus tard, donc Enregistrez ces informations dans un endroit sûr. N'oubliez pas d'exécuter cette commande une fois pour chaque coffre-fort de clés.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="9ec2e-360">Dans Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-360">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="9ec2e-361">Office 365: configuration de la clé client pour Exchange Online et Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-361">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="9ec2e-362"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-362"></span></span>

<span data-ttu-id="9ec2e-p150">Avant de commencer, vérifiez que vous avez terminé les tâches requises pour configurer Azure Key Vault. Pour plus d'informations, consultez la rubrique [tâches terminées dans Azure Key Vault et Microsoft FastTrack pour la clé client](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="9ec2e-365">Pour configurer la clé client pour Exchange Online et Skype entreprise, vous devez effectuer ces étapes en vous connectant à distance à Exchange Online à l'aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-365">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="9ec2e-366">Créer une stratégie de chiffrement de données (DEP) à utiliser avec Exchange Online et Skype entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-366">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="9ec2e-367"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-367"></span></span>

<span data-ttu-id="9ec2e-p151">Une DEP est associée à un ensemble de clés stockées dans Azure Key Vault. Vous affectez une DEP à une boîte aux lettres dans Office 365. Office 365 utilisera ensuite les clés identifiées dans la stratégie pour chiffrer la boîte aux lettres. Pour créer la DEP, vous avez besoin des URI de coffre-fort que vous avez obtenus précédemment. Consultez [la rubrique obtenir l'URI pour chaque clé Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="9ec2e-p152">Pensez! Lorsque vous créez une DEP, vous spécifiez deux clés qui résident dans deux coffres de clés Azure différents. Assurez-vous que ces clés se situent dans deux régions Azure distinctes pour garantir la redondance géographique.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="9ec2e-376">Pour créer la DEP, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-376">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="9ec2e-377">Sur votre ordinateur local, à l'aide d'un compte professionnel ou scolaire disposant d'autorisations d'administrateur général dans votre organisation Office 365, [Connectez-vous à Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) en ouvrant Windows PowerShell et en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-377">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="9ec2e-378">Dans la boîte de dialogue demande d'informations d'identification Windows PowerShell, entrez vos informations de compte professionnel ou scolaire, cliquez sur **OK**, puis entrez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-378">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="9ec2e-379">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-379">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="9ec2e-380">Pour créer une DEP, utilisez la cmdlet New-DataEncryptionPolicy en tapant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-380">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="9ec2e-381">Où :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-381">Where:</span></span>
    
   -  <span data-ttu-id="9ec2e-p153">*PolicyName* est le nom que vous souhaitez utiliser pour la stratégie. Les noms ne peuvent pas contenir d'espaces. Par exemple, USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="9ec2e-p154">*PolicyDescription* est une description conviviale de la stratégie qui vous permettra de vous souvenir de ce à quoi la stratégie est destinée. Vous pouvez inclure des espaces dans la description. Par exemple, la clé racine des boîtes aux lettres des États-Unis et de ses territoires.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="9ec2e-p155">*KeyVaultURI1* est l'URI de la première clé de la stratégie. Par exemple, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="9ec2e-p156">*KeyVaultURI2* est l'URI de la deuxième clé de la stratégie. Par exemple, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Séparez les deux URI par une virgule et un espace.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="9ec2e-393">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-393">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="9ec2e-394">Affecter une DEP à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="9ec2e-394">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="9ec2e-395"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-395"></span></span>

<span data-ttu-id="9ec2e-p157">Affecter la DEP à une boîte aux lettres à l'aide de la cmdlet Set-Mailbox. Une fois que vous avez affecté la stratégie, Office 365 peut chiffrer la boîte aux lettres à l'aide de la clé désignée dans la DEP.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="9ec2e-p158">Où *MailboxIdParameter* spécifie une boîte aux lettres. Pour plus d'informations sur la cmdlet Set-Mailbox, consultez la rubrique [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="9ec2e-400">Valider le chiffrement de boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="9ec2e-400">Validate mailbox encryption</span></span>
<span data-ttu-id="9ec2e-401"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-401"></span></span>

<span data-ttu-id="9ec2e-p159">Le chiffrement d'une boîte aux lettres peut prendre du temps. Pour une attribution de stratégie de première exécution, la boîte aux lettres doit également effectuer le déplacement d'une base de données à une autre pour que le service puisse chiffrer la boîte aux lettres. Nous vous recommandons d'attendre 72 heures avant de valider le chiffrement après avoir modifié une DEP ou la première fois que vous affectez une DEP à une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="9ec2e-405">Utilisez la cmdlet Get-MailboxStatistics pour déterminer si une boîte aux lettres est chiffrée.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-405">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="9ec2e-406">La propriété IsEncrypted renvoie la valeur **true** si la boîte aux lettres est chiffrée et la valeur **false** si la boîte aux lettres n'est pas chiffrée.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-406">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="9ec2e-p160">Le temps nécessaire au déplacement des boîtes aux lettres dépend du nombre de boîtes aux lettres auxquelles vous affectez une DEP pour la première fois, ainsi que de la taille des boîtes aux lettres. Si les boîtes aux lettres n'ont pas été chiffrées après une semaine à partir du moment où vous avez attribué la DEP, lancez un déplacement de boîte aux lettres pour les boîtes aux lettres non chiffrées à l'aide de la cmdlet New-MoveRequest.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="9ec2e-409">Office 365: configuration de la clé client pour SharePoint Online et OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-409">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="9ec2e-410"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-410"></span></span>

<span data-ttu-id="9ec2e-p161">Avant de commencer, vérifiez que vous avez terminé les tâches requises pour configurer Azure Key Vault. Pour plus d'informations, consultez la rubrique [tâches terminées dans Azure Key Vault et Microsoft FastTrack pour la clé client](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="9ec2e-413">Pour configurer la clé client pour SharePoint Online et OneDrive entreprise, vous devez effectuer ces étapes en vous connectant à distance à SharePoint Online avec Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-413">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="9ec2e-414">Créer une stratégie de chiffrement de données (DEP) pour chaque région de SharePoint Online et OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-414">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="9ec2e-415"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-415"></span></span>

<span data-ttu-id="9ec2e-p162">Une DEP est associée à un ensemble de clés stockées dans Azure Key Vault. Vous appliquez une DEP à toutes vos données dans un emplacement géographique, également appelé géo. Si vous utilisez la fonctionnalité multigéographique d'Office 365 (actuellement en version d'évaluation), vous pouvez créer une DEP par zone géographique. Si vous n'utilisez pas de multi-géo, vous pouvez créer une DEP dans Office 365 pour une utilisation avec SharePoint Online et OneDrive entreprise. Office 365 utilisera ensuite les clés identifiées dans la DEP pour chiffrer vos données dans cette région. Pour créer la DEP, vous avez besoin des URI de coffre-fort que vous avez obtenus précédemment. Consultez [la rubrique obtenir l'URI pour chaque clé Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="9ec2e-p163">Pensez! Lorsque vous créez une DEP, vous spécifiez deux clés qui résident dans deux coffres de clés Azure différents. Assurez-vous que ces clés se situent dans deux régions Azure distinctes pour garantir la redondance géographique.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="9ec2e-426">Pour créer une DEP, vous devez vous connecter à distance à SharePoint Online à l'aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-426">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="9ec2e-427">Sur votre ordinateur local, à l'aide d'un compte professionnel ou scolaire disposant d'autorisations d'administrateur général dans votre organisation Office 365, [Connectez-vous à SharePoint Online PowerShell](https://technet.microsoft.com/library/fp161372.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-427">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="9ec2e-428">Dans Microsoft SharePoint Online Management Shell, exécutez la cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-428">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="9ec2e-p164">Lorsque vous enregistrez la DEP, le chiffrement commence sur les données de la région géographique. Cela peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="9ec2e-431">Valider le chiffrement des sites de groupe, des sites d'équipe et de OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="9ec2e-431">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="9ec2e-432"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-432"></span></span>

<span data-ttu-id="9ec2e-433">Vous pouvez vérifier l'état du chiffrement en exécutant la cmdlet Get-SPODataEncryptionPolicy comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-433">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="9ec2e-434">La sortie de cette cmdlet comprend les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-434">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="9ec2e-435">URI de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-435">The URI of the primary key.</span></span>
    
- <span data-ttu-id="9ec2e-436">URI de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-436">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="9ec2e-p165">État de chiffrement de la zone géographique. Les États possibles sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="9ec2e-439">Non **enregistré:** Le chiffrement de clé client n'a pas encore été appliqué.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-439">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="9ec2e-p166">**Inscription:** Le chiffrement de clés client a été appliqué et vos fichiers sont en cours de chiffrement. Si votre région est dans cet État, vous verrez également des informations sur le pourcentage de sites dans la zone géographique, afin que vous puissiez surveiller la progression du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="9ec2e-442">**Inscrit:** Le chiffrement de clés client a été appliqué et tous les fichiers de tous les sites ont été chiffrés.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-442">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="9ec2e-p167">**Roulement:** Un roulement de clé est en cours. Si votre région est dans cet État, vous verrez également des informations sur le pourcentage de sites ayant terminé l'opération de déploiement de clés afin que vous puissiez surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="9ec2e-445">Gestion de la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="9ec2e-445">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="9ec2e-446"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-446"></span></span>

<span data-ttu-id="9ec2e-447">Une fois que vous avez configuré la clé client pour Office 365, vous pouvez effectuer ces tâches de gestion supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-447">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="9ec2e-448">Restaurer les clés Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="9ec2e-448">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="9ec2e-449">Laminage ou rotation d'une clé dans le coffre-fort de clés Azure que vous utilisez avec la clé client</span><span class="sxs-lookup"><span data-stu-id="9ec2e-449">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="9ec2e-450">Gérer les autorisations de coffre-fort</span><span class="sxs-lookup"><span data-stu-id="9ec2e-450">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="9ec2e-451">Déterminer la DEP affectée à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="9ec2e-451">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="9ec2e-452">Restaurer les clés Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="9ec2e-452">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="9ec2e-453"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-453"></span></span>

<span data-ttu-id="9ec2e-p168">Avant d'effectuer une restauration, utilisez les fonctionnalités de récupération fournies par la fonction de suppression récupérable. Toutes les clés utilisées avec la clé client doivent être activées pour la suppression logicielle. La suppression douce se comporte comme une corbeille et permet la récupération jusqu'à 90 jours sans nécessiter de restauration. La restauration doit être uniquement requise dans des circonstances extrêmes ou inhabituelles, par exemple en cas de perte de la clé ou du coffre-fort. Si vous devez restaurer une clé à utiliser avec la clé client, dans Azure PowerShell, exécutez la cmdlet reStore-AzureKeyVaultKey comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="9ec2e-459">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-459">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="9ec2e-p169">S'il existe déjà une clé portant le même nom dans le coffre-fort de clés, l'opération de restauration échoue. ReStore-AzureKeyVaultKey restaure toutes les versions clés et toutes les métadonnées pour la clé, y compris le nom de la clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="9ec2e-462">Laminage ou rotation d'une clé dans le coffre-fort de clés Azure que vous utilisez avec la clé client</span><span class="sxs-lookup"><span data-stu-id="9ec2e-462">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="9ec2e-463"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-463"></span></span>

<span data-ttu-id="9ec2e-p170">Les touches de roulement ne sont pas requises par le coffre-fort des clés Azure ou par la clé client. En outre, les clés protégées par un HSM sont quasiment impossibles à compromettre. Même si une clé racine était en possession d'un acteur malveillant, il n'est pas possible de l'utiliser pour déchiffrer les données, étant donné que seul le code Office 365 sait comment l'utiliser. Toutefois, le lancement d'une clé est pris en charge par la clé client.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="9ec2e-p171">N'annulez une clé de chiffrement que vous utilisez avec la clé du client lorsqu'il existe une raison technique claire ou qu'une exigence de conformité exige que vous deviez annuler la clé. En outre, ne supprimez pas de clés qui sont ou n'ont pas été associées à des stratégies. Lorsque vous restaurez vos clés, le contenu est chiffré avec les clés précédentes. Par exemple, bien que les boîtes aux lettres actives soient rechiffrées fréquemment, les boîtes aux lettres inactives, déconnectées et désactivées peuvent toujours être chiffrées avec les clés précédentes. SharePoint Online effectue des sauvegardes de contenu à des fins de restauration et de récupération, de sorte qu'il peut toujours y avoir un archivage de contenu à l'aide de clés plus anciennes.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="9ec2e-p172">Pour garantir la sécurité de vos données, SharePoint Online ne permet pas qu'une seule opération de roulier de clés soit en cours à la fois. Si vous souhaitez exécuter les deux clés dans un coffre-fort de clés, vous devez attendre que la première opération de la première clé soit entièrement terminée. Nous vous recommandons d'échelonner vos opérations de roulement de clé à différents intervalles, de sorte qu'il ne s'agit pas d'un problème.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="9ec2e-p173">Lorsque vous annulez une touche, vous demandez une nouvelle version d'une clé existante. Pour demander une nouvelle version d'une clé existante, vous utilisez la même cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), avec la même syntaxe que celle que vous avez utilisée pour créer la clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="9ec2e-478">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-478">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="9ec2e-p174">Dans cet exemple, étant donné qu'une clé nommée **contoso-O365EX-na-VaultA1-Key001** existe déjà dans la chambre forte de **contoso-O365EX-na-VaultA1** , une nouvelle version de clé sera créée. L'opération ajoute une nouvelle version de clé. Cette opération conserve les versions de clés précédentes dans l'historique des versions de la clé, afin que les données précédemment chiffrées avec cette clé puissent toujours être déchiffrées. Une fois que vous avez terminé le lancement de n'importe quelle clé associée à une DEP, vous devez exécuter une applet de commande supplémentaire pour vous assurer que la clé client commence à utiliser la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="9ec2e-483">Activer Exchange Online et Skype entreprise pour utiliser une nouvelle clé après avoir fait rouler ou pivoter des clés dans le coffre-fort des clés Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-483">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="9ec2e-484">Lorsque vous effectuez l'une ou l'autre des clés Azure Key Vault associées à une DEP utilisée avec Exchange Online et Skype entreprise, vous devez exécuter la commande suivante pour mettre à jour la DEP et activer Office 365 pour qu'il démarre à l'aide de la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-484">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="9ec2e-485">Pour indiquer à la clé du client d'utiliser la nouvelle clé pour chiffrer les boîtes aux lettres dans Office 365 exécutez la cmdlet Set-DataEncryptionPolicy comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-485">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="9ec2e-p175">Dans les 48 heures, les boîtes aux lettres actives chiffrées à l'aide de cette stratégie sont associées à la clé mise à jour. Suivez les étapes décrites dans la procédure [déterminer la DEP attribuée à une boîte aux lettres](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) pour vérifier la valeur de la propriété DataEncryptionPolicyID de la boîte aux lettres. La valeur de cette propriété change une fois que la clé mise à jour a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="9ec2e-489">Activer SharePoint Online et OneDrive entreprise pour utiliser une nouvelle clé après avoir fait rouler ou pivoter des clés dans le coffre-fort des clés Azure</span><span class="sxs-lookup"><span data-stu-id="9ec2e-489">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="9ec2e-490">Lorsque vous effectuez l'une des clés Azure Key Vault associées à une DEP utilisée avec SharePoint Online et OneDrive entreprise, vous devez exécuter la cmdlet [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) pour mettre à jour la DEP et activer Office 365 pour qu'il commence à utiliser la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-490">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="9ec2e-p176">Cela démarrera l'opération de déploiement de clés pour SharePoint Online et OneDrive entreprise. Cette action n'est pas immédiate. Pour voir la progression de l'opération de la séquence de touches, exécutez la cmdlet Get-SPODataEncryptionPolicy comme suit:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="9ec2e-494">Gérer les autorisations de coffre-fort</span><span class="sxs-lookup"><span data-stu-id="9ec2e-494">Manage key vault permissions</span></span>
<span data-ttu-id="9ec2e-495"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-495"></span></span>

<span data-ttu-id="9ec2e-p177">Plusieurs cmdlets sont disponibles, qui vous permettent d'afficher et, si nécessaire, de supprimer des autorisations de coffre-fort clé. Vous devrez peut-être supprimer des autorisations, par exemple, lorsqu'un employé quitte l'équipe.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="9ec2e-498">Pour afficher les autorisations de coffre-fort, exécutez la cmdlet Get-AzureRmKeyVault:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-498">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="9ec2e-499">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-499">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="9ec2e-500">Pour supprimer les autorisations d'un administrateur, exécutez l'applet de commande Remove-AzureRmKeyVaultAccessPolicy:</span><span class="sxs-lookup"><span data-stu-id="9ec2e-500">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="9ec2e-501">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="9ec2e-501">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="9ec2e-502">Déterminer la DEP affectée à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="9ec2e-502">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="9ec2e-503"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="9ec2e-503"></span></span>

<span data-ttu-id="9ec2e-p178">Pour déterminer la DEP affectée à une boîte aux lettres, utilisez la cmdlet Get-MailboxStatistics. L'applet de commande renvoie un identificateur unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="9ec2e-p179">Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres. Pour plus d'informations sur la cmdlet Get-MailboxStatistics, consultez la rubrique [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ec2e-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="9ec2e-508">Utilisez le GUID pour connaître le nom convivial de la DEP à laquelle la boîte aux lettres est affectée en exécutant l'applet de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-508">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="9ec2e-509">Où *GUID* est le GUID renvoyé par la cmdlet Get-MailboxStatistics à l'étape précédente.</span><span class="sxs-lookup"><span data-stu-id="9ec2e-509">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  

