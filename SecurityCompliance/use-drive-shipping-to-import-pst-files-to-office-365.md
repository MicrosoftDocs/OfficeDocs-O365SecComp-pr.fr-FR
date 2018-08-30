---
title: Utiliser l’envoi de lecteur pour importer les fichiers de votre organisation PST vers Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 40829b57-793c-4d41-b171-e9270129173d
description: 'Pour les administrateurs : Apprenez à l’importation des fichiers PST de votre organisation aux boîtes aux lettres Office 365 en copiant des fichiers PST sur un disque dur, puis livraison à Microsoft. '
ms.openlocfilehash: ebe88918b6c25e18562db7817d22fbf71f05e4c7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528017"
---
# <a name="use-drive-shipping-to-import-your-organization-pst-files-to-office-365"></a>Utiliser l’envoi de lecteur pour importer les fichiers de votre organisation PST vers Office 365

**Cet article est destiné aux administrateurs. Vous essayez d’importer des fichiers PST à votre propre boîte aux lettres ? Voir [messagerie importation, contacts et calendrier à partir d’un fichier Outlook .pst](https://go.microsoft.com/fwlink/p/?LinkID=785075)**
   
Utilisez le service Office 365 importer et le lecteur d’expédition pour l’importation en bloc des fichiers PST aux boîtes aux lettres de l’utilisateur. Lecteur de transaction signifie que vous copiez les fichiers PST sur un disque dur et puis livrées physiquement le lecteur à Microsoft. Lorsque Microsoft reçoit votre disque dur, personnel du centre de données copie les données à partir du disque dur pour une zone de stockage dans le nuage Microsoft. Ensuite, vous avez la possibilité de supprimer les données PST ne sont réellement importées dans les boîtes aux lettres cible en définissant des filtres qui déterminent quelles données obtient importées. Après le démarrage de la tâche d’importation, le service d’importation importe les données de PST à partir de la zone de stockage pour les boîtes aux lettres utilisateur. Pour importer des fichiers PST vers les boîtes aux lettres à l’aide de livraison lecteur solution consiste à migrer la messagerie de votre organisation vers Office 365.
  
Voici les étapes nécessaires pour utiliser le lecteur d’expédition pour importer des fichiers PST aux boîtes aux lettres Office 365 :
  
[Étape 1 : Télécharger la clé de stockage d’informations sécurisé et l’outil d’importation PST](#step-1-download-the-secure-storage-key-and-pst-import-tool)

[Étape 2 : Copier les fichiers PST sur le disque dur](#step-2-copy-the-pst-files-to-the-hard-drive)

[Étape 3 : Créer le fichier de mappage d’importation PST](#step-3-create-the-pst-import-mapping-file)

[Étape 4 : Créer une tâche d’importation PST dans Office 365](#step-4-create-a-pst-import-job-in-office-365)

[Étape 5 : Expédier le disque dur à Microsoft](#step-5-ship-the-hard-drive-to-microsoft)

[Étape 6 : Filtrer les données et démarrer le travail d’importation PST](#step-6-filter-data-and-start-the-pst-import-job)
  
> [!IMPORTANT]
> Vous devez effectuer l’étape 1 une fois pour télécharger l’outil d’importation et de la clé de stockage d’informations sécurisé. Après avoir effectué ces étapes, suivez étape 2 à 6 à chaque fois que vous souhaitez envoyer un disque dur à Microsoft. 
  
Pour le Forum aux questions sur l’utilisation du lecteur pour importer des fichiers PST vers Office 365, voir les [questions fréquentes sur l’utilisation du lecteur pour importer des fichiers PST de l’envoi](faqimporting-pst-files-to-office-365.md#using-drive-shipping-to-import-pst-files)d’expédition. 
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être le rôle importer exporter des boîtes aux lettres dans Exchange Online pour importer des fichiers PST aux boîtes aux lettres Office 365. Par défaut, ce rôle n’est pas affecté à un groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle de boîte aux lettres importer exporter au groupe de rôles de gestion de l’organisation. Ou vous pouvez créer un nouveau groupe de rôles, attribuer le rôle de boîte aux lettres importer exporter et puis ajoutez-vous en tant que membre. Pour plus d’informations, voir le « ajouter un rôle à un groupe de rôles » ou les sections de la « créer un groupe de rôles » dans [Gérer les groupes de rôles](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    En outre, pour créer l’importation des travaux de sécurité Office 365 &amp; centre de conformité, une des opérations suivantes doivent être remplie :
    
  - Vous devez être affecté le rôle destinataires de messagerie dans Exchange Online. Par défaut, ce rôle est attribué aux groupes de rôles de gestion de l’organisation et la gestion des destinataires.
    
    Ou
    
  - Vous devez être un administrateur global dans votre organisation Office 365.
    
    > [!TIP]
    > Envisagez de créer un nouveau groupe de rôles dans Exchange Online est spécifiquement conçu pour l’importation des fichiers PST vers Office 365. Pour le niveau minimal de privilèges nécessaires pour importer des fichiers PST, attribuer les rôles destinataires de messagerie et de boîte aux lettres importer exporter vers le nouveau groupe de rôles et ajouter des membres. 
  
- Vous devez stocker les fichiers PST que vous souhaitez copier sur un disque dur sur un serveur de fichiers ou un dossier partagé dans votre organisation. À l’étape 2, vous allez exécuter l’outil d’Azure importer exporter (WAImportExport.exe) qui copie les fichiers PST qui sont stockées sur ce serveur de fichiers ou un dossier sur le disque dur partagé.
    
- Uniquement de 2,5 pouces à semi-conducteurs (SSD) des lecteurs ou 2,5 ou 3,5 pouces SATA II/III des disques durs internes sont prises en charge pour une utilisation avec le service Office 365 importation. Vous pouvez utiliser des disques durs jusqu'à 10 To. Pour les tâches d’importation, est traité uniquement le premier volume de données sur le disque dur. Le volume de données doit être au format NTFS. Lors de la copie des données sur un disque dur, vous pouvez joindre directement à l’aide d’un 2,5 pouces SSD 2,5 ou 3,5 pouces connecteur SATA II/III ou vous pouvez joindre en externe à l’aide d’un 2,5 pouces SSD externe ou 2,5 ou 3,5 adaptateur SATA II/III USB de pouce.
    
    > [!IMPORTANT]
    > Les disques durs externes qui sont fournis avec un adaptateur USB intégré ne sont pas pris en charge par le service Office 365 importation. En outre, le disque à l’intérieur de la casse d’un disque dur externe ne peut pas être utilisé. Veuillez ne pas envoyer des disques durs externes. 
  
- Le disque dur qui vous copiez les fichiers PST doit être chiffré avec BitLocker. L’outil WAImportExport.exe que vous exécutez à l’étape 2 vous aideront à configurer BitLocker. Il génère également une clé de chiffrement BitLocker Microsoft personnel du centre de données utilisera pour accéder au lecteur pour télécharger les fichiers PST vers la zone de stockage Azure dans le nuage de Microsoft.
    
- Lecteur de livraison est disponible via un Microsoft Enterprise accord. Lecteur de livraison n’est pas disponible par le biais de Microsoft Products Services contrat (MPSA).
    
- Le coût pour importer des fichiers PST aux boîtes aux lettres Office 365 utilisant l’envoi de lecteur est 2 dollars par Go de données. Par exemple, si vous livrez un disque dur qui contient les 1 000 Go (1 To) des fichiers PST, le coût est de 2 000 dollars. Vous pouvez travailler avec un partenaire pour régler les frais d’importation. Pour plus d’informations sur la recherche d’un partenaire, voir [Rechercher votre partenaire Office 365 ou un revendeur](https://go.microsoft.com/fwlink/p/?LinkId=785197).
    
- Vous, ou votre organisation, devez également disposer d’un compte auprès de FedEx ou DHL. 
    
  - Organisations des États-Unis, Brésil, Europe doivent disposer de comptes de FedEx.
    
  - Organisations de l’Asie de l’est, Asie du Sud-est, Japon, République de Corée et Australie doivent disposer de comptes DHL.
    
    Microsoft utilisera (et facturera) ce compte pour vous renvoyer le disque dur. 
    
- Il est possible que le disque dur que vous expédiez à Microsoft doive franchir des frontières internationales. Dans ce cas, vous devez vous assurer que le disque dur et les données qu’il contient sont importées et/ou exportées en conformité avec les lois applicables. Avant d’envoyer un disque dur, vérifiez auprès de vos conseillers juridiques que votre disque et vos données peuvent être légalement expédiés au centre de données Microsoft concerné. Cela permettra de garantir un délai de livraison raisonnable chez Microsoft.
    
- Cette procédure implique la copie et l’enregistrement d’une clé de stockage sécurisée et une clé de chiffrement BitLocker. N’oubliez pas de prendre des précautions pour protéger ces clés comme vous le feriez protéger les mots de passe ou d’autres informations relatives à la sécurité. Par exemple, vous pouvez les enregistrer dans un document Microsoft Word protégés par mot de passe ou les enregistrer sur un lecteur USB chiffré. Voir la section [plus d’informations](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) pour obtenir un exemple de ces clés. 
    
- Une fois les fichiers PST sont importées dans une boîte aux lettres Office 365, le blocage de rétention définition pour la boîte aux lettres est activé pour une durée indéterminée. Cela signifie que la stratégie de rétention attribuée à la boîte aux lettres ne sera pas traitée jusqu'à ce que vous désactivez le blocage de rétention ou définissez une date pour désactiver le blocage. Pourquoi nous réalisons cela ? Si les messages importés dans une boîte aux lettres sont anciennes, ils peuvent définitivement supprimés (définitivement) parce que leur période de rétention a expiré en fonction des paramètres de rétention configurées pour la boîte aux lettres. Placer la boîte aux lettres sur le blocage de rétention vous donne le temps de propriétaire de boîte aux lettres de gérer ces messages nouvellement importées ou le permettent de modifier les paramètres de rétention pour la boîte aux lettres du temps. Voir la section [plus d’informations](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) pour obtenir des suggestions sur la gestion de la période de rétention. 
    
- Par défaut, la taille maximale des messages pouvant être reçus par une boîte aux lettres Office 365 est 35 Mo. C’est parce que la valeur par défaut de la propriété *MaxReceiveSize* pour une boîte aux lettres est définie à 35 Mo. Toutefois, la limite de taille maximale de message de réception dans Office 365 est de 150 Mo. Par conséquent, si vous importez un fichier PST contenant un élément plu de 35 Mo, le service Office 365 importer, nous allons modifier automatiquement la valeur de la propriété *MaxReceiveSize* sur la boîte aux lettres cible à 150 Mo. Cela permet aux messages de 150 Mo pour être importés dans les boîtes aux lettres utilisateur. 
    
    > [!TIP]
    > Pour identifier le message reçoit la taille d’une boîte aux lettres, vous pouvez exécuter cette commande dans Exchange Online PowerShell : `Get-Mailbox <user mailbox> | FL MaxReceiveSize`. 
  
- Vous pouvez importer des fichiers PST à une boîte aux lettres inactive dans Office 365. Cela en spécifiant le GUID de la boîte aux lettres inactive dans le `Mailbox` paramètre dans le fichier de mappage d’importation PST. Voir [étape 3 : créer le fichier de mappage d’importation PST](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) pour plus d’informations. 
    
- Dans un déploiement Exchange hybride, vous pouvez importer des fichiers PST à une boîte aux lettres d’archive en nuage pour un utilisateur de boîte aux lettres principale est local. Pour cela, procédez comme suit dans le fichier de mappage d’importation PST :
    
  - Spécifiez l’adresse de messagerie pour la boîte aux lettres locale de l’utilisateur dans le `Mailbox` paramètre. 
    
  - Spécifiez la valeur **TRUE** dans le `IsArchive` paramètre. 
    
    Voir [étape 3 : créer le fichier de mappage d’importation PST](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) pour plus d’informations. 

## <a name="step-1-download-the-secure-storage-key-and-pst-import-tool"></a>Étape 1 : Télécharger la clé de stockage d’informations sécurisé et l’outil d’importation PST

La première étape consiste à télécharger la clé de stockage d’informations sécurisé et l’outil et que vous utiliserez à l’étape 2 pour copier les fichiers PST sur le disque dur.
  
> [!IMPORTANT]
> Vous devez utiliser la version de l’outil d’importation/exportation Azure 1 (WAimportExportV1) pour réussir à importer des fichiers PST à l’aide de la méthode de livraison de lecteur. Version 2 de l’outil d’importation/exportation Azure n’est pas pris en charge et l’utiliser entraînera incorrectement préparer le disque dur pour la tâche d’importation. N’oubliez pas de télécharger l’outil d’importation/exportation Azure à partir de la sécurité &amp; centre de conformité en suivant les procédures décrites dans cette étape. 
  
1. Accédez à [https://protection.office.com/](https://protection.office.com/) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** \> **Import**.
    
    > [!NOTE]
    > Comme indiqué plus haut, vous devez disposer des autorisations appropriées pour accéder à la page **d’importation** de la sécurité &amp; centre de conformité. 
  
3. Dans la page **Importer** , cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **nouvelle tâche d’importation**.
    
4. Dans l’Assistant Importation de projet, tapez un nom pour la tâche d’importation PST, puis cliquez sur **suivant**. Utilisez les lettres minuscules, chiffres, des traits d’union et des traits de soulignement. Impossible d’utiliser des lettres majuscules ou inclure des espaces dans le nom.
    
5. Dans la page **Choisissez Importer le type de travail** , cliquez sur les **disques durs destinataire à un de nos emplacements physiques** et puis cliquez sur **suivant**.
    
    ![Cliquez sur les disques durs destinataire à un de nos emplacements physiques pour créer un lecteur de travail d’importation de transaction](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. Dans la page **Importer des données** , effectuez le des deux opérations suivantes : 
    
    ![Copiez la clé de stockage sécurisée et télécharger l’outil Azure importer exporter sur la page Importer des données](media/e22e0b48-e5ce-48e0-95bc-0490a2b3b983.png)
  
    a à l’étape 2, cliquez sur **Copier la clé de stockage d’informations sécurisé**. Une fois la clé de stockage s’affiche, cliquez sur **Copier dans le Presse-papiers** et collez-le et enregistrez-le dans un fichier afin que vous pouvez y accéder ultérieurement.
    
    b à l’étape 3, **Téléchargez l’outil d’importation/exportation Azure** pour télécharger et installer l’outil d’importation/exportation Azure (version 1).
    
    - Dans la fenêtre contextuelle, cliquez sur **Enregistrer** \> **Enregistrer sous** pour enregistrer le fichier WaImportExportV1.zip dans un dossier sur votre ordinateur local. 
    
    - Extrayez le fichier WaImportExportV1.zip.
    
7. Cliquez sur **Annuler** pour fermer l’Assistant. 
    
    Vous devez revenir à la page **Importer** de la sécurité &amp; centre de conformité lors de la création de la tâche d’importation à l’étape 4. 

## <a name="step-2-copy-the-pst-files-to-the-hard-drive"></a>Étape 2 : Copier les fichiers PST sur le disque dur

L’étape suivante consiste à utiliser l’outil WAImportExport.exe pour copier des fichiers PST sur le disque dur. Cet outil chiffre le disque dur avec BitLocker, copie les fichiers pst sur le disque dur et crée un fichier journal qui stocke des informations sur le processus de copie. Pour effectuer cette étape, les fichiers PST doivent se trouver dans un partage de fichiers ou un serveur de fichiers dans votre organisation. Il s’agit du répertoire source de la procédure suivante. 
  
> [!IMPORTANT]
> Après avoir exécuté l’outil WAImportExport.exe la première fois un disque dur, vous devez utiliser une syntaxe différente chaque heure après cela. Cette syntaxe est expliquée à l’étape 4 de cette procédure pour copier des fichiers PST sur le disque dur. 
  
1. Ouvrez une invite de commandes sur votre ordinateur local.
    
    > [!TIP]
    > Si vous exécutez l’invite de commandes en tant qu’administrateur (en sélectionnant « Exécuter en tant qu’administrateur » quand vous l’ouvrez), la fenêtre d’invite de commandes affiche des messages d’erreur. Cela peut vous aider à résoudre les problèmes d’exécution de l’outil WAImportExport.exe. 
  
2. Accédez au répertoire où vous avez installé l’outil WAImportExport.exe à l’étape 1.
    
3. Exécutez la commande suivante lorsque vous utilisez l’outil WAImportExport.exe pour la première fois pour copier les fichiers PST sur un disque dur.

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requises. 
    
    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `/j:` <br/> |Indique le nom du fichier journal. Ce fichier est enregistré dans le dossier où se trouve l’outil WAImportExport.exe. Un fichier journal doit être créé sur chaque disque dur envoyé à Microsoft. Chaque fois que vous exécutez l’outil WAImportTool.exe pour copier des fichiers PST sur un disque dur, des informations sont ajoutées au fichier journal de ce disque. 
  <br/> Personnel du centre de données de Microsoft utilise les informations dans le fichier journal pour associer le disque dur à la tâche d’importation que vous créez à l’étape 4 et pour télécharger les fichiers PST vers la zone de stockage Azure dans le nuage de Microsoft.  <br/> | `/j:PSTHDD1.jrn` <br/> |
    | `/t:` <br/> |Indique la lettre de lecteur du disque dur quand celui-ci est connecté à votre ordinateur local.  <br/> | `/t:h` <br/> |
    | `/id:` <br/> |Indique le nom de la session de copie. Une session est définie dès que vous exécutez l’outil WAImportExport.exe pour copier des fichiers sur le disque dur. Les fichiers PST sont copiés dans un dossier portant le même nom que la session spécifiée par ce paramètre.   <br/> | `/id:driveship1` <br/> |
    | `/srcdir:` <br/> |Spécifie le répertoire source de votre organisation qui contient les fichiers PST qui seront copiés pendant la session. Veillez à mettre la valeur de ce paramètre avec des guillemets (« »).  <br/> | `/srcdir:"\\FILESERVER01\PSTs"` <br/> |
    | `/dstdir:` <br/> |Spécifie le répertoire de destination dans la zone de stockage Azure dans le nuage Microsoft où les fichiers PST sera téléchargé. Vous devez utiliser la valeur `ingestiondata/`. Veillez à mettre la valeur de ce paramètre avec des guillemets (« »).<br/> Si vous le souhaitez, vous pouvez également ajouter un chemin d’accès supplémentaires à la valeur de ce paramètre. Par exemple, vous pouvez utiliser le chemin d’accès de fichier du répertoire source sur le disque dur (converti en un format d’URL), qui est spécifié dans le `/srcdir:` paramètre. Par exemple, `\\FILESERVER01\PSTs` est remplacée par `FILESERVER01/PSTs`. Dans ce cas, vous toujours devez inclure `ingestiondata` dans le chemin d’accès du fichier. Dans cet exemple, la valeur de la `/dstdir:` paramètre serait `"ingestiondata/FILESERVER01/PSTs"`.<br/> Pour ajouter le chemin d’accès de fichier supplémentaire est si vous disposez des fichiers PST portant le même nom.  <br/> > [!NOTE]> Si vous incluez le chemin d’accès facultatif, l’espace de noms d’un fichier PST après son téléchargement à la zone de stockage Azure inclut le chemin d’accès et le nom du fichier PST. par exemple, `FILESERVER01/PSTs/annb.pst`. Si vous n’incluez pas un chemin d’accès, l’espace de noms est uniquement le nom de fichier PST ; par exemple `annb.pst`.           | `/dstdir:"ingestiondata/"` <br/> Ou  <br/>  `/dstdir:"ingestiondata/FILESERVER01/PSTs"` <br/> |
    | `/sk:` <br/> |Spécifie la clé de compte de stockage que vous avez obtenu à l’étape 1. Veillez à mettre la valeur de ce paramètre avec des guillemets (« »).  <br/> | `"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ=="` <br/> |
    | `/encrypt` <br/> |Ce commutateur active BitLocker pour le disque dur. Ce paramètre est obligatoire la première fois que vous exécutez l’outil WAImportExport.exe.  <br/> La clé de chiffrement BitLocker est copiée dans le fichier journal et le fichier journal qui est créé si vous utilisez le `/logfile:` paramètre. Comme expliqué précédemment, le fichier journal est enregistré dans le même dossier où se trouve l’outil WAImportExport.exe.<br/> | `/encrypt` <br/> |
    | `/logdir:` <br/> |Ce paramètre facultatif spécifie un dossier pour enregistrer les fichiers journaux. Le cas contraire, les fichiers journaux de sauvegarde sont dans le même dossier où se trouve l’outil WAImportExport.exe. Veillez à mettre la valeur de ce paramètre avec des guillemets (« »).  <br/> | `/logdir:"c:\users\admin\desktop\PstImportLogs"` <br/> |
   
    Voici un exemple de la syntaxe de l’outil WAImportExport.exe qui reprend les valeurs réelles de chaque paramètre :
    
    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER01\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"
    ```

    Une fois la commande exécutée, les messages d’état affichent la progression du processus de copie des fichiers PST sur le disque dur. Un message d’état final affiche le nombre total de fichiers qui ont été copiés. 
    
4. Exécutez cette commande chaque fois que vous exécutez l’outil WAImportExport.ext pour copier des fichiers PST sur le même disque dur.

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 
    ```

    Voici un exemple de la syntaxe pour copier ultérieurement des fichiers PST sur le même disque dur.  

    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER01\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```

## <a name="step-3-create-the-pst-import-mapping-file"></a>Étape 3 : Créer le fichier de mappage d’importation PST

Une fois que le personnel du centre de données Microsoft télécharger les fichiers PST à partir du disque dur pour la zone de stockage Azure, le service d’importation utilise les informations dans le fichier de mappage d’importation PST, qui est un fichier CSV (valeurs) séparés par des virgules, qui spécifie les boîtes aux lettres utilisateur le fichier PST les fichiers seront importées dans. Vous envoyez ce fichier CSV dans l’étape suivante lorsque vous créez une tâche d’importation PST.
  
1. [Téléchargez une copie du fichier de mappage importation PST](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
2. Ouvrez ou enregistrez le fichier CSV sur votre ordinateur local. L’exemple suivant montre le contenu d’un fichier de mappage d’importation PST (ouvert dans le Bloc-notes). Utilisez plutôt Microsoft Excel pour modifier le fichier CSV.

    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,FILESERVER01/PSTs,annb.pst,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,annb_archive.pst,annb@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,FILESERVER01/PSTs,donh.pst,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,donh_archive.pst,donh@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,FILESERVER01/PSTs,pilarp.pst,pilarp@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,pilarp_archive.pst,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,,tonyk.pst,tonyk@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,tonyk_archive.pst,tonyk@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,,zrinkam.pst,zrinkam@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,zrinkam_archive.pst,zrinkam@contoso.onmicrosoft.com,TRUE,,,,,
    ```

    La première ligne, ou ligne d’en-tête du fichier CSV répertorie les paramètres qui servira par le service d’importation PST pour importer les fichiers PST vers les boîtes aux lettres. Nom de chaque paramètre est séparée par une virgule. Chaque ligne sous la ligne d’en-tête représente les valeurs des paramètres d’importation d’un fichier PST dans une boîte aux lettres spécifique. Vous aurez besoin une ligne pour chaque fichier PST qui a été copié sur le disque dur. Veillez à remplacer les données d’espace réservé dans le fichier de mappage de vos données réelles.

    > [!NOTE]
    > Ne modifiez en aucun cas la ligne d’en-tête, ni les paramètres SharePoint ; ils seront ignorés pendant le processus d’importation des fichiers PST. 
  
3. Utilisez les informations du tableau suivant pour remplir le fichier CSV avec les informations requises.
    
    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Spécifie le service Office 365 pour les données seront importées. Pour importer des fichiers PST aux boîtes aux lettres de l’utilisateur, utilisez `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> | Spécifie l’emplacement du dossier dans la zone de stockage Azure fichiers PST sont copiées à lors de l’expédition du disque dur à Microsoft.  <br/>  Vous ajoutez dans cette colonne dans le fichier CSV dépend de ce que vous avez spécifié dans pour le `/dstdir:` paramètre à l’étape précédente.  <br/>  Si vous avez utilisé `/dstdir:"ingestiondata/"`, puis laissez ce paramètre vide dans le fichier CSV.  <br/>  Si vous avez inclus un chemin d’accès facultatif pour la valeur de la `/dstdir:` paramètre (par exemple, `/dstdir:"ingestiondata/FILESERVER01/PSTs"`, puis utiliser ce chemin d’accès (sans compter « ingestiondata ») pour ce paramètre dans le fichier CSV. La valeur pour ce paramètre respecte la casse.<br/>  Les deux cas, ** n’incluez pas « ingestiondata » dans la valeur de la `FilePath` paramètre. Laissez ce paramètre vide ou spécifiez uniquement le chemin d’accès facultatif.<br/> > [!IMPORTANT]> La casse pour le nom de chemin d’accès du fichier doit être la même casse que vous avez spécifié dans le `/dstdir:` paramètre à l’étape précédente. Par exemple, si vous avez utilisé `"ingestiondata/FILESERVER01/PSTs"` pour le nom du sous-dossier dans l’étape précédente, mais ensuite utilisé `fileserver01/psts` dans les `FilePath` paramètre dans le fichier CSV, l’importation du fichier PST échouera. Veillez à utiliser la même casse dans les deux instances.           |(Laisser vide)  <br/> Ou  <br/>  `FILESERVER01/PSTs` <br/> |
    | `Name` <br/> |Spécifie le nom du fichier qui sera importé dans la boîte aux lettres de l’utilisateur. La valeur pour ce paramètre respecte la casse.<br/> > [!IMPORTANT]> La casse pour le nom de fichier PST dans le fichier CSV doit être la même que le fichier .pst qui a été téléchargé vers l’emplacement de stockage Azure à l’étape 2. Par exemple, si vous utilisez `annb.pst` dans les `Name` paramètre dans le fichier CSV, mais le nom du fichier PST réel est `AnnB.pst`, l’importation de ce fichier PST échouera. N’oubliez pas que le nom du fichier .pst dans le fichier CSV utilise la même casse que le fichier PST.           | `annb.pst` <br/> |
    | `Mailbox` <br/> |Spécifie l’adresse de messagerie de la boîte aux lettres qui est importé dans le fichier PST. Notez que vous ne pouvez pas spécifier un dossier public, car le Service d’importation PST ne prend pas en charge l’importation de fichiers PST aux dossiers publics.<br/> Pour importer un fichier PST dans une boîte aux lettres inactive, vous devez spécifier la boîte aux lettres GUID pour ce paramètre. Pour obtenir ce GUID, exécutez la commande PowerShell suivante dans Exchange Online : « Get-Mailbox <identity of inactive mailbox> - InactiveMailboxOnly | Guid FL` <br/> > [!NOTE]> In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox<identity of active mailbox> | Guid FL`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command:  `Get-Mailbox <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | Guid FL ».           | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Indique si le fichier PST doit être importé dans la boîte aux lettres d’archivage de l’utilisateur. Il existe deux options :<br/> **FALSE** Importe le fichier PST à la boîte aux lettres principale de l’utilisateur.  <br/> **La valeur TRUE** Importe le fichier PST boîte aux lettres d’archive de l’utilisateur. Cela suppose que [boîte aux lettres de l’utilisateur archive est activé](enable-archive-mailboxes.md). Si vous définissez ce paramètre sur `TRUE` et boîte aux lettres de l’utilisateur archive n’est pas activé, l’importation de cet utilisateur échouera. Notez que si une importation échoue pour un utilisateur (étant donné que leur archivage n’est pas activé et que cette propriété est définie sur `TRUE`), les autres utilisateurs de la tâche d’importation ne sont pas affectées.<br/>  Si vous laissez ce paramètre vide, le fichier est importé dans la boîte aux lettres principale de l’utilisateur.  <br/> **Remarque :** Pour importer un fichier PST dans une boîte aux lettres d’archive en nuage pour un utilisateur de boîte aux lettres principale est locale, il suffit de spécifier `TRUE` pour ce paramètre et spécifiez l’adresse de messagerie pour la boîte aux lettres locale de l’utilisateur pour le `Mailbox` paramètre.  <br/> | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Spécifie le dossier de boîte aux lettres importé dans le fichier PST.  <br/>  Si vous laissez ce paramètre vide, le fichier PST est importé dans un nouveau dossier nommé **importés** situé à la racine de la boîte aux lettres (le même niveau que le dossier boîte de réception et les autres dossiers de boîte aux lettres par défaut).  <br/>  Si vous spécifiez `/`, éléments dans le fichier PST seront importées directement dans le dossier boîte de réception de l’utilisateur.  <br/>  Si vous spécifiez `/<foldername>`, éléments dans le fichier PST seront importées dans un dossier nommé * \<foldername\> * . Par exemple, si vous utilisez `/ImportedPst`, éléments est importées dans un dossier nommé **ImportedPst**. Ce dossier sera situé dans la boîte aux lettres de l’utilisateur au même niveau que le dossier boîte de réception.<br/> |(Laisser vide)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Ce paramètre facultatif spécifie une valeur numérique pour la page de codes à utiliser pour l’importation des fichiers PST dans le format de fichier ANSI. Ce paramètre est utilisé pour l’importation des fichiers PST d’organisations chinois, japonais et coréen (CJC), car ces langues utilisent généralement un jeu de caractères codés sur deux octets (DBCS) pour le codage de caractères. Si ce paramètre n’est pas utilisé pour importer des fichiers PST pour les langues qui utilisent DBCS pour les noms de dossier de boîte aux lettres, les noms de dossiers sont souvent tronqués après leur importation.<br/> Pour obtenir la liste de valeurs prises en charge à utiliser pour ce paramètre, voir [Identificateurs de Page de Code](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> > [!NOTE]> Comme indiqué, ce paramètre est facultatif et n’avez pas à inclure dans le fichier CSV. Ou vous pouvez inclure et laissez la valeur vide pour une ou plusieurs lignes.           |(Laisser vide)  <br/> Ou  <br/>  `932`(qui est l’identificateur de page de codes pour le japonais ANSI/OEM)  <br/> |
    | `SPFileContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPManifestContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPSiteUrl` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |

## <a name="step-4-create-a-pst-import-job-in-office-365"></a>Étape 4 : Créer une tâche d’importation PST dans Office 365

L’étape suivante consiste à créer le travail d’importation PST dans le service d’importation dans Office 365. Comme expliqué précédemment, vous envoyez le fichier de mappage d’importation PST que vous avez créé à l’étape 3. Après avoir créé la nouvelle tâche, le service d’importation utilisera les informations dans le fichier de mappage pour importer les fichiers PST vers la boîte aux lettres de l’utilisateur spécifié une fois que les fichiers PST sont copiés à partir du disque dur dans la zone de stockage Azure et que vous créez et lancez la tâche d’importation.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** , puis cliquez sur **Importer**.
    
3. Dans la page **Importer** , cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **nouvelle tâche d’importation**.
    
    > [!NOTE]
    > Comme indiqué plus haut, vous devez disposer des autorisations appropriées pour accéder à la page **d’importation** de la sécurité &amp; centre de conformité. 
  
4. Tapez un nom pour la tâche d’importation PST, puis cliquez sur **suivant**. Utilisez les lettres minuscules, chiffres, des traits d’union et des traits de soulignement. Impossible d’utiliser des lettres majuscules ou inclure des espaces dans le nom.
    
5. Dans la page **Choisissez Importer le type de travail** , cliquez sur les **disques durs destinataire à un de nos emplacements physiques** et puis cliquez sur **suivant**.
    
    ![Cliquez sur les disques durs destinataire à un de nos emplacements physiques pour créer un lecteur de travail d’importation de transaction](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. À l’étape 6, cliquez sur les cases à cocher **préparées mes disques durs et de l’ont accès aux fichiers de journal lecteur nécessaire** et **je ont accès au fichier de mappage** , puis cliquez sur **suivant**.
    
    ![Cliquez sur les deux cases à cocher à l’étape 6](media/fad43078-ea68-4acd-b2ed-75a800183262.png)
  
7. Dans la page **Sélectionnez le fichier de lecteur** , cliquez sur **Sélectionner le fichier de lecteur**, puis accédez au dossier même où se trouve l’outil WAImportExport.exe. Le fichier journal qui a été créé à l’étape 2 a été copié dans ce dossier.
    
    ![Cliquez sur fichier lecteur pour envoyer le fichier journal qui a été créé lorsque vous avez exécuté l’outil WAImportExport.exe](media/1ea35c04-bd88-4d7e-b7d9-dc390149d94f.png)
  
8. Sélectionnez le fichier journal ; par exemple, `PSTHDD1.jrn`.
    
    > [!TIP]
    > Lorsque vous avez exécuté l’outil WAImportExport.exe à l’étape 2, le nom du fichier journal a été spécifié par le `/j:` paramètre. 
  
9. Une fois que le nom du fichier lecteur apparaît sous le **nom de fichier lecteur**, cliquez sur **Valider** pour vérifier votre fichier lecteur pour les erreurs. 
    
    ![Cliquez sur Valider pour valider le fichier de lecteur que vous avez sélectionné](media/4b707f5a-152a-4e74-b9f5-449c88d1fec4.png)
  
    Le fichier de lecteur doit être validés pour créer une tâche d’importation PST. Notez que le nom de fichier est devenu vert après sa validation avec succès. Si la validation échoue, cliquez sur le lien **Afficher le journal** . Un rapport d’erreurs de validation est ouvert, un message d’erreur avec des informations sur la raison pour laquelle le fichier a échoué. 
    
    > [!NOTE]
    > Vous devez ajouter et valider un fichier journal pour chaque disque dur qu'envoyer à Microsoft. 
  
10. Après l’ajout et la validation d’un fichier journal pour chaque disque dur que vous allez envoyer à Microsoft, cliquez sur **suivant**.
    
11. Cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **Sélectionner le fichier de mappage** pour envoyer le fichier de mappage d’importation PST que vous avez créé à l’étape 3. 
    
    ![Cliquez sur Sélectionnez un mappage un fichier pour envoyer le fichier CSV que vous avez créé pour la tâche d’importation](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
12. Après le nom de la CSV fichier s’affiche sous le **nom de fichier de mappage**, cliquez sur **Valider** pour vérifier votre fichier CSV pour les erreurs. 
    
    ![Cliquez sur Valider pour vérifier le fichier CSV pour les erreurs](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    Le fichier CSV doit être validés pour créer une tâche d’importation PST. Notez que le nom de fichier est devenu vert après sa validation avec succès. Si la validation échoue, cliquez sur le lien **Afficher le journal** . Un rapport d’erreurs de validation est ouvert, un message d’erreur pour chaque ligne dans le fichier qui a échoué. 
    
13. Une fois le fichier de mappage PST est validé avec succès, cliquez sur **suivant**.
    
14. Dans la page de **fournir les informations de contact** , tapez vos informations de contact dans les zones concernées. 
    
    Notez que l’adresse de l’emplacement de Microsoft vous enverra vos disques durs est affiché. Cette adresse est généré automatiquement en fonction de votre centre de données Office 365. Copiez cette adresse dans un fichier ou prendre une capture d’écran.
    
15. Lire les termes et conditions, activez la case à cocher, puis cliquez sur **Enregistrer** pour soumettre le travail d’importation. 
    
    Une fois la tâche d’importation est correctement créée, une page d’état s’affiche indiquant les étapes du processus de livraison de lecteur.
    
16. Dans la page **Importer** , cliquez sur ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour affiché le nouveau lecteur transaction travail d’importation dans la liste des tâches d’importation. Notez que le statut est défini sur **en attente pour le numéro de suivi**. Vous pouvez également cliquer sur la tâche d’importation pour afficher la page état flottant, qui contient des informations plus détaillées sur la tâche d’importation.
 
## <a name="step-5-ship-the-hard-drive-to-microsoft"></a>Étape 5 : Expédier le disque dur à Microsoft

L’étape suivante consiste à envoyer le disque dur à Microsoft et ensuite fournir le numéro de suivi de l’expédition et retourner des informations d’expédition pour la tâche de transaction du lecteur. Une fois que le lecteur est reçu par Microsoft, il faudra entre 7 et 10 jours ouvrés pour les données personnel du centre de téléchargement de vos fichiers PST vers la zone de stockage Azure pour votre organisation.
  
> [!NOTE]
> Si vous ne fournissez pas le nombre de suivi et les informations d’expédition retour dans les 14 jours de la création de la tâche d’importation, le travail d’importation aura expiré. Dans ce cas, vous devrez créer un nouveau lecteur de travail d’importation de transaction (voir [étape 4 : créer une tâche d’importation PST dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step4)) et soumettre de nouveau le fichier de disque et le fichier de mappage d’importation PST. 
  
### <a name="ship-the-hard-drive"></a>Envoyer le disque dur

Gardez ces informations à l’esprit quand vous envoyez des disques durs à Microsoft :
  
- Ne pas envoyer l’adaptateur SATA-USB ; Vous ne devez expédier le disque dur.
    
- Emballez le disque dur correctement (par exemple, utilisez un sac anti-statique ou du papier bulle).
    
- Prenez le transporteur de votre choix pour envoyer le disque dur à Microsoft.
    
- Destinataire du disque dur vers l’adresse de l’emplacement de Microsoft qui a été affiché lorsque vous avez créé la tâche d’importation à l’étape 4. Veillez à inclure « Office 365 importation Service » dans l’adresse du destinataire.
    
- Une fois votre disque dur envoyé, pensez à noter le nom du transporteur et le numéro de suivi. Vous devrez les indiquer à l’étape suivante.
    
### <a name="enter-the-tracking-number-and-other-shipping-information"></a>Entrer le numéro de suivi et d’autres informations d’expédition

Une fois le disque dur envoyé à Microsoft, effectuez les étapes suivantes sur la page du service d’importation.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche, cliquez sur **la gouvernance des données** , puis cliquez sur **Importer**.
    
3. Dans la page **Importer** , cliquez sur le travail de l’expédition de lecteur que vous souhaitez entrer le numéro de suivi pour. 
    
4. Sur la page flottant état, cliquez sur **entrée suivi du numéro**.
    
5. Fournissez les informations suivantes :
    
1. **Opérateur de remise** Tapez le nom de l’opérateur de remise que vous avez utilisé pour envoyer le disque dur à Microsoft. 
    
2. **Numéro de suivi** Tapez le numéro de suivi de l’expédition du disque dur. 
    
3. **Numéro de compte transporteur de retour** Tapez le numéro de compte de votre organisation pour l’opérateur répertorié sous **renvoyer opérateur**. Microsoft utilise (et fixer) ce compte pour envoyer votre disque dur avec vous. Notez que les organisations des États-Unis pour l’Europe, doit posséder un compte avec FedEx. Les organisations en Asie et le reste du monde, doit posséder un compte avec DHL.
    
6. Cliquez sur **Enregistrer** pour enregistrer ces informations pour la tâche d’importation. 
    
    Dans la page **Importer** , cliquez sur ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour mettre à jour les informations de votre lecteur de travail d’importation de transaction. Notez que l’état est maintenant définie sur **des lecteurs en transit**.

## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Étape 6 : Filtrer les données et démarrer le travail d’importation PST

Une fois que votre disque dur est reçu par Microsoft, l’état de la tâche d’importation dans la page **Importer** devient **lecteurs reçu**. Personnel du centre de données utilise les informations dans le fichier journal pour télécharger vos fichiers PST vers la zone de stockage Azure pour votre organisation. À ce stade, le statut devient **importation en cours**. Comme indiqué précédemment, il faudra entre 7 à 10 jours après réception de votre disque dur pour télécharger les fichiers PST.
  
Une fois les fichiers PST sont téléchargées vers Azure, l’état est modifiée à **l’analyse en cours**. Cela indique que Office 365 analyse des données dans les fichiers PST (de façon sécurisée) pour identifier l’âge des éléments et les différents types de messages inclus dans les fichiers PST. Lorsque l’analyse est terminée et que les données sont prêtes à importer, l’état de la tâche d’importation est remplacée par **l’analyse terminée**. À ce stade, vous avez la possibilité d’importer toutes les données contenues dans les fichiers PST, ou vous pouvez ajuster les données importées en définissant des filtres qui déterminent quelles données obtient importées.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche, cliquez sur **la gouvernance des données** > **Import**.
    
3. Dans la page **Importer** , cliquez sur **prêt à importer dans Office 365** pour le travail d’importation que vous avez créé à l’étape 4. 
    
    ![Cliquez sur prêt à importer dans Office 365 en regard de la tâche d’importation que vous avez créé](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Une page brusque s’affiche avec des informations sur les fichiers PST et autres informations sur la tâche d’importation.
    
4. Cliquez sur **Importer vers Office 365**.
    
5. La page **Filtrer vos données** s’affiche. Il contient les détails de données résultant de l’analyse effectuée sur les fichiers PST par Office 365, notamment des informations sur l’âge des données. À ce stade, vous avez la possibilité pour filtrer les données qui seront importées ou importer toutes les données étant. 
    
    ![Vous pouvez ajuster les données dans les fichiers PST ou importer des](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
6. Effectuez l’une des opérations suivantes :
    
    r. pour découper les données que vous importez, cliquez sur **Oui, je veux filtrer avant l’importation**.
    
    Pour des instructions détaillées sur le filtrage des données dans les fichiers PST et avant de démarrer la tâche d’importation, voir [filtrer les données lors de l’importation des fichiers PST vers Office 365](filter-data-when-importing-pst-files.md).
    
    Ou
    
    b. pour importer toutes les données dans les fichiers PST, cliquez sur **non, je veux tout, importer** et cliquez sur **suivant**.
    
7. Si vous choisissez d’importer toutes les données, cliquez sur **Importer des données** pour démarrer la tâche d’importation. 
    
    L’état de la tâche d’importation est affiché dans la page **Importer** . Cliquez sur ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) **Actualiser** pour mettre à jour les informations d’état qui s’affiche dans la colonne **état** . Cliquez sur la tâche d’importation pour afficher la page état flottant, qui affiche les informations d’état sur chaque fichier PST à importer. Lorsque l’importation est terminée et fichiers PST ont été importées dans les boîtes aux lettres utilisateur, le statut deviendra sur **terminée**.

## <a name="view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Afficher la liste des fichiers PST téléchargé vers Office 365

Vous pouvez installer et utiliser Microsoft Azure stockage Explorer (qui est un outil gratuit, open source) pour afficher la liste des fichiers PST que nous avons téléchargés (par le personnel du centre de données Microsoft) dans la zone de stockage Azure pour votre organisation. Vous pouvez le faire pour vérifier que les fichiers PST des disques durs que vous avez envoyée à Microsoft ont été correctement téléchargés vers la zone de stockage Azure.
  
Microsoft Azure stockage Explorer est en mode Aperçu.
  
 **Important :** Vous ne pouvez pas utiliser l’Explorateur de solutions de stockage Azure pour télécharger ou modifier des fichiers PST. La seule méthode prise en charge pour l’importation des fichiers PST vers Office 365 consiste à utiliser AzCopy. En outre, vous ne pouvez supprimer les fichiers PST que vous avez téléchargée à l’objet blob Azure. Si vous essayez de supprimer un fichier PST, vous recevrez une erreur n’ayant ne pas les autorisations requises. Notez que tous les fichiers PST sont automatiquement supprimés de votre zone de stockage Azure. S’il y a aucune tâche d’importation en cours, puis tous les fichiers PST dans le ** ingestiondata ** conteneur sont supprimés de 30 jours après la dernière tâche d’importation a été créée. 
  
Pour installer l’Explorateur de solutions de stockage Azure et se connecter à votre zone de stockage Azure :
  
1. Effectuez les étapes suivantes pour obtenir l’URL de la Signature de l’accès partagé (sa) pour votre organisation. Cette URL est une combinaison de l’URL de réseau pour l’emplacement de stockage Azure dans le nuage Microsoft de votre organisation et une clé SAS. Cette clé fournit des autorisations nécessaires pour accéder à l’emplacement de stockage Azure de votre organisation.
    
1. Accédez à [https://protection.office.com/](https://protection.office.com/) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche de la sécurité &amp; centre de conformité, cliquez sur **la gouvernance des données** \> **Import**.
    
3. Dans la page **Importer** , cliquez sur ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) **nouvelle tâche d’importation**.
    
4. Dans l’Assistant Importation de projet, tapez un nom pour la tâche d’importation PST, puis cliquez sur **suivant**. Utilisez les lettres minuscules, chiffres, des traits d’union et des traits de soulignement. Impossible d’utiliser des lettres majuscules ou inclure des espaces dans le nom.
    
5. Dans la page **Choisissez Importer le type de travail** , cliquez sur **télécharger vos données** , puis sur **suivant**.
    
6. À l’étape 2, cliquez sur **Afficher les URL SAS de téléchargement réseau**.
    
7. Une fois que l’URL est affichée, copiez-le et enregistrez-le dans un fichier. Veillez à copier l’URL entière.
    
    > [!IMPORTANT]
    > N’oubliez pas de prendre des précautions pour protéger l’URL SAS. Cela peut servir à tout le monde pour accéder à la zone de stockage Azure pour votre organisation. 
  
8. Cliquez sur **Annuler** pour fermer l’Assistant Importation de projet. 
    
2. Téléchargez et installez l' [outil Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
3. Démarrez l’Explorateur de stockage Microsoft Azure, cliquez sur **Comptes de stockage** dans le volet gauche, puis cliquez sur **se connecter au stockage Azure**.
    
    ![Comptes de stockage d’avec le bouton droit, puis cliquez sur se connecter au stockage Azure](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
4. Cliquez sur **utiliser une chaîne de connexion ou URI de signature (sa) accès partagé** , cliquez sur **suivant**.
    
5. Cliquez sur **utiliser un URI SAS**, collez l’URL SAS que vous avez obtenu à l’étape 1 à dans la zone sous **URI**dans, puis cliquez sur **suivant**.
    
6. Dans la page **Résumé de connexion** , vous pouvez passez en revue les informations de connexion, puis cliquez sur **se connecter**.
    
    Le conteneur **ingestiondata** est ouvert ; Il contient les fichiers PST de votre disque dur. Le conteneur **ingestiondata** se trouve sous les **Comptes de stockage** \> **(Services SAS-Attached)** \> **Conteneurs Blob**.
    
    ![L’explorateur de stockage Azure affiche la liste des fichiers PST que vous avez téléchargés](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
7. Lorsque vous avez terminé à l’aide de l’Explorateur de stockage Microsoft Azure, avec le bouton droit **ingestiondata**, puis cliquez sur **Détacher** de se déconnecter de votre zone de stockage Azure. Sinon, vous recevrez une erreur la prochaine fois que vous essayez de joindre. 
    
    ![Cliquez avec le bouton droit de la souris sur ingestion, puis cliquez sur Détacher pour vous déconnecter de votre zone de stockage Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  

  
## <a name="troubleshooting-tips"></a>Conseils de dépannage
<a name="troubleshootingtips"> </a>

- **Que se passe-t-il si le travail d’importation échoue en raison d’erreurs dans le fichier de mappage PST importation CSV ?** Si une tâche d’importation échoue en raison d’erreurs dans le fichier de mappage, vous n’êtes pas obligé de nouveau livrées le disque dur à Microsoft afin de créer une nouvelle tâche d’importation. C’est parce que les fichiers PST du disque dur que vous avez soumis pour la tâche d’importation transaction lecteur ont déjà été téléchargées vers la zone de stockage Azure pour votre organisation. Dans ce cas, vous devez simplement Corrigez les erreurs dans le fichier de mappage PST importation CSV, puis créer un nouveau travail d’importation « téléchargement réseau » et envoyer le fichier de mappage CSV révisé. Pour créer et démarrer un nouveau travail d’importation de téléchargement réseau, voir [étape 5 : créer une tâche d’importation PST dans Office 365](use-network-upload-to-import-pst-files.md#step-5-create-a-pst-import-job-in-office-365) et [étape 6 : filtrer les données et démarrer le travail d’importation PST](use-network-upload-to-import-pst-files.md#step-6-filter-data-and-start-the-pst-import-job) dans la rubrique « Utilisation réseau de téléchargement pour importer des fichiers PST vers Office 365. » 
    
    > [!NOTE]
    > Pour vous aider à résoudre le fichier de mappage de PST importation CSV, utilisez l’outil de [l’Explorateur de solutions de stockage Azure](#view-a-list-of-the-pst-files-uploaded-to-office-365) pour afficher la structure de dossiers dans le conteneur **ingestiondata** pour les fichiers PST de votre disque dur qui ont été téléchargés dans la zone de stockage Azure. Erreurs de mappage de fichier sont généralement dû à une valeur incorrecte dans le paramètre de chemin d’accès. Ce paramètre spécifie l’emplacement d’un fichier PST dans la zone de stockage Azure. Voir la description du paramètre FilePath dans un tableau à [l’étape 3](#step-3-create-the-pst-import-mapping-file). Comme expliqué précédemment, l’emplacement des fichiers PST dans la zone de stockage Azure a été spécifié par le `/dstdir:` paramètre lorsque vous avez exécuté l’outil WAImportExport.exe à [l’étape 2](#step-2-copy-the-pst-files-to-the-hard-drive). 
  

  
## <a name="more-information"></a>Plus d'informations

- Envoi de lecteur est un moyen efficace pour importer les grandes quantités de données d’archivage messages vers Office 365 pour tirer parti des fonctionnalités de conformité qui sont disponibles pour votre organisation. Une fois que les données d’archivage sont importées dans les boîtes aux lettres utilisateur, vous pouvez :
    
  - Activer des [boîtes aux lettres d’archive](enable-archive-mailboxes.md) et [Développer automatiquement l’archivage](enable-unlimited-archiving.md) pour permettre aux utilisateurs d’espace de stockage de boîtes aux lettres supplémentaires pour les données. 
    
  - Placer les boîtes aux lettres en [Litige](https://go.microsoft.com/fwlink/?linkid=856286) de conservation des données. 
    
  - Utilisez Microsoft [eDiscovery outils](search-for-content.md) pour rechercher les données. 
    
  - Appliquer des [stratégies de rétention Office 365](retention-policies.md) pour contrôler la durée de conservation des données et l’action à entreprendre après expiration de la période de rétention. 
    
  - Recherche [journal d’audit Office 365](search-the-audit-log-in-security-and-compliance.md) pour les événements associés à ces données. 
    
  - Importer des données de [boîtes aux lettres inactives](create-and-manage-inactive-mailboxes.md) pour archiver des données à des fins de conformité aux. 
    
  - Protéger votre organisation contre la [perte de données](data-loss-prevention-policies.md) d’informations sensibles. 
    
- Voici un exemple de la clé de compte de stockage sécurisé et d’une clé de chiffrement BitLocker. Cet exemple contient également la syntaxe de la commande WAImportExport.exe qui permet de copier les fichiers PST sur un disque dur. Veillez à prendre toutes les précautions nécessaires pour protéger ces clés, tout comme vous le feriez avec vos mots de passe ou d’autres informations de sécurité.
    

    ```
    Secure storage account key: 

    yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==

    BitLocker encryption key:

    397386-221353-718905-535249-156728-127017-683716-083391

  COMMAND SYNTAX

  First time:

  WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>

  Subsequent times:

  WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 

  EXAMPLES

  First time:

  WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER1\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"

  Subsequent times:

  WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER1\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```
   
- Comme expliqué précédemment, le service Office 365 importation Active le blocage de rétention définition (pour une durée indéterminée) une fois que les fichiers PST sont importées dans une boîte aux lettres. Cela signifie que la propriété *RentionHoldEnabled* est définie sur `True` afin que la stratégie de rétention attribuée à la boîte aux lettres ne sera pas traitée. Ainsi, le temps de propriétaire de boîte aux lettres pour gérer les messages nouvellement importées en empêchant une suppression ou une stratégie d’archivage de supprimer ou de l’archivage des messages plus anciens. Voici quelques étapes à que suivre pour gérer ce blocage de rétention : 
    
  - Après un certain temps, vous pouvez désactiver le blocage de rétention en exécutant la `Set-Mailbox -RetentionHoldEnabled $false` commande. Pour plus d’informations, voir [archive une boîte aux lettres sur la rétention](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
  - Vous pouvez configurer le blocage de rétention afin qu’il est désactivé sur une date dans le futur. Pour cela, exécutez le `Set-Mailbox -EndDateForRetentionHold <date>` commande. Par exemple, en supposant que la date du jour est le 1 juillet 2016 et vous souhaitez le blocage de rétention désactivé des 30 derniers jours, vous exécuterez la commande suivante : `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. Dans ce scénario, laissez la propriété *RentionHoldEnabled* la valeur *True* . Pour plus d’informations, voir [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
  - Vous pouvez modifier les paramètres de la stratégie de rétention qui est affectée à la boîte aux lettres afin que les anciens éléments qui ont été importés ne sont pas immédiatement supprimés ou déplacés vers la boîte aux lettres de l’utilisateur archive. Par exemple, vous pouvez augmenter l’âge de rétention pour une stratégie de suppression ou d’archivage qui est affectée à la boîte aux lettres. Dans ce scénario, vous devez désactiver le blocage de rétention sur la boîte aux lettres une fois que vous avez modifié les paramètres de la stratégie de rétention. Pour plus d’informations, voir [configurer une stratégie d’archivage et de suppression des boîtes aux lettres dans votre organisation Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    

  

