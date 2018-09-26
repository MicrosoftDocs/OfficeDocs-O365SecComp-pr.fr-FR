---
title: Rapports de la sécurité Office 365 &amp; centre de conformité
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/1/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: 'Utilisez le Office 365 Security &amp; rapports de centre de conformité pour obtenir différents rapports pour votre organisation Exchange Online et SharePoint Online, ainsi que Azure Active Directory.  '
ms.openlocfilehash: 019ccc49352db1aaf392287f62fa63f66913e293
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038337"
---
# <a name="reports-in-the-office-365-security-amp-compliance-center"></a>Rapports de la sécurité Office 365 &amp; centre de conformité

Vous pouvez utiliser la page **Afficher les rapports** de sécurité Office 365 &amp; centre de conformité pour accéder rapidement aux rapports d’audit pour votre organisation Exchange Online et SharePoint Online. Vous pouvez également accéder Azure Active Directory (AD) utilisateur connexion rapports, rapports d’activité de l’utilisateur, et ouvrir une session à partir de la page **Afficher les rapports** d’audit de l’Azure AD. Il s’agit, car votre abonnement payant à Office 365 comprend un abonnement gratuit à Microsoft Azure. La première fois que vous tentez d’accéder à ces rapports Azure, vous devrez effectuer un processus d’enregistrement unique. 
  
> [!TIP]
> Pour afficher les rapports supplémentaires sur l’activité dans votre organisation Office 365, voir [Les rapports d’activité dans le centre d’administration d’Office 365](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263). 
  
 **Avant de commencer**
  
Vous devez disposer des autorisations suivantes pour afficher les rapports de sécurité &amp; centre de conformité.
  
- Vous devez attribuer le rôle de lecture de la sécurité dans le centre d’administration Exchange (EAC) pour afficher les rapports de sécurité &amp; centre de conformité. Par défaut, ce rôle est attribué pour les groupes de rôles de gestion de l’organisation et la lecture de sécurité dans le centre d’administration Exchange.
    
- Vous devez attribuer le rôle de gestion de la conformité DLP dans la sécurité &amp; centre de conformité pour afficher les rapports DLP (et les stratégies DLP) de la sécurité &amp; centre de conformité. Par défaut, ce rôle est attribué aux groupes de rôle administrateur de conformité, gestion de l’organisation et administrateur de sécurité de la sécurité &amp; centre de conformité.
    
En outre, vous devez attribuer le rôle de protection contre la perte de données dans le CAE pour afficher les rapports DLP (et les stratégies DLP) dans le CAE. Par défaut, ce rôle est attribué aux groupes de rôle de gestion de la conformité et de gestion de l’organisation dans le CAE.
  
 **Pour ouvrir la page Rapports d’affichage de la sécurité &amp; centre de conformité :**
  
1. Accédez à [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports).
    
2. Connectez-vous à Office 365 avec les informations d’identification pour un compte d’utilisateur dans votre organisation Office 365.
    
Dans la page **Afficher les rapports** , vous pouvez afficher les types de rapports suivants : 
  
- [Rapports d’audit dans EOP](#auditing-reports)
- [Rapport d’examen de surveillance](#supervisory-review-report)
- [Rapports de protection contre la perte de données](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>Rapports d'audit

Le tableau suivant décrit les rapports, dans la section **audit** , dans la page **Afficher les rapports** de sécurité &amp; centre de conformité. 
  
|**Rapport**|**Description**|
|:-----|:-----|
|**Rapport du journal d’audit Office 365** <br/> |Vous pouvez rechercher le journal d’audit de Office 365 pour l’activité utilisateur et d’administration dans votre organisation Office 365. Le rapport contient les entrées utilisateur et administrateur de l’activité dans Exchange Online, SharePoint Online, OneDrive pour les entreprises et Azure Active Directory, qui est le service d’annuaire pour Office 365. Pour plus d’informations, voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).<br/> |
|**Rapports Azure AD** <br/> |Pour rechercher les inhabituelle ou suspecte activité de connexion dans votre organisation Office 365, vous pouvez utiliser la connexion et l’activité des rapports dans Microsoft Azure. Vous pouvez également afficher les événements dans le journal d’audit Azure AD. Pour afficher les rapports dans Azure, cliquez simplement sur **Azure AD d’afficher les rapports**. Pour plus d’informations, voir :<br/><br/>[Utilisez votre abonnement Azure Active Directory disponible dans Office 365](use-your-free-azure-ad-subscription-in-office-365.md). <br/> [Afficher vos rapports d’accès et d’utilisation](http://go.microsoft.com/fwlink/p/?LinkId=506902).  <br/> |
|**Rapports d’audit Exchange** <br/> | Vous pouvez utiliser la fonctionnalité d’audit dans Office 365 pour suivre les modifications apportées à votre configuration Exchange Online par les administrateurs de votre organisation. Modifications apportées à votre organisation Exchange Online par un administrateur de centre de données Microsoft ou par un administrateur délégué sont également consignées. Pour Exchange Online, d’audit d’administrateur la journalisation est activée par défaut, afin que vous n’êtes pas obligé de faire quoi que ce soit pour l’activer. Exchange Online fournit également d’audit de boîte aux lettres la journalisation pour vous permettre de suivre l’accès aux boîtes aux lettres par une personne autre que le propriétaire de la boîte aux lettres. Vous devez activer la boîte aux lettres enregistrement d’audit pour chaque boîte aux lettres que vous souhaitez effectuer le suivi d’accès non-propriétaire.<br/>  Enregistrement d’audit pour l’administration et de boîte aux lettres, vous pouvez exécuter des rapports d’audit pour afficher les entrées du journal d’audit. Vous pouvez également exporter des journaux d’audit boîtes aux lettres et d’administration, qui vous sont envoyées dans les 24 heures dans un fichier XML qui est lié au message électronique.<br/><br/>Pour plus d’informations sur l’exportation des journaux d’audit, voir :  <br/><br/> [Exporter les journaux d’audit de boîte aux lettres](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [Afficher et exporter le journal d’audit de centre de données d’administration](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [Rechercher les modifications de groupe de rôles ou des journaux d’audit administrateur](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Rapports d’audit Exchange](http://go.microsoft.com/fwlink/p/?LinkID=395232).  <br/> |
   
## <a name="supervisory-review-report"></a>Rapport d’examen de surveillance

Avec le rapport d’examen de surveillance, vous pouvez voir l’état de toutes les stratégies de supervision dans votre organisation. Pour plus d’informations, voir [Configure surveillance passez en revue les stratégies pour votre organisation](configure-supervision-policies.md).
  
## <a name="data-loss-prevention-reports"></a>Rapports de protection contre la perte de données

Les rapports de protection contre la perte de données (DLP) contiennent des informations sur les stratégies DLP et les règles qui ont été appliqués au contenu contiennent des données sensibles dans votre organisation Office 365. Vous pouvez également configurer le rapport pour afficher des informations sur les actions de DLP basée sur les règles de stratégie DLP. Pour plus d’informations, voir [Afficher le rapport pour la protection contre la perte de données](view-the-dlp-reports.md).
