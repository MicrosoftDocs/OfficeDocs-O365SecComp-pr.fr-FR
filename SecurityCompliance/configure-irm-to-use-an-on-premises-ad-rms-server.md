---
title: Configuration de la Gestion des droits relatifs à l’information (IRM) pour utiliser un serveur AD RMS local
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/13/2017
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 3ecde857-4b7c-451d-b4aa-9eeffc8a8c61
ms.collection:
- M365-security-compliance
description: Cette rubrique décrit la configuration de la gestion des droits relatifs à l'information de manière à utiliser un serveur AD RMS.
ms.openlocfilehash: 1da66c5afa37c96c061a4bf25c0858e4e71e2313
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693033"
---
# <a name="configure-irm-to-use-an-on-premises-ad-rms-server"></a><span data-ttu-id="43ab7-103">Configuration de la Gestion des droits relatifs à l’information (IRM) pour utiliser un serveur AD RMS local</span><span class="sxs-lookup"><span data-stu-id="43ab7-103">Configure IRM to use an on-premises AD RMS server</span></span>
  
<span data-ttu-id="43ab7-104">Pour une utilisation avec des déploiements locaux, la gestion des droits relatifs à l'information (IRM) dans Exchange Online utilise les services AD RMS (Active Directory Rights Management Services), une technologie de protection des informations dans Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="43ab7-104">For use with on-premises deployments, Information Rights Management (IRM) in Exchange Online uses Active Directory Rights Management Services (AD RMS), an information protection technology in Windows Server 2008 and later.</span></span> <span data-ttu-id="43ab7-105">La protection IRM permet d'appliquer un modèle de stratégie de droits AD RMS à un message électronique.</span><span class="sxs-lookup"><span data-stu-id="43ab7-105">IRM protection is applied to email by applying an AD RMS rights policy template to an email message.</span></span> <span data-ttu-id="43ab7-106">Les droits sont joints au message lui-même pour que la protection s'effectue en ligne et hors connexion, et à l'intérieur et à l'extérieur du pare-feu de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="43ab7-106">Rights are attached to the message itself so that protection occurs online and offline and inside and outside of your organization's firewall.</span></span>
  
<span data-ttu-id="43ab7-107">Cette rubrique décrit la configuration de la gestion des droits relatifs à l'information de manière à utiliser un serveur AD RMS.</span><span class="sxs-lookup"><span data-stu-id="43ab7-107">This topic shows you how to configure IRM to use an AD RMS server.</span></span> <span data-ttu-id="43ab7-108">Pour plus d'informations sur l'utilisation des nouvelles fonctionnalités pour le chiffrement de messages Office 365 avec Azure Active Directory et Azure Rights Management, consultez le [Forum aux questions sur le chiffrement de messages office 365](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e).</span><span class="sxs-lookup"><span data-stu-id="43ab7-108">For information about using the new capabilities for Office 365 Message Encryption with Azure Active Directory and Azure Rights Management, see the [Office 365 Message Encryption FAQ](https://support.office.com/article/0432dce9-d9b6-4e73-8a13-4a932eb0081e).</span></span>
  
