---
title: Utiliser le chargement réseau pour importer des fichiers PST chiffrés via RMS dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 84a595b8-cd77-4f66-ac52-57a33ddd4773
description: Découvrez comment utiliser le chargement réseau pour importer des fichiers PST chiffrés RMS dans des boîtes aux lettres utilisateur dans Office 365.
ms.openlocfilehash: 46f77f3fe173da23e08284884bb85c69ab53f710
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958295"
---
# <a name="use-network-upload-to-import-rms-encrypted-pst-files-to-office-365"></a>Utiliser le chargement réseau pour importer des fichiers PST chiffrés via RMS dans Office 365

**Cet article est destiné aux administrateurs. Essayez-vous d'importer des fichiers PST dans votre propre boîte aux lettres? Voir [importer le courrier, les contacts et le calendrier à partir d'un fichier. pst Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)**
   
Utilisez l'option de chargement réseau et le service d'importation Office 365 pour importer des fichiers PST dans des boîtes aux lettres utilisateur. Le chargement réseau signifie que vous téléchargez les fichiers PST dans une zone de stockage temporaire dans le Cloud de Microsoft. Le service d'importation Office 365 copie les fichiers PST de la zone de stockage vers les boîtes aux lettres des utilisateurs cibles. Une nouvelle fonctionnalité du service d'importation vous permet de chiffrer vos fichiers PST avant de les télécharger et de les stocker sur le Cloud Microsoft. Ces fichiers seront déchiffrés une fois importés dans les boîtes aux lettres d’utilisateur. 
  
Voici les étapes à suivre pour chiffrer et importer des fichiers PST dans des boîtes aux lettres Office 365:
  
