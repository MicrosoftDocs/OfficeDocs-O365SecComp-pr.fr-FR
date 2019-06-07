---
title: Liens fiables Office 365 ATP (Protection avancée contre les menaces)
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.date: 05/17/2019
ms.topic: overview
f1_keywords:
- "197503"
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
- ZVO160
- ZXL160
- ZPP160
- ZWD160
ms.assetid: dd6a1fef-ec4a-4cf4-a25a-bb591c5811e3
description: La fonctionnalité liens fiables permet de vérifier le temps de cliquer sur les liens hypertexte dans les documents Office et dans les messages électroniques. Utilisez des liens fiables pour protéger votre organisation contre le hameçonnage et les autres attaques.
ms.openlocfilehash: 4f1449fb97ad8d8f263073c917eed2c399bf4f22
ms.sourcegitcommit: ff1d18aaddde2048f1cf88338c916295cf8c354e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2019
ms.locfileid: "34748577"
---
# <a name="office-365-atp-safe-links"></a>Liens fiables Office 365 ATP (Protection avancée contre les menaces)

## <a name="overview-of-office-365-atp-safe-links"></a>Vue d’ensemble des liens fiables Office 365 ATP

> [!IMPORTANT]
> Cet article est destiné aux clients professionnels qui disposent d' [Office 365 Advanced Threat Protection](office-365-atp.md). Si vous utilisez Outlook.com, Office 365 Home ou Office 365 Personal, et que vous recherchez des informations sur les liens fiables dans Outlook, consultez [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Office 365 DAV Safe Links (partie de la [protection avancée contre les menaces](office-365-atp.md)) peut vous aider à protéger votre organisation en fournissant un temps de clic pour la vérification des adresses Web (URL) dans [les messages électroniques](how-atp-safe-links-works.md#how-atp-safe-links-works-with-urls-in-email) et les [documents Office](how-atp-safe-links-works.md#how-atp-safe-links-works-with-urls-in-office-documents). La protection est définie via les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) définies par votre équipe de sécurité Office 365.
  
Une fois vos stratégies de liens fiables ATP en place, les administrateurs globaux d’Office 365, les administrateurs de sécurité et les lecteurs de sécurité peuvent [afficher des rapports pour une protection avancée contre les menaces](view-reports-for-atp.md). Les informations contenues dans ces rapports peuvent aider votre équipe de sécurité à prendre des mesures supplémentaires pour protéger votre organisation ou Rechercher des incidents de sécurité.

