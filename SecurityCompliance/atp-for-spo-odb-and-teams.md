---
title: Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/18/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
description: Étendre Office 365 avancée protection contre les menaces de fichiers dans SharePoint Online, OneDrive entreprise et Microsoft Teams pour permettre une collaboration plus sûre pour votre organisation.
ms.openlocfilehash: ea1c77273be70ce27f60bfaeae3544d605553a32
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528525"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="509a4-103">Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft</span><span class="sxs-lookup"><span data-stu-id="509a4-103">Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="509a4-p101">Personnes régulièrement les fichiers de partager et collaborer à l’aide de SharePoint, OneDrive et Teams Microsoft. Avec [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), votre organisation peut collaborer de manière plus sûre. DAV permet de détecter et de bloquer les fichiers qui sont identifiés comme malveillants dans les sites d’équipe et des bibliothèques de documents. Lisez cet article pour obtenir une vue d’ensemble de DAV pour SharePoint Online, OneDrive pour les entreprises et Teams Microsoft, puis effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="509a4-p101">People regularly share files and collaborate using SharePoint, OneDrive, and Microsoft Teams. With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can collaborate in a safer manner. ATP helps detect and block files that are identified as malicious in team sites and document libraries. Read this article to get an overview of ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams, and then take your next steps.</span></span> 
  
> [!TIP]
> <span data-ttu-id="509a4-p102">Pour effectuer les tâches décrites dans cet article, vous devez être un administrateur global d’Office 365 ou un administrateur de sécurité. Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="509a4-p102">In order to perform the tasks described in this article, you must be an Office 365 global administrator or a security administrator. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-it-works"></a><span data-ttu-id="509a4-110">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="509a4-110">How it works</span></span>

<span data-ttu-id="509a4-p103">Lorsqu’un fichier dans SharePoint Online, OneDrive entreprise et Microsoft Teams a été identifié comme malveillants, DAV intègre directement les magasins de fichiers pour verrouiller ce fichier. L’image suivante montre un exemple d’un fichier malveillant détecté dans une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="509a4-p103">When a file in SharePoint Online, OneDrive for Business, and Microsoft Teams has been identified as malicious, ATP directly integrates with the file stores to lock that file. The following image shows an example of a malicious file detected in a library.</span></span>
  
