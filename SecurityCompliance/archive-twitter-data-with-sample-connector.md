---
title: Utiliser un exemple de connecteur pour archiver les données Twitter dans Office 365 (version préliminaire)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Les administrateurs peuvent configurer un connecteur natif pour importer des données Twitter dans Office 365. Cela vous permet d’archiver des données provenant de sources de données tierces dans Office 365 de sorte que vous puissiez utiliser les fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données tierces de votre organisation.
ms.openlocfilehash: 6780e3fbb53e2326994e03815403c1e5ae0d0616
ms.sourcegitcommit: f2798d46acfbd56314e809cd3fe0350be807e420
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2019
ms.locfileid: "35014683"
---
# <a name="use-a-sample-connector-to-archive-twitter-data-in-office-365-preview"></a>Utiliser un exemple de connecteur pour archiver les données Twitter dans Office 365 (version préliminaire)

L’exemple de fonctionnalité de connecteur permettant d’archiver des données Twitter dans Office 365 est en aperçu.

Utilisez un exemple de connecteur dans le centre de sécurité & conformité dans Office 365 pour importer et archiver des données à partir de Twitter. Une fois que vous avez configuré et configuré un exemple de connecteur, il se connecte au compte Twitter de votre organisation (de manière planifiée), convertit le contenu d’un élément en un format de message électronique, puis importe ces éléments dans une boîte aux lettres dans Office 365.

Une fois les données Twitter importées, vous pouvez appliquer les fonctionnalités de conformité d’Office 365 telles que les stratégies de conservation pour litige, la recherche de contenu, l’archivage inaltérable, l’audit, la surveillance et les stratégies de rétention d’Office 365 aux données stockées dans la boîte aux lettres. Par exemple, vous pouvez rechercher des données Twitter à l’aide de la recherche de contenu ou associer la boîte aux lettres dans laquelle les données sont stockées avec un dépositaire dans un cas avancé de découverte électronique. L’utilisation d’un exemple de connecteur pour importer et archiver des données Twitter dans Office 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.

> [!NOTE]
> Actuellement, seuls les exemples de connecteurs pour les [pages](archive-facebook-data-with-sample-connector.md) de l’entreprise Twitter et Facebook sont disponibles pour l’aperçu. D’autres exemples de connecteurs seront bientôt disponibles.


## <a name="prerequisites-for-setting-up-a-connector-for-twitter"></a>Conditions préalables à la configuration d’un connecteur pour Twitter

Vous devez remplir les conditions préalables suivantes avant de pouvoir installer et configurer un exemple de connecteur dans le centre de sécurité & Compliance Center pour importer et archiver des données à partir du compte Twitter de votre organisation. 

- Vous avez besoin d’un compte Twitter pour votre organisation; vous devez vous connecter à ce compte lors de la configuration du connecteur.

