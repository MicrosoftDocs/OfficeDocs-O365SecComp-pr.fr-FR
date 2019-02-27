---
title: Contrôle de vos données dans Office 365 à l'aide de la Clé client.
ms.author: krowley
author: kccross
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
ms.openlocfilehash: 219ddb94727cd2b708f734a77a8397b3bc3f1064
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296667"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a>Contrôle de vos données dans Office 365 à l'aide de la Clé client.

Avec la clé client, vous contrôlez les clés de chiffrement de votre organisation, puis vous configurez Office 365 afin de les utiliser pour chiffrer vos données au repos dans les centres de données de Microsoft. En d'autres termes, la clé client permet aux clients d'ajouter une couche de chiffrement qui leur appartient, avec leurs clés. Les données de Rest incluent des données à partir d'Exchange Online et de Skype entreprise, qui sont stockées dans des boîtes aux lettres et des fichiers stockés dans SharePoint Online et OneDrive entreprise.
  
Vous devez configurer Azure avant de pouvoir utiliser la clé client pour Office 365. Cette rubrique décrit les étapes à suivre pour créer et configurer les ressources Azure requises, puis fournit la procédure de configuration de la clé client dans Office 365. Une fois que vous avez terminé la configuration d'Azure, vous déterminez la stratégie et, par conséquent, les clés, à affecter aux boîtes aux lettres et aux fichiers de votre organisation. Les boîtes aux lettres et les fichiers pour lesquels vous n'affectez pas de stratégie utilisent des stratégies de chiffrement qui sont contrôlées et gérées par Microsoft. Pour plus d'informations sur la clé client ou pour obtenir une vue d'ensemble, consultez la rubrique [customEr Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).
  
> [!IMPORTANT]
> Nous vous recommandons vivement de suivre les meilleures pratiques de cette rubrique. Ces éléments sont appelés « **Conseil** » et « **important**». La clé client vous permet de contrôler les clés de chiffrement racines dont l'étendue peut être aussi importante que l'ensemble de votre organisation. Cela signifie que les erreurs comprises avec ces clés peuvent avoir un impact général et peuvent entraîner des interruptions de service ou une perte irrévocable de vos données. 
  
## <a name="before-you-begin-setting-up-customer-key"></a>Avant de commencer la configuration de la clé client
<a name="Beforeyoustart"> </a>

Avant de commencer, assurez-vous que vous disposez de la licence appropriée pour votre organisation. La clé client dans Office 365 est proposée dans Office 365 E5 ou le SKU de conformité avancée.
  