<span data-ttu-id="509a4-113">[![Capture d’écran de fichiers dans OneDrive entreprise avec identifié comme malveillants](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="509a4-113">[![Screenshot of files in OneDrive for Business with one detected as malicious](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="509a4-p104">Bien que les fichiers bloqués apparaît toujours dans la bibliothèque de documents et le web, les applications de bureau ou mobiles, les fichiers bloqués ne peut pas être ouvert, copié, déplacé ou partagé. Personnes peuvent, toutefois, supprimer un fichier bloqué. Voici un exemple de rôle qui ressemble à sur appareil mobile d’un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="509a4-p104">Although the blocked file is still listed in the document library and web, mobile, or desktop applications, the blocked file cannot be opened, copied, moved, or shared. People can, however, delete a blocked file. Here's an example of what that looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="509a4-117">[![Capture d’écran de la suppression d’un fichier bloqué depuis OneDrive entreprise de l’application mobile OneDrive](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="509a4-117">[![Screenshot of deleting a blocked file from OneDrive for Business from the OneDrive mobile app](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="509a4-p105">Selon la configuration de Office 365, les personnes peuvent ou ne peut pas avoir la possibilité de télécharger un fichier bloqué. Voici ce que le téléchargement d’un fichier bloqué sur l’appareil mobile d’un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="509a4-p105">Depending on how Office 365 is configured, people might or might not have the ability to download a blocked file. Here's what downloading a blocked file looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="509a4-120">[![Capture d’écran de téléchargement d’un fichier bloqué dans OneDrive entreprise](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="509a4-120">[![Screenshot of downloading a blocked file in OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="509a4-121">Pour plus d’informations, voir [activer Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](turn-on-atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="509a4-121">To learn more, see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>
  
### <a name="keep-the-following-points-in-mind"></a><span data-ttu-id="509a4-122">Gardez les points suivants à l’esprit</span><span class="sxs-lookup"><span data-stu-id="509a4-122">Keep the following points in mind</span></span>

- <span data-ttu-id="509a4-p106">DAV n’analyse pas chaque fichier dans SharePoint Online, OneDrive pour les professionnels ou Teams Microsoft. Il s’agit de par sa conception. Les fichiers sont analysés en mode asynchrone, via un processus qui utilise des événements d’activité partage et invité ainsi que heuristique actives et les signaux des menaces pour identifier les fichiers malveillants.</span><span class="sxs-lookup"><span data-stu-id="509a4-p106">ATP will not scan every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams. This is by design. Files are scanned asynchronously, through a process that uses sharing and guest activity events along with smart heuristics and threat signals to identify malicious files.</span></span>
    
- <span data-ttu-id="509a4-126">Les fichiers qui sont identifiés comme malveillants dans SharePoint Online, OneDrive, ou de l’entreprise Microsoft Teams s’afficheront dans les [rapports pour Office 365 avancée protection contre les menaces](view-reports-for-atp.md) et dans l’Explorateur de menace (partie des [Informations sur les menaces Office 365](office-365-ti.md)).</span><span class="sxs-lookup"><span data-stu-id="509a4-126">Files that are identified as malicious in SharePoint Online, OneDrive for Business, or Microsoft Teams will show up in [reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md) and in Threat Explorer (part of [Office 365 Threat Intelligence](office-365-ti.md)).</span></span>
    
- <span data-ttu-id="509a4-p107">DAV fait partie de threat protection stratégie globale votre organisation, qui inclut anti-spam et protection anti-programme malveillant, ainsi que des liens fiables et pièces jointes fiables. Pour plus d’informations, consultez la rubrique [protection contre les menaces dans Office 365](protect-against-threats.md).</span><span class="sxs-lookup"><span data-stu-id="509a4-p107">ATP is part of your organization's overall threat protection strategy, which includes anti-spam and anti-malware protection, as well as Safe Links and Safe Attachments. To learn more, see [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="509a4-p108">Un administrateur SharePoint Online permettre déterminer s’il faut permettre aux utilisateurs de télécharger des fichiers qui sont détectés comme malveillants. Cette opération est effectuée en exécutant la cmdlet Set-SPOTenant PowerShell à l’aide d’un paramètre DisallowInfectedFileDownload (voir [activer Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](turn-on-atp-for-spo-odb-and-teams.md)).</span><span class="sxs-lookup"><span data-stu-id="509a4-p108">A SharePoint Online administrator can determine whether to enable people to download files that are detected as malicious. This is done by running the Set-SPOTenant PowerShell cmdlet using a DisallowInfectedFileDownload parameter (see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)).</span></span>
    
## <a name="new-quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="509a4-131">(Nouveau) ! Mise en quarantaine dans DAV pour SharePoint Online, OneDrive entreprise et les équipes Microsoft</span><span class="sxs-lookup"><span data-stu-id="509a4-131">(New!) Quarantine in ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams</span></span>

 <span data-ttu-id="509a4-132">** À partir de fin mai 2018, les fonctionnalités de [mise en quarantaine](quarantine-email-messages.md) dans la sécurité &amp; centre de conformité sont accordées à DAV pour SharePoint Online, OneDrive entreprise et Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="509a4-132">**Beginning in late May 2018, [quarantine](quarantine-email-messages.md) capabilities in the Security &amp; Compliance Center are being extended to ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span> **
  
<span data-ttu-id="509a4-p109">Lorsqu’un fichier dans SharePoint Online, OneDrive, ou de l’entreprise Microsoft Teams est identifiée comme malveillants, outre DAV bloquer le fichier ouvert ou partagé, ce fichier est inclus dans une liste d’éléments mis en quarantaine. (Dans la sécurité &amp; centre de conformité, accédez à la **Gestion des menaces** \> **révision** \> **mise en quarantaine** et filtrage de contenu.)</span><span class="sxs-lookup"><span data-stu-id="509a4-p109">When a file in SharePoint Online, OneDrive for Business, or Microsoft Teams is identified as malicious, in addition to ATP blocking the file from being opened or shared, that file is included in a list of quarantined items. (In the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Quarantine** and filter for Content.)</span></span> 
  
<span data-ttu-id="509a4-135">Si vous faites partie de l’équipe de sécurité de votre organisation Office 365 et nécessaires [autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md), vous pouvez télécharger, version, rapport et supprimer des fichiers qui sont détectés comme malveillants par DAV à partir de la mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="509a4-135">If you're part of your organization's Office 365 security team and have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), you can download, release, report, and delete files that are detected as malicious by ATP from quarantine.</span></span>
  
- <span data-ttu-id="509a4-p110">**Création de rapports et de la libération** d’un fichier supprime le bloc de DAV sur le fichier dans la bibliothèque de documents ou site d’équipe respectifs pour SharePoint, OneDrive ou Teams Microsoft. Les utilisateurs peuvent ensuite ouvrir, partager et téléchargez le fichier. Et, lorsque l’option **Envoyer le rapport à Microsoft** est sélectionnée, le fichier est signalé comme un faux positif à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="509a4-p110">**Releasing and reporting** a file removes the ATP block on the file in the respective team site or document library for SharePoint, OneDrive, or Microsoft Teams. Users are then able to open, share, and download the file. And, when the **Send report to Microsoft** option is selected, the file is reported as a false positive to Microsoft.</span></span> 
    
- <span data-ttu-id="509a4-p111">**Suppression d’un fichier** supprime le fichier de mise en quarantaine ; Toutefois, le fichier est toujours bloqué d’être ouvert ou partagé. Le fichier doit être supprimé dans son site respectifs document bibliothèque ou de l’équipe (SharePoint Online, OneDrive, ou de l’entreprise Microsoft Teams).</span><span class="sxs-lookup"><span data-stu-id="509a4-p111">**Deleting a file** removes the file from quarantine; however, the file is still blocked from being opened or shared. The file must also be deleted in its respective document library or team site (SharePoint Online, OneDrive for Business, or Microsoft Teams).</span></span> 
    
- <span data-ttu-id="509a4-141">**Téléchargement d’un fichier** vous permet de télécharger et d’analyser le fichier pour n’importe quel nombre de faux positifs.</span><span class="sxs-lookup"><span data-stu-id="509a4-141">**Downloading a file** enables you to download and analyze the file for any false positives.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="509a4-142">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="509a4-142">Next steps</span></span>

- [<span data-ttu-id="509a4-143">Activer Office 365 DAV pour SharePoint, OneDrive et les équipes de Microsoft</span><span class="sxs-lookup"><span data-stu-id="509a4-143">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)
    
- [<span data-ttu-id="509a4-144">Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="509a4-144">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
## <a name="related-topics"></a><span data-ttu-id="509a4-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="509a4-145">Related topics</span></span>

[<span data-ttu-id="509a4-146">Protection de Microsoft Office 365 menace avancées</span><span class="sxs-lookup"><span data-stu-id="509a4-146">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="509a4-147">Afficher les rapports pour Office 365 avancée protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="509a4-147">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="509a4-148">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="509a4-148">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

