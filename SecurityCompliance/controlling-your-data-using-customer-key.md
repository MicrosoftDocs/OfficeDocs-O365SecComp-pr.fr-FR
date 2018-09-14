---
title: Contrôler vos données dans Office 365 à l'aide de la clé client
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: Découvrez comment configurer la clé client pour Office 365 pour Exchange Online, Skype pour les entreprises, SharePoint Online et OneDrive for Business. Avec la clé client, vous contrôler les clés de chiffrement de votre organisation, puis configurez Office 365 pour les utiliser pour chiffrer vos données au repos dans les centres de données de Microsoft.
ms.openlocfilehash: 3eeccd03b89aa5a79ceba536d3f13c7a881b6ca7
ms.sourcegitcommit: ef0bb05a0cf7974ae5083c7551ce3fe4ab7a9544
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "23965608"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="aa8b9-104">Contrôler vos données dans Office 365 à l'aide de la clé client</span><span class="sxs-lookup"><span data-stu-id="aa8b9-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="aa8b9-p102">Avec la clé client, vous contrôler les clés de chiffrement de votre organisation, puis configurez Office 365 pour les utiliser pour chiffrer vos données au repos dans les centres de données de Microsoft. Données au repos comprennent des données à partir d’Exchange Online et Skype pour les entreprises qui est stocké dans les boîtes aux lettres et les fichiers qui sont stockés dans SharePoint Online et OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="aa8b9-p103">Vous devez configurer Azure avant de pouvoir utiliser la clé client pour Office 365. Cette rubrique décrit les étapes à suivre pour créer et configurer les ressources requises Azure et puis fournit les étapes de configuration de la clé client dans Office 365. Après avoir terminé le programme d’installation Azure, vous déterminez la stratégie et par conséquent, les clés, à affecter aux boîtes aux lettres et des fichiers dans votre organisation. Boîtes aux lettres et fichiers pour lesquels vous n’affecter une stratégie utiliseront les stratégies de chiffrement qui sont contrôlés et gérés par Microsoft. Pour plus d’informations sur la clé client, ou pour une vue d’ensemble, voir la [Clé client pour Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="aa8b9-p104">Il est vivement recommandé de suivre les meilleures pratiques dans cette rubrique. Il s’agit **Conseil** et **IMPORTANT**. Client clé vous permet de contrôler les clés de chiffrement racine dont la portée peut être aussi grand que la totalité de votre organisation. Cela signifie que commises avec ces touches peuvent avoir un impact large et risque de provoquer des interruptions de service ou la perte irrévocable de vos données.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="aa8b9-116">Avant de commencer la configuration de la clé client</span><span class="sxs-lookup"><span data-stu-id="aa8b9-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="aa8b9-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-117"></span></span>

