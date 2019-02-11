---
title: Gérer les applications OAuth à l’aide de la sécurité des applications cloud Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Applications OAuth dans Office 365 Cloud application sécurité vous aident à gérer les applications de que vos utilisateurs téléchargement pour une utilisation avec des données d’Office 365
ms.openlocfilehash: ae32e3c6b15f4ad4794a3dd08c3992adaeba655c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603685"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a>Gérer les applications OAuth à l’aide de la sécurité des applications cloud Office 365

|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étapes suivantes](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
Personnes amour applications et ils les téléchargent souvent, notamment les applications que les employés de réflexion seront gagner du temps en facilitant à leur travail ou établissement des informations. Cependant, certaines applications susceptibles de contenir un risque pour votre organisation, en fonction de quelles informations ils accèdent et comment gérer ces informations. Avec [Office 365 Cloud application sécurité](office-365-cas-overview.md), si vous êtes un administrateur global ou de sécurité, vous pouvez gérer les applications OAuth pour votre organisation. Vous pouvez voir les applications qui utilisent les données d’Office 365, les autorisations de ces applications ont et bien plus encore. 
  
Cet article décrit comment créer une requête de l’application, où aller pour gérer les applications OAuth et comment approuver, interdire ou un état d’une application.
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a>Comment trouver la page OAuth gérer des applications

> [!NOTE]
> Applications OAuth sont gérées dans le portail Office 365 Cloud Application Security. Vous devez être un administrateur global ou un administrateur de sécurité pour effectuer la tâche suivante. Pour en savoir plus, consultez [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
1. Accédez au portail de sécurité des applications dans le nuage ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) et se connecter.
  
2. Choisissez **étudier** \> **applications OAuth**.<br/>![Dans le portail O365 autorités de certification, cliquez sur examiner.](media/OCAS-OAuthApps.png)<br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a>Vous verrez dans la page applications de gérer les OAuth

Le tableau suivant décrit les contrôles et les options disponibles dans la page applications de OAuth gérer.
  
|**Élément**|**Description**|
|:-----|:-----|
|Icône de base dans la barre d’application requête  <br/> ![Icône qui indique le mode de requête de base pour l’interrogation](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Sélectionnez cette option pour passer à la vue avancée.  <br/> (Si vous voyez **base**, vous utilisez l’affichage avancé)  <br/> |
|Icône avancée dans la barre d’application requête  <br/> ![Icône qui indique l’affichage de requête avancées pour l’interrogation](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Sélectionnez cette option pour passer à la vue de base.  <br/> (Si vous voyez **Avancé**, vous utilisez l’affichage de base.)  <br/> |
|Ouvrir ou fermer tous les détails icône dans la liste de l’application  <br/> ![Cliquez sur cette icône pour ouvrir ou fermer tous les détails pour toutes les applications](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Sélectionnez cette icône pour afficher plus ou moins plus d’informations sur chaque application.  <br/> |
|Icône d’exportation dans la liste de l’application  <br/> ![Cliquez sur cette icône pour exporter un fichier csv de toutes les applications](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Sélectionnez cette icône pour exporter un fichier CSV contenant une liste des applications, le nombre d’utilisateurs pour chaque application, les autorisations associées à l’application, le niveau d’autorisation, l’état de l’application, et utiliser le niveau de la Communauté.  <br/> |
|Nom  <br/> |Permet d’afficher le nom d’une application, sélectionnez le nom à afficher plus d’informations, telles que sa description, publisher, site Web d’application et les ID d’application.  <br/> |
|Autorisé par  <br/> |Permet de voir combien d’utilisateurs ont autorisés à une application pour accéder à leur compte Office 365. Sélectionnez le numéro pour afficher plus d’informations, telle qu’une liste des comptes d’utilisateurs.  <br/> |
|Niveau d’autorisation  <br/> ![Icône qui indique le niveau de permisiions pour une application](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Permet de déterminer le niveau d’accès une application a aux données d’Office 365. Les niveaux d’autorisation indiquent **faible**, **moyen**ou **élevé**, où **faible** peut indiquer que l’application accède uniquement au profil et le nom d’un utilisateur. Sélectionnez le niveau pour afficher plus d’informations, telles que les autorisations accordées à l’application, l’utilisation de la Communauté et activité associé dans le [journal de la gouvernance](suspend-or-restore-an-account-in-ocas.md).<br/> |
|Dernière autorisés <br/> |Permet d’afficher la date et l’heure qu'une application OAuth dernière a été autorisée à accéder aux données de votre organisation Office 365. <br/>  |
|Actions<br/>![Applications OAuth](media/OCAS-OAuthAppApproveBanReport.png)<br/> |Permet d’afficher ou pour marquer une application comme approuvé ou exclus, signaler une application OAuth à Microsoft, ou conservez l’indéterminée.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Marquer une application approuvée

Dans la page **OAuth gérer les applications** , recherchez l’application que vous souhaitez approuver et choisissez l’icône **d’application de marquer comme approuvée** . 
  
![Choisissez l’application de la marque sous forme d’icône approuvé](media/OCAS-MarkOAuthApproved.png)
  
L’icône s’affiche en verte et l’application est approuvée pour tous vos utilisateurs Office 365.
  
> [!NOTE]
> Lorsque vous marquez une application approuvée, il n’a aucun effet sur l’utilisateur final. Visuellement les applications approuvées permet de les séparer des applications qui n’ont pas été vérifiées. 
  
## <a name="ban-an-app"></a>Interdire l’accès à une application

1. Dans la page **OAuth gérer les applications** , recherchez l’application que vous souhaitez interdire et sélectionnez l’icône **application marquer comme interdites** .<br/>![Choisissez l’application de la marque sous forme d’icône interdit](media/OCAS-MarkOAuthBanned.png)
  
2. Dans la boîte de message de notification, conservez le texte existant comme il est, ou personnaliser le texte. Indiquez si vous souhaitez permettre aux utilisateurs de connaître interdits par leur application. <br/>![Le modèle de messagerie pour une application interdit](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. Choisissez **application interdiction**.

## <a name="report-an-oauth-app-to-microsoft"></a>Signaler à Microsoft les une application OAuth

Si vous souhaitez envoyer une application OAuth à Microsoft pour analyse, vous pouvez signaler cette application.

1. Dans la page **applications OAuth gérer** , recherchez l’application que vous voulez envoyer pour analyse.

2. Sélectionnez les points de suspension vertical, puis **rapport App..**.<br/>![Signaler une application OAuth](media/OCAS-MarkOAuthReported.png)<br/>

3. Dans la boîte de dialogue **rapport de cette application** , utilisez la liste déroulante pour indiquer votre problème. Par défaut, **cette application est malveillante** est sélectionnée. Toutefois, vous pouvez choisir sur un des autres options disponibles.<br/>![Signaler une application OAuth](media/OCAS-ReportOAuthApp.png)<br/>

4. (Recommandé) L’option de vous contacter sélectionné et vérifier (ou modifier) l’adresse de messagerie répertorié.

5. Choisissez **Submit (Envoyer)**. 
    
## <a name="create-an-app-query"></a>Créer une requête de l’application

Nous recommandons l’utilisation de la vue avancée, qui ressemble à ceci : 

![Vue avancée](media/OCAS-OAuthAppsAdvQueryView.png)

Dans la barre de requête d’application, si vous voyez **Avancé**, vous utilisez l’affichage de base. Cliquez (ou appuyez) **Avancé** pour accéder à la vue avancée. 

![Affichage de base](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. Dans la barre de requête, utilisez la liste **Sélectionnez un filtre** pour choisir une option. 
    - **Application** Applications avec certains noms
    - **État de l’application** Applications en fonction de leur état (approuvé, exclus ou indéterminé)
    - **Utilisation de la Communauté** Les applications en fonction de la Communauté utiliser niveaux (rares, Uncommon ou commune)
    - **Niveau d’autorisation** En fonction de certains niveaux d’autorisation des applications 
    - **Autorisations** Applications qui nécessitent certaines autorisations
    - **Publisher**  Applications à partir de certains éditeurs
    - **Utilisateur** Applications autorisés d’un utilisateur donné
   
2. Sélectionnez **est égal à** ou **n’est pas égal**, puis spécifiez une valeur pour votre filtre.
    
3. Pour ajouter d’autres filtres, sélectionnez le signe plus)![Ajouter une icône de filtre pour l’interrogation d’applications](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)), puis répétez les étapes 2 et 3.
    
4. Pour supprimer un filtre, sélectionnez le x (![Supprimer une icône de filtre pour l’interrogation d’applications](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) en regard du nom d’un filtre.
    
Les filtres sont appliqués automatiquement, et la liste des applications est mis à jour en conséquence.
  
## <a name="next-steps"></a>Étapes suivantes

- [Passez en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- Passez en revue vos [sources de données Office 365 nuage sécurité des applications et de journaux de trafic Web](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)
    