- Votre organisation doit disposer d’un abonnement Azure valide. Si vous n’avez pas d’abonnement Azure existant, vous pouvez vous inscrire à l’une de ces options:

    - [Inscrivez-vous à un abonnement Azure d’une année gratuite](https://azure.microsoft.com/free) 

    - [S’inscrire pour un abonnement Azure avec paiement en tant que](https://azure.microsoft.com/pricing/purchase-options/pay-as-you-go/)

    > [!NOTE]
    > L' [abonnement Azure Active Directory gratuit](use-your-free-azure-ad-subscription-in-office-365.md) qui est inclus avec votre abonnement Office 365 ne prend pas en charge les connecteurs d’exemple dans le centre de sécurité & Compliance Center.

- Votre organisation doit consentir à autoriser le service d’importation Office 365 à accéder aux données de boîte aux lettres dans votre organisation. Pour accepter cette demande, accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), connectez-vous à l’aide des informations d’identification d’un administrateur général Office 365, puis acceptez la demande.

- L’utilisateur qui configure le connecteur personnalisé dans la sécurité & conformité (à l’étape 7) doit se voir attribuer le rôle importation/exportation de boîte aux lettres dans Exchange Online. Par défaut, ce rôle n’est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle exportation d’importation de boîte aux lettres au groupe de rôles gestion de l’organisation dans Exchange Online. Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d’exportation d’importation de boîte aux lettres, puis ajouter les utilisateurs appropriés en tant que membres. Pour plus d’informations, reportez-vous aux sections [créer des groupes de rôles](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) ou modifier des [groupes](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) de rôles dans l’article «gérer des groupes de rôles dans Exchange Online».

## <a name="step-1-download-the-pre-built-connector-app-package-from-github"></a>Étape 1: Télécharger le package d’application de connecteur pré-généré à partir de GitHub

La première étape consiste à télécharger le code source de l’exemple de l’application de connecteur Twitter qui utilisera une API Twitter pour se connecter à votre compte Twitter et extraire les données afin de pouvoir les importer dans Office 365.

1. Accédez à [ce site github](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases). 
2. Sous la dernière version, cliquez sur le fichier **SampleConnector. zip** .
3. Enregistrez le fichier ZIP à un emplacement sur votre ordinateur local. Vous téléchargez ce fichier zip vers Azure à l’étape 4.

## <a name="step-2-create-an-app-in-azure-active-directory"></a>Étape 2: créer une application dans Azure Active Directory

L’étape suivante consiste à inscrire une nouvelle application dans Azure Active Directory (AAD). Cette application correspond à la ressource Web App que vous implémentez à l’étape 4 pour le connecteur Twitter. 

Pour obtenir des instructions pas à pas, reportez-vous à [l’étape 2: créer une application dans Azure Active Directory](deploy-twitter-connector.md#step-2-create-an-app-in-azure-active-directory).

Lors de l’exécution de cette étape (en suivant les instructions pas à pas), vous enregistrez les informations suivantes dans un fichier texte. Les valeurs de ces éléments seront utilisées dans les étapes ultérieures du processus de déploiement.

- ID d’application AAD
- Clé secrète de l’application AAD
- URI de l’application AAD
- ID de locataire

## <a name="step-3-create-an-azure-storage-account"></a>Étape 3: créer un compte de stockage Azure

Le connecteur Twitter que vous déployez pour votre organisation télécharge les éléments à partir de Twitter vers l’emplacement de stockage Azure que vous créez au cours de cette étape. Une fois que vous avez créé un connecteur personnalisé dans le centre de sécurité & conformité (à l’étape 7), le service d’importation Office 365 copie les données Twitter à partir de l’emplacement de stockage Azure vers une boîte aux lettres dans Office 365. Comme indiqué précédemment dans la section [conditions préalables](#prerequisites-for-setting-up-a-connector-for-twitter) , vous devez disposer d’un abonnement Azure valide pour créer un compte de stockage Azure.

Pour obtenir des instructions pas à pas, reportez-vous à [l’étape 3: créer un compte de stockage Azure](deploy-twitter-connector.md#step-3-create-an-azure-storage-account).

Lors de l’exécution de cette étape (en suivant les instructions pas à pas), vous enregistrez l’URI de chaîne de connexion qui est généré. Vous utilisez cette chaîne lors de la création d’une ressource d’application Web dans Azure à l’étape 4.

## <a name="step-4-create-a-web-app-resource-in-azure"></a>Étape 4: créer une ressource d’application Web dans Azure

L’étape suivante consiste à créer une ressource d’application Web dans Azure pour le connecteur Twitter. 

Pour obtenir des instructions pas à pas, reportez-vous à [l’étape 4: créer une ressource d’application Web dans Azure](deploy-twitter-connector.md#step-4-create-a-new-web-app-resource-in-azure).

Lors de l’exécution de cette étape (en suivant les instructions pas à pas), vous devez fournir les informations suivantes (que vous avez copiées dans un fichier texte après avoir effectué les étapes précédentes) lors de la création de la ressource d’application Web.

- APISecretKey: vous créez cette clé secrète lors de l’exécution de cette étape; elle est utilisée à l’étape 7.
- StorageAccountConnectionString – URI de chaîne de connexion que vous avez copiée après avoir créé le compte de stockage Azure à l’étape 3.
- tenantId – ID de client de votre organisation Office 365 que vous avez copié après avoir créé l’application de connecteur Twitter dans Azure Active Directory à l’étape 2.

Par ailleurs, vous téléchargez le fichier SampleConnector. zip (que vous avez téléchargé à l’étape 1) dans cette étape pour déployer le code source pour l’application de connecteur Twitter.

Une fois cette étape terminée, veillez à copier l’URL du service d’application Azure ( https://twitterconnector.azurewebsites.net)par exemple,. Vous devez utiliser cela pour effectuer l’étape 5, étape 6, et étape 7).

## <a name="step-5-create-developer-app-on-twitter"></a>Étape 5: créer une application de développeur sur Twitter

L’étape suivante consiste à créer et configurer une application de développeur sur Twitter. Le connecteur personnalisé que vous créez à l’étape 7 utilise l’application Twitter pour interagir avec l’API Twitter afin d’obtenir des données à partir du compte Twitter de votre organisation.

Pour obtenir des instructions pas à pas, reportez-vous à [l’étape 5: créer l’application Twitter](deploy-twitter-connector.md#step-5-create-the-twitter-app).

Lors de l’exécution de cette étape (en suivant les instructions pas à pas), vous enregistrez les informations suivantes dans un fichier texte. Les valeurs de ces éléments seront utilisées pour configurer l’application connecteur Twitter à l’étape 6.

- Clé de l’API Twitter
- Clé secrète de l’API Twitter
- Jeton d’accès Twitter
- Jeton d’accès Twitter secret

## <a name="step-6-configure-the-twitter-connector-app"></a>Étape 6: configuration de l’application de connecteur Twitter

L’étape suivante consiste à ajouter des paramètres de configuration à l’application du connecteur Twitter que vous avez chargée lors de la création de la ressource Azure Web App à l’étape 4. Pour ce faire, accédez à la page d’accueil de votre application de connecteur et configurez-la.

Pour obtenir des instructions pas à pas, reportez-vous à [l’étape 6: configuration de l’application Web de connecteur](deploy-twitter-connector.md#step-6-configure-the-connector-web-app).

Lors de l’exécution de cette étape (en suivant les instructions pas à pas), vous devez fournir les informations suivantes (que vous avez copiées dans un fichier texte après avoir effectué les étapes précédentes):

- Clé de l’API Twitter (obtenue à l’étape 5)
- Clé secrète de l’API Twitter (obtenue à l’étape 5)
- Jeton d’accès Twitter (obtenu à l’étape 5)
- Jeton d’accès Twitter secret (obtenu à l’étape 5)
- ID d’application Azure Active Directory (l’ID d’application AAD obtenu à l’étape 2)
- Clé secrète de l’application Azure Active Directory (la clé secrète de l’application AAD obtenue à l’étape 2)
- URI de l’application Azure Active Directory (URI de l’application AAD obtenue à l’étape 2, par exemple,https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213)

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a>Étape 7: configurer un connecteur personnalisé dans le centre de sécurité & conformité

La dernière étape consiste à configurer le connecteur personnalisé dans le centre de sécurité & conformité qui importe les données du compte Twitter de votre organisation vers une boîte aux lettres spécifiée dans Office 365. Une fois cette étape terminée, le service d’importation Office 365 démarrera le processus d’importation de données de Twitter vers Office 365. 

Pour obtenir des instructions détaillées, reportez-vous à [l’étape 7: configurer un connecteur personnalisé dans le centre de sécurité et de conformité](deploy-twitter-connector.md#step-7-set-up-a-custom-connector-in-the-security-and-compliance-center). 

Lors de l’exécution de cette étape (en suivant les instructions pas à pas), vous devez fournir les informations suivantes (que vous avez copiées dans un fichier texte après avoir effectué les étapes).

- URL du service d’application Azure (obtenue à l’étape 4; par exemple,https://twitterconnector.azurewebsites.net)
- APISecretKey (que vous avez créé à l’étape 4)
