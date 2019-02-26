---
title: Afficher des informations sur les fichiers malveillants détectés dans SharePoint, OneDrive ou Microsoft teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
ms.collection:
- M365-security-compliance
description: Découvrez où aller pour afficher des informations sur les fichiers malveillants détectés dans SharePoint, OneDrive ou teams et comment effectuer des actions sur ces fichiers.
ms.openlocfilehash: f5304f78ddec884748dd7d1090e2a7895044d045
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/25/2019
ms.locfileid: "30241896"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="291f2-103">Afficher des informations sur les fichiers malveillants détectés dans SharePoint, OneDrive ou Microsoft teams</span><span class="sxs-lookup"><span data-stu-id="291f2-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="291f2-p101">[Office 365 ATP pour SharePoint, OneDrive et Microsoft](atp-for-spo-odb-and-teams.md) teams protège votre organisation contre les fichiers malveillants dans les bibliothèques de documents et les sites d'équipe. Lorsqu'un fichier malveillant est détecté, ce fichier est bloqué afin que personne ne puisse l'ouvrir, le copier, le déplacer ou le partager tant que d'autres actions ne sont pas effectuées par l'équipe de sécurité de l'organisation. Lisez cet article pour savoir comment afficher des informations sur les fichiers détectés et connaître les actions à effectuer.</span><span class="sxs-lookup"><span data-stu-id="291f2-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="291f2-107">Pour effectuer les tâches décrites dans cet article, vous devez disposer des [autorisations nécessaires pour le centre de &amp; sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="291f2-107">In order to perform the tasks described in this article, you must have the necessary [permissions for the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="291f2-108">Affichage des rapports avec des informations sur les fichiers détectés</span><span class="sxs-lookup"><span data-stu-id="291f2-108">View reports with information about detected files</span></span>

<span data-ttu-id="291f2-109">Pour afficher l'État et des informations détaillées sur les fichiers qui ont été détectés par la protection avancée contre les menaces d'Office 365, vous pouvez utiliser le rapport d'état de protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="291f2-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat Protection Status report.</span></span>
  
1. <span data-ttu-id="291f2-110">dans le [centre de sécurité &amp; conformité Office 365](https://protection.office.com), choisissez **rapports** \> **tableau de bord** \> de **Protection contre les menaces**.</span><span class="sxs-lookup"><span data-stu-id="291f2-110">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
    
2. <span data-ttu-id="291f2-111">Dans le coin supérieur droit du rapport, choisissez **afficher le tableau des détails**.</span><span class="sxs-lookup"><span data-stu-id="291f2-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="291f2-112">Affichez la liste des fichiers détectés dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="291f2-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="291f2-113">Sélectionnez un élément dans la liste pour afficher des informations détaillées, notamment les actions prises, le nom de fichier, le chemin d'accès au fichier, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="291f2-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="291f2-114">Choisissez l'onglet **analyse avancée** pour afficher des informations, telles que le comportement observé et les détails de l'analyse.</span><span class="sxs-lookup"><span data-stu-id="291f2-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="291f2-115">Afficher et effectuer des actions sur les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="291f2-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="291f2-116">dans le centre de sécurité &amp; conformité d'Office 365, sélectionnez **gestion** \> des menaces- **vérification** \> de la **mise en quarantaine**.</span><span class="sxs-lookup"><span data-stu-id="291f2-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="291f2-117">Dans le coin supérieur gauche, modifiez le filtre de **courrier électronique** en **contenu**.</span><span class="sxs-lookup"><span data-stu-id="291f2-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="291f2-118">Sélectionnez un élément dans la liste pour afficher des informations détaillées, y compris l'URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="291f2-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="291f2-119">Choisissez une action disponible.</span><span class="sxs-lookup"><span data-stu-id="291f2-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="291f2-120">Choisissez **Release &amp; Report** pour débloquer le fichier.</span><span class="sxs-lookup"><span data-stu-id="291f2-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="291f2-121">Sélectionnez **Envoyer le rapport à Microsoft** pour signaler le fichier comme faux positif à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="291f2-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="291f2-122">Choisissez **Télécharger un fichier** pour rechercher plus d'renseignements sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="291f2-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="291f2-p102">Choisissez **supprimer** pour supprimer le fichier de la liste des éléments mis en quarantaine. Si vous choisissez cette option, vous devez également supprimer le fichier de sa bibliothèque respective dans SharePoint Online, OneDrive entreprise ou Microsoft Teams. Cette option ne débloque pas l'ouverture ou le partage d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="291f2-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="291f2-126">Cliquez sur **Fermer** pour fermer les détails d'un élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="291f2-126">Choose **Close** to close the details for a selected item.</span></span> 
  
  

