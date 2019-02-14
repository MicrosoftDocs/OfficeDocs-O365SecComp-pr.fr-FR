---
title: Liens fiables ATP Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/11/2019
ms.topic: overview
f1_keywords:
- "197503"
ms.service: o365-administration
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
description: La fonctionnalité de liens fiables offre-heure des clics de vérification des liens hypertexte dans les documents Office et dans les messages électroniques. Utilisez les liens sécurisés pour protéger votre organisation contre les attaques par hameçonnage et les autres attaques.
ms.openlocfilehash: 77b7ac4af8cd9ad27f18af6fd55588e320da69ac
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995345"
---
# <a name="office-365-atp-safe-links"></a>Liens fiables ATP Office 365

## <a name="overview-of-office-365-atp-safe-links"></a>Vue d’ensemble de liens de DAV Safe Office 365

> [!IMPORTANT]
> Cet article est destiné aux entreprises. Si vous êtes un utilisateur vous recherchez des informations sur les liens sécurisés dans Outlook, voir [sécurité Outlook.com avancés](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Office 365 DAV liens sécurisés (partie de la [Protection contre les menaces avancées](office-365-atp.md)) peuvent aider à protéger votre organisation en fournissant-heure des clics de vérification des adresses web (URL) dans [les messages électroniques](#how-atp-safe-links-works-with-email) et des [documents Office](#how-atp-safe-links-works-with-office-documents). Protection est définie par le biais de [liens fiables DAV stratégies](set-up-atp-safe-links-policies.md) définies par votre équipe de sécurité d’Office 365. 
  
Une fois vos stratégies de liens fiables DAV sont mis en place, les administrateurs globaux Office 365, les administrateurs de sécurité et les lecteurs de sécurité peuvent [Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md). Les informations contenues dans ces rapports peuvent aider votre équipe de sécurité à prendre des mesures supplémentaires pour protéger votre organisation ou de rechercher des incidents de sécurité.

En tant [nouvelles fonctionnalités sont ajoutées à la vente](office-365-atp.md#new-features-are-continually-being-added-to-atp), votre équipe de sécurité d’Office 365 pour ajouter ou modifier les stratégies de liens fiables DAV de votre organisation. En outre, vous pouvez remarquer des modifications et des améliorations, telles que nos nouvellement révisées [pages avertissement](atp-safe-links-warning-pages.md) et le lien native d’affichage dans Outlook.
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a>Fonctionnement des liens fiables DAV avec des URL dans le message électronique

À un niveau élevé, voici le fonctionne de protection des liens fiables DAV pour les URL dans le message électronique (hébergé dans Office 365, pas sur site) :
  
1. Personnes reçoivent des messages électroniques, dont certains contiennent des URL.
    
2. Tout le courrier conduit via Exchange Online Protection, où IP (internet protocol) et le format d’enveloppe filtre, en fonction de signature de programmes malveillants, anti-spam et contre les programmes malveillants filtres sont appliqués. 
    
3. Courrier électronique arrive-t-il dans la boîte de réception des utilisateurs.
    
4. Un utilisateur se connecte à Office 365 et accède à leur boîte de réception.
    
5. L’utilisateur ouvre un message électronique et clique sur une URL dans le message électronique.
    
6. La fonctionnalité des liens sans échec DAV vérifie immédiatement l’URL avant d’ouvrir le site Web. L’URL est identifiée comme bloqué, malveillantes ou sécurisé.
    
    - Si l’URL est un site Web qui est inclus dans une [liste d’URL « Pas de rewrite » personnalisée](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) pour une stratégie qui s’applique à l’utilisateur, le site Web s’ouvre. 
    
    - Si l’URL est sur un site Web qui est inclus dans [personnalisé liste URL bloquée l’organisation](set-up-a-custom-blocked-urls-list-wtih-atp.md), une [page d’avertissement](atp-safe-links-warning-pages.md) s’ouvre. 
    
    - Si l’URL est sur un site Web qui a été déterminé malveillante, une [page d’avertissement](atp-safe-links-warning-pages.md) s’ouvre. 
    
    - Si l’URL accède à un fichier téléchargeable et votre organisation [liens fiables DAV stratégies](set-up-atp-safe-links-policies.md) sont configurées pour analyser le contenu, le fichier téléchargeable est vérifié. 
    
    - Si l’URL est déterminée pour être sûr, le site Web s’ouvre.
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>Fonctionnement des liens fiables DAV avec des URL dans les documents Office

À un niveau élevé, voici le fonctionne de protection DAV des liens sécurisés pour les URL dans les applications Office 365 ProPlus (versions actuelles de Word, Excel et PowerPoint sur Windows ou Mac, les applications Office sur iOS ou Android appareils, Visio sur Office Online, OneNote en ligne et Windows) :
  
1. Personnes ont installé Office 365 ProPlus sur leur ordinateur, smartphone ou tablette. (Ou, ils sont à l’aide en ligne Office dans leur navigateur.)
    
2. Un utilisateur ouvre une Word, Excel, PowerPoint ou Visio et se connecte à Office 365 pour entreprises à l’aide de leur compte professionnel ou de l’école. Le document contient des URL.
    
3. Lorsque l’utilisateur clique sur une URL dans le document, le lien est vérifié par le service de liens fiables DAV.
    
  - Si l’URL est un site Web qui est inclus dans une [liste d’URL « Pas de rewrite » personnalisée](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) pour une stratégie qui s’applique à l’utilisateur, que l’utilisateur est nécessaire pour le site Web. 
    
  - Si l’URL est sur un site Web qui est inclus dans [personnalisé liste URL bloquée l’organisation](set-up-a-custom-blocked-urls-list-wtih-atp.md), l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).
    
  - Si l’URL est sur un site Web qui a été déterminé malveillante, l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).
    
  - Si l’URL accède à un fichier à télécharger et les [stratégies de liens fiables DAV](set-up-atp-safe-links-policies.md) sont configurés pour l’analyse des téléchargements, le fichier téléchargeable est vérifié. 
    
  - Si l’URL est fiable, l’utilisateur est dirigé vers le site Web.

## <a name="how-to-get-atp-safe-links-protection"></a>Comment obtenir la protection des liens fiables DAV

Tout d’abord, assurez-vous que votre abonnement comprend la [Protection contre les menaces avancées](office-365-atp.md). DAV est inclus dans les abonnements, tels que [Microsoft 365 pour entreprises](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation A5, etc.. Si votre organisation a un abonnement à Office 365 qui n’inclut pas d’Office 365 DAV, vous pouvez acheter potentiellement DAV comme module complémentaire. Pour plus d’informations, voir [plans Office 365 avancée protection contre les menaces et les prix](https://products.office.com/exchange/advance-threat-protection) et [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 
  
Ensuite, assurez-vous que vos stratégies de liens fiables DAV sont définis. (Voir [définir des stratégies Office 365 DAV fiables liens](set-up-atp-safe-links-policies.md)). Fonctionnalités de liens fiables DAV sont actifs quand :
  
- **Liens approuvés DAV stratégies sont configurés** pour le courrier électronique et pour les documents Word, Excel, PowerPoint et Visio. (Voir [définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)).

- **Les applications client Office 365 sont configurées pour utiliser l’authentification moderne** (il s’agit de protection DAV fiables liens dans les documents Office). (Voir [authentification moderne pour Office 2016](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).) 
    
- **Les utilisateurs ont connecté à Office 365** à l’aide de leur compte professionnel ou de l’école. (Voir [se connecter à Office ou Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)).
    
- **Passe de messagerie de votre organisation via Exchange Online Protection**.  

Pour définir (ou modifier) les stratégies de vente, vous devez posséder un des rôles décrits dans le tableau suivant :

|Rôle  |Où/procédure affecté  |
|---------|---------|
|Administrateur Global d’Office 365 |La personne qui s’inscrit à acheter Office 365 est un administrateur global par défaut. (Voir [les rôles d’administration sur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) pour en savoir plus).         |
|Administrateur de sécurité |Centre d’administration Active Directory Azure ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Gestion de l’organisation en ligne Exchange |Centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a>Pour rendre la protection de liens fiables DAV qu’est en place

En tant qu’un administrateur global ou administrateur de sécurité, veillez à consulter vos [stratégies de liens fiables DAV](set-up-atp-safe-links-policies.md). Stratégies de liens fiables DAV pour déterminer si protection applicable des liens hypertexte dans les messages électroniques, ou à l’URL dans des documents Office.

Une fois que les stratégies de liens fiables DAV sont en place, l’équipe de sécurité de votre organisation peut voir voir fonctionne de protection des liens fiables DAV pour votre organisation est en [affichage de rapports de protection contre les menaces avancées](view-reports-for-atp.md). 

## <a name="example-scenarios"></a>Exemples de scénarios
  
Le tableau suivant décrit quelques exemples de scénarios où protection liens fiables DAV peut ou ne peut pas en place. (Dans tous les cas, nous partons du principe que l’organisation a Office 365 entreprise E5.)
  
|**Exemple de scénario**|**Protection des liens fiables DAV applicable dans ce cas ?**|
|:-----|:-----|
|Jean est un membre d’un groupe qui possède des stratégies de liens fiables DAV couvrant les URL dans le courrier électronique et des documents Office. Jean ouvre une présentation PowerPoint que quelqu'un envoyé, puis clique sur une URL de la présentation.  <br/> |Oui. Les stratégies de liens fiables DAV définis s’appliquent à de Jean groupe, de Jean courrier électronique et des documents Word, Excel, PowerPoint ou Visio Jean s’ouvre, dans la mesure où Jean est connectée et l’utilisation Office 365 ProPlus sur des appareils Android, iOS ou Windows.  <br/> |
|Dans l’organisation, non globale ou de sécurité de Chris les administrateurs ont défini des stratégies de liens fiables DAV encore. Chris reçoit un message électronique contenant une URL vers un site Web malveillant. Chris connaît l’URL est malveillant et clique sur le lien.  <br/> |non. La stratégie par défaut qui couvre les URL pour tout le monde dans l’organisation doit être définie dans l’ordre de protection à mettre en place.  <br/> |
|Dans organisation, non globale ou de sécurité Pat administrateurs défini ou modifié les stratégies de liens fiables DAV encore. Pat s’ouvre un document Word et clique sur une URL dans le fichier.  <br/> |Stratégie de No. A qui inclut les documents Office doit être défini dans l’ordre de protection à mettre en place. Voir [définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md).<br/> |
|Organisation de Lee dispose d’une stratégie de liens fiables DAV ayant `http://tailspintoys.com` répertorié en tant qu’un site Web bloqué. Lee reçoit un message électronique qui contient une URL vers `http://tailspintoys.com/aboutus/trythispage`. Lee clique sur l’URL.<br/> |Cela dépend si l’intégralité du site et tous ses sous-pages sont inclus dans la liste des bloqué URL. Voir [configurer une liste d’URL bloquée personnalisée à l’aide de liens fiables DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md).<br/> |
|Importation des collègues de Jean, Marie envoie un courrier électronique à Jean, ne pas savoir que le courrier électronique contienne une URL malveillante.  <br/> |Cela dépend si les stratégies de liens fiables DAV sont définies pour le courrier électronique envoyé au sein de l’organisation. Voir [définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md).<br/> |


  

