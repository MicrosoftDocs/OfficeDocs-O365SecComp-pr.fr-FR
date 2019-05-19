---
title: Ajouter des dépositaires à un cas avancé eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 8cc3d7db959c31c4657bb8c0d270f014e598e143
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155336"
---
# <a name="add-custodians-to-an-advanced-ediscovery-case"></a>Ajouter des dépositaires à un cas avancé eDiscovery

Utilisez l’outil de gestion des dépositaires intégré dans Advanced eDiscovery pour coordonner vos flux de travail concernant la gestion des dépositaires et l’identification des sources de données appropriées et privatives de ressources associées à un cas. Lorsque vous ajoutez un dépositaire, le système peut automatiquement identifier et placer un blocage sur sa boîte aux lettres Exchange et sur son compte OneDrive entreprise. Lors du processus de découverte de votre enquête, vous pouvez également identifier des sources de données supplémentaires (telles que des boîtes aux lettres, des sites ou des équipes) auxquelles un dépositaire a accédé ou auquel il a contribué. Dans ce cas, vous pouvez utiliser l’outil de gestion des dépositaires pour associer ces sources de données à un dépositaire spécifique. Après avoir ajouté des dépositaires à un cas et associé à d’autres sources de données, vous pouvez conserver rapidement les données et rechercher les données privatives de temps.

Utilisez le flux de travail suivant pour ajouter et gérer des dépositaires dans des cas avancés de découverte électronique. 

![Onglet gestion des dépositaires](../media/CustodianMgtPage.png)

## <a name="before-you-begin"></a>Avant de commencer

Pour ajouter des dépositaires à un cas, vous devez être membre du groupe de rôles gestionnaire de découverte électronique. Vous bénéficierez ainsi des autorisations nécessaires pour ajouter des dépositaires à un cas et mettre en place une conservation sur les sources de données privatives de Troie.


## <a name="step-1-add-potential-custodians"></a>Étape 1: ajouter des dépositaires potentiels

La première étape consiste à identifier et à ajouter des dépositaires à la demande de devis.

1. Sur la page d’accueil de la **découverte électronique avancée** , cliquez sur le cas auquel vous souhaitez ajouter des dépositaires. 
 
2. Cliquez sur **** l’onglet dépositaires, puis cliquez sur **+ Ajouter**des dépositaires.

3. Recherchez les dépositaires à ajouter au cas. Tapez la première partie du nom d’une personne pour afficher les utilisateurs de l’Azure Active Directory de votre organisation. Lorsque vous trouvez la personne appropriée, cliquez sur son nom pour l’ajouter à la liste.

   ![Identifier les dépositaires potentiels](../media/AddCustodianStep1.png)
 
4. Après avoir ajouté tous les dépositaires pertinents, cliquez sur **suivant** pour sélectionner les sources de données principales des dépositaires.
  
## <a name="step-2-select-custodian-data-sources"></a>Étape 2: sélection des sources de données du dépositaire

Après avoir ajouté des dépositaires, l’outil dépositaire vous aidera à identifier les principales sources de données appartenant à chaque dépositaire; en particulier, ces emplacements de données sont la boîte aux lettres Exchange du dépositaire et le compte OneDrive. 

Pour identifier les sources de données des dépositaires: 

1. Pour sélectionner la boîte aux lettres Exchange pour tous les dépositaires, cliquez sur la case à cocher **Exchange** en haut de la colonne. Notez que vous pouvez désélectionner la case à cocher d’un dépositaire spécifique pour supprimer une boîte aux lettres en tant qu’emplacement privative. Vous pouvez également laisser la case à cocher **Exchange** en haut de la colonne désélectionnée, puis activer la case à cocher pour les dépositaires individuels. 
 
   ![Sélectionner des sources de données privatives de Troie](../media/AddCustodianStep2.png)
 
2. Répétez la même opération pour les comptes OneDrive des dépositaires. 

    Une fois que vous avez sélectionné les sources de données des dépositaires, le système tente automatiquement d’identifier et de vérifier ces sources de données, puis les ajoute à la casse en tant que sources de données associées aux dépositaires.
 
4. Cliquez sur **suivant** pour commencer à associer des sources de données supplémentaires aux dépositaires dans le cas.

## <a name="step-3-associate-additional-data-sources-to-a-custodian"></a>Étape 3: associer des sources de données supplémentaires à un dépositaire

Selon le cas que vous étudiez, vous devrez peut-être également rechercher (et conserver le contenu dans) les boîtes aux lettres auxquelles un dépositaire spécifique a accès, les groupes Office 365 auxquels un dépositaire est actuellement membre ou les sites auxquels un dépositaire a également accédé. Ainsi, en plus des sources de données des dépositaires que vous avez spécifiées à l’étape précédente, vous pouvez également associer des sources de données Office 365 supplémentaires à un dépositaire dans le cas. 

Pour mapper des boîtes aux lettres, des sites ou des équipes à un dépositaire spécifique:

