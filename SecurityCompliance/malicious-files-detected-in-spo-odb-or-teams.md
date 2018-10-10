---
title: Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Découvrez où aller pour afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou équipes et comment effectuer une action sur ces fichiers.
ms.openlocfilehash: 370e5e3d4d7fd5f35caa8ef993f6245d15ee9999
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454271"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="d2916-103">Afficher des informations sur les fichiers malveillants détecté dans SharePoint, OneDrive ou Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d2916-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="d2916-p101">[Office 365 DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) protège votre organisation à partir des fichiers malveillants dans les bibliothèques de documents et des sites d’équipe. Lorsqu’un fichier malveillant est détecté, ce fichier est bloqué afin qu’aucun participant ne peut ouvrir, copier, déplacer ou partager jusqu'à ce que les autres actions effectuées par l’équipe de sécurité de l’organisation. Lisez cet article pour savoir comment afficher des informations sur les fichiers détectés et les actions à effectuer.</span><span class="sxs-lookup"><span data-stu-id="d2916-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="d2916-107">Afin d’effectuer les tâches décrites dans cet article, vous devez disposer nécessaires [autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d2916-107">In order to perform the tasks described in this article, you must have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="d2916-108">Afficher les rapports avec des informations sur les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="d2916-108">View reports with information about detected files</span></span>

<span data-ttu-id="d2916-109">Pour afficher l’état et des informations détaillées sur les fichiers qui ont été détectés par Office 365 DAV, vous pouvez utiliser le rapport d’état Threat protection.</span><span class="sxs-lookup"><span data-stu-id="d2916-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat protection status report.</span></span>
  
1. <span data-ttu-id="d2916-110">De sécurité Office 365 &amp; centre de conformité, cliquez sur **rapports** \> **tableau de bord** \> **état de protection de menace**.</span><span class="sxs-lookup"><span data-stu-id="d2916-110">In the Office 365 Security &amp; Compliance Center, choose **Reports** \> **Dashboard** \> **Threat protection status**.</span></span>
    
2. <span data-ttu-id="d2916-111">Dans le coin supérieur droit du rapport, cliquez sur **Afficher la table de détails**.</span><span class="sxs-lookup"><span data-stu-id="d2916-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="d2916-112">Afficher la liste des fichiers qui ont été détectés dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="d2916-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="d2916-113">Sélectionnez un élément dans la liste pour afficher des informations détaillées, y compris les actions effectuées, le nom de fichier, le chemin d’accès du fichier et plus.</span><span class="sxs-lookup"><span data-stu-id="d2916-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="d2916-114">Sélectionnez l’onglet **Analyse avancée** pour afficher des informations, telles qu’observée comportement et analyse les détails.</span><span class="sxs-lookup"><span data-stu-id="d2916-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="d2916-115">Afficher et agir sur les fichiers de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d2916-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="d2916-116">De sécurité Office 365 &amp; centre de conformité, cliquez sur **Gestion des menaces** \> **révision** \> **mise en quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="d2916-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="d2916-117">Dans le coin supérieur gauche, modifiez le filtre de **courrier électronique** au **contenu**.</span><span class="sxs-lookup"><span data-stu-id="d2916-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="d2916-118">Sélectionnez un élément dans la liste pour afficher des informations détaillées, y compris l’URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="d2916-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="d2916-119">Choisissez une action disponible.</span><span class="sxs-lookup"><span data-stu-id="d2916-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="d2916-120">Choisissez **version &amp; rapport** à débloquer le fichier.</span><span class="sxs-lookup"><span data-stu-id="d2916-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="d2916-121">Sélectionnez **Envoyer le rapport à Microsoft** à enregistrer le fichier comme un faux positif dans Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d2916-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="d2916-122">Cliquez sur **Télécharger le fichier** à étudier davantage le fichier.</span><span class="sxs-lookup"><span data-stu-id="d2916-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="d2916-p102">Cliquez sur **Supprimer** pour supprimer le fichier de la liste des éléments mis en quarantaine. Si vous choisissez cette option, vous devez également supprimer le fichier à partir de sa bibliothèque respectif dans SharePoint Online, OneDrive pour les professionnels ou Teams Microsoft. Cette option ne pas débloquer un fichier ouvert ou partagé.</span><span class="sxs-lookup"><span data-stu-id="d2916-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="d2916-126">Cliquez sur **Fermer** pour fermer les détails d’un élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d2916-126">Choose **Close** to close the details for a selected item.</span></span> 
  
## <a name="related-topics"></a><span data-ttu-id="d2916-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2916-127">Related topics</span></span>

[<span data-ttu-id="d2916-128">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="d2916-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="d2916-129">Afficher les rapports pour Office 365 avancée protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="d2916-129">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="d2916-130">Autorisations de sécurité Office 365 &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="d2916-130">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

[<span data-ttu-id="d2916-131">Gérer les messages mis en quarantaine et les fichiers en tant qu’administrateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="d2916-131">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
  