Ensuite, pour comprendre les concepts et les procédures présentés dans cette rubrique, consultez la documentation sur le [coffre de stockage de clés Azure](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . De même, familiarisez-vous avec les termes utilisés dans Azure, par exemple, [client](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).
  
Pour fournir des commentaires sur la clé client, y compris la documentation, envoyez vos idées, suggestions et perspectives à customerkeyfeedback@microsoft.com.
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a>Vue d'ensemble de la configuration de la clé client pour Office 365
<a name="Overview"> </a>

Pour configurer la clé client, vous devez effectuer ces tâches. Le reste de cette rubrique fournit des instructions détaillées pour chaque tâche, ou des liens vers des informations supplémentaires pour chaque étape du processus.
  
**Dans Azure et Microsoft FastTrack:**
  
Vous effectuerez la plupart de ces tâches en vous connectant à distance à Azure PowerShell. Pour obtenir de meilleurs résultats, utilisez la version 4.4.0 ou une version ultérieure d'Azure PowerShell.
  
- [Créer deux nouveaux abonnements Azure](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [Enregistrer des abonnements Azure pour utiliser une période de rétention obligatoire](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    L'inscription peut prendre entre un et cinq jours ouvrés.
    
- [Soumettre une demande d'activation de la clé client pour Office 365](controlling-your-data-using-customer-key.md#FastTrack)
    
    Une fois que vous avez créé les deux nouveaux abonnements Azure, vous devez soumettre la demande d'offre de clé client appropriée en remplissant un formulaire Web hébergé dans le portail Microsoft FastTrack. **L'équipe FastTrack ne fournit pas d'assistance pour la clé client. Office utilise simplement le portail FastTrack pour vous permettre d'envoyer le formulaire et de nous aider à suivre les offres pertinentes pour la clé client**.
  
Une fois que vous avez soumis une offre de clé de client, Microsoft révise votre demande et vous avertit lorsque vous pouvez effectuer les autres tâches de configuration. Ce processus peut prendre jusqu'à cinq jours ouvrés.
    
- [Créer un coffre-fort de clés Azure pour chaque abonnement](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [Attribuer des autorisations à chaque coffre-fort de clés](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [Activer, puis confirmer la suppression logicielle de vos coffres-forts principaux](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [Ajouter une clé à chaque coffre-fort de clés en créant ou en important une clé](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [Vérifier le niveau de récupération de vos clés](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [Sauvegarder le coffre de clés Azure](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [Valider les paramètres de configuration de coffre-fort de clés Azure](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [Obtenir l'URI de chaque clé Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI)
    
**Dans Office 365:**
  
Exchange Online et Skype entreprise:
  
- [Créer une stratégie de chiffrement de données (DEP) à utiliser avec Exchange Online et Skype entreprise](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [Affecter une DEP à une boîte aux lettres](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [Valider le chiffrement de boîtes aux lettres](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
SharePoint Online et OneDrive entreprise:
  
- [Créer une stratégie de chiffrement de données (DEP) pour chaque région de SharePoint Online et OneDrive entreprise](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [Valider le chiffrement des sites de groupe, des sites d'équipe et de OneDrive entreprise](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a>Effectuer des tâches dans Azure Key Vault et Microsoft FastTrack pour la clé client
<a name="AzureSteps"> </a>

Effectuez ces tâches dans Azure Key Vault afin de configurer la clé client pour Office 365. Vous devrez effectuer ces étapes, que vous souhaitiez configurer la clé client pour Exchange Online et Skype entreprise ou SharePoint Online et OneDrive entreprise ou pour tous les services pris en charge dans Office 365.
  
### <a name="create-two-new-azure-subscriptions"></a>Créer deux nouveaux abonnements Azure
<a name="Create2newsubs"> </a>

Deux abonnements Azure sont requis pour la clé client. Pour une meilleure pratique, Microsoft vous recommande de créer de nouveaux abonnements Azure à utiliser avec la clé client. Les clés Azure Key Vault peuvent uniquement être autorisées pour les applications dans le même client Azure Active Directory (AAD), vous devez créer les nouveaux abonnements à l'aide du même client Azure AD utilisé avec votre organisation Office 365 où les DEPs seront attribués. Par exemple, à l'aide de votre compte professionnel ou scolaire disposant de privilèges d'administrateur général dans votre organisation Office 365. Pour obtenir la procédure détaillée, consultez la rubrique [Inscrivez-vous à Azure en tant qu'organisation](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).
  
> [!IMPORTANT]
> La clé client nécessite deux clés pour chaque stratégie de chiffrement de données (DEP). Pour ce faire, vous devez créer deux abonnements Azure. En guise de meilleure pratique, Microsoft recommande que les membres distincts de votre organisation configurent une clé dans chaque abonnement. En outre, ces abonnements Azure ne doivent être utilisés que pour administrer les clés de chiffrement pour Office 365. Cela protège votre organisation si l'un de vos opérateurs supprime accidentellement, intentionnellement ou de manière malveillante ou non des clés dont il est responsable.<br/> Nous vous recommandons de configurer de nouveaux abonnements Azure uniquement utilisés pour gérer les ressources Azure Key Vault à utiliser avec la clé client. Il n'existe pas de limite pratique au nombre d'abonnements Azure que vous pouvez créer pour votre organisation. Le suivi de ces meilleures pratiques réduira l'impact de l'erreur humaine tout en aidant à gérer les ressources utilisées par la clé client. 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a>Soumettre une demande d'activation de la clé client pour Office 365
<a name="FastTrack"> </a>

Une fois que vous avez terminé les étapes Azure, vous devrez soumettre une demande d'offre dans le [portail Microsoft FastTrack](https://fasttrack.microsoft.com/). Une fois que vous avez soumis une demande via le portail Web FastTrack, Microsoft vérifie les données de configuration du coffre de clés Azure et les informations de contact que vous avez fournies. Les sélections effectuées dans le formulaire d'offre concernant les responsables autorisés de votre organisation sont essentielles et nécessaires à la réalisation de l'enregistrement de la clé client. Les responsables de votre organisation sélectionnés dans le formulaire seront utilisés pour garantir l'authenticité de toute demande de révocation et de destruction de toutes les clés utilisées avec une stratégie de chiffrement des données de clé client. Vous devrez effectuer cette étape une fois pour activer la clé client pour la couverture Exchange Online et Skype entreprise et une deuxième fois pour activer la clé client pour SharePoint Online et OneDrive entreprise.
  
Pour soumettre une offre d'activation de la clé client, procédez comme suit:
  
1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, connectez-vous au [portail Microsoft FastTrack](https://fasttrack.microsoft.com/).
    
2. Une fois que vous êtes connecté, accédez au **tableau de bord**.
    
3. Choisissez **offres**, puis passez en revue la liste des offres actuelles.
    
4. Choisissez **en savoir plus** pour l'offre qui vous concerne: 
    
  - **Exchange Online et Skype entreprise:** Sélectionnez **en savoir plus** sur la **clé client pour** l'offre Exchange. 
    
  - **SharePoint Online et OneDrive entreprise:** Choisissez **en savoir plus** sur la **clé client pour SharePoint et OneDrive entreprise** . 
    
5. Sur la page Détails de l' **offre** , sélectionnez **créer une demande**.
    
6. Renseignez toutes les informations pertinentes et les informations demandées dans le formulaire d'offre. Prêtez particulièrement attention à vos choix pour les responsables de votre organisation autorisés à approuver la destruction permanente et irréversible des clés et des données de chiffrement. Une fois que vous avez terminé le formulaire, sélectionnez **Envoyer**.
    
    Ce processus peut prendre jusqu'à cinq jours ouvrés une fois que Microsoft a été informé de votre demande.
    
7. Passez à la section période de rétention obligatoire ci-dessous.
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a>Enregistrer des abonnements Azure pour utiliser une période de rétention obligatoire
<a name="RegisterSubsforMRP"> </a>

La perte temporaire ou définitive de clés de chiffrement racine peut être très perturbatrice ou même catastrophique pour les opérations de service et peut entraîner une perte de données. Pour cette raison, les ressources utilisées avec la clé client nécessitent une protection renforcée. Toutes les ressources Azure utilisées avec les mécanismes de protection de l'offre de clé client au-delà de la configuration par défaut. Les abonnements Azure peuvent être balisés ou enregistrés de manière à empêcher toute annulation immédiate et irrévocable. Il s'agit de l'enregistrement pour une période de rétention obligatoire. Les étapes requises pour enregistrer les abonnements Azure pour une période de rétention obligatoire nécessitent une collaboration avec l'équipe Office 365. Ce processus peut prendre entre un et cinq jours ouvrés. Auparavant, il était parfois appelé «ne pas annuler».
  
Avant de contacter l'équipe Office 365, vous devez effectuer les étapes suivantes pour chaque abonnement Azure que vous utilisez avec la clé client:
  
1. Connectez-vous à votre abonnement Azure avec Azure PowerShell. Pour obtenir des instructions, consultez la rubrique [se connecter avec Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
2. Exécutez la cmdlet Register-AzureRmProviderFeature pour enregistrer vos abonnements afin d'utiliser une période de rétention obligatoire.
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. Contactez Microsoft pour finaliser le processus. Pour l'équipe SharePoint et OneDrive entreprise, contactez [Spock@microsoft.com](mailto:spock@microsoft.com). Pour Exchange Online et Skype entreprise, contactez [exock@microsoft.com](mailto:exock@microsoft.com). Le contrat de niveau de service (SLA) pour la fin de ce processus est de cinq jours ouvrés une fois que Microsoft a été informé (et vérifié) que vous avez enregistré vos abonnements afin d'utiliser une période de rétention obligatoire. Incluez les éléments suivants dans votre courrier:
    
    **Subject**: clé client pour \< *le nom de domaine complet de votre client*\> 
    
    **Body**: ID d'abonnement pour lesquels vous souhaitez que la période de rétention obligatoire soit finalisée. 
    
4. Une fois que vous recevez une notification de Microsoft que l'enregistrement est terminé, vérifiez l'état de votre inscription en exécutant la cmdlet Get-AzureRmProviderFeature comme suit:
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. Après avoir vérifié que la propriété **d'État** de l'inscription de la cmdlet Get-AzureRmProviderFeature renvoie la valeur **Registered**, exécutez la commande suivante pour terminer le processus:
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a>Créer un coffre-fort de clés Azure pour chaque abonnement
<a name="CreateKeyVault"> </a>

Les étapes de création d'un coffre-fort clé sont documentées dans [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), qui vous guide tout au long de l'installation et du lancement d'Azure PowerShell, de la connexion à votre abonnement Azure, de la création d'un groupe de ressources et de la création d'un coffre-fort de clés dans ce Groupe de ressources.
  
Lorsque vous créez un coffre-fort de clés, vous devez choisir un SKU: standard ou Premium. La référence SKU standard permet de protéger les clés du coffre-fort de clés Azure avec le logiciel: il n'existe pas de protection de clé HSM (Hardware Security Module) et la référence Premium permet d'utiliser des HSM pour la protection des clés de coffre-fort. La clé client accepte les coffres clés qui utilisent l'un des deux SKU, bien que Microsoft recommande vivement d'utiliser uniquement le SKU Premium. Le coût des opérations avec des clés de l'un des deux types est le même, de sorte que la seule différence de coût est le coût par mois pour chaque clé protégée par HSM. Pour plus d'informations, consultez la rubrique [prix clé du coffre](https://azure.microsoft.com/pricing/details/key-vault/) . 
  
> [!IMPORTANT]
> Utilisez les coffres-forts de clés SKU Premium et les clés protégées par HSM pour les données de production, et utilisez uniquement les clés et coffres-forts de clé SKU standard à des fins de test et de validation. 
  
Pour chaque service Office 365 avec lequel vous utiliserez la clé client, créez un coffre-fort de clés dans chacun des deux abonnements Azure que vous avez créés. Par exemple, pour Exchange Online et Skype entreprise uniquement ou SharePoint Online et OneDrive entreprise uniquement, vous ne devez créer qu'une seule paire de coffres-forts. Pour activer la clé client pour Exchange Online et SharePoint Online, vous devez créer deux paires de coffres-forts clés.
  
Utilisez une convention d'affectation de noms pour les coffres-forts de clés reflétant l'utilisation prévue de la DEP avec laquelle vous allez associer les coffres-forts. Consultez la section Méthodes conseillées ci-dessous pour connaître les recommandations de convention d'affectation de noms.
  
Créez un ensemble distinct de coffres couplés pour chaque stratégie de chiffrement de données. Pour Exchange Online, l'étendue d'une stratégie de chiffrement de données est choisie par vous lorsque vous affectez la stratégie à la boîte aux lettres. Une boîte aux lettres ne peut avoir qu'une seule stratégie affectée, et vous pouvez créer jusqu'à 50 stratégies. Pour SharePoint Online, l'étendue d'une stratégie est l'ensemble des données d'une organisation se trouvant dans un emplacement géographique ou dans une région géographique.
  
La création de coffre-fort de clés nécessite également la création de groupes de ressources Azure, car les coffres clés nécessitent une capacité de stockage (bien que très petite) et la journalisation de coffre de clés, si elle est activée, génère également des données stockées. Pour une meilleure pratique, Microsoft recommande d'utiliser des administrateurs distincts pour gérer chaque groupe de ressources, avec l'administration alignée sur l'ensemble des administrateurs qui géreront toutes les ressources liées à la clé client correspondante.
  
> [!IMPORTANT]
> Pour optimiser la disponibilité, vos coffres-forts principaux doivent se trouver dans des régions proches de votre service Office 365. Par exemple, si votre organisation Exchange Online est en Amérique du Nord, placez vos coffres clés en Amérique du Nord. Si votre organisation Exchange Online est en Europe, placez vos coffres clés en Europe.<br/>Utiliser un préfixe commun pour les coffres clés, et inclure une abréviation de l'utilisation et de l'étendue du coffre-fort de clés et des clés (par exemple, pour le service Contoso SharePoint où les coffres seront situés en Amérique du Nord, une paire possible de noms est contoso-O365SP-NA-VaultA1 et Contoso-O365SP-NA-VaultA2. Les noms de coffre-fort sont des chaînes uniques au sein d'Azure, de sorte que vous devrez peut-être essayer des variantes des noms souhaités au cas où les noms souhaités seraient déjà réclamés par d'autres clients Azure. Depuis juillet 2017, les noms de coffre-fort ne peuvent pas être modifiés, c'est pourquoi il est recommandé de disposer d'un plan écrit pour la configuration et d'utiliser une deuxième personne pour vérifier que le plan est exécuté correctement.<br/>Si possible, créez vos coffres dans des régions non couplées. Les régions Azure couplées fournissent une haute disponibilité entre les domaines ayant échoué. Par conséquent, les paires régionales peuvent être considérées comme la région de sauvegarde de chacune d'elles. Cela signifie qu'une ressource Azure placée dans une région bénéficie automatiquement de la tolérance de panne par le biais de la région couplée. Pour cette raison, le choix des régions pour deux coffres utilisés dans une DEP lorsque les régions sont couplées signifie que seul un total de deux régions de disponibilité est en cours d'utilisation. La plupart des régions géographiques n'ont que deux régions, de sorte qu'il n'est pas encore possible de sélectionner des régions non couplées. Si possible, choisissez deux régions non couplées pour les deux coffres utilisés avec une DEP. Cette opération bénéficie d'un total de quatre régions de disponibilité. Pour plus d'informations, consultez la rubrique [services de continuité d'activité et de récupération d'urgence (BCDR): régions coupléEs Azure](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) pour obtenir la liste actuelle des paires régionales. 
  
### <a name="assign-permissions-to-each-key-vault"></a>Attribuer des autorisations à chaque coffre-fort de clés
<a name="KeyVaultPerms"> </a>

Pour chaque coffre-fort de clés, vous devez définir trois ensembles distincts d'autorisations pour la clé client, en fonction de votre implémentation. Par exemple, vous devez définir un ensemble d'autorisations pour chacun des éléments suivants:
  
- **Administrateurs de coffre-fort principal** qui effectueront la gestion quotidienne de votre coffre-fort pour votre organisation. Ces tâches incluent Backup, Create, Get, Import, List et Restore. 
    
    > [!IMPORTANT]
    > Le jeu d'autorisations affectées aux administrateurs de coffre-fort n'inclut pas l'autorisation de suppression de clés. Cette procédure est intentionnelle et pratique importante. La suppression de clés de chiffrement n'est généralement pas effectuée, car cette opération détruit définitivement les données. Nous vous recommandons de ne pas accorder cette autorisation aux administrateurs de coffre-fort par défaut. Au lieu de cela, réservez ceci pour les contributeurs de coffre-fort principal et ne l'attribuez à un administrateur de manière courte qu'une fois qu'une bonne compréhension des conséquences est comprise. 
  
    Pour attribuer ces autorisations à un utilisateur dans votre organisation Office 365, connectez-vous à votre abonnement Azure avec Azure PowerShell. Pour obtenir des instructions, consultez la rubrique [se connecter avec Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
- Exécutez la cmdlet Set-AzureRmKeyVaultAccessPolicy pour attribuer les autorisations nécessaires.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  Par exemple :
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- Les contributeurs de **coffre-fort de clé** qui peuvent modifier les autorisations sur le coffre-fort des clés Azure. Vous devrez modifier ces autorisations lorsque les employés quittent ou rejoignent votre équipe, ou dans la situation extrêmement rare que les administrateurs clés de coffre-fort ont besoin de l'autorisation de supprimer ou de restaurer une clé. Cet ensemble de contributeurs de coffre-fort doit recevoir le rôle de **contributeur** sur votre coffre-fort de clés. Vous pouvez attribuer ce rôle à l'aide d'Azure Resource Manager. Pour obtenir la procédure détaillée, consultez [la rubrique utiliser le contrôle d'accès basé sur un rôle pour gérer l'accès à vos ressources d'abonnement Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). L'administrateur qui crée un abonnement bénéficie implicitement de cet accès, ainsi que de la possibilité d'affecter d'autres administrateurs au rôle contributeur.
    
- Si vous envisagez d'utiliser la clé client avec Exchange Online et Skype entreprise, vous devez accorder à Office 365 l'autorisation d'utiliser le coffre-fort de clés pour Exchange Online et Skype entreprise. De même, si vous avez l'intention d'utiliser la clé client avec SharePoint Online et OneDrive entreprise, vous devez ajouter des autorisations pour l'Office 365 afin d'utiliser le coffre-fort de clés pour SharePoint Online et OneDrive entreprise. Pour accorder l'autorisation à Office 365, exécutez la cmdlet **Set-AzureRmKeyVaultAccessPolicy** à l'aide de la syntaxe suivante: 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    Où :
    
  - *VAULTNAME* est le nom du coffre-fort de clés que vous avez créé. 
    
  - Pour Exchange Online et Skype entreprise, remplacez *Office 365 AppID* par`00000002-0000-0ff1-ce00-000000000000`
    
  - Pour SharePoint Online et OneDrive entreprise, remplacez *Office 365 AppID* par`00000003-0000-0ff1-ce00-000000000000`
    
  Exemple: définition des autorisations pour Exchange Online et Skype entreprise:
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  Exemple: définition des autorisations pour SharePoint Online et OneDrive entreprise
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a>Activer, puis confirmer la suppression logicielle de vos coffres-forts principaux
<a name="SoftDelete"> </a>

Lorsque vous pouvez rapidement récupérer vos clés, il est moins probable que vous rencontriez une panne de service étendue en raison de la suppression accidentelle ou malveillante de clés. Vous devez activer cette configuration, appelée suppression récupérable, avant de pouvoir utiliser vos clés avec la clé client. L'activation de la suppression douce vous permet de récupérer des clés ou des coffres dans les 90 jours suivant la suppression sans avoir à les restaurer à partir d'une sauvegarde.
  
Pour activer la suppression logicielle sur vos coffres-forts principaux, procédez comme suit:
  
1. Connectez-vous à votre abonnement Azure avec Windows PowerShell. Pour obtenir des instructions, consultez la rubrique [se connecter avec Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).
    
2. Exécutez la cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . Dans cet exemple, *VAULTNAME* est le nom du coffre-fort de clés pour lequel vous activez la suppression douce: 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. Vérifiez que la suppression logicielle est configurée pour le coffre-fort de clés en exécutant la cmdlet **Get-AzureRmKeyVault** . Si la suppression logicielle est correctement configurée pour le coffre-fort de clés, la suppression logicielle est-elle activée? la propriété renvoie la valeur **true**: 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a>Ajouter une clé à chaque coffre-fort de clés en créant ou en important une clé
<a name="AddKeystoKeyVault"> </a>

Il existe deux façons d'ajouter des clés à un coffre-fort de clés Azure; vous pouvez créer une clé directement dans le coffre-fort de clés ou importer une clé. La création d'une clé directement dans le coffre-fort est la méthode moins compliquée, tandis que l'importation d'une clé fournit un contrôle total sur la génération de la clé.
  
Pour créer une clé directement dans votre coffre-fort de clés, exécutez la cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) comme suit: 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

Où :
  
-  *VAULTNAME* est le nom du coffre-fort de clés dans lequel vous souhaitez créer la clé. 
    
-  *keyName* est le nom que vous souhaitez donner à la nouvelle clé. 
    
    > [!TIP]
    > Clés de nom à l'aide d'une convention d'affectation de noms similaire à celle décrite ci-dessus pour les coffres clés. De cette manière, dans les outils qui affichent uniquement le nom de la clé, la chaîne est auto-descriptive. 
  
- Si vous avez l'intention de protéger la clé avec un HSM, vérifiez que vous spécifiez **HSM** comme valeur du paramètre _destination_ , sinon, spécifiez **Software**.
    
Par exemple,
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

Pour importer directement une clé dans votre coffre-fort de clés, vous devez disposer d'un module de sécurité matérielle Thales nShield.
  
Certaines organisations préfèrent établir la provenance de leurs clés, et la méthode this fournit également les éléments suivants:
  
- L'ensemble d'outils utilisé pour l'importation comprend l'attestation de Thales indiquant que la clé d'échange Key (KEK) utilisée pour chiffrer la clé que vous générez n'est pas exportable et qu'elle est générée à l'intérieur d'un HSM authentique fabriqué par Thales.
    
- L'ensemble d'outils inclut l'attestation de Thales qui a également été générée par le World Key Vault Security sur un autoHSM authentique fabriqué par Thales. Cette attestation prouve que Microsoft utilise également du matériel Thales authentique.
    
Vérifiez auprès de votre groupe de sécurité si les attestations ci-dessus sont requises. Pour obtenir la procédure détaillée de création d'une clé locale et de son importation dans votre coffre-fort de clés, consultez [la rubrique How to Generate and Transfer My protected Keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Utilisez les instructions Azure pour créer une clé dans chaque coffre-fort de clés.
  
### <a name="check-the-recovery-level-of-your-keys"></a>Vérifier le niveau de récupération de vos clés
<a name="CheckKeyRecoveryLevel"> </a>

Office 365 nécessite que le abonnement Azure Key Vault soit défini sur do not Cancel et que les clés utilisées par la clé client aient activé la suppression douce. Vous pouvez vérifier cela en examinant le niveau de récupération de vos clés.
  
Pour vérifier le niveau de récupération d'une clé, dans Azure PowerShell, exécutez la cmdlet Get-AzureKeyVaultKey comme suit:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

Si la propriété de _niveau de récupération_ renvoie une valeur autre que **récupérable + ProtectedSubscription**, vous devez consulter cette rubrique et vous assurer que vous avez suivi toutes les étapes de mise en place de l'abonnement dans la liste ne pas annuler et que vous avez activé la suppression douce sur chaque coffre-fort de votre clé.
  
### <a name="backup-azure-key-vault"></a>Sauvegarder le coffre de clés Azure
<a name="BackupAzureKeyVaultkeys"> </a>

Immédiatement après la création ou la modification d'une clé, effectuez une sauvegarde et stockez des copies de la sauvegarde, en ligne et hors connexion. Les copies hors connexion ne doivent pas être connectées à un réseau, par exemple dans une installation de stockage sécurisé physique ou commerciale. Au moins une copie de la sauvegarde doit être stockée à un emplacement accessible en cas de sinistre. Les objets BLOB de sauvegarde constituent le seul moyen de restaurer le matériel de clé si une clé de coffre-fort de clé est détruite définitivement ou s'il est inopérable. Les clés externes au coffre-fort Azure et qui ont été importées vers le coffre-fort Azure ne sont pas qualifiées de sauvegarde car les métadonnées nécessaires à l'utilisation de la clé par le client n'existent pas avec la clé externe. Seule une sauvegarde effectuée à partir du coffre-fort de clés Azure peut être utilisée pour les opérations de restauration avec la clé client. Par conséquent, il est essentiel qu'une sauvegarde du coffre de clés Azure soit effectuée une fois qu'une clé est chargée ou créée.
  
Pour créer une sauvegarde d'une clé Azure Key Vault, exécutez la cmdlet [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) comme suit:
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

Assurez-vous que votre fichier de `.backup`sortie utilise le suffixe.
  
Le fichier de sortie résultant de cette cmdlet est chiffré et ne peut pas être utilisé en dehors du coffre-fort de clés Azure. La sauvegarde ne peut être restaurée qu'à partir de l'abonnement Azure à partir duquel la sauvegarde a été effectuée.
  
> [!TIP]
> Pour le fichier de sortie, choisissez une combinaison de votre nom de coffre-fort et de votre nom de clé. Cela fera en sorte que le nom de fichier soit auto-descriptif. Elle garantit également que les noms de fichier de sauvegarde n'entrent pas en conflit. 
  
Par exemple :
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a>Valider les paramètres de configuration de coffre-fort de clés Azure
<a name="Validateconfiguration"> </a>

Effectuer la validation avant d'utiliser des clés dans une DEP est facultatif, mais fortement recommandé. En particulier, si vous utilisez les étapes pour configurer vos clés et coffres-forts autres que ceux décrits dans cette rubrique, vous devez valider l'intégrité de vos ressources Azure Key Vault avant de configurer la clé client.
  
Pour vérifier que les opérations Get, wrapKey et unwrapKey sont activées sur vos clés, procédez comme suit:
  
Exécutez la cmdlet [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) comme suit: 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

Dans la sortie, recherchez la stratégie d'accès et l'identité Exchange Online (GUID) ou l'identité SharePoint Online (GUID), selon le cas. Les trois autorisations ci-dessus doivent être affichées sous autorisations sur clés.
  
Si la configuration de la stratégie d'accès est incorrecte, exécutez la cmdlet Set-AzureRmKeyVaultAccessPolicy comme suit:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

Par exemple, pour Exchange Online et Skype entreprise:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

Par exemple, pour SharePoint Online et OneDrive entreprise:
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

Pour vérifier qu'une date d'expiration n'est pas définie pour vos clés, exécutez la cmdlet [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) comme suit: 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

Une clé expirée ne peut pas être utilisée par la clé client et les opérations tentées avec une clé expirée échoueront, ce qui peut entraîner une panne de service. Il est vivement recommandé que les clés utilisées avec la clé client n'aient pas de date d'expiration. Une date d'expiration, une fois définie, ne peut pas être supprimée, mais peut être remplacée par une date différente. Si une clé doit être utilisée avec une date d'expiration définie, modifiez la valeur d'expiration sur 12/31/9999. Les clés dont la date d'expiration est définie sur une date autre que 12/31/9999 ne réussiront pas la validation d'Office 365.
  
Pour modifier une date d'expiration qui a été définie sur une valeur autre que 12/31/9999, exécutez la cmdlet [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) comme suit: 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> Ne définissez pas de date d'expiration sur les clés de chiffrement que vous utilisez avec la clé client. 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a>Obtenir l'URI de chaque clé Azure Key Vault
<a name="GetKeyURI"> </a>

Une fois que vous avez effectué toutes les étapes dans Azure pour configurer votre coffre-fort de clés et ajouté vos clés, exécutez la commande suivante pour obtenir l'URI de la clé dans chaque coffre-fort de clés. Vous devrez utiliser ces URI lorsque vous créerez et affecterez chaque DEP plus tard, donc Enregistrez ces informations dans un endroit sûr. N'oubliez pas d'exécuter cette commande une fois pour chaque coffre-fort de clés.
  
Dans Azure PowerShell:
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a>Office 365: configuration de la clé client pour Exchange Online et Skype entreprise
<a name="AzureSteps"> </a>

Avant de commencer, vérifiez que vous avez terminé les tâches requises pour configurer Azure Key Vault. Pour plus d'informations, consultez la rubrique [tâches terminées dans Azure Key Vault et Microsoft FastTrack pour la clé client](controlling-your-data-using-customer-key.md#AzureSteps) . 
  
Pour configurer la clé client pour Exchange Online et Skype entreprise, vous devez effectuer ces étapes en vous connectant à distance à Exchange Online à l'aide de Windows PowerShell.
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a>Créer une stratégie de chiffrement de données (DEP) à utiliser avec Exchange Online et Skype entreprise
<a name="CreateDEP4EXOSkype"> </a>

Une DEP est associée à un ensemble de clés stockées dans Azure Key Vault. Vous affectez une DEP à une boîte aux lettres dans Office 365. Office 365 utilisera ensuite les clés identifiées dans la stratégie pour chiffrer la boîte aux lettres. Pour créer la DEP, vous avez besoin des URI de coffre-fort que vous avez obtenus précédemment. Consultez [la rubrique obtenir l'URI pour chaque clé Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI) pour obtenir des instructions. 
  
Pensez! Lorsque vous créez une DEP, vous spécifiez deux clés qui résident dans deux coffres de clés Azure différents. Assurez-vous que ces clés se situent dans deux régions Azure distinctes pour garantir la redondance géographique.
  
Pour créer la DEP, procédez comme suit:
  
1. Sur votre ordinateur local, à l'aide d'un compte professionnel ou scolaire disposant d'autorisations d'administrateur général dans votre organisation Office 365, [Connectez-vous à Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) en ouvrant Windows PowerShell et en exécutant la commande suivante. 
    
   ```
   $UserCredential = Get-Credential
   ```

2. Dans la boîte de dialogue demande d'informations d'identification Windows PowerShell, entrez vos informations de compte professionnel ou scolaire, cliquez sur **OK**, puis entrez la commande suivante. 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. Exécutez la commande suivante.
    
   ```
   Import-PSSession $Session
   ```

4. Pour créer une DEP, utilisez la cmdlet New-DataEncryptionPolicy en tapant la commande suivante.
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   Où :
    
   -  *PolicyName* est le nom que vous souhaitez utiliser pour la stratégie. Les noms ne peuvent pas contenir d'espaces. Par exemple, USA_mailboxes. 
    
   -  *PolicyDescription* est une description conviviale de la stratégie qui vous permettra de vous souvenir de ce à quoi la stratégie est destinée. Vous pouvez inclure des espaces dans la description. Par exemple, la clé racine des boîtes aux lettres des États-Unis et de ses territoires. 
    
   -  *KeyVaultURI1* est l'URI de la première clé de la stratégie. Par exemple, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01. 
    
   -  *KeyVaultURI2* est l'URI de la deuxième clé de la stratégie. Par exemple, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Séparez les deux URI par une virgule et un espace. 
    
   Exemple :
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a>Affecter une DEP à une boîte aux lettres
<a name="assignDEPtomailbox"> </a>

Affecter la DEP à une boîte aux lettres à l'aide de la cmdlet Set-Mailbox. Une fois que vous avez affecté la stratégie, Office 365 peut chiffrer la boîte aux lettres à l'aide de la clé désignée dans la DEP.
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

Où *MailboxIdParameter* spécifie une boîte aux lettres. Pour plus d'informations sur la cmdlet Set-Mailbox, consultez la rubrique [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).
  
### <a name="validate-mailbox-encryption"></a>Valider le chiffrement de boîtes aux lettres
<a name="validatemailboxencryption"> </a>

Le chiffrement d'une boîte aux lettres peut prendre du temps. Pour une attribution de stratégie de première exécution, la boîte aux lettres doit également effectuer le déplacement d'une base de données à une autre pour que le service puisse chiffrer la boîte aux lettres. Nous vous recommandons d'attendre 72 heures avant de valider le chiffrement après avoir modifié une DEP ou la première fois que vous affectez une DEP à une boîte aux lettres.
  
Utilisez la cmdlet Get-MailboxStatistics pour déterminer si une boîte aux lettres est chiffrée.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

La propriété IsEncrypted renvoie la valeur **true** si la boîte aux lettres est chiffrée et la valeur **false** si la boîte aux lettres n'est pas chiffrée. 

Le temps nécessaire au déplacement des boîtes aux lettres dépend du nombre de boîtes aux lettres auxquelles vous affectez une DEP pour la première fois, ainsi que de la taille des boîtes aux lettres. Si les boîtes aux lettres n'ont pas été chiffrées après une semaine à partir du moment où vous avez attribué la DEP, lancez un déplacement de boîte aux lettres pour les boîtes aux lettres non chiffrées à l'aide de la cmdlet New-MoveRequest.

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a>Office 365: configuration de la clé client pour SharePoint Online et OneDrive entreprise
<a name="AzureSteps"> </a>

Avant de commencer, vérifiez que vous avez terminé les tâches requises pour configurer Azure Key Vault. Pour plus d'informations, consultez la rubrique [tâches terminées dans Azure Key Vault et Microsoft FastTrack pour la clé client](controlling-your-data-using-customer-key.md#AzureSteps) . 
  
Pour configurer la clé client pour SharePoint Online et OneDrive entreprise, vous devez effectuer ces étapes en vous connectant à distance à SharePoint Online avec Windows PowerShell.
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a>Créer une stratégie de chiffrement de données (DEP) pour chaque région de SharePoint Online et OneDrive entreprise
<a name="CreateDEP4SPOODfB"> </a>

Une DEP est associée à un ensemble de clés stockées dans Azure Key Vault. Vous appliquez une DEP à toutes vos données dans un emplacement géographique, également appelé géo. Si vous utilisez la fonctionnalité multigéographique d'Office 365 (actuellement en version d'évaluation), vous pouvez créer une DEP par zone géographique. Si vous n'utilisez pas de multi-géo, vous pouvez créer une DEP dans Office 365 pour une utilisation avec SharePoint Online et OneDrive entreprise. Office 365 utilisera ensuite les clés identifiées dans la DEP pour chiffrer vos données dans cette région. Pour créer la DEP, vous avez besoin des URI de coffre-fort que vous avez obtenus précédemment. Consultez [la rubrique obtenir l'URI pour chaque clé Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI) pour obtenir des instructions. 
  
Pensez! Lorsque vous créez une DEP, vous spécifiez deux clés qui résident dans deux coffres de clés Azure différents. Assurez-vous que ces clés se situent dans deux régions Azure distinctes pour garantir la redondance géographique.
  
Pour créer une DEP, vous devez vous connecter à distance à SharePoint Online à l'aide de Windows PowerShell.
  
1. Sur votre ordinateur local, à l'aide d'un compte professionnel ou scolaire disposant d'autorisations d'administrateur général dans votre organisation Office 365, [Connectez-vous à SharePoint Online PowerShell](https://technet.microsoft.com/library/fp161372.aspx).
    
2. Dans Microsoft SharePoint Online Management Shell, exécutez la cmdlet [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) comme suit: 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   Lorsque vous enregistrez la DEP, le chiffrement commence sur les données de la région géographique. Cela peut prendre un certain temps.
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a>Valider le chiffrement des sites de groupe, des sites d'équipe et de OneDrive entreprise
<a name="validateencryptionSPO"> </a>

Vous pouvez vérifier l'état du chiffrement en exécutant la cmdlet Get-SPODataEncryptionPolicy comme suit:
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

La sortie de cette cmdlet comprend les éléments suivants:
  
- URI de la clé primaire.
    
- URI de la clé secondaire.
    
- État de chiffrement de la zone géographique. Les États possibles sont les suivants:
    
  - Non **enregistré:** Le chiffrement de clé client n'a pas encore été appliqué. 
    
  - **Inscription:** Le chiffrement de clés client a été appliqué et vos fichiers sont en cours de chiffrement. Si votre région est dans cet État, vous verrez également des informations sur le pourcentage de sites dans la zone géographique, afin que vous puissiez surveiller la progression du chiffrement. 
    
  - **Inscrit:** Le chiffrement de clés client a été appliqué et tous les fichiers de tous les sites ont été chiffrés. 
    
  - **Roulement:** Un roulement de clé est en cours. Si votre région est dans cet État, vous verrez également des informations sur le pourcentage de sites ayant terminé l'opération de déploiement de clés afin que vous puissiez surveiller la progression. 
    
## <a name="managing-customer-key-for-office-365"></a>Gestion de la clé client pour Office 365
<a name="ManageCustomerKey"> </a>

Une fois que vous avez configuré la clé client pour Office 365, vous pouvez effectuer ces tâches de gestion supplémentaires.
  
- [Restaurer les clés Azure Key Vault](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [Laminage ou rotation d'une clé dans le coffre-fort de clés Azure que vous utilisez avec la clé client](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [Gérer les autorisations de coffre-fort](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [Déterminer la DEP affectée à une boîte aux lettres](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a>Restaurer les clés Azure Key Vault
<a name="RestoreAzureKeyVaultKeys"> </a>

Avant d'effectuer une restauration, utilisez les fonctionnalités de récupération fournies par la fonction de suppression récupérable. Toutes les clés utilisées avec la clé client doivent être activées pour la suppression logicielle. La suppression douce se comporte comme une corbeille et permet la récupération jusqu'à 90 jours sans nécessiter de restauration. La restauration doit être uniquement requise dans des circonstances extrêmes ou inhabituelles, par exemple en cas de perte de la clé ou du coffre-fort. Si vous devez restaurer une clé à utiliser avec la clé client, dans Azure PowerShell, exécutez la cmdlet reStore-AzureKeyVaultKey comme suit:
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

Par exemple :
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

S'il existe déjà une clé portant le même nom dans le coffre-fort de clés, l'opération de restauration échoue. ReStore-AzureKeyVaultKey restaure toutes les versions clés et toutes les métadonnées pour la clé, y compris le nom de la clé.
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a>Laminage ou rotation d'une clé dans le coffre-fort de clés Azure que vous utilisez avec la clé client
<a name="RollCKkey"> </a>

Les touches de roulement ne sont pas requises par le coffre-fort des clés Azure ou par la clé client. En outre, les clés protégées par un HSM sont quasiment impossibles à compromettre. Même si une clé racine était en possession d'un acteur malveillant, il n'est pas possible de l'utiliser pour déchiffrer les données, étant donné que seul le code Office 365 sait comment l'utiliser. Toutefois, le lancement d'une clé est pris en charge par la clé client.
  
> [!CAUTION]
> N'annulez une clé de chiffrement que vous utilisez avec la clé du client lorsqu'il existe une raison technique claire ou qu'une exigence de conformité exige que vous deviez annuler la clé. En outre, ne supprimez pas de clés qui sont ou n'ont pas été associées à des stratégies. Lorsque vous restaurez vos clés, le contenu est chiffré avec les clés précédentes. Par exemple, bien que les boîtes aux lettres actives soient rechiffrées fréquemment, les boîtes aux lettres inactives, déconnectées et désactivées peuvent toujours être chiffrées avec les clés précédentes. SharePoint Online effectue des sauvegardes de contenu à des fins de restauration et de récupération, de sorte qu'il peut toujours y avoir un archivage de contenu à l'aide de clés plus anciennes.<br/> Pour garantir la sécurité de vos données, SharePoint Online ne permet pas qu'une seule opération de roulier de clés soit en cours à la fois. Si vous souhaitez exécuter les deux clés dans un coffre-fort de clés, vous devez attendre que la première opération de la première clé soit entièrement terminée. Nous vous recommandons d'échelonner vos opérations de roulement de clé à différents intervalles, de sorte qu'il ne s'agit pas d'un problème. 
  
Lorsque vous annulez une touche, vous demandez une nouvelle version d'une clé existante. Pour demander une nouvelle version d'une clé existante, vous utilisez la même cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), avec la même syntaxe que celle que vous avez utilisée pour créer la clé.
  
Par exemple :
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

Dans cet exemple, étant donné qu'une clé nommée **contoso-O365EX-na-VaultA1-Key001** existe déjà dans la chambre forte de **contoso-O365EX-na-VaultA1** , une nouvelle version de clé sera créée. L'opération ajoute une nouvelle version de clé. Cette opération conserve les versions de clés précédentes dans l'historique des versions de la clé, afin que les données précédemment chiffrées avec cette clé puissent toujours être déchiffrées. Une fois que vous avez terminé le lancement de n'importe quelle clé associée à une DEP, vous devez exécuter une applet de commande supplémentaire pour vous assurer que la clé client commence à utiliser la nouvelle clé. 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Activer Exchange Online et Skype entreprise pour utiliser une nouvelle clé après avoir fait rouler ou pivoter des clés dans le coffre-fort des clés Azure

Lorsque vous effectuez l'une ou l'autre des clés Azure Key Vault associées à une DEP utilisée avec Exchange Online et Skype entreprise, vous devez exécuter la commande suivante pour mettre à jour la DEP et activer Office 365 pour qu'il démarre à l'aide de la nouvelle clé.
  
Pour indiquer à la clé du client d'utiliser la nouvelle clé pour chiffrer les boîtes aux lettres dans Office 365 exécutez la cmdlet Set-DataEncryptionPolicy comme suit:
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

Dans les 48 heures, les boîtes aux lettres actives chiffrées à l'aide de cette stratégie sont associées à la clé mise à jour. Suivez les étapes décrites dans la procédure [déterminer la DEP attribuée à une boîte aux lettres](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) pour vérifier la valeur de la propriété DataEncryptionPolicyID de la boîte aux lettres. La valeur de cette propriété change une fois que la clé mise à jour a été appliquée. 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Activer SharePoint Online et OneDrive entreprise pour utiliser une nouvelle clé après avoir fait rouler ou pivoter des clés dans le coffre-fort des clés Azure

Lorsque vous effectuez l'une des clés Azure Key Vault associées à une DEP utilisée avec SharePoint Online et OneDrive entreprise, vous devez exécuter la cmdlet [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) pour mettre à jour la DEP et activer Office 365 pour qu'il commence à utiliser la nouvelle clé. 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

Cela démarrera l'opération de déploiement de clés pour SharePoint Online et OneDrive entreprise. Cette action n'est pas immédiate. Pour voir la progression de l'opération de la séquence de touches, exécutez la cmdlet Get-SPODataEncryptionPolicy comme suit:
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a>Gérer les autorisations de coffre-fort
<a name="Managekeyvaultperms"> </a>

Plusieurs cmdlets sont disponibles, qui vous permettent d'afficher et, si nécessaire, de supprimer des autorisations de coffre-fort clé. Vous devrez peut-être supprimer des autorisations, par exemple, lorsqu'un employé quitte l'équipe.
  
Pour afficher les autorisations de coffre-fort, exécutez la cmdlet Get-AzureRmKeyVault:
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

Par exemple :
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

Pour supprimer les autorisations d'un administrateur, exécutez l'applet de commande Remove-AzureRmKeyVaultAccessPolicy:
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

Par exemple :
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a>Déterminer la DEP affectée à une boîte aux lettres
<a name="DeterminemailboxDEP"> </a>

Pour déterminer la DEP affectée à une boîte aux lettres, utilisez la cmdlet Get-MailboxStatistics. L'applet de commande renvoie un identificateur unique (GUID).
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres. Pour plus d'informations sur la cmdlet Get-MailboxStatistics, consultez la rubrique [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).
  
Utilisez le GUID pour connaître le nom convivial de la DEP à laquelle la boîte aux lettres est affectée en exécutant l'applet de commande suivante.
  
```
Get-DataEncryptionPolicy <GUID>
```

Où *GUID* est le GUID renvoyé par la cmdlet Get-MailboxStatistics à l'étape précédente. 
  

