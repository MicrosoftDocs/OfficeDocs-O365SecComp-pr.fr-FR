---
title: Gérer les applications OAuth à l’aide de la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Applications OAuth dans Office 365 la sécurité des applications Cloud vous aide à gérer les applications que les utilisateurs téléchargent pour une utilisation avec les données Office 365
ms.openlocfilehash: 0d9916414d55abb73fd99eaf30c3b6df0648b191
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260136"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a>Gérer les applications OAuth à l’aide de la sécurité des applications cloud Office 365

|Évaluation * *\>**|Planification * *\>**|Déploiement * *\>**|Utilisation * * * *|
|:-----|:-----|:-----|:-----|
|[Commencer l'évaluation](office-365-cas-overview.md) <br/> |[Commencer la planification](get-ready-for-office-365-cas.md) <br/> |[Démarrer le déploiement](turn-on-office-365-cas.md) <br/> |Vous êtes là!  <br/> [Étapes suivantes](#next-steps)<br/> |
   
Les personnes aiment les applications et elles les téléchargent souvent, en particulier les applications que les personnes pensent gagner du temps en facilitant l'accès à leurs informations professionnelles ou scolaires. Toutefois, certaines applications peuvent potentiellement présenter un risque de sécurité pour votre organisation, en fonction de leurs informations d'accès et de leur gestion. Avec la [sécurité des applications Cloud d'Office 365](office-365-cas-overview.md), si vous êtes un administrateur global ou de sécurité, vous pouvez gérer les applications OAuth pour votre organisation. Vous pouvez voir les applications que les utilisateurs utilisent avec les données Office 365, les autorisations de ces applications, et bien plus encore. 
  
Cet article explique où accéder à la rubrique gérer les applications OAuth, comment approuver, bloquer ou signaler une application, et comment créer une requête d'application.
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a>Comment trouver la page gérer les applications OAuth

> [!NOTE]
> Les applications OAuth sont gérées dans le portail de sécurité des applications Cloud Office 365. Vous devez être un administrateur général ou un administrateur de sécurité pour effectuer la tâche suivante. Pour plus d'informations [, consultez la rubrique autorisations dans &amp; le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). 
  
1. Accédez au portail de sécurité des applications Cloud[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)() et connectez-vous.
  
2. Sélectionnez **examiner** \> les **applications OAuth**.<br/>![Dans le portail CAS d'O365, sélectionnez enquête.](media/OCAS-OAuthApps.png)<br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a>Ce que vous verrez dans la page gérer les applications OAuth

Le tableau suivant décrit les contrôles et les options disponibles dans la page gérer les applications OAuth.
  
|**Item**|**Description**|
|:-----|:-----|
|Icône de base dans la barre de requête de l'application  <br/> ![Icône indiquant le mode de requête de base pour les requêtes](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Sélectionnez cette option pour basculer vers l'affichage avancé.  <br/> (Si vous voyez de **base**, vous utilisez l'affichage avancé)  <br/> |
|Icône avancé dans la barre de requête de l'application  <br/> ![Icône indiquant l'affichage de requêtes avancées pour les requêtes](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Sélectionnez cette option pour basculer vers l'affichage de base.  <br/> (Si vous voyez **avancé**, vous utilisez l'affichage de base.)  <br/> |
|Icône ouvrir ou fermer toutes les détails dans la liste des applications  <br/> ![Cliquez sur cette icône pour ouvrir ou fermer tous les détails de toutes les applications.](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Sélectionnez cette icône pour afficher plus ou moins de détails sur chaque application.  <br/> |
|Icône exporter dans la liste des applications  <br/> ![Cliquez sur cette icône pour exporter un fichier CSV de toutes les applications](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Sélectionnez cette icône pour exporter un fichier CSV contenant une liste d'applications, le nombre d'utilisateurs pour chaque application, les autorisations associées à l'application, le niveau d'autorisation, l'état de l'application et le niveau d'utilisation de la communauté.  <br/> |
|Nom  <br/> |Utilisez cette pour afficher le nom d'une application. Sélectionnez le nom pour afficher plus d'informations, telles que sa description, son éditeur, son site Web d'application et son ID d'application.  <br/> |
|Autorisé par  <br/> |Utilisez cette méthode pour voir le nombre d'utilisateurs qui ont autorisé une application à accéder à leur compte Office 365. Sélectionnez le numéro pour afficher plus d'informations, telles que la liste des comptes d'utilisateur.  <br/> |
|Niveau d'autorisation  <br/> ![Icône indiquant le niveau permisiions pour une application](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Utilisez cette méthode pour voir le niveau d'accès d'une application aux données Office 365. Les niveaux d'autorisation indiquent **faible**, **moyen**ou **élevé**, où **faible** peut indiquer que l'application accède uniquement au profil et au nom d'un utilisateur. Sélectionnez le niveau pour afficher plus d'informations, telles que les autorisations accordées à l'application, l'utilisation de la communauté et l'activité connexe dans le [Journal de gouvernance](suspend-or-restore-an-account-in-ocas.md).  <br/> |
|Dernière autorisation <br/> |Utilisez cette pour afficher la date et l'heure auxquelles une application OAuth a été autorisée pour la dernière fois pour accéder aux données Office 365 de votre organisation. <br/>  |
|Actions<br/>![Applications OAuth](media/OCAS-OAuthAppApproveBanReport.png)<br/> |Utilisez cette option pour afficher ou marquer une application comme approuvée ou interdite, signaler une application OAuth à Microsoft ou la laisser comme non déterminée.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Marquer une application comme approuvée

Dans la page **gérer les applications OAuth** , recherchez l'application que vous souhaitez approuver, puis sélectionnez l'icône **marquer l'application comme approuvée** . 
  
![Sélectionnez l'icône marquer l'application comme approuvée](media/OCAS-MarkOAuthApproved.png)
  
L'icône devient verte et l'application est approuvée pour tous vos utilisateurs d'Office 365.
  
> [!NOTE]
> Lorsque vous marquez une application comme approuvée, il n'y a aucun effet sur l'utilisateur final. Le marquage visuel des applications approuvées permet de les séparer des applications qui n'ont pas encore été révisées. 
  
## <a name="ban-an-app"></a>Interdire une application

1. Dans la page **gérer les applications OAuth** , recherchez l'application que vous souhaitez interdire, puis sélectionnez l'icône **marquer l'application comme interdite** .<br/>![Sélectionnez l'icône marquer l'application comme interdite.](media/OCAS-MarkOAuthBanned.png)
  
2. Dans la boîte de message de notification, conservez le texte existant tel quel, ou personnalisez le texte. Indiquez si les utilisateurs doivent savoir que leur application a été interdite. <br/>![Modèle de courrier d'une application interdite](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. Sélectionnez **interdire l'application**.

## <a name="report-an-oauth-app-to-microsoft"></a>Signaler une application OAuth à Microsoft

Si vous souhaitez soumettre une application OAuth à Microsoft pour analyse, vous pouvez signaler cette application.

1. Dans la page **gérer les applications OAuth** , recherchez l'application que vous souhaitez soumettre pour analyse.

2. Sélectionnez les points de suspension verticaux, puis choisissez **application de rapport...**.<br/>![Signaler une application OAuth](media/OCAS-MarkOAuthReported.png)<br/>

3. Dans la boîte de dialogue **signaler cette application** , utilisez la liste déroulante pour indiquer votre préoccupation. Par défaut, **cette application est malveillante** . Toutefois, vous pouvez choisir l'une des autres options disponibles. <br/>![Signaler une application OAuth](media/OCAS-ReportOAuthApp.png)<br/>

4. Recommandation Conservez l'option de contact que vous avez sélectionnée et confirmez (ou modifiez) l'adresse de messagerie indiquée.

5. Choose **Submit**. 
    
## <a name="create-an-app-query"></a>Créer une requête d'application

Nous vous recommandons d'utiliser l'affichage avancé, qui se présente comme suit: 

![Affichage avancé](media/OCAS-OAuthAppsAdvQueryView.png)

Dans la barre de requête application, si vous voyez **avancé**, vous utilisez l'affichage de base. Cliquez (ou appuyez) sur **avancé** pour accéder à l'affichage avancé. 

![Affichage de base](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. Dans la barre de requête, sélectionnez une option dans la liste **Sélectionner une** liste de filtres. 
    - **Application** Applications portant certains noms
    - **État** de l'application Applications en fonction de leur état (approuvé, interdit ou indéterminé)
    - **Utilisation communautaire** Applications basées sur les niveaux d'utilisation de la Communauté (rare, rares ou communs)
    - **Niveau d'autorisation** Applications basées sur certains niveaux d'autorisation 
    - **Autorisations** Applications qui requièrent certaines autorisations
    - **Éditeur**  Applications de certains éditeurs
    - **User (utilisateur** ) Applications autorisées par un certain utilisateur
   
2. Sélectionnez **est égal** ou **** différent de, puis spécifiez une valeur pour votre filtre.
    
3. Pour ajouter des filtres supplémentaires, sélectionnez le signe plus (![Ajouter une icône de filtre pour les applications de requête](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)), puis répétez les étapes 2 et 3.
    
4. Pour supprimer un filtre, sélectionnez le x (![Supprimer une icône de filtre pour les applications de requête](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) en regard d'un nom de filtre.
    
Les filtres sont appliqués automatiquement et la liste applications est mise à jour en conséquence.
  
## <a name="next-steps"></a>Étapes suivantes

- [Passer en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- Passez en revue les [journaux de trafic Web et les sources de données pour Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Examiner vos [activités d'utilisation pour Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    

