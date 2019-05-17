---
title: Déploiement d’un connecteur pour l’archivage des données Twitter dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: Les administrateurs peuvent configurer un connecteur natif pour importer et archiver des données Twitter vers Office 365. Une fois ces données importées dans Office 365, vous pouvez utiliser des fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données Twitter de votre organisation.
ms.openlocfilehash: 2f9d4842a834858b40e1d788f34f4fb8b2d5b9fd
ms.sourcegitcommit: 5bd7a97aeab1c89e0a3660ba7bdb3200224107a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/16/2019
ms.locfileid: "34103863"
---
# <a name="deploy-a-connector-to-archive-twitter-data-in-office-365"></a>Déploiement d’un connecteur pour l’archivage des données Twitter dans Office 365

Cet article contient le processus étape par étape pour déployer un connecteur qui utilise le service d’importation Office 365 pour importer des données à partir du compte Twitter de votre organisation vers Office 365. Pour une vue d’ensemble de ce processus et une liste des conditions préalables requises pour déployer un connecteur Twitter, reportez-vous à la rubrique [utiliser un exemple de connecteur pour archiver des données Twitter dans Office 365 (version d’évaluation)](archive-twitter-data-with-sample-connector.md). 

## <a name="step-1-download-the-package"></a>Étape 1: Télécharger le package

Téléchargez le package prédéfini à partir de la section Release dans le référentiel GitHub à l' [https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases](https://github.com/microsoft/m365-sample-twitter-connector-csharp-aspnet/releases)adresse. Sous la dernière version, téléchargez le fichier zip nommé **SampleConnector. zip**. Vous allez télécharger ce fichier zip vers Azure à l’étape 4.

## <a name="step-2-create-an-app-in-azure-active-directory"></a>Étape 2: créer une application dans Azure Active Directory

1. Accédez à <https://portal.azure.com> et connectez-vous à l’aide des informations d’identification d’un compte d’administrateur global Office 365.

   ![](media/TCimage01.png)

2. Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.

   ![](media/TCimage02.png)

3. Dans le volet de navigation de gauche, cliquez sur **inscriptions des applications (aperçu)** , puis cliquez sur **nouvelle inscription**.

   ![](media/TCimage03.png)

4. Inscrivez l’application. Sous **URI de redirection (facultatif)**, sélectionnez Web dans la liste déroulante type d' <https://portal.azure.com> application, puis tapez dans la zone de l’URI.

   ![](media/TCimage04.png)

5. Copiez l’ID d' **application (client)** et l' **ID de répertoire (** client) et enregistrez-les dans un fichier texte ou un autre emplacement sûr. Vous utiliserez ces ID dans les étapes ultérieures.

    ![](media/TCimage05.png)

6. Accédez à **certificats & secrets de la nouvelle application** , puis sous **secrets client** , cliquez sur **nouvelle clé secrète client**.

   ![](media/TCimage06.png)

7. Créer une nouvelle clé secrète. Dans la zone Description, tapez le secret, puis choisissez une période d’expiration. 

   ![](media/TCimage08.png)

8. Copiez la valeur de la clé secrète et enregistrez-la dans un fichier texte ou dans un autre emplacement de stockage. Il s’agit de la clé secrète de l’application AAD que vous utiliserez plus tard.

   ![](media/TCimage09.png)