À mesure que de [nouvelles fonctionnalités sont ajoutées à](office-365-atp.md#new-features-in-office-365-atp)la protection avancée contre les menaces, votre équipe de sécurité Office 365 peut ajouter ou modifier les [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md)de votre organisation. En outre, vous pouvez remarquer des modifications et des améliorations, telles que les [pages d’avertissement](atp-safe-links-warning-pages.md) et le rendu de liens natifs nouvellement modifiés dans Outlook (introduits dans la version 1809 d’Office 365 ProPlus).
         
## <a name="how-to-get-atp-safe-links-protection"></a>Comment obtenir la protection des liens fiables ATP

Tout d’abord, assurez-vous **que votre abonnement inclut la [protection avancée contre les menaces](office-365-atp.md)**. La protection avancée contre les menaces est incluse dans les abonnements, tels que [microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation a5, etc. Si votre organisation dispose d’un abonnement Office 365 qui n’inclut pas Office 365 ATP, vous pouvez acheter l’ATP en tant que module complémentaire. Pour plus d’informations, reportez-vous aux ressources suivantes : 

- [Offres et tarifs de protection avancée contre les menaces Office 365](https://products.office.com/exchange/advance-threat-protection)

- [Description du service Office 365 - Protection avancée contre les menaces](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) 
  
Ensuite, assurez-vous **que vos stratégies de liens fiables ATP sont définies**. (Consultez la rubrique [set up Office 365 ATP Safe Links Policies](set-up-atp-safe-links-policies.md).) Les fonctionnalités de liens fiables ATP sont actives dans les cas suivants:
  
- Les stratégies de liens fiables ATP sont configurées pour le courrier électronique et les documents Office. (Voir [configurer des stratégies de liens fiables ATP dans Office 365](set-up-atp-safe-links-policies.md).)

- Les applications clientes Office 365 sont configurées pour utiliser l’authentification moderne (il s’agit de la protection des liens fiables ATP dans les documents Office). (Consultez la rubrique [authentification moderne pour Office 2016](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).) 
    
- Les utilisateurs se sont connectés à Office 365 à l’aide de leur compte professionnel ou scolaire. (Voir [connexion à Office ou office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)
    
- La messagerie de votre organisation passe par Exchange Online Protection.  

Assurez- **vous également que vous disposez des autorisations nécessaires**. Pour définir (ou modifier) des stratégies ATP, vous devez disposer d’un rôle approprié. Certains exemples sont décrits dans le tableau suivant:

|Role  |WHERE/How Assigned  |
|---------|---------|
|Administrateur général Office 365 |La personne qui s’inscrit pour acheter Office 365 est un administrateur global par défaut. (Pour en savoir plus, consultez la rubrique [à propos des rôles d’administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Administrateur de sécurité |Centre d’administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()|
|Gestion de l’organisation Exchange Online |Centre d’administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>ou <br>  Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a>Comment s’assurer que la protection des liens fiables DAV est en place

En tant qu’administrateur général ou administrateur de sécurité, veillez à consulter régulièrement vos [stratégies de liens fiables ATP](set-up-atp-safe-links-policies.md) . Les stratégies de liens fiables ATP déterminent si la protection s’applique aux liens hypertexte dans les messages électroniques uniquement ou aux URL des documents Office également.

Une fois les stratégies de liens fiables ATP en place, l’équipe de sécurité de votre organisation peut voir le fonctionnement de la protection des liens fiables disponible pour votre organisation en [affichant des rapports pour une protection avancée contre les menaces](view-reports-for-atp.md). 

## <a name="example-scenarios"></a>Exemples de scénarios
  
Le tableau suivant décrit certains exemples de scénarios dans lesquels la protection des liens fiables ATP peut ou non être mise en place. (Dans tous ces cas, nous partons du principe que l’organisation dispose d’Office 365 entreprise E5).
  
|**Exemple de scénario**|**Est-ce que la protection des liens fiables DAV s’applique dans ce cas?**|
|:-----|:-----|
|Jean est membre d’un groupe qui a des stratégies de liens fiables ATP couvrant les URL des documents de messagerie et Office. Jean ouvre une présentation PowerPoint qu’une personne a envoyée, puis clique sur une URL dans la présentation.  <br/> |Oui. Les stratégies de liens fiables ATP définies s’appliquent au groupe de Jean, à la messagerie de Jean, ainsi qu’aux documents Word, Excel, PowerPoint ou Visio que Jean ouvre, tant que Jean est connecté et qu’il utilise Office 365 ProPlus sur des appareils Windows, iOS ou Android.  <br/> |
|Dans l’organisation de Chris, aucun administrateur général ou de sécurité n’a défini de stratégie de liens fiables ATP. Chris reçoit un courrier électronique contenant une URL vers un site Web malveillant. Chris ignore que l’URL est malveillante et clique sur le lien.  <br/> |Non. La stratégie par défaut qui couvre les URL de tous les membres de l’organisation doit être définie de manière à ce que la protection soit mise en place.  <br/> |
|Dans l’organisation de Pat, aucun administrateur général ou de sécurité n’a défini ou modifié les stratégies de liens fiables ATP. Pat ouvre un document Word et clique sur une URL dans le fichier.  <br/> |Non. Une stratégie qui inclut des documents Office doit être définie de manière à ce que la protection soit mise en place. Consultez la rubrique [configurer des stratégies de liens fiables ATP dans Office 365](set-up-atp-safe-links-policies.md).  <br/> |
|L’organisation de Lee a une stratégie de liens approuvés ATP `http://tailspintoys.com` qui apparaît sous la forme d’un site Web bloqué. Lee reçoit un message électronique contenant une URL vers `http://tailspintoys.com/aboutus/trythispage`. Lee clique sur l’URL.  <br/> |Cela dépend du fait que le site entier et toutes ses sous-pages sont inclus dans la liste des URL bloquées. Consultez [la rubrique Configurer une liste d’URL bloquées personnalisées à l’aide de liens fiables ATP](set-up-a-custom-blocked-urls-list-wtih-atp.md).  <br/> |
|Marie, collègue de Jean, envoie un message électronique à Jean, sans savoir que le courrier électronique contient une URL malveillante.  <br/> |Cela dépend du fait que des stratégies de liens fiables ATP sont définies pour les messages envoyés au sein de l’organisation. Consultez la rubrique [configurer des stratégies de liens fiables ATP dans Office 365](set-up-atp-safe-links-policies.md).  <br/> |


  

