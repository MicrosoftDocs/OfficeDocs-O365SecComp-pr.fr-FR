---
title: Créer des rapports de découverte d’application à l’aide de la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Créer des rapports avec Office 365 Cloud App de sécurité qui vous permettent de comprendre comment les personnes dans votre organisation utilisent Office 365 et autres applications.
ms.openlocfilehash: 6842912f42072e21608955bde5250f0774c7bba4
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014866"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a>Créer des rapports de découverte d’application à l’aide de la sécurité des applications cloud Office 365

Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étapes suivantes](#next-steps) <br/> |
   
Sécurité d’application Office 365 nuage permet les administrateurs globaux, les administrateurs de sécurité et les lecteurs de sécurité Familiarisez-vous avec les services en nuage à l’aide de personnes dans une organisation. Par exemple, vous pouvez voir où les utilisateurs sont le stockage et collaborer sur des documents et la quantité de données est en cours de téléchargement pour les applications ou services qui sont en dehors d’Office 365.
  
Pour générer un rapport de détection d’application, vous téléchargez manuellement vos fichiers de journaux de trafic web à partir de votre pare-feu et des proxys et Office 365 Cloud Application Security analyse et analyse les fichiers pour votre rapport.
  
> [!NOTE]
> Vous devez être un administrateur global, un administrateur de sécurité ou un lecteur de sécurité pour effectuer les tâches décrites dans cet article. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="create-a-report-with-app-discovery"></a>Créer un rapport avec la détection d’application

Pour créer un rapport de détection d’application, vous identifiez la source de données de fournisseur pour les fichiers journaux que vous souhaitez avoir analysé, sélectionnez les fichiers journaux et puis demande le rapport.
  
> [!NOTE]
> Utilisez les fichiers journaux de trafic web qui incluent des périodes de trafic de pointe pour obtenir la meilleure représentation d’utilisation dans votre organisation. 
  
1. Collecter les [journaux de trafic web et des sources de données Office 365 nuage sécurité des applications](web-traffic-logs-and-data-sources-for-ocas.md).
    
2. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école. 
    
3. Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.
    
4. Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.
    
5. Choisissez **découvrir** \> **Création de rapports**.
    
    ![Dans le portail Office 365 autorités de certification, cliquez sur découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
6. Spécifiez un nom et une description pour votre rapport, puis sélectionnez la source de données pour les journaux de trafic web dans la liste **source de données** . 
    
    ![Dans les autorités de certification O365, choisissez découvrir \> créer le nouveau rapport](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)
  
    > [!NOTE]
    > Si une source de données que vous souhaitez utiliser n’est pas répertoriée, vous pouvez demander que, il doit être ajouté. Sélectionnez **autre** pour la **source de données**, puis tapez le nom de la source de données que vous essayez de télécharger. Nous allons consulter le journal et vous permettent de savoir si nous ajouter la prise en charge pour la source de données qui l’a généré. 
  
7. Accédez à l’emplacement des fichiers journaux que vous avez collecté et sélectionnez les fichiers. Les fichiers journaux doivent avoir été générées par la source de données que vous avez choisi pour le rapport.
    
8. Cliquez sur **créer** pour démarrer le processus de création de rapport. 
    
9. Pour afficher le statut du rapport, cliquez sur **Gérer les rapports de capture instantanée**. Lorsqu’un état est prêt, vous verrez l’option **Afficher l’état** . 
    
## <a name="next-steps"></a>Étapes suivantes

- [Passez en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365](review-app-discovery-findings-in-ocas.md)
    
- Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)
    