[Étape 1: configurer Azure Rights Management pour l'importation des fichiers PST](#step-1-set-up-azure-rights-management-for-pst-import)

[Étape 2 : Générer une clé de chiffrement pour l’importation PST](#step-2-generate-an-encryption-key-for-pst-import)

[Étape 3: obtenir l'ID de client RMS et l'URL de licence](#step-3-obtain-rms-tenant-id-and-licensing-url)

[Étape 4: Télécharger les outils d'importation PST et copier l'URL SAS](#step-4-download-the-pst-import-tools-and-copy-the-sas-url)

[Étape 5: chiffrer et charger vos fichiers PST dans Office 365](#step-5-encrypt-and-upload-your-pst-files-to-office-365)

[Module Étape 6: afficher la liste des fichiers PST téléchargés vers Office 365](#optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Étape 7: créer le fichier de mappage d'importation PST](#step-7-create-the-pst-import-mapping-file)

[Étape 8 : Créer une tâche d’importation PST dans Office 365](#step-8-create-a-pst-import-job-in-office-365)
  
> [!IMPORTANT]
> Vous devez effectuer les étapes 1 à 4 une seule fois pour configurer et configurer votre organisation pour chiffrer et importer des fichiers PST dans des boîtes aux lettres Office 365. Après avoir effectué ces étapes, suivez les étapes 5 à 8 chaque fois que vous souhaitez chiffrer, télécharger et importer un lot de fichiers PST. 
  
Pour plus d'informations sur l'importation de données dans Office 365, consultez [la rubrique vue d'ensemble de l'importation des fichiers PST de votre organisation dans office 365](importing-pst-files-to-office-365.md).
  
## <a name="before-you-begin"></a>Avant de commencer

- Vous devez disposer du rôle d'exportation d'importation de boîte aux lettres dans Exchange Online pour importer des fichiers PST dans des boîtes aux lettres Office 365. Par défaut, ce rôle n'est affecté à aucun groupe de rôles dans Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. Pour plus d'informations, consultez les sections «ajouter un rôle à un groupe de rôles» ou «créer un groupe de rôles» dans [gérer des groupes de rôles](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    De plus, pour créer des travaux d'importation dans le centre de sécurité & Compliance Center, l'une des conditions suivantes doit être vraie:
    
  - Vous devez disposer du rôle destinataires de messagerie dans Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Ou
    
  - Vous devez être un administrateur général dans votre organisation Office 365.
    
  > [!TIP]
  > EnVisagez de créer un nouveau groupe de rôles dans Exchange Online spécialement destiné à l'importation de fichiers PST dans Office 365. Pour le niveau minimal de privilèges requis pour importer des fichiers PST, attribuez les rôles importation de boîte aux lettres et destinataires des messages au nouveau groupe de rôles, puis ajoutez des membres. 
  
- Vous devez stocker les fichiers PST que vous souhaitez importer vers Office 365 sur un serveur de fichiers ou un dossier partagé de votre organisation. À l'étape 5, vous allez exécuter l'ImportTool Office 365, qui chiffre et télécharge les fichiers PST stockés sur ce serveur de fichiers ou dossier partagé vers Office 365.
    
- Cette procédure nécessite la copie et l’enregistrement d’une clé de chiffrement, d’une clé de stockage, de clés d’identification et d’URL. Ces informations seront utilisées à l'étape 5 pour chiffrer et charger vos fichiers PST. Veillez à prendre toutes les précautions nécessaires pour protéger ces clés, tout comme vous le feriez avec vos mots de passe ou d’autres informations de sécurité. Par exemple, vous pouvez les enregistrer dans un document Microsoft Word protégé par mot de passe ou dans un lecteur USB chiffré. Consultez la section [Plus d’informations](#more-information) pour obtenir un exemple de ces clés, ID et URL. 
    
- Vous pouvez importer des fichiers PST dans une boîte aux lettres inactive dans Office 365. Pour ce faire, spécifiez le GUID de la boîte aux lettres inactive dans le `Mailbox` paramètre dans le fichier de mappage d'importation PST. Pour plus d'informations, voir l' [étape 7](#step-7-create-the-pst-import-mapping-file) . 
    
- Dans un déploiement hybride Exchange, vous pouvez importer des fichiers PST dans une boîte aux lettres d'archivage informatique pour un utilisateur dont la boîte aux lettres principale est locale. Pour ce faire, procédez comme suit dans le fichier de mappage d'importation PST:
    
  - Spécifiez l'adresse de messagerie de la boîte aux lettres locale de l' `Mailbox` utilisateur dans le paramètre. 
    
  - Spécifiez la valeur **true** dans `IsArchive` le paramètre. 
    
    Pour plus d'informations, voir l' [étape 7](#step-7-create-the-pst-import-mapping-file) . 
    
- Une fois que les fichiers PST sont importés dans une boîte aux lettres Office 365, le paramètre de blocage de rétention de la boîte aux lettres est activé pour une durée indéterminée. Cela signifie que la stratégie de rétention attribuée à la boîte aux lettres ne sera pas traitée tant que vous n'aurez pas désactivé le blocage de rétention ou défini une date pour désactiver la conservation. Pourquoi effectuer cette opération? Si les messages importés dans une boîte aux lettres sont obsolètes, ils peuvent être supprimés définitivement (purgés) car leur période de rétention a expiré en fonction des paramètres de rétention configurés pour la boîte aux lettres. Lorsque la boîte aux lettres est mise en attente de rétention, le propriétaire de la boîte aux lettres peut gérer ces messages nouvellement importés ou modifier les paramètres de rétention pour la boîte aux lettres. Consultez la section [plus d'informations](#more-information) pour obtenir des suggestions sur la gestion du blocage de rétention. 
    
- Si vous n'avez pas besoin de chiffrer vos fichiers PST avant de les télécharger vers Office 365, consultez la rubrique [utiliser le chargement réseau pour importer des fichiers PST dans office 365](use-network-upload-to-import-pst-files.md).
    
- Pour obtenir des questions fréquemment posées sur l'utilisation du chargement réseau pour importer des fichiers PST dans Office 365, consultez la rubrique [FAQ sur l'importation de fichiers PST dans office 365](faqimporting-pst-files-to-office-365.md).
  
## <a name="step-1-set-up-azure-rights-management-for-pst-import"></a>Étape 1 : Configurer Azure Rights Management pour importer des fichiers PST 

L'importation PST utilise la fonctionnalité de chiffrement fournie par le service Azure Rights Management (Azure RMS) dans Office 365. Cela vous permet de chiffrer les fichiers PST avant de les télécharger vers Office 365. 
  
La configuration d'Azure RMS pour l'importation PST se compose de trois étapes:
  
- [Activation d'Azure RMS](#activating-azure-rms)
    
- [Configuration de RMS dans Exchange Online](#configuring-rms-in-exchange-online)
    
- [Installation du client Active Directory RMS](#installing-the-active-directory-rms-client)
    
### <a name="activating-azure-rms"></a>Activation d'Azure RMS

Azure RMS est désactivé par défaut, mais vous ou un autre administrateur de votre organisation l'avez peut-être activé. Suivez les instructions relatives à l'activation de la [gestion des droits Azure](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) pour installer et activer Azure DRM.
  
### <a name="configuring-rms-in-exchange-online"></a>Configuration de RMS dans Exchange Online

Une fois que vous avez activé le service gestion des droits, l'étape suivante consiste à configurer la gestion des droits relatifs à l'information (IRM) dans Exchange Online pour utiliser Azure RMS. Pour plus d'informations, consultez la rubrique [configurer la gestion des droits relatifs à l'information pour utiliser Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=394816).
  
1. [Connectez-vous à Exchange Online à l'aide de Remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554 ).
    
2. Exécutez la commande suivante pour définir l’URL de partage de la clé RMS.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation <RMS key sharing location>
    ```

    Reportez-vous au tableau suivant pour déterminer l’emplacement de partage de la clé RMS correspondant à l’emplacement de votre organisation.
    
    |**Emplacement**|**Emplacement de partage de la clé RMS**|
    |:-----|:-----|
    |Amérique du Nord  <br/> | `https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Union européenne  <br/> | `https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Région  <br/> | `https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Amérique du Sud  <br/> | `https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Office 365 Secteur Public (nuage communautaire propre aux gouvernements)  <br/> | `https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>0,1</sup> <br/> |
   
    > [!NOTE]
    > <sup>1</sup> seuls les clients ayant acheté les références Office 365 pour le gouvernement (Cloud communautaire du gouvernement) doivent utiliser cet emplacement de partage de clé RMS. 
  
    Par exemple, cette commande configure l'emplacement de partage de la clé RMS Online dans Exchange Online pour un client situé en Amérique du Nord.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
    ```

3. Exécutez la commande suivante pour importer un domaine de publication approuvé (publication approuvé) à partir de RMS Online vers votre organisation Office 365. 
    
    ```
    Import-RMSTrustedPublishingDomain -RMSOnline -Name "RMS Online"
    ```

    Un domaine de publication approuvé contient les paramètres nécessaires à l’utilisation des fonctionnalités RMS dans votre organisation, notamment les fichiers PST de chiffrement.  
    
4. Exécutez la commande suivante pour activer la gestion des droits relatifs à l'information pour votre organisation Office 365.
    
    ```
    Set-IRMConfiguration -InternalLicensingEnabled $true
    ```

### <a name="installing-the-active-directory-rms-client"></a>Installation du client Active Directory RMS

Enfin, vous devez télécharger le client RMS (Rights Management Services) 2.1. Ce logiciel permet de protéger l'accès à Azure RMS et de protéger les informations transitant par des applications qui utilisent Azure RMS. Installez le client RMS sur le même ordinateur que celui que vous utiliserez pour chiffrer et télécharger les fichiers PST à l'étape 5. 
  
1. Télécharger le [client du service gestion des droits 2,1](https://www.microsoft.com/en-us/download/details.aspx?id=38396).
    
2. Exécutez l’Assistant du client Active Directory Rights Management Service 2.1 pour installer le client.

## <a name="step-2-generate-an-encryption-key-for-pst-import"></a>Étape 2 : Générer une clé de chiffrement pour l’importation PST

Une fois que vous avez configuré Azure RMS, l'étape suivante consiste à générer une clé de chiffrement (appelée clé symétrique) qui sera utilisée pour chiffrer les fichiers PST que vous téléchargez vers Office 365. Pour ce faire, vous devez ajouter le service d'importation PST en tant que principal de service dans Azure Active Directory. L'ajout de cette application en tant que principal de service permet au service d'importation PST de s'authentifier directement auprès d'Azure Active Directory lorsque vous téléchargez les fichiers PST vers l'emplacement de stockage Azure à l'étape 5.
  
1. Démarrez le module Azure Active Directory pour Windows PowerShell.
    
2. Exécutez la commande suivante pour vous connecter au service Microsoft Online.
    
    ```
    Connect-MsolService
    ```

3. Entrez les informations d'identification d'un compte d'administrateur dans votre organisation Office 365, puis cliquez sur **OK**.
    
4. Exécutez la commande suivante pour générer une clé de chiffrement (appelée clé symétrique). Pour cela, vous devez créer un principal de chiffrement PST.
    
    ```
    New-MsolServicePrincipal -DisplayName PstEncryptionPrincipal
    ```

    Le système affiche la clé symétrique et les propriétés du nouveau principal de chiffrement PST.
    
    ![Copiez et enregistrez la clé symétrique qui est affichée](media/0003fdea-dace-41d2-b49d-f5c98c6230ca.png)
  
5. Copiez la clé symétrique dans un fichier texte ou Word. Comme indiqué précédemment, veillez à prendre les précautions nécessaires pour protéger ce fichier. Étant donné que la clé symétrique n’est affichée qu’une seule fois, vous pouvez également effectuer une capture d’écran de la fenêtre et l’enregistrer dans le même fichier.  
    
    > [!IMPORTANT]
    > Une fois le principal de chiffrement PST créé, vous ne pourrez pas récupérer la clé symétrique à l’aide de la cmdlet **Get-MsolServicePrincipal**. C’est pourquoi vous devez enregistrer la clé. 
  
Conservez le module Azure Active Directory pour Windows PowerShell ouvert et connecté au service Microsoft Online. Vous devrez exécuter une commande dans cette fenêtre à l’étape suivante.

## <a name="step-3-obtain-rms-tenant-id-and-licensing-url"></a>Étape 3: obtenir l'ID de client RMS et l'URL de licence

L'étape suivante consiste à obtenir l'URL de l'ID de client et de l'emplacement des licences pour le service Azure RMS pour votre organisation. Copiez et enregistrez les informations dans le fichier contenant la clé symétrique obtenue à l’étape 2. L'ID et l'URL seront utilisés à l'étape 5 pour chiffrer vos fichiers PST.
  
1. Dans le module Azure Active Directory pour Windows PowerShell (qui est connecté au service Microsoft Online), exécutez la commande suivante pour vous connecter au service Azure RMS dans votre organisation Office 365.
    
    ```
    Connect-AadrmService 
    ```

2. Entrez les informations d'identification d'un compte d'administrateur dans votre organisation Office 365, puis cliquez sur **OK**.
    
3. Exécutez la commande suivante pour afficher l'ID de client pour le service Azure RMS dans votre organisation Office 365.
    
    ```
    Get-AadrmConfiguration | FL BPOSId
    ```

    Copiez et enregistrez la valeur de `BPOSId` la propriété. 
    
4. Exécutez la commande suivante pour afficher l'emplacement de gestion des licences pour votre service Azure RMS.
    
    ```
    Get-AadrmConfiguration | FL LicensingIntranetDistributionPointUrl
    ```

    Copiez et enregistrez la valeur de `LicensingIntranetDistributionPointUrl` la propriété. 

## <a name="step-4-download-the-pst-import-tools-and-copy-the-sas-url"></a>Étape 4: Télécharger les outils d'importation PST et copier l'URL SAS

À présent que vous avez configuré Azure RMS et obtenu les ID nécessaires au chiffrement des fichiers PST, l'étape suivante consiste à télécharger et à installer les outils que vous exécuterez à l'étape 5 pour chiffrer et télécharger des fichiers PST dans Office 365. Ces outils sont l'outil AzCopy d'Azure et l'outil de chiffrement des données Office 365. Vous copierez également l'URL SAS de votre organisation. Cette URL est une combinaison de l'URL réseau de l'emplacement de stockage Azure dans le Cloud Microsoft pour votre organisation et d'une clé SAS (Shared Access signature). Cette clé vous fournit les autorisations nécessaires pour télécharger des fichiers PST vers votre emplacement de stockage Azure. Enregistrez-le dans le fichier dans lequel vous avez copié les autres informations à l'étape 2 et à l'étape 3. Comme indiqué précédemment, prenez des précautions pour protéger l'URL SAS. 
  
> [!IMPORTANT]
> Vous devez utiliser Azure AzCopy version 5,0 pour télécharger des fichiers PST vers l'emplacement de stockage Azure. Les versions plus récentes de l'outil AzCopy ne sont pas prises en charge pour l'importation de fichiers PST dans Office 365. Assurez-vous de télécharger l'outil AzCopy à partir de la page **Télécharger des fichiers sur le réseau** en suivant les procédures décrites dans cette étape. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide des informations d'identification d'un compte d'administrateur de votre organisation Office 365.
    
3. Dans le volet de gauche, cliquez sur **gouvernance des données** , puis sur **Importer**.
    
4. Sur la page **Importation**, cliquez sur **Ouvrir le service d’importation**.
    
5. sur la page **importer des données dans Office 365** , cliquez sur nouvelle icône](media/ITPro-EAC-AddIcon.gif)ajouter **un travail** ![, puis cliquez sur **télécharger des messages électroniques (fichiers PST)**.
    
6. Sur la page **Télécharger des fichiers sur le réseau** , à l'étape 2, cliquez sur **afficher l'URL SAS de chargement réseau**.
    
7. Une fois l'URL affichée, copiez-la et enregistrez-la dans le fichier où vous avez enregistré les autres clés. Veillez à copier la totalité de l’URL. 
    
8. À l'étape 3, cliquez sur **Télécharger l'outil Azure AzCopy** pour télécharger et installer l'outil AzCopy Azure. 
    
9. Dans la fenêtre contextuelle, cliquez sur **Exécuter** pour installer l’outil AzCopy d’Azure. 
    
    > [!IMPORTANT]
    > Veillez à installer l'outil Azure AzCopy à l'emplacement par défaut, qui `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` se trouve sur un ordinateur exécutant Windows 64 bits. Cela est dû au fait que lorsque vous exécutez le O365ImportTool. exe à l'étape 5, il recherche l'outil AzCopy à cet emplacement. 
  
10. Une fois que vous avez installé l'outil Azure AzCopy, cliquez sur **Télécharger l'outil de chiffrement de données et d'importation Office 365**.
    
11. Dans la fenêtre contextuelle, cliquez sur **Enregistrer** \> **Enregistrer sous** pour enregistrer le fichier O365ImportTool. zip dans un dossier sur votre ordinateur local. 
    
12. Décompressez le fichier O365ImportTool.zip.
    
13. Cliquez sur **Annuler** pour fermer la page **Télécharger des fichiers sur le réseau** . 
 
## <a name="step-5-encrypt-and-upload-your-pst-files-to-office-365"></a>Étape 5: chiffrer et charger vos fichiers PST dans Office 365

Une fois que vous avez terminé les étapes 1 à 4, vous êtes prêt à utiliser l'outil O365ImportTool. exe pour chiffrer et télécharger des fichiers PST dans Office 365. Cet outil chiffre vos fichiers PST, puis les télécharge et les stocke dans un emplacement de stockage Azure dans le Cloud Microsoft. Pour cela, les fichiers PST doivent se trouver sur un dossier partagé ou un serveur de fichiers dans votre organisation. Il s’agit du répertoire source mentionné dans la procédure suivante. Chaque fois que vous exécutez l’outil O365ImportTool.exe, vous devez spécifier un répertoire source différent. 
  
1. Ouvrez une invite de commandes sur votre ordinateur local.
    
2. Accédez au répertoire où vous avez installé l’outil O365ImportTool.exe à l’étape 4.
    
3. Exécutez la commande suivante pour chiffrer et télécharger des fichiers PST dans Office 365.
    
    ```
    O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL> /upload-destSAS:<SAS key>
    ```

    Le tableau suivant décrit les paramètres et leurs valeurs requises. Notez que les informations obtenues lors des étapes précédentes sont utilisées pour remplir les valeurs de ces paramètres.
    
    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `/srcdir:` <br/> |Spécifie le répertoire source de votre organisation qui contient les fichiers PST qui seront chargés vers Office 365.  <br/> | `/srcdir:\\FILESERVER01\PSTs` <br/> |
    | `/protect-rmsserver:` <br/> |Spécifie l'emplacement de la gestion des licences pour votre service Azure RMS. Utilisez la valeur de la `LicensingIntranetDistributionPointUrl` propriété que vous avez obtenue à l'étape 3. N'oubliez pas de placer la valeur de ce paramètre entre guillemets doubles ("").  <br/> | `/protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing"` <br/> |
    | `/protect-tenantid:` <br/> |Spécifie l'identité de votre organisation Azure RMS. Utilisez la valeur de la `BPOSId` propriété que vous avez obtenue à l'étape 3.  <br/> | `/protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b` <br/> |
    | `/protect-key:` <br/> |Indique la clé symétrique obtenue à l’étape 2. N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/> | `/protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867="` <br/> |
    | `/transfer:` <br/> |Indique si vous téléchargez des fichiers PST sur le réseau ou les expédiez sur un disque dur. La valeur `upload` indique que vous téléchargez les fichiers sur le réseau. La valeur `drive` indique que vous expédiez les fichiers PST sur un disque dur.  <br/> | `/transfer:upload` <br/> |
    | `/upload-dest:` <br/> |Spécifie la destination dans Office 365 où vos fichiers PST seront téléchargés; Il s'agit de l'emplacement de stockage Azure pour votre organisation. La valeur de ce paramètre est constituée de l'URL de chargement réseau à partir de l'URL SAS que vous avez copiée à l'étape 4. N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/><br/> **Conseil:** Module Vous pouvez spécifier un sous-dossier dans l'emplacement de stockage Azure dans lequel télécharger les fichiers PST chiffrés. Pour ce faire, vous devez ajouter un emplacement de sous-dossier (après «ingestiondata») dans l'URL de chargement réseau. Le premier exemple ne spécifie pas un sous-dossier; Cela signifie que les fichiers PST seront téléchargés vers la racine (nommé *ingestiondata* ) de l'emplacement de stockage Azure. Le deuxième exemple télécharge les fichiers PST dans un sous-dossier (nommé *EncryptedPSTs* ) dans l'emplacement de stockage Azure.           | `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata"` <br/> Ou  <br/>  `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs"` <br/> |
    | `/upload-destSAS:` <br/> |Spécifie la clé SAS de votre organisation. La valeur de ce paramètre est constituée de la clé SAS de l'URL SAS que vous avez copiée à l'étape 4. Notez que le premier caractère de la clé SAS est un point d'interrogation («?»). N’oubliez pas de placer la valeur de ce paramètre entre guillemets doubles (" ").  <br/> | `/upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/recurse` <br/> |Ce commutateur facultatif spécifie le mode récursif de sorte que l'outil O365ImportTool. exe copie les fichiers PST situés dans des sous-dossiers du répertoire source spécifié par le `/srcdir:` paramètre.  <br/><br/> **Remarque:** Si vous incluez ce commutateur, les fichiers PST dans les sous-dossiers auront un nom de chemin d'accès de fichier différent dans l'emplacement de stockage Azure après leur téléchargement. Vous devrez spécifier le chemin d’accès exact du fichier CSV créé à l’étape 7.           | `/recurse` <br/> |
   
    Voici un exemple de la syntaxe de l’outil O365ImportTool.exe qui reprend les valeurs réelles de chaque paramètre :
    
    ```
    O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b  /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
    ```

    Une fois la commande exécutée, les messages d’état affichent la progression du processus de chiffrement et de téléchargement des fichiers PST. Un message d’état final affiche le nombre total de fichiers qui ont été chiffrés et téléchargés.  
    
    > [!TIP]
    > Après avoir correctement exécuté la commande O365ImportTool.exe et vérifié que tous les paramètres sont corrects, enregistrez une copie de la syntaxe de la ligne de commande dans le même fichier (sécurisé) où vous avez copié les informations obtenues dans les étapes précédentes. Ensuite, vous pouvez copier et coller cette commande dans une invite de commandes chaque fois que vous souhaitez exécuter l'outil O365ImportTool. exe pour chiffrer et télécharger des fichiers PST dans Office 365. Les seules valeurs que vous devrez peut-être modifier sont celles pour `/srcdir:` les `/upload-dest:` paramètres et. 
  
## <a name="optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Module Étape 6: afficher la liste des fichiers PST téléchargés vers Office 365

Au cours d'une étape facultative, vous pouvez installer et utiliser l'Explorateur de stockage Microsoft Azure (il s'agit d'un outil gratuit open source) pour afficher la liste des fichiers PST que vous avez téléchargés vers le BLOB Azure. Il y a trois bonnes raisons de procéder comme suit:
  
- Vérifiez que les fichiers PST du dossier partagé ou du serveur de fichiers de votre organisation ont bien été téléchargés vers le BLOB Azure.

- Vérifiez que les fichiers PST sont chiffrés. Les fichiers PST chiffrés ont `.pfile` une extension ajoutée au nom de fichier PST; par exemple, `pilarp.pst.pfile`.
    
- Vérifiez le nom de fichier (et le chemin d'accès du sous-dossier si vous en avez inclus un) pour chaque fichier PST téléchargé vers le BLOB Azure. Cela s’avère très utile lorsque vous créez le fichier mappage PST à l’étape suivante, car vous devez spécifier le chemin d’accès de dossier et le nom de fichier pour chaque fichier PST. La vérification de ces noms peut permettre de réduire les erreurs potentielles dans votre fichier de mappage PST.
    
L'Explorateur de stockage Microsoft Azure est en mode aperçu. 
  
 > [!IMPORTANT]
>  Vous ne pouvez pas utiliser l'Explorateur de stockage Azure pour télécharger ou modifier des fichiers PST. La seule méthode prise en charge pour l'importation de fichiers PST dans Office 365 consiste à utiliser AzCopy. De plus, vous ne pouvez pas supprimer les fichiers PST que vous avez téléchargés vers le BLOB Azure. Si vous tentez de supprimer un fichier PST, vous recevrez une erreur indiquant que vous ne disposez pas des autorisations requises. Notez que tous les fichiers PST sont automatiquement supprimés de votre zone de stockage Azure. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created. 
  
Pour installer Azure Storage Explorer et vous connecter à votre zone de stockage Azure:
  
1. Téléchargez et installez l' [outil Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Démarrez l'Explorateur de stockage Microsoft Azure, cliquez avec le bouton droit sur **comptes de stockage** dans le volet de gauche, puis cliquez sur **se connecter à Azure Storage**. 
    
    ![Cliquez avec le bouton droit sur comptes de stockage, puis cliquez sur se connecter à Azure Storage](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Dans la zone située sous **se connecter à Azure Storage**, collez l'URL SAS que vous avez obtenue à l'étape 4, puis cliquez sur **suivant**. 
    
    ![Collez l'URL SAS dans la zone de la page se connecter à Azure Storage.](media/5d034128-e087-48e1-9ebc-4c9fa262d5b7.png)
  
4. Sur la page **Résumé de connexion** , vous pouvez passer en revue les informations de connexion, puis cliquer sur **se connecter**. 
    
5. Sous **comptes de stockage**, développez le nœud **(service SAS)** , puis le nœud **conteneurs BLOB** . 
    
6. Cliquez avec le bouton droit sur **ingestiondata**, puis cliquez sur **Ouvrir l’éditeur de conteneur d’objets blob**.
    
    ![Cliquez avec le bouton droit sur ingestiondata, puis cliquez sur Ouvrir l’éditeur de conteneur d’objets blob](media/f50eee30-9202-4efc-904a-2895a0bc388d.png)
  
    La zone de stockage Azure, avec une liste des fichiers PST que vous avez téléchargés à l'étape 5, s'affiche.
    
    ![L’explorateur de stockage Azure affiche la liste des fichiers PST que vous avez téléchargés](media/a448ae43-e744-4153-8304-22b59e93883c.png)
  
7. Lorsque vous avez terminé d'utiliser l'Explorateur de stockage Microsoft Azure, cliquez avec le bouton droit sur **ingestiondata**, puis cliquez sur détacher pour vous déconnecter de votre zone de stockage Azure. **** Dans le cas contraire, vous recevrez une erreur la prochaine fois que vous tenterez de joindre un élément. 
    
    ![Cliquez avec le bouton droit de la souris sur ingestion, puis cliquez sur Détacher pour vous déconnecter de votre zone de stockage Azure](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-7-create-the-pst-import-mapping-file"></a>Étape 7: créer le fichier de mappage d'importation PST

Une fois que les fichiers PST ont été chiffrés et téléchargés dans l'emplacement de stockage Azure de votre organisation Office 365, l'étape suivante consiste à créer un fichier de valeurs séparées par des virgules (CSV) qui spécifie les boîtes aux lettres utilisateur dans lesquelles les fichiers PST seront importés. Ce fichier PST est envoyé à l’étape suivante lors de la création d’une tâche d’importation PST.
  
1. [Téléchargez une copie du fichier de mappage d'importation PST](https://go.microsoft.com/fwlink/p/?LinkId=544717). 
    
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

    La première ligne ou ligne d’en-tête du fichier CSV répertorie les paramètres qui seront utilisés par le service d’importation pour importer les fichiers PST dans les boîtes aux lettres d’utilisateur. Les noms des paramètres sont séparés par des virgules. Chaque ligne sous la ligne d’en-tête représente les valeurs des paramètres pour l’importation d’un fichier PST dans une boîte aux lettres spécifique. Vous aurez besoin d’une ligne pour chaque fichier PST que vous souhaitez importer dans une boîte aux lettres d’utilisateur. N’oubliez pas de remplacer les espaces réservés dans le fichier de mappage par les données réelles.
    
    > [!NOTE]
    > Ne modifiez en aucun cas la ligne d’en-tête, ni les paramètres SharePoint ; ils seront ignorés pendant le processus d’importation des fichiers PST. 
  
3. Utilisez les informations du tableau suivant pour remplir le fichier CSV avec les informations requises.
    
    |**Paramètre**|**Description**|**Exemple**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Spécifie le service Office 365 vers lequel les données seront importées. Pour importer des fichiers PST dans des boîtes aux lettres `Exchange`utilisateur, utilisez.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Spécifie l'emplacement du dossier dans l'emplacement de stockage Azure dans lequel vous avez téléchargé les fichiers PST à l'étape 5.  <br/>  Si vous n'avez pas inclus de nom de sous-dossier facultatif dans l' `/upload-dest:` URL réseau dans le paramètre de l'étape 5, laissez ce paramètre vide dans le fichier CSV. Si vous avez inclus un nom de sous-dossier, spécifiez-le dans ce paramètre. La valeur de ce paramètre est sensible à la casse. Dans les deux cas, n'incluez *pas* «ingestiondata» dans `FilePath` la valeur du paramètre.  <br/> <br/>**Important:** Le nom du chemin d'accès du fichier doit être identique à celui que vous avez utilisé si vous avez inclus un nom de sous-dossier facultatif dans `/upload-dest:` l'URL SAS dans le paramètre de l'étape 5. Par exemple, si vous avez `EncryptedPSTs` utilisé pour le nom du sous-dossier à l'étape `encryptedpsts` 5, `FilePath` puis que vous utilisez dans le paramètre du fichier CSV, l'importation du fichier PST échouera. Veillez à utiliser la même casse dans les deux instances.           |(Laisser vide)  <br/> Ou  <br/>  `EncryptedPSTs` <br/> |
    | `Name` <br/> |Indique le nom du fichier PST qui sera importé dans la boîte aux lettres d’utilisateur.  La valeur de ce paramètre est sensible à la casse. Étant donné que les fichiers PST téléchargés vers l'emplacement de stockage Azure sont chiffrés, une `.pfile` extension est ajoutée au nom de fichier PST. Vous devez ajouter l' `.pfile` extension au nom des fichiers PST dans le fichier CSV.  <br/><br/> **Important:** Le nom du fichier PST dans le fichier CSV doit être le même que celui du fichier PST qui a été téléchargé vers l'emplacement de stockage Azure à l'étape 5. Par exemple, si vous utilisez `annb.pst.pfile` le `Name` paramètre dans le fichier CSV, mais que le nom du fichier PST réel est `AnnB.pst`, l'importation de ce fichier PST échoue. Assurez-vous que le nom du fichier PST dans le fichier CSV utilise la même casse que le fichier PST réel.           | `annb.pst.pfile` <br/> |
    | `Mailbox` <br/> |Indique l’adresse de messagerie de la boîte aux lettres dans laquelle le fichier PST est importé.   <br/> Pour importer un fichier PST dans une boîte aux lettres inactive, vous devez spécifier le GUID de la boîte aux lettres de ce paramètre. Pour obtenir ce GUID, exécutez la commande PowerShell suivante dans Exchange Online:`Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL Guid` <br/><br/> **Remarque:** Dans certains cas, vous pouvez avoir plusieurs boîtes aux lettres avec la même adresse de messagerie, où une boîte aux lettres est une boîte aux lettres active et l'autre est dans un état supprimé (ou inactif). Dans ce cas, vous devez spécifier le GUID de boîte aux lettres pour identifier de manière unique la boîte aux lettres dans laquelle importer le fichier PST. Pour obtenir ce GUID pour les boîtes aux lettres actives, exécutez la commande PowerShell `Get-Mailbox - <identity of active mailbox> | FL Guid`suivante:. Pour obtenir le GUID des boîtes aux lettres supprimées (ou inactives), exécutez la commande suivante:`Get-Mailbox - <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`           | `annb@contoso.onmicrosoft.com` <br/> Ou  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Indique si le fichier PST doit être importé dans la boîte aux lettres d’archivage de l’utilisateur. Il existe deux options :  <br/> **Valeur false** Importe le fichier PST dans la boîte aux lettres principale de l'utilisateur.  <br/> **True** Importe le fichier PST dans la boîte aux lettres d'archivage de l'utilisateur.  <br/>  If you leave this parameter blank, the PST file is imported to the user's primary mailbox.  <br/><br/> **Remarque:** Pour importer un fichier PST dans une boîte aux lettres d'archivage informatique pour un utilisateur dont la boîte aux lettres principale est locale, spécifiez simplement **true** pour ce paramètre et spécifiez l'adresse de messagerie de la boîte aux `Mailbox` lettres locale de l'utilisateur pour le paramètre.           | `FALSE` <br/> Ou  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Spécifie le dossier de boîte aux lettres dans lequel le fichier PST est importé.  <br/>  Si vous laissez ce paramètre vide, le fichier PST sera importé dans un nouveau dossier nommé **** importés au niveau racine de la boîte aux lettres (le même niveau que le dossier boîte de réception et les autres dossiers de boîte aux lettres par défaut).  <br/>  Si vous spécifiez `/`, les éléments du fichier PST seront importés directement dans le dossier boîte de réception de l'utilisateur.  <br/>  Si vous spécifiez `/<foldername>`, les éléments du fichier PST seront importés dans un sous-dossier nommé * \<NomDossier\> * . Par exemple, si vous avez `/ImportedPst`utilisé, les éléments seraient importés dans un sous-dossier nommé **ImportedPst**. Ce sous-dossier sera situé dans le dossier boîte de réception de l'utilisateur.  <br/><br/> **Conseil:** EnVisagez d'exécuter quelques lots de test pour tester ce paramètre afin de déterminer le meilleur emplacement de dossier dans lequel importer les fichiers PST.           |(Laisser vide)  <br/> Ou  <br/>  `/` <br/> Ou  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Ce paramètre facultatif spécifie une valeur numérique pour la page de codes à utiliser pour l'importation des fichiers PST au format de fichier ANSI. Ce paramètre est utilisé pour l'importation de fichiers PST à partir d'organisations chinoises, japonaises et coréennes, car ces langues utilisent généralement un jeu de caractères DBCS (Double Byte Character Set) pour le codage des caractères. Si ce paramètre n'est pas utilisé pour importer des fichiers PST pour les langues qui utilisent des caractères DBCS pour les noms de dossier de boîte aux lettres, les noms de dossier sont souvent tronqués après leur importation. Pour obtenir la liste des valeurs prises en charge à utiliser pour ce paramètre, consultez la rubrique identificateurs de la [page de code](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/><br/> **Remarque:** Comme indiqué précédemment, il s'agit d'un paramètre facultatif et vous n'avez pas besoin de l'inclure dans le fichier CSV. Vous pouvez également l'inclure et laisser la valeur vide pour une ou plusieurs lignes.           |(Laisser vide)  <br/> Ou  <br/>  `932`(il s'agit de l'identificateur de page de code pour le japonais ANSI/OEM)  <br/> |
    | `SPFileContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPManifestContainer` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
    | `SPSiteUrl` <br/> |Pour l’importation PST, laissez ce paramètre vide.   <br/> |Non applicable  <br/> |
  
## <a name="step-8-create-a-pst-import-job-in-office-365"></a>Étape 8 : Créer une tâche d’importation PST dans Office 365

La dernière étape consiste à créer le travail d'importation PST dans le service d'importation dans Office 365. Comme indiqué précédemment, vous devez envoyer le fichier de mappage d’importation PST créé à l’étape 7. Une fois le nouveau travail créé, le service d'importation utilise les informations du fichier de mappage pour annuler le chiffrement et importer les fichiers PST (que vous avez téléchargé vers Office 365 à l'étape 5) vers la boîte aux lettres de l'utilisateur spécifié. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide des informations d'identification d'un compte d'administrateur de votre organisation Office 365.
    
3. Dans le volet de gauche, cliquez sur **gouvernance des données** , puis sur **Importer**.
    
4. Sur la page **Importation**, cliquez sur **Ouvrir le service d’importation**.
    
5. sur la page **importer des données dans Office 365** , cliquez sur nouvelle icône](media/ITPro-EAC-AddIcon.gif)ajouter **un travail**![, puis cliquez sur **télécharger des messages électroniques (fichiers PST)**.
    
6. Sur la page **Télécharger les fichiers sur le réseau**, sélectionnez **J’ai terminé de télécharger mes fichiers** et **J’ai accès au fichier de mappage**, puis cliquez sur **Suivant**.  
    
7. Entrez le nom de la tâche d’importation PST, puis cliquez sur **Suivant**.
    
8. Cliquez sur **Ajouter** ![une](media/ITPro-EAC-AddIcon.gif) icône pour sélectionner le fichier de mappage PST que vous avez créé à l'étape 7. 
    
9. Lorsque le nom du fichier CSV apparaît dans la liste, sélectionnez-le, puis cliquez sur **Valider** pour vérifier que votre fichier CSV ne contient pas d’erreurs.  
    
    > [!NOTE]
    > Comme indiqué précédemment, lorsque les fichiers PST sont chiffrés, une `.pfile` extension est ajoutée au nom de fichier PST. Vous devez ajouter l' `.pfile` extension au nom des fichiers PST dans le fichier CSV. Sinon, le fichier CSV ne sera pas validé. 
  
    Le fichier CSV doit être validé pour créer la tâche d’importation PST. Si la validation échoue, cliquez sur le lien **Non valide** dans la colonne **État**. Une copie de votre fichier de mappage d’importation PST s’ouvre avec un message d’erreur pour chaque ligne du fichier ayant échoué. 
    
10. Une fois le fichier de mappage PST validé, lisez les conditions d’utilisation, puis cliquez sur la case à cocher.
    
11. Cliquez sur **Terminer** pour envoyer la tâche. 
    
    Le travail est affiché dans la liste des travaux d'importation PST sur la page **importer des données dans Office 365** . 
    
12. Sélectionnez le travail, puis ****![cliquez sur Actualiser l'icône](media/O365-MDM-Policy-RefreshIcon.gif) actualiser pour mettre à jour les informations d'État affichées dans le volet d'informations. 
    
13. Dans le volet d’informations, cliquez sur **Afficher les détails** pour consulter l’état le plus récent de la tâche sélectionnée. 
 
## <a name="more-information"></a>Plus d’informations

- Pourquoi importer des fichiers PST vers Office 365?
    
  - Il s'agit d'un moyen efficace pour migrer le courrier électronique de votre organisation vers Office 365.
    
  - Cela vous aide à répondre aux besoins de conformité de votre organisation en vous permettant de réaliser les opérations suivantes :
    
  - Activer les boîtes aux lettres d’archivage pour donner aux utilisateurs un espace de stockage de boîte aux lettres supplémentaire.
    
  - Placer des boîtes aux lettres en conservation inaltérable pour ne pas perdre le contenu.
    
  - Utiliser les outils de découverte électronique Microsoft pour rechercher du contenu dans des boîtes aux lettres.
    
  - Adopter des stratégies de rétention pour contrôler la durée de conservation du contenu des boîtes aux lettres.
    
  - Recherchez dans le journal d'audit Office 365 des événements liés à la boîte aux lettres.
    
  - Cela vous aide à protéger votre organisation contre la perte de données. Les fichiers PST importés vers les boîtes aux lettres Office 365 héritent des fonctionnalités de haute disponibilité d'Exchange Online, par opposition au stockage des données sur l'ordinateur d'un utilisateur.
    
  - L’utilisateur peut accéder aux données à partir de n’importe quel périphérique, car elles sont stockées dans le cloud.
    
- Voici un exemple des clés, des ID et des URL obtenus aux étapes 2, 3 et 4. Cet exemple contient également la syntaxe de la commande exécutée dans l'outil O365ImportTool. exe pour chiffrer et télécharger des fichiers PST dans Office 365. Veillez à prendre toutes les précautions nécessaires pour protéger ces clés, tout comme vous le feriez avec vos mots de passe ou d’autres informations de sécurité.
    
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

- Comme expliqué précédemment, le service d'importation Office 365 active le paramètre de blocage de rétention (pour une durée indéterminée) une fois que les fichiers PST sont importés dans une boîte aux lettres. Cela signifie que la propriété *RentionHoldEnabled* est définie `True` sur de sorte que la stratégie de rétention attribuée à la boîte aux lettres ne soit pas traitée. Le propriétaire de la boîte aux lettres peut ainsi gérer les messages nouvellement importés en empêchant une suppression ou une stratégie d'archivage de supprimer ou d'archiver les anciens messages. Voici quelques étapes que vous pouvez suivre pour gérer ce blocage de rétention: 
    
  - Au bout d'un certain temps, vous pouvez désactiver le blocage de rétention en `Set-Mailbox -RetentionHoldEnabled $false` exécutant la commande. Pour obtenir des instructions, consultez [la rubrique placer une boîte aux lettres en blocage de](https://go.microsoft.com/fwlink/p/?LinkId=544749)rétention.
    
  - Vous pouvez configurer le blocage de rétention de sorte qu'il soit désactivé à une date ultérieure. Pour ce faire, exécutez la `Set-Mailbox -EndDateForRetentionHold <date>` commande. Par exemple, en supposant que la date du jour est le 1er juin 2016 et que vous voulez désactiver le blocage de rétention dans 30 jours, exécutez la `Set-Mailbox -EndDateForRetentionHold 7/1/2016`commande suivante:. Dans ce scénario, vous devez laisser la propriété *RentionHoldEnabled* définie sur `True`. Pour plus d'informations, consultez la rubrique [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
  - Vous pouvez modifier les paramètres de la stratégie de rétention attribuée à la boîte aux lettres de sorte que les éléments plus anciens qui ont été importés ne soient pas immédiatement supprimés ou déplacés vers la boîte aux lettres d'archivage de l'utilisateur. Par exemple, vous pouvez rallonger l'âge de rétention d'une stratégie de suppression ou d'archivage affectée à la boîte aux lettres. Dans ce scénario, vous devez désactiver le blocage de rétention sur la boîte aux lettres après avoir modifié les paramètres de la stratégie de rétention. Pour plus d'informations, consultez [la rubrique Configurer une stratégie d'archivage et de suppression pour les boîtes aux lettres dans votre organisation Office 365](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
