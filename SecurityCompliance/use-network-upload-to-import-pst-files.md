---
title: Utiliser le chargement réseau pour importer les fichiers PST de votre organisation vers Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: 'Pour les administrateurs: Découvrez comment utiliser le chargement réseau pour importer en bloc plusieurs fichiers PST dans des boîtes aux lettres utilisateur dans Office 365.'
ms.openlocfilehash: 73123d5f36a01b31cfc38e6404bd400bb722fb36
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958575"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>Utiliser le chargement réseau pour importer les fichiers PST de votre organisation vers Office 365

> [!NOTE]
> Cet article est destiné aux administrateurs. Vous souhaitez importer des fichiers PST dans votre propre boîte aux lettres ? Voir [importer le courrier, les contacts et le calendrier à partir d'un fichier. pst Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)
  
Voici les instructions pas à pas pour utiliser le chargement réseau pour importer en bloc plusieurs fichiers PST vers des boîtes aux lettres Office 365. Pour obtenir des questions fréquemment posées sur l'utilisation du chargement réseau pour importer des fichiers PST vers des boîtes aux lettres Office 365, consultez la rubrique [FAQ sur l'utilisation du chargement réseau pour importer des fichiers PST](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files).
  
[Étape 1: Copiez l'URL SAS et installez Azure AzCopy](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[Étape 2: chargement de vos fichiers PST dans Office 365](#step-2-upload-your-pst-files-to-office-365)

[Module Étape 3: afficher la liste des fichiers PST téléchargés vers Office 365](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Étape 4: créer le fichier de mappage d'importation PST](#step-4-create-the-pst-import-mapping-file)

[Étape 5: créer une tâche d'importation PST dans Office 365](#step-5-create-a-pst-import-job-in-office-365)

[Étape 6: filtrer les données et démarrer le travail d'importation PST](#step-6-filter-data-and-start-the-pst-import-job)

Notez que vous devez effectuer l'étape 1 une seule fois pour importer des fichiers PST dans des boîtes aux lettres Office 365. Après avoir effectué ces étapes, suivez les étapes 2 à 6 chaque fois que vous souhaitez télécharger et importer un lot de fichiers PST.

## <a name="before-you-begin"></a>Avant de commencer
  
- Vous devez disposer du rôle d'exportation d'importation de boîte aux lettres dans Exchange Online pour importer des fichiers PST dans des boîtes aux lettres Office 365. Par défaut, ce rôle n'est affecté à aucun groupe de rôles dans Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. Pour plus d'informations, consultez les sections «ajouter un rôle à un groupe de rôles» ou «créer un groupe de rôles» dans [gérer des groupes de rôles](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    De plus, pour créer des travaux d'importation dans le centre de sécurité & Compliance Center, l'une des conditions suivantes doit être vraie:
    
  - Vous devez disposer du rôle destinataires de messagerie dans Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Ou
    
  - Vous devez être un administrateur général dans votre organisation Office 365.
    
  > [!TIP]
    > EnVisagez de créer un nouveau groupe de rôles dans Exchange Online spécialement destiné à l'importation de fichiers PST dans Office 365. Pour le niveau minimal de privilèges requis pour importer des fichiers PST, attribuez les rôles importation de boîte aux lettres et destinataires des messages au nouveau groupe de rôles, puis ajoutez des membres. 
  
- La seule méthode prise en charge pour l'importation de fichiers PST dans Office 365 consiste à utiliser l'outil AzCopy d'Azure, comme décrit dans cette rubrique. Vous ne pouvez pas utiliser l'Explorateur de stockage Azure pour télécharger des fichiers PST directement dans la zone de stockage Azure.
    
- Vous devez stocker les fichiers PST que vous souhaitez importer vers Office 365 sur un serveur de fichiers ou un dossier partagé de votre organisation. À l'étape 2, vous allez exécuter l'outil Azure AzCopy qui télécharge les fichiers PST stockés sur ce serveur de fichiers ou dossier partagé vers Office 365.
    
- Cette procédure implique la copie et l'enregistrement d'une copie d'une URL qui contient une touche d'accès. Ces informations seront utilisées à l'étape 2 pour télécharger vos fichiers PST, et à l'étape 3 Si vous souhaitez afficher la liste des fichiers PST téléchargés vers Office 365. Veillez à prendre des précautions pour protéger cette URL, comme vous le feriez pour protéger les mots de passe ou d'autres informations relatives à la sécurité. Par exemple, vous pouvez l'enregistrer dans un document Microsoft Word protégé par mot de passe ou sur un lecteur USB chiffré. Consultez la section [more information](#more-information) pour obtenir un exemple de cette combinaison d'URL et de clé. 
    
- Vous pouvez importer des fichiers PST dans une boîte aux lettres inactive dans Office 365. Pour ce faire, spécifiez le GUID de la boîte aux lettres inactive dans le `Mailbox` paramètre dans le fichier de mappage d'importation PST. Pour plus d'informations, rePortez-vous à l'étape 4 de l'onglet **instructions** de cette rubrique. 
    
- Dans un déploiement hybride Exchange, vous pouvez importer des fichiers PST dans une boîte aux lettres d'archivage informatique pour un utilisateur dont la boîte aux lettres principale est locale. Pour ce faire, procédez comme suit dans le fichier de mappage d'importation PST:
    
  - Spécifiez l'adresse de messagerie de la boîte aux lettres locale de l' `Mailbox` utilisateur dans le paramètre. 
    
  - Spécifiez la valeur **true** dans `IsArchive` le paramètre. 
    
    Pour plus d'informations, consultez l' [étape 4](#step-4-create-the-pst-import-mapping-file) . 
    
- Une fois que les fichiers PST sont importés dans une boîte aux lettres Office 365, le paramètre de blocage de rétention de la boîte aux lettres est activé pour une durée indéterminée. Cela signifie que la stratégie de rétention attribuée à la boîte aux lettres ne sera pas traitée tant que vous n'aurez pas désactivé le blocage de rétention ou défini une date pour désactiver la conservation. Pourquoi effectuer cette opération? Si les messages importés dans une boîte aux lettres sont obsolètes, ils peuvent être supprimés définitivement (purgés) car leur période de rétention a expiré en fonction des paramètres de rétention configurés pour la boîte aux lettres. Lorsque la boîte aux lettres est mise en attente de rétention, le propriétaire de la boîte aux lettres peut gérer ces messages nouvellement importés ou modifier les paramètres de rétention pour la boîte aux lettres. Pour obtenir des suggestions sur la gestion du blocage de rétention, voir l'onglet **More info** dans cette rubrique. 
    
- Par défaut, la taille maximale des messages pouvant être reçus par une boîte aux lettres Office 365 est de 35 Mo. Cela est dû au fait que la valeur par défaut de la propriété *MaxReceiveSize* pour une boîte aux lettres est définie sur 35 Mo. Toutefois, la limite de la taille maximale des messages dans Office 365 est de 150 Mo. Par conséquent, si vous importez un fichier PST contenant un élément dont la taille est supérieure à 35 Mo, le service d'importation Office 365 modifiera automatiquement la valeur de la propriété *MaxReceiveSize* de la boîte aux lettres cible sur 150 Mo. Cela permet l'importation de messages allant jusqu'à 150 Mo dans les boîtes aux lettres utilisateur. 
    
    > [!TIP]
    > Pour identifier la taille de réception des messages pour une boîte aux lettres, vous pouvez exécuter cette commande dans `Get-Mailbox <user mailbox> | FL MaxReceiveSize`Exchange Online PowerShell:. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>Étape 1: Copiez l'URL SAS et installez Azure AzCopy

La première étape consiste à télécharger et à installer l'outil AzCopy d'Azure, qui est l'outil que vous exécuterez à l'étape 2 pour télécharger des fichiers PST vers Office 365. Vous copierez également l'URL SAS de votre organisation. Cette URL est une combinaison de l'URL réseau de l'emplacement de stockage Azure dans le Cloud Microsoft pour votre organisation et d'une clé SAS (Shared Access signature). Cette clé vous fournit les autorisations nécessaires pour télécharger des fichiers PST vers votre emplacement de stockage Azure. Veillez à prendre des précautions pour protéger l'URL SAS. Elle est propre à votre organisation et sera utilisée à l'étape 2.

> [!IMPORTANT]
> Pour importer des fichiers PST à l'aide de la méthode de chargement réseau, nous vous recommandons d'utiliser la version d'Azure AzCopy qui peut être téléchargée à l'étape 6B de la procédure suivante.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l'aide des informations d'identification d'un compte administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche du centre de sécurité & conformité, cliquez sur **importation**de la **gouvernance** \> de données.
    
    > [!NOTE]
    > Vous devez disposer des autorisations appropriées pour accéder à la page d' **importation** dans le centre de sécurité _AMP_ Compliance Center. Pour plus d'informations, rePortez-vous à la section **avant de commencer** . 
    
3. Sur la page **Importer** , cliquez ![sur Ajouter](media/ITPro-EAC-AddIcon.gif) une icône **nouveau travail d'importation**.
    
    L'Assistant importation de tâche s'affiche.
    
4. Tapez un nom pour le travail d'importation PST, puis cliquez sur **suivant**. Utilisez des lettres minuscules, des chiffres, des tirets et des traits de soulignement. Vous ne pouvez pas utiliser des lettres majuscules ou inclure des espaces dans le nom.
    
5. Sur la page **voulez-vous télécharger ou expédier les données?** , cliquez sur **télécharger vos données** , puis sur **suivant**.
    
    ![Cliquez sur charger vos données pour créer un travail d'importation de chargement réseau.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Sur la page **Importer les données** , procédez comme suit: 
    
    ![Copiez l'URL SAS et téléchargez l'outil AzCopy Azure sur la page importer les données.](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a. À l'étape 2, cliquez sur **afficher l'URL SAS de chargement réseau**. Une fois l'URL de la version SAS affichée, cliquez sur **copier dans le presse-papiers** , puis collez-la dans un fichier pour pouvoir y accéder ultérieurement.
    
    b. À l'étape 3, cliquez sur **Télécharger Azure AzCopy** pour télécharger et installer l'outil AzCopy Azure. Dans la fenêtre contextuelle, cliquez sur **exécuter** pour installer AzCopy. 
    
> [!NOTE]
> Vous pouvez laisser la page **Importer les données** ouverte (pour le cas où vous devriez recopier l'URL SAS) ou cliquer sur **Annuler** pour la fermer. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>Étape 2: chargement de vos fichiers PST dans Office 365

Vous êtes maintenant prêt à utiliser l'outil AzCopy. exe pour télécharger des fichiers PST dans Office 365. Cet outil les télécharge et les stocke dans un emplacement de stockage Azure dans le Cloud de Microsoft. Comme expliqué précédemment, l'emplacement de stockage Azure sur lequel vous chargez vos fichiers PST réside dans le même centre de Microsoft local que celui où se trouve votre organisation Office 365. Pour cela, les fichiers PST doivent se trouver sur un dossier partagé ou un serveur de fichiers dans votre organisation. Il s’agit du répertoire source mentionné dans la procédure suivante. Chaque fois que vous exécutez l'outil AzCopy, vous pouvez spécifier un autre répertoire source. 
  
1. Ouvrez une invite de commandes sur votre ordinateur local.
    
2. Accédez au répertoire où vous avez installé l’outil AzCopy.exe à l’étape 1. Si vous avez installé l'outil à l'emplacement par défaut, `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`accédez à.
    
3. Exécutez la commande suivante pour télécharger les fichiers PST vers Office 365.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    > [!IMPORTANT] 
    > Vous devez spécifier un répertoire comme emplacement source dans la commande précédente; vous ne pouvez pas spécifier un fichier PST individuel. Tous les fichiers PST dans le répertoire source seront téléchargés.
 
    Le tableau suivant décrit les paramètres AzCopy. exe et leurs valeurs requises. Les informations que vous avez obtenues à l'étape précédente sont utilisées dans les valeurs de ces paramètres.
    
    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Spécifie le répertoire source de votre organisation qui contient les fichiers PST qui seront chargés vers Office 365.  <br/> N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |Spécifie l'URL SAS que vous avez obtenue à l'étape 1.  <br/> N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/> **Conseil:** Module Vous pouvez spécifier un sous-dossier dans l'emplacement de stockage Azure dans lequel télécharger les fichiers PST. Pour ce faire, vous devez ajouter un emplacement de sous-dossier (après «ingestiondata») dans l'URL SAS. Le premier exemple ne spécifie pas un sous-dossier; Cela signifie que les fichiers PST seront téléchargés vers la racine (nommé *ingestiondata* ) de l'emplacement de stockage Azure. Le deuxième exemple télécharge les fichiers PST dans un sous-dossier (nommé *PSTFiles* ) à la racine de l'emplacement de stockage Azure.  <br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> Ou  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |Inscrit les messages de statut détaillés dans un fichier journal. Par défaut, le fichier journal détaillé est nommé AzCopyVerbose.log dans %LocalAppData%\Microsoft\Azure\AzCopy. Si vous spécifiez un emplacement de fichier existant pour cette option, le journal détaillé est ajouté au fichier.  <br/> N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |Ce commutateur facultatif spécifie le mode récursif de sorte que l'outil AzCopy copie les fichiers PST situés dans des sous-dossiers du répertoire source spécifié par le `/Source:` paramètre.  <br/> **Remarque:** Si vous incluez ce commutateur, les fichiers PST dans les sous-dossiers auront un nom de chemin d'accès de fichier différent dans l'emplacement de stockage Azure après leur téléchargement. Vous devrez spécifier le chemin d'accès exact du fichier dans le fichier CSV que vous créez à l'étape 4.  <br/> | `/S` <br/> |
    | `/Y` <br/> |Ce commutateur obligatoire permet l'utilisation de jetons SAS en écriture seule lorsque vous téléchargez les fichiers PST vers l'emplacement de stockage Azure. L'URL SAS que vous avez obtenue à l'étape 1 ( `/Dest:` et spécifiée dans le paramètre) est une URL SAS en écriture seule, c'est pourquoi vous devez inclure ce commutateur. Notez qu'une URL SAS en écriture seule ne vous empêchera pas d'utiliser l'Explorateur de stockage Azure pour afficher la liste des fichiers PST téléchargés vers l'emplacement de stockage Azure.  <br/> | `/Y` <br/> |
   
Voici un exemple de la syntaxe de l’outil AzCopy.exe qui reprend les valeurs réelles de chaque paramètre :
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

Une fois la commande exécutée, les messages d’état affichent la progression du processus de chargement des fichiers PST. Un message d’état final affiche le nombre total de fichiers qui ont été téléchargés. 

> [!TIP]
> Une fois que vous avez exécuté la commande AzCopy. exe et vérifié que tous les paramètres sont corrects, enregistrez une copie de la syntaxe de la ligne de commande dans le même fichier (sécurisé) où vous avez copié les informations obtenues à l'étape 1. Ensuite, vous pouvez copier et coller cette commande dans une invite de commandes chaque fois que vous souhaitez exécuter l'outil AzCopy. exe pour télécharger des fichiers PST vers Office 365. La seule valeur que vous devrez peut-être modifier sont celles du `/Source:` paramètre. Ceci dépend du répertoire source où se trouvent les fichiers PST.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Module Étape 3: afficher la liste des fichiers PST téléchargés vers Office 365

Au cours d'une étape facultative, vous pouvez installer et utiliser l'Explorateur de stockage Microsoft Azure (il s'agit d'un outil gratuit open source) pour afficher la liste des fichiers PST que vous avez téléchargés vers le BLOB Azure. Il existe deux raisons à le faire :
  
- Vérifiez que les fichiers PST du dossier partagé ou du serveur de fichiers de votre organisation ont bien été téléchargés vers le BLOB Azure.
    
- Vérifiez le nom de fichier (et le chemin d'accès du sous-dossier si vous en avez inclus un) pour chaque fichier PST téléchargé vers le BLOB Azure. Cela s’avère très utile lorsque vous créez le fichier mappage PST à l’étape suivante, car vous devez spécifier le chemin d’accès de dossier et le nom de fichier pour chaque fichier PST. La vérification de ces noms peut permettre de réduire les erreurs potentielles dans votre fichier de mappage PST.
    
L'Explorateur de stockage Microsoft Azure est en mode aperçu.
  
> [!IMPORTANT]
> Vous ne pouvez pas utiliser l'Explorateur de stockage Azure pour télécharger ou modifier des fichiers PST. La seule méthode prise en charge pour l'importation de fichiers PST dans Office 365 consiste à utiliser AzCopy. De plus, vous ne pouvez pas supprimer les fichiers PST que vous avez téléchargés vers le BLOB Azure. Si vous tentez de supprimer un fichier PST, vous recevrez une erreur indiquant que vous ne disposez pas des autorisations requises. Notez que tous les fichiers PST sont automatiquement supprimés de votre zone de stockage Azure. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created.
  
Pour installer Azure Storage Explorer et vous connecter à votre zone de stockage Azure:
  
1. Téléchargez et installez l' [outil Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Démarrez l'Explorateur de stockage Microsoft Azure, cliquez avec le bouton droit sur **comptes de stockage** dans le volet de gauche, puis cliquez sur **se connecter à Azure Storage**.
    
    ![Cliquez avec le bouton droit sur comptes de stockage, puis cliquez sur se connecter à Azure Storage](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Cliquez sur **utiliser une chaîne de connexion ou un URI SAS (Shared Access signature)** , puis cliquez sur **suivant**.
    
4. Cliquez sur **utiliser un URI SAS**, collez l'URL SAS que vous avez obtenue à l'étape 1 dans la zone sous **URI**, puis cliquez sur **suivant**.
    
5. Sur la page **Résumé de connexion** , vous pouvez passer en revue les informations de connexion, puis cliquer sur **se connecter**.
    
    Le conteneur **ingestiondata** est ouvert; Il contient les fichiers PST que vous avez téléchargés à l'étape 2. Le **conteneur ingestiondata** se trouve sous les **conteneurs BLOB** **de comptes** \> \> de **stockage** (services SAS). 
    
    ![L’explorateur de stockage Azure affiche la liste des fichiers PST que vous avez téléchargés](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Lorsque vous avez terminé d'utiliser l'Explorateur de stockage Microsoft Azure, cliquez avec le bouton droit sur **ingestiondata**, puis cliquez sur détacher pour vous déconnecter de votre zone de stockage Azure. **** Dans le cas contraire, vous recevrez une erreur la prochaine fois que vous tenterez de joindre un élément. 
    
    ![Cliquez avec le bouton droit de la souris sur ingestion, puis cliquez sur Détacher pour vous déconnecter de votre zone de stockage Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>Étape 4: créer le fichier de mappage d'importation PST

Une fois les fichiers PST téléchargés vers l'emplacement de stockage Azure de votre organisation Office 365, l'étape suivante consiste à créer un fichier de valeurs séparées par des virgules (CSV) qui spécifie les boîtes aux lettres utilisateur dans lesquelles les fichiers PST seront importés. Vous allez envoyer ce fichier CSV à l'étape suivante lors de la création d'une tâche d'importation PST.
  
1. [Téléchargez une copie du fichier de mappage d'importation PST](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
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
    La première ligne ou ligne d’en-tête du fichier CSV répertorie les paramètres qui seront utilisés par le service d’importation pour importer les fichiers PST dans les boîtes aux lettres d’utilisateur. Les noms des paramètres sont séparés par des virgules. Chaque ligne sous la ligne d’en-tête représente les valeurs des paramètres pour l’importation d’un fichier PST dans une boîte aux lettres spécifique. Vous aurez besoin d’une ligne pour chaque fichier PST que vous souhaitez importer dans une boîte aux lettres d’utilisateur. N’oubliez pas de remplacer les espaces réservés dans le fichier de mappage par les données réelles.

   **Remarque:** Ne modifiez rien dans la ligne d'en-tête, y compris les paramètres SharePoint; ils seront ignorés pendant le processus d'importation PST. 

 3. Utilisez les informations du tableau suivant pour remplir le fichier CSV avec les informations requises.


    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Spécifie le service Office 365 vers lequel les données seront importées. Pour importer des fichiers PST dans des boîtes aux lettres `Exchange`utilisateur, utilisez.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Spécifie l'emplacement du dossier dans l'emplacement de stockage Azure dans lequel vous avez téléchargé les fichiers PST à l'étape 2.  <br/> Si vous n'avez pas inclus de nom de sous-dossier facultatif dans l' `/Dest:` URL SAS dans le paramètre à l'étape 2, laissez ce paramètre vide dans le fichier CSV. Si vous avez inclus un nom de sous-dossier, spécifiez-le dans ce paramètre (voir le deuxième exemple). La valeur de ce paramètre est sensible à la casse.  <br/> Dans les deux cas, n'incluez *pas* «ingestiondata» dans `FilePath` la valeur du paramètre.  <br/><br/> **Important:** Le nom du chemin d'accès du fichier doit être identique à celui que vous avez utilisé si vous avez inclus un nom de sous-dossier facultatif dans l' `/Dest:` URL SAS dans le paramètre de l'étape 2. Par exemple, si vous avez `PSTFiles` utilisé pour le nom du sous-dossier à l'étape `pstfiles` 2, `FilePath` puis que vous utilisez dans le paramètre du fichier CSV, l'importation du fichier PST échouera. Veillez à utiliser la même casse dans les deux instances.  <br/> |(Laisser vide)  <br/> Ou  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |Indique le nom du fichier PST qui sera importé dans la boîte aux lettres d’utilisateur.  La valeur de ce paramètre est sensible à la casse.  <br/> <br/>**Important:** Le nom du fichier PST dans le fichier CSV doit être le même que celui du fichier PST qui a été téléchargé vers l'emplacement de stockage Azure à l'étape 2. Par exemple, si vous utilisez `annb.pst` le `Name` paramètre dans le fichier CSV, mais que le nom du fichier PST réel est `AnnB.pst`, l'importation de ce fichier PST échoue. Assurez-vous que le nom du fichier PST dans le fichier CSV utilise la même casse que le fichier PST réel.  <br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |Indique l’adresse de messagerie de la boîte aux lettres dans laquelle le fichier PST est importé.  Notez que vous ne pouvez pas spécifier un dossier public, car le service d’importation PST ne prend pas en charge l’importation de fichiers PST dans les dossiers publics.  <br/> Pour importer un fichier PST dans une boîte aux lettres inactive, vous devez spécifier le GUID de la boîte aux lettres de ce paramètre. Pour obtenir ce GUID, exécutez la commande PowerShell suivante dans Exchange Online:`Get-Mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> <br/>**Remarque:** Dans certains cas, vous pouvez avoir plusieurs boîtes aux lettres avec la même adresse de messagerie, où une boîte aux lettres est une boîte aux lettres active et l'autre est dans un état supprimé (ou inactif). Dans ce cas, vous devez spécifier le GUID de boîte aux lettres pour identifier de manière unique la boîte aux lettres dans laquelle importer le fichier PST. Pour obtenir ce GUID pour les boîtes aux lettres actives, exécutez la commande PowerShell `Get-Mailbox <identity of active mailbox> | FL Guid`suivante:. Pour obtenir le GUID des boîtes aux lettres supprimées (ou inactives), exécutez cette `Get-Mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`commande.  <br/> | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Indique si le fichier PST doit être importé dans la boîte aux lettres d’archivage de l’utilisateur. Il existe deux options :  <br/><br/>**False** -importe le fichier PST dans la boîte aux lettres principale de l'utilisateur.  <br/> **True** : importe le fichier PST dans la boîte aux lettres d'archivage de l'utilisateur. This assumes that the [user's archive mailbox is enabled](enable-archive-mailboxes.md). <br/><br/>Si vous définissez ce paramètre sur `TRUE` et que la boîte aux lettres d'archivage de l'utilisateur n'est pas activée, l'importation de cet utilisateur échoue. Notez que si une importation échoue pour un utilisateur (car son archive n'est pas activée et que cette propriété `TRUE`est définie sur), les autres utilisateurs de la tâche d'importation ne seront pas affectés.  <br/>  If you leave this parameter blank, the PST file is imported to the user's primary mailbox.  <br/> <br/>**Remarque:** Pour importer un fichier PST dans une boîte aux lettres d'archivage informatique pour un utilisateur dont la boîte aux lettres principale est locale `TRUE` , spécifiez simplement pour ce paramètre et spécifiez l'adresse de messagerie de la boîte aux `Mailbox` lettres locale de l'utilisateur pour le paramètre.  <br/> | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Spécifie le dossier de boîte aux lettres dans lequel le fichier PST est importé.  <br/>  Si vous laissez ce paramètre vide, le fichier PST sera importé dans un nouveau dossier nommé **** importés au niveau racine de la boîte aux lettres (le même niveau que le dossier boîte de réception et les autres dossiers de boîte aux lettres par défaut).  <br/>  Si vous spécifiez `/`, les éléments du fichier PST seront importés directement dans le dossier boîte de réception de l'utilisateur.  <br/><br/>  Si vous spécifiez `/<foldername>`, les éléments du fichier PST seront importés dans un dossier nommé * \<NomDossier\> * . Par exemple, si vous utilisez `/ImportedPst`, les éléments seraient importés dans un dossier nommé **ImportedPst**. Ce dossier sera situé dans la boîte aux lettres de l'utilisateur au même niveau que le dossier boîte de réception.  <br/><br/> **Conseil:** EnVisagez d'exécuter quelques lots de test pour tester ce paramètre afin de déterminer le meilleur emplacement de dossier dans lequel importer les fichiers PST.  <br/> |(Laisser vide)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Ce paramètre facultatif spécifie une valeur numérique pour la page de codes à utiliser pour l'importation des fichiers PST au format de fichier ANSI. Ce paramètre est utilisé pour l'importation de fichiers PST à partir d'organisations chinoises, japonaises et coréennes, car ces langues utilisent généralement un jeu de caractères DBCS (Double Byte Character Set) pour le codage des caractères. Si ce paramètre n'est pas utilisé pour importer des fichiers PST pour les langues qui utilisent des caractères DBCS pour les noms de dossier de boîte aux lettres, les noms de dossier sont souvent tronqués après leur importation.  <br/><br/> Pour obtenir la liste des valeurs prises en charge à utiliser pour ce paramètre, consultez la rubrique identificateurs de la [page de code](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> <br/>**Remarque:** Comme indiqué précédemment, il s'agit d'un paramètre facultatif et vous n'avez pas besoin de l'inclure dans le fichier CSV. Vous pouvez également l'inclure et laisser la valeur vide pour une ou plusieurs lignes.  <br/> |(Laisser vide)  <br/> Ou  <br/>  `932`(il s'agit de l'identificateur de page de code pour le japonais ANSI/OEM)  <br/> |
    | `SPFileContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPManifestContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPSiteUrl` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>Étape 5: créer une tâche d'importation PST dans Office 365

L'étape suivante consiste à créer le travail d'importation PST dans le service d'importation dans Office 365. Comme expliqué précédemment, vous allez envoyer le fichier de mappage d'importation PST que vous avez créé à l'étape 4. Une fois le nouveau travail créé, Office 365 analyse les données des fichiers PST, puis vous donne la possibilité de filtrer les données importées dans les boîtes aux lettres spécifiées dans le fichier de mappage d'importation PST (Voir l' [étape 6](#step-6-filter-data-and-start-the-pst-import-job)).
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l'aide des informations d'identification d'un compte administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche du centre de sécurité & conformité, cliquez sur **gouvernance des données** , puis sur **Importer**.
    
3. Sur la page **Importer** , cliquez ![sur Ajouter](media/ITPro-EAC-AddIcon.gif) une icône **nouveau travail d'importation**.
    
    **Remarque:** Vous devez disposer des autorisations appropriées pour accéder à la page d' **importation** dans le centre de sécurité _AMP_ Compliance Center pour créer une tâche d'importation. Pour plus d'informations, rePortez-vous à la section **avant de commencer** . 
    
4. Tapez un nom pour le travail d'importation PST, puis cliquez sur **suivant**. Utilisez des lettres minuscules, des chiffres, des tirets et des traits de soulignement. Vous ne pouvez pas utiliser des lettres majuscules ou inclure des espaces dans le nom.
    
5. Sur la page **voulez-vous télécharger ou expédier les données?** , cliquez sur **télécharger vos données** , puis sur **suivant**.
    
    ![Cliquez sur charger vos données pour créer un travail d'importation de chargement réseau.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. À l'étape 4 de la page **importer des données** , cliquez sur les cases à cocher j'ai effectué le **téléchargement des fichiers** et j'ai **accès au fichier de mappage** , puis cliquez sur **suivant**.
    
    ![Cliquez sur les deux cases à cocher à l'étape 4](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. Dans la page **Sélectionner le fichier de mappage** , cliquez sur **Sélectionner un fichier de mappage** pour soumettre le fichier de mappage d'importation PST que vous avez créé à l'étape 4. 
    
    ![Cliquez sur Sélectionner le fichier de mappage pour envoyer le fichier CSV que vous avez créé pour le travail d'importation.](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. Une fois le nom du fichier CSV affiché sous **nom du fichier de mappage**, cliquez sur **valider** pour vérifier que votre fichier CSV contient des erreurs. 
    
    ![Cliquez sur valider pour vérifier que le fichier CSV contient des erreurs.](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    Le fichier CSV doit être validé pour créer la tâche d’importation PST. Remarque le nom de fichier est changé en vert une fois qu'il a été validé. Si la validation échoue, cliquez sur le lien **afficher le journal** . Un rapport d'erreur de validation est ouvert, avec un message d'erreur pour chaque ligne du fichier ayant échoué. 
    
9. Une fois le fichier de mappage PST correctement validé, lisez le document conditions générales, puis cliquez sur la case à cocher.
    
10. Cliquez sur **Enregistrer** pour soumettre le travail, puis cliquez sur **Fermer** une fois le travail créé. 
    
    Une page de menu volant d'État s'affiche avec l'état **analyse en cours** et la nouvelle tâche d'importation s'affiche dans la liste sur la page d' **importation** . 
    
11. Cliquez **** ![sur Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) l'icône Actualiser pour mettre à jour les informations d'État affichées dans la colonne **État** . Lorsque l'analyse est terminée et que les données sont prêtes à être importées, l'État devient **analyse terminée**.
    
    Vous pouvez cliquer sur le travail d'importation pour afficher la page de menu volant d'État, qui contient des informations plus détaillées sur la tâche d'importation, telles que l'état de chaque fichier PST figurant dans le fichier de mappage.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Étape 6: filtrer les données et démarrer le travail d'importation PST

Après avoir créé le travail d'importation à l'étape 5, Office 365 analyse les données dans les fichiers PST (de manière sûre et sécurisée) en identifiant l'âge des éléments et les différents types de messages inclus dans les fichiers PST. Lorsque l'analyse est terminée et que les données sont prêtes à être importées, vous avez la possibilité d'importer toutes les données contenues dans les fichiers PST ou vous pouvez réduire les données importées en définissant des filtres qui contrôlent les données à importer.
  
1. Sur la page d' **importation** dans le centre de sécurité & conformité, cliquez sur **prêt pour importer vers Office 365** pour le travail d'importation que vous avez créé à l'étape 5. 
    
    ![Cliquez sur prêt pour importer vers Office 365 en regard de la tâche d'importation que vous avez créée.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Une page de survol s'affiche avec des informations sur les fichiers PST et d'autres informations sur la tâche d'importation.
    
2. Sur la page de menu volant, cliquez sur **importer vers Office 365**.
    
    La page **filtrer vos données** s'affiche. Elle contient les données fournies par l'analyse effectuée sur les fichiers PST par Office 365, y compris des informations sur l'ancienneté des données. À ce stade, vous avez la possibilité de filtrer les données qui seront importées ou d'importer toutes les données telles quelles. 
    
    ![Vous pouvez découper les données dans les fichiers PST ou les importer tout](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. Effectuez l’une des opérations suivantes :
    
    a. Pour découper les données que vous importez, cliquez sur **Oui, je veux les filtrer avant l'importation**.
    
    Pour obtenir des instructions détaillées détaillées sur le filtrage des données dans les fichiers PST et sur le démarrage de la tâche d'importation, voir [filtrer des données lors de l'importation de fichiers PST dans Office 365](filter-data-when-importing-pst-files.md).
    
    Ou
    
    b. Pour importer toutes les données des fichiers PST, cliquez sur **non, je veux tout importer,** puis cliquez sur **suivant**.
    
4. Si vous avez choisi d'importer toutes les données, cliquez sur **importer des données** pour démarrer le travail d'importation. 
    
    L'état de la tâche d'importation est affiché sur la page d' **importation** . Cliquez ![sur Actualiser l'icône](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour mettre à jour les informations d'État affichées dans la colonne **État** . Cliquez sur le travail d'importation pour afficher la page de menu volant d'État, qui affiche des informations sur l'état de chaque fichier PST importé. 

## <a name="how-the-import-process-works"></a>Fonctionnement du processus d'importation
  
Vous pouvez utiliser l'option de chargement réseau et le service d'importation Office 365 pour importer en bloc des fichiers PST dans des boîtes aux lettres utilisateur. Le chargement réseau signifie que vous téléchargez les fichiers PST dans une zone de stockage temporaire dans le Cloud de Microsoft. Le service d'importation Office 365 copie les fichiers PST de la zone de stockage vers les boîtes aux lettres des utilisateurs cibles.
  
Voici une illustration et une description du processus de chargement réseau pour importer des fichiers PST dans des boîtes aux lettres dans Office 365.
  
![Flux de travail du processus de chargement réseau pour importer des fichiers PST vers Office 365](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Téléchargez l'outil d'importation PST et la clé vers l'emplacement de stockage privé Azure** : la première étape consiste à télécharger l'outil de ligne de commande Azure AzCopy et à utiliser une clé d'accès pour télécharger les fichiers PST vers un emplacement de stockage Azure dans le Cloud Microsoft. Vous les obtenez à partir de la page d' **importation** dans le centre de sécurité _AMP_ Compliance Center. La clé (appelée clé de signature d'accès sécurisé (SAS) vous fournit les autorisations nécessaires pour télécharger des fichiers PST vers un emplacement de stockage Azure sécurisé et privé. Cette clé d'accès est propre à votre organisation et empêche tout accès non autorisé à vos fichiers PST une fois qu'ils sont téléchargés vers le Cloud Microsoft. Notez que l'importation de fichiers PST dans Office 365 ne nécessite pas que votre organisation dispose d'un abonnement Azure distinct. 
    
2. **Chargement des fichiers PST dans l'emplacement de stockage Azure** : l'étape suivante consiste à utiliser l'outil AzCopy. exe (téléchargé à l'étape 1) pour télécharger et stocker vos fichiers PST dans un emplacement de stockage Azure qui réside dans le même centre de Microsoft régional où votre Office 365 Organisation. Pour les télécharger, les fichiers PST que vous souhaitez importer vers Office 365 doivent être situés dans un partage de fichiers ou un serveur de fichiers de votre organisation.
    
    Notez qu'il existe une étape facultative que vous pouvez effectuer pour afficher la liste des fichiers PST une fois qu'ils sont téléchargés vers l'emplacement de stockage Azure.
    
3. **Créer un fichier de mappage d'importation PST** -une fois que les fichiers PST ont été téléchargés vers l'emplacement de stockage Azure, l'étape suivante consiste à créer un fichier de valeurs séparées par des virgules (CSV) qui spécifie les boîtes aux lettres d'utilisateur dans lesquelles les fichiers PST seront importés, Notez qu'un fichier PST peut être  importé dans la boîte aux lettres principale d'un utilisateur ou dans sa boîte aux lettres d'archivage. Le service d'importation Office 365 utilisera les informations du fichier CSV pour importer les fichiers PST.
    
4. **Créer une tâche d'importation PST** : l'étape suivante consiste à créer une tâche d'importation PST sur la page d' **importation** dans le centre de sécurité & Compliance Center et à envoyer le fichier de mappage d'importation PST créé à l'étape précédente. Après avoir créé la tâche d'importation, Office 365 analyse les données dans les fichiers PST, puis vous offre la possibilité de définir des filtres qui contrôlent les données importées dans les boîtes aux lettres spécifiées dans le fichier de mappage d'importation PST. 
    
5. **Filtrer les données PST qui seront importées dans des boîtes aux lettres** -après la création et le démarrage de la tâche d'importation, Office 365 analyse les données dans les fichiers PST (en toute sécurité et en toute sécurité) en identifiant l'âge des éléments et les différents types de messages inclus dans les fichiers PST. . Lorsque l'analyse est terminée et que les données sont prêtes à être importées, vous avez la possibilité d'importer toutes les données contenues dans les fichiers PST ou vous pouvez réduire les données importées en définissant des filtres qui contrôlent les données à importer.
    
6. **Démarrer le travail d'importation PST** : une fois la tâche d'importation démarrée, Office 365 utilise les informations du fichier de mappage d'importation PST pour importer les fichiers PST à partir de l'emplacement de stockage Azure vers les boîtes aux lettres utilisateur. Les informations d'État relatives à la tâche d'importation (y compris les informations relatives à chaque fichier PST importé) sont affichées dans la page d' **importation** dans le centre de sécurité _AMP_ Compliance Center. Une fois le travail d'importation terminé, l'état du travail est défini sur **terminé**.
  
## <a name="more-information"></a>Plus d’informations

- Pourquoi importer des fichiers PST vers Office 365?
    
  - Il s'agit d'un moyen efficace pour importer les données de messagerie d'archivage de votre organisation vers Office 365.
    
  - L’utilisateur peut accéder aux données à partir de n’importe quel périphérique, car elles sont stockées dans le cloud.
    
  - Elle permet de répondre aux besoins de conformité de votre organisation en vous permettant d'appliquer les fonctionnalités de conformité d'Office 365 aux données des fichiers PST que vous avez importés. Cela inclut les opérations suivantes :
    
  - Activation des [boîtes aux lettres](enable-archive-mailboxes.md) d'archivage et de [l'archivage à extension automatique](enable-unlimited-archiving.md) pour fournir aux utilisateurs un espace de stockage supplémentaire pour les boîtes aux lettres pour stocker les données que vous avez importées. 
    
  - Placer des boîtes aux lettres en [conservation pour litige](https://go.microsoft.com/fwlink/?linkid=856286) afin de conserver les données que vous avez importées. 
    
  - Utilisation des [Outils eDiscovery](search-for-content.md) de Microsoft pour rechercher les données que vous avez importées. 
    
  - Utilisation des stratégies de rétention d' [Office 365](retention-policies.md) pour contrôler la durée pendant laquelle les données que vous avez importées seront conservées, ainsi que les mesures à prendre après l'expiration de la période de rétention. 
    
  - Recherche dans le [Journal d'audit Office 365](search-the-audit-log-in-security-and-compliance.md) pour les événements liés aux boîtes aux lettres qui affectent les données que vous avez importées. 
    
  - Importation de données dans des [boîtes aux lettres](create-and-manage-inactive-mailboxes.md) inactives pour archiver des données à des fins de conformité. 
    
  - Utilisation des stratégies de protection contre la [perte de données](data-loss-prevention-policies.md) pour empêcher les données sensibles de fuir en dehors de votre organisation. 
  
- Voici un exemple de l'URL de signature d'accès partagé (SAS) obtenue à l'étape 1. Cet exemple contient également la syntaxe de la commande exécutée dans l'outil AzCopy. exe pour charger des fichiers PST dans Office 365. Veillez à prendre des précautions pour protéger l'URL SAS de la même manière que vous protégeriez les mots de passe ou d'autres informations relatives à la sécurité.

    ```
    SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D

    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y

    EXAMPLES

    This example uploads PST files to the root of the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
    
    This example uploads PST files to a subfolder named PSTFiles  in the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
``

- As previously explained, the Office 365 Import service turns on the retention hold setting (for an indefinite duration) after PST files are imported to a mailbox. This means the  *RetentionHoldEnabled*  property is set to  **True** so that the retention policy assigned to the mailbox won't be processed. This gives the mailbox owner time to manage the newly-imported messages by preventing a deletion or archive policy from deleting or archiving older messages. Here are some steps you can take to manage this retention hold: 
    
    - After a certain period of time, you can turn off the retention hold by running the **Set-Mailbox -RetentionHoldEnabled $false** command. For instructions, see [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
   - You can configure the retention hold so that it's turned off on some date in the future. You do this by running the **Set-Mailbox -EndDateForRetentionHold *date*** command. For example, assuming that today's date is June 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  **Set-Mailbox -EndDateForRetentionHold 7/1/2016**. In this scenario, you would leave the  **RetentionHoldEnabled**  property set to  *True*. For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
   - You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    
