---
title: Créer des rapports de découverte d’application à l’aide de la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Créer des rapports avec la sécurité des applications Cloud Office 365 qui vous permettent de comprendre comment les personnes de votre organisation utilisent Office 365 et d'autres applications.
ms.openlocfilehash: e0d515ddd9b08aa4a70276177060f273cc89949e
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087293"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a>Créer des rapports de découverte d’application à l’aide de la sécurité des applications cloud Office 365

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |[Démarrer le déploiement](turn-on-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étapes suivantes](#next-steps) <br/> |
   
Office 365 Cloud App Security aide les administrateurs généraux, les administrateurs de sécurité et les lecteurs de sécurité à obtenir des informations sur les services Cloud que les utilisateurs d'une organisation utilisent. Par exemple, vous pouvez voir où les utilisateurs stockent et collaborent sur des documents et la proportion de données téléchargées vers des applications ou des services qui se trouvent en dehors d'Office 365.
  
Pour générer un rapport de découverte d'application, vous devez charger manuellement vos fichiers journaux de trafic Web à partir de vos pare-feu et de vos proxys, puis Office 365 Cloud App Security analyse et analyse ces fichiers pour votre rapport.
  
> [!NOTE]
> Vous devez être un administrateur général, un administrateur de sécurité ou un lecteur de sécurité pour effectuer les tâches décrites dans cet article. Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="create-a-report-with-app-discovery"></a>Créer un rapport avec la découverte des applications

Pour créer un rapport de découverte d'application, identifiez la source de données du fournisseur pour les fichiers journaux que vous souhaitez analyser, sélectionnez les fichiers journaux, puis demandez le rapport.
  
> [!NOTE]
> Utilisez les fichiers journaux du trafic Web qui incluent des périodes de trafic maximale pour obtenir la meilleure représentation de l'utilisation dans votre organisation. 
  
1. Collectez vos [journaux de trafic Web et sources de données pour la sécurité des applications Cloud Office 365](web-traffic-logs-and-data-sources-for-ocas.md).
    
2. Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous. 
       
3. Sélectionnez **Discover** \> **créer un rapport**. <br>![Dans le portail Office 365 CAS, sélectionnez découvrir](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)<br>
  
4. Spécifiez un nom et une description pour votre rapport, puis sélectionnez la source de données pour vos journaux de trafic Web dans la liste **source de données** . <br>![Dans les autorités de certification O365 \> , choisissez découvrir créer un rapport](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)<br>Si une source de données que vous souhaitez utiliser n'est pas disponible, vous pouvez demander son ajout. Sélectionnez **autre** pour **source de données**, puis tapez le nom de la source de données que vous essayez de télécharger. Nous allons examiner le journal et vous indiquer si nous ajoutons la prise en charge de la source de données qui l'a générée. 
  
5. Naviguez jusqu'à l'emplacement des fichiers journaux que vous avez collectés et sélectionnez les fichiers. Les fichiers journaux doivent avoir été générés par la source de données que vous avez choisie pour le rapport.
    
6. Cliquez sur **créer** pour démarrer le processus de création de rapports. 
    
7. Pour afficher l'état du rapport, cliquez sur **gérer les rapports de capture instantanée**. Lorsqu'un État est prêt, l'option Afficher le **rapport** s'affiche. 
    
## <a name="next-steps"></a>Étapes suivantes

- [Passer en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- [Passer en revue les détections d'applications dans la sécurité des applications cloud Office 365](review-app-discovery-findings-in-ocas.md)
    
- Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    

