---
title: Office 365 DAV Safe liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: overview
f1_keywords:
- "197503"
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
- ZVO160
- ZXL160
- ZPP160
- ZWD160
ms.assetid: dd6a1fef-ec4a-4cf4-a25a-bb591c5811e3
description: La fonctionnalité de liens fiables offre-heure des clics de vérification des liens hypertexte dans les documents Office et dans les messages électroniques. Utilisez les liens sécurisés pour protéger votre organisation contre les attaques par hameçonnage et les autres attaques.
ms.openlocfilehash: 24960aa20d2870c7aea37a4b76f1792de21f6b5b
ms.sourcegitcommit: a8884b9675559018e1fddec1c0cc2de0bc3bdde5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "23839944"
---
# <a name="office-365-atp-safe-links"></a>Office 365 DAV Safe liens

Office 365 DAV fiables liens (liens fiables DAV) (ainsi que les [Pièces jointes sûres Office 365 DAV](atp-safe-attachments.md)) est un ensemble de fonctionnalités de sécurité offertes dans le cadre [d’Office 365 avancée protection contre les menaces](office-365-atp.md) pour les entreprises. Liens approuvés DAV permet de protéger votre organisation en fournissant-heure des clics de vérification des adresses web (URL) dans les messages électroniques et des documents Office. Protection est définie par le biais de [liens fiables DAV stratégies](set-up-atp-safe-links-policies.md) définies par votre équipe de sécurité d’Office 365. 
  
Une fois vos stratégies de liens fiables DAV sont mis en place, les administrateurs globaux Office 365, les administrateurs de sécurité et les lecteurs de sécurité peuvent [Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md). Les informations contenues dans ces rapports peuvent aider votre équipe de sécurité à prendre des mesures supplémentaires pour protéger votre organisation ou de rechercher des incidents de sécurité.
  
Nouvelles fonctionnalités sont régulièrement ajoutées aux liens fiables DAV :
  
- Au début de la liaison tardive 2017 octobre, protection liens fiables DAV est étendue pour appliquer aux URL dans un e-mail ainsi que les URL dans les documents Office 365 ProPlus, telles que Word, Excel, PowerPoint et Visio sur Windows, ainsi que Office applications sur les périphériques iOS ou Android.
    
- Au début de mars 2018, protection liens fiables DAV est étendue s’appliquent aux messages envoyés entre les personnes dans une organisation.
    
- À partir du deuxième semestre 2018, protection liens fiables DAV est étendue pour appliquer aux URL dans Office Online (Word en ligne, Online Excel, PowerPoint en ligne et OneNote en ligne) et Office 365 ProPlus sur Mac.
    
- Début de septembre 2018, [pages d’avertissement Office 365 DAV](atp-safe-links-warning-pages.md) fonctionnalité un jeu de couleurs, plus de détails et la possibilité de passer à un site en dépit de donné avertissements et des recommandations. 
         
## <a name="how-atp-safe-links-in-email-works"></a>Fonctionnement des liens fiables DAV dans le message électronique

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
    
## <a name="how-atp-safe-links-in-office-documents-works"></a>Fonctionnement des liens fiables DAV dans des documents Office

À un niveau élevé, voici le fonctionne de protection DAV des liens sécurisés pour les URL dans les applications Office 365 ProPlus (versions actuelles de OneNote, Word, Excel et PowerPoint sur Windows ou Mac, les applications Office sur iOS ou Android appareils, Visio sur Windows et Office Online) :
  
1. Personnes ont installé Office 365 ProPlus sur leur ordinateur, smartphone ou tablette.
    
2. Un utilisateur ouvre une Word, Excel, PowerPoint ou Visio et se connecte à Office 365 pour entreprises à l’aide de leur compte professionnel ou de l’école. Le document contient des URL.
    
3. Lorsque l’utilisateur clique sur une URL dans le document, le lien est vérifié par le service de liens fiables DAV.
    
  - Si l’URL est un site Web qui est inclus dans une [liste d’URL « Pas de rewrite » personnalisée](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) pour une stratégie qui s’applique à l’utilisateur, que l’utilisateur est nécessaire pour le site Web. 
    
  - Si l’URL est sur un site Web qui est inclus dans [personnalisé liste URL bloquée l’organisation](set-up-a-custom-blocked-urls-list-wtih-atp.md), l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).
    
  - Si l’URL est sur un site Web qui a été déterminé malveillante, l’utilisateur est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md).
    
  - Si l’URL accède à un fichier à télécharger et les [stratégies de liens fiables DAV](set-up-atp-safe-links-policies.md) sont configurés pour l’analyse des téléchargements, le fichier téléchargeable est vérifié. 
    
  - Si l’URL est fiable, l’utilisateur est dirigé vers le site Web.
    
## <a name="how-to-get-atp-safe-links-protection"></a>Comment obtenir la protection des liens fiables DAV