9. Accédez au **manifeste** et copiez le identifierUris (également appelé URI de l’application AAD) en surbrillance dans la capture d’écran suivante. Copiez l’URI de l’application AAD dans un fichier texte ou un autre emplacement de stockage. Vous l’utiliserez à l’étape 6.

    ![](media/TCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a>Étape 3: créer un compte de stockage Azure

1.  Accédez à la page d’accueil Azure de votre organisation.

    ![](media/TCimage11.png)

2. Cliquez sur **créer une ressource** et tapez le **compte de stockage** dans la zone de recherche.

   ![](media/TCimage12.png)

3. Cliquez sur **stockage**, puis sur **compte de stockage**.

   ![](media/TCimage13.png)

4. Sur la page **créer un compte de stockage** , dans la zone abonnement, sélectionnez **paiement en cours** ou **version d’évaluation gratuite** en fonction du type d’abonnement Azure dont vous disposez. 

   ![](media/TCimage14.png)

5. Sélectionnez ou créez un groupe de ressources.

   ![](media/TCimage15.png)

6. Tapez un nom pour le compte de stockage.

   ![](media/TCimage16.png)

7. Passez en revue, puis cliquez sur **créer** pour créer le compte de stockage.

   ![](media/TCimage17.png)

8. Après quelques instants, cliquez **** sur Actualiser, puis sur **accéder à la ressource** pour accéder au compte de stockage.

   ![](media/TCimage18.png)

9. Cliquez sur **touches d’accès** dans le volet de navigation de gauche.

   ![](media/TCimage19.png)

10. Copiez une **chaîne de connexion** et enregistrez-la dans un fichier texte ou un autre emplacement de stockage. Vous l’utiliserez lors de la création d’une ressource d’application Web à l’étape 4.

    ![](media/TCimage20.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a>Étape 4: créer une nouvelle ressource d’application Web dans Azure

1. Sur la page d' **Accueil** du portail Azure, cliquez sur **créer une \> ressource \> tout le Web App**. Dans la page **application Web** , cliquez sur **créer**.

   ![](media/TCimage21.png)

2. Renseignez les détails (comme indiqué ci-dessous), puis créez l’application Web. Notez que le nom que vous entrez dans la zone nom de l' **application** sera utilisé pour créer l’URL du service d’application Azure. par exemple twitterconnector.azurewebsites.net.

   ![](media/TCimage22.png)

3. Accédez à la ressource d’application Web nouvellement créée, cliquez sur paramètres de l' **application** dans le volet de navigation de gauche. Sous **paramètres**de l’application, cliquez sur **Ajouter un nouveau paramètre** , puis ajoutez les trois paramètres suivants. Utilisez les valeurs (que vous avez copiées dans le fichier texte à partir des étapes précédentes): 

    - **APISecretKey** : vous pouvez taper n’importe quelle valeur comme clé secrète. Il sera utilisé pour accéder à l’application Web de connecteur à l’étape 7.

    - **StorageAccountConnectionString** – URI de chaîne de connexion que vous avez copiée après avoir créé le compte de stockage Azure à l’étape 3.

    - **tenantId** – ID de client de votre organisation Office 365 que vous avez copié après avoir créé l’application de connecteur Twitter dans Azure Active Directory à l’étape 2.

    ![](media/TCimage23.png)

4. Sous **paramètres généraux**, cliquez sur **en** regard de l’est **toujours activé**. Cliquez sur **Enregistrer** en haut de la page pour enregistrer les paramètres de l’application.

   ![](media/TCimage24.png)

5. La dernière étape consiste à télécharger le code source de l’application du connecteur vers Azure que vous avez téléchargé à l’étape 1. Dans un navigateur Web, accédez à https://<AzureAppResourceName>. SCM.azurewebsites.net/ZipDeployUi. Par exemple, si le nom de votre ressource d’application Azure (que vous avez nommée à l’étape 2 de cette section) est **twitterconnector**, vous accédez https://twitterconnector.scm.azurewebsites.net/ZipDeployUià.

6. Faites glisser et déposez le SampleConnector. zip (que vous avez téléchargé à l’étape 1) sur cette page. Une fois que les fichiers sont téléchargés et que le déploiement réussit, la page ressemblera à la capture d’écran suivante.

   ![](media/TCimage25.png)

## <a name="step-5-create-the-twitter-app"></a>Étape 5: créer l’application Twitter

1. Accédez à https://developer.twitter.com, connectez-vous à l’aide des informations d’identification pour le compte de développeur de votre organisation, puis cliquez sur **applications**.

   ![TCimage25-5. png](media/TCimage25-5.png)
2. Cliquez sur **créer une application**.
   
   ![](media/TCimage26.png)

3. Sous **Détails**de l’application, ajoutez des informations sur l’application.

   ![](media/TCimage27.png)

4. Dans le tableau de bord du développeur Twitter, sélectionnez l’application que vous venez de créer et copiez l’ID d’application affiché et enregistrez-le dans un fichier texte ou dans un autre emplacement de stockage. Ensuite, cliquez sur **Détails**.
   
   ![](media/TCimage28.png)

5. Sous l’onglet **clés et jetons** , sous clés de l' **API consommateur** , copiez la clé secrète de l’API et enregistrez-la dans un fichier texte ou un autre emplacement de stockage. Ensuite, cliquez sur **créer** pour générer un jeton d’accès et un secret de jeton d’accès, puis copiez-les dans un fichier texte ou un autre emplacement de stockage.
   
   ![](media/TCimage29.png)

   Ensuite, cliquez sur **créer** pour générer un jeton d’accès et un secret de jeton d’accès, puis copiez-les dans un fichier texte ou un autre emplacement de stockage.

6. Cliquez sur l’onglet **autorisations** et configurez les autorisations comme indiqué dans la capture d’écran suivante:

   ![](media/TCimage30.png)

7. Une fois que vous avez enregistré les paramètres d’autorisation, cliquez sur l’onglet Détails de l' **application** , puis cliquez sur **modifier > modifier les détails**.

   ![](media/TCimage31.png)

8. Effectuez les tâches suivantes:

   - Activez la case à cocher pour autoriser l’application de connecteur à se connecter à Twitter.
   
   - Ajoutez l’URI de redirection OAuth en utilisant le format suivant: ** \<connectorserviceuri>/views/TwitterOAuth**, où la valeur de *connectorserviceuri* est l’URL de service d’application Azure pour votre organisation; par exemple https://twitterconnector.azurewebsites.net/Views/TwitterOAuth.

   ![](media/TCimage32.png)

L’application de développeur Twitter est maintenant prête à être utilisée.

## <a name="step-6-configure-the-connector-web-app"></a>Étape 6: configuration de l’application Web de connecteur 

1. Accédez à https://\<AzureAppResourceName>. azurewebsites. net (où **AzureAppResourceName** est le nom de votre ressource d’application Azure que vous avez nommée à l’étape 4) par exemple, si le nom est **twitterconnector**, accédez à https://twitterconnector.azurewebsites.net. La page d’accueil de l’application ressemblera à la capture d’écran suivante.

   ![](media/FBCimage41.png)

2. Cliquez sur **configurer** pour afficher une page de connexion.

   ![](media/FBCimage42.png)

3. Dans la zone ID de locataire, tapez ou collez l’ID de votre client (que vous avez obtenu à l’étape 2). Dans la zone mot de passe, tapez ou collez le APISecretKey (que vous avez obtenu à l’étape 2), puis cliquez sur **définir les paramètres de configuration** pour afficher la page Détails de la **configuration** .

   ![](media/TCimage35.png)

4. Sous **Détails**de la configuration, entrez les paramètres de configuration suivants 

   - **ID de l’application Twitter** : ID de l’application Twitter que vous avez créée à l’étape 5.
   - Clé secrète de l' **application Twitter** : clé secrète de l’API pour l’application Twitter que vous avez créée à l’étape 5.
   - **Jeton client Twitter** : jeton d’accès que vous avez créé à l’étape 5.
   - **Clé secrète de jeton client Twitter** -jeton d’accès secret que vous avez créé à l’étape 5.
   - **ID d’application AAD** : ID d’application pour l’application Azure Active Directory que vous avez créée à l’étape 2
   - **Clé secrète de l’application AAD** : valeur de la clé secrète APISecretKey que vous avez créée à l’étape 4.
   - **URI de l’application AAD** : URI de l’application AAD obtenue à l’étape 2; par exemple, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.
   - **Clé d’instrumentation Insights** de l’application-laissez cette zone vide.

5. Cliquez sur **Enregistrer** pour enregistrer les paramètres du connecteur.

## <a name="step-7-set-up-a-custom-connector-in-the-security-and-compliance-center"></a>Étape 7: configurer un connecteur personnalisé dans le centre de sécurité et de conformité

1.  Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données \> importer des données**tierces.

    ![](media/TCimage36.png)

2. Cliquez sur **Ajouter un connecteur** , puis sur **Twitter**.

   ![](media/TCimage37.png)

3. Dans la page **Ajouter une application connecteur** , entrez les informations suivantes, puis cliquez sur **valider le connecteur**.

    - Dans la première zone, tapez un nom pour le connecteur, tel que **Twitter**.
    - Dans la deuxième zone, tapez ou collez la valeur du APISecretKey que vous avez ajouté à l’étape 4.
    - Dans la troisième zone, tapez ou collez l’URL du service d’application Azure; par exemple **https://twitterconnector.azurewebsites.net**.

   Une fois le connecteur validé, cliquez sur **suivant**.

   ![](media/TCimage38.png)

4. Cliquez sur **connexion avec application connecteur**.

   ![](media/TCimage39.png)

5. Tapez ou collez à nouveau le APISecretKey, puis cliquez sur **connexion au service connecteur**.

   ![](media/TCimage40.png)


6. Cliquez sur **continuer avec Twitter**.

7. Sur la page de connexion Twitter, connectez-vous à l’aide des informations d’identification du compte pour le compte Twitter de votre organisation.

   ![](media/TCimage42.png)

   Une fois que vous êtes connecté, la page Twitter affiche le message suivant: «travail de connecteur Twitter correctement configuré».

8. Cliquez sur **Terminer** pour terminer la configuration du connecteur Twitter.

9. Sur la page **définir les filtres** , vous pouvez appliquer un filtre pour importer (et archiver) les éléments qui sont un certain âge. Cliquez sur **Suivant**.

   ![](media/TCimage44.png)

10. Sur la page **définir le compte de stockage** , sélectionnez la boîte aux lettres Office 365 vers laquelle les éléments Twitter seront importés.

    ![](media/TCimage45.png)

11. Vérifiez vos paramètres, puis cliquez sur **Terminer** pour terminer l’installation du connecteur dans le centre de sécurité _AMP_ Compliance Center.

    ![](media/TCimage46.png)

    ![](media/TCimage47.png)

12. Accédez à la page **données** tierces d’archivage pour voir la progression du processus d’importation.

    ![](media/TCimage48.png)
