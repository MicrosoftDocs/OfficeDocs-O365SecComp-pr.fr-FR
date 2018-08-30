---
title: Contrôle de vos données dans Office 365 à l’aide de la clé de client
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: Découvrez comment configurer la clé client pour Office 365 pour Exchange Online, Skype pour les entreprises, SharePoint Online et OneDrive for Business. Avec la clé client, vous contrôler les clés de chiffrement de votre organisation, puis configurez Office 365 pour les utiliser pour chiffrer vos données au repos dans les centres de données de Microsoft.
ms.openlocfilehash: f8d7c12c32ca74b842f676f4a2ccde4d1c758361
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559229"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a>Contrôle de vos données dans Office 365 à l’aide de la clé de client

Avec la clé client, vous contrôler les clés de chiffrement de votre organisation, puis configurez Office 365 pour les utiliser pour chiffrer vos données au repos dans les centres de données de Microsoft. Données au repos comprennent des données à partir d’Exchange Online et Skype pour les entreprises qui est stocké dans les boîtes aux lettres et les fichiers qui sont stockés dans SharePoint Online et OneDrive for Business.
  
Vous devez configurer Azure avant de pouvoir utiliser la clé client pour Office 365. Cette rubrique décrit les étapes à suivre pour créer et configurer les ressources requises Azure et puis fournit les étapes de configuration de la clé client dans Office 365. Après avoir terminé le programme d’installation Azure, vous déterminez la stratégie et par conséquent, les clés, à affecter aux boîtes aux lettres et des fichiers dans votre organisation. Boîtes aux lettres et fichiers pour lesquels vous n’affecter une stratégie utiliseront les stratégies de chiffrement qui sont contrôlés et gérés par Microsoft. Pour plus d’informations sur la clé client, ou pour une vue d’ensemble, voir la [Clé client pour Office 365 FAQ](service-encryption-with-customer-key-faq.md).
  
> [!IMPORTANT]
> Il est vivement recommandé de suivre les meilleures pratiques dans cette rubrique. Il s’agit **Conseil** et **IMPORTANT**. Client clé vous permet de contrôler les clés de chiffrement racine dont la portée peut être aussi grand que la totalité de votre organisation. Cela signifie que commises avec ces touches peuvent avoir un impact large et risque de provoquer des interruptions de service ou la perte irrévocable de vos données. 
  
## <a name="before-you-begin-setting-up-customer-key"></a>Avant de commencer la configuration de la clé client
<a name="Beforeyoustart"> </a>

Avant de commencer, assurez-vous que la gestion des licences approprié pour votre organisation. Clé de client dans Office 365 est proposée dans Office 365 E5 ou la référence de conformité avancées.
  
