---
title: Gestion des destinataires dans Exchange Online Protection (EOP)
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 2921f544-8257-4bae-8e3a-ce9250e9f162
description: Microsoft Exchange Online Protection (EOP) vous propose plusieurs façons de gérer vos destinataires de message. En tant qu'administrateur, vous pouvez réaliser certaines tâches de gestion dans le Centre d'administration Exchange (CAE) ou utiliser Windows PowerShell, et vous pouvez vérifier d'autres tâches de gestion réalisées dans le Centre d'administration Office 365 de Microsoft.
ms.openlocfilehash: 0159604eaa4e021d9ccef544306e8b274af11f18
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027571"
---
# <a name="manage-recipients-in-eop"></a><span data-ttu-id="468e9-104">Gestion des destinataires dans Exchange Online Protection (EOP)</span><span class="sxs-lookup"><span data-stu-id="468e9-104">Manage recipients in EOP</span></span>

<span data-ttu-id="468e9-p102">Microsoft Exchange Online Protection (EOP) vous propose plusieurs façons de gérer vos destinataires de message. En tant qu'administrateur, vous pouvez réaliser certaines tâches de gestion dans le Centre d'administration Exchange (CAE) ou utiliser Windows PowerShell, et vous pouvez vérifier d'autres tâches de gestion réalisées dans le Centre d'administration Office 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="468e9-p102">Microsoft Exchange Online Protection (EOP) offers several ways to manage your mail recipients. As an administrator, you can perform certain management tasks within the Exchange admin center (EAC) or using remote Windows PowerShell, and verify other management tasks performed in the Microsoft Office 365 admin center.</span></span>
  
<span data-ttu-id="468e9-107">EOP prend en charge les types de destinataires suivants :</span><span class="sxs-lookup"><span data-stu-id="468e9-107">EOP supports the following types of recipients:</span></span>
  
- <span data-ttu-id="468e9-p103">**Utilisateurs de messagerie** Les utilisateurs de messagerie sont les destinataires dans votre EOP gérés domaines. Ces destinataires ont des informations d’identification d’ouverture de session dans votre organisation Office 365, mais ils ont des adresses de messagerie externes, ce qui signifie que leurs boîtes aux lettres de destinataires sont trouvent en dehors de votre organisation en nuage. Vous pouvez ajouter des utilisateurs de messagerie afin qu’ils peuvent recevoir du courrier et vous pouvez également créer des règles de transport pour des utilisateurs spécifiques. Vous pouvez également assigner des rôles pour les utilisateurs de messagerie dans votre organisation ; les utilisateurs avec des privilèges de groupe de rôles de gestion peuvent accéder au centre d’administration Exchange (CAE) et effectuer certaines tâches de gestion. Pour en savoir plus sur les rôles d’utilisateur et comment assigner des rôles d’utilisateur dans EOP, voir [Gérer les autorisations du groupe de rôles d’administration dans EOP](manage-admin-role-group-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="468e9-p103">**Mail Users** Mail users are recipients in your EOP managed domains. These recipients have logon credentials in your Office 365 organization, but they have external email addresses, meaning that their recipient mailboxes are located outside of your cloud organization. You can add mail users so that they can receive mail and you can also create transport rules for specific users. You can also assign roles to mail users in your organization; users with management role group privileges can access the Exchange admin center (EAC) and perform certain management tasks. To learn more about user roles and how to assign user roles in EOP, see [Manage admin role group permissions in EOP](manage-admin-role-group-permissions-in-eop.md).</span></span>
    
    <span data-ttu-id="468e9-113">Pour plus d'informations sur la gestion des utilisateurs de messagerie dans EOP, consultez la rubrique [Gestion des utilisateurs de messagerie dans EOP](manage-mail-users-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="468e9-113">For more information about managing mail users in EOP, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>
    
- <span data-ttu-id="468e9-114">**Groupes** Les utilisateurs de messagerie peuvent être regroupés dans des groupes de distribution ou des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="468e9-114">**Groups** Mail users can be grouped together into distribution groups or security groups.</span></span> 
    
    <span data-ttu-id="468e9-115">Pour plus d'informations sur la gestion des groupes dans EOP, consultez la rubrique [Gestion des groupes dans Exchange Online Protection (EOP)](manage-groups-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="468e9-115">For more information about managing groups in EOP, see [Manage groups in EOP](manage-groups-in-eop.md).</span></span>
    
<span data-ttu-id="468e9-p104">Vous recherchez la version Exchange Online de cette rubrique ? Consultez la rubrique [Recipients in Exchange Online](http://technet.microsoft.com/library/50d16941-5cd7-435d-8715-e2b69f8410ab.aspx).</span><span class="sxs-lookup"><span data-stu-id="468e9-p104">Looking for the Exchange Online version of this topic? See [Recipients in Exchange Online](http://technet.microsoft.com/library/50d16941-5cd7-435d-8715-e2b69f8410ab.aspx).</span></span>
  
<span data-ttu-id="468e9-p105">Vous recherchez la version Exchange Server de cette rubrique ? Consultez la rubrique [Recipients](http://technet.microsoft.com/library/40300ed4-85a5-463d-bb3a-cf787bd44e9d.aspx).</span><span class="sxs-lookup"><span data-stu-id="468e9-p105">Looking for the Exchange Server version of this topic? See [Recipients](http://technet.microsoft.com/library/40300ed4-85a5-463d-bb3a-cf787bd44e9d.aspx).</span></span>
  

