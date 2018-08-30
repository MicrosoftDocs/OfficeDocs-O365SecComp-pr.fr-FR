---
title: Affichage des rapports de protection contre la perte de données
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 41eb4324-c513-4fa5-91c8-8fbd8aaba83b
description: Les rapports DLP dans Office 365, vous pouvez rapidement afficher le nombre de correspondances de stratégies DLP, substitutions ou faux positifs ; voir si elles sont tendances monter ou Descendre dans le temps ; filtrer le rapport de différentes façons ; et afficher des détails supplémentaires en sélectionnant un point sur une ligne dans le graphique.
ms.openlocfilehash: 379e66fc3f2611cf338739d030c2b1d48e7416d8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013908"
---
# <a name="view-the-reports-for-data-loss-prevention"></a>Affichage des rapports de protection contre la perte de données

Après avoir créé des stratégies de protection contre la perte de données, vous souhaiterez vérifier qu’elles fonctionnent que vous destiné et en vous aidant à la conformité. Les rapports de sécurité Office 365 avec la DLP &amp; centre de conformité, vous pouvez rapidement afficher :
  
- **Correspondances de stratégies DLP** Ce rapport affiche le nombre de correspondances de stratégies DLP au fil du temps. Vous pouvez filtrer le rapport par date, l’emplacement, stratégie ou action. Vous pouvez utiliser ce rapport pour : 
    
  - Paramétrer ou d’affiner vos stratégies DLP comme les exécuter en mode test. Vous pouvez afficher la règle spécifique qui correspondent à du contenu.
    
  - Vous concentrer sur des périodes de temps spécifiques et comprendre les raisons des pics et des tendances.
    
  - Découvrez les processus métiers enfreignant les stratégies DLP de votre organisation.
    
  - Comprendre n’importe quel impact sur l’activité de stratégies DLP en consultant la rubrique les actions sont appliquées au contenu.
    
  - Vérifier la conformité avec une stratégie DLP spécifique en affichant les correspondances pour cette stratégie.
    
  - Afficher la liste des utilisateurs les plus fréquents, recommencez les utilisateurs qui travaillent aux incidents dans votre organisation.
    
  - Afficher une liste des principaux types d’informations sensibles dans votre organisation.
    
- **Incidents DLP** Ce rapport indique également les correspondances de stratégies au fil du temps, comme la stratégie correspond à l’état. Toutefois, la stratégie établit une correspondance avec rapport montre correspond au niveau de la règle ; par exemple, si un message électronique mis en correspondance les trois règles différentes, la stratégie établit une correspondance avec rapport affiche trois différents éléments de ligne. En revanche, le rapport d’incidents montre correspond au niveau élément ; par exemple, si un message électronique mis en correspondance les trois règles différentes, le rapport d’incidents montre un élément de ligne de ce type de contenu. 
    
  Étant donné que le nombre de rapport est regroupée différemment, le rapport de correspondances de stratégie est préférable d’identification des correspondances avec des règles spécifiques et réglage de stratégies DLP. Le rapport d’incidents est préférable de l’identification des éléments de contenu spécifiques qui sont problématiques pour vos stratégies DLP.
    
- **Les substitutions et DLP faux positifs** Si votre stratégie DLP permet aux utilisateurs de remplacer ou signaler un faux positif, ce rapport affiche le nombre de ces instances au fil du temps. Vous pouvez filtrer le rapport par date, emplacement ou la stratégie. Vous pouvez utiliser ce rapport pour : 
    
  - Paramétrer ou d’affiner vos stratégies DLP en consultant la rubrique les stratégies provoquer un nombre élevé de faux positifs.
    
  - Afficher les justificatifs présentés par les utilisateurs lorsqu’ils résolvent un Conseil de stratégie en remplacement de la stratégie.
    
  - Découvrir où se substitue à conflit de stratégies DLP à des processus métiers valide par entraîner un nombre élevé de l’utilisateur.
    
Tous les rapports DLP peuvent afficher les données de la période de quatre mois plus récente. Les données les plus récentes peuvent prendre jusqu'à 24 heures pour apparaître dans les rapports.
  
Vous trouverez ces rapports à la sécurité &amp; centre de conformité \> **rapports** \> **tableau de bord**.
  
![Rapport des correspondances de stratégies DLP](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a>Affichez la justification envoyée par un utilisateur pour une substitution

Si votre stratégie DLP permet aux utilisateurs de remplacer, vous pouvez utiliser le faux positif et remplacer le rapport à afficher le texte envoyé par des utilisateurs dans le Conseil de stratégie.
  
![Champ justification dans les détails de l’état de substitution et un faux positif DLP](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a>Effectuer une action sur les conseils et recommandations

États peuvent afficher des conseils et recommandations où vous pouvez cliquer sur l’icône d’avertissement rouge pour afficher des informations sur les problèmes potentiels et mesures correctives possibles.
  
![En cliquant sur une icône de détails pour afficher les détails et les actions à entreprendre](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a>Recherchez les applets de commande pour les rapports DLP

Pour utiliser la plupart des applets de commande pour la sécurité &amp; centre de conformité, vous devez :
  
1. [Se connecter à l’Office 365 Security &amp; centre de conformité à l’aide de PowerShell à distance](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Utilisez une de ces [Office 365 sécurité &amp; centre de conformité des applets de commande](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
Toutefois, les rapports DLP doivent extraire des données dans Office 365, notamment Exchange Online. Pour cette raison, les applets de commande pour les rapports DLP sont disponibles dans Exchange Online Powershell — pas de sécurité &amp; Powershell du centre de conformité. Par conséquent, pour utiliser les applets de commande pour les rapports DLP, vous devez :
  
1. [Connect to Exchange Online using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Utilisez une de ces applets de commande pour les rapports DLP :
    
      - [Get-DlpDetectionsReport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [Get-DlpDetailReport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

