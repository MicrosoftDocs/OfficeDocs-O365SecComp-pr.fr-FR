---
title: Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Examen des rapports de découverte d'application dans Office 365 Cloud App Security peut vous aider à en savoir plus sur la façon dont les employés de votre organisation utilisent des applications Cloud. Une fois que vous avez créé des rapports de découverte d'application à l'aide de fichiers journaux de vos pare-feu et de vos proxys, examinez les résultats dans le tableau de bord de découverte d'application.
ms.openlocfilehash: f50ad372450b2a1404829eeb6f6964c1d954dccd
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264962"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a>Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365
  
|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |[Démarrer le déploiement](turn-on-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étapes suivantes](#next-steps) <br/> |
   
Le tableau de bord de découverte du Cloud fonctionne avec les journaux de trafic Web de votre organisation pour fournir des informations détaillées sur l'utilisation des applications Cloud. Si vous êtes un administrateur général, un administrateur de sécurité ou un lecteur de sécurité, et que votre organisation a [créé des rapports de découverte d'application dans Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), vous pouvez utiliser le tableau de bord de découverte de Cloud pour obtenir des informations sur la façon dont les personnes de votre Organisation utilisent Office 365 et d'autres applications Cloud. (Le tableau de bord de découverte du Cloud est également appelé découverte d'application de productivité.)
  
 Le tableau de bord de découverte du Cloud vous permet d'afficher des informations détaillées sur la façon dont les membres de votre organisation utilisent Office 365 et d'autres applications. 
  
![Le tableau de bord de découverte du Cloud a été mis à jour](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a>Accéder au tableau de bord de découverte Cloud

1. Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous.
    
2. Accédez à **** \> la vue d' **exploration du tableau de bord de découverte Cloud**.
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a>Afficher les principaux utilisateurs, adresses IP, applications et niveaux de risque

Le tableau de bord de découverte du Cloud vous donne une vue d'ensemble des applications utilisées avec Office 365 dans votre organisation, des alertes ouvertes, des utilisateurs les plus fréquents et des niveaux de risque.
  
![Recherche dans le Cloud dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. Dans l'onglet **tableau de bord** , examinez l'ensemble de l'application Cloud dans votre organisation dans la section vue d'ensemble en haut de l'écran. 
    
2. Voir les **catégories Office 365** pour les applications utilisées dans votre organisation. 
    
3. Consultez le widget **applications découvertes** pour consulter l'utilisation d'Office 365 et d'autres applications dans cet affichage. 
    
4. Examinez les **principaux utilisateurs** et les **principaux adresses IP** pour identifier les personnes qui utilisent Office 365 et les applications Cloud les plus utilisées dans votre organisation. 
    
5. Voir où les applications que les personnes utilisent sont par emplacement géographique à l'aide de la carte d' **emplacement de siège** de l'application. 
    
6. Au-dessus de la zone cartes, jetez un œil à la note de risque des applications découvertes dans la section vue d'ensemble des **niveaux de risque** . Vous pouvez examiner les risques en utilisant les mêmes groupes et catégories que ceux que vous avez utilisés dans la zone **applications découvertes** . Par exemple, vous pouvez voir la proportion de trafic dans chaque regroupement provenant d'applications à risque élevé, moyen ou faible. 
    
## <a name="dive-deeper-into-the-information"></a>Approfondir les informations

Vous pouvez utiliser la découverte du Cloud pour avoir un aperçu approfondi des applications, des sous-domaines, des adresses IP et des utilisateurs.
  
1. Dans le tableau de bord de découverte du Cloud, sélectionnez l'onglet **applications découvertes** . 
    
2. Utilisez la section filtres pour afficher les applications par nom, catégorie, niveau d'utilisation ou date de dernière vue.
    
3. Dans la liste des résultats, placez le curseur sur le nom d'une application pour afficher le lien **afficher les sous-domaines** .<br/> ![Passer en regard d'une application pour révéler un lien permettant d'afficher les détails d'un sous-domaine](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)<br/>Des informations détaillées sur l'application sélectionnée s'affichent.
    
4. Pour afficher les détails des adresses IP, cliquez sur l'onglet **adresses IP** .<br/>![La découverte du Cloud affiche des informations détaillées sur les adresses IP](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)<br/>Dans la liste des résultats, sélectionnez une adresse IP individuelle pour afficher des informations plus détaillées.
    
5. Pour afficher des détails sur les utilisateurs d'Office 365 au sein de votre organisation, cliquez sur l'onglet **utilisateurs** .<br/>![Découverte du Cloud: informations sur les utilisateurs](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a>Exclure des entités

Vous pouvez exclure certains utilisateurs ou adresses IP de votre système afin de vous concentrer sur des informations plus spécifiques.
  
1. Choisissez **paramètres** \> de **découverte du Cloud**.
    
2. Choisissez **exclure des entités**.
    
3. Choisissez **utilisateurs exclus** ou **adresses IP exclues**.
    
4. Spécifiez les utilisateurs ou les adresses IP, puis dans la zone **Commentaires** , tapez des informations expliquant pourquoi vous excluez ces utilisateurs ou adresses IP. 
    
5. Sélectionnez **Ajouter**.
    
## <a name="next-steps"></a>Étapes suivantes

- [Passer en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [Créer des rapports de découverte d'application](create-app-discovery-reports-in-ocas.md)
    
- Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    