Fonctionnalités des liens fiables DAV font partie de la [Protection contre les menaces avancées](office-365-atp.md), inclus dans Office 365 entreprise E5. Si votre organisation utilise un autre abonnement Office 365 pour entreprises, contre les menaces avancées peut être acheté comme module complémentaire. Pour plus d’informations, voir [Office 365 Platform Service Description : Office 365 sécurité &amp; centre de conformité](https://technet.microsoft.com/en-us/library/dn933793.aspx) et [acheter ou modifier un module complémentaire pour Office 365 pour entreprises](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).
  
Les fonctionnalités des liens fiables DAV sont actifs quand :
  
- **Liens approuvés DAV stratégies sont configurés** pour le courrier électronique et pour les documents Word, Excel, PowerPoint et Visio. (Voir [définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)).

- **Les applications client office 365 sont configurées pour utiliser l’authentification moderne** avec Azure Active Directory d’authentification de la bibliothèque. Pour plus d’informations, consultez [Authentification moderne pour 2016 Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016). 
    
- **Les utilisateurs ont connecté à Office 365** à l’aide de leur compte professionnel ou de l’école. (Voir [se connecter à Office ou Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)).
    
- **Que courrier électronique de l’organisation est hébergée dans Office 365**, pas dans un serveur local. 
    
## <a name="make-sure-atp-safe-links-protection-is-in-place"></a>Assurez-vous que la protection des liens fiables DAV est en place

Un excellent moyen de voir le fonctionne de protection des liens fiables DAV pour votre organisation est en [affichage des rapports de protection contre les menaces avancées](view-reports-for-atp.md). En outre, un administrateur global ou de sécurité, veillez à consulter vos [stratégies de liens fiables DAV](set-up-atp-safe-links-policies.md). Stratégies de liens fiables DAV pour déterminer si protection applicable des liens hypertexte dans les messages électroniques, ou à l’URL dans des documents Office.
  
Le tableau suivant décrit quelques exemples de scénarios où protection liens fiables DAV peut ou ne peut pas en place. Dans tous les cas, nous supposons que l’organisation a Office 365 entreprise E5.
  
|**Exemple de scénario**|**Protection des liens fiables DAV applicable dans ce cas ?**|
|:-----|:-----|
|Jean est un membre d’un groupe qui possède des stratégies de liens fiables DAV couvrant les URL dans le courrier électronique et des documents Office. Jean ouvre une présentation que quelqu'un envoyés dans PowerPoint 2016, puis clique sur une URL de la présentation.  <br/> |Oui. Les stratégies de liens fiables DAV définis s’appliquent à de Jean groupe, de Jean courrier électronique et des documents Word, Excel, PowerPoint ou Visio Jean s’ouvre, dans la mesure où Jean est connectée et l’utilisation Office 365 ProPlus sur des appareils Android, iOS ou Windows.  <br/> |
|Dans l’organisation, non globale ou de sécurité de Chris les administrateurs ont défini des stratégies de liens fiables DAV encore. Chris reçoit un message électronique contenant une URL vers un site Web malveillant. Chris connaît l’URL est malveillant et clique sur le lien.  <br/> |Non. La stratégie par défaut qui couvre les URL pour tout le monde dans l’organisation doit être définie dans l’ordre de protection à mettre en place.  <br/> |
|Dans organisation, non globale ou de sécurité Pat administrateurs défini ou modifié les stratégies de liens fiables DAV encore. Pat s’ouvre un document Word et clique sur une URL dans le fichier.  <br/> |Stratégie de No. A qui inclut les documents Office doit être défini dans l’ordre de protection à mettre en place. Voir [définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md).<br/> |
|Organisation de Lee dispose d’une stratégie de liens fiables DAV ayant `http://tailspintoys.com` répertorié en tant qu’un site Web bloqué. Lee reçoit un message électronique qui contient une URL vers `http://tailspintoys.com/aboutus/trythispage`. Lee clique sur l’URL.<br/> |Cela dépend si l’intégralité du site et tous ses sous-pages sont inclus dans la liste des bloqué URL. Voir [configurer une liste d’URL bloquée personnalisée à l’aide de liens fiables DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md).<br/> |
|Importation des collègues de Jean, Marie envoie un courrier électronique à Jean, ne pas savoir que le courrier électronique contienne une URL malveillante.  <br/> |Cela dépend si les stratégies de liens fiables DAV sont définies pour le courrier électronique envoyé au sein de l’organisation. Voir [définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md).<br/> |
   
## <a name="related-topics"></a>Voir aussi

[Protection de Microsoft Office 365 menace avancées](office-365-atp.md)
  
[Définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)
  
[Pièces jointes DAV Safe dans Office 365](atp-safe-attachments.md)
  
[Fonctionnalités anti-hameçonnage de DAV dans Office 365](atp-anti-phishing.md)
  
[Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md)
  

