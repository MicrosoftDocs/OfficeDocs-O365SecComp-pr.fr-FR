---
title: Set up Information Rights Management (IRM) in SharePoint admin center
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 239ce6eb-4e81-42db-bf86-a01362fed65c
description: Découvrez comment utiliser la gestion des droits relatifs à l’information (IRM) de SharePoint Online via Microsoft Azure Active Directory Rights Management Services (RMS) pour protéger les listes et les bibliothèques de documents SharePoint.
ms.openlocfilehash: 6fc51eaaf7f5d5d22167d10ab70d45dbf03cc6d2
ms.sourcegitcommit: 7c1cb9e8adb1c3e9c667f4cf02ca3cec3ec1e171
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2019
ms.locfileid: "35792070"
---
# <a name="set-up-information-rights-management-irm-in-sharepoint-admin-center"></a>Set up Information Rights Management (IRM) in SharePoint admin center

## <a name="introduction"></a>Introduction

Dans SharePoint Online, la protection IRM est appliquée aux fichiers au niveau de la liste et de la bibliothèque. Pour que votre organisation puisse utiliser la protection IRM, vous devez d’abord configurer la gestion des droits. IRM s’appuie sur le service Azure Rights Management d’Azure information protection pour chiffrer et affecter des restrictions d’utilisation. Certains plans Office 365 incluent la gestion des droits Azure, mais pas tous. Pour en savoir plus, consultez [la prise en charge d’Azure Rights Management par les services et les applications Office](https://docs.microsoft.com/azure/information-protection/understand-explore/office-apps-services-support).
  
## <a name="turn-on-irm-service-using-sharepoint-admin-center"></a>Activer le service IRM à l’aide du centre d’administration SharePoint

Pour que votre organisation puisse protéger les bibliothèques et les listes SharePoint, vous devez d’abord activer le service gestion des droits pour votre organisation. Pour savoir comment voir [activation d’Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/activate-service). Vous devez utiliser un compte professionnel ou scolaire qui dispose des privilèges d’administrateur général Office 365 pour activer le service gestion des droits. Dans le cas contraire, vous ne pourrez pas utiliser les fonctionnalités de gestion des droits relatifs à l’information avec SharePoint Online.
  
Après avoir activé le service RMS, connectez-vous au centre d’administration SharePoint pour activer la gestion des droits relatifs à l’information.
  
1. Connectez-vous à Office 365 en tant qu’administrateur général ou SharePoint.
    
2. Sélectionnez l’icône du lanceur d’applications ![Icône du lanceur d’applications dans Office 365](media/e5aee650-c566-4100-aaad-4cc2355d909f.png) dans la partie supérieure gauche, puis **Administrateur** pour ouvrir le centre d’administration Microsoft 365. (Si vous ne voyez pas la mosaïque Administration, vous ne disposez pas des autorisations d’administrateur Office 365 dans votre organisation.) 
    
3. Dans le volet de gauche, choisissez **centres** \> d’administration **SharePoint**.
    
4. Dans le volet gauche, choisissez **paramètres**, puis **page paramètres classiques**.
    
5. Dans la section gestion des droits relatifs à l' **information (IRM)** , sélectionnez **utiliser le service IRM spécifié dans votre configuration**, puis actualiser les **paramètres IRM**. Une fois que vous avez actualisé les paramètres IRM, les personnes de votre organisation peuvent commencer à utiliser la gestion des droits relatifs à l’information dans leurs bibliothèques de documents et listes SharePoint. Toutefois, les options permettant d’effectuer cette opération peuvent prendre jusqu’à une heure pour apparaître dans les paramètres de la bibliothèque et les paramètres de la liste.
    
## <a name="irm-enable-sharepoint-document-libraries-and-lists"></a>IRM-activer les listes et les bibliothèques de documents SharePoint
<a name="__toc220831191"> </a>

Après l’actualisation des paramètres IRM, les propriétaires de site peuvent protéger leurs listes et bibliothèques de documents SharePoint par IRM. Pour plus d’informations, consultez [la rubrique appliquer la gestion des droits relatifs à l’information à une liste ou une bibliothèque](apply-irm-to-a-list-or-library.md).
  
Lorsque les propriétaires de site activent la gestion des droits relatifs à l’information pour une liste ou une bibliothèque, ils peuvent protéger tous les types de fichiers pris en charge dans cette liste ou bibliothèque. Lorsque la gestion des droits relatifs à l’information est activée pour une bibliothèque, Rights Management s’applique à tous les fichiers de cette bibliothèque. Lorsque vous activez la gestion des droits relatifs à l’information (IRM) pour une liste, Rights Management s’applique uniquement aux fichiers joints à des éléments de liste, et non aux éléments de liste réels.
  
Lorsque des personnes téléchargent des fichiers dans une liste ou une bibliothèque activée pour IRM, les fichiers sont chiffrés de sorte que seules les personnes autorisées puissent les afficher. Chaque fichier géré par des droits contient également une licence d’émission qui impose des restrictions sur les personnes qui visualisent le fichier. Les restrictions habituelles incluent la création d’un fichier en lecture seule, la désactivation de la copie de texte, l’interdiction de l’enregistrement d’une copie locale et l’interdiction d’impression du fichier. Les programmes clients qui peuvent lire les types de fichiers pris en charge par IRM utilisent la licence d’émission dans le fichier géré par des droits pour appliquer ces restrictions. Voici comment un fichier géré par des droits conserve sa protection même après avoir été téléchargé. Pour activer la gestion des droits relatifs à l’information sur une liste ou une bibliothèque, voir [apply Information Rights Management to a list or Library](apply-irm-to-a-list-or-library.md).
  
Vous ne pouvez pas créer ou modifier des documents dans une bibliothèque activée pour IRM à l’aide d’Office dans un navigateur. Au lieu de cela, une personne à la fois peut télécharger et modifier des fichiers chiffrés par IRM. Utiliser l’archivage et l’extraction pour gérer la *co-création* ou la création entre plusieurs utilisateurs. 
  
Lorsque vous téléchargez un fichier PDF à partir d’une bibliothèque protégée par IRM, Office 365 crée un fichier PDF protégé. L’extension du fichier n’est pas modifiée, mais le fichier est protégé. Pour afficher ce fichier, vous devez disposer d’Azure information protection Viewer, de l’intégralité du client Azure information protection ou d’une autre application qui prend en charge l’affichage des fichiers PDF protégés. 
  
SharePoint Online prend en charge le chiffrement des types de fichiers suivants:
  
- PDF
    
- Formats de fichiers 97-2003 pour les programmes Microsoft Office suivants: Word, Excel et PowerPoint
    
- Formats Office Open XML pour les programmes Microsoft Office suivants: Word, Excel et PowerPoint
    
- Format XPS (XML Paper Specification)
    
## <a name="next-steps"></a>Étapes suivantes
<a name="__toc220831191"> </a>

Une fois que vous avez activé la gestion des droits relatifs à l’information pour SharePoint Online, vous pouvez commencer à appliquer la gestion des droits aux listes et aux bibliothèques. Pour plus d’informations, consultez [la rubrique appliquer la gestion des droits relatifs à l’information à une liste ou une bibliothèque](apply-irm-to-a-list-or-library.md).
  
Le nouveau client de synchronisation OneDrive pour Windows prend désormais en charge la synchronisation des bibliothèques de documents SharePoint et des emplacements OneDrive protégés par IRM (tant que le paramètre IRM de la bibliothèque n’est pas défini pour faire expirer les droits d’accès au document). Pour plus d’informations ou pour commencer à déployer le nouveau client de synchronisation, voir [Deploy The New OneDrive Sync client for Windows](https://support.office.com/article/3f3a511c-30c6-404a-98bf-76f95c519668).
  
[Haut de la page](#introduction)  

