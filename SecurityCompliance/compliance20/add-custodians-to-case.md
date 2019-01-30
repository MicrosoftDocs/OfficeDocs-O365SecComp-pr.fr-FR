---
title: Ajouter des dépositaires à une affaire eDiscovery avancées (Preview)
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
ms.openlocfilehash: d9a7dc6b1c2eeffdcd49be64d1d09d4a2bda782b
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607691"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a>Ajouter des dépositaires à une découverte électronique avancée (Preview) cas

À l’aide de la découverte électronique avancée (Preview), vous pouvez utiliser l’outil de gestion intégrés dépositaire pour coordonner votre flux de travail autour de la gestion des dépositaires et identification des sources de données pertinentes, garde au sein d’un cas. Lorsque vous ajoutez un dépositaire, le système peut automatiquement identifier et archives permanentes dans leur boîte aux lettres Exchange principale et de OneDrive pour le site de l’entreprise. Lorsque vous effectuez votre recherche, vous pouvez également découvrir et mapper les autres boîtes aux lettres ou les sites qu’un dépositaire accessible dans le passé ou des équipes qu’un dépositaire est un membre de la journée.

Utilisez le flux de travail suivante pour ajouter et gérer des dépositaires dans les cas eDiscovery avancées (Preview) dans le centre de conformité de & sécurité. 

## <a name="step-1-identify-potential-custodians"></a>Étape 1 : Identifier les éventuels dépositaires

La première étape consiste à identifier les dépositaires appropriés pour votre question. Pour ajouter des dépositaires à un cas, vous devez être un membre de la découverte électronique responsables ou un groupe de rôles Administrateurs eDiscovery.   

Pour ajouter des dépositaires à une affaire eDiscovery avancées (Preview) existant :

1. À partir de la page **Avancé eDiscovery (Preview)** , accédez à votre cas.
 
2. Après avoir sélectionné un incident, accédez à l’onglet **dépositaires** , cliquez sur **+ Ajouter dépositaire**. 
 
3. Choisissez les dépositaires que vous souhaitez ajouter à la casse. Vous pouvez démarrer en tapant pour rechercher et sélectionner les utilisateurs dans Azure Active Directory votre organisation.
 
4. Une fois que vous avez finalisé la liste des dépositaires, cliquez sur **suivant** pour commencer à identifier les sources de données potentielles. 
   
## <a name="optional-step-2-select-custodian-data-sources"></a>(Facultatif) Étape 2 : Sélectionner les sources de données dépositaire

Une fois que vous avez ajouté dépositaires à un cas, vous pouvez exploiter Office 365 pour vous aider à identifier et conserver les sources de données principale dépositaire. Ce flux de travail la prochaine étape consiste à sélectionner les sources de données détenus par les dépositaires spécifiés à l’étape 1. 

Pour identifier les sources de données dépositaire : 

1. Pour chaque conservateur, sélectionnez **Exchange** si vous souhaitez que le système à identifier et ajouter des boîtes aux lettres Exchange principale du dépositaire automatiquement. 
 
2. Pour chaque conservateur, sélectionnez **OneDrive** si vous souhaitez que le système à identifier et ajoutez principal OneDrive URL du dépositaire automatiquement. 

    Une fois que vous avez effectué vos sélections, ils système essaiera automatiquement identifier les sources de données et les ajouter à votre cas.
 
4. Cliquez sur **suivant** pour commencer le mappage des sources de données supplémentaires à votre dépositaire.

## <a name="optional-step-3-map-additional-data-sources"></a>(Facultatif) Étape 3 : Mapper des sources de données supplémentaires

Selon votre cas, vous pouvez également ajouter des boîtes aux lettres qui ont utilisés par le passé, un dépositaire donné groupes où un dépositaire est actuellement un membre, ou des sites qu’un dépositaire avait accès dans le passé. En plus des sources de données principale dépositaire, vous pouvez ajouter des sources de données Office 365 supplémentaires à un dépositaire ou tirer parti d’Office 365 pour vous aider à identifier les sources de données potentiellement pertinentes ainsi. 

