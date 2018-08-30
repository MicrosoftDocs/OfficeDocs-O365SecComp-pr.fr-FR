---
title: Prendre en main la stratégie DLP par défaut
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/10/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
description: Avant de créer même votre stratégie de protection contre la perte données premier, DLP contribue à protéger vos informations sensibles avec une stratégie par défaut. Cette stratégie par défaut et ses aident à protéger votre contenu sensible par pour vous avertir lorsque le numéro de carte de messagerie ou des documents contenant un crédit ont été partagé avec une personne extérieure à votre organisation recommandation (voir ci-dessous).
ms.openlocfilehash: 1b522a2c04e72353970ef5dfcd62183023a01994
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528765"
---
# <a name="get-started-with-the-default-dlp-policy"></a>Prendre en main la stratégie DLP par défaut

Avant de créer même votre stratégie de protection contre la perte données premier, DLP contribue à protéger vos informations sensibles avec une stratégie par défaut. Cette stratégie par défaut et ses aident à protéger votre contenu sensible par pour vous avertir lorsque le numéro de carte de messagerie ou des documents contenant un crédit ont été partagé avec une personne extérieure à votre organisation recommandation (voir ci-dessous). Cette recommandation s’affiche sur la page **d’accueil** de la sécurité &amp; centre de conformité. 
  
Vous pouvez utiliser ce widget afficher rapidement quand et la quantité d’informations sensible a été partagée et puis affiner la stratégie DLP par défaut dans seulement un ou deux clics. Vous pouvez également modifier la stratégie DLP par défaut à tout moment, car elle est entièrement personnalisable. Notez que si vous ne voyez pas la recommandation en premier lieu, essayez de cliquer sur **+ plus** en bas de la section **recommandé pour vous** . 
  
![Widget nommé supplémentaires protéger le contenu partagé](media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a>Afficher le rapport et affiner la stratégie DLP par défaut

Lorsque le widget vous indique que les utilisateurs ont les informations sensibles partagées avec des personnes extérieures à votre organisation, choisissez **une stratégie DLP affiner** en bas. 
  
Le rapport détaillé vous indique quand et comment la quantité de contenu qui contient les numéros de carte de crédit a été partagée au cours des 30 derniers jours. Notez que les correspondances de règle peuvent prendre jusqu'à 48 heures s’affiche dans le widget.
  
Pour protéger les informations sensibles, la stratégie DLP par défaut :
  
- Détecte lorsque le contenu de Exchange, SharePoint et OneDrive qui contient au moins une carte de crédit est partagé avec des personnes extérieures à votre organisation.
    
- Affiche un Conseil de stratégie et envoie une notification par courrier électronique aux utilisateurs lorsqu’ils essaient de partager ces informations sensibles avec des personnes extérieures à votre organisation. Pour plus d’informations sur ces options, voir [Envoyer des notifications par courrier électronique et afficher les conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md).
    
- Génère des rapports d’activité détaillées afin que vous pouvez suivre des éléments comme ayant le contenu partagé avec des personnes extérieures à votre organisation et lorsque que. Vous pouvez utiliser les [rapports DLP](view-the-dlp-reports.md) et [des données du journal d’audit](search-the-audit-log-in-security-and-compliance.md) (où **activité** = **DLP**) pour afficher ces informations.
    
Pour affiner rapidement la stratégie DLP par défaut, vous pouvez choisir de façon à :
  
- Vous envoyer un message électronique de rapport d’incident lorsque les utilisateurs partagent ces informations sensibles avec des personnes extérieures à votre organisation.
    
- Ajouter d’autres utilisateurs pour le rapport d’incident e-mail.
    
- Bloquez l’accès au contenu contenant les informations sensibles, mais autoriser l’utilisateur à remplacer et partager ou envoyer s’ils doivent.
    
Pour plus d’informations sur les rapports d’incidents ou restriction de l’accès, voir [vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).
  
Si vous souhaitez modifier ces options ultérieurement, vous pouvez modifier la valeur par défaut la stratégie DLP à tout moment - voir la section suivante.
  
![Paramètres widget nommé supplémentaires de protection du contenu partagé](media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a>Modifier la stratégie DLP par défaut

Cette stratégie est nommée **stratégie par défaut Office 365 DLP** et s’affiche sous la **prévention des pertes de données** dans la page **stratégie** de la sécurité &amp; centre de conformité. 
  
Cette stratégie est entièrement personnalisable, identique à toute stratégie DLP que vous avez créés à partir de zéro. Vous pouvez également désactiver ou supprimer la stratégie, afin que vos utilisateurs ne peuvent plus recevoir des conseils de stratégie ou les notifications de messagerie.
  
![Stratégie DLP nommée stratégie par défaut Office 365 DLP](media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a>Lorsque le widget et n’apparaît pas

Le widget nommé **davantage protéger le contenu partagé** apparaît dans la section **recommandé pour vous** de la page **d’accueil** de la sécurité &amp; centre de conformité. 
  
Ce widget s’affiche uniquement lorsque :
  
- Il n’existe aucune stratégies de prévention de perte de données de la sécurité &amp; centre de conformité ou le centre d’administration Exchange. Ce widget est destiné à vous aider à prendre en main DLP, elle n’apparaît pas si vous disposez déjà de stratégies DLP.
    
- Contenu contenant au moins une carte de crédit a été partagé avec une personne extérieure à votre organisation au cours des 30 derniers jours.
    
Notez que les correspondances de règle peuvent prendre jusqu'à 48 heures soit disponible pour le widget, une fois que les informations sensibles partagées en externe sont détectées, elle peut prendre jusqu'à deux jours de la recommandation apparaisse.
  
Enfin, une fois que vous utilisez le widget pour affiner la stratégie DLP par défaut, le widget disparaît de la page **d’accueil** . 
  