<span data-ttu-id="43ab7-109">Pour en savoir plus sur la Gestion des droits relatifs à l'information dans Exchange Online, consultez la rubrique [Gestion des droits relatifs à l'information (IRM) dans Exchange Online](information-rights-management-in-exchange-online.md).</span><span class="sxs-lookup"><span data-stu-id="43ab7-109">To learn more about IRM in Exchange Online, see [Information Rights Management in Exchange Online](information-rights-management-in-exchange-online.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="43ab7-110">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="43ab7-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="43ab7-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="43ab7-111"></span></span>

- <span data-ttu-id="43ab7-112">Durée d'exécution estimée de cette tâche : 30 minutes</span><span class="sxs-lookup"><span data-stu-id="43ab7-112">Estimated time to complete this task: 30 minutes</span></span>
    
- <span data-ttu-id="43ab7-p103">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure. Pour voir les autorisations qui vous sont nécessaires, consultez l'entrée « Gestion des droits relatifs à l'information » dans la rubrique [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx).</span><span class="sxs-lookup"><span data-stu-id="43ab7-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Information Rights Management" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="43ab7-p104">Le serveur AD RMS doit exécuter Windows Server 2008 ou une version ultérieure. Pour plus d'informations sur le déploiement d'AD RMS, consultez [Installation d'un cluster AD RMS](https://go.microsoft.com/fwlink/?LinkId=210873).</span><span class="sxs-lookup"><span data-stu-id="43ab7-p104">The AD RMS server must be running Windows Server 2008 or later. For details about how to deploy AD RMS, see [Installing an AD RMS Cluster](https://go.microsoft.com/fwlink/?LinkId=210873).</span></span>
    
- <span data-ttu-id="43ab7-117">Pour plus d'informations sur l'installation et la configuration de Windows PowerShell et la connexion au service, consultez la rubrique [Connexion à Exchange Online à l'aide de Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span><span class="sxs-lookup"><span data-stu-id="43ab7-117">For details about how to install and configure Windows PowerShell and connect to the service, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="43ab7-118">Pour des informations sur les raccourcis clavier applicables aux procédures de cette rubrique, voir Raccourcis clavier dans Exchange 2013 **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="43ab7-118">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="43ab7-p105">Vous rencontrez des difficultés ? Demandez de l'aide en participant aux forums Exchange. Visitez les forums sur les pages [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), et [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="43ab7-p105">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="how-do-you-do-this"></a><span data-ttu-id="43ab7-122">Comment procéder ?</span><span class="sxs-lookup"><span data-stu-id="43ab7-122">How do you do this?</span></span>
<span data-ttu-id="43ab7-123"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="43ab7-123"></span></span>

### <a name="step-1-use-the-ad-rms-console-to-export-a-trusted-publishing-domain-tpd-from-an-ad-rms-server"></a><span data-ttu-id="43ab7-124">Étape 1 : utiliser la console AD RMS pour exporter un domaine de publication approuvé (TPD) à partir d'un serveur AD RMS</span><span class="sxs-lookup"><span data-stu-id="43ab7-124">Step 1: Use the AD RMS console to export a trusted publishing domain (TPD) from an AD RMS server</span></span>

<span data-ttu-id="43ab7-p106">La première étape consiste à exporter un domaine de publication approuvé vers un fichier XML local à partir du serveur AD RMS local. Le domaine de publication approuvé contient les paramètres suivants requis pour utiliser les fonctionnalités RMS :</span><span class="sxs-lookup"><span data-stu-id="43ab7-p106">The first step is to export a trusted publishing domain (TPD) from the on-premises AD RMS server to an XML file. The TPD contains the following settings needed to use RMS features:</span></span> 
  
- <span data-ttu-id="43ab7-127">le certificat de licence serveur (SLC) utilisé pour signer et chiffrer les certificats et licences ;</span><span class="sxs-lookup"><span data-stu-id="43ab7-127">The server licensor certificate (SLC) used for signing and encrypting certificates and licenses</span></span>
    
- <span data-ttu-id="43ab7-128">les URL utilisées pour les licences et les publications ;</span><span class="sxs-lookup"><span data-stu-id="43ab7-128">The URLs used for licensing and publishing</span></span>
    
- <span data-ttu-id="43ab7-129">les modèles de stratégie de droits AD RMS créés avec le SLC spécifique au domaine de publication approuvé.</span><span class="sxs-lookup"><span data-stu-id="43ab7-129">The AD RMS rights policy templates that were created with the specific SLC for that TPD</span></span>
    
<span data-ttu-id="43ab7-130">Quand vous importez le domaine de publication approuvé, il est stocké et protégé dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="43ab7-130">When you import the TPD, it's stored and protected in Exchange Online.</span></span>
  
1. <span data-ttu-id="43ab7-131">Ouvrez la console Active Directory Rights Management Services et développez le cluster AD RMS.</span><span class="sxs-lookup"><span data-stu-id="43ab7-131">Open the Active Directory Rights Management Services console, and then expand the AD RMS cluster.</span></span>
    
2. <span data-ttu-id="43ab7-132">Dans l'arborescence de la console, développez **Stratégies d'approbation**, puis cliquez sur **Domaines de publication approuvés**.</span><span class="sxs-lookup"><span data-stu-id="43ab7-132">In the console tree, expand **Trust Policies**, and then click **Trusted Publishing Domains**.</span></span>
    
3. <span data-ttu-id="43ab7-133">Dans le volet des résultats, sélectionnez le certificat du domaine à exporter.</span><span class="sxs-lookup"><span data-stu-id="43ab7-133">In the results pane, select the certificate for the domain you want to export.</span></span>
    
4. <span data-ttu-id="43ab7-134">Dans le volet **Actions**, cliquez sur **Exporter le domaine de publication approuvé**.</span><span class="sxs-lookup"><span data-stu-id="43ab7-134">In the **Actions** pane, click **Export Trusted Publishing Domain**.</span></span>
    
5. <span data-ttu-id="43ab7-p107">Dans la zone **Fichier de domaine de publication**, cliquez sur **Enregistrer sous** pour enregistrer le fichier dans un emplacement spécifique sur l'ordinateur local. Entrez un nom de fichier et assurez-vous de spécifier l'extension de fichier  `.xml`, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="43ab7-p107">In the **Publishing domain file** box, click **Save As** to save the file to a specific location on the local computer. Type a file name, making sure to specify the  `.xml` file name extension, and then click **Save**.</span></span>
    
6. <span data-ttu-id="43ab7-p108">Dans les zones **Mot de passe** et **Confirmer le mot de passe**, entrez un mot de passe fort qui sera utilisé pour chiffrer le fichier de domaine de publication approuvé. Vous devrez spécifier ce mot de passe lors de l'importation du domaine de publication approuvé vers votre système de messagerie en nuage.</span><span class="sxs-lookup"><span data-stu-id="43ab7-p108">In the **Password** and **Confirm Password** boxes, type a strong password that will be used to encrypt the trusted publishing domain file. You will have to specify this password when you import the TPD to your cloud-based email organization.</span></span> 
    
### <a name="step-2-use-the-exchange-management-shell-to-import-the-tpd-to-exchange-online"></a><span data-ttu-id="43ab7-139">Étape 2 : utiliser l'Environnement de ligne de commande Exchange Management Shell pour importer le domaine de publication approuvé dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="43ab7-139">Step 2: Use the Exchange Management Shell to import the TPD to Exchange Online</span></span>

<span data-ttu-id="43ab7-p109">Après avoir exporté le domaine de publication approuvé vers un fichier XML, vous devez l'importer dans Exchange Online. Quand un domaine de publication approuvé est importé, les modèles AD RMS de votre organisation sont également importés. Quand le premier domaine de publication approuvé est importé, il devient le domaine de publication approuvé par défaut de votre organisation en nuage. Si vous importez un autre domaine de publication approuvé, vous pouvez utiliser le commutateur **Par défaut** pour le définir en tant que domaine de publication approuvé par défaut disponible aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="43ab7-p109">After the TPD is exported to an XML file, you have to import it to Exchange Online. When a TPD is imported, your organization's AD RMS templates are also imported. When the first TPD is imported, it becomes the default TPD for your cloud-based organization. If you import another TPD, you can use the **Default** switch to make it the default TPD that is available to users.</span></span> 
  
<span data-ttu-id="43ab7-144">Pour importer le domaine de publication approuvé, exécutez la commande suivante dans Windows PowerShell :</span><span class="sxs-lookup"><span data-stu-id="43ab7-144">To import the TPD, run the following command in Windows PowerShell:</span></span>
  
```
Import-RMSTrustedPublishingDomain -FileData $([byte[]](Get-Content -Encoding byte -Path <path to exported TPD file> -ReadCount 0)) -Name "<name of TPD>" -ExtranetLicensingUrl <URL> -IntranetLicensingUrl <URL>
```

<span data-ttu-id="43ab7-p110">Vous pouvez obtenir les valeurs des paramètres  _ExtranetLicensingUrl_ et  _IntranetLicensingUrl_ dans la console Active Directory Rights Management Services. Sélectionnez le cluster AD RMS dans l'arborescence de la console. Les URL des licences s'affichent dans le volet des résultats. Ces URL sont utilisées par les clients de messagerie quand le contenu doit être déchiffré et quand Exchange Online doit déterminer quel domaine de publication approuvé il convient d'utiliser.</span><span class="sxs-lookup"><span data-stu-id="43ab7-p110">You can obtain the values for the  _ExtranetLicensingUrl_ and  _IntranetLicensingUrl_ parameters in the Active Directory Rights Management Services console. Select the AD RMS cluster in the console tree. The licensing URLs are displayed in the results pane. These URLs are used by email clients when content has to be decrypted and when Exchange Online needs to determine which TPD to use.</span></span> 
  
<span data-ttu-id="43ab7-p111">Quand vous utilisez cette commande, vous êtes invité à saisir un mot de passe. Entrez le mot de passe que vous avez spécifié lors de l'exportation du domaine de publication approuvé à partir de votre serveur AD RMS.</span><span class="sxs-lookup"><span data-stu-id="43ab7-p111">When you run this command, you'll be prompted for a password. Enter the password that you specified when you exported the TPD from your AD RMS server.</span></span>
  
<span data-ttu-id="43ab7-p112">Par exemple; la commande suivante importe le domaine de publication approuvé appelé « Exported TPD », à l'aide du fichier XML exporté à partir de votre serveur AD RMS et enregistré sur l'ordinateur de votre compte d'administrateur. Le paramètre Nom est utilisé pour spécifier un nom pour le domaine de publication approuvé.</span><span class="sxs-lookup"><span data-stu-id="43ab7-p112">For example, the following command imports the TPD named Exported TPD using the XML file that you exported from your AD RMS server and saved to the desktop of the Administrator account. The Name parameter is used to specify a name to the TPD.</span></span>
  
```
Import-RMSTrustedPublishingDomain -FileData $([byte[]](Get-Content -Encoding byte -Path C:\Users\Administrator\Desktop\ExportTPD.xml -ReadCount 0)) -Name "Exported TPD" -ExtranetLicensingUrl https://corp.contoso.com/_wmcs/licensing -IntranetLicensingUrl https://rmsserver/_wmcs/licensing
```

<span data-ttu-id="43ab7-153">Pour plus d'informations sur la syntaxe et les paramètres, consultez la rubrique [Import-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/7c5e7a0f-9c9d-4863-bab8-bcc729cc16a6.aspx).</span><span class="sxs-lookup"><span data-stu-id="43ab7-153">For detailed syntax and parameter information, see [Import-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/7c5e7a0f-9c9d-4863-bab8-bcc729cc16a6.aspx).</span></span>
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="43ab7-154">Comment savoir si cette étape a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="43ab7-154">How do you know this step worked?</span></span>

<span data-ttu-id="43ab7-p113">Pour vérifier que le domaine de publication a bien été importé, exécutez la cmdlet **Get-RMSTrustedPublishingDomain** pour récupérer les domaines de publication approuvés dans votre organisation Exchange Online. Pour plus de détails, consultez les exemples de la rubrique [Get-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/69499195-f08f-41bd-b0ed-443688410b12.aspx).</span><span class="sxs-lookup"><span data-stu-id="43ab7-p113">To verify that you have successfully imported the TPD, run the **Get-RMSTrustedPublishingDomain** cmdlet to retrieve TPDs in your Exchange Online organization. For details, see the examples in [Get-RMSTrustedPublishingDomain](http://technet.microsoft.com/library/69499195-f08f-41bd-b0ed-443688410b12.aspx).</span></span>
  
### <a name="step-3-use-the-exchange-management-shell-to-distribute-an-ad-rms-rights-policy-template"></a><span data-ttu-id="43ab7-157">Étape 3 : utiliser l'Environnement de ligne de commande Exchange Management Shell pour distribuer un modèle de stratégie de droits AD RMS</span><span class="sxs-lookup"><span data-stu-id="43ab7-157">Step 3: Use the Exchange Management Shell to distribute an AD RMS rights policy template</span></span>

<span data-ttu-id="43ab7-158">Après avoir importé le domaine de publication approuvé, vous devez vous assurer qu'un modèle de stratégie de droits AD RMS est distribué.</span><span class="sxs-lookup"><span data-stu-id="43ab7-158">After you import the TPD, you must make sure an AD RMS rights policy template is distributed.</span></span> <span data-ttu-id="43ab7-159">Un modèle distribué est visible par les utilisateurs d'Outlook sur le Web (anciennement appelé Outlook Web App), qui peuvent ensuite appliquer les modèles à un message électronique.</span><span class="sxs-lookup"><span data-stu-id="43ab7-159">A distributed template is visible to Outlook on the web (formerly known as Outlook Web App) users, who can then apply the templates to an email message.</span></span>
  
<span data-ttu-id="43ab7-160">Pour renvoyer une liste de tous les modèles du domaine de publication approuvé par défaut, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="43ab7-160">To return a list of all templates contained in the default TPD, run the following command:</span></span>
  
```
Get-RMSTemplate -Type All | fl
```

<span data-ttu-id="43ab7-161">Si la valeur du paramètre  _Type_ est  `Archived`, le modèle n'est pas visible aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="43ab7-161">If the value of the  _Type_ parameter is  `Archived`, the template isn't visible to users.</span></span> <span data-ttu-id="43ab7-162">Seuls les modèles distribués dans le publication approuvé par défaut sont disponibles dans Outlook sur le Web.</span><span class="sxs-lookup"><span data-stu-id="43ab7-162">Only distributed templates in the default TPD are available in Outlook on the web.</span></span>
  
<span data-ttu-id="43ab7-163">Pour distribuer un modèle, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="43ab7-163">To distribute a template, run the following command:</span></span>
  
```
Set-RMSTemplate -Identity "<name of the template>" -Type Distributed
```

<span data-ttu-id="43ab7-164">Par exemple, la commande suivante importe le modèle « Propriétaire ».</span><span class="sxs-lookup"><span data-stu-id="43ab7-164">For example, the following command imports the Company Confidential template.</span></span>
  
```
Set-RMSTemplate -Identity "Company Confidential" -Type Distributed
```

<span data-ttu-id="43ab7-165">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, consultez les rubriques [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx) et [Set-RMSTemplate](http://technet.microsoft.com/library/4637f6b8-751a-4f5e-8869-428250230382.aspx).</span><span class="sxs-lookup"><span data-stu-id="43ab7-165">For detailed syntax and parameter information, see [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx) and [Set-RMSTemplate](http://technet.microsoft.com/library/4637f6b8-751a-4f5e-8869-428250230382.aspx).</span></span>
  
 <span data-ttu-id="43ab7-166">**Modèle Ne pas transférer**</span><span class="sxs-lookup"><span data-stu-id="43ab7-166">**The Do Not Forward template**</span></span>
  
<span data-ttu-id="43ab7-p116">Quand vous importez le domaine de publication approuvé par défaut de votre organisation locale dans Exchange Online, un modèle de stratégie de droits AD RMS nommé **Ne pas transférer** est importé. C'est le modèle distribué par défaut quand vous importez le domaine de publication approuvé par défaut. Vous ne pouvez pas utiliser la cmdlet **Set-RMSTemplate** pour modifier le modèle **Ne pas transférer**.</span><span class="sxs-lookup"><span data-stu-id="43ab7-p116">When you import the default TPD from your on-premises organization into Exchange Online, one AD RMS rights policy template named **Do Not Forward** is imported. By default, this template is distributed when you import the default TPD. You can't use the **Set-RMSTemplate** cmdlet to modify the **Do Not Forward** template.</span></span> 
  
<span data-ttu-id="43ab7-p117">When the **Do Not Forward** template is applied to a message, only the recipients addressed in the message can read the message. Additionally, recipients can't do the following:</span><span class="sxs-lookup"><span data-stu-id="43ab7-p117">When the **Do Not Forward** template is applied to a message, only the recipients addressed in the message can read the message. Additionally, recipients can't do the following:</span></span> 
  
- <span data-ttu-id="43ab7-172">transférer le message à une autre personne ;</span><span class="sxs-lookup"><span data-stu-id="43ab7-172">Forward the message to another person.</span></span>
    
- <span data-ttu-id="43ab7-173">copier le contenu du message ;</span><span class="sxs-lookup"><span data-stu-id="43ab7-173">Copy content from the message.</span></span>
    
- <span data-ttu-id="43ab7-174">imprimer le message.</span><span class="sxs-lookup"><span data-stu-id="43ab7-174">Print the message.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="43ab7-175">Le modèle **Ne pas transférer** ne peut pas empêcher qu'un message soit copié avec un programme de capture d'écran tiers, pris en photo, ou simplement copié à la main par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="43ab7-175">The **Do Not Forward** template can't prevent information in a message from being copied with third-party screen capture programs, cameras, or users manually transcribing the information</span></span> 
  
<span data-ttu-id="43ab7-p118">Vous pouvez créer des modèles de stratégie de droits AD RMS supplémentaires sur le serveur AD RMS de votre organisation locale pour répondre aux exigences de protection IRM. Si vous créez des modèles de stratégie de droits AD RMS supplémentaires, vous devez de nouveau exporter le domaine de publication approuvé à partir du serveur AD RMS local et l'actualiser dans l'organisation de messagerie en nuage.</span><span class="sxs-lookup"><span data-stu-id="43ab7-p118">You can create additional AD RMS rights policy templates on the AD RMS server in your on-premises organization to meet your IRM protection requirements. If you create additional AD RMS rights policy templates, you have to export the TPD from the on-premises AD RMS server again and refresh the TPD in the cloud-based email organization.</span></span> 
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="43ab7-178">Comment savoir si cette étape a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="43ab7-178">How do you know this step worked?</span></span>

<span data-ttu-id="43ab7-p119">Pour vérifier qu'un modèle de stratégie de droits AD RMS a été distribué correctement, exécutez la cmdlet **Get-RMSTemplate** pour vérifier les propriétés du modèle. Pour plus de détails, consultez les exemples de la rubrique [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx).</span><span class="sxs-lookup"><span data-stu-id="43ab7-p119">To verify that you have successfully distributed and AD RMS rights policy template, run the **Get-RMSTemplate** cmdlet to check the template's properties. For details, see the examples in [Get-RMSTemplate](http://technet.microsoft.com/library/4a5066e8-b770-4aa2-b464-0d2190914f71.aspx).</span></span>
  
### <a name="step-4-use-the-exchange-management-shell-to-enable-irm"></a><span data-ttu-id="43ab7-181">Étape 4: utiliser l'Environnement de ligne de commande Exchange Management Shell pour activer la Gestion des droits relatifs à l'information</span><span class="sxs-lookup"><span data-stu-id="43ab7-181">Step 4: Use the Exchange Management Shell to enable IRM</span></span>

<span data-ttu-id="43ab7-182">Après avoir importé le domaine de publication approuvé et distribué un modèle de stratégie de droits AD RMS, exécutez la commande suivante pour activer la Gestion des droits relatifs à l'information dans votre organisation de messagerie en nuage.</span><span class="sxs-lookup"><span data-stu-id="43ab7-182">After you import the TPD and distribute an AD RMS rights policy template, run the following command to enable IRM for your cloud-based email organization.</span></span>
  
```
Set-IRMConfiguration -InternalLicensingEnabled $true
```

<span data-ttu-id="43ab7-183">Pour plus d'informations sur la syntaxe et les paramètres, consultez la rubrique [Set-IRMConfiguration](http://technet.microsoft.com/library/5df0b56a-7bcc-4be2-b4b8-4de16720476c.aspx).</span><span class="sxs-lookup"><span data-stu-id="43ab7-183">For detailed syntax and parameter information, see [Set-IRMConfiguration](http://technet.microsoft.com/library/5df0b56a-7bcc-4be2-b4b8-4de16720476c.aspx).</span></span>
  
#### <a name="how-do-you-know-this-step-worked"></a><span data-ttu-id="43ab7-184">Comment savoir si cette étape a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="43ab7-184">How do you know this step worked?</span></span>

<span data-ttu-id="43ab7-185">Pour vérifier que l'IRM a bien été activée, exécutez la cmdlet [Get-IRMConfiguration](http://technet.microsoft.com/library/e1821219-fe18-4642-a9c2-58eb0aadd61a.aspx) pour vérifier la configuration IRM dans l'organisation Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="43ab7-185">To verify that you have successfully enabled IRM, run the [Get-IRMConfiguration](http://technet.microsoft.com/library/e1821219-fe18-4642-a9c2-58eb0aadd61a.aspx) cmdlet to check IRM configuration in the Exchange Online organization.</span></span> 
  
## <a name="how-do-you-know-this-task-worked"></a><span data-ttu-id="43ab7-186">Comment savoir si cette tâche a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="43ab7-186">How do you know this task worked?</span></span>
<span data-ttu-id="43ab7-187"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="43ab7-187"></span></span>

<span data-ttu-id="43ab7-188">Pour vérifier que vous avez correctement importé le domaine de publication approuvé et activé la fonctionnalité IRM, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="43ab7-188">To verify that you have successfully imported the TPD and enabled IRM, do the following:</span></span>
  
- <span data-ttu-id="43ab7-p120">Exécutez la cmdlet **Test-IRMConfiguration** pour tester la fonctionnalité IRM. Pour plus d'informations, consultez « Exemple 1 » dans la rubrique [Test-IRMConfiguration](http://technet.microsoft.com/library/a730e7ff-a67f-4360-b5ff-70d171bb5e1d.aspx).</span><span class="sxs-lookup"><span data-stu-id="43ab7-p120">Use the **Test-IRMConfiguration** cmdlet to test IRM functionality. For details, see "Example 1" in [Test-IRMConfiguration](http://technet.microsoft.com/library/a730e7ff-a67f-4360-b5ff-70d171bb5e1d.aspx).</span></span>
    
- <span data-ttu-id="43ab7-191">Rédigez un nouveau message dans Outlook sur le Web et protégez l'IRM en sélectionnant l'option **définir les autorisations** dans le ![menu étendu (](media/ITPro-EAC-MoreOptionsIcon.gif)icône Options supplémentaires).</span><span class="sxs-lookup"><span data-stu-id="43ab7-191">Compose a new message in Outlook on the web and IRM-protect it by selecting **Set permissions** option from the extended menu ( ![More Options Icon](media/ITPro-EAC-MoreOptionsIcon.gif)).</span></span>
    

