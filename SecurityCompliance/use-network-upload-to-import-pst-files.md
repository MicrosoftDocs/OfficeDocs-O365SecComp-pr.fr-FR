---
title: Téléchargement du réseau permet d’importer des fichiers de votre organisation PST vers Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: 'Pour les administrateurs : Découvrez comment utiliser le téléchargement de réseau à plusieurs fichiers PST aux boîtes aux lettres utilisateur dans Office 365-importation en bloc.'
ms.openlocfilehash: c5bcaed9075939d098ac4bf9fbf4d8a94007232c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527854"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>Téléchargement du réseau permet d’importer des fichiers de votre organisation PST vers Office 365

> [!NOTE]
> Cet article est destiné aux administrateurs. Vous essayez d’importer des fichiers PST à votre propre boîte aux lettres ? Voir [messagerie importation, contacts et calendrier à partir d’un fichier Outlook .pst](https://go.microsoft.com/fwlink/p/?LinkID=785075)
  
Voici les instructions pas à pas requises pour utiliser le téléchargement de réseau à plusieurs fichiers PST aux boîtes aux lettres Office 365-importation en bloc. Pour des questions fréquemment posées sur l’utilisation de téléchargement du réseau pour l’importation en bloc des fichiers PST aux boîtes aux lettres Office 365, consultez le [FAQ pour l’utilisation de téléchargement réseau pour importer des fichiers PST](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files).
  
[Étape 1 : Copiez l’URL SAS et installer AzCopy Azure](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[Étape 2 : Télécharger vos fichiers PST vers Office 365](#step-2-upload-your-pst-files-to-office-365)

[(Facultatif) Étape 3 : Afficher une liste des fichiers PST téléchargé vers Office 365](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Étape 4 : Créer le fichier de mappage d’importation PST](#step-4-create-the-pst-import-mapping-file)

[Étape 5 : Créer une tâche d’importation PST dans Office 365](#step-5-create-a-pst-import-job-in-office-365)

[Étape 6 : Filtrer les données et démarrer le travail d’importation PST](#step-6-filter-data-and-start-the-pst-import-job)

Notez que vous devez effectuer l’étape 1 qu’une seule fois pour importer des fichiers PST aux boîtes aux lettres Office 365. Après avoir effectué ces étapes, suivez étape 2 à 6 à chaque fois que vous souhaitez télécharger et importer un lot de fichiers PST.

## <a name="before-you-begin"></a>Avant de commencer
  
- Vous devez être le rôle importer exporter des boîtes aux lettres dans Exchange Online pour importer des fichiers PST aux boîtes aux lettres Office 365. Par défaut, ce rôle n’est pas affecté à un groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle de boîte aux lettres importer exporter au groupe de rôles de gestion de l’organisation. Ou vous pouvez créer un nouveau groupe de rôles, attribuer le rôle de boîte aux lettres importer exporter et puis ajoutez-vous en tant que membre. Pour plus d’informations, voir le « ajouter un rôle à un groupe de rôles » ou les sections de la « créer un groupe de rôles » dans [Gérer les groupes de rôles](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    En outre, pour créer l’importation des travaux de sécurité Office 365 &amp; centre de conformité, une des opérations suivantes doivent être remplie :
    
  - Vous devez être affecté le rôle destinataires de messagerie dans Exchange Online. Par défaut, ce rôle est attribué aux groupes de rôles de gestion de l’organisation et la gestion des destinataires.
    
    Ou
    
  - Vous devez être un administrateur global dans votre organisation Office 365.
    
  > [!TIP]
    > Envisagez de créer un nouveau groupe de rôles dans Exchange Online est spécifiquement conçu pour l’importation des fichiers PST vers Office 365. Pour le niveau minimal de privilèges nécessaires pour importer des fichiers PST, attribuer les rôles destinataires de messagerie et de boîte aux lettres importer exporter vers le nouveau groupe de rôles et ajouter des membres. 
  
- La seule méthode prise en charge pour l’importation des fichiers PST vers Office 365 consiste à utiliser l’outil AzCopy Azure, comme décrit dans cette rubrique. Vous ne pouvez pas utiliser l’Explorateur de solutions de stockage Azure pour télécharger les fichiers PST directement à la zone de stockage Azure.
    
- Vous devez stocker les fichiers PST que vous souhaitez importer vers Office 365 sur un serveur de fichiers ou un dossier partagé dans votre organisation. À l’étape 2, vous allez exécuter l’outil de AzCopy Azure qui télécharge les fichiers PST qui sont stockées sur ce serveur de fichiers ou dossier à Office 365 partagé.
    
- Cette procédure consiste à copier et enregistrer une copie d’une URL qui contient une touche d’accès. Ces informations sont utilisées à l’étape 2 pour télécharger vos fichiers PST et à l’étape 3 Si vous souhaitez afficher la liste des fichiers PST téléchargé vers Office 365. N’oubliez pas de prendre des précautions pour protéger cette URL comme vous le feriez protéger les mots de passe ou d’autres informations relatives à la sécurité. Par exemple vous pourrez l’enregistrer à un document Microsoft Word protégés par mot de passe ou sur un lecteur USB chiffré. Voir que la section [plus d’informations](#more-information) pour obtenir un exemple de ce combinés URL et la clé. 
    
- Vous pouvez importer des fichiers PST à une boîte aux lettres inactive dans Office 365. Cela en spécifiant le GUID de la boîte aux lettres inactive dans le `Mailbox` paramètre dans le fichier de mappage d’importation PST. Sous l’onglet **Instructions** de cette rubrique pour plus d’informations, voir l’étape 4. 
    
- Dans un déploiement Exchange hybride, vous pouvez importer des fichiers PST à une boîte aux lettres d’archive en nuage pour un utilisateur de boîte aux lettres principale est local. Pour cela, procédez comme suit dans le fichier de mappage d’importation PST :
    
  - Spécifiez l’adresse de messagerie pour la boîte aux lettres locale de l’utilisateur dans le `Mailbox` paramètre. 
    
  - Spécifiez la valeur **TRUE** dans le `IsArchive` paramètre. 
    
    Pour plus d’informations, voir [l’étape 4](#step-4-create-the-pst-import-mapping-file) . 
    
- Une fois les fichiers PST sont importées dans une boîte aux lettres Office 365, le blocage de rétention définition pour la boîte aux lettres est activé pour une durée indéterminée. Cela signifie que la stratégie de rétention attribuée à la boîte aux lettres ne sera pas traitée jusqu'à ce que vous désactivez le blocage de rétention ou définissez une date pour désactiver le blocage. Pourquoi nous réalisons cela ? Si les messages importés dans une boîte aux lettres sont anciennes, ils peuvent définitivement supprimés (définitivement) parce que leur période de rétention a expiré en fonction des paramètres de rétention configurées pour la boîte aux lettres. Placer la boîte aux lettres sur le blocage de rétention vous donne le temps de propriétaire de boîte aux lettres de gérer ces messages nouvellement importées ou le permettent de modifier les paramètres de rétention pour la boîte aux lettres du temps. Consultez l’onglet **informations supplémentaires** dans cette rubrique pour obtenir des suggestions sur la gestion de la période de rétention. 
    
- Par défaut, la taille maximale des messages pouvant être reçus par une boîte aux lettres Office 365 est 35 Mo. C’est parce que la valeur par défaut de la propriété *MaxReceiveSize* pour une boîte aux lettres est définie à 35 Mo. Toutefois, la limite de taille maximale de message de réception dans Office 365 est de 150 Mo. Par conséquent, si vous importez un fichier PST contenant un élément plu de 35 Mo, le service Office 365 importer, nous allons modifier automatiquement la valeur de la propriété *MaxReceiveSize* sur la boîte aux lettres cible à 150 Mo. Cela permet aux messages de 150 Mo pour être importés dans les boîtes aux lettres utilisateur. 
    
    > [!TIP]
    > Pour identifier le message reçoit la taille d’une boîte aux lettres, vous pouvez exécuter cette commande dans Exchange Online PowerShell : `Get-Mailbox <user mailbox> | FL MaxReceiveSize`. 

### <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>Étape 1 : Copiez l’URL SAS et installer AzCopy Azure

La première étape consiste à télécharger et installer l’outil AzCopy Azure, qui est un outil qui vous allez exécuter à l’étape 2 pour télécharger des fichiers PST dans Office 365. Vous allez également copier l’URL SAS pour votre organisation. Cette URL est une combinaison de l’URL de réseau pour l’emplacement de stockage Azure dans le nuage Microsoft pour votre organisation et une clé de Signature de l’accès partagé (sa). Cette clé fournit des autorisations nécessaires pour télécharger des fichiers PST vers votre emplacement de stockage Azure. N’oubliez pas de prendre des précautions pour protéger l’URL SAS. Il est propre à votre organisation et sera utilisé à l’étape 2.
  
 **Important :** Nous recommandons d’utiliser version Azure AzCopy méthode de téléchargement 7.1.0 pour importer des fichiers PST à l’utilisation du réseau. Version 7.1.0 est téléchargée à l’étape 6 b dans la procédure suivante. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** \> **Import**.
    
    **Remarque :** Vous devez disposer des autorisations appropriées pour accéder à la page **d’importation** de la sécurité &amp; centre de conformité. Consultez la section **avant de commencer** , pour plus d’informations. 
    
3. Dans la page **Importer** , cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **nouvelle tâche d’importation**.
    
    L’Assistant Importation de travail s’affiche.
    
4. Tapez un nom pour la tâche d’importation PST, puis cliquez sur **suivant**. Utilisez les lettres minuscules, chiffres, des traits d’union et des traits de soulignement. Impossible d’utiliser des lettres majuscules ou inclure des espaces dans le nom.
    
5. Sur le **vous souhaitez télécharger ou envoyer des données ?** de page, cliquez sur **télécharger vos données** , puis sur **suivant**.
    
    ![Cliquez sur Télécharger vos données pour créer un téléchargement réseau tâche d’importation](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Dans la page **Importer des données** , effectuez le des deux opérations suivantes : 
    
    ![Copiez l’URL SAS et télécharger l’outil AzCopy Azure sur la page Importer des données](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a à l’étape 2, cliquez sur **Afficher les URL SAS de téléchargement réseau**. Une fois que l’URL SAS s’affiche, cliquez sur **Copier dans le Presse-papiers** et collez-le et enregistrez-le dans un fichier afin que vous pouvez y accéder ultérieurement.
    
    b à l’étape 3, cliquez sur **Télécharger un AzCopy Azure** pour télécharger et installer l’outil AzCopy Azure. Comme indiqué plus haut, version 7.1.0 sera téléchargée. Dans la fenêtre contextuelle, cliquez sur **exécuter** pour installer AzCopy. 
    
  **Remarque :** Vous pouvez laisser la page **Importer des données** open (au cas où vous devez copier de nouveau l’URL SAS) ou cliquez sur **Annuler** pour la fermer. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>Étape 2 : Télécharger vos fichiers PST vers Office 365

Vous êtes maintenant prêt à utiliser l’outil AzCopy.exe pour télécharger des fichiers PST vers Office 365. Cet outil télécharge et les stocke dans un emplacement de stockage Azure dans le nuage de Microsoft. Comme expliqué précédemment, l’emplacement de stockage Azure que vous téléchargez vos fichiers PST réside dans le même Microsoft Centre de données régional où se trouve votre organisation Office 365. Pour effectuer cette étape, les fichiers PST doivent se trouver dans un partage de fichiers ou un serveur de fichiers dans votre organisation. Il s’agit du répertoire source de la procédure suivante. Chaque fois que vous exécutez l’outil AzCopy, vous pouvez spécifier un répertoire source différents. 
  
1. Ouvrez une invite de commandes sur votre ordinateur local.
    
2. Accédez au répertoire où vous avez installé l’outil AzCopy.exe à l’étape 1. Si vous avez installé l’outil à l’emplacement par défaut, accédez à `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`.
    
3. Exécutez la commande suivante pour télécharger les fichiers PST vers Office 365.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    Le tableau suivant décrit les paramètres et leurs valeurs requises. Notez que les informations que vous avez obtenu à l’étape précédente sont utilisées dans les valeurs de ces paramètres.
    
    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Spécifie le répertoire source de votre organisation qui contient les fichiers PST qui seront téléchargés vers Office 365.  <br/> N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |Spécifie l’URL d’associations de sécurité que vous avez obtenu à l’étape 1.  <br/> N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/> **Conseil :** (Facultatif) Vous pouvez spécifier un sous-dossier à l’emplacement de stockage Azure pour télécharger les fichiers PST. Pour cela, en ajoutant un emplacement sous-dossier (après « ingestiondata ») dans l’URL SAS. Le premier exemple ne spécifie pas un sous-dossier ; Cela signifie que les fichiers PST sera téléchargé à la racine (appelée *ingestiondata* ) de l’emplacement de stockage Azure. Le deuxième exemple télécharge les fichiers PST dans un sous-dossier (nommé *PSTFiles* ) à la racine de l’emplacement de stockage Azure.<br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> Ou  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |Inscrit les messages de statut détaillés dans un fichier journal. Par défaut, le fichier journal détaillé est nommé AzCopyVerbose.log dans %LocalAppData%\Microsoft\Azure\AzCopy. Si vous spécifiez un emplacement de fichier existant pour cette option, le journal détaillé est ajouté au fichier.  <br/> N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |Ce commutateur facultatif spécifie le mode récursive afin que l’outil AzCopy copie les fichiers pst qui se trouvent dans des sous-dossiers dans le répertoire source spécifié par le `/Source:` paramètre.  <br/> **Remarque :** Si vous incluez ce commutateur, des fichiers PST dans les sous-dossiers a un chemin d’accès de fichier différent dans l’emplacement de stockage Azure après leur téléchargement. Vous devrez spécifier le chemin d’accès exact du fichier dans le fichier CSV que vous créez à l’étape 4.<br/> | `/S` <br/> |
    | `/Y` <br/> |Ce commutateur requis autorise l’utilisation de jetons SAS écriture seule lorsque vous téléchargez les fichiers PST à l’emplacement de stockage Azure. L’URL SAS obtenu à l’étape 1 (et spécifié dans `/Dest:` paramètre) est une URL SAS écriture seule, c’est pourquoi vous devez inclure ce commutateur. Notez qu’une URL SAS écriture seule n’empêche pas vous permet d’afficher une liste des fichiers PST téléchargés vers l’emplacement de stockage Azure à l’aide de l’Explorateur de solutions de stockage Azure.<br/> | `/Y` <br/> |
   
Voici un exemple de la syntaxe de l’outil AzCopy.exe qui reprend les valeurs réelles de chaque paramètre :
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

Une fois la commande exécutée, les messages d’état affichent la progression du processus de chargement des fichiers PST. Un message d’état final affiche le nombre total de fichiers qui ont été téléchargés. 
    
**Conseil :** Une fois que vous exécutez la commande AzCopy.exe de correctement et vérifiez que tous les paramètres sont corrects, enregistrer une copie de la syntaxe de ligne de commande pour le même fichier (sécurisée) où vous avez copié les informations obtenues à l’étape 1. Ensuite, vous pouvez copier et coller cette commande dans une invite de commandes chaque fois que vous souhaitez exécuter l’outil AzCopy.exe pour télécharger des fichiers PST vers Office 365. La seule valeur, vous devrez peut-être modifier sont ceux de la `/Source:` paramètre. Cela dépend du répertoire source où se trouvent les fichiers PST. 

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(Facultatif) Étape 3 : Afficher une liste des fichiers PST téléchargé vers Office 365

Comme une étape facultative, vous pouvez installer et utiliser Microsoft Azure stockage Explorer (qui est un outil gratuit, open source) pour afficher la liste des fichiers PST que vous avez téléchargée à l’objet blob Azure. Il existe deux raisons à cela :
  
- Vérifiez que les fichiers PST à partir du dossier partagé ou le serveur de fichiers dans votre organisation ont été correctement téléchargés vers l’objet blob Azure.
    
- Vérifiez le nom de fichier (et le chemin d’accès sous-dossier si vous avez inclus un) pour chaque fichier PST téléchargé vers l’objet blob Azure. Il s’agit très utile lorsque vous créez le fichier PST mappage du fichier à l’étape suivante, car vous devez spécifier le chemin d’accès du dossier et le nom de fichier pour chaque fichier PST. Vérification de ces noms permettent de réduire les erreurs dans votre fichier de mappage PST.
    
Microsoft Azure stockage Explorer est en mode Aperçu.
  
 **Important :** Vous ne pouvez pas utiliser l’Explorateur de solutions de stockage Azure pour télécharger ou modifier des fichiers PST. La seule méthode prise en charge pour l’importation des fichiers PST vers Office 365 consiste à utiliser AzCopy. En outre, vous ne pouvez supprimer les fichiers PST que vous avez téléchargée à l’objet blob Azure. Si vous essayez de supprimer un fichier PST, vous recevrez une erreur n’ayant ne pas les autorisations requises. Notez que tous les fichiers PST sont automatiquement supprimés de votre zone de stockage Azure. S’il y a aucune tâche d’importation en cours, puis tous les fichiers PST dans le ** ingestiondata ** conteneur sont supprimés de 30 jours après la dernière tâche d’importation a été créée. 
  
Pour installer l’Explorateur de solutions de stockage Azure et se connecter à votre zone de stockage Azure :
  
1. Téléchargez et installez l' [outil Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Démarrez l’Explorateur de stockage Microsoft Azure, cliquez sur **Comptes de stockage** dans le volet gauche, puis cliquez sur **se connecter au stockage Azure**.
    
    ![Comptes de stockage d’avec le bouton droit, puis cliquez sur se connecter au stockage Azure](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Cliquez sur **utiliser une chaîne de connexion ou URI de signature (sa) accès partagé** , cliquez sur **suivant**.
    
4. Cliquez sur **utiliser un URI SAS**, collez l’URL SAS que vous avez obtenu à l’étape 1 dans la zone sous **URI**, puis cliquez sur **suivant**.
    
5. Dans la page **Résumé de connexion** , vous pouvez passez en revue les informations de connexion, puis cliquez sur **se connecter**.
    
    Le conteneur **ingestiondata** est ouvert ; Il contient les fichiers PST que vous avez téléchargé à l’étape 2. Le conteneur **ingestiondata** se trouve sous les **Comptes de stockage** \> **(Services SAS-Attached)** \> **Conteneurs Blob**. 
    
    ![L’explorateur de stockage Azure affiche la liste des fichiers PST que vous avez téléchargés](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Lorsque vous avez terminé à l’aide de l’Explorateur de stockage Microsoft Azure, avec le bouton droit **ingestiondata**, puis cliquez sur **Détacher** de se déconnecter de votre zone de stockage Azure. Sinon, vous recevrez une erreur la prochaine fois que vous essayez de joindre. 
    
    ![Cliquez avec le bouton droit de la souris sur ingestion, puis cliquez sur Détacher pour vous déconnecter de votre zone de stockage Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>Étape 4 : Créer le fichier de mappage d’importation PST

Une fois que les fichiers PST ont été téléchargés à l’emplacement de stockage Azure pour votre organisation Office 365, l’étape suivante consiste à créer une virgule séparés fichier CSV (valeurs) qui spécifie les boîtes aux lettres utilisateur les fichiers PST sera importés à. Vous allez envoyer ce fichier CSV dans l’étape suivante lorsque vous créez une tâche d’importation PST.
  
1. [Téléchargez une copie du fichier de mappage importation PST](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
2. Ouvrez ou enregistrez le fichier CSV sur votre ordinateur local. L’exemple suivant montre le contenu d’un fichier de mappage d’importation PST (ouvert dans le Bloc-notes). Utilisez plutôt Microsoft Excel pour modifier le fichier CSV.


    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,,annb.pst,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,annb_archive.pst,annb@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,,donh.pst,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,donh_archive.pst,donh@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,PSTFiles,pilarp.pst,pilarp@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,PSTFiles,pilarp_archive.pst,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,PSTFiles,tonyk.pst,tonyk@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,PSTFiles,tonyk_archive.pst,tonyk@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,PSTFiles,zrinkam.pst,zrinkam@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,PSTFiles,zrinkam_archive.pst,zrinkam@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    ```
    La première ligne, ou ligne d’en-tête du fichier CSV répertorie les paramètres qui servira par le service d’importation PST pour importer les fichiers PST vers les boîtes aux lettres. Nom de chaque paramètre est séparée par une virgule. Chaque ligne sous la ligne d’en-tête représente les valeurs des paramètres d’importation d’un fichier PST dans une boîte aux lettres spécifique. Vous aurez besoin une ligne pour chaque fichier PST que vous souhaitez importer dans une boîte aux lettres de l’utilisateur. Veillez à remplacer les données d’espace réservé dans le fichier de mappage de vos données réelles.

   **Remarque :** Ne modifiez rien dans la ligne d’en-tête, y compris les paramètres de SharePoint ; elles seront ignorées pendant le processus d’importation PST. 

 3. Utilisez les informations du tableau suivant pour remplir le fichier CSV avec les informations requises.


    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Spécifie le service Office 365 pour les données seront importées. Pour importer des fichiers PST aux boîtes aux lettres de l’utilisateur, utilisez `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Spécifie l’emplacement du dossier à l’emplacement de stockage Azure que que vous avez téléchargé les fichiers PST à l’étape 2.  <br/> Si vous n’avez pas inclure un nom facultatif sous-dossier dans l’URL SAS dans le `/Dest:` paramètre à l’étape 2, laissez ce paramètre vide dans le fichier CSV. Si vous avez inclus un nom du sous-dossier, spécifier dans ce paramètre (voir le deuxième exemple). La valeur pour ce paramètre respecte la casse.<br/> Les deux cas, ** n’incluez pas « ingestiondata » dans la valeur de la `FilePath` paramètre.  <br/><br/> **Important :** Le cas pour le nom de chemin d’accès du fichier doit être identique à la casse utilisé si vous avez inclus un nom facultatif sous-dossier dans l’URL SAS dans le `/Dest:` paramètre à l’étape 2. Par exemple, si vous avez utilisé `PSTFiles` pour le sous-dossier de nom à l’étape 2 et ensuite utiliser `pstfiles` dans les `FilePath` paramètre dans le fichier CSV, l’importation du fichier PST échouera. Veillez à utiliser la même casse dans les deux instances.<br/> |(Laisser vide)  <br/> Ou  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |Spécifie le nom du fichier qui sera importé dans la boîte aux lettres de l’utilisateur. La valeur pour ce paramètre respecte la casse.<br/> <br/>**Important :** Le cas pour le nom de fichier PST dans le fichier CSV doit être la même que le fichier .pst qui a été téléchargé vers l’emplacement de stockage Azure à l’étape 2. Par exemple, si vous utilisez `annb.pst` dans les `Name` paramètre dans le fichier CSV, mais le nom du fichier PST réel est `AnnB.pst`, l’importation de ce fichier PST échouera. N’oubliez pas que le nom du fichier .pst dans le fichier CSV utilise la même casse que le fichier PST.<br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |Spécifie l’adresse de messagerie de la boîte aux lettres qui est importé dans le fichier PST. Notez que vous ne pouvez pas spécifier un dossier public, car le Service d’importation PST ne prend pas en charge l’importation de fichiers PST aux dossiers publics.<br/> Pour importer un fichier PST dans une boîte aux lettres inactive, vous devez spécifier la boîte aux lettres GUID pour ce paramètre. Pour obtenir ce GUID, exécutez la commande PowerShell suivante dans Exchange Online : « Get-Mailbox <identity of inactive mailbox> - InactiveMailboxOnly | Guid FL` <br/> <br/>**Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox<identity of active mailbox> | Guid FL`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-Mailbox <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | Guid FL ».  <br/> | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Indique si le fichier PST doit être importé dans la boîte aux lettres d’archivage de l’utilisateur. Il existe deux options :<br/><br/>**FALSE** - importe le fichier PST à la boîte aux lettres principale de l’utilisateur.  <br/> **TRUE** - importe le fichier PST boîte aux lettres d’archive de l’utilisateur. Cela suppose que [boîte aux lettres de l’utilisateur archive est activé](enable-archive-mailboxes.md).<br/><br/>Si vous définissez ce paramètre sur `TRUE` et boîte aux lettres de l’utilisateur archive n’est pas activé, l’importation de cet utilisateur échouera. Notez que si une importation échoue pour un utilisateur (étant donné que leur archivage n’est pas activé et que cette propriété est définie sur `TRUE`), les autres utilisateurs de la tâche d’importation ne sont pas affectées.<br/>  Si vous laissez ce paramètre vide, le fichier est importé dans la boîte aux lettres principale de l’utilisateur.  <br/> <br/>**Remarque :** Pour importer un fichier PST dans une boîte aux lettres d’archive en nuage pour un utilisateur de boîte aux lettres principale est locale, il suffit de spécifier `TRUE` pour ce paramètre et spécifiez l’adresse de messagerie pour la boîte aux lettres locale de l’utilisateur pour le `Mailbox` paramètre.  <br/> | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Spécifie le dossier de boîte aux lettres importé dans le fichier PST.  <br/>  Si vous laissez ce paramètre vide, le fichier PST est importé dans un nouveau dossier nommé **importés** situé à la racine de la boîte aux lettres (le même niveau que le dossier boîte de réception et les autres dossiers de boîte aux lettres par défaut).  <br/>  Si vous spécifiez `/`, éléments dans le fichier PST seront importées directement dans le dossier boîte de réception de l’utilisateur.  <br/><br/>  Si vous spécifiez `/<foldername>`, éléments dans le fichier PST seront importées dans un dossier nommé * \<foldername\> * . Par exemple, si vous utilisez `/ImportedPst`, éléments est importées dans un dossier nommé **ImportedPst**. Ce dossier sera situé dans la boîte aux lettres de l’utilisateur au même niveau que le dossier boîte de réception.<br/><br/> **Conseil :** Pensez à exécuter plusieurs lots de test pour tester ce paramètre afin de déterminer le meilleur emplacement de dossier pour importer des fichiers pst.  <br/> |(Laisser vide)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Ce paramètre facultatif spécifie une valeur numérique pour la page de codes à utiliser pour l’importation des fichiers PST dans le format de fichier ANSI. Ce paramètre est utilisé pour l’importation des fichiers PST d’organisations chinois, japonais et coréen (CJC), car ces langues utilisent généralement un jeu de caractères codés sur deux octets (DBCS) pour le codage de caractères. Si ce paramètre n’est pas utilisé pour importer des fichiers PST pour les langues qui utilisent DBCS pour les noms de dossier de boîte aux lettres, les noms de dossiers sont souvent tronqués après leur importation.<br/><br/> Pour obtenir la liste de valeurs prises en charge à utiliser pour ce paramètre, voir [Identificateurs de Page de Code](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> <br/>**Remarque :** Comme indiqué, ce paramètre est facultatif et n’avez pas à inclure dans le fichier CSV. Ou vous pouvez inclure et laissez la valeur vide pour une ou plusieurs lignes.<br/> |(Laisser vide)  <br/> Ou  <br/>  `932`(qui est l’identificateur de page de codes pour le japonais ANSI/OEM)  <br/> |
    | `SPFileContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPManifestContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPSiteUrl` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>Étape 5 : Créer une tâche d’importation PST dans Office 365

L’étape suivante consiste à créer le travail d’importation PST dans le service d’importation dans Office 365. Comme expliqué précédemment, vous envoyez le fichier de mappage d’importation PST que vous avez créé à l’étape 4. Après avoir créé le nouveau projet, Office 365 analyse les données dans les fichiers PST et vous donne la possibilité de filtrer les données qui obtient effectivement importées pour les boîtes aux lettres spécifiés dans le fichier de mappage d’importation PST (voir [l’étape 6](#step-6-filter-data-and-start-the-pst-import-job)).
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** , puis cliquez sur **Importer**.
    
3. Dans la page **Importer** , cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **nouvelle tâche d’importation**.
    
    **Remarque :** Vous devez disposer des autorisations appropriées pour accéder à la page **Importer** dans la sécurité &amp; centre de conformité pour créer une nouvelle tâche d’importation. Consultez la section **avant de commencer** , pour plus d’informations. 
    
4. Tapez un nom pour la tâche d’importation PST, puis cliquez sur **suivant**. Utilisez les lettres minuscules, chiffres, des traits d’union et des traits de soulignement. Impossible d’utiliser des lettres majuscules ou inclure des espaces dans le nom.
    
5. Sur le **vous souhaitez télécharger ou envoyer des données ?** de page, cliquez sur **télécharger vos données** , puis sur **suivant**.
    
    ![Cliquez sur Télécharger vos données pour créer un téléchargement réseau tâche d’importation](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. À l’étape 4 dans la page **Importer des données** , cliquez sur le **terminé téléchargement mes fichiers** et **je ont accès au fichier de mappage** de cases à cocher, puis cliquez sur **suivant**.
    
    ![Cliquez sur les deux cases à cocher à l’étape 4](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. Dans la page **Sélectionner le fichier de mappage** , cliquez sur **Sélectionner le fichier de mappage** pour envoyer le fichier de mappage d’importation PST que vous avez créé à l’étape 4. 
    
    ![Cliquez sur Sélectionnez un mappage un fichier pour envoyer le fichier CSV que vous avez créé pour la tâche d’importation](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. Après le nom de la CSV fichier s’affiche sous le **nom de fichier de mappage**, cliquez sur **Valider** pour vérifier votre fichier CSV pour les erreurs. 
    
    ![Cliquez sur Valider pour vérifier le fichier CSV pour les erreurs](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    Le fichier CSV doit être validés pour créer une tâche d’importation PST. Notez que le nom de fichier est devenu vert après sa validation avec succès. Si la validation échoue, cliquez sur le lien **Afficher le journal** . Un rapport d’erreurs de validation est ouvert, un message d’erreur pour chaque ligne dans le fichier qui a échoué. 
    
9. Une fois le fichier de mappage PST est validé avec succès, lire les termes et conditions, puis cliquez sur la case à cocher.
    
10. Cliquez sur **Enregistrer** pour soumettre le travail, puis cliquez sur **Fermer** une fois que le travail est créé avec succès. 
    
    Une page d’état flottant s’affiche, avec un état **d’analyse en cours** et la nouvelle tâche d’importation est affichée dans la liste dans la page **Importer** . 
    
11. Cliquez sur **Actualiser**![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations d’état qui s’affiche dans la colonne **état** . Lorsque l’analyse est terminée et les données sont prêtes à importer, l’état est modifiée pour **l’analyse terminée**.
    
    Vous pouvez cliquer sur la tâche pour afficher la page état flottant, qui contient des informations plus détaillées sur la tâche d’importation telles que l’état de chaque fichier PST répertorié dans le fichier de mappage d’importation.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Étape 6 : Filtrer les données et démarrer le travail d’importation PST

Après avoir créé la tâche d’importation à l’étape 5, Office 365 analyse les données dans les fichiers PST (de façon sécurisée) en identifiant l’âge des éléments et les différents types de messages inclus dans les fichiers PST. Lorsque l’analyse est terminée et que les données sont prêtes à importer, vous avez la possibilité d’importer toutes les données contenues dans les fichiers PST, ou vous pouvez ajuster les données importées en définissant des filtres qui déterminent quelles données obtient importées.
  
1. Dans la page **Importer** dans la sécurité &amp; centre de conformité, cliquez sur **prêt à importer dans Office 365** pour le travail d’importation que vous avez créé à l’étape 5. 
    
    ![Cliquez sur prêt à importer dans Office 365 en regard de la tâche d’importation que vous avez créé](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Une page brusque s’affiche avec des informations sur les fichiers PST et autres informations sur la tâche d’importation.
    
2. Dans la page mobile, cliquez sur **Importer à Office 365**.
    
    La page **Filtrer vos données** s’affiche. Il contient les détails de données résultant de l’analyse effectuée sur les fichiers PST par Office 365, notamment des informations sur l’âge des données. À ce stade, vous avez la possibilité pour filtrer les données qui seront importées ou importer toutes les données étant. 
    
    ![Vous pouvez ajuster les données dans les fichiers PST ou importer des](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. Effectuez l’une des opérations suivantes :
    
    r. pour découper les données que vous importez, cliquez sur **Oui, je veux filtrer avant l’importation**.
    
    Pour des instructions détaillées sur le filtrage des données dans les fichiers PST et avant de démarrer la tâche d’importation, voir [filtrer les données lors de l’importation des fichiers PST vers Office 365](filter-data-when-importing-pst-files.md).
    
    Ou
    
    b. pour importer toutes les données dans les fichiers PST, cliquez sur **non, je veux tout, importer** et cliquez sur **suivant**.
    
4. Si vous choisissez d’importer toutes les données, cliquez sur **Importer des données** pour démarrer la tâche d’importation. 
    
    L’état de la tâche d’importation est un affichage dans la page **Importer** . Cliquez sur ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour mettre à jour les informations d’état qui s’affiche dans la colonne **état** . Cliquez sur la tâche d’importation pour afficher la page état flottant, qui affiche les informations d’état sur chaque fichier PST à importer. 

## <a name="how-the-import-process-works"></a>Comment fonctionne le processus d’importation
  
Vous pouvez utiliser l’option de téléchargement de réseau et le service Office 365 importer pour l’importation en bloc des fichiers PST aux boîtes aux lettres de l’utilisateur. Téléchargement du réseau signifie que vous téléchargez les fichiers PST une zone de stockage temporaire dans le nuage de Microsoft. Le service Office 365 importation copie ensuite les fichiers PST à partir de la zone de stockage pour les boîtes aux lettres cible.
  
Voici une illustration et une description du processus de téléchargement de réseau pour importer des fichiers PST aux boîtes aux lettres dans Office 365.
  
![Télécharger des flux de travail du réseau de processus pour importer des fichiers PST vers Office 365](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Télécharger le fichier PST importer outil et l’emplacement de stockage Azure clé Private** - la première étape consiste à télécharger l’outil de ligne de commande AzCopy Azure et une touche d’accès utilisé pour télécharger les fichiers PST vers un emplacement de stockage Azure dans le nuage de Microsoft. Vous obtenez à partir de la page **Importer** de sécurité Office 365 &amp; centre de conformité. La clé (appelé une clé de signature (sa) d’un accès sécurisé, vous donne les autorisations nécessaires pour télécharger des fichiers PST à privé et sécuriser l’emplacement de stockage Azure. Cette clé d’accès est unique à votre organisation et permet d’empêcher tout accès non autorisé à vos fichiers PST après leur téléchargement vers le nuage Microsoft. Notez que l’importation de fichiers PST vers Office 365 ne nécessite pas votre organisation à un abonnement Azure distinct. 
    
2. **Télécharger les fichiers PST à l’emplacement de stockage Azure** - l’étape suivante consiste à utiliser l’outil AzCopy.exe (téléchargé à l’étape 1) pour télécharger et stocker vos fichiers PST dans un emplacement de stockage Azure qui réside dans le même centre de données Microsoft régional où Office 365 organisation se trouve. Pour les télécharger, les fichiers PST que vous souhaitez importer vers Office 365 doivent se trouver dans un partage de fichiers ou un serveur de fichiers dans votre organisation.
    
    Notez qu’il existe une étape facultative que vous pouvez effectuer pour afficher la liste des fichiers PST après leur téléchargement à l’emplacement de stockage Azure.
    
3. **Créer un fichier de mappage d’importation PST** - une fois les fichiers PST ont été téléchargés à l’emplacement de stockage Azure, l’étape suivante consiste à créer un fichier (CSV) de valeurs séparées par des virgules qui spécifie les boîtes aux lettres utilisateur les fichiers PST sera importées dans un fichier PST peut être  importées dans la boîte aux lettres principale d’un utilisateur ou de leur boîte aux lettres d’archive. Le service Office 365 importer utilisera les informations dans le fichier CSV pour importer les fichiers PST.
    
4. **Tâche d’importation de créer un fichier PST** - l’étape suivante consiste à créer une tâche d’importation PST dans la page **Importer** dans la sécurité &amp; centre de conformité et soumettre le fichier de mappage d’importation PST créé à l’étape précédente. Après avoir créé la tâche d’importation, Office 365 analyse les données dans les fichiers PST et vous donne la possibilité de définir des filtres qui déterminent quelles données obtient réellement importées pour les boîtes aux lettres spécifiés dans le fichier de mappage d’importation PST. 
    
5. **Filtre les données PST qui seront importées dans des boîtes aux lettres** - une fois la tâche d’importation est créée et lancée, Office 365 analyse les données dans les fichiers PST (en toute sécurité) en identifiant l’âge des éléments et les différents types de messages inclus dans les fichiers PST . Lorsque l’analyse est terminée et que les données sont prêtes à importer, vous avez la possibilité d’importer toutes les données contenues dans les fichiers PST, ou vous pouvez ajuster les données importées en définissant des filtres qui déterminent quelles données obtient importées.
    
6. **Démarrer le travail d’importation PST** - après le démarrage de la tâche d’importation, Office 365 utilise les informations dans le fichier de mappage d’importation PST pour importer les fichiers PST à partir de l’emplacement de stockage Azure annuel aux boîtes aux lettres de l’utilisateur. Informations de statut de la tâche d’importation (y compris les informations sur chaque fichier PST à importer) s’affiche dans la page **Importer** dans la sécurité &amp; centre de conformité. Lorsque la tâche d’importation est terminée, le statut de la tâche est défini sur **terminé**.
  
## <a name="more-information"></a>Plus d'informations

- Pourquoi importer des fichiers PST vers Office 365 ?
    
  - C’est un bon moyen pour importer les données de messagerie archivage de votre organisation vers Office 365.
    
  - L’utilisateur peut accéder aux données à partir de n’importe quel périphérique, car elles sont stockées dans le cloud.
    
  - Il permet de gérer les besoins de conformité de votre organisation en vous permettant d’appliquer des fonctionnalités de conformité d’Office 365 pour les données à partir des fichiers PST que vous avez importé. Cela inclut :
    
  - Activation des [boîtes aux lettres d’archive](enable-archive-mailboxes.md) et [Développer automatiquement l’archivage](enable-unlimited-archiving.md) pour permettre aux utilisateurs d’espace de stockage de boîte aux lettres supplémentaire pour les données que vous avez importé. 
    
  - Placer les boîtes aux lettres en [Litige](https://go.microsoft.com/fwlink/?linkid=856286) pour conserver les données que vous avez importé. 
    
  - À l’aide Microsoft [eDiscovery outils](search-for-content.md) pour rechercher les données que vous avez importé. 
    
  - À l’aide de [stratégies de rétention Office 365](retention-policies.md) pour contrôler la durée de conservation des données que vous avez importé et l’action à entreprendre après expiration de la période de rétention. 
    
  - Recherche dans [journal d’audit Office 365](search-the-audit-log-in-security-and-compliance.md) pour les événements liés à la boîte aux lettres qui affectent les données que vous avez importé. 
    
  - Importation de données de [boîtes aux lettres inactives](create-and-manage-inactive-mailboxes.md) pour archiver des données à des fins de conformité aux. 
    
  - À l’aide de [stratégies de protection contre la perte de données](data-loss-prevention-policies.md) pour empêcher les données sensibles d’une fuite en dehors de votre organisation. 
  
- Voici un exemple de l’URL de Signature de l’accès partagé (sa) est obtenue à l’étape 1. Cet exemple montre comment contient également la syntaxe de la commande que vous exécutez dans l’outil AzCopy.exe pour télécharger des fichiers PST dans Office 365. N’oubliez pas de prendre des précautions pour protéger l’URL SAS comme vous le feriez protéger les mots de passe ou d’autres informations relatives à la sécurité.

    ```
    SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D

    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y

    EXAMPLES

    This example uploads PST files to the root of the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
    
    This example uploads PST files to a subfolder named PSTFiles  in the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
``

- As previously explained, the Office 365 Import service turns on the retention hold setting (for an indefinite duration) after PST files are imported to a mailbox. This means the  *RetentionHoldEnabled*  property is set to  `True` so that the retention policy assigned to the mailbox won't be processed. This gives the mailbox owner time to manage the newly-imported messages by preventing a deletion or archive policy from deleting or archiving older messages. Here are some steps you can take to manage this retention hold: 
    
    - After a certain period of time, you can turn off the retention hold by running the  `Set-Mailbox -RetentionHoldEnabled $false` command. For instructions, see [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
   - You can configure the retention hold so that it's turned off on some date in the future. You do this by running the  `Set-Mailbox -EndDateForRetentionHold <date>` command. For example, assuming that today's date is July 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. In this scenario, you would leave the  *RetentionHoldEnabled*  property set to  *True*  . For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
   - You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    
