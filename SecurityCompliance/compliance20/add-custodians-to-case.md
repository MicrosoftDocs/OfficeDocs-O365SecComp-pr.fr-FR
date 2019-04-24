---
title: Ajouter des dépositaires à un cas avancé eDiscovery (aperçu)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: fe208f4a9f7927d8481d5c6ec8b901baafb98626
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243556"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a>Ajouter des dépositaires à un cas avancé eDiscovery (aperçu)

Advanced eDiscovery (aperçu) vous permet d'utiliser l'outil de gestion des dépositaires intégré pour coordonner vos flux de travail en matière de gestion des dépositaires et d'identification des sources de données appropriées dans un cas. Lorsque vous ajoutez un dépositaire, le système peut automatiquement identifier et placer des suspensions sur sa boîte aux lettres Exchange principale et sur le site OneDrive entreprise. Lors de votre découverte, vous pouvez également dévoiler et mapper des boîtes aux lettres ou des sites supplémentaires auxquels un dépositaire est accédé par le passé ou teams dont le dépositaire est membre.

Utilisez le flux de travail suivant pour ajouter et gérer des dépositaires dans les cas avancés de découverte électronique (préversion) dans le centre de sécurité & Compliance Center. 

![Onglet gestion des dépositaires](../media/CustodianMgtPage.png)


## <a name="step-1-identify-potential-custodians"></a>Étape 1: identifier les dépositaires potentiels

La première étape consiste à identifier les dépositaires appropriés pour votre question. Pour ajouter des dépositaires à un cas, vous devez être membre du groupe de rôles gestionnaires eDiscovery ou administrateurs eDiscovery.   

![Identifier les dépositaires potentiels](../media/AddCustodianStep1.png)

Pour ajouter des dépositaires à une sacoche eDiscovery (préversion) avancée existante:

1. À partir de la page **Advanced eDiscovery (aperçu)** , accédez à votre cas.
 
2. Une fois que vous avez sélectionné un cas, accédez **** à l'onglet dépositaires et cliquez sur **+ Ajouter un dépositaire**. 
 
3. Choisissez les dépositaires que vous souhaitez ajouter à l'incident. Vous pouvez commencer par taper pour rechercher et sélectionner les utilisateurs dans Azure Active Directory de votre organisation.
 
4. Après avoir finalisé la liste des dépositaires, cliquez sur **suivant** pour commencer à identifier les sources de données potentielles. 
  
## <a name="optional-step-2-select-custodian-data-sources"></a>Module Étape 2: sélection des sources de données du dépositaire

Une fois que vous avez ajouté des dépositaires à un cas, vous pouvez tirer parti d'Office 365 pour vous aider à identifier et à conserver les sources de données des dépositaires principaux. L'étape suivante de ce flux de travail consiste à sélectionner les sources de données appartenant aux dépositaires spécifiées à l'étape 1. 

![Sélectionner des sources de données privatives de Troie](../media/AddCustodianStep2.png)

Pour identifier les sources de données des dépositaires: 

1. Pour chaque dépositaire, sélectionnez **Exchange** si vous souhaitez que le système identifie automatiquement et ajoute la boîte aux lettres Exchange principale du dépositaire. 
 
2. Pour chaque dépositaire, sélectionnez **OneDrive** si vous voulez que le système identifie automatiquement et ajoute l'URL onedrive principale du dépositaire. 

    Une fois que vous avez effectué vos sélections, le système tente automatiquement d'identifier les sources de données et de les ajouter à votre cas.
 
4. Cliquez sur **suivant** pour commencer à mapper des sources de données supplémentaires à votre dépositaire.

## <a name="optional-step-3-map-additional-data-sources"></a>Module Étape 3: mapper des sources de données supplémentaires

En fonction de votre cas, vous pouvez également ajouter des boîtes aux lettres qu'un dépositaire donné a peut-être utilisé dans le passé, des groupes pour lesquels un dépositaire est actuellement membre ou des sites auxquels un dépositaire a accès dans le passé. En plus des sources de données des dépositaires principaux, vous pouvez ajouter des sources de données Office 365 supplémentaires à un dépositaire ou utiliser Office 365 pour vous aider à identifier également les sources de données pertinentes. 

![Mapper des sources de données supplémentaires](../media/AddCustodianStep3.PNG)