1. Sur la page **Sélectionner des sources de données supplémentaires** , cliquez sur **Ajouter** dans la ligne du dépositaire spécifique. 
  
   ![Mapper des sources de données supplémentaires](../media/AddCustodianStep3.PNG)

2. Sur la page de menu volant, vous pouvez spécifier une source de données à partir des services Office 365 suivants:
  
   -  **Courrier Exchange** -cliquez sur **choisir les utilisateurs, les groupes ou les équipes** , puis cliquez sur **choisir les utilisateurs, les groupes ou les équipes** . Utilisez la zone de recherche pour trouver les boîtes aux lettres à associer au dépositaire. Pour spécifier les boîtes aux lettres à affecter au dépositaire sélectionné, utilisez la zone de recherche pour rechercher des boîtes aux lettres utilisateur et des groupes de distribution. Vous pouvez également affecter la boîte aux lettres associée pour un groupe Office 365 ou une équipe Microsoft. Activez la case à cocher utilisateur, groupe, équipe, cliquez sur **choisir**, puis sur **Terminer**.

        > [!NOTE]
        > Lorsque vous cliquez sur choisir les utilisateurs, les groupes ou les équipes pour spécifier des boîtes aux lettres, le sélecteur de boîtes aux lettres affiché est vide. Il s’agit d’une conception qui améliore les performances. Pour ajouter une boîte aux lettres à cette liste, tapez un nom ou un alias (un minimum de 3 caractères) dans la zone de recherche.
     
     - **Sites SharePoint** : cliquez sur **choisir des sites** , puis cliquez à nouveau sur choisir les **sites** pour afficher la liste des sites SharePoint dans votre organisation. Pour associer un site au dépositaire, vous pouvez sélectionner un site dans la liste ou vous pouvez taper l’URL d’un autre site ou d’un site associé à un groupe Office 365, Microsoft Team ou un compte OneDrive.
     
     - **Teams** : cliquez sur **choisir teams** , puis cliquez sur **choisir les équipes** pour afficher la liste de Microsoft teams dont le dépositaire est actuellement membre. Sélectionnez les équipes que vous souhaitez ajouter à votre dépositaire. Une fois sélectionné, le système identifie automatiquement & sélectionnez le site SharePoint et la boîte aux lettres de groupe associés associés à cette équipe Microsoft. Cliquez sur **choisir**, puis sur **Terminer**.

       ![Mapper des sources de données](../media/AddCustodianStep4.PNG)
        
      > [!NOTE]
      > Pour associer une équipe supplémentaire à un dépositaire, vous devez ajouter séparément la boîte aux lettres et le site associés à l’équipe à l’aide des emplacements de **messagerie Exchange** et de **sites SharePoint** .

Une fois que vous avez terminé d’associer des sources de données supplémentaires aux dépositaires, vous pouvez afficher le nombre total de boîtes aux lettres, de sites et de équipes associées à chaque dépositaire dans la **page Sélectionner des sources de données supplémentaires**. Une fois que vous avez finalisé les sources de données pertinentes pour un dépositaire spécifique, cette association est conservée et utilisée pendant les étapes de collecte, de traitement et de révision dans le flux de travail de découverte électronique.

## <a name="step-4-place-custodians-on-hold"></a>Étape 4: placer des dépositaires en conservation

Une fois que vous avez finalisé les dépositaires et les sources de données à ajouter à l’incident, vous pouvez éventuellement placer une partie ou la totalité des dépositaires en attente. Lorsque vous mettez un dépositaire en conservation, tout le contenu de tous les emplacements de contenu associés au dépositaire est conservé jusqu’à ce que vous supprimiez le blocage ou libériez le dépositaire du. Dans certains cas, vous souhaiterez peut-être ajouter des dépositaires à un cas sans les mettre en attente.

Pour placer les dépositaires et les sources de données en conservation:

1. Sur la page **bloquer les dépositaires sélectionnés** , activez la case à cocher en attente en haut de la colonne pour placer tous les dépositaires en attente. **** Notez que vous pouvez désélectionner la case à cocher d’un dépositaire spécifique à retirer de la suspension. Vous pouvez également laisser la case à cocher **suspendre** en haut de la colonne désélectionnée, puis activer la case à cocher pour les dépositaires individuels. 
 
   ![Placer des suspensions](../media/AddCustodianStep5.PNG)

2. Vérifiez que le dépositaire contient des sélections, puis cliquez sur **Terminer**.

Si vous ne placez pas de dépositaire, le dépositaire et les sources de données associées seront ajoutés à la casse, mais le contenu de ces sources de données ne sera pas mis en attente.

Une fois qu’un dépositaire est mis en attente, une stratégie de blocage des dépositaires contenant toutes les sources privatives de place est automatiquement créée. Pour afficher cette stratégie:

1. Sur la page d' **Accueil** de l’incident, cliquez sur l’onglet **suspensions** , puis cliquez sur **CustodianHold-GUID**,  

2. Sur la page de la fenêtre volante, cliquez sur **modifier la suspension** pour afficher toutes les sources de données de dépositaire mises en attente.