Pour mapper des boîtes aux lettres, des sites ou des équipes à un dépositaire spécifique :
1. Sélectionnez **mise à jour** pour affecter des emplacements de contenu, tels que les boîtes aux lettres, les sites et les équipes, à un dépositaire spécifique. 

2. Dans la fenêtre mobile, spécifiez les éléments suivants :
   
  -  **Boîtes aux lettres Exchange** - cliquez sur **Choisir des utilisateurs, des équipes ou des groupes** , puis sur **Choisir des utilisateurs, des équipes ou des groupes** . Pour spécifier les boîtes aux lettres à affecter à la dépositaire sélectionné, utilisez la zone Rechercher pour rechercher les boîtes aux lettres utilisateur et des groupes de distribution. Vous pouvez également assigner la boîte aux lettres associée pour un groupe d’Office 365 ou un Team Microsoft. Sélectionnez l’utilisateur, le groupe, la case à cocher de l’équipe, cliquez sur **Choisir**, puis cliquez sur **terminé**.

      > [!NOTE]
      > Lorsque vous cliquez sur Choisir des utilisateurs, des groupes ou équipes pour spécifier les boîtes aux lettres, le sélecteur de boîte aux lettres qui s’affiche est vide. Il s’agit par défaut pour améliorer les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche.
     
   - **Sites SharePoint** : cliquez sur **Choisir les sites** , puis sur **Choisir les sites** pour spécifier supplémentaires SharePoint et OneDrive pour les sites entreprise que vous souhaitez attribuer à la dépositaire sélectionné. Vous pouvez également ajouter l’URL du site SharePoint pour un groupe d’Office 365 ou un Team Microsoft. Tapez l’URL pour chaque site que vous voulez affecter. Cliquez sur **Choisir**, puis cliquez sur **terminé**.
   - **Les équipes Microsoft** – **Choisissez les équipes** et cliquez sur **Choisir des équipes** pour afficher une liste de groupes Microsoft Team que le dépositaire est un membre de la journée. Sélectionnez les équipes que vous souhaitez ajouter à votre dépositaire. Une fois sélectionné, le système identifie automatiquement & sélectionner que le site SharePoint et les boîtes aux lettres de groupe associé associé à ce Microsoft Team. Cliquez sur **Choisir**, puis cliquez sur **terminé**.
        
      > [!NOTE]
      > Pour ajouter d’autres Teams Microsoft, vous devrez ajouter séparément les boîtes aux lettres et un site SharePoint comme indiqué ci-dessus.

Une fois que vous avez terminé le mappage des sources de votre, vous pouvez afficher le total boîtes aux lettres, les sites et les équipes pour les dépositaires que vous venez d’ajouter. Lorsque vous avez finalisé les sources de données pertinentes pour un dépositaire spécifique, ce mappage sera être conservé et étendu pour la collection de découverte électronique, le traitement et passer en revue les flux de travail. 

## <a name="optional-step-4-place-custodians-on-hold"></a>(Facultatif) Étape 4 : Suspendre dépositaires sur

 Une fois que vous avez finalisé la dépositaires et sources de données que vous souhaitez ajouter à votre cas, vous pouvez éventuellement placer certains ou tous vos dépositaires sur mise en suspens. Lorsque vous bloquez un dépositaire, le contenu mappé à cet utilisateur est conservé jusqu'à ce que vous relâchiez la dépositaire à partir de la casse ou jusqu'à ce que vous supprimez la suspension. Dans certains cas, vous souhaiterez peut-être ajouter dépositaires à un cas sans les placer en attente. 

Pour placer les sélectionné dépositaires et sources de données sur contiennent :

1. Vérifiez vos sélections dépositaire et sélectionnez le checkox placer chaque dépositaire en attente. Une fois qu’un dépositaire est mis en attente, une stratégie de blocage dépositaire contenant les sources de toutes les garde sera créée automatiquement. Si l’option n’est pas activée, les sources de données dépositaire & sélectionné seront ajoutés à la casse, mais le contenu n’est pas conservé.

2. Accédez à l’onglet **contient** et sélectionnez la **Stratégie de blocage de dépositaire**. 

3. Cliquez sur **Modifier** pour afficher toutes les sources de données dépositaire sélectionné.
