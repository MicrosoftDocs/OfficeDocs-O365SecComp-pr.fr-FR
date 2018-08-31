---
title: Utiliser le chargement réseau pour importer des fichiers PST chiffrés via RMS dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 84a595b8-cd77-4f66-ac52-57a33ddd4773
description: Découvrez comment télécharger réseau permet d’importer des fichiers PST RMS chiffrés aux boîtes aux lettres utilisateur dans Office 365.
ms.openlocfilehash: 6460512e2d6085df684841248dc286d39dbd9d87
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528718"
---
# <a name="use-network-upload-to-import-rms-encrypted-pst-files-to-office-365"></a>Utiliser le chargement réseau pour importer des fichiers PST chiffrés via RMS dans Office 365

**Cet article est destiné aux administrateurs. Vous essayez d’importer des fichiers PST à votre propre boîte aux lettres ? Voir [messagerie importation, contacts et calendrier à partir d’un fichier Outlook .pst](https://go.microsoft.com/fwlink/p/?LinkID=785075)**
   
Utilisation du réseau télécharger option et le service Office 365 importer pour importer des fichiers PST vers les boîtes aux lettres. Téléchargement du réseau signifie que vous téléchargez les fichiers PST une zone de stockage temporaire dans le nuage de Microsoft. Le service Office 365 importation copie ensuite les fichiers PST à partir de la zone de stockage pour les boîtes aux lettres cible. Une nouvelle fonctionnalité du service d’importation vous permet de chiffrer les fichiers PST avant qu’ils sont téléchargés et stockés sur le nuage Microsoft. Ces fichiers seront non chiffrées lors de leur importation aux boîtes aux lettres de l’utilisateur. 
  
Voici les étapes nécessaires pour chiffrer et importer des fichiers PST aux boîtes aux lettres Office 365 :
  
[Étape 1 : Configurer Azure Rights Management pour importer des fichiers PST ](#step-1-set-up-azure-rights-management-for-pst-import)

[Étape 2 : Générer une clé de chiffrement pour l’importation PST](#step-2-generate-an-encryption-key-for-pst-import)

[Étape 3 : Obtenir l’ID de client RMS et l’URL de gestion des licences](#step-3-obtain-rms-tenant-id-and-licensing-url)

[Étape 4 : Téléchargez les outils d’importation PST et copiez l’URL SAS](#step-4-download-the-pst-import-tools-and-copy-the-sas-url)

[Étape 5 : Chiffrer et télécharger vos fichiers PST vers Office 365](#step-5-encrypt-and-upload-your-pst-files-to-office-365)

[(Facultatif) Étape 6 : Afficher une liste des fichiers PST téléchargé vers Office 365](#optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Étape 7 : Créer le fichier de mappage d’importation PST](#step-7-create-the-pst-import-mapping-file)

[Étape 8 : Créer une tâche d’importation PST dans Office 365](#step-8-create-a-pst-import-job-in-office-365)
  
> [!IMPORTANT]
> Vous devez effectuer l’étape 1 à l’étape 4 qu’une seule fois pour installer et configurer votre organisation pour chiffrer et importer des fichiers PST aux boîtes aux lettres Office 365. Après avoir effectué ces étapes, suivez étape 5 à 8 étape chaque fois que vous souhaitez chiffrer, télécharger et importer un lot de fichiers PST. 
  
Pour plus d’informations sur l’importation de données dans Office 365, voir [vue d’ensemble de l’importation de votre entreprise de fichiers PST vers Office 365](importing-pst-files-to-office-365.md).
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez être le rôle importer exporter des boîtes aux lettres dans Exchange Online pour importer des fichiers PST aux boîtes aux lettres Office 365. Par défaut, ce rôle n’est pas affecté à un groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle de boîte aux lettres importer exporter au groupe de rôles de gestion de l’organisation. Ou vous pouvez créer un nouveau groupe de rôles, attribuer le rôle de boîte aux lettres importer exporter et puis ajoutez-vous en tant que membre. Pour plus d’informations, voir le « ajouter un rôle à un groupe de rôles » ou les sections de la « créer un groupe de rôles » dans [Gérer les groupes de rôles](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    En outre, pour créer l’importation des travaux de sécurité Office 365 &amp; centre de conformité, une des opérations suivantes doivent être remplie :
    
  - Vous devez être affecté le rôle destinataires de messagerie dans Exchange Online. Par défaut, ce rôle est attribué aux groupes de rôles de gestion de l’organisation et la gestion des destinataires.
    
    Ou
    
  - Vous devez être un administrateur global dans votre organisation Office 365.
    
  > [!TIP]
  > Envisagez de créer un nouveau groupe de rôles dans Exchange Online est spécifiquement conçu pour l’importation des fichiers PST vers Office 365. Pour le niveau minimal de privilèges nécessaires pour importer des fichiers PST, attribuer les rôles destinataires de messagerie et de boîte aux lettres importer exporter vers le nouveau groupe de rôles et ajouter des membres. 
  
- Vous devez stocker les fichiers PST que vous souhaitez importer vers Office 365 sur un serveur de fichiers ou un dossier partagé dans votre organisation. À l’étape 5, vous allez exécuter la ImportTool Office 365, qui permettra de chiffrer et de télécharger les fichiers PST qui sont stockées sur ce serveur de fichiers ou dossier à Office 365 partagé.
    
- Cette procédure consiste à copier et enregistrer une copie d’une clé de chiffrement, une clé de stockage et un nombre d’URL et les clés d’identification. Ces informations servira à l’étape 5 pour chiffrer et télécharger vos fichiers PST. N’oubliez pas de prendre des précautions pour protéger ces simplement comme vous le feriez protéger les mots de passe ou d’autres informations relatives à la sécurité. Par exemple, vous pouvez les enregistrer dans un document Microsoft Word protégés par mot de passe ou les enregistrer sur un lecteur USB chiffré. Voir la section [plus d’informations](#more-information) pour un exemple de ces clés, ID et des URL. 
    
- Vous pouvez importer des fichiers PST à une boîte aux lettres inactive dans Office 365. Cela en spécifiant le GUID de la boîte aux lettres inactive dans le `Mailbox` paramètre dans le fichier de mappage d’importation PST. Pour plus d’informations, consultez [l’étape 7](#step-7-create-the-pst-import-mapping-file) . 
    
- Dans un déploiement Exchange hybride, vous pouvez importer des fichiers PST à une boîte aux lettres d’archive en nuage pour un utilisateur de boîte aux lettres principale est local. Pour cela, procédez comme suit dans le fichier de mappage d’importation PST :
    
  - Spécifiez l’adresse de messagerie pour la boîte aux lettres locale de l’utilisateur dans le `Mailbox` paramètre. 
    
  - Spécifiez la valeur **TRUE** dans le `IsArchive` paramètre. 
    
    Pour plus d’informations, consultez [l’étape 7](#step-7-create-the-pst-import-mapping-file) . 
    
- Une fois les fichiers PST sont importées dans une boîte aux lettres Office 365, le blocage de rétention définition pour la boîte aux lettres est activé pour une durée indéterminée. Cela signifie que la stratégie de rétention attribuée à la boîte aux lettres ne sera pas traitée jusqu'à ce que vous désactivez le blocage de rétention ou définissez une date pour désactiver le blocage. Pourquoi nous réalisons cela ? Si les messages importés dans une boîte aux lettres sont anciennes, ils peuvent définitivement supprimés (définitivement) parce que leur période de rétention a expiré en fonction des paramètres de rétention configurées pour la boîte aux lettres. Placer la boîte aux lettres sur le blocage de rétention vous donne le temps de propriétaire de boîte aux lettres de gérer ces messages nouvellement importées ou le permettent de modifier les paramètres de rétention pour la boîte aux lettres du temps. Voir la section [plus d’informations](#more-information) pour obtenir des suggestions sur la gestion de la période de rétention. 
    
- Si vous n’avez pas besoin chiffrer les fichiers PST avant de les télécharger vers Office 365, voir [utiliser le réseau télécharger pour importer des fichiers PST vers Office 365](use-network-upload-to-import-pst-files.md).
    
- Pour des questions fréquemment posées sur l’utilisation de téléchargement réseau pour importer des fichiers PST vers Office 365, voir [FAQ sur l’importation de fichiers PST vers Office 365](faqimporting-pst-files-to-office-365.md).
  
## <a name="step-1-set-up-azure-rights-management-for-pst-import"></a>Étape 1 : Configurer Azure Rights Management pour importer des fichiers PST 

Importation PST utilise la fonctionnalité de chiffrement fournie par le service Azure Rights Management (Services RMS Azure) dans Office 365. Cela vous permet pour chiffrer les fichiers PST avant de les télécharger vers Office 365. 
  
Configuration RMS Azure à l’importation PST se compose de trois étapes :
  
- [Activation d’Azure RMS](#activate-azure-rms)
    
- [Configuration de RMS dans Exchange Online](#configure-rms-in-exchange-online)
    
- [Installer le Client RMS Active Directory](#install-the-active-directory-rms-client)
    
### <a name="activating-azure-rms"></a>Activation d’Azure RMS

Azure RMS est désactivé par défaut, mais vous ou un autre administrateur de votre organisation peut avoir activée. Suivez les instructions sur l' [Activation d’Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) pour installer et activer Azure DRM.
  
### <a name="configuring-rms-in-exchange-online"></a>Configuration de RMS dans Exchange Online

Une fois que vous avez activé le service de gestion des droits, l’étape suivante consiste à définir Information Rights Management (IRM) dans Exchange Online à utiliser RMS Azure. Pour plus d’informations, voir [Configurer l’IRM à utiliser Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=394816).
  
1. [Se connecter à Exchange Online à l’aide de PowerShell à distance](https://go.microsoft.com/fwlink/p/?LinkId=396554 ).
    
2. Exécutez la commande suivante pour définir l’URL de partage de la clé RMS.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation <RMS key sharing location>
    ```

    Reportez-vous au tableau suivant pour déterminer l’emplacement de partage de la clé RMS correspondant à l’emplacement de votre organisation.
    
    |**Emplacement**|**Emplacement de partage de la clé RMS**|
    |:-----|:-----|
    |Amérique du Nord  <br/> | `https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Union européenne  <br/> | `https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Asie  <br/> | `https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Amérique du Sud  <br/> | `https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Office 365 pour le gouvernement (nuage communautaire propre aux gouvernements)  <br/> | `https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>1</sup> <br/> |
   
    > [!NOTE]
    > <sup>1</sup> uniquement les clients ayant acheté Office 365 pour les éditions gouvernement (nuage communautaire de gouvernement) doivent utiliser cet emplacement de partage de clé RMS. 
  
    Par exemple, cette commande configure la clé RMS Online emplacement de partage dans Exchange Online pour un client situé en Amérique du Nord.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
    ```

3. Exécutez la commande suivante pour importer une confiance domaine de publication (TPD) à partir de RMS Online dans votre organisation Office 365. 
    
    ```
    Import-RMSTrustedPublishingDomain -RMSOnline -Name "RMS Online"
    ```

    Un domaine de publication approuvé contient les paramètres nécessaires à l’utilisation des fonctionnalités RMS dans votre organisation, notamment les fichiers PST de chiffrement.  
    
4. Exécutez la commande suivante pour activer IRM pour votre organisation Office 365.
    
    ```
    Set-IRMConfiguration -InternalLicensingEnabled $true
    ```

### <a name="installing-the-active-directory-rms-client"></a>Installer le Client RMS Active Directory

Dans cette section de la dernière étape consiste à télécharger le Client Rights Management Services (RMS) 2.1. Ce logiciel permet de protéger l’accès aux Azure RMS et protège les informations transitant par les applications qui utilisent Azure RMS installer le client RMS sur le même ordinateur que vous allez utiliser pour chiffrer les fichiers PST à l’étape 5. 
  
1. Télécharger le [Client de Service de gestion des droits 2.1](https://www.microsoft.com/en-us/download/details.aspx?id=38396).
    
2. Exécutez l’Assistant du client Active Directory Rights Management Service 2.1 pour installer le client.

## <a name="step-2-generate-an-encryption-key-for-pst-import"></a>Étape 2 : Générer une clé de chiffrement pour l’importation PST

Une fois que vous avez configuré Azure RMS, l’étape suivante consiste à générer une clé de chiffrement (appelée une clé symétrique) qui sera utilisée pour chiffrer les fichiers PST que vous téléchargez sur Office 365. Pour cela, vous allez ajouter le service d’importation PST en tant que service principal dans Azure Active Directory. Ajout de cette application comme un principal de service permettra de s’authentifier directement auprès d’Azure Active Directory lorsque vous téléchargez le service importation PST chiffré les fichiers PST à l’emplacement de stockage Azure à l’étape 5.
  
1. Démarrez le Module Azure Active Directory pour Windows PowerShell.
    
2. Exécutez la commande suivante pour vous connecter au service Microsoft Online.
    
    ```
    Connect-MsolService
    ```

3. Entrez les informations d’identification pour un compte d’administrateur de votre organisation Office 365, puis cliquez sur **OK**.
    
4. Exécutez la commande suivante pour générer une clé de chiffrement (appelée clé symétrique). Pour cela, vous devez créer un principal de chiffrement PST.
    
    ```
    New-MsolServicePrincipal -DisplayName PstEncryptionPrincipal
    ```

    Le système affiche la clé symétrique et les propriétés du nouveau principal de chiffrement PST.
    
    ![Copiez et enregistrez la clé symétrique qui est affichée](media/0003fdea-dace-41d2-b49d-f5c98c6230ca.png)
  
5. Copiez la clé symétrique dans un fichier texte ou Word. Comme indiqué précédemment, veillez à prendre les précautions nécessaires pour protéger ce fichier. Étant donné que la clé symétrique n’est affichée qu’une seule fois, vous pouvez également effectuer une capture d’écran de la fenêtre et l’enregistrer dans le même fichier.  
    
    > [!IMPORTANT]
    > Une fois le principal de chiffrement PST créé, vous ne pourrez pas récupérer la clé symétrique à l’aide de la cmdlet **Get-MsolServicePrincipal**. C’est pourquoi vous devez enregistrer la clé. 
  
Conserver l’Azure Active Directory Module pour Windows PowerShell ouverte et connectée au service Microsoft Online. Vous devez exécuter une commande dans cette fenêtre dans l’étape suivante.

## <a name="step-3-obtain-rms-tenant-id-and-licensing-url"></a>Étape 3 : Obtenir l’ID de client RMS et l’URL de gestion des licences

L’étape suivante consiste à obtenir le client ID et l’URL d’emplacement de gestion des licences pour le service RMS Azure pour votre organisation. Copiez et enregistrer les informations sur le même fichier qui contient la clé symétrique à l’étape 2. L’ID et l’URL seront utilisé à l’étape 5 pour chiffrer les fichiers PST.
  
1. Dans le Azure Module Active Directory pour Windows PowerShell (qui est connectée au service Microsoft Online), exécutez la commande suivante pour vous connecter au service RMS Azure dans votre organisation Office 365.
    
    ```
    Connect-AadrmService 
    ```

2. Entrez les informations d’identification pour un compte d’administrateur de votre organisation Office 365, puis cliquez sur **OK**.
    
3. Exécutez la commande suivante pour afficher l’ID de client pour le service RMS Azure dans votre organisation Office 365.
    
    ```
    Get-AadrmConfiguration | FL BPOSId
    ```

    Copiez et enregistrez la valeur de la `BPOSId` propriété. 
    
4. Exécutez la commande suivante pour afficher l’emplacement de gestion des licences pour votre service RMS Azure.
    
    ```
    Get-AadrmConfiguration | FL LicensingIntranetDistributionPointUrl
    ```

    Copiez et enregistrez la valeur de la `LicensingIntranetDistributionPointUrl` propriété. 

## <a name="step-4-download-the-pst-import-tools-and-copy-the-sas-url"></a>Étape 4 : Téléchargez les outils d’importation PST et copiez l’URL SAS

Maintenant que vous avez configuré RMS Azure et obtenir les ID nécessaires pour chiffrer les fichiers PST, l’étape suivante consiste à télécharger et installer les outils que vous allez exécuter à l’étape 5 pour chiffrer et PST de téléchargement de fichiers vers Office 365. Ces outils sont les outils AzCopy Azure et le chiffrement de données Office 365. Vous allez également copier l’URL SAS pour votre organisation. Cette URL est une combinaison de l’URL de réseau pour l’emplacement de stockage Azure dans le nuage Microsoft pour votre organisation et une clé de Signature de l’accès partagé (sa). Cette clé fournit des autorisations nécessaires pour télécharger des fichiers PST vers votre emplacement de stockage Azure. Enregistrez-le dans le même fichier que vous avez copié les autres informations à dans l’étape 2 et l’étape 3. Comme indiqué précédemment, prendre des précautions pour protéger l’URL SAS. 
  
> [!IMPORTANT]
> Vous devez utiliser Azure AzCopy version 5.0 pour télécharger correctement les fichiers PST à l’emplacement de stockage Azure. Nouvelles versions de l’outil AzCopy ne sont pas pris en charge pour l’importation des fichiers PST vers Office 365. Veillez à télécharger l’outil AzCopy à partir de la page **télécharger les fichiers sur le réseau** en suivant les procédures décrites dans cette étape. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 avec les informations d’identification pour un compte d’administrateur de votre organisation Office 365.
    
3. Dans le volet gauche, cliquez sur **la gouvernance des données** , puis cliquez sur **Importer**.
    
4. Sur la page **Importation**, cliquez sur **Ouvrir le service d’importation**.
    
5. Dans la page **Importer des données dans Office 365** , cliquez sur **Nouveau travail** ![ajouter une icône](media/ITPro-EAC-AddIcon.gif), puis cliquez sur **télécharger les messages électroniques (fichiers PST)**.
    
6. Dans la page **télécharger les fichiers sur le réseau** , à l’étape 2, cliquez sur **Afficher les URL SAS de téléchargement réseau**.
    
7. Une fois que l’URL est affichée, copiez-le et enregistrez-le dans le fichier où vous avez enregistré les autres clés. Veillez à copier l’URL entière. 
    
8. À l’étape 3, cliquez sur **Télécharger l’outil AzCopy Azure** pour télécharger et installer l’outil AzCopy Azure. 
    
9. Dans la fenêtre contextuelle, cliquez sur **Exécuter** pour installer l’outil AzCopy d’Azure. 
    
    > [!IMPORTANT]
    > Veillez à installer l’outil AzCopy Azure dans l’emplacement par défaut, qui est `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` sur un ordinateur exécutant Windows 64 bits. C’est parce que lorsque vous exécutez le O365ImportTool.exe à l’étape 5, il recherche l’outil AzCopy à cet emplacement. 
  
10. Une fois que vous avez installé l’outil AzCopy Azure, cliquez sur **Télécharger le chiffrement de données Office 365 et l’outil d’importation**.
    
11. Dans la fenêtre contextuelle, cliquez sur **Enregistrer** \> **Enregistrer sous** pour enregistrer le fichier O365ImportTool.zip dans un dossier sur votre ordinateur local. 
    
12. Décompressez le fichier O365ImportTool.zip.
    
13. Cliquez sur **Annuler** pour fermer la page de **téléchargement de fichiers sur le réseau** . 
 
## <a name="step-5-encrypt-and-upload-your-pst-files-to-office-365"></a>Étape 5 : Chiffrer et télécharger vos fichiers PST vers Office 365

Une fois que vous avez terminé le Step 1 à l’étape 4, vous êtes prêt à utiliser l’outil O365ImportTool.exe pour chiffrer et télécharger des fichiers PST vers Office 365. Cet outil crypte vos fichiers PST, puis télécharge et les stocke dans un emplacement de stockage Azure dans le nuage de Microsoft. Pour effectuer cette étape, les fichiers PST doivent se trouver dans un partage de fichiers ou un serveur de fichiers dans votre organisation. Il s’agit du répertoire source de la procédure suivante. Chaque fois que vous exécutez l’outil O365ImportTool.exe, vous pouvez spécifier un répertoire source différents. 
  
1. Ouvrez une invite de commandes sur votre ordinateur local.
    
2. Accédez au répertoire où vous avez installé l’outil O365ImportTool.exe à l’étape 4.
    
3. Exécutez la commande suivante pour chiffrer et télécharger des fichiers PST vers Office 365.
    
    ```
    O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL> /upload-destSAS:<SAS key>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requises. Notez que les informations obtenues lors des étapes précédentes sont utilisées pour remplir les valeurs de ces paramètres.
    
    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `/srcdir:` <br/> |Spécifie le répertoire source de votre organisation qui contient les fichiers PST qui seront téléchargés vers Office 365.  <br/> | `/srcdir:\\FILESERVER01\PSTs` <br/> |
    | `/protect-rmsserver:` <br/> |Spécifie l’emplacement de gestion des licences pour votre service RMS Azure. Utilisez la valeur de la `LicensingIntranetDistributionPointUrl` propriété que vous avez obtenu à l’étape 3. Veillez à mettre la valeur de ce paramètre avec des guillemets (« »)<br/> | `/protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing"` <br/> |
    | `/protect-tenantid:` <br/> |Spécifie l’identité de votre organisation Azure RMS. Utilisez la valeur de la `BPOSId` propriété que vous avez obtenu à l’étape 3.<br/> | `/protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b` <br/> |
    | `/protect-key:` <br/> |Spécifie la clé symétrique que vous avez obtenu à l’étape 2. Veillez à mettre la valeur de ce paramètre avec des guillemets (« »).  <br/> | `/protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867="` <br/> |
    | `/transfer:` <br/> |Spécifie si vous téléchargez les fichiers PST sur le réseau ou les expédiez sur un disque dur. La valeur `upload` indique que vous téléchargez les fichiers sur le réseau. La valeur `drive` indique que vous fournissez les fichiers pst sur un disque dur.<br/> | `/transfer:upload` <br/> |
    | `/upload-dest:` <br/> |Spécifie la destination dans Office 365 où vos fichiers PST seront téléchargés. Il s’agit de l’emplacement de stockage Azure pour votre organisation. La valeur pour ce paramètre est constituée de l’URL de téléchargement de réseau à partir de l’URL SAS que vous avez copié à l’étape 4. Veillez à mettre la valeur de ce paramètre avec des guillemets (« »).<br/><br/> **Conseil :** (Facultatif) Vous pouvez spécifier un sous-dossier à l’emplacement de stockage Azure pour télécharger les fichiers PST chiffrés. Pour cela, en ajoutant un emplacement sous-dossier (après « ingestiondata ») dans l’URL de téléchargement du réseau. Le premier exemple ne spécifie pas un sous-dossier ; Cela signifie que les fichiers PST sera téléchargé à la racine (appelée *ingestiondata* ) de l’emplacement de stockage Azure. Le deuxième exemple télécharge les fichiers PST dans un sous-dossier (nommé *EncryptedPSTs* ) dans l’emplacement de stockage Azure.           | `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata"` <br/> Ou  <br/>  `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs"` <br/> |
    | `/upload-destSAS:` <br/> |Spécifie la clé SAS pour votre organisation. La valeur pour ce paramètre se compose de la clé SAS à partir de l’URL SAS que vous avez copié à l’étape 4. Notez que le premier caractère de la touche SAS est un point d’interrogation (« ? »). Veillez à mettre la valeur de ce paramètre avec des guillemets (« »).  <br/> | `/upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/recurse` <br/> |Ce commutateur facultatif spécifie le mode récursive afin que l’outil O365ImportTool.exe copie les fichiers pst qui se trouvent dans des sous-dossiers dans le répertoire source spécifié par le `/srcdir:` paramètre.  <br/><br/> **Remarque :** Si vous incluez ce commutateur, des fichiers PST dans les sous-dossiers a un chemin d’accès de fichier différent dans l’emplacement de stockage Azure après leur téléchargement. Vous devrez spécifier le chemin d’accès exact du fichier dans le fichier CSV que vous créez à l’étape 7.           | `/recurse` <br/> |
   
    Voici un exemple de la syntaxe de l’outil O365ImportTool.exe qui reprend les valeurs réelles de chaque paramètre :
    
    ```
    O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b  /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
    ```

    Une fois la commande exécutée, les messages d’état affichent la progression du processus de chiffrement et de téléchargement des fichiers PST. Un message d’état final affiche le nombre total de fichiers qui ont été chiffrés et téléchargés.  
    
    > [!TIP]
    > Une fois que vous exécutez la commande O365ImportTool.exe de correctement et vérifiez que tous les paramètres sont corrects, enregistrer une copie de la syntaxe de ligne de commande pour le même fichier (sécurisée) où vous avez copié les informations obtenues lors des étapes précédentes. Ensuite, vous pouvez copier et coller cette commande dans une invite de commandes chaque fois que vous souhaitez exécuter l’outil O365ImportTool.exe pour chiffrer et télécharger des fichiers PST vers Office 365. Les seules valeurs que vous devrez peut-être modifier sont ceux de la `/srcdir:` et `/upload-dest:` paramètres. 
  
## <a name="optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(Facultatif) Étape 6 : Afficher une liste des fichiers PST téléchargé vers Office 365

Comme une étape facultative, vous pouvez installer et utiliser Microsoft Azure stockage Explorer (qui est un outil gratuit, open source) pour afficher la liste des fichiers PST que vous avez téléchargée à l’objet blob Azure. Il existe trois bonnes raisons à cela :
  
- Vérifiez que les fichiers PST à partir du dossier partagé ou le serveur de fichiers dans votre organisation ont été correctement téléchargés vers l’objet blob Azure.

- Vérifiez que les fichiers PST sont chiffrées. Les fichiers PST chiffrés ont une `.pfile` extension ajoutée au nom de fichier PST ; par exemple, `pilarp.pst.pfile`.
    
- Vérifiez le nom de fichier (et le chemin d’accès sous-dossier si vous avez inclus un) pour chaque fichier PST téléchargé vers l’objet blob Azure. Il s’agit très utile lorsque vous créez le fichier PST mappage du fichier à l’étape suivante, car vous devez spécifier le chemin d’accès du dossier et le nom de fichier pour chaque fichier PST. Vérification de ces noms permettent de réduire les erreurs dans votre fichier de mappage PST.
    
Microsoft Azure stockage Explorer est en mode Aperçu. 
  
 > [!IMPORTANT]
>  Vous ne pouvez pas utiliser l’Explorateur de solutions de stockage Azure pour télécharger ou modifier des fichiers PST. La seule méthode prise en charge pour l’importation des fichiers PST vers Office 365 consiste à utiliser AzCopy. En outre, vous ne pouvez supprimer les fichiers PST que vous avez téléchargée à l’objet blob Azure. Si vous essayez de supprimer un fichier PST, vous recevrez une erreur n’ayant ne pas les autorisations requises. Notez que tous les fichiers PST sont automatiquement supprimés de votre zone de stockage Azure. S’il y a aucune tâche d’importation en cours, puis tous les fichiers PST dans le conteneur **ingestiondata** n’est supprimés de 30 jours après que la dernière tâche d’importation a été créée. 
  
Pour installer l’Explorateur de solutions de stockage Azure et se connecter à votre zone de stockage Azure :
  
1. Téléchargez et installez l' [outil Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Démarrez l’Explorateur de stockage Microsoft Azure, cliquez sur **Comptes de stockage** dans le volet gauche, puis cliquez sur **se connecter au stockage Azure**. 
    
    ![Comptes de stockage d’avec le bouton droit, puis cliquez sur se connecter au stockage Azure](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Dans la zone sous **se connecter au stockage Azure**, collez l’URL SAS que vous avez obtenu à l’étape 4, puis cliquez sur **suivant**. 
    
    ![Collez l’URL SAS dans la zone sur la page connexion à un stockage Azure](media/5d034128-e087-48e1-9ebc-4c9fa262d5b7.png)
  
4. Dans la page **Résumé de connexion** , vous pouvez passez en revue les informations de connexion, puis cliquez sur **se connecter**. 
    
5. Sous **Comptes de stockage**, développez le nœud **Service SAS ()** , puis développez le nœud de **Conteneurs Blob** . 
    
6. Avec le bouton droit **ingestiondata**, puis cliquez sur **Ouvrir l’éditeur de conteneur Blob**.
    
    ![Cliquez avec le bouton droit sur ingestiondata, puis cliquez sur Ouvrir l’éditeur de conteneur d’objets blob](media/f50eee30-9202-4efc-904a-2895a0bc388d.png)
  
    La zone de stockage Azure, avec une liste des fichiers PST que vous avez téléchargé à l’étape 5 est affichée.
    
    ![L’explorateur de stockage Azure affiche la liste des fichiers PST que vous avez téléchargés](media/a448ae43-e744-4153-8304-22b59e93883c.png)
  
7. Lorsque vous avez terminé à l’aide de l’Explorateur de stockage Microsoft Azure, avec le bouton droit **ingestiondata**, puis cliquez sur **Détacher** de se déconnecter de votre zone de stockage Azure. Sinon, vous recevrez une erreur la prochaine fois que vous essayez de joindre. 
    
    ![Cliquez avec le bouton droit de la souris sur ingestion, puis cliquez sur Détacher pour vous déconnecter de votre zone de stockage Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-7-create-the-pst-import-mapping-file"></a>Étape 7 : Créer le fichier de mappage d’importation PST

Une fois que les fichiers PST ont été chiffrées et téléchargés vers l’emplacement de stockage Azure pour votre organisation Office 365, l’étape suivante consiste à créer une virgule séparés fichier CSV (valeurs) qui spécifie les boîtes aux lettres utilisateur les fichiers PST sera importés à. Vous envoyez ce fichier CSV dans l’étape suivante lorsque vous créez une tâche d’importation PST.
  
1. [Téléchargez une copie du fichier de mappage importation PST](https://go.microsoft.com/fwlink/p/?LinkId=544717). 
    
2. Ouvrez ou enregistrez le fichier CSV sur votre ordinateur local. L’exemple suivant montre le contenu d’un fichier de mappage d’importation PST (ouvert dans le Bloc-notes). Utilisez plutôt Microsoft Excel pour modifier le fichier CSV.
    
    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,,annb.pst.pfile,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,annb_archive.pst.pfile,annb@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,,donh.pst.pfile,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,donh_archive.pst.pfile,donh@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,pilarp.pst.pfile,pilarp@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,pilarp_archive.pst.pfile,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,tonyk.pst.pfile,tonyk@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,tonyk_archive.pst.pfile,tonyk@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,zrinkam.pst.pfile,zrinkam@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,zrinkam_archive.pst.pfile,zrinkam@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    ```

    La première ligne, ou ligne d’en-tête du fichier CSV répertorie les paramètres qui servira par le service d’importation PST pour importer les fichiers PST vers les boîtes aux lettres. Nom de chaque paramètre est séparée par une virgule. Chaque ligne sous la ligne d’en-tête représente les valeurs des paramètres d’importation d’un fichier PST dans une boîte aux lettres spécifique. Vous aurez besoin une ligne pour chaque fichier PST que vous souhaitez importer dans une boîte aux lettres de l’utilisateur. Veillez à remplacer les données d’espace réservé dans le fichier de mappage de vos données réelles.
    
    > [!NOTE]
    > Ne modifiez en aucun cas la ligne d’en-tête, ni les paramètres SharePoint ; ils seront ignorés pendant le processus d’importation des fichiers PST. 
  
3. Utilisez les informations du tableau suivant pour remplir le fichier CSV avec les informations requises.
    
    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Spécifie le service Office 365 pour les données seront importées. Pour importer des fichiers PST aux boîtes aux lettres de l’utilisateur, utilisez `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Spécifie l’emplacement du dossier à l’emplacement de stockage Azure que que vous avez téléchargé les fichiers PST à l’étape 5.  <br/>  Si vous n’avez pas inclure un nom facultatif sous-dossier dans l’URL de réseau dans le `/upload-dest:` paramètre à l’étape 5, laissez ce paramètre vide dans le fichier CSV. Si vous avez inclus un nom du sous-dossier, spécifier dans ce paramètre. La valeur pour ce paramètre respecte la casse. Les deux cas, ** n’incluez pas « ingestiondata » dans la valeur de la `FilePath` paramètre.<br/> <br/>**Important :** Le cas pour le nom de chemin d’accès du fichier doit être la même casse que vous avez utilisé si vous avez inclus un nom facultatif sous-dossier dans l’URL SAS dans le `/upload-dest:` paramètre à l’étape 5. Par exemple, si vous avez utilisé `EncryptedPSTs` pour le sous-dossier de nom à l’étape 5 et ensuite utiliser `encryptedpsts` dans les `FilePath` paramètre dans le fichier CSV, l’importation du fichier PST échouera. Veillez à utiliser la même casse dans les deux instances.           |(Laisser vide)  <br/> Ou  <br/>  `EncryptedPSTs` <br/> |
    | `Name` <br/> |Spécifie le nom du fichier qui sera importé dans la boîte aux lettres de l’utilisateur. La valeur pour ce paramètre respecte la casse. Étant donné que les fichiers PST qui sont téléchargés vers l’emplacement de stockage Azure sont chiffrées, un `.pfile` extension est ajoutée au nom de fichier PST. Vous devez ajouter le `.pfile` extension sur le nom de fichier des fichiers dans le fichier CSV.<br/><br/> **Important :** Le cas pour le nom de fichier PST dans le fichier CSV doit être la même que le fichier .pst qui a été téléchargé vers l’emplacement de stockage Azure à l’étape 5. Par exemple, si vous utilisez `annb.pst.pfile` dans les `Name` paramètre dans le fichier CSV, mais le nom du fichier PST réel est `AnnB.pst`, l’importation de ce fichier PST échouera. N’oubliez pas que le nom du fichier .pst dans le fichier CSV utilise la même casse que le fichier PST.           | `annb.pst.pfile` <br/> |
    | `Mailbox` <br/> |Indique l’adresse de messagerie de la boîte aux lettres dans laquelle le fichier PST est importé.   <br/> Pour importer un fichier PST dans une boîte aux lettres inactive, vous devez spécifier la boîte aux lettres GUID pour ce paramètre. Pour obtenir ce GUID, exécutez la commande PowerShell suivante dans Exchange Online : « Get-Mailbox - InactiveMailboxOnly<identity of inactive mailbox> | Guid FL` <br/><br/> **Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox -<identity of active mailbox> | Guid FL`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-Mailbox - <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | Guid FL'           | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Indique si le fichier PST doit être importé dans la boîte aux lettres d’archivage de l’utilisateur. Il existe deux options :<br/> **FALSE** Importe le fichier PST à la boîte aux lettres principale de l’utilisateur.  <br/> **La valeur TRUE** Importe le fichier PST boîte aux lettres d’archive de l’utilisateur.  <br/>  Si vous laissez ce paramètre vide, le fichier est importé dans la boîte aux lettres principale de l’utilisateur.  <br/><br/> **Remarque :** Pour importer un fichier PST dans une boîte aux lettres d’archive en nuage pour un utilisateur de boîte aux lettres principale est locale, juste spécifiez **TRUE** pour ce paramètre et spécifiez l’adresse de messagerie pour la boîte aux lettres locale de l’utilisateur pour le `Mailbox` paramètre.           | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Spécifie le dossier de boîte aux lettres importé dans le fichier PST.  <br/>  Si vous laissez ce paramètre vide, le fichier PST est importé dans un nouveau dossier nommé **importés** situé à la racine de la boîte aux lettres (le même niveau que le dossier boîte de réception et les autres dossiers de boîte aux lettres par défaut).  <br/>  Si vous spécifiez `/`, éléments dans le fichier PST seront importées directement dans le dossier boîte de réception de l’utilisateur.  <br/>  Si vous spécifiez `/<foldername>`, éléments dans le fichier PST seront importées dans un sous-dossier nommé * \<foldername\> * . Par exemple, si vous avez utilisé `/ImportedPst`, éléments est importées dans un sous-dossier nommé **ImportedPst**. Ce sous-dossier sera situé dans le dossier boîte de réception de l’utilisateur.<br/><br/> **Conseil :** Pensez à exécuter plusieurs lots de test pour tester ce paramètre afin de déterminer le meilleur emplacement de dossier pour importer des fichiers pst.           |(Laisser vide)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Ce paramètre facultatif spécifie une valeur numérique pour la page de codes à utiliser pour l’importation des fichiers PST dans le format de fichier ANSI. Ce paramètre est utilisé pour l’importation des fichiers PST d’organisations chinois, japonais et coréen (CJC), car ces langues utilisent généralement un jeu de caractères codés sur deux octets (DBCS) pour le codage de caractères. Si ce paramètre n’est pas utilisé pour importer des fichiers PST pour les langues qui utilisent DBCS pour les noms de dossier de boîte aux lettres, les noms de dossiers sont souvent tronqués après leur importation. Pour obtenir la liste de valeurs prises en charge à utiliser pour ce paramètre, voir [Identificateurs de Page de Code](https://go.microsoft.com/fwlink/p/?LinkId=328514).<br/><br/> **Remarque :** Comme indiqué, ce paramètre est facultatif et n’avez pas à inclure dans le fichier CSV. Ou vous pouvez inclure et laissez la valeur vide pour une ou plusieurs lignes.           |(Laisser vide)  <br/> Ou  <br/>  `932`(qui est l’identificateur de page de codes pour le japonais ANSI/OEM)  <br/> |
    | `SPFileContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPManifestContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPSiteUrl` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
  
## <a name="step-8-create-a-pst-import-job-in-office-365"></a>Étape 8 : Créer une tâche d’importation PST dans Office 365

La dernière étape consiste à créer le travail d’importation PST dans le service d’importation dans Office 365. Comme expliqué précédemment, vous envoyez le fichier de mappage d’importation PST que vous avez créé à l’étape 7. Après avoir créé la nouvelle tâche, le service d’importation utilise les informations dans le fichier de mappage d’annulation-chiffrer et importer les fichiers PST (que vous avez téléchargé vers Office 365 à l’étape 5) dans la boîte aux lettres de l’utilisateur spécifié. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 avec les informations d’identification pour un compte d’administrateur de votre organisation Office 365.
    
3. Dans le volet gauche, cliquez sur **la gouvernance des données** , puis cliquez sur **Importer**.
    
4. Sur la page **Importation**, cliquez sur **Ouvrir le service d’importation**.
    
5. Dans la page **Importer des données dans Office 365** , cliquez sur **Nouveau travail**![ajouter une icône](media/ITPro-EAC-AddIcon.gif), puis cliquez sur **télécharger les messages électroniques (fichiers PST)**.
    
6. Sur la page **Télécharger les fichiers sur le réseau**, sélectionnez **J’ai terminé de télécharger mes fichiers** et **J’ai accès au fichier de mappage**, puis cliquez sur **Suivant**.  
    
7. Entrez le nom de la tâche d’importation PST, puis cliquez sur **Suivant**.
    
8. Cliquez sur **Ajouter** ![ajouter une icône](media/ITPro-EAC-AddIcon.gif) pour sélectionner le fichier PST mappage que vous avez créé à l’étape 7. 
    
9. Lorsque le nom du fichier CSV apparaît dans la liste, sélectionnez-le, puis cliquez sur **Valider** pour vérifier que votre fichier CSV ne contient pas d’erreurs.  
    
    > [!NOTE]
    > Précédente comme indiqué, lorsque les fichiers PST sont chiffrées, un `.pfile` extension est ajoutée au nom de fichier PST. Vous devez ajouter le `.pfile` extension sur le nom de fichier des fichiers dans le fichier CSV. Si vous n’est pas le cas, la validation du fichier CSV échouera. 
  
    Le fichier CSV doit être validé pour créer la tâche d’importation PST. Si la validation échoue, cliquez sur le lien **Non valide** dans la colonne **État**. Une copie de votre fichier de mappage d’importation PST s’ouvre avec un message d’erreur pour chaque ligne du fichier ayant échoué. 
    
10. Une fois le fichier de mappage PST validé, lisez les conditions d’utilisation, puis cliquez sur la case à cocher.
    
11. Cliquez sur **Terminer** pour envoyer la tâche. 
    
    Le travail est affiché dans la liste des tâches d’importation PST dans la page **Importer des données dans Office 365** . 
    
12. Sélectionnez la tâche, cliquez sur **Actualiser**![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations d’état qui s’affiche dans le volet détails. 
    
13. Dans le volet d’informations, cliquez sur **Afficher les détails** pour consulter l’état le plus récent de la tâche sélectionnée. 
 
## <a name="more-information"></a>Plus d'informations

- Pourquoi importer des fichiers PST vers Office 365 ?
    
  - C’est un bon moyen de migration de messagerie de votre organisation vers Office 365.
    
  - Cela vous aide à répondre aux besoins de conformité de votre organisation en vous permettant de réaliser les opérations suivantes :
    
  - Activer les boîtes aux lettres d’archivage pour donner aux utilisateurs un espace de stockage de boîte aux lettres supplémentaire.
    
  - Placer des boîtes aux lettres en conservation inaltérable pour ne pas perdre le contenu.
    
  - Utiliser les outils de découverte électronique Microsoft pour rechercher du contenu dans des boîtes aux lettres.
    
  - Adopter des stratégies de rétention pour contrôler la durée de conservation du contenu des boîtes aux lettres.
    
  - Journal d’audit de recherche Office 365 pour les événements liés à la boîte aux lettres.
    
  - Il vous aide à protéger contre la perte de données. Les fichiers PST qui sont importés vers des boîtes aux lettres Office 365 héritent les fonctionnalités de haute disponibilité d’Exchange Online, au lieu de stockage des données sur l’ordinateur d’un utilisateur.
    
  - L’utilisateur peut accéder aux données à partir de n’importe quel périphérique, car elles sont stockées dans le cloud.
    
- Voici un exemple des clés, des ID et des URL qui sont obtenus lors des étapes 2, 3 et 4. Cet exemple montre comment contient également la syntaxe de la commande que vous exécutez dans l’outil O365ImportTool.exe pour chiffrer et PST de téléchargement de fichiers vers Office 365. N’oubliez pas de prendre des précautions pour protéger ces simplement comme vous le feriez protéger les mots de passe ou d’autres informations relatives à la sécurité.
    
  ```
  Symmetric key: l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=

  BPOSId: 42745b33-2a5c-4726-8a2a-ca43caa0f74b

  LicensingIntranetDistributionPointUrl (RMS licensing location): https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing
  
  SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D
  
  O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL from the SAS URL> /upload-destSAS:<SAS key from the SAS URL>
  
  EXAMPLES
  
  This example uploads PST files to the root of the Azure storage location:

  O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b /protect-ownerid:45beb445-4d06-47df-8e61-6ca1a88a080e /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
  
  This example uploads PST files to a subfolder named EncryptedPSTs  in the Azure storage location:
  
  O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b /protect-ownerid:45beb445-4d06-47df-8e61-6ca1a88a080e /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
  ```

- Comme expliqué précédemment, le service Office 365 importation Active le blocage de rétention définition (pour une durée indéterminée) une fois que les fichiers PST sont importées dans une boîte aux lettres. Cela signifie que la propriété *RentionHoldEnabled* est définie sur `True` afin que la stratégie de rétention attribuée à la boîte aux lettres ne sera pas traitée. Ainsi, le temps de propriétaire de boîte aux lettres pour gérer les messages nouvellement importées en empêchant une suppression ou une stratégie d’archivage de supprimer ou de l’archivage des messages plus anciens. Voici quelques étapes à que suivre pour gérer ce blocage de rétention : 
    
  - Après un certain temps, vous pouvez désactiver le blocage de rétention en exécutant la `Set-Mailbox -RetentionHoldEnabled $false` commande. Pour plus d’informations, voir [archive une boîte aux lettres sur la rétention](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
  - Vous pouvez configurer le blocage de rétention afin qu’il est désactivé sur une date dans le futur. Pour cela, exécutez le `Set-Mailbox -EndDateForRetentionHold <date>` commande. Par exemple, en supposant que la date du jour est le 1 juillet 2016 et vous souhaitez le blocage de rétention désactivé des 30 derniers jours, vous exécuterez la commande suivante : `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. Dans ce scénario, laissez la propriété *RentionHoldEnabled* définie sur `True`. Pour plus d’informations, voir [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
  - Vous pouvez modifier les paramètres de la stratégie de rétention qui est affectée à la boîte aux lettres afin que les anciens éléments qui ont été importés ne sont pas immédiatement supprimés ou déplacés vers la boîte aux lettres de l’utilisateur archive. Par exemple, vous pouvez augmenter l’âge de rétention pour une stratégie de suppression ou d’archivage qui est affectée à la boîte aux lettres. Dans ce scénario, vous devez désactiver le blocage de rétention sur la boîte aux lettres une fois que vous avez modifié les paramètres de la stratégie de rétention. Pour plus d’informations, voir [configurer une stratégie d’archivage et de suppression des boîtes aux lettres dans votre organisation Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
