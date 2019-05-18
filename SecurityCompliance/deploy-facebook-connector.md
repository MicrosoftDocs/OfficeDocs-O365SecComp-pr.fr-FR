---
title: Déployer un connecteur pour archiver des données Facebook dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: Les administrateurs peuvent configurer un connecteur natif pour importer et archiver des pages Facebook dans Office 365. Une fois ces données importées dans Office 365, vous pouvez utiliser des fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer la gouvernance des données Facebook de votre organisation.
ms.openlocfilehash: b0ec46cea2dd5722633e7fc302cdd0d03cd5d56d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150556"
---
# <a name="deploy-a-connector-to-archive-facebook-data-in-office-365"></a>Déployer un connecteur pour archiver des données Facebook dans Office 365

Cet article contient le processus étape par étape pour déployer un connecteur qui utilise le service d’importation Office 365 pour importer des données à partir de pages d’entreprise Facebook vers Office 365. Pour une vue d’ensemble de ce processus et une liste des conditions préalables requises pour déployer un connecteur Facebook, voir [utiliser un exemple de connecteur pour archiver des données Facebook dans Office 365 (version d’évaluation)](archive-facebook-data-with-sample-connector.md). 

## <a name="step-1-download-the-package"></a>Étape 1: Télécharger le package

Téléchargez le package prédéfini à partir de la section Release dans le référentiel GitHub à l’adresse <https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases>suivante:. Sous la dernière version, téléchargez le fichier zip nommé **SampleConnector. zip**. Vous allez télécharger ce fichier zip vers Azure à l’étape 4.

## <a name="step-2-create-an-app-in-azure-active-directory"></a>Étape 2: créer une application dans Azure Active Directory

1. Accédez à <https://portal.azure.com> et connectez-vous à l’aide des informations d’identification d’un compte d’administrateur global Office 365.

    ![Créer une application dans AAD](media/FBCimage1.png)

2. Dans le volet de navigation de gauche, cliquez sur **Azure Active Directory**.

    ![](media/FBCimage2.png)

3. Dans le volet de navigation de gauche, cliquez sur **inscriptions des applications (aperçu)** , puis cliquez sur **nouvelle inscription**.

    ![](media/FBCimage3.png)

4. Inscrivez l’application. Sous URI de redirection, sélectionnez Web dans la liste déroulante type d' <https://portal.azure.com> application, puis tapez dans la zone de l’URI.

   ![](media/FBCimage4.png)

5. Copiez l’ID d' **application (client)** et l' **ID de répertoire (** client) et enregistrez-les dans un fichier texte ou un autre emplacement sûr. Vous utiliserez ces ID dans les étapes ultérieures.

   ![](media/FBCimage5.png)

6. Accédez à **certificats & secrets de la nouvelle application.**

   ![](media/FBCimage6.png)

7. Cliquez sur **nouvelle clé secrète client**

   ![](media/FBCimage7.png)

8. Créer une nouvelle clé secrète. Dans la zone Description, tapez le secret, puis choisissez une période d’expiration. 

    ![](media/FBCimage8.png)

9. Copiez la valeur de la clé secrète et enregistrez-la dans un fichier texte ou dans un autre emplacement de stockage. Il s’agit de la clé secrète de l’application AAD que vous utiliserez plus tard.

   ![](media/FBCimage9.png)

