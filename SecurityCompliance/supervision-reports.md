---
title: Rapports de surveillance
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2a762db5-e1c9-4c09-aa8e-bef49ce97209
description: Utiliser des rapports de surveillance pour voir de messages électroniques qui doivent conformité et qui doit exécuter.
ms.openlocfilehash: e18d083c0aad8be945c628516e593462da8e3898
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527700"
---
# <a name="supervision-reports"></a>Rapports de surveillance

Définissent des stratégies de surveillance communications dans votre organisation doivent passer en revue les pour la conformité et qui effectue les révisions. Utilisez les rapports de surveillance pour afficher l’activité de révision au niveau de la stratégie et de réviseur. Pour chaque stratégie, vous pouvez également afficher les statistiques live sur l’état actuel de l’activité de révision. [En savoir plus sur les stratégies de surveillance](configure-supervision-policies.md) . 
  
> [!NOTE]
> À l’aide de stratégies de surveillance requiert un abonnement à Office 365 E5 pour votre organisation. Si vous n’avez qu’un plan et essayer de surveillance, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Vous pouvez utiliser les rapports de surveillance :
  
- Vérifiez que vos stratégies fonctionnent comme prévu. 
    
- Découvrez combien de messages est identifiés pour révision.
    
- Découvrez combien de messages ne sont pas conformes et ceux qui est en passant révision. Ces informations peuvent vous aider à décider s’il faut affiner vos stratégies ou modifier le nombre de relecteurs.
    
## <a name="view-the-supervision-report"></a>Afficher le rapport de surveillance

1. Se connecter à la [sécurité &amp; centre de conformité](https://protection.office.com/) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation Office 365 qui dispose d’autorisations pour afficher les rapports de surveillance... 
    
2. Accédez aux **rapports** \> **tableau de bord**. Vous verrez un widget de création de rapports de surveillance et d’autres rapports que vous avez accès à.
    
3. Cliquez sur le widget de **surveillance** pour ouvrir la page rapport détaillé. 
    
> [!NOTE]
> Si vous n’êtes pas en mesure d’accéder à la page **rapports** , vérifiez que vous êtes membre du groupe de rôles de supervision, comme indiqué dans [rendre disponibles dans votre organisation de surveillance](configure-supervision-policies.md#SRavailable). Soient inclus dans cette permet de groupe de rôle pour créer et gérer le contrôle des stratégies et exécutez le rapport. 
  
## <a name="how-to-use-the-report"></a>Comment utiliser le rapport

Lorsqu’une stratégie de surveillance identifie un message électronique pour révision, le courrier électronique est remis au dossier de surveillance du réviseur dans Outlook et Outlook web app. Ce rapport répertorie le nom de chaque stratégie et le nombre de communications à chaque étape du processus de révision.
  
Utilisez l’état :
  
- Afficher les données pour toutes les stratégies spécifiques ou.
    
- Afficher les données regroupement par type de balise (par exemple, conforme, Questionable, etc.), réviseur ou type de message.
    
- Exporter des données vers un fichier CSV.
    
- Filtrer les données en fonction de la date d’activité la révision, type de balise, réviseur, type de message.
    
Voici une répartition des valeurs que vous pouvez voir dans la colonne **type de balise** . 
  
|**Type de balise**|**Cela signifie**|
|:-----|:-----|
|Pas de révision  <br/> |Le nombre de messages électroniques qui n’ont pas encore été révisées. Ces e-mails sont en attente de révision dans le dossier de contrôle du réviseur dans Outlook.  <br/> |
|Compatible  <br/> |Le nombre de messages électroniques révisé et marqué comme conforme. Aucune action supplémentaire n’est nécessaire.  <br/> |
|Suspects  <br/> |Le nombre de messages électroniques révisé et marqués suspect. Sous la forme d’un indicateur ; autres réviseurs peuvent aider à vérifier si un message électronique doit être une enquête de la conformité.  <br/> |
|Non compatibles (actif)  <br/> |Le nombre d’e-mails non conformes qui étudie relecteurs.  <br/> |
|Non compatibles (résolu)  <br/> |Le nombre de messages électroniques non conformes qui relecteurs étudier et de résoudre.  <br/> |
   
## <a name="more-details"></a>Plus de détails

- Stratégies de surveillance doivent tout d’abord être mis en service avant qu’ils n’apparaissent pas dans ce rapport.
    
- Si les stratégies sont supprimés, les données d’historique sont toujours affichées. Cependant, ils sont indiqués comme une stratégie « inexistant » et la fonction **Exporter** n’est pas disponible. 
    
- Si le rapport n’affiche toutes les données par défaut, il peut être car la plage de dates actuel n’a aucune donnée à afficher. Dans ces cas-là, utilisez le contrôle de **filtres** pour modifier la plage de dates. 
    

