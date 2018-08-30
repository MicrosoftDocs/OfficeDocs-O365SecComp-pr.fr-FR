---
title: Passez en revue les conclusions de découverte d’application dans Office 365 Cloud application sécurité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Consultation des rapports de détection d’application dans la gestion de la sécurité avancée peut vous aider à en savoir plus sur l’utilisation des applications dans le nuage par les personnes dans votre organisation. Une fois que vous avez créé des rapports de découverte d’application à l’aide de fichiers journaux à partir de votre pare-feu et des proxys, passez en revue les résultats du tableau de bord de détection d’application.
ms.openlocfilehash: 188ef87920b26069e7d99057662b3812be22e46c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527508"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a>Passez en revue les conclusions de découverte d’application dans Office 365 Cloud application sécurité
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étapes suivantes](#next-steps) <br/> |
   
Le tableau de bord dans le nuage découverte fonctionne avec les journaux de trafic web de votre organisation pour fournir des informations détaillées sur l’utilisation des applications dans le nuage. Si vous êtes un administrateur global, un administrateur de sécurité ou un lecteur de sécurité et que votre organisation a [créé des rapports de découverte d’application dans Office 365 Cloud application sécurité](create-app-discovery-reports-in-ocas.md), vous pouvez utiliser le tableau de bord de découverte dans le nuage pour bien comprendre comment les personnes figurant dans votre organisation utilisent Office 365 et autres applications dans le nuage. (Le tableau de bord de découverte dans le nuage est également appelé détection d’application de la productivité).
  
 **À compter de mars 2018, le tableau de bord de découverte dans le nuage offre de nouvelles fonctionnalités** qui vous permet d’afficher des informations détaillées sur comment personnes dans votre organisation sont l’utilisation d’Office 365 et autres applications. 
  
![Le tableau de bord dans le nuage découverte a été mis à jour.](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a>Accédez au tableau de bord de découverte dans le nuage

1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.) 
    
2. Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.
    
    (Si Office 365 Cloud application sécurité n’est pas encore activée, et vous êtes un administrateur global, [Activer la sécurité d’application Office 365 dans le nuage](turn-on-office-365-cas.md).)
    
3. Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.
    
4. Accédez à **découvrir** \> **tableau de bord de découverte dans le nuage**.
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a>Voir vos utilisateurs les plus fréquents, IP les adresses, applications et des niveaux de risques

Le tableau de bord de découverte dans le Cloud vous donne une vue d’ensemble d’un coup de œil des applications qui sont utilisés avec Office 365 dans votre organisation, les alertes actives, utilisateurs les plus fréquents et des niveaux de risques.
  
![Dashboaard de découverte dans le nuage](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. Sous l’onglet **tableau de bord** , examinez l’utilisation d’application cloud globale de votre organisation dans la section vue d’ensemble dans la partie supérieure de l’écran. 
    
2. Afficher les **catégories d’Office 365** pour les applications qui sont utilisés dans votre organisation. 
    
3. Examinez le widget **découvert applications** pour voir l’utilisation d’Office 365 et d’autres applications dans cet affichage. 
    
4. Examinez le widget **d’utilisateurs les plus fréquents** et **adresses IP haut** pour identifier les personnes qui utilisent Office 365 et applications le plus dans votre organisation en nuage. 
    
5. Voir où les applications à l’aide de personnes en emplacement géographique à l’aide de la carte **d’emplacements de sièges sociaux d’applications** . 
    
6. Au-dessus de la zone cartes, jetez un œil à note des applications découvertes dans la vue d’ensemble **des niveaux de risques** . Vous pouvez examiner les risques des groupes et des catégories que vous avez utilisée dans la zone **applications découvert** . Par exemple, vous pouvez voir la quantité de trafic dans chaque regroupement est à partir d’applications risque élevé, moyen ou faible. 
    
## <a name="dive-deeper-into-the-information"></a>Les informations aller plus loin

Vous pouvez utiliser dans le nuage découverte pour jetez un œil plus approfondi à des applications, les sous-domaines, les adresses IP et les utilisateurs.
  
1. Dans le tableau de bord de découverte dans le nuage, choisissez l’onglet **applications découvert** . 
    
2. Utilisez la section filtres pour afficher les applications par nom, catégorie, au niveau de l’utilisation ou dernière date affichée.
    
3. Dans la liste des résultats, placez le curseur par un nom d’application pour faire apparaître le lien **Afficher les sous-domaines** . 
    
    ![En regard d’une application pour afficher un lien pour afficher les détails du sous-domaine de pointage](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)
  
    Des informations détaillées sur l’application sélectionnée seront affiche.
    
4. Pour afficher plus d’informations sur les adresses IP, sélectionnez l’onglet **adresses IP** . 
    
    ![Découverte de nuage affiche des informations détaillées sur les adresses IP](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)
  
    Dans la liste des résultats, sélectionnez une adresse IP pour afficher des informations plus détaillées.
    
5. Pour afficher plus d’informations sur les utilisateurs d’Office 365 au sein de votre organisation, sélectionnez l’onglet **utilisateurs** . 
    
    ![Découverte de nuage - informations sur les utilisateurs](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a>Exclure les entités

Vous pouvez exclure certains utilisateurs du système ou les adresses IP afin de se concentrer sur des informations plus spécifiques.
  
1. Choisir les **paramètres** \> **paramètres de découverte dans le nuage**.
    
2. Choisissez **exclure des entités**.
    
3. Choisissez **exclu des utilisateurs** ou **des adresses IP exclus**.
    
4. Spécifier les utilisateurs ou les adresses IP et dans la zone **commentaires** , tapez les informations sur pourquoi de l’exclusion de ces utilisateurs ou des adresses IP. 
    
5. Sélectionnez **Ajouter**.
    
## <a name="next-steps"></a>Étapes suivantes

- [Passez en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [Créer des rapports de détection d’application](create-app-discovery-reports-in-ocas.md)
    
- Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)
    

