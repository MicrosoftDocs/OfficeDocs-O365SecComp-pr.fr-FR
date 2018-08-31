---
title: Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Autorisations d’application dans Office 365 Cloud application sécurité vous aident à gérer les applications de que vos utilisateurs téléchargement pour une utilisation avec des données d’Office 365
ms.openlocfilehash: 7bda35bbbf3a16cd1d386adcb03b1c7c4176913a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528493"
---
# <a name="manage-app-permissions-using-office-365-cloud-app-security"></a>Gérer les autorisations d’application à l’aide de la sécurité d’application Office 365 dans le nuage

Gestion de la sécurité Office 365 avancée est désormais sécurité d’application Office 365 dans le nuage.
  
|Évaluation **\>**|Planification **\>**|Déploiement **\>**|Utilisation du ***|
|:-----|:-----|:-----|:-----|
|[Commencer à évaluer](office-365-cas-overview.md) <br/> |[Commencer à planifier](get-ready-for-office-365-cas.md) <br/> |[Commencer à déployer](turn-on-office-365-cas.md) <br/> |Vous êtes ici !  <br/> [Étapes suivantes](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
Personnes amour applications et ils les téléchargent souvent, notamment les applications que les employés de réflexion seront gagner du temps en facilitant à leur travail ou établissement des informations. Cependant, certaines applications susceptibles de contenir un risque pour votre organisation, en fonction de quelles informations ils accèdent et comment gérer ces informations. Avec [Office 365 Cloud application sécurité](office-365-cas-overview.md), si vous êtes un administrateur global ou de sécurité, vous pouvez gérer les autorisations d’application pour votre organisation. Vous pouvez voir les applications qui utilisent les données d’Office 365, les autorisations de ces applications ont et bien plus encore. 
  
Cet article décrit comment créer une requête de l’application, où aller pour gérer les autorisations d’application et comment approuver ou interdire l’accès à une application.
  
## <a name="how-to-find-the-manage-app-permissions-page"></a>Comment trouver la page Gérer les autorisations application
<a name="findappperms"> </a>

> [!NOTE]
> Autorisations d’application sont gérées dans le portail Office 365 Cloud Application Security. Vous devez être un administrateur global ou un administrateur de sécurité pour effectuer la tâche suivante. Pour en savoir plus, consultez [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md). 
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. (Cela vous amène à la sécurité &amp; centre de conformité.) 
    
2. Accédez à des **alertes** \> **Gestion avancée des alertes**.
    
3. Cliquez (ou appuyez) **accédez à la sécurité d’application Office 365 dans le nuage**.
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    > [!NOTE]
    > Si la sécurité d’application Office 365 dans le nuage n’est pas encore activée, vous pouvez le faire dans cette page. Consultez [préparer à Office 365 nuage sécurité des applications](get-ready-for-office-365-cas.md). 
  
4. Cliquez sur **examiner** \> **autorisations d’application**.
    
    ![Dans le portail O365 autorités de certification, cliquez sur examiner.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
## <a name="what-youll-see-on-the-manage-app-permissions-page"></a>Vous verrez sur la page Gérer les autorisations application
<a name="whatsonpage"> </a>

Le tableau suivant décrit les contrôles et les options disponibles sur la page Gérer les autorisations application.
  
|**Élément**|**Description**|
|:-----|:-----|
|Icône de base dans la barre d’application requête  <br/> ![Icône qui indique le mode de requête de base pour interroger les autorisations d’application](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|Sélectionnez cette option pour passer à la vue avancée.  <br/> (Si vous voyez **base**, vous utilisez l’affichage avancé)  <br/> |
|Icône avancée dans la barre d’application requête  <br/> ![Icône qui indique que la vue de requête pour interroger les autorisations d’application avancée](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|Sélectionnez cette option pour passer à la vue de base.  <br/> (Si vous voyez **Avancé**, vous utilisez l’affichage de base.)  <br/> |
|Ouvrir ou fermer tous les détails icône dans la liste de l’application  <br/> ![Cliquez sur cette icône pour ouvrir ou fermer tous les détails pour toutes les applications](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|Sélectionnez cette icône pour afficher plus ou moins plus d’informations sur chaque application.  <br/> |
|Icône d’exportation dans la liste de l’application  <br/> ![Cliquez sur cette icône pour exporter un fichier csv de toutes les applications](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|Sélectionnez cette icône pour exporter un fichier CSV contenant une liste des applications, le nombre d’utilisateurs pour chaque application, les autorisations associées à l’application, le niveau d’autorisation, l’état de l’application, et utiliser le niveau de la Communauté.  <br/> |
|Name  <br/> |Permet d’afficher le nom d’une application, sélectionnez le nom à afficher plus d’informations, telles que sa description, publisher, site Web d’application et les ID d’application.  <br/> |
|Autorisé par  <br/> |Permet de voir combien d’utilisateurs ont autorisés à une application pour accéder à leur compte Office 365. Sélectionnez le numéro pour afficher plus d’informations, telle qu’une liste des comptes d’utilisateurs.  <br/> |
|Niveau d’autorisation  <br/> ![Icône qui indique le niveau de permisiions pour une application](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|Permet de déterminer le niveau d’accès une application a aux données d’Office 365. Les niveaux d’autorisation indiquent **faible**, **moyen**ou **élevé**, où **faible** peut indiquer que l’application accède uniquement au profil et le nom d’un utilisateur. Sélectionnez le niveau pour afficher plus d’informations, telles que les autorisations accordées à l’application, l’utilisation de la Communauté et activité associé dans le [journal de la gouvernance](suspend-or-restore-an-account-in-ocas.md).<br/> |
|État d’application ( **indéterminé**, **approuvé**ou **exclus**)  <br/> ![Icônes d’autorisations application une fois autorisés, bloqués ou aucune action n’a été pris par un administrateur](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)|Utiliser cette option pour marquer une application comme approuvé ou exclus, ou conservez l’indéterminée.  <br/> |
   
## <a name="mark-an-app-as-approved"></a>Marquer une application approuvée
<a name="approveapp"> </a>

Dans la page **Gérer les autorisations d’application** , recherchez l’application que vous souhaitez approuver et choisissez l’icône **d’application de marquer comme approuvée** . 
  
![Choisissez l’application de la marque sous forme d’icône approuvé](media/dd1b7690-441a-48c9-9c3a-58466513c63d.png)
  
L’icône s’affiche en verte et l’application est approuvée pour tous vos utilisateurs Office 365.
  
> [!NOTE]
> Lorsque vous marquez une application approuvée, il n’a aucun effet sur l’utilisateur final. Visuellement les applications approuvées permet de les séparer des applications qui n’ont pas été vérifiées. 
  
## <a name="ban-an-app"></a>Interdire l’accès à une application
<a name="banapp"> </a>

1. Dans la page **Gérer les autorisations d’application** , recherchez l’application que vous souhaitez interdire et sélectionnez l’icône **application marquer comme interdites** . 
    
    ![Choisissez l’application de la marque sous forme d’icône interdit](media/b9b1c5f6-fde7-46d5-8589-1564d05702b3.png)
  
2. Indiquez si vous souhaitez permettre aux utilisateurs de connaître interdits par leur application.
    
    (Recommandé) Pour informer les utilisateurs, sélectionnez **avertir les utilisateurs ayant accès à cette application interdite**et comment ajouter ou modifier un message de notification personnalisé.
    
    Pour ne pas informer les utilisateurs, désactivez **avertir les utilisateurs ayant accès à cette application interdite**.
    
    ![Le modèle de messagerie pour une application interdit](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)
  
3. Choisissez **application interdiction**.
    
## <a name="create-an-app-query"></a>Créer une requête de l’application
<a name="createapp"> </a>

1. Dans la barre de requête d’application, si vous voyez les **Options avancées**, cliquez sur (ou appuyez sur) pour accéder à la vue avancée. (Si vous voyez Basic, vous utilisez la vue avancée ; conserver votre affichage tel qu’il s’agit.)
    
2. Utilisez la liste **Sélectionnez un filtre** pour choisir une option. Le tableau suivant récapitule les options de filtre disponibles. 
    
|**Utilisez ce filtre**|**Pour afficher**|
|:-----|:-----|
|**App** <br/> |Applications avec certains noms  <br/> |
|**État de l’application** <br/> |Applications en fonction de leur état (approuvé, exclus ou indéterminé)  <br/> |
|**Utilisation de la Communauté** <br/> |Les applications en fonction de la Communauté utiliser niveaux (rares, Uncommon ou commune)  <br/> |
|**Niveau d’autorisation** <br/> |En fonction de certains niveaux d’autorisation des applications  <br/> |
|**Autorisations** <br/> |Applications qui nécessitent certaines autorisations  <br/> |
|**Éditeur** <br/> |Applications à partir de certains éditeurs  <br/> |
|**User** <br/> |Applications autorisés d’un utilisateur donné  <br/> |
   
3. Sélectionnez **est égal à** ou **n’est pas égal**, puis spécifiez une valeur pour votre filtre.
    
4. Pour ajouter d’autres filtres, sélectionnez le signe plus)![Ajouter une icône de filtre pour l’interrogation d’applications](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)), puis répétez les étapes 2 et 3.
    
5. Pour supprimer un filtre, sélectionnez le x (![Supprimer une icône de filtre pour l’interrogation d’applications](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)) en regard du nom d’un filtre.
    
Les filtres sont appliqués automatiquement, et la liste des applications est mis à jour en conséquence.
  
## <a name="next-steps"></a>Étapes suivantes
<a name="nextsteps"> </a>

- [Passez en revue et effectuer une action sur les alertes](review-office-365-cas-alerts.md)
    
- Passez en revue vos [sources de données Office 365 nuage sécurité des applications et de journaux de trafic Web](web-traffic-logs-and-data-sources-for-ocas.md)
    
- Passez en revue vos [activités utilisation Office 365 nuage sécurité des applications](utilization-activities-for-ocas.md)
    