Pour mapper des boîtes aux lettres, des sites ou des équipes à un dépositaire spécifique:
1. Sélectionnez **Ajouter** pour affecter des emplacements de contenu, tels que des boîtes aux lettres, des sites et des équipes, à un dépositaire spécifique. 

2. Dans le menu volant, spécifiez les ![éléments suivants: mapper des sources de données](../media/AddCustodianStep4.PNG)
  -  **Boîtes aux lettres Exchange** : cliquez sur **choisir les utilisateurs, les groupes ou les équipes** , puis cliquez à nouveau sur **choisir les utilisateurs, les groupes ou les équipes** . Pour spécifier les boîtes aux lettres à affecter au dépositaire sélectionné, utilisez la zone de recherche pour rechercher des boîtes aux lettres utilisateur et des groupes de distribution. Vous pouvez également affecter la boîte aux lettres associée pour un groupe Office 365 ou une équipe Microsoft. Activez la case à cocher utilisateur, groupe, équipe, cliquez sur **choisir**, puis sur **Terminer**.

        > [!NOTE]
        > Lorsque vous cliquez sur choisir les utilisateurs, les groupes ou les équipes pour spécifier des boîtes aux lettres, le sélecteur de boîtes aux lettres affiché est vide. Il s'agit d'une conception qui améliore les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche.
     
     - **Sites SharePoint** : cliquez sur **choisir des sites** , puis cliquez sur choisir de nouveau les **sites** pour spécifier d'autres sites SharePoint et OneDrive entreprise que vous souhaitez affecter au dépositaire sélectionné. Vous pouvez également ajouter l'URL du site SharePoint pour un groupe Office 365 ou une équipe Microsoft. Tapez l'URL de chaque site que vous souhaitez attribuer. Cliquez sur **choisir**, puis sur **Terminer**.
     - **Microsoft** teams – cliquez sur **choisir teams** , puis cliquez sur **choisir les équipes** pour afficher la liste des groupes d'équipes Microsoft dont le dépositaire est membre. Sélectionnez les équipes que vous souhaitez ajouter à votre dépositaire. Une fois sélectionné, le système identifie automatiquement & sélectionnez le site SharePoint et la boîte aux lettres de groupe associés associés à cette équipe Microsoft. Cliquez sur **choisir**, puis sur **Terminer**.
        
      > [!NOTE]
      > Pour ajouter des Microsoft teams supplémentaires, vous devez ajouter séparément la boîte aux lettres et le site SharePoint, comme indiqué ci-dessus.

Une fois que vous avez terminé le mappage de vos sources, vous pouvez afficher le nombre total de boîtes aux lettres, de sites et d'équipes pour les dépositaires que vous venez d'ajouter. Une fois que vous avez finalisé les sources de données pertinentes pour un dépositaire spécifique, ce mappage est maintenu et étendu aux flux de travail de collecte, de traitement et de révision de découverte électronique. 

## <a name="optional-step-4-place-custodians-on-hold"></a>Module Étape 4: placer des dépositaires en conservation

![Placer des suspensions](../media/AddCustodianStep5.PNG)

Une fois que vous avez finalisé les dépositaires et les sources de données que vous souhaitez ajouter à votre cas, vous pouvez éventuellement placer une partie ou la totalité de vos dépositaires en conservation. Lorsque vous mettez un dépositaire en conservation, le contenu mappé sur cet utilisateur est conservé jusqu'à ce que vous relâchiez le déblocage du dépositaire ou jusqu'à ce que vous supprimiez le blocage. Dans certains cas, vous souhaiterez peut-être ajouter des dépositaires à un cas sans les mettre en attente. 

Pour placer les dépositaires et les sources de données sélectionnés en conservation:

1. Vérifiez vos sélections de dépositaire et activez la case à cocher pour placer chaque dépositaire en conservation. Une fois qu'un dépositaire est mis en attente, une stratégie de blocage des dépositaires contenant toutes les sources privatives de place est automatiquement créée. Si cette option n'est pas cochée, le dépositaire et les sources de données sélectionnées seront ajoutés, mais le contenu ne sera pas préservé.

2. Accédez à l' **** onglet suspensions et sélectionnez la **stratégie de blocage**des dépositaires. 

3. Cliquez sur **modifier** pour afficher toutes les sources de données de dépositaire sélectionnées.

   