Ensuite, pour comprendre les concepts et les procédures décrites dans cette rubrique, vous devez examiner la documentation [Azure clé coffre-fort](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . En outre, vous familiariser avec les termes utilisés dans Azure, par exemple, le [client](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).
  
Pour fournir des commentaires sur la clé client, y compris la documentation, envoyez vos idées et suggestions perspectives à customerkeyfeedback@microsoft.com.
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a>Vue d’ensemble de la configuration de la clé client pour Office 365
<a name="Overview"> </a>

Pour configurer la clé client, vous allez effectuer ces tâches. Le reste de cette rubrique fournit des instructions détaillées pour chaque tâche, ou à des liens vers des plus d’informations pour chaque étape du processus.
  
**Dans Azure et FastTrack Microsoft :**
  
Vous allez exécuter la plupart de ces tâches en vous connectant à distance PowerShell Azure. Pour obtenir les meilleurs résultats, utilisez version 4.4.0 ou ultérieure de Windows Azure PowerShell.
  
- [Créer deux nouveaux abonnements Azure](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [Enregistrer des abonnements Azure pour utiliser une période de rétention obligatoire](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    L’inscription peut prendre entre un et cinq jours ouvrés.
    
- [Pour soumettre une demande pour activer la clé client pour Office 365](controlling-your-data-using-customer-key.md#FastTrack)
    
    Une fois que vous avez créé les deux nouveaux abonnements Azure, vous devez envoyer la demande d’offre de clé de client appropriée en effectuant un formulaire web qui est hébergé dans le portail Microsoft FastTrack. L’équipe FastTrack ne fournit pas d’assistance avec la clé client. Office utilise simplement le portail FastTrack pour vous permettre d’envoyer le formulaire et pour suivre les offres pertinentes pour la clé client.
  
Une fois que vous avez soumis une offre de la clé client, Microsoft passe en revue votre demande et vous avertit que vous pouvez passer avec les autres tâches de configuration. Ce processus peut prendre jusqu'à cinq jours ouvrés.
    
- [Créer un coffre-fort de clé Azure premium dans chaque abonnement](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [Attribuer des autorisations à chaque clé coffre-fort](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [Activer et Confirmer suppression réversible sur votre chambres fortes clés](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [Ajoutez une clé pour chaque clé coffre-fort soit par la création ou l’importation d’une clé](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [Vérifier le niveau de restauration de vos clés](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [Sauvegarde coffre-fort clé Azure](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [Valider les paramètres de configuration Azure clé coffre-fort](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [Obtenir l’URI pour chaque clé Azure clé coffre-fort](controlling-your-data-using-customer-key.md#GetKeyURI)
    
**Dans Office 365 :**
  
Exchange Online et Skype pour les entreprises :
  
- [Créer une stratégie de chiffrement des données (PED) pour une utilisation avec Exchange Online et Skype pour les entreprises](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [Affecter un PED à une boîte aux lettres](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [Valider le chiffrement de la boîte aux lettres](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
SharePoint Online et OneDrive entreprise :
  
- [Créer une stratégie de chiffrement des données (PED) pour chaque OneDrive et SharePoint Online pour entreprise geo](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [Valider le chiffrement du groupe de Sites, Sites d’équipe et OneDrive entreprise](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a>Effectuer des tâches dans Azure clé coffre-fort et FastTrack Microsoft pour la clé client
<a name="AzureSteps"> </a>

Effectuer ces tâches dans Azure clé coffre-fort afin de configurer la clé client pour Office 365. Vous devez effectuer ces étapes que vous envisagez de configurer la clé client pour Exchange Online et Skype pour Business ou SharePoint Online et OneDrive for Business ou pour tous les services pris en charge dans Office 365.
  
### <a name="create-two-new-azure-subscriptions"></a>Créer deux nouveaux abonnements Azure
<a name="Create2newsubs"> </a>

Deux abonnements Azure sont requis pour la clé client. Meilleure pratique, Microsoft recommande que vous créez des nouveaux abonnements Azure pour une utilisation avec la clé client. Clés de clé coffre-fort Azure ne peuvent être autorisées pour les applications dans le même client Azure Active Directory (DAS), vous devez créer les nouveaux abonnements à l’aide du même client Azure AD utilisé avec votre organisation Office 365 dans lequel le Dép. sera attribué. Par exemple, à l’aide de votre compte professionnel ou de l’école ayant des privilèges d’administrateur global dans votre organisation Office 365. Pour obtenir la procédure détaillée, voir [s’inscrire pour Azure comme une organisation](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).
  
> [!IMPORTANT]
> Clé de client nécessite deux clés pour chaque stratégie de chiffrement des données (PED). Pour ce faire, vous devez créer deux abonnements Azure. Microsoft recommande d’ont distinct des membres de votre organisation pour configurer une clé dans chaque abonnement. En outre, ces abonnements Azure doivent uniquement être utilisés pour administrer les clés de chiffrement pour Office 365. Il protège votre organisation en cas d’un de vos opérateurs intentionnellement accidentelle ou intentionnelle supprime ou dans le cas contraire mismanages les clés pour lesquels ils sont chargés.<br/> Nous vous recommandons de configurer les nouveaux abonnements Azure qui sont uniquement utilisés pour la gestion des ressources Azure clé coffre-fort pour une utilisation avec la clé client. Il n’existe aucune limite au nombre d’abonnements Azure que vous pouvez créer pour votre organisation. Suivant ces meilleures pratiques réduit l’impact d’une erreur humaine tout en aidant à gérer les ressources utilisées par la clé client. 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a>Pour soumettre une demande pour activer la clé client pour Office 365
<a name="FastTrack"> </a>

Une fois que vous avez terminé les étapes Azure, vous devez soumettre une demande offre dans le [portail Microsoft FastTrack](https://fasttrack.microsoft.com/). Une fois que vous avez soumis une demande via le portail web FastTrack, Microsoft vérifie les informations de contact et les données de configuration Azure clé coffre-fort que vous avez fournis. Les sélections effectuées dans l’écran offre concernant les agents autorisés de votre organisation est nécessaire pour la fin de l’enregistrement de clé de client et critique. Les agents de votre organisation que vous sélectionnez dans le formulaire sera utilisé pour assurer l’authenticité de toute demande de révoquer et détruire toutes les clés utilisées avec une règle de chiffrement des données de clé de client. Vous devez effectuer cette étape une fois pour activer la clé client pour Exchange Online et Skype pour la couverture d’entreprise et une deuxième fois activer la clé client pour SharePoint Online et OneDrive for Business.
  
Pour soumettre une offre pour activer la clé client, procédez comme suit :
  
1. À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, connectez-vous au [portail Microsoft FastTrack](https://fasttrack.microsoft.com/).
    
2. Une fois que vous êtes connecté dans, accédez au **tableau de bord**.
    
3. Choisissez **offre**, puis passez en revue la liste des offres en cours.
    
4. Choisissez **En savoir plus** pour l’offre s’applique à vous : 
    
  - **Exchange Online et Skype pour les entreprises :** Choisissez **En savoir plus** sur l’offre de **Clé de client pour Exchange** . 
    
  - **SharePoint Online et OneDrive for Business :** Choisissez **En savoir plus** sur la **Clé de client pour SharePoint et OneDrive entreprise** offre. 
    
5. Dans la page **Détails de l’offre** , choisissez **Créer une demande**.
    
6. Remplissez tous les détails applicables et les informations demandées dans le formulaire offre. Une attention particulière à vos sélections pour les responsables de votre organisation que vous voulez autoriser à approuver la destruction définitive et irréversible de clés de chiffrement et de données. Une fois que vous avez terminé le formulaire, cliquez sur **Envoyer**.
    
    Ce processus peut prendre jusqu'à cinq jours ouvrés une fois que Microsoft a été averti de votre demande.
    
7. Passez à la section de période de rétention obligatoire ci-dessous.
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a>Enregistrer des abonnements Azure pour utiliser une période de rétention obligatoire
<a name="RegisterSubsforMRP"> </a>

La perte temporaire ou permanente racine des clés de chiffrement peut être très gênants ou même des catastrophes à l’opération de service et peut entraîner une perte de données. Pour cette raison, les ressources utilisées avec la clé client nécessitent une protection renforcée. Toutes les ressources Azure qui sont utilisés avec la clé client offrent des mécanismes de protection au-delà de la configuration par défaut. Abonnements Azure peuvent être marqués ou enregistrés d’une manière qui empêche l’annulation de l’exécution et irrévocable. Il est appelé inscription pour une période de rétention obligatoire. Les étapes nécessaires à l’enregistrement des abonnements Azure pour une période de rétention obligatoire requièrent la collaboration avec l’équipe Office 365. Ce processus peut prendre entre un et cinq jours ouvrés. Auparavant, il a été parfois appelé « Ne pas annuler ».
  
Avant de contacter l’équipe Office 365, vous devez effectuer les étapes suivantes pour chaque abonnement Azure que vous utilisez avec la clé client :
  
1. Connectez-vous à votre abonnement Azure avec Azure PowerShell. Pour plus d’informations, voir [Connectez-vous avec Windows Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
2. Exécutez l’applet de commande Register-AzureRmProviderFeature pour enregistrer vos abonnements pour utiliser une période de rétention obligatoire.
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. Contacter Microsoft pour que le processus de finalisation. Pour SharePoint et OneDrive équipe commerciale, contactez [spock@microsoft.com](mailto:spock@microsoft.com). Pour Exchange Online et Skype pour les entreprises, contactez [exock@microsoft.com](mailto:exock@microsoft.com). Le contrat de niveau de Service (SLA) pour la fin de ce processus est cinq jours ouvrés une fois que Microsoft a été averti (et vérifié) que vous avez enregistré vos abonnements pour utiliser une période de rétention obligatoire. Inclure les éléments suivants dans votre courrier électronique :
    
    **Objet**: clé de client pour \< *au nom de domaine complet de votre client*\> 
    
    **Corps**: ID d’abonnement pour laquelle vous voulez permettre la rétention obligatoire période finalisée. 
    
4. Une fois que vous recevez une notification à partir de Microsoft que l’inscription est terminée, vérifiez l’état de l’enregistrement en exécutant l’applet de commande Get-AzureRmProviderFeature comme suit :
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. Après avoir vérifié que la propriété **State de l’inscription** de l’applet de commande Get-AzureRmProviderFeature renvoie la valeur **Registered**, exécutez la commande suivante pour terminer le processus :
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a>Créer un coffre-fort de clé Azure premium dans chaque abonnement
<a name="CreateKeyVault"> </a>

Les étapes pour créer un coffre-fort clé sont documentées dans la [Mise en route avec Azure clé coffre-fort](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), qui vous guide à travers l’installation et lancement d’Azure PowerShell, connexion à votre abonnement Azure, création d’un groupe de ressources et création d’un coffre-fort clé qui groupe de ressources.
  
Lorsque vous créez un coffre-fort clé, vous devez choisir une référence SKU : Standard ou Premium. La référence Standard permet clés Azure clé coffre-fort d’être protégé avec le logiciel - il n’existe aucune protection clés du Module de sécurité matériel (HSM) - et la version Premium permet d’utiliser HSM pour la protection des clés de la clé coffre-fort. Clé de client accepte chambres fortes clés qui utilisent soit SKU, bien que Microsoft recommande vivement que vous utilisez uniquement la version Premium. Le coût des opérations avec des clés de des types est la même, la seule différence de coût est le coût par mois pour chaque clé HSM protégé. Pour plus d’informations, voir [clé coffre-fort prix](https://azure.microsoft.com/pricing/details/key-vault/) . 
  
> [!IMPORTANT]
> Utilisez les clés protégés par HSM chambres fortes clés SKU Premium pour les données de production et uniquement chambres fortes clés SKU Standard et les clés à des fins de test et de validation. 
  
Pour chaque service Office 365 avec lequel vous allez utiliser la clé client, créez un coffre-fort clé dans chaque abonnement Azure deux que vous avez créé. Par exemple, pour Exchange Online et Skype pour les professionnels uniquement ou SharePoint Online et OneDrive entreprise uniquement, vous allez créer uniquement une paire de chambres fortes. Pour activer la clé client pour Exchange Online et SharePoint Online, vous allez créer deux paires de clés chambres fortes.
  
Utilisez une convention d’affectation de noms pour chambres fortes clés qui reflète l’utilisation prévue de la prévention avec lequel vous allez associer les chambres fortes. Voir la section méthodes conseillées ci-dessous pour les recommandations de la convention d’affectation de noms.
  
Créer un ensemble distinct et paire de chambres fortes pour chaque stratégie de chiffrement des données. Pour Exchange Online, l’étendue d’une stratégie de chiffrement des données est choisi par vous lorsque vous attribuez la stratégie de boîte aux lettres. Une boîte aux lettres peut avoir qu’une seule stratégie attribuée, et vous pouvez créer des stratégies à cinquante. Pour SharePoint Online l’étendue d’une stratégie est toutes les données au sein d’une organisation dans un emplacement géographique ou localisés.
  
La création d’une clé chambres fortes requiert également la création de groupes de ressources Azure, puisqu’il chambres fortes clés besoin de capacité de stockage (bien que très petite) coffre-fort clé journalisation, si activé, génère des données stockées. En règle générale Microsoft recommande l’utilisation de distincts pour les administrateurs à gérer chaque groupe de ressources, avec l’administration alignée sur l’ensemble des administrateurs de gérer toutes les ressources associées de clé de client.
  
> [!IMPORTANT]
> Pour optimiser la disponibilité, votre chambres fortes clés doivent être dans les zones près votre service Office 365. Par exemple, si votre organisation Exchange Online est en Amérique du Nord, placez votre chambres fortes clés en Amérique du Nord. Si votre organisation Exchange Online est Europe, placez votre chambres fortes clés en Europe.<br/>Utiliser un préfixe commun pour chambres fortes clés et inclure une abréviation de l’utilisation et l’étendue de la clé coffre-fort et les clés (par exemple, pour le service de Contoso SharePoint où se trouvera le chambres fortes en Amérique du Nord, une paire de noms possible est Contoso-O365SP-NA-VaultA1 et Contoso-O365SP-NA-VaultA2. Noms de coffre-fort sont des chaînes global uniques dans Azure, vous serez peut-être amené à essayer les variantes de vos noms de votre choix au cas où les noms de votre choix sont déjà réclamés par d’autres clients Azure. À compter de juillet 2017 noms coffre-fort ne peut pas être modifiés pour une meilleure pratique consiste à disposer d’un plan écrit pour le programme d’installation et d’utiliser une deuxième personne pour vérifier que le plan est exécuté correctement.<br/>Si possible, créez votre chambres fortes dans les zones non couplé. Paire de régions Azure fournissent une haute disponibilité sur plusieurs domaines d’échec de service. Par conséquent, paires régionaux peuvent être considérés comme l’autre région sauvegarde. Cela signifie qu’une ressource Azure qui est placée dans une région gagne automatiquement la tolérance de panne par le biais de la région associée. Pour cette raison, choix des régions pour deux chambres fortes utilisés dans un PED où les zones sont couplés signifie qu’uniquement un total de deux régions de disponibilité sont en cours d’utilisation. La plupart des régions ont seulement deux régions, afin qu’il n’est pas encore possible de sélectionner des régions non couplé. Dans la mesure du possible, choisissez deux régions non couplé pour les deux chambres fortes utilisés avec une prévention Il bénéficie d’un total de quatre zones de disponibilité. Pour plus d’informations, voir [Business continuité d’activité et récupération d’urgence (BCDR) : Azure couplé régions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) pour une liste de paires régionaux en cours. 
  
### <a name="assign-permissions-to-each-key-vault"></a>Attribuer des autorisations à chaque clé coffre-fort
<a name="KeyVaultPerms"> </a>

Pour chaque clé coffre-fort, vous devez définir trois ensembles distincts d’autorisations pour la clé client, en fonction de votre implémentation. Par exemple, vous devez définir un ensemble d’autorisations pour les éléments suivants :
  
- **Les administrateurs de coffre-fort clé** qui exécutera la gestion quotidienne de votre coffre-fort clé pour votre organisation. Ces tâches incluent la sauvegarde, créer, obtient, importer, répertorier et restaurer. 
    
    > [!IMPORTANT]
    > Le jeu d’autorisations affecté aux administrateurs de coffre-fort clés n’inclut pas l’autorisation de supprimer des clés. Il s’agit intentionnelle et essentiel. Suppression des clés de chiffrement est généralement pas effectuée, dans la mesure où effectuant donc définitivement détruit les données. Meilleure pratique, n’accordez pas cette autorisation aux administrateurs de coffre-fort clés par défaut. Au lieu de cela, cette réserve pour les collaborateurs clés coffre-fort et uniquement l’attribuer à un administrateur de manière à court terme une fois une bonne compréhension des conséquences est comprise. 
  
    Pour affecter ces autorisations à un utilisateur dans votre organisation Office 365, connectez-vous à votre abonnement Azure avec Azure PowerShell. Pour plus d’informations, voir [Connectez-vous avec Windows Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).
    
- Exécutez l’applet de commande Set-AzureRmKeyVaultAccessPolicy pour attribuer les autorisations nécessaires.
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  Par exemple :
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- **Les collaborateurs coffre-fort clé** qui peut modifier les autorisations sur le coffre-fort clé Azure lui-même. Vous devrez modifier ces autorisations, comme les employés quittent ou rejoignent de votre équipe, ou dans le cas très rare que la clé vault administrateurs légitimement doivent autorisé à supprimer ou restaurer une clé. Cet ensemble de clés coffre-fort collaborateurs doit bénéficier du rôle de **collaborateur** sur votre clé coffre-fort. Vous pouvez attribuer ce rôle à l’aide du Gestionnaire de ressources Azure. Pour obtenir la procédure détaillée, voir [Contrôle d’accès Use Role-Based pour gérer l’accès aux ressources de votre abonnement Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). L’administrateur qui crée un abonnement a cet accès implicitement, ainsi que la possibilité d’affecter les autres administrateurs au rôle de collaborateur.
    
- Si vous envisagez d’utiliser la clé client avec Exchange Online et Skype pour les entreprises, vous devez octroyer une autorisation à Office 365 utilisent la clé coffre-fort part Exchange Online et Skype pour les entreprises. De même, si vous envisagez d’utiliser la clé client avec SharePoint Online et OneDrive entreprise, vous devez ajouter l’autorisation pour Office 365 utiliser la clé coffre-fort part SharePoint Online et OneDrive for Business. Pour accorder l’autorisation à Office 365, exécutez l’applet de commande **Set-AzureRmKeyVaultAccessPolicy** à l’aide de la syntaxe suivante : 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    Où :
    
  - *vaultname* est le nom de la clé coffre-fort que vous avez créé. 
    
  - Pour Exchange Online et Skype pour les entreprises, remplacez *appID Office 365* avec`00000002-0000-0ff1-ce00-000000000000`
    
  - Pour SharePoint Online et OneDrive entreprise, remplacez *appID Office 365* avec`00000003-0000-0ff1-ce00-000000000000`
    
  Exemple : Définition des autorisations pour Exchange Online et Skype pour les entreprises :
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  Exemple : Définition des autorisations pour SharePoint Online et OneDrive entreprise
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a>Activer et Confirmer suppression réversible sur votre chambres fortes clés
<a name="SoftDelete"> </a>

Lorsque vous pouvez récupérer rapidement vos clés, vous sont moins susceptibles de rencontrer une panne de l’étendue de service en raison de clés accidentelle ou intentionnelle supprimées. Vous devez activer cette configuration, appelée suppression logicielle, avant de pouvoir utiliser vos clés avec la clé client. Activation supprimer souple vous permet de récupérer des clés ou des chambres fortes au sein de la suppression de 90 jours sans avoir à les restaurer à partir de la sauvegarde.
  
Pour activer l’option Supprimer logicielle sur votre chambres fortes clés, procédez comme suit :
  
1. Connectez-vous à votre abonnement Azure avec Windows Powershell. Pour plus d’informations, voir [Connectez-vous avec Windows Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).
    
2. Exécutez l’applet de commande [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . Dans cet exemple, *vaultname* est le nom de la clé coffre-fort pour lequel vous activez suppression réversible : 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. Confirmer la suppression réversible est configurée pour le coffre-fort clé en exécutant l’applet de commande **Get-AzureRmKeyVault** . Si la suppression réversible est correctement configurée pour la clé coffre-fort, le logiciel supprimer activé ? propriété renvoie la valeur **True**: 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a>Ajoutez une clé pour chaque clé coffre-fort soit par la création ou l’importation d’une clé
<a name="AddKeystoKeyVault"> </a>

Il existe deux façons d’ajouter des clés à un coffre-fort clé Azure ; Vous pouvez créer une clé directement dans la clé de coffre-fort, ou vous pouvez importer une clé. Création d’une clé directement dans la clé de coffre-fort est la méthode moins compliquée, alors que l’importation d’une clé offre un contrôle total sur la façon dont la clé est générée.
  
Pour créer une clé directement dans votre clé coffre-fort, exécutez l’applet de commande [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) comme suit : 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

Où :
  
-  *vaultname* est le nom de la clé coffre-fort dans lequel vous souhaitez créer la clé. 
    
-  *nom* est le nom que vous souhaitez attribuer à la nouvelle clé. 
    
    > [!TIP]
    > Nom de clés à l’aide d’une convention d’affectation de noms similaire comme décrit ci-dessus pour chambres fortes clés. Ainsi, dans les outils qui affichent uniquement le nom de clé, la chaîne est libre décrivant. 
  
- Si vous envisagez de protéger la clé avec un module HSM, assurez-vous que vous spécifiez **HSM** comme valeur du paramètre _Destination_ , spécifiez dans le cas contraire, les **logiciels**.
    
Par exemple,
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

Pour importer une clé directement dans votre coffre-fort clé, vous devez avoir un Module de sécurité matériel de nShield Thales.
  
Certaines organisations préfèrent cette approche pour établir la provenance de leurs clés et cette méthode offre également les éléments suivants :
  
- L’ensemble d’outils utilisé pour l’importation inclut attestation de Thales que la clé d’Exchange clé (KEK) qui est utilisé pour crypter la clé que vous générez n’est pas exportable et est généré à l’intérieur d’un module HSM authentique qui a été fabriqué par Thales.
    
- L’ensemble d’outils inclut attestation de Thales que le monde de la sécurité Azure clé coffre-fort a également été généré sur un véritable HSM fabriqué par Thales. Cette attestation est donc vous que Microsoft utilise également authentique matériel Thales.
    
Renseignez-vous auprès de votre groupe de sécurité pour déterminer si les attestations ci-dessus sont nécessaires. Pour connaître les étapes détaillées créer une clé locale et l’importer dans votre coffre-fort clé, voir [comment générer et transférer les clés protégés par HSM pour Azure clé coffre-fort](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Utilisez les instructions Azure pour créer une clé dans chaque clé coffre-fort.
  
### <a name="check-the-recovery-level-of-your-keys"></a>Vérifier le niveau de restauration de vos clés
<a name="CheckKeyRecoveryLevel"> </a>

Office 365 nécessite que l’abonnement Azure clé coffre-fort est défini sur ne pas annuler et que les touches utilisées par la clé client ont suppression réversible activée. Vous pouvez le vérifier en regardant le niveau de restauration sur vos clés.
  
Pour vérifier le niveau de restauration d’une clé, dans Windows Azure PowerShell, exécutez l’applet de commande Get-AzureKeyVaultKey comme suit :
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

Si la propriété de _Niveau de restauration_ renvoie rien d’autre que la valeur **Récupérable + ProtectedSubscription**, vous devrez consulter cette rubrique et vous assurer que vous avez suivi toutes les étapes pour placer la liste ne pas annuler l’abonnement et que vous avez activée sur chacun de vos chambres fortes clés de suppression réversible.
  
### <a name="backup-azure-key-vault"></a>Sauvegarde coffre-fort clé Azure
<a name="BackupAzureKeyVaultkeys"> </a>

Immédiatement après la création ou toute modification apportée à une clé, effectuez une sauvegarde et de stocker des copies de la sauvegarde, en ligne et hors connexion. Copies hors connexion ne doivent pas connectés à un réseau, tels que dans un emplacement de stockage physique sans échec ou commerciale. Au moins une copie de la sauvegarde doit être stockée dans un emplacement accessible en cas d’incident. Les objets BLOB sauvegarde sont le seul moyen de la restauration de clé une clé clé coffre-fort doit être définitivement supprimée ou sinon rendue inutilisable. Clés qui sont externes à Azure clé coffre-fort et ont été importés à Azure clé coffre-fort ne constituent pas une sauvegarde car les métadonnées nécessaires pour la clé client d’utiliser la clé n’existent pas avec la clé externe. Uniquement une sauvegarde effectuée à partir d’Azure clé coffre-fort utilisable pour les opérations de restauration avec la clé client. Par conséquent, il est essentiel qu’une sauvegarde de Azure clé coffre-fort être effectuée une fois qu’une clé est téléchargée ou créée.
  
Pour créer une sauvegarde d’une clé Azure clé coffre-fort, exécutez l’applet de commande [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) comme suit :
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

Assurez-vous que votre fichier de sortie utilise le suffixe `.backup`.
  
Le fichier de sortie résultant de cette applet de commande est chiffré et ne peut pas être utilisé en dehors d’Azure clé coffre-fort. La sauvegarde peut être restaurée uniquement à l’abonnement Azure à partir de laquelle la sauvegarde a été effectuée.
  
> [!TIP]
> Le fichier de sortie, choisissez une combinaison de votre nom de coffre-fort et le nom de la clé. Cela permettra le nom de fichier décrivant automatique. Il permet également de garantir que les noms de fichier de sauvegarde n’entrent pas en conflit. 
  
Par exemple :
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a>Valider les paramètres de configuration Azure clé coffre-fort
<a name="Validateconfiguration"> </a>

Exécution de la validation avant d’utiliser des clés dans une PED est facultative mais fortement recommandée. En particulier, si vous utilisez des étapes pour configurer vos clés et chambres fortes autres que celles décrites dans cette rubrique, vous devez valider l’intégrité de vos ressources Azure clé coffre-fort avant de configurer la clé client.
  
Pour vérifier que vos clés ont des opérations get, wrapKey et unwrapKey activées :
  
Exécutez l’applet de commande [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) comme suit : 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

Dans la sortie, rechercher la stratégie d’accès et l’identité (GUID) Exchange Online ou l’identité SharePoint Online (GUID) comme il convient. Les trois les autorisations doivent être indiqués sous autorisations aux clés.
  
Si la configuration de stratégie d’accès est incorrecte, exécutez l’applet de commande Set-AzureRmKeyVaultAccessPolicy comme suit :
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

Par exemple, pour Exchange Online et Skype pour les entreprises :
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

Par exemple, pour SharePoint Online et OneDrive entreprise :
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

Pour vérifier que la date d’expiration n’est pas définie pour les clés, exécutez l’applet de commande [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) comme suit : 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

Une clé arrivés à expiration ne peut pas être utilisée par la clé client et tentées avec une clé arrivés à expiration des opérations échoue et éventuellement entraîner une interruption de service. Il est vivement recommandé que les clés utilisées avec la clé client n’ont pas une date d’expiration. Une date d’expiration, une fois que set, ne peut pas être supprimée, mais peut être modifiée à une date différente. Si une clé ayant une date d’expiration de la valeur doit être utilisée, modifiez la valeur d’expiration au 12/31/9999. Touches avec une date d’expiration définie sur une date différente de 12/31/9999 ne passera pas la validation d’Office 365.
  
Pour modifier une date d’expiration qui a une valeur autre que 12/31/9999, exécutez l’applet de commande [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) comme suit : 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> Ne définissez pas de clés de chiffrement que vous utilisez avec la clé client dates d’expiration. 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a>Obtenir l’URI pour chaque clé Azure clé coffre-fort
<a name="GetKeyURI"> </a>

Une fois que vous avez effectué toutes les étapes dans Azure pour configurer votre chambres fortes clés et ajouter vos clés, exécutez la commande suivante pour obtenir l’URI de la clé dans chaque clé coffre-fort. Vous devrez utiliser ces URI lorsque vous créez et affectez chaque PED ultérieurement, enregistre ces informations dans un endroit sûr. N’oubliez pas d’exécuter cette commande une fois pour chaque clé coffre-fort.
  
Dans Azure PowerShell :
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a>Office 365 : Configuration de la clé client pour Exchange Online et Skype pour les entreprises
<a name="AzureSteps"> </a>

Avant de commencer, assurez-vous que vous avez effectué les tâches requises pour configurer Azure clé coffre-fort. Pour plus d’informations, voir [effectuer des tâches dans Azure clé coffre-fort et FastTrack Microsoft pour la clé client](controlling-your-data-using-customer-key.md#AzureSteps) . 
  
Pour configurer la clé client pour Exchange Online et Skype pour les entreprises, vous devez effectuer ces étapes en vous connectant à distance à Exchange Online avec Windows PowerShell.
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a>Créer une stratégie de chiffrement des données (PED) pour une utilisation avec Exchange Online et Skype pour les entreprises
<a name="CreateDEP4EXOSkype"> </a>

Un PED est associé à un ensemble de clés stockées dans Azure clé coffre-fort. Vous assignez un PED à une boîte aux lettres dans Office 365. Office 365 utilise les clés identifiés dans la stratégie pour crypter la boîte aux lettres. Pour créer la prévention, vous devez les URI de coffre-fort clé que vous avez obtenu précédemment. Pour obtenir des instructions, consultez la rubrique [obtenir l’URI pour chaque clé Azure clé coffre-fort](controlling-your-data-using-customer-key.md#GetKeyURI) . 
  
N’oubliez pas ! Lorsque vous créez un PED, vous spécifiez deux clés qui se trouvent dans deux différentes chambres fortes de clé Azure. Assurez-vous que ces clés sont trouvent dans deux régions Azure distinctes pour assurer la redondance géographique.
  
Pour créer la prévention, procédez comme suit :
  
1. Sur votre ordinateur local, avec un compte professionnel ou de l’école dispose des autorisations d’administrateur global dans votre organisation Office 365, [se connecter à Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) en ouvrant Windows PowerShell et en exécutant la commande suivante. 
    
   ```
   $UserCredential = Get-Credential
   ```

2. Dans la boîte de dialogue demande d’informations d’identification Windows PowerShell, entrez votre travail ou établissement des informations de compte et cliquez sur **OK**, puis entrez la commande suivante. 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. Exécutez la commande suivante.
    
   ```
   Import-PSSession $Session
   ```

4. Pour créer un PED, utilisez l’applet de commande New-DataEncryptionPolicy en tapant la commande suivante.
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   Où :
    
   -  *PolicyName* est le nom que vous souhaitez utiliser pour la stratégie. Les noms ne peuvent pas contenir d’espaces. Par exemple, USA_mailboxes. 
    
   -  *PolicyDescription* est une description conviviale de la stratégie qui permet de mémoriser est la stratégie pour. Vous pouvez inclure des espaces dans la description. Par exemple, racine clé pour les boîtes aux lettres des États-Unis et ses territoires. 
    
   -  *KeyVaultURI1* est l’URI de la première clé dans la stratégie. Par exemple, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01. 
    
   -  *KeyVaultURI2* est l’URI de la deuxième clé dans la stratégie. Par exemple, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Séparez les deux URI par une virgule et un espace. 
    
   Exemple :
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a>Affecter un PED à une boîte aux lettres
<a name="assignDEPtomailbox"> </a>

Affecter la prévention à une boîte aux lettres à l’aide de l’applet de commande Set-Mailbox. Une fois que vous assignez à la stratégie, Office 365 peut chiffrer la boîte aux lettres avec la clé indiquée dans la prévention
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

Où *MailboxIdParameter* spécifie une boîte aux lettres. Pour plus d’informations sur la cmdlet Set-Mailbox, voir [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).
  
### <a name="validate-mailbox-encryption"></a>Valider le chiffrement de la boîte aux lettres
<a name="validatemailboxencryption"> </a>

Chiffrer une boîte aux lettres peut prendre un certain temps. Pour l’affectation de stratégie première fois, la boîte aux lettres doit également effectuer le déplacement d’une base de données vers un autre avant que le service peut crypter la boîte aux lettres. Nous vous conseillons d’attendre 72 heures avant de valider le chiffrement une fois que vous modifiez un PED ou la première fois que vous affectez une PED à une boîte aux lettres.
  
Utilisez l’applet de commande Get-MailboxStatistics pour déterminer si une boîte aux lettres est chiffré.
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

La propriété IsEncrypted renvoie la valeur **true** si la boîte aux lettres est chiffré et la valeur **false** si la boîte aux lettres n’est pas chiffré. 

La durée des déplacements de boîtes aux lettres varie selon le nombre de boîtes aux lettres à laquelle vous affectez une PED pour la première fois, ainsi que la taille des boîtes aux lettres. Si les boîtes aux lettres n’ont pas été chiffrées après une semaine depuis le moment où vous avez affecté la prévention, d’initier un déplacement de boîte aux lettres pour les boîtes aux lettres non chiffrés à l’aide de l’applet de commande New-MoveRequest.

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a>Office 365 : Configuration de la clé client pour SharePoint Online et OneDrive entreprise
<a name="AzureSteps"> </a>

Avant de commencer, assurez-vous que vous avez effectué les tâches requises pour configurer Azure clé coffre-fort. Pour plus d’informations, voir [effectuer des tâches dans Azure clé coffre-fort et FastTrack Microsoft pour la clé client](controlling-your-data-using-customer-key.md#AzureSteps) . 
  
Pour configurer la clé client pour SharePoint Online et OneDrive entreprise, vous devez effectuer ces étapes en vous connectant à distance à SharePoint Online avec Windows PowerShell.
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a>Créer une stratégie de chiffrement des données (PED) pour chaque OneDrive et SharePoint Online pour entreprise geo
<a name="CreateDEP4SPOODfB"> </a>

Un PED est associé à un ensemble de clés stockées dans Azure clé coffre-fort. Vous appliquez un PED à toutes vos données dans un emplacement géographique, également appelé une geo. Si vous utilisez la fonctionnalité multi-geo d’Office 365 (en aperçu), vous pouvez créer un PED par localisés. Si vous n’utilisez pas multi-localisés, vous pouvez créer un PED dans Office 365 pour une utilisation avec SharePoint Online et OneDrive for Business. Office 365 utilise les clés identifiés dans le PED pour chiffrer des données dans cette zone géographique. Pour créer la prévention, vous devez les URI de coffre-fort clé que vous avez obtenu précédemment. Pour obtenir des instructions, consultez la rubrique [obtenir l’URI pour chaque clé Azure clé coffre-fort](controlling-your-data-using-customer-key.md#GetKeyURI) . 
  
N’oubliez pas ! Lorsque vous créez un PED, vous spécifiez deux clés qui se trouvent dans deux différentes chambres fortes de clé Azure. Assurez-vous que ces clés sont trouvent dans deux régions Azure distinctes pour assurer la redondance géographique.
  
Pour créer un PED, vous devez vous connecter à distance à SharePoint Online à l’aide de Windows PowerShell.
  
1. Sur votre ordinateur local, à l’aide un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365, [se connecter à SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx)Professionnel ou de l’école.
    
2. Dans Microsoft SharePoint Online Management Shell, exécutez l’applet de commande [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) comme suit : 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   Lorsque vous enregistrez la prévention, le chiffrement commence les données dans la zone géographique. Cela peut prendre un certain temps.
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a>Valider le chiffrement du groupe de Sites, Sites d’équipe et OneDrive entreprise
<a name="validateencryptionSPO"> </a>

Vous pouvez vérifier l’état de chiffrement en exécutant l’applet de commande Get-SPODataEncryptionPolicy comme suit :
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

La sortie de cette applet de commande comprend :
  
- L’URI de la clé primaire.
    
- L’URI de la clé secondaire.
    
- L’état de chiffrement pour la zone géographique. États possibles sont les suivantes :
    
  - **Non enregistré :** Chiffrement de la clé client n’a pas été appliqué. 
    
  - **Inscription :** Chiffrement de la clé client a été appliqué et vos fichiers sont en cours de chiffrement. Si votre geo est dans cet état, vous devez également être affichées plus d’informations sur quel pourcentage de sites dans la zone géographique sont complètes de sorte que vous pouvez surveiller la progression de chiffrement. 
    
  - **Enregistré :** Chiffrement de la clé client a été appliqué, et tous les fichiers dans tous les sites ont été chiffrés. 
    
  - **Propagées :** Appliquer une clé est en cours. Si votre geo est dans cet état, vous devez également être affichées plus d’informations sur quel pourcentage de sites avoir effectué l’opération roll clés afin que vous pouvez surveiller la progression. 
    
## <a name="managing-customer-key-for-office-365"></a>Gestion de la clé client pour Office 365
<a name="ManageCustomerKey"> </a>

Une fois que vous avez configuré la clé client pour Office 365, vous pouvez effectuer ces tâches de gestion supplémentaires.
  
- [Restaurer les clés de coffre-fort de clé Azure](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [Restauration ou faire pivoter une clé dans Azure clé coffre-fort que vous utilisez avec la clé client](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [Gérer les autorisations de clés coffre-fort](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [Déterminer la PED affecté à une boîte aux lettres](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a>Restaurer les clés de coffre-fort de clé Azure
<a name="RestoreAzureKeyVaultKeys"> </a>

Avant d’effectuer une restauration, utilisez les fonctionnalités de récupération fournies par suppression réversible. Toutes les clés qui sont utilisés avec la clé client sont requis pour que la suppression réversible activée. Suppression réversible agit comme une Corbeille et permet la récupération pendant 90 jours sans avoir besoin de restaurer. Restauration doit être requis uniquement dans les circonstances extrêmes ou inhabituelles, par exemple, si la clé ou la clé coffre-fort est perdue. Si vous devez restaurer une clé pour une utilisation avec la clé de client dans Azure PowerShell, exécutez l’applet de commande Restore-AzureKeyVaultKey comme suit :
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

Par exemple :
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

Si une clé portant le même nom existe déjà dans le coffre-fort clé, l’opération de restauration échoue. Restauration-AzureKeyVaultKey restaure toutes les versions principales et toutes les métadonnées pour la clé, y compris le nom de la clé.
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a>Restauration ou faire pivoter une clé dans Azure clé coffre-fort que vous utilisez avec la clé client
<a name="RollCKkey"> </a>

Déploiement clés n’est pas requis par un coffre-fort de clé Azure ou par clé client. En outre, les clés qui sont protégés par un HSM sont pratiquement impossibles de compromettre. Même si une clé de la racine de la possession d’un acteur malveillant il n’existe aucun moyen possible de l’utiliser pour déchiffrer des données, dans la mesure où Office 365 uniquement le code sait comment l’utiliser. Restauration d’une clé est toutefois, pris en charge par clé client.
  
> [!CAUTION]
> Déployer uniquement une clé de chiffrement que vous utilisez avec la clé client lorsque existe une raison technique effacer ou une exigence de conformité dicte que vous devrez déployer la clé. En outre, ne supprimez pas toutes les clés qui sont ou ont été associés à des stratégies. Lorsque vous faites vos clés, les qu’il n’y être contenu chiffré avec les précédentes clés. Par exemple, tandis que les boîtes aux lettres actives sont nouveau chiffrées fréquemment, inactif, les boîtes aux lettres déconnectées et désactivées peuvent toujours chiffrées avec les précédentes clés. SharePoint Online effectue sauvegarde de contenu à des fins de restauration et de récupération, il peut être toujours contenu archivé à l’aide des anciennes clés.<br/> Pour garantir la sécurité de vos données, SharePoint Online permettra pas plus d’une clé reporter opération en cours à la fois. Si vous souhaitez déployer à la fois des clés dans un coffre-fort clé, vous devrez attendre la première opération roll clés à entièrement terminée. Nous conseillons échelonnez vos opérations de déploiement clés à des intervalles différents, afin que ce n’est pas un problème. 
  
Lorsque vous faites une clé, vous demandez une nouvelle version d’une clé existante. Pour demander une nouvelle version d’une clé existante, vous utilisez la cmdlet [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), même avec la même syntaxe que vous avez utilisé pour créer la clé en premier lieu.
  
Par exemple :
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

Dans cet exemple, car une clé nommée **Contoso-O365EX-NA-VaultA1-Key001** déjà existe dans le coffre-fort **Contoso-O365EX-NA-VaultA1** , une nouvelle version de clés sera créée. L’opération ajoute une nouvelle version de la clé. Cette opération permet de conserver les versions précédentes de clé dans l’historique de version de la clé, afin que les données précédemment chiffrées avec cette clé peuvent toujours être déchiffrées. Une fois que vous avez terminé de roulement n’importe quelle touche qui est associé à un PED, vous devez exécuter une applet de commande supplémentaire pour garantir la que clé client commence avec la nouvelle clé. 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Activer Exchange Online et Skype pour les entreprises à utiliser une nouvelle clé après avoir reporter ou rotation des clés dans Azure clé coffre-fort

Lorsque vous faites une des clés Azure clé coffre-fort associés à un PED utilisé avec Exchange Online et Skype pour les entreprises, vous devez exécuter la commande suivante pour mettre à jour de la prévention et activer Office 365 commencer à utiliser la nouvelle clé.
  
Pour indiquer la clé de client à utiliser la nouvelle clé pour chiffrer les boîtes aux lettres dans Office 365, exécutez l’applet de commande Set-DataEncryptionPolicy comme suit :
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

Dans les 48 heures, les boîtes aux lettres actives chiffrées à l’aide de cette stratégie sera associés à la clé de mise à jour. Utilisez les étapes de [déterminer la PED affecté à une boîte aux lettres](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) pour vérifier la valeur de la propriété DataEncryptionPolicyID pour la boîte aux lettres. La valeur de cette propriété modifie une fois la clé de mise à jour a été appliquée. 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a>Activer SharePoint Online et OneDrive entreprise à utiliser une nouvelle clé après avoir reporter ou rotation des clés dans Azure clé coffre-fort

Lorsque vous faites une des clés Azure clé coffre-fort associés à un PED utilisée avec SharePoint Online et OneDrive pour les entreprises, vous devez exécuter l’applet de commande [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) pour mettre à jour la prévention et activer Office 365 commencer à utiliser la nouvelle clé. 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

Démarre l’opération de déploiement clés pour SharePoint Online et OneDrive for Business. Cette action n’est pas immédiate. Pour afficher la progression de la clé à l’opération, exécutez l’applet de commande Get-SPODataEncryptionPolicy comme suit :
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a>Gérer les autorisations de clés coffre-fort
<a name="Managekeyvaultperms"> </a>

Plusieurs applets de commande qui permettent d’afficher et, si nécessaire, supprimer des autorisations de clés coffre-fort. Vous devrez peut-être supprimer les autorisations, par exemple, lorsqu’un employé quitte l’équipe.
  
Pour afficher les autorisations de clés coffre-fort, exécutez l’applet de commande Get-AzureRmKeyVault :
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

Par exemple :
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

Pour supprimer des autorisations d’administrateur, exécutez l’applet de commande Remove-AzureRmKeyVaultAccessPolicy :
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

Par exemple :
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a>Déterminer la PED affecté à une boîte aux lettres
<a name="DeterminemailboxDEP"> </a>

Pour déterminer la PED affecté à une boîte aux lettres, utilisez l’applet de commande Get-MailboxStatistics. L’applet de commande renvoie l’identificateur unique (GUID).
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

Où *GeneralMailboxOrMailUserIdParameter* spécifie une boîte aux lettres. Pour plus d’informations sur l’applet de commande Get-MailboxStatistics, voir [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).
  
Utilisez le GUID pour trouver le nom convivial de la prévention affectée de la boîte aux lettres en exécutant la cmdlet suivante.
  
```
Get-DataEncryptionPolicy <GUID>
```

Où *GUID* est le GUID renvoyé par l’applet de commande Get-MailboxStatistics à l’étape précédente. 
  

