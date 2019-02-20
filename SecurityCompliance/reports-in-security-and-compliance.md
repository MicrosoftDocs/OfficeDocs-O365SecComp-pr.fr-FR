---
title: Rapports dans le Centre de conformité et sécurité Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: "Utilisez le centre de sécurité & conformité d'Office 365 pour obtenir divers rapports pour votre organisation SharePoint Online et Exchange Online, ainsi que pour les rapports Azure Active Directory.  "
ms.openlocfilehash: 36e6d3efce1758d52cd30451a2b60b19f4654056
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087303"
---
# <a name="reports-in-the-office-365-security--compliance-center"></a>Rapports dans le Centre de conformité et sécurité Office 365

Vous pouvez utiliser la page **afficher les rapports** du centre de conformité & de la sécurité d'Office 365 pour accéder rapidement aux rapports d'audit de vos organisations SharePoint Online et Exchange Online. Vous pouvez également accéder aux rapports de connexion de l'utilisateur Azure Active Directory (AD), aux rapports d'activité de l'utilisateur et au Journal d'audit Azure AD à partir de la page **afficher les rapports** . Cela est dû au fait que votre abonnement Office 365 payant inclut un abonnement gratuit à Microsoft Azure. La première fois que vous essayez d'accéder à ces rapports Azure, vous devez effectuer un processus d'enregistrement unique. 
  
> [!TIP]
> Pour afficher des rapports supplémentaires sur l'activité dans votre organisation Office 365, reportez-vous à [rapports d'activité dans le centre d'administration office 365](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263). 
  
 **Avant de commencer**
  
Vous avez besoin des autorisations suivantes pour afficher des rapports dans le centre de sécurité & Compliance Center.
  
- Vous devez disposer du rôle lecteur de sécurité dans le centre d'administration Exchange pour afficher les rapports dans le centre de sécurité & Compliance Center. Par défaut, ce rôle est affecté aux groupes de rôles gestion de l'organisation et lecteur de sécurité dans le centre d'administration Exchange.
    
- Vous devez disposer du rôle de gestion de conformité DLP en affichage seul dans le centre de sécurité & Compliance Center pour afficher les rapports DLP dans le centre de sécurité & Compliance Center. Par défaut, ce rôle est affecté aux groupes de rôles Administrateur de conformité, gestion de l'organisation, administrateur de sécurité et lecteur de sécurité dans le centre de sécurité & Compliance Center.

- De plus, vous devez disposer du rôle de destinataires en affichage seul dans le centre d'administration Exchange pour afficher les rapports DLP dans le centre d'administration Exchange. Par défaut, ce rôle est affecté aux groupes de rôles gestion de la conformité, gestion de l'organisation et gestion de l'organisation en affichage seul du centre d'administration Exchange.
  
 **Pour ouvrir la page afficher les rapports dans le centre de sécurité & conformité, procédez comme suit:**
  
1. Accédez à [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports).
    
2. Connectez-vous à Office 365 à l'aide des informations d'identification d'un compte d'utilisateur dans votre organisation Office 365.
    
Sur la page **afficher les rapports** , vous pouvez afficher les types de rapports suivants: 
  
- [Rapports d’audit dans EOP](#auditing-reports)
- [Rapport de vérification de surveillance](#supervisory-review-report)
- [Rapports de protection contre la perte de données](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>Rapports d'audit

Le tableau suivant décrit les rapports figurant dans la section **audit** de la page **afficher les rapports** du centre de sécurité et de conformité &. 
  
|**Rapport**|**Description**|
|:-----|:-----|
|**Rapport du journal d'audit Office 365** <br/> |Vous pouvez rechercher dans le journal d'audit Office 365 des activités de l'utilisateur et de l'administrateur dans votre organisation Office 365. Le rapport contient les entrées utilisateur et administrateur dans Exchange Online, SharePoint Online, OneDrive entreprise et Azure Active Directory, qui est le service d'annuaire pour Office 365. Pour plus d'informations, reportez-vous à [la rubrique Search the Audit Log in the Office 365 Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md).<br/> |
|**Rapports Azure AD** <br/> |Pour rechercher des activités de connexion inhabituelles ou suspectes dans votre organisation Office 365, vous pouvez utiliser des rapports de connexion et d'activité dans Microsoft Azure. Vous pouvez également afficher les événements dans le journal d'audit Azure AD. Pour afficher les rapports dans Azure, il vous suffit de cliquer sur **afficher les rapports Azure ad**. Pour plus d'informations, voir:<br/><br/>[Utilisez votre abonnement Azure Active Directory gratuit dans Office 365](use-your-free-azure-ad-subscription-in-office-365.md). <br/> [Afficher vos rapports d'utilisation et d'accès](http://go.microsoft.com/fwlink/p/?LinkId=506902).  <br/> |
|**Rapports d’audit Exchange** <br/> | Vous pouvez utiliser la fonctionnalité d'audit dans Office 365 pour suivre les modifications apportées à votre configuration Exchange Online par les administrateurs de votre organisation. Les modifications apportées à votre organisation Exchange Online par un administrateur du centre de données Microsoft ou par un administrateur délégué sont également consignées. Pour Exchange Online, la journalisation d'audit de l'administrateur est activée par défaut, de sorte que vous n'avez rien à faire pour l'activer. Exchange Online fournit également une journalisation d'audit de boîte aux lettres pour vous permettre de suivre l'accès aux boîtes aux lettres par une personne autre que le propriétaire de la boîte aux lettres. Vous devez activer l'enregistrement d'audit de boîte aux lettres pour chaque boîte aux lettres dont vous souhaitez suivre l'accès non-propriétaire.<br/>  Pour l'enregistrement d'audit de l'administrateur et de la boîte aux lettres, vous pouvez exécuter des rapports d'audit pour afficher les entrées du journal d'audit. Vous pouvez également exporter des journaux d'audit de boîte aux lettres et d'administration, qui vous sont envoyés dans les 24 heures, dans un fichier XML joint à un message électronique.<br/><br/>Pour plus d'informations sur l'exportation des journaux d'audit, voir:  <br/><br/> [Exporter les journaux d’audit de boîte aux lettres](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [Afficher et exporter le journal d'audit de l'administrateur de centre de fichiers](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [Rechercher les modifications des groupes de rôles ou les journaux d’audit de l’administrateur](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Rapports d'audit Exchange](http://go.microsoft.com/fwlink/p/?LinkID=395232).  <br/> |
   
## <a name="supervisory-review-report"></a>Rapport de vérification de surveillance

Avec le rapport de vérification de surveillance, vous pouvez voir l'état de toutes les stratégies de vérification de surveillance dans votre organisation. Pour plus d'informations, consultez [la rubrique Configurer des stratégies de vérification de surveillance pour votre organisation](configure-supervision-policies.md).
  
## <a name="data-loss-prevention-reports"></a>Rapports de protection contre la perte de données

Les rapports de protection contre la perte de données (DLP) contiennent des informations sur les stratégies et les règles DLP appliquées au contenu contenant des données sensibles dans votre organisation Office 365. Vous pouvez également configurer le rapport pour qu'il affiche des informations sur les actions DLP basées sur votre stratégie et vos règles DLP. Pour plus d'informations, consultez [la rubrique afficher le rapport de protection contre la perte de données](view-the-dlp-reports.md).
