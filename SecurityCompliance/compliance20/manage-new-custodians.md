---
title: Gestion des dépositaires dans un cas eDiscovery avancées (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 742f6bc35b67071fba528e6a0ce543ecc6915762
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607717"
---
# <a name="managing-custodians-in-an-advanced-ediscovery-preview-case"></a>Gestion des dépositaires dans un cas eDiscovery avancées (Preview)

L’onglet dépositaires contient une liste triable de tous les dépositaires dans ce cas. Après avoir ajouté dépositaires à un cas, plus d’informations sur chaque dépositaire seront automatiquement collectées d’Azure Active Directory.

## <a name="viewing-custodian-details"></a>Affichage des détails dépositaire

La page flottant qui contient des détails dépositaire s’affiche après avoir ajouté un dépositaire à un cas et que vous les sélectionnez dans la liste sous l’onglet **dépositaires** . À partir de là, vous pouvez afficher tous les détails associés à ce dépositaire. La page flottant contient les champs suivants :

- Informations de contact

  - **Nom complet**: le nom affiché dans le carnet d’adresses pour le dépositaire. Il s’agit généralement de la combinaison du prénom de le dépositaire, initiale et le nom du milieu.
  - **/ SMTP Mail**: adresse SMTP le pour le dépositaire, par exemple, jeff@contoso.onmicrosoft.com.  
  - **Titre**: la fonction du dépositaire.
  - **Service**: le nom du service dans lequel fonctionne le dépositaire.
  - **Responsable**: responsable du dépositaire. Le responsable désigné reçoit toutes les communications pour cet dépositaire escalade.
  
- Informations d’emplacement

  - **Ville**: la ville dans laquelle se trouve le dépositaire.
  - **State**: état ou province dans l’adresse du dépositaire.
  - **Pays/région**: la pays/la région dans laquelle se trouve le dépositaire ; par exemple, « US » ou « Royaume-Uni ».
  - **Office**: l’emplacement de bureau en place du dépositaire de l’entreprise.

- Informations d’un incident

  - **État de blocage**: indique si le dépositaire a été mis en attente. 
  - **État de communication**: indique si le dépositaire a reçu un avis de suspension. Si le dépositaire a reçu un avis, ce sera marqué comme étant *publiée*. Si le dépositaire n’a pas été émis un avis, puis ce statut sera *non publié*. 
  - **État**: l’état de la dépositaire dans le cas. Il s’agit *Active* si le dépositaire est toujours en attente pour le cas. Si un dépositaire est supprimé à partir d’un cas, leur statut devient *lancé*. 

- Statut de traitement

  - **État de l’indexation**: indique l’état de la tâche d’indexation en profondeur.  
  - **Heure de mise à jour de la dernière indexation**: indique le datestamp de lorsque la tâche d’indexation approfondie a été déclenchée pour la dernière.
  - **Sources de données**: indique le nombre de boîtes aux lettres, les sites et les équipes qui ont été sélectionnées pour le dépositaire.

## <a name="updating-a-custodian"></a>Mise à jour un dépositaire

Fur et à votre cas, vous pouvez constater qu’il peuvent exister des sources de données supplémentaires pertinents pour un & spécifique dépositaire votre cas. Dans d’autres scénarios, vous souhaiterez peut-être supprimer certaines sources de données qui ont été révisées et considérés comme non pertinents.

Pour mettre à jour un dépositaire et les sources de données sélectionnées :

1. Sélectionnez un incident existant à partir de **découverte électronique > eDiscovery avancées (Preview)**.
  
2. Dans ce cas, cliquez sur l’onglet **dépositaires** .
  
3. Sélectionnez le custodian(s) dans la liste, cliquez sur **Modifier les sources**.
  
4. Mettre à jour les sélections pour Exchange et OneDrive les emplacements en cliquant sur **Choisir des sources de données**.
  
5. Ajouter ou supprimer des équipes, SharePoint ou Exchange boîtes aux lettres mappées l’utilisateur en cliquant sur Sélectionner les **sources de données supplémentaires**. Pour plus d’informations sur la façon dont vous permettent de mapper les données sources pour un dépositaire, voir [Ajouter dépositaires à une découverte électronique avancée (Preview) cas](add-custodians-to-case.md).
  
6. Pour mettre à jour l’état de conservation dépositaire, cliquez sur **garde archives permanentes**et activer ou désactiver la suspension pour dépositaires.

> [!TIP]
> Vous pouvez sélectionner plusieurs dépositaires pour effectuer les actions en bloc, telles que la réindexation, l’annulation ou modification d’un jeu de dépositaires.

## <a name="resolving-custodian-processing-errors"></a>Résolution des erreurs de traitement dépositaire

Dans la plupart des flux de travail juridique, après que dépositaires sont ajoutés à une enquête spécifique, un sous-ensemble de données d’utilisateurs est recherché. En raison de fichiers volumineux ou l’endommagement possible, certains éléments dans des sources de données des dépositaires peuvent être partiellement indexées. À l’aide de la fonctionnalité d’indexation approfondie eDiscovery avancées (Preview), ces éléments indexés partiellement peuvent être automatiquement convertis en nouvelle analyse et une réindexation de ces éléments à la demande. 

Lorsqu’un dépositaire est ajouté à un cas, leurs données seront automatiquement « profondeur indexées », qui permet aux utilisateurs de laisser ces partiellement indexée éléments place au lieu de devoir télécharger, corriger et exécutez de nouveau les recherches en dehors d’Office 365. Pendant le cycle de vie d’un incident, un utilisateur peut résoudre les éléments ou ajouter de nouvelles sources de données pour un dépositaire donné. Cela peut nécessiter l’Index dépositaire à mettre à jour. 

Pour déclencher un processus de renouvellement d’indexation adresse partiellement des éléments indexés :

1. Accédez à la **découverte électronique > avancée découverte électronique (Preview)** et sélectionnez un incident existant.

2. Dans ce cas, cliquez sur à **onglet dépositaires**. 

3. Sélectionnez le custodian(s) devant réindexation, puis cliquez sur **index de la mise à jour** dans la page mobile.

4. Vérifier l’état de l’index de dépositaire en cliquant sur le lien dans la colonne **travail indexation état** sous l’onglet **dépositaires** .  

5. L’état pour le processus de renouvellement d’indexation peut être suivi également dans l’onglet **tâches** .

Pour plus d’informations sur les éléments indexés partiellement nouveau indexation et correction, voir [fixation de traitement des erreurs d’eDiscovery avancée (Preview)](processing-data-for-case.md).

## <a name="releasing-a-custodian-from-a-case"></a>Libération d’un dépositaire à partir d’un cas

Un dépositaire est publié dans les situations de cas où un incident est fermé, un dépositaire n’est plus tenu de conserver le contenu d’un cas ou lorsqu’un dépositaire est considéré comme pas plus être pertinentes à un emplacement donné. 

Si vous relâchez un dépositaire après qu’un avis de suspension a été publié, une note de version est envoyé vers le dépositaire. En outre, les suspensions garde attribuées aux version finale dépositaires seront également supprimées.

Si le dépositaire a été placé sur une suspension en mode silencieux, où ils ont été délivrés pas les notifications de conservation légale, alors les suspensions garde attribuées aux version finale dépositaires seront supprimées.  

Pour libérer un dépositaire : 

1.  Accédez à l’onglet **dépositaires** .

2.  Sélectionnez le dépositaire dans la liste et cliquez sur **dépositaires version** dans la page mobile.

    L’état de la dépositaire sous l’onglet **dépositaires** est défini sur **lancé** et l' **état de blocage** sur la page flottant est modifiée à **inactif/Inactive**. 

> [!TIP]
> Un dépositaire peut être simultanément être impliqués dans plusieurs domaines de conservation légale. Lorsque l’utilisateur relâche un dépositaire à partir d’un cas, les suspensions et les notifications entre autres questions ne sont pas affectées.

## <a name="related-information"></a>Informations connexes

 - Attributs de l’utilisateur dans Active Directory 
 - [Correction d’erreur lors du traitement des données](error-remediation.md) 
 - [Utilisation des communications](managing-custodian-communications.md)
