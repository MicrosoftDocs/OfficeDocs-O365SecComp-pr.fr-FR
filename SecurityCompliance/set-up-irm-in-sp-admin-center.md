---
title: Définir des Information Rights Management (IRM) dans le centre d’administration SharePoint
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 239ce6eb-4e81-42db-bf86-a01362fed65c
description: Découvrez comment utiliser SharePoint Online IRM par le biais de Microsoft Azure Active Directory Rights Management Services (RMS) pour protéger les listes et bibliothèques de documents SharePoint.
ms.openlocfilehash: dea8c71ce67207b3c40a1f934f90e63740f70f29
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528104"
---
# <a name="set-up-information-rights-management-irm-in-sharepoint-admin-center"></a>Définir des Information Rights Management (IRM) dans le centre d’administration SharePoint

Dans SharePoint Online, la protection IRM est appliquée aux fichiers au niveau de la liste et de bibliothèque. Avant de votre organisation permettre utiliser la protection IRM, vous devez tout d’abord définir la gestion des droits. IRM s’appuie sur le service de Azure Rights Management à partir de la Protection des informations Azure pour chiffrer et affecter les restrictions d’utilisation. Certains plans Office 365 incluent Azure Rights Management, mais pas tous. Pour en savoir plus, consultez [services et applications Office comment prendre en charge Azure Rights Management](https://docs.microsoft.com/azure/information-protection/understand-explore/office-apps-services-support).
  
## <a name="turn-on-irm-service-using-sharepoint-admin-center"></a>Activer le service IRM à l’aide du centre d’administration SharePoint

Avant que votre organisation peut les listes et bibliothèques SharePoint de protection IRM, vous devez activer le service de gestion des droits pour votre organisation. Pour savoir comment voir [Activation Azure Rights Management](https://docs.microsoft.com/information-protection/deploy-use/activate-service). Vous devez utiliser un compte professionnel ou de l’école disposant de privilèges d’administrateur général Office 365 pour activer le service de gestion des droits. Dans le cas contraire, vous ne pourrez pas utiliser les fonctionnalités IRM avec SharePoint Online.
  
Après avoir activé le service de gestion des droits, connectez-vous au centre d’administration SharePoint pour activer IRM.
  
1. Connectez-vous à Office 365 en tant qu’administrateur général ou SharePoint.
    
2. Sélectionnez l’icône du lanceur d’applications ![Icône du lanceur d’applications dans Office 365](media/e5aee650-c566-4100-aaad-4cc2355d909f.png) dans le coin supérieur gauche, puis sélectionnez **Administration** pour ouvrir le centre d’administration Office 365. (Si la vignette d’administration ne s’affiche pas, vous ne disposez pas des autorisations d’administrateur Office 365 dans votre organisation.) 
    
3. Dans le volet gauche, choisissez **Admin centres** \> **SharePoint**.
    
4. Dans le volet gauche, cliquez sur **paramètres**.
    
5. Dans la section **Information Rights Management (IRM)** , sélectionnez **utiliser le service IRM spécifié dans votre configuration**, puis **Actualiser les paramètres IRM**. Une fois que vous actualisez des paramètres IRM, personnes dans votre organisation peuvent commencer à l’aide d’IRM dans leurs listes SharePoint et les bibliothèques de documents. Toutefois, les options à le faire peuvent prendre une heure apparaissent dans les paramètres de la bibliothèque et les paramètres de la liste.
    
## <a name="irm-enable-sharepoint-document-libraries-and-lists"></a>Listes et bibliothèques de documents SharePoint activer IRM
<a name="__toc220831191"> </a>

Après l’actualisation des paramètres IRM, les propriétaires de sites peuvent Protégez-le leurs listes SharePoint et les bibliothèques de documents. Pour plus d’informations, voir [Appliquer Information Rights Management pour une liste ou une bibliothèque](apply-irm-to-a-list-or-library.md).
  
Lorsque les propriétaires de sites activer IRM pour une liste ou une bibliothèque, ils peuvent protéger tous les types de fichiers pris en charge dans cette liste ou bibliothèque. Lorsqu’IRM est activé pour une bibliothèque, gestion des droits s’applique à tous les fichiers dans cette bibliothèque. Lorsque vous activez IRM pour une liste, gestion des droits s’applique uniquement aux fichiers qui sont joints à des éléments de liste, pas les éléments de liste proprement dite.
  
Lorsque les utilisateurs téléchargent des fichiers dans une IRM activé une liste ou une bibliothèque, les fichiers sont chiffrés afin que seules les personnes autorisées puissent les consulter. Chaque fichier géré par des droits contient aussi une licence d’émission qui impose des restrictions sur les personnes qui permet d’afficher le fichier. Restrictions habituelles consistent un fichier en lecture seule, désactivation de la copie de texte, empêcher l’enregistrement d’une copie locale et de l’impression du fichier. Les programmes clients qui peuvent lire des types de fichiers pris en charge IRM utilisent la licence d’émission dans le fichier géré par des droits pour appliquer ces restrictions. Voici comment un fichier géré par des droits conserve sa protection même après que l’avoir téléchargé. Pour activer IRM sur une liste ou une bibliothèque, voir [Appliquer Information Rights Management pour une liste ou une bibliothèque](apply-irm-to-a-list-or-library.md).
  
Vous ne pouvez pas créer ou modifier des documents dans une bibliothèque protégée par IRM à l’aide d’Office Online. Au lieu de cela, une personne à la fois peut télécharger et modifier des fichiers chiffrés par IRM. Utilisation d’archivage et extraction afin de gérer la *co-création* ou de plusieurs utilisateurs. 
  
Lorsque vous téléchargez un fichier PDF à partir d’une bibliothèque protégés par IRM, Office 365 crée un fichier PDF protégé. Ne modifie pas l’extension de fichier, mais le fichier est protégé. Pour afficher ce fichier, vous devez la visionneuse de Protection des informations Azure, le client de la Protection des informations Azure complète, ou une autre application qui prend en charge d’affichage protégé des fichiers PDF. 
  
SharePoint Online prend en charge le chiffrement des types de fichiers suivants :
  
- PDF
    
- Les formats de fichiers 97-2003 pour les programmes Microsoft Office suivants : Word, Excel et PowerPoint
    
- Des formats Office Open XML pour les programmes Microsoft Office suivants : Word, Excel et PowerPoint
    
- Le format XML Paper Specification (XPS)
    
## <a name="next-steps"></a>Étapes suivantes
<a name="__toc220831191"> </a>

Une fois que vous avez activé IRM pour SharePoint Online, vous pouvez démarrer l’application de gestion des droits relatifs à des listes et bibliothèques. Pour plus d’informations, voir [Appliquer Information Rights Management pour une liste ou une bibliothèque](apply-irm-to-a-list-or-library.md).
  
Le nouveau client de synchronisation OneDrive pour Windows prend désormais en charge la synchronisation des bibliothèques de documents protégés par IRM de SharePoint et les emplacements de OneDrive (à condition que le paramètre IRM pour la bibliothèque n’est pas défini sur expiration des droits d’accès de document). Pour plus d’informations, ou de déployer le nouveau client de synchronisation, voir [déployer le nouveau client de synchronisation OneDrive pour Windows](https://support.office.com/article/3f3a511c-30c6-404a-98bf-76f95c519668).
  
[Haut de Page](set-up-irm-in-sp-admin-center.md#__top)
  