10. Accédez au **manifeste** et copiez le identifierUris (également appelé URI de l’application AAD) en surbrillance dans la capture d’écran suivante. Copiez l’URI de l’application AAD dans un fichier texte ou un autre emplacement de stockage. Vous l’utiliserez à l’étape 6.

   ![](media/FBCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a>Étape 3: créer un compte de stockage Azure

1. Accédez à la page d’accueil Azure de votre organisation.

    ![](media/FBCimage11.png)

2. Cliquez sur **créer une ressource** et tapez le **compte de stockage** dans la zone de recherche.

    ![](media/FBCimage12.png)

3. Cliquez sur **stockage**, puis sur **compte de stockage**.

    ![](media/FBCimage13.png)

4. Sur la page **créer un compte de stockage** , dans la zone abonnement, sélectionnez **paiement en cours** ou **version d’évaluation gratuite** en fonction du type d’abonnement Azure dont vous disposez. Ensuite, sélectionnez ou créez un groupe de ressources.

    ![](media/FBCimage14.png)

5. Tapez un nom pour le compte de stockage.

    ![](media/FBCimage15.png)

6. Passez en revue, puis cliquez sur **créer** pour créer le compte de stockage.

    ![](media/FBCimage16.png)

7. Après quelques instants, cliquez **** sur Actualiser, puis sur **accéder à la ressource** pour accéder au compte de stockage.

    ![](media/FBCimage17.png)

8. Cliquez sur **touches d’accès** dans le volet de navigation de gauche.

    ![](media/FBCimage18.png)

9. Copiez une **chaîne de connexion** et enregistrez-la dans un fichier texte ou un autre emplacement de stockage. Vous l’utiliserez lors de la création d’une ressource d’application Web.

    ![](media/FBCimage19.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a>Étape 4: créer une nouvelle ressource d’application Web dans Azure

1. Sur la page d' **Accueil** du portail Azure, cliquez sur **créer une \> ressource \> tout le Web App**. Dans la page **application Web** , cliquez sur **créer**. 

   ![](media/FBCimage20.png)

2. Renseignez les détails (comme indiqué ci-dessous), puis créez l’application Web. Notez que le nom que vous entrez dans la zone nom de l' **application** sera utilisé pour créer l’URL du service d’application Azure. par exemple fbconnector.azurewebsites.net.

   ![](media/FBCimage21.png)

3. Accédez à la ressource d’application Web nouvellement créée, cliquez sur paramètres de l' **application** dans le volet de navigation de gauche. Sous paramètres de l’application, cliquez sur Ajouter un nouveau paramètre, puis ajoutez les trois paramètres suivants. Utilisez les valeurs (que vous avez copiées dans le fichier texte à partir des étapes précédentes): 

    - **APISecretKey** : vous pouvez taper n’importe quelle valeur comme clé secrète. Il sera utilisé pour accéder à l’application Web de connecteur à l’étape 7.

    - **StorageAccountConnectionString** – URI de chaîne de connexion que vous avez copiée après avoir créé le compte de stockage Azure à l’étape 3.

    - **tenantId** : ID de client de votre organisation Office 365 que vous avez copié après avoir créé l’application de connecteur Facebook dans Azure Active Directory à l’étape 2.

    ![](media/FBCimage22.png)

4. Sous **paramètres généraux**, cliquez sur **en** regard de l’est **toujours activé**. Cliquez sur **Enregistrer** en haut de la page pour enregistrer les paramètres de l’application.

   ![](media/FBCimage23.png)

5. La dernière étape consiste à télécharger le code source de l’application du connecteur vers Azure que vous avez téléchargé à l’étape 1. Dans un navigateur Web, accédez à https://<AzureAppResourceName>. SCM.azurewebsites.net/ZipDeployUi. Par exemple, si le nom de votre ressource d’application Azure (que vous avez nommée à l’étape 2 de cette section) est **fbconnector**, vous accédez https://fbconnector.scm.azurewebsites.net/ZipDeployUià. 

6. Faites glisser et déposez le SampleConnector. zip (que vous avez téléchargé à l’étape 1) sur cette page. Une fois que les fichiers sont téléchargés et que le déploiement réussit, la page ressemblera à la capture d’écran suivante.

   ![](media/FBCimage24.png)

## <a name="step-5-register-the-facebook-app"></a>Étape 5: inscrire l’application Facebook

1. Accédez à <https://developers.facebook.com> , connectez-vous à l’aide des informations d’identification du compte pour les pages d’entreprise Facebook de votre organisation, puis cliquez sur **Ajouter une nouvelle application**.

   ![](media/FBCimage25.png)

2. Créer un ID d’application.

   ![](media/FBCimage26.png)

3. Dans le volet de navigation de gauche, cliquez sur **Ajouter des produits** , puis cliquez sur **configurer** dans la vignette de **connexion Facebook** .

   ![](media/FBCimage27.png)

4. Sur la page intégration de la connexion Facebook, cliquez sur **Web**.

   ![](media/FBCimage28.png)

5. Ajoutez l’URL du service d’application Azure; par exemple https://fbconnector.azurewebsites.net.

   ![](media/FBCimage29.png)

6. Complétez la section démarrage rapide de la configuration de connexion Facebook.

   ![](media/FBCimage30.png)

7. Dans le volet de navigation de gauche sous **connexion Facebook**, cliquez sur **paramètres**, puis ajoutez l’URI de redirection OAuth dans la zone URI de **redirection OAuth valide** ; Utilisez le format ** \<connectorserviceuri>/views/FacebookOAuth**, où la valeur de connectorserviceuri est l’URL de service d’application Azure pour votre organisation; par exemple https://fbconnector.azurewebsites.net.

   ![](media/FBCimage31.png)

8. Dans le volet de navigation de gauche, cliquez sur **Ajouter des produits** , puis sur webhooks **.** Dans le menu déroulant **page** , cliquez sur **page**. 

   ![](media/FBCimage32.png)

9. Ajoutez l’URL de rappel des webhooks et ajoutez un jeton de vérification. Le format de l’URL de rappel, utilisez le format ** <connectorserviceuri>/API/FbPageWebhook**, où la valeur de connectorserviceuri est l’URL de service d’application Azure pour votre organisation; par exemple https://fbconnector.azurewebsites.net. 

    Le jeton Verify doit ressembler à un mot de passe fort. Copiez le jeton de vérification dans un fichier texte ou un autre emplacement de stockage.

     ![](media/FBCimage33.png)

10. Testez et abonnez-vous au point de terminaison pour le flux.

    ![](media/FBCimage34.png)

11. Ajoutez une URL de confidentialité, une icône d’application et une utilisation professionnelle. Copiez également l’ID de l’application et la clé secrète de l’application dans un fichier texte ou un autre emplacement de stockage.

    ![](media/FBCimage35.png)

12. Rendez l’application publique.

    ![](media/FBCimage36.png)

13. Ajouter un utilisateur au rôle administrateur ou testeur.

    ![](media/FBCimage37.png)

14. Ajoutez l’autorisation d' **accès au contenu public** de la page.

    ![](media/FBCimage38.png)

15. Ajouter l’autorisation gérer les pages.

    ![](media/FBCimage39.png)

16. Obtenir l’application examinée par Facebook.

    ![](media/FBCimage40.png)

## <a name="step-6-configure-the-connector-web-app"></a>Étape 6: configuration de l’application Web de connecteur

1. Accédez à https://\<AzureAppResourceName>. azurewebsites. net (où AzureAppResourceName est le nom de votre ressource d’application Azure que vous avez nommée à l’étape 4) par exemple, si le nom est **fbconnector**, accédez à https://fbconnector.azurewebsites.net. La page d’accueil de l’application ressemblera à la capture d’écran suivante.


   ![](media/FBCimage41.png)

2. Cliquez sur **configurer** pour afficher une page de connexion.
 
   ![](media/FBCimage42.png)

3. Dans la zone ID de locataire, tapez ou collez l’ID de votre client (que vous avez obtenu à l’étape 2). Dans la zone mot de passe, tapez ou collez le APISecretKey (que vous avez obtenu à l’étape 2), puis cliquez sur **définir les paramètres de configuration** pour afficher la page Détails de la **configuration** .

    ![](media/FBCimage43.png)


4. Sous **Détails**de la configuration, entrez les paramètres de configuration suivants 

   - **ID d’application Facebook** : ID d’application pour l’application Facebook que vous avez obtenue à l’étape 5.
   - **Clé d’application Facebook** : la clé secrète de l’application Facebook que vous avez obtenue à l’étape 5.
   - **Contrôle** des webhooks Facebook: le jeton de vérification que vous avez créé à l’étape 5.
   - **ID d’application AAD** : ID d’application pour l’application Azure Active Directory que vous avez créée à l’étape 2.
   - **Clé secrète de l’application AAD** : valeur de la clé secrète APISecretKey que vous avez créée à l’étape 4.
   - **URI de l’application AAD** : URI de l’application AAD obtenue à l’étape 2; par exemple, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.
   - **Clé d’instrumentation Insights** de l’application-laissez cette zone vide.

5. Cliquez sur **Enregistrer** pour enregistrer les paramètres du connecteur.

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a>Étape 7: configurer un connecteur personnalisé dans le centre de sécurité & Compliance Center

1. Accédez à <https://protection.office.com> , puis cliquez sur importation de la **gouvernance \> des données \> importer des données**tierces.

   ![](media/FBCimage44.png)

2.  Cliquez sur **Ajouter un connecteur** , puis sur **pages Facebook**.

    ![](media/FBCimage46.png)

3.  Dans la page **Ajouter une application connecteur** , entrez les informations suivantes, puis cliquez sur **valider le connecteur**.

    - Dans la première zone, tapez un nom pour le connecteur, tel que **Facebook**.
    - Dans la deuxième zone, tapez ou collez la valeur du APISecretKey que vous avez ajouté à l’étape 4.
    - Dans la troisième zone, tapez ou collez l’URL du service d’application Azure; par exemple **https://fbconnector.azurewebsites.net**.
 
    Une fois le connecteur validé, cliquez sur **suivant**.
    
    ![](media/FBCimage47.png)

4.  Cliquez sur **connexion avec application connecteur**.

    ![](media/FBCimage45.png)

5. Tapez ou collez à nouveau le APISecretKey, puis cliquez sur **connexion au service connecteur**.

   ![](media/FBCimage48.png)


6. Cliquez sur **connexion avec Facebook.**

   ![](media/FBCimage49.png)

7. Sur la page **se connecter à Facebook** , connectez-vous à l’aide des informations d’identification du compte pour les pages de l’entreprise Facebook de votre organisation. Vérifiez que le compte Facebook auquel vous êtes connecté se voit attribuer le rôle d’administrateur pour les pages d’entreprise Facebook de votre organisation.

   ![](media/FBCimage50.png)

8. Cliquez sur **Sélectionner les pages** pour choisir les pages professionnelles de votre organisation que vous souhaitez archiver dans Office 365.

   ![](media/FBCimage51.png)

9. Une liste des pages d’entreprise gérées par le compte Facebook auquel vous vous êtes connecté s’affiche. Sélectionnez la page à archiver, puis cliquez sur **Enregistrer**.

    ![](media/FBCimage52.png)

10. Cliquez sur **Terminer** pour quitter le programme d’installation de l’application de service connecteur.

    ![](media/FBCimage53.png)

11. Sur la page **définir les filtres** , vous pouvez appliquer un filtre pour importer (et archiver) les éléments qui sont un certain âge. Cliquez sur **Suivant**.

    ![](media/FBCimage54.png)

12. Sur la page **définir le compte de stockage** , sélectionnez la boîte aux lettres Office 365 dans laquelle les éléments des pages Facebook de l’entreprise que vous avez sélectionnées seront importés.

    ![](media/FBCimage55.png)

13. Vérifiez vos paramètres, puis cliquez sur **Terminer** pour terminer l’installation du connecteur dans le centre de sécurité _AMP_ Compliance Center.

    ![](media/FBCimage56.png)

14. Accédez à la page **données** tierces d’archivage pour voir la progression du processus d’importation.

    ![](media/FBCimage58.png)