<span data-ttu-id="aa8b9-p105">Avant de commencer, assurez-vous que la gestion des licences approprié pour votre organisation. Clé de client dans Office 365 est proposée dans Office 365 E5 ou la référence de conformité avancées.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="aa8b9-p106">Ensuite, pour comprendre les concepts et les procédures décrites dans cette rubrique, vous devez examiner la documentation [Azure clé coffre-fort](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . En outre, vous familiariser avec les termes utilisés dans Azure, par exemple, le [client](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="aa8b9-122">Pour fournir des commentaires sur la clé client, y compris la documentation, envoyez vos idées et suggestions perspectives à customerkeyfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="aa8b9-123">Vue d’ensemble de la configuration de la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="aa8b9-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="aa8b9-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-124"></span></span>

<span data-ttu-id="aa8b9-p107">Pour configurer la clé client, vous allez effectuer ces tâches. Le reste de cette rubrique fournit des instructions détaillées pour chaque tâche, ou à des liens vers des plus d’informations pour chaque étape du processus.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="aa8b9-127">**Dans Azure et FastTrack Microsoft :**</span><span class="sxs-lookup"><span data-stu-id="aa8b9-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="aa8b9-p108">Vous allez exécuter la plupart de ces tâches en vous connectant à distance PowerShell Azure. Pour obtenir les meilleurs résultats, utilisez version 4.4.0 ou ultérieure de Windows Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="aa8b9-130">Créer deux nouveaux abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="aa8b9-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="aa8b9-131">Enregistrer des abonnements Azure pour utiliser une période de rétention obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa8b9-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="aa8b9-132">L’inscription peut prendre entre un et cinq jours ouvrés.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="aa8b9-133">Pour soumettre une demande pour activer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="aa8b9-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="aa8b9-p109">Une fois que vous avez créé les deux nouveaux abonnements Azure, vous devez envoyer la demande d’offre de clé de client appropriée en effectuant un formulaire web qui est hébergé dans le portail Microsoft FastTrack. L’équipe FastTrack ne fournit pas d’assistance avec la clé client. Office utilise simplement le portail FastTrack pour vous permettre d’envoyer le formulaire et pour suivre les offres pertinentes pour la clé client.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key.</span></span>
  
<span data-ttu-id="aa8b9-p110">Une fois que vous avez soumis une offre de la clé client, Microsoft passe en revue votre demande et vous avertit que vous pouvez passer avec les autres tâches de configuration. Ce processus peut prendre jusqu'à cinq jours ouvrés.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="aa8b9-139">Créer un coffre-fort de clé Azure premium dans chaque abonnement</span><span class="sxs-lookup"><span data-stu-id="aa8b9-139">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="aa8b9-140">Attribuer des autorisations à chaque clé coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-140">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="aa8b9-141">Activer et Confirmer suppression réversible sur votre chambres fortes clés</span><span class="sxs-lookup"><span data-stu-id="aa8b9-141">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="aa8b9-142">Ajoutez une clé pour chaque clé coffre-fort soit par la création ou l’importation d’une clé</span><span class="sxs-lookup"><span data-stu-id="aa8b9-142">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="aa8b9-143">Vérifier le niveau de restauration de vos clés</span><span class="sxs-lookup"><span data-stu-id="aa8b9-143">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="aa8b9-144">Sauvegarde coffre-fort clé Azure</span><span class="sxs-lookup"><span data-stu-id="aa8b9-144">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="aa8b9-145">Valider les paramètres de configuration Azure clé coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-145">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="aa8b9-146">Obtenir l’URI pour chaque clé Azure clé coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-146">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="aa8b9-147">**Dans Office 365 :**</span><span class="sxs-lookup"><span data-stu-id="aa8b9-147">**In Office 365:**</span></span>
  
<span data-ttu-id="aa8b9-148">Exchange Online et Skype pour les entreprises :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-148">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="aa8b9-149">Créer une stratégie de chiffrement des données (PED) pour une utilisation avec Exchange Online et Skype pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="aa8b9-149">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="aa8b9-150">Affecter un PED à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="aa8b9-150">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="aa8b9-151">Valider le chiffrement de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="aa8b9-151">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="aa8b9-152">SharePoint Online et OneDrive entreprise :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-152">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="aa8b9-153">Créer une stratégie de chiffrement des données (PED) pour chaque OneDrive et SharePoint Online pour entreprise geo</span><span class="sxs-lookup"><span data-stu-id="aa8b9-153">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="aa8b9-154">Valider le chiffrement du groupe de Sites, Sites d’équipe et OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="aa8b9-154">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="aa8b9-155">Effectuer des tâches dans Azure clé coffre-fort et FastTrack Microsoft pour la clé client</span><span class="sxs-lookup"><span data-stu-id="aa8b9-155">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="aa8b9-156"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-156"></span></span>

<span data-ttu-id="aa8b9-p111">Effectuer ces tâches dans Azure clé coffre-fort afin de configurer la clé client pour Office 365. Vous devez effectuer ces étapes que vous envisagez de configurer la clé client pour Exchange Online et Skype pour Business ou SharePoint Online et OneDrive for Business ou pour tous les services pris en charge dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="aa8b9-159">Créer deux nouveaux abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="aa8b9-159">Create two new Azure subscriptions</span></span>
<span data-ttu-id="aa8b9-160"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-160"></span></span>

<span data-ttu-id="aa8b9-p112">Deux abonnements Azure sont requis pour la clé client. Meilleure pratique, Microsoft recommande que vous créez des nouveaux abonnements Azure pour une utilisation avec la clé client. Clés de clé coffre-fort Azure ne peuvent être autorisées pour les applications dans le même client Azure Active Directory (DAS), vous devez créer les nouveaux abonnements à l’aide du même client Azure AD utilisé avec votre organisation Office 365 dans lequel le Dép. sera attribué. Par exemple, à l’aide de votre compte professionnel ou de l’école ayant des privilèges d’administrateur global dans votre organisation Office 365. Pour obtenir la procédure détaillée, voir [s’inscrire pour Azure comme une organisation](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="aa8b9-p113">Clé de client nécessite deux clés pour chaque stratégie de chiffrement des données (PED). Pour ce faire, vous devez créer deux abonnements Azure. Microsoft recommande d’ont distinct des membres de votre organisation pour configurer une clé dans chaque abonnement. En outre, ces abonnements Azure doivent uniquement être utilisés pour administrer les clés de chiffrement pour Office 365. Il protège votre organisation en cas d’un de vos opérateurs intentionnellement accidentelle ou intentionnelle supprime ou dans le cas contraire mismanages les clés pour lesquels ils sont chargés.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="aa8b9-p114">Nous vous recommandons de configurer les nouveaux abonnements Azure qui sont uniquement utilisés pour la gestion des ressources Azure clé coffre-fort pour une utilisation avec la clé client. Il n’existe aucune limite au nombre d’abonnements Azure que vous pouvez créer pour votre organisation. Suivant ces meilleures pratiques réduit l’impact d’une erreur humaine tout en aidant à gérer les ressources utilisées par la clé client.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="aa8b9-174">Pour soumettre une demande pour activer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="aa8b9-174">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="aa8b9-175"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-175"></span></span>

<span data-ttu-id="aa8b9-p115">Une fois que vous avez terminé les étapes Azure, vous devez soumettre une demande offre dans le [portail Microsoft FastTrack](https://fasttrack.microsoft.com/). Une fois que vous avez soumis une demande via le portail web FastTrack, Microsoft vérifie les informations de contact et les données de configuration Azure clé coffre-fort que vous avez fournis. Les sélections effectuées dans l’écran offre concernant les agents autorisés de votre organisation est nécessaire pour la fin de l’enregistrement de clé de client et critique. Les agents de votre organisation que vous sélectionnez dans le formulaire sera utilisé pour assurer l’authenticité de toute demande de révoquer et détruire toutes les clés utilisées avec une règle de chiffrement des données de clé de client. Vous devez effectuer cette étape une fois pour activer la clé client pour Exchange Online et Skype pour la couverture d’entreprise et une deuxième fois activer la clé client pour SharePoint Online et OneDrive for Business.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="aa8b9-181">Pour soumettre une offre pour activer la clé client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-181">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="aa8b9-182">À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, connectez-vous au [portail Microsoft FastTrack](https://fasttrack.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-182">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="aa8b9-183">Une fois que vous êtes connecté dans, accédez au **tableau de bord**.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-183">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="aa8b9-184">Choisissez **offre**, puis passez en revue la liste des offres en cours.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-184">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="aa8b9-185">Choisissez **En savoir plus** pour l’offre s’applique à vous :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-185">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="aa8b9-186">**Exchange Online et Skype pour les entreprises :** Choisissez **En savoir plus** sur l’offre de **Clé de client pour Exchange** .</span><span class="sxs-lookup"><span data-stu-id="aa8b9-186">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="aa8b9-187">**SharePoint Online et OneDrive for Business :** Choisissez **En savoir plus** sur la **Clé de client pour SharePoint et OneDrive entreprise** offre.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-187">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="aa8b9-188">Dans la page **Détails de l’offre** , choisissez **Créer une demande**.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-188">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="aa8b9-p116">Remplissez tous les détails applicables et les informations demandées dans le formulaire offre. Une attention particulière à vos sélections pour les responsables de votre organisation que vous voulez autoriser à approuver la destruction définitive et irréversible de clés de chiffrement et de données. Une fois que vous avez terminé le formulaire, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="aa8b9-192">Ce processus peut prendre jusqu'à cinq jours ouvrés une fois que Microsoft a été averti de votre demande.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-192">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="aa8b9-193">Passez à la section de période de rétention obligatoire ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-193">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="aa8b9-194">Enregistrer des abonnements Azure pour utiliser une période de rétention obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa8b9-194">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="aa8b9-195"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-195"></span></span>

<span data-ttu-id="aa8b9-p117">La perte temporaire ou permanente racine des clés de chiffrement peut être très gênants ou même des catastrophes à l’opération de service et peut entraîner une perte de données. Pour cette raison, les ressources utilisées avec la clé client nécessitent une protection renforcée. Toutes les ressources Azure qui sont utilisés avec la clé client offrent des mécanismes de protection au-delà de la configuration par défaut. Abonnements Azure peuvent être marqués ou enregistrés d’une manière qui empêche l’annulation de l’exécution et irrévocable. Il est appelé inscription pour une période de rétention obligatoire. Les étapes nécessaires à l’enregistrement des abonnements Azure pour une période de rétention obligatoire requièrent la collaboration avec l’équipe Office 365. Ce processus peut prendre entre un et cinq jours ouvrés. Auparavant, il a été parfois appelé « Ne pas annuler ».</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="aa8b9-204">Avant de contacter l’équipe Office 365, vous devez effectuer les étapes suivantes pour chaque abonnement Azure que vous utilisez avec la clé client :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-204">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="aa8b9-p118">Connectez-vous à votre abonnement Azure avec Azure PowerShell. Pour plus d’informations, voir [Connectez-vous avec Windows Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="aa8b9-207">Exécutez l’applet de commande Register-AzureRmProviderFeature pour enregistrer vos abonnements pour utiliser une période de rétention obligatoire.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-207">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="aa8b9-p119">Contacter Microsoft pour que le processus de finalisation. Pour SharePoint et OneDrive équipe commerciale, contactez [spock@microsoft.com](mailto:spock@microsoft.com). Pour Exchange Online et Skype pour les entreprises, contactez [exock@microsoft.com](mailto:exock@microsoft.com). Le contrat de niveau de Service (SLA) pour la fin de ce processus est cinq jours ouvrés une fois que Microsoft a été averti (et vérifié) que vous avez enregistré vos abonnements pour utiliser une période de rétention obligatoire. Inclure les éléments suivants dans votre courrier électronique :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="aa8b9-213">**Objet**: clé de client pour \< *au nom de domaine complet de votre client*\></span><span class="sxs-lookup"><span data-stu-id="aa8b9-213">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="aa8b9-214">**Corps**: ID d’abonnement pour laquelle vous voulez permettre la rétention obligatoire période finalisée.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-214">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="aa8b9-215">Une fois que vous recevez une notification à partir de Microsoft que l’inscription est terminée, vérifiez l’état de l’enregistrement en exécutant l’applet de commande Get-AzureRmProviderFeature comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-215">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="aa8b9-216">Après avoir vérifié que la propriété **State de l’inscription** de l’applet de commande Get-AzureRmProviderFeature renvoie la valeur **Registered**, exécutez la commande suivante pour terminer le processus :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-216">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="aa8b9-217">Créer un coffre-fort de clé Azure premium dans chaque abonnement</span><span class="sxs-lookup"><span data-stu-id="aa8b9-217">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="aa8b9-218"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-218"></span></span>

<span data-ttu-id="aa8b9-219">Les étapes pour créer un coffre-fort clé sont documentées dans la [Mise en route avec Azure clé coffre-fort](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), qui vous guide à travers l’installation et lancement d’Azure PowerShell, connexion à votre abonnement Azure, création d’un groupe de ressources et création d’un coffre-fort clé qui groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-219">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="aa8b9-p120">Lorsque vous créez un coffre-fort clé, vous devez choisir une référence SKU : Standard ou Premium. La référence Standard permet clés Azure clé coffre-fort d’être protégé avec le logiciel - il n’existe aucune protection clés du Module de sécurité matériel (HSM) - et la version Premium permet d’utiliser HSM pour la protection des clés de la clé coffre-fort. Clé de client accepte chambres fortes clés qui utilisent soit SKU, bien que Microsoft recommande vivement que vous utilisez uniquement la version Premium. Le coût des opérations avec des clés de des types est la même, la seule différence de coût est le coût par mois pour chaque clé HSM protégé. Pour plus d’informations, voir [clé coffre-fort prix](https://azure.microsoft.com/pricing/details/key-vault/) .</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="aa8b9-225">Utilisez les clés protégés par HSM chambres fortes clés SKU Premium pour les données de production et uniquement chambres fortes clés SKU Standard et les clés à des fins de test et de validation.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-225">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="aa8b9-p121">Pour chaque service Office 365 avec lequel vous allez utiliser la clé client, créez un coffre-fort clé dans chaque abonnement Azure deux que vous avez créé. Par exemple, pour Exchange Online et Skype pour les professionnels uniquement ou SharePoint Online et OneDrive entreprise uniquement, vous allez créer uniquement une paire de chambres fortes. Pour activer la clé client pour Exchange Online et SharePoint Online, vous allez créer deux paires de clés chambres fortes.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="aa8b9-p122">Utilisez une convention d’affectation de noms pour chambres fortes clés qui reflète l’utilisation prévue de la prévention avec lequel vous allez associer les chambres fortes. Voir la section méthodes conseillées ci-dessous pour les recommandations de la convention d’affectation de noms.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="aa8b9-p123">Créer un ensemble distinct et paire de chambres fortes pour chaque stratégie de chiffrement des données. Pour Exchange Online, l’étendue d’une stratégie de chiffrement des données est choisi par vous lorsque vous attribuez la stratégie de boîte aux lettres. Une boîte aux lettres peut avoir qu’une seule stratégie attribuée, et vous pouvez créer des stratégies à cinquante. Pour SharePoint Online l’étendue d’une stratégie est toutes les données au sein d’une organisation dans un emplacement géographique ou localisés.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="aa8b9-p124">La création d’une clé chambres fortes requiert également la création de groupes de ressources Azure, puisqu’il chambres fortes clés besoin de capacité de stockage (bien que très petite) coffre-fort clé journalisation, si activé, génère des données stockées. En règle générale Microsoft recommande l’utilisation de distincts pour les administrateurs à gérer chaque groupe de ressources, avec l’administration alignée sur l’ensemble des administrateurs de gérer toutes les ressources associées de clé de client.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="aa8b9-p125">Pour optimiser la disponibilité, votre chambres fortes clés doivent être dans les zones près votre service Office 365. Par exemple, si votre organisation Exchange Online est en Amérique du Nord, placez votre chambres fortes clés en Amérique du Nord. Si votre organisation Exchange Online est Europe, placez votre chambres fortes clés en Europe.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="aa8b9-p126">Utiliser un préfixe commun pour chambres fortes clés et inclure une abréviation de l’utilisation et l’étendue de la clé coffre-fort et les clés (par exemple, pour le service de Contoso SharePoint où se trouvera le chambres fortes en Amérique du Nord, une paire de noms possible est Contoso-O365SP-NA-VaultA1 et Contoso-O365SP-NA-VaultA2. Noms de coffre-fort sont des chaînes global uniques dans Azure, vous serez peut-être amené à essayer les variantes de vos noms de votre choix au cas où les noms de votre choix sont déjà réclamés par d’autres clients Azure. À compter de juillet 2017 noms coffre-fort ne peut pas être modifiés pour une meilleure pratique consiste à disposer d’un plan écrit pour le programme d’installation et d’utiliser une deuxième personne pour vérifier que le plan est exécuté correctement.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="aa8b9-p127">Si possible, créez votre chambres fortes dans les zones non couplé. Paire de régions Azure fournissent une haute disponibilité sur plusieurs domaines d’échec de service. Par conséquent, paires régionaux peuvent être considérés comme l’autre région sauvegarde. Cela signifie qu’une ressource Azure qui est placée dans une région gagne automatiquement la tolérance de panne par le biais de la région associée. Pour cette raison, choix des régions pour deux chambres fortes utilisés dans un PED où les zones sont couplés signifie qu’uniquement un total de deux régions de disponibilité sont en cours d’utilisation. La plupart des régions ont seulement deux régions, afin qu’il n’est pas encore possible de sélectionner des régions non couplé. Dans la mesure du possible, choisissez deux régions non couplé pour les deux chambres fortes utilisés avec une prévention Il bénéficie d’un total de quatre zones de disponibilité. Pour plus d’informations, voir [Business continuité d’activité et récupération d’urgence (BCDR) : Azure couplé régions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) pour une liste de paires régionaux en cours.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="aa8b9-252">Attribuer des autorisations à chaque clé coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-252">Assign permissions to each key vault</span></span>
<span data-ttu-id="aa8b9-253"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-253"></span></span>

<span data-ttu-id="aa8b9-p128">Pour chaque clé coffre-fort, vous devez définir trois ensembles distincts d’autorisations pour la clé client, en fonction de votre implémentation. Par exemple, vous devez définir un ensemble d’autorisations pour les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="aa8b9-p129">**Les administrateurs de coffre-fort clé** qui exécutera la gestion quotidienne de votre coffre-fort clé pour votre organisation. Ces tâches incluent la sauvegarde, créer, obtient, importer, répertorier et restaurer.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="aa8b9-p130">Le jeu d’autorisations affecté aux administrateurs de coffre-fort clés n’inclut pas l’autorisation de supprimer des clés. Il s’agit intentionnelle et essentiel. Suppression des clés de chiffrement est généralement pas effectuée, dans la mesure où effectuant donc définitivement détruit les données. Meilleure pratique, n’accordez pas cette autorisation aux administrateurs de coffre-fort clés par défaut. Au lieu de cela, cette réserve pour les collaborateurs clés coffre-fort et uniquement l’attribuer à un administrateur de manière à court terme une fois une bonne compréhension des conséquences est comprise.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="aa8b9-p131">Pour affecter ces autorisations à un utilisateur dans votre organisation Office 365, connectez-vous à votre abonnement Azure avec Azure PowerShell. Pour plus d’informations, voir [Connectez-vous avec Windows Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="aa8b9-265">Exécutez l’applet de commande Set-AzureRmKeyVaultAccessPolicy pour attribuer les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-265">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="aa8b9-266">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-266">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="aa8b9-p132">**Les collaborateurs coffre-fort clé** qui peut modifier les autorisations sur le coffre-fort clé Azure lui-même. Vous devrez modifier ces autorisations, comme les employés quittent ou rejoignent de votre équipe, ou dans le cas très rare que la clé vault administrateurs légitimement doivent autorisé à supprimer ou restaurer une clé. Cet ensemble de clés coffre-fort collaborateurs doit bénéficier du rôle de **collaborateur** sur votre clé coffre-fort. Vous pouvez attribuer ce rôle à l’aide du Gestionnaire de ressources Azure. Pour obtenir la procédure détaillée, voir [Contrôle d’accès Use Role-Based pour gérer l’accès aux ressources de votre abonnement Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). L’administrateur qui crée un abonnement a cet accès implicitement, ainsi que la possibilité d’affecter les autres administrateurs au rôle de collaborateur.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="aa8b9-p133">Si vous envisagez d’utiliser la clé client avec Exchange Online et Skype pour les entreprises, vous devez octroyer une autorisation à Office 365 utilisent la clé coffre-fort part Exchange Online et Skype pour les entreprises. De même, si vous envisagez d’utiliser la clé client avec SharePoint Online et OneDrive entreprise, vous devez ajouter l’autorisation pour Office 365 utiliser la clé coffre-fort part SharePoint Online et OneDrive for Business. Pour accorder l’autorisation à Office 365, exécutez l’applet de commande **Set-AzureRmKeyVaultAccessPolicy** à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="aa8b9-276">Où :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-276">Where:</span></span>
    
  - <span data-ttu-id="aa8b9-277">*vaultname* est le nom de la clé coffre-fort que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-277">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="aa8b9-278">Pour Exchange Online et Skype pour les entreprises, remplacez *appID Office 365* avec`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="aa8b9-278">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="aa8b9-279">Pour SharePoint Online et OneDrive entreprise, remplacez *appID Office 365* avec`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="aa8b9-279">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="aa8b9-280">Exemple : Définition des autorisations pour Exchange Online et Skype pour les entreprises :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-280">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="aa8b9-281">Exemple : Définition des autorisations pour SharePoint Online et OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="aa8b9-281">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="aa8b9-282">Activer et Confirmer suppression réversible sur votre chambres fortes clés</span><span class="sxs-lookup"><span data-stu-id="aa8b9-282">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="aa8b9-283"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-283"></span></span>

<span data-ttu-id="aa8b9-p134">Lorsque vous pouvez récupérer rapidement vos clés, vous sont moins susceptibles de rencontrer une panne de l’étendue de service en raison de clés accidentelle ou intentionnelle supprimées. Vous devez activer cette configuration, appelée suppression logicielle, avant de pouvoir utiliser vos clés avec la clé client. Activation supprimer souple vous permet de récupérer des clés ou des chambres fortes au sein de la suppression de 90 jours sans avoir à les restaurer à partir de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="aa8b9-287">Pour activer l’option Supprimer logicielle sur votre chambres fortes clés, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-287">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="aa8b9-p135">Connectez-vous à votre abonnement Azure avec Windows Powershell. Pour plus d’informations, voir [Connectez-vous avec Windows Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="aa8b9-p136">Exécutez l’applet de commande [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . Dans cet exemple, *vaultname* est le nom de la clé coffre-fort pour lequel vous activez suppression réversible :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="aa8b9-p137">Confirmer la suppression réversible est configurée pour le coffre-fort clé en exécutant l’applet de commande **Get-AzureRmKeyVault** . Si la suppression réversible est correctement configurée pour la clé coffre-fort, le logiciel supprimer activé ? propriété renvoie la valeur **True**:</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="aa8b9-294">Ajoutez une clé pour chaque clé coffre-fort soit par la création ou l’importation d’une clé</span><span class="sxs-lookup"><span data-stu-id="aa8b9-294">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="aa8b9-295"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-295"></span></span>

<span data-ttu-id="aa8b9-p138">Il existe deux façons d’ajouter des clés à un coffre-fort clé Azure ; Vous pouvez créer une clé directement dans la clé de coffre-fort, ou vous pouvez importer une clé. Création d’une clé directement dans la clé de coffre-fort est la méthode moins compliquée, alors que l’importation d’une clé offre un contrôle total sur la façon dont la clé est générée.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="aa8b9-298">Pour créer une clé directement dans votre clé coffre-fort, exécutez l’applet de commande [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-298">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="aa8b9-299">Où :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-299">Where:</span></span>
  
-  <span data-ttu-id="aa8b9-300">*vaultname* est le nom de la clé coffre-fort dans lequel vous souhaitez créer la clé.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-300">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="aa8b9-301">*nom* est le nom que vous souhaitez attribuer à la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-301">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="aa8b9-p139">Nom de clés à l’aide d’une convention d’affectation de noms similaire comme décrit ci-dessus pour chambres fortes clés. Ainsi, dans les outils qui affichent uniquement le nom de clé, la chaîne est libre décrivant.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="aa8b9-304">Si vous envisagez de protéger la clé avec un module HSM, assurez-vous que vous spécifiez **HSM** comme valeur du paramètre _Destination_ , spécifiez dans le cas contraire, les **logiciels**.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-304">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="aa8b9-305">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="aa8b9-305">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="aa8b9-306">Pour importer une clé directement dans votre coffre-fort clé, vous devez avoir un Module de sécurité matériel de nShield Thales.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-306">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="aa8b9-307">Certaines organisations préfèrent cette approche pour établir la provenance de leurs clés et cette méthode offre également les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-307">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="aa8b9-308">L’ensemble d’outils utilisé pour l’importation inclut attestation de Thales que la clé d’Exchange clé (KEK) qui est utilisé pour crypter la clé que vous générez n’est pas exportable et est généré à l’intérieur d’un module HSM authentique qui a été fabriqué par Thales.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-308">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="aa8b9-p140">L’ensemble d’outils inclut attestation de Thales que le monde de la sécurité Azure clé coffre-fort a également été généré sur un véritable HSM fabriqué par Thales. Cette attestation est donc vous que Microsoft utilise également authentique matériel Thales.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="aa8b9-p141">Renseignez-vous auprès de votre groupe de sécurité pour déterminer si les attestations ci-dessus sont nécessaires. Pour connaître les étapes détaillées créer une clé locale et l’importer dans votre coffre-fort clé, voir [comment générer et transférer les clés protégés par HSM pour Azure clé coffre-fort](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Utilisez les instructions Azure pour créer une clé dans chaque clé coffre-fort.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="aa8b9-314">Vérifier le niveau de restauration de vos clés</span><span class="sxs-lookup"><span data-stu-id="aa8b9-314">Check the recovery level of your keys</span></span>
<span data-ttu-id="aa8b9-315"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-315"></span></span>

<span data-ttu-id="aa8b9-p142">Office 365 nécessite que l’abonnement Azure clé coffre-fort est défini sur ne pas annuler et que les touches utilisées par la clé client ont suppression réversible activée. Vous pouvez le vérifier en regardant le niveau de restauration sur vos clés.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="aa8b9-318">Pour vérifier le niveau de restauration d’une clé, dans Windows Azure PowerShell, exécutez l’applet de commande Get-AzureKeyVaultKey comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-318">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="aa8b9-319">Si la propriété de _Niveau de restauration_ renvoie rien d’autre que la valeur **Récupérable + ProtectedSubscription**, vous devrez consulter cette rubrique et vous assurer que vous avez suivi toutes les étapes pour placer la liste ne pas annuler l’abonnement et que vous avez activée sur chacun de vos chambres fortes clés de suppression réversible.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-319">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="aa8b9-320">Sauvegarde coffre-fort clé Azure</span><span class="sxs-lookup"><span data-stu-id="aa8b9-320">Backup Azure Key Vault</span></span>
<span data-ttu-id="aa8b9-321"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-321"></span></span>

<span data-ttu-id="aa8b9-p143">Immédiatement après la création ou toute modification apportée à une clé, effectuez une sauvegarde et de stocker des copies de la sauvegarde, en ligne et hors connexion. Copies hors connexion ne doivent pas connectés à un réseau, tels que dans un emplacement de stockage physique sans échec ou commerciale. Au moins une copie de la sauvegarde doit être stockée dans un emplacement accessible en cas d’incident. Les objets BLOB sauvegarde sont le seul moyen de la restauration de clé une clé clé coffre-fort doit être définitivement supprimée ou sinon rendue inutilisable. Clés qui sont externes à Azure clé coffre-fort et ont été importés à Azure clé coffre-fort ne constituent pas une sauvegarde car les métadonnées nécessaires pour la clé client d’utiliser la clé n’existent pas avec la clé externe. Uniquement une sauvegarde effectuée à partir d’Azure clé coffre-fort utilisable pour les opérations de restauration avec la clé client. Par conséquent, il est essentiel qu’une sauvegarde de Azure clé coffre-fort être effectuée une fois qu’une clé est téléchargée ou créée.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="aa8b9-329">Pour créer une sauvegarde d’une clé Azure clé coffre-fort, exécutez l’applet de commande [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-329">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="aa8b9-330">Assurez-vous que votre fichier de sortie utilise le suffixe `.backup`.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-330">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="aa8b9-p144">Le fichier de sortie résultant de cette applet de commande est chiffré et ne peut pas être utilisé en dehors d’Azure clé coffre-fort. La sauvegarde peut être restaurée uniquement à l’abonnement Azure à partir de laquelle la sauvegarde a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="aa8b9-p145">Le fichier de sortie, choisissez une combinaison de votre nom de coffre-fort et le nom de la clé. Cela permettra le nom de fichier décrivant automatique. Il permet également de garantir que les noms de fichier de sauvegarde n’entrent pas en conflit.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="aa8b9-336">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-336">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="aa8b9-337">Valider les paramètres de configuration Azure clé coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-337">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="aa8b9-338"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-338"></span></span>

<span data-ttu-id="aa8b9-p146">Exécution de la validation avant d’utiliser des clés dans une PED est facultative mais fortement recommandée. En particulier, si vous utilisez des étapes pour configurer vos clés et chambres fortes autres que celles décrites dans cette rubrique, vous devez valider l’intégrité de vos ressources Azure clé coffre-fort avant de configurer la clé client.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="aa8b9-341">Pour vérifier que vos clés ont des opérations get, wrapKey et unwrapKey activées :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-341">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="aa8b9-342">Exécutez l’applet de commande [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-342">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="aa8b9-p147">Dans la sortie, rechercher la stratégie d’accès et l’identité (GUID) Exchange Online ou l’identité SharePoint Online (GUID) comme il convient. Les trois les autorisations doivent être indiqués sous autorisations aux clés.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="aa8b9-345">Si la configuration de stratégie d’accès est incorrecte, exécutez l’applet de commande Set-AzureRmKeyVaultAccessPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-345">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="aa8b9-346">Par exemple, pour Exchange Online et Skype pour les entreprises :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-346">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="aa8b9-347">Par exemple, pour SharePoint Online et OneDrive entreprise :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-347">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="aa8b9-348">Pour vérifier que la date d’expiration n’est pas définie pour les clés, exécutez l’applet de commande [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-348">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="aa8b9-p148">Une clé arrivés à expiration ne peut pas être utilisée par la clé client et tentées avec une clé arrivés à expiration des opérations échoue et éventuellement entraîner une interruption de service. Il est vivement recommandé que les clés utilisées avec la clé client n’ont pas une date d’expiration. Une date d’expiration, une fois que set, ne peut pas être supprimée, mais peut être modifiée à une date différente. Si une clé ayant une date d’expiration de la valeur doit être utilisée, modifiez la valeur d’expiration au 12/31/9999. Touches avec une date d’expiration définie sur une date différente de 12/31/9999 ne passera pas la validation d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="aa8b9-354">Pour modifier une date d’expiration qui a une valeur autre que 12/31/9999, exécutez l’applet de commande [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-354">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="aa8b9-355">Ne définissez pas de clés de chiffrement que vous utilisez avec la clé client dates d’expiration.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-355">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="aa8b9-356">Obtenir l’URI pour chaque clé Azure clé coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-356">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="aa8b9-357"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-357"></span></span>

<span data-ttu-id="aa8b9-p149">Une fois que vous avez effectué toutes les étapes dans Azure pour configurer votre chambres fortes clés et ajouter vos clés, exécutez la commande suivante pour obtenir l’URI de la clé dans chaque clé coffre-fort. Vous devrez utiliser ces URI lorsque vous créez et affectez chaque PED ultérieurement, enregistre ces informations dans un endroit sûr. N’oubliez pas d’exécuter cette commande une fois pour chaque clé coffre-fort.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="aa8b9-361">Dans Azure PowerShell :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-361">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="aa8b9-362">Office 365 : Configuration de la clé client pour Exchange Online et Skype pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="aa8b9-362">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="aa8b9-363"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-363"></span></span>

<span data-ttu-id="aa8b9-p150">Avant de commencer, assurez-vous que vous avez effectué les tâches requises pour configurer Azure clé coffre-fort. Pour plus d’informations, voir [effectuer des tâches dans Azure clé coffre-fort et FastTrack Microsoft pour la clé client](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="aa8b9-366">Pour configurer la clé client pour Exchange Online et Skype pour les entreprises, vous devez effectuer ces étapes en vous connectant à distance à Exchange Online avec Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-366">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="aa8b9-367">Créer une stratégie de chiffrement des données (PED) pour une utilisation avec Exchange Online et Skype pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="aa8b9-367">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="aa8b9-368"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-368"></span></span>

<span data-ttu-id="aa8b9-p151">Un PED est associé à un ensemble de clés stockées dans Azure clé coffre-fort. Vous assignez un PED à une boîte aux lettres dans Office 365. Office 365 utilise les clés identifiés dans la stratégie pour crypter la boîte aux lettres. Pour créer la prévention, vous devez les URI de coffre-fort clé que vous avez obtenu précédemment. Pour obtenir des instructions, consultez la rubrique [obtenir l’URI pour chaque clé Azure clé coffre-fort](controlling-your-data-using-customer-key.md#GetKeyURI) .</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="aa8b9-p152">N’oubliez pas ! Lorsque vous créez un PED, vous spécifiez deux clés qui se trouvent dans deux différentes chambres fortes de clé Azure. Assurez-vous que ces clés sont trouvent dans deux régions Azure distinctes pour assurer la redondance géographique.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="aa8b9-377">Pour créer la prévention, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-377">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="aa8b9-378">Sur votre ordinateur local, avec un compte professionnel ou de l’école dispose des autorisations d’administrateur global dans votre organisation Office 365, [se connecter à Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) en ouvrant Windows PowerShell et en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-378">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="aa8b9-379">Dans la boîte de dialogue demande d’informations d’identification Windows PowerShell, entrez votre travail ou établissement des informations de compte et cliquez sur **OK**, puis entrez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-379">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="aa8b9-380">Exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-380">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="aa8b9-381">Pour créer un PED, utilisez l’applet de commande New-DataEncryptionPolicy en tapant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-381">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="aa8b9-382">Où :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-382">Where:</span></span>
    
   -  <span data-ttu-id="aa8b9-p153">*PolicyName* est le nom que vous souhaitez utiliser pour la stratégie. Les noms ne peuvent pas contenir d’espaces. Par exemple, USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="aa8b9-p154">*PolicyDescription* est une description conviviale de la stratégie qui permet de mémoriser est la stratégie pour. Vous pouvez inclure des espaces dans la description. Par exemple, racine clé pour les boîtes aux lettres des États-Unis et ses territoires.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="aa8b9-p155">*KeyVaultURI1* est l’URI de la première clé dans la stratégie. Par exemple, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="aa8b9-p156">*KeyVaultURI2* est l’URI de la deuxième clé dans la stratégie. Par exemple, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Séparez les deux URI par une virgule et un espace.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="aa8b9-394">Exemple :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-394">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="aa8b9-395">Affecter un PED à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="aa8b9-395">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="aa8b9-396"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-396"></span></span>

<span data-ttu-id="aa8b9-p157">Affecter la prévention à une boîte aux lettres à l’aide de l’applet de commande Set-Mailbox. Une fois que vous assignez à la stratégie, Office 365 peut chiffrer la boîte aux lettres avec la clé indiquée dans la prévention</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="aa8b9-p158">Où *MailboxIdParameter* spécifie une boîte aux lettres. Pour plus d’informations sur la cmdlet Set-Mailbox, voir [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="aa8b9-401">Valider le chiffrement de la boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="aa8b9-401">Validate mailbox encryption</span></span>
<span data-ttu-id="aa8b9-402"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-402"></span></span>

<span data-ttu-id="aa8b9-p159">Chiffrer une boîte aux lettres peut prendre un certain temps. Pour l’affectation de stratégie première fois, la boîte aux lettres doit également effectuer le déplacement d’une base de données vers un autre avant que le service peut crypter la boîte aux lettres. Nous vous conseillons d’attendre 72 heures avant de valider le chiffrement une fois que vous modifiez un PED ou la première fois que vous affectez une PED à une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="aa8b9-406">Utilisez l’applet de commande Get-MailboxStatistics pour déterminer si une boîte aux lettres est chiffré.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-406">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="aa8b9-407">La propriété IsEncrypted renvoie la valeur **true** si la boîte aux lettres est chiffré et la valeur **false** si la boîte aux lettres n’est pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-407">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="aa8b9-p160">La durée des déplacements de boîtes aux lettres varie selon le nombre de boîtes aux lettres à laquelle vous affectez une PED pour la première fois, ainsi que la taille des boîtes aux lettres. Si les boîtes aux lettres n’ont pas été chiffrées après une semaine depuis le moment où vous avez affecté la prévention, d’initier un déplacement de boîte aux lettres pour les boîtes aux lettres non chiffrés à l’aide de l’applet de commande New-MoveRequest.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="aa8b9-410">Office 365 : Configuration de la clé client pour SharePoint Online et OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="aa8b9-410">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="aa8b9-411"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-411"></span></span>

<span data-ttu-id="aa8b9-p161">Avant de commencer, assurez-vous que vous avez effectué les tâches requises pour configurer Azure clé coffre-fort. Pour plus d’informations, voir [effectuer des tâches dans Azure clé coffre-fort et FastTrack Microsoft pour la clé client](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="aa8b9-414">Pour configurer la clé client pour SharePoint Online et OneDrive entreprise, vous devez effectuer ces étapes en vous connectant à distance à SharePoint Online avec Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-414">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="aa8b9-415">Créer une stratégie de chiffrement des données (PED) pour chaque OneDrive et SharePoint Online pour entreprise geo</span><span class="sxs-lookup"><span data-stu-id="aa8b9-415">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="aa8b9-416"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-416"></span></span>

<span data-ttu-id="aa8b9-p162">Un PED est associé à un ensemble de clés stockées dans Azure clé coffre-fort. Vous appliquez un PED à toutes vos données dans un emplacement géographique, également appelé une geo. Si vous utilisez la fonctionnalité multi-geo d’Office 365 (en aperçu), vous pouvez créer un PED par localisés. Si vous n’utilisez pas multi-localisés, vous pouvez créer un PED dans Office 365 pour une utilisation avec SharePoint Online et OneDrive for Business. Office 365 utilise les clés identifiés dans le PED pour chiffrer des données dans cette zone géographique. Pour créer la prévention, vous devez les URI de coffre-fort clé que vous avez obtenu précédemment. Pour obtenir des instructions, consultez la rubrique [obtenir l’URI pour chaque clé Azure clé coffre-fort](controlling-your-data-using-customer-key.md#GetKeyURI) .</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="aa8b9-p163">N’oubliez pas ! Lorsque vous créez un PED, vous spécifiez deux clés qui se trouvent dans deux différentes chambres fortes de clé Azure. Assurez-vous que ces clés sont trouvent dans deux régions Azure distinctes pour assurer la redondance géographique.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="aa8b9-427">Pour créer un PED, vous devez vous connecter à distance à SharePoint Online à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-427">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="aa8b9-428">Sur votre ordinateur local, à l’aide un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365, [se connecter à SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx)Professionnel ou de l’école.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-428">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="aa8b9-429">Dans Microsoft SharePoint Online Management Shell, exécutez l’applet de commande [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-429">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="aa8b9-p164">Lorsque vous enregistrez la prévention, le chiffrement commence les données dans la zone géographique. Cela peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="aa8b9-432">Valider le chiffrement du groupe de Sites, Sites d’équipe et OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="aa8b9-432">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="aa8b9-433"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-433"></span></span>

<span data-ttu-id="aa8b9-434">Vous pouvez vérifier l’état de chiffrement en exécutant l’applet de commande Get-SPODataEncryptionPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-434">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="aa8b9-435">La sortie de cette applet de commande comprend :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-435">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="aa8b9-436">L’URI de la clé primaire.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-436">The URI of the primary key.</span></span>
    
- <span data-ttu-id="aa8b9-437">L’URI de la clé secondaire.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-437">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="aa8b9-p165">L’état de chiffrement pour la zone géographique. États possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="aa8b9-440">**Non enregistré :** Chiffrement de la clé client n’a pas été appliqué.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-440">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="aa8b9-p166">**Inscription :** Chiffrement de la clé client a été appliqué et vos fichiers sont en cours de chiffrement. Si votre geo est dans cet état, vous devez également être affichées plus d’informations sur quel pourcentage de sites dans la zone géographique sont complètes de sorte que vous pouvez surveiller la progression de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="aa8b9-443">**Enregistré :** Chiffrement de la clé client a été appliqué, et tous les fichiers dans tous les sites ont été chiffrés.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-443">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="aa8b9-p167">**Propagées :** Appliquer une clé est en cours. Si votre geo est dans cet état, vous devez également être affichées plus d’informations sur quel pourcentage de sites avoir effectué l’opération roll clés afin que vous pouvez surveiller la progression.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="aa8b9-446">Gestion de la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="aa8b9-446">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="aa8b9-447"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-447"></span></span>

<span data-ttu-id="aa8b9-448">Une fois que vous avez configuré la clé client pour Office 365, vous pouvez effectuer ces tâches de gestion supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-448">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="aa8b9-449">Restaurer les clés de coffre-fort de clé Azure</span><span class="sxs-lookup"><span data-stu-id="aa8b9-449">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="aa8b9-450">Restauration ou faire pivoter une clé dans Azure clé coffre-fort que vous utilisez avec la clé client</span><span class="sxs-lookup"><span data-stu-id="aa8b9-450">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="aa8b9-451">Gérer les autorisations de clés coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-451">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="aa8b9-452">Déterminer la PED affecté à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="aa8b9-452">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="aa8b9-453">Restaurer les clés de coffre-fort de clé Azure</span><span class="sxs-lookup"><span data-stu-id="aa8b9-453">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="aa8b9-454"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-454"></span></span>

<span data-ttu-id="aa8b9-p168">Avant d’effectuer une restauration, utilisez les fonctionnalités de récupération fournies par suppression réversible. Toutes les clés qui sont utilisés avec la clé client sont requis pour que la suppression réversible activée. Suppression réversible agit comme une Corbeille et permet la récupération pendant 90 jours sans avoir besoin de restaurer. Restauration doit être requis uniquement dans les circonstances extrêmes ou inhabituelles, par exemple, si la clé ou la clé coffre-fort est perdue. Si vous devez restaurer une clé pour une utilisation avec la clé de client dans Azure PowerShell, exécutez l’applet de commande Restore-AzureKeyVaultKey comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="aa8b9-460">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-460">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="aa8b9-p169">Si une clé portant le même nom existe déjà dans le coffre-fort clé, l’opération de restauration échoue. Restauration-AzureKeyVaultKey restaure toutes les versions principales et toutes les métadonnées pour la clé, y compris le nom de la clé.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="aa8b9-463">Restauration ou faire pivoter une clé dans Azure clé coffre-fort que vous utilisez avec la clé client</span><span class="sxs-lookup"><span data-stu-id="aa8b9-463">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="aa8b9-464"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-464"></span></span>

<span data-ttu-id="aa8b9-p170">Déploiement clés n’est pas requis par un coffre-fort de clé Azure ou par clé client. En outre, les clés qui sont protégés par un HSM sont pratiquement impossibles de compromettre. Même si une clé de la racine de la possession d’un acteur malveillant il n’existe aucun moyen possible de l’utiliser pour déchiffrer des données, dans la mesure où Office 365 uniquement le code sait comment l’utiliser. Restauration d’une clé est toutefois, pris en charge par clé client.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="aa8b9-p171">Déployer uniquement une clé de chiffrement que vous utilisez avec la clé client lorsque existe une raison technique effacer ou une exigence de conformité dicte que vous devrez déployer la clé. En outre, ne supprimez pas toutes les clés qui sont ou ont été associés à des stratégies. Lorsque vous faites vos clés, les qu’il n’y être contenu chiffré avec les précédentes clés. Par exemple, tandis que les boîtes aux lettres actives sont nouveau chiffrées fréquemment, inactif, les boîtes aux lettres déconnectées et désactivées peuvent toujours chiffrées avec les précédentes clés. SharePoint Online effectue sauvegarde de contenu à des fins de restauration et de récupération, il peut être toujours contenu archivé à l’aide des anciennes clés.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="aa8b9-p172">Pour garantir la sécurité de vos données, SharePoint Online permettra pas plus d’une clé reporter opération en cours à la fois. Si vous souhaitez déployer à la fois des clés dans un coffre-fort clé, vous devrez attendre la première opération roll clés à entièrement terminée. Nous conseillons échelonnez vos opérations de déploiement clés à des intervalles différents, afin que ce n’est pas un problème.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="aa8b9-p173">Lorsque vous faites une clé, vous demandez une nouvelle version d’une clé existante. Pour demander une nouvelle version d’une clé existante, vous utilisez la cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), même avec la même syntaxe que vous avez utilisé pour créer la clé en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="aa8b9-479">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-479">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="aa8b9-p174">Dans cet exemple, car une clé nommée **Contoso-O365EX-NA-VaultA1-Key001** déjà existe dans le coffre-fort **Contoso-O365EX-NA-VaultA1** , une nouvelle version de clés sera créée. L’opération ajoute une nouvelle version de la clé. Cette opération permet de conserver les versions précédentes de clé dans l’historique de version de la clé, afin que les données précédemment chiffrées avec cette clé peuvent toujours être déchiffrées. Une fois que vous avez terminé de roulement n’importe quelle touche qui est associé à un PED, vous devez exécuter une applet de commande supplémentaire pour garantir la que clé client commence avec la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="aa8b9-484">Activer Exchange Online et Skype pour les entreprises à utiliser une nouvelle clé après avoir reporter ou rotation des clés dans Azure clé coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-484">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="aa8b9-485">Lorsque vous faites une des clés Azure clé coffre-fort associés à un PED utilisé avec Exchange Online et Skype pour les entreprises, vous devez exécuter la commande suivante pour mettre à jour de la prévention et activer Office 365 commencer à utiliser la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-485">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="aa8b9-486">Pour indiquer la clé de client à utiliser la nouvelle clé pour chiffrer les boîtes aux lettres dans Office 365, exécutez l’applet de commande Set-DataEncryptionPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-486">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="aa8b9-p175">Dans les 48 heures, les boîtes aux lettres actives chiffrées à l’aide de cette stratégie sera associés à la clé de mise à jour. Utilisez les étapes de [déterminer la PED affecté à une boîte aux lettres](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) pour vérifier la valeur de la propriété DataEncryptionPolicyID pour la boîte aux lettres. La valeur de cette propriété modifie une fois la clé de mise à jour a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="aa8b9-490">Activer SharePoint Online et OneDrive entreprise à utiliser une nouvelle clé après avoir reporter ou rotation des clés dans Azure clé coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-490">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="aa8b9-491">Lorsque vous faites une des clés Azure clé coffre-fort associés à un PED utilisée avec SharePoint Online et OneDrive pour les entreprises, vous devez exécuter l’applet de commande [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) pour mettre à jour la prévention et activer Office 365 commencer à utiliser la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-491">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="aa8b9-p176">Démarre l’opération de déploiement clés pour SharePoint Online et OneDrive for Business. Cette action n’est pas immédiate. Pour afficher la progression de la clé à l’opération, exécutez l’applet de commande Get-SPODataEncryptionPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="aa8b9-495">Gérer les autorisations de clés coffre-fort</span><span class="sxs-lookup"><span data-stu-id="aa8b9-495">Manage key vault permissions</span></span>
<span data-ttu-id="aa8b9-496"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-496"></span></span>

<span data-ttu-id="aa8b9-p177">Plusieurs applets de commande qui permettent d’afficher et, si nécessaire, supprimer des autorisations de clés coffre-fort. Vous devrez peut-être supprimer les autorisations, par exemple, lorsqu’un employé quitte l’équipe.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="aa8b9-499">Pour afficher les autorisations de clés coffre-fort, exécutez l’applet de commande Get-AzureRmKeyVault :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-499">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="aa8b9-500">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-500">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="aa8b9-501">Pour supprimer des autorisations d’administrateur, exécutez l’applet de commande Remove-AzureRmKeyVaultAccessPolicy :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-501">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="aa8b9-502">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="aa8b9-502">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="aa8b9-503">Déterminer la PED affecté à une boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="aa8b9-503">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="aa8b9-504"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="aa8b9-504"></span></span>

<span data-ttu-id="aa8b9-p178">Pour déterminer la PED affecté à une boîte aux lettres, utilisez l’applet de commande Get-MailboxStatistics. L’applet de commande renvoie l’identificateur unique (GUID).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="aa8b9-p179">Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres. Pour plus d’informations sur l’applet de commande Get-MailboxStatistics, voir [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa8b9-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="aa8b9-509">Utilisez le GUID pour trouver le nom convivial de la prévention affectée de la boîte aux lettres en exécutant la cmdlet suivante.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-509">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="aa8b9-510">Où *GUID* est le GUID renvoyé par l’applet de commande Get-MailboxStatistics à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="aa8b9-510">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  

