---
title: Gérer les personnes concernées par les enquêtes de données (aperçu)
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
ms.openlocfilehash: d06dde60ae75cfea1bf1d79f445b613d20a76363
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030045"
---
# <a name="manage-people-of-interest-in-data-investigations-preview"></a>Gérer les personnes concernées par les enquêtes de données (aperçu)

Les enquêtes sur les données impliquent souvent des personnes intéressantes. En règle générale, il s'agit de personnes qui possèdent les données déplacées, sensibles ou malveillantes que vous recherchez ou qui cherchent à corriger. Dans les **enquêtes de données (** préversion), vous pouvez les ajouter pour découvrir les sources de données à utiliser pour la portée de votre recherche ou afficher des informations supplémentaires telles que les journaux de contact, d'emplacement et d'activité. 


## <a name="add-people-of-interest"></a>Ajouter des personnes intéressantes

Dans l'onglet **personnes** , vous pouvez ajouter des personnes intéressantes et découvrir leurs sources de données telles que les boîtes aux lettres Exchange ou le site OneDrive entreprise que vous pouvez utiliser pour étendre votre recherche. Lorsqu'elles sont délimitées par des personnes intéressantes, les recherches sont plus performantes et précises car l'outil réexécute toutes les données non indexées, telles que les images ou les types de fichiers non pris en charge. Vous pouvez également consulter les informations de contact, les informations d'emplacement et les journaux d'activité que vous pouvez utiliser pour initier des communications ou approfondir leurs activités. 

Pour ajouter des personnes intéressantes à une enquête:

1. À partir de la page **enquêtes de données (aperçu)** , accédez à votre enquête.
 
2. Une fois que vous avez sélectionné une enquête, accédez à l'onglet **personnes d'intérêt** et cliquez sur **+ Ajouter des personnes qui**vous intéressent. 
 
3. Choisissez les personnes que vous souhaitez ajouter à l'enquête. Vous pouvez commencer par taper pour rechercher et sélectionner les utilisateurs dans Azure Active Directory de votre organisation.
 
4. Une fois que vous avez finalisé la liste des personnes intéressantes, cliquez sur **suivant** pour mapper leurs sources de données. 

5. Module Pour chaque personne, sélectionnez **Exchange** pour ajouter la boîte aux lettres Exchange principale de la personne et **onedrive** pour ajouter le site onedrive entreprise principal de la personne.

6. Module Cliquez sur **suivant** pour ajouter d'autres sources de données que vous souhaitez associer à vos personnes intéressantes.

7. Module Sélectionnez **mettre à jour** pour affecter des emplacements de contenu, comme des boîtes aux lettres, des sites et des équipes à une personne. 

8. Module Dans le menu volant:
   
    -  **Boîtes aux lettres Exchange** : cliquez sur **choisir les utilisateurs, les groupes ou les équipes** , puis cliquez à nouveau sur **choisir les utilisateurs, les groupes ou les équipes** . Pour ajouter d'autres boîtes aux lettres, utilisez la zone de recherche pour rechercher des boîtes aux lettres utilisateur et des groupes de distribution. Vous pouvez également ajouter des boîtes aux lettres utilisées pour stocker un groupe Office 365 ou des informations d'équipe Microsoft. Activez la case à cocher utilisateur, groupe, équipe, cliquez sur **choisir**, puis sur **Terminer**.

        > [!NOTE]
        > Lorsque vous cliquez sur choisir les utilisateurs, les groupes ou les équipes pour spécifier des boîtes aux lettres, le sélecteur de boîtes aux lettres affiché est vide. Il s'agit d'une conception qui améliore les performances. Pour ajouter des personnes à cette liste, tapez un nom (un minimum de 3 caractères) dans la zone de recherche.
     
     - **Sites SharePoint** : cliquez sur **choisir des sites** , puis cliquez à nouveau sur choisir les **sites** pour spécifier d'autres sites SharePoint et OneDrive entreprise que vous wwant ajouter à une personne. Vous pouvez également ajouter l'URL du site SharePoint pour un groupe Office 365 ou une équipe Microsoft. Tapez l'URL de chaque site que vous souhaitez attribuer. Cliquez sur **choisir**, puis sur **Terminer**.
     - **Microsoft** teams – cliquez sur **choisir teams** , puis cliquez sur **choisir les équipes** pour afficher la liste des groupes d'équipes Microsoft dont la personne est aujourd'hui membre. Sélectionnez les équipes que vous souhaitez ajouter à la personne. Une fois sélectionné, le système identifie automatiquement & sélectionnez le site SharePoint et la boîte aux lettres de groupe associés associés à cette équipe Microsoft. Cliquez sur **choisir**, puis sur **Terminer**.
        
      > [!NOTE]
      > Pour ajouter des Microsoft teams supplémentaires, vous devez ajouter séparément la boîte aux lettres et le site SharePoint, comme indiqué ci-dessus.

Une fois que vous avez terminé le mappage des sources de données aux personnes intéressantes, vous pouvez voir le résumé du nombre total de boîtes aux lettres, de sites et d'équipes que vous venez d'ajouter. Si vous mappez des sources de données supplémentaires à des personnes intéressantes et que votre recherche par des personnes intéressantes, le mappage de document à des personnes d'intérêt persiste tout au long de l'enquête, facilitant l'Organisation des preuves ou la génération d'un rapport par des personnes intéressantes . 

## <a name="view-additional-people-of-interest-information"></a>Afficher des informations supplémentaires sur les personnes concernées

Dans l'onglet **personnes** , cliquez sur une personne que vous ADEED. Dans un menu volant, vous verrez:

- Informations de contact

  - **Nom d'affichage**: nom du Peron affiché dans le carnet d'adresses. Il s'agit généralement de la combinaison du prénom, de l'initiale du deuxième prénom et du nom de famille.
  - **Mail/SMTP**: adresse SMTP de la personne, par exemple, Jeff@contoso.onmicrosoft.com.  
  - **Titre**: fonction.
  - **Department**: nom du service dans lequel la personne travaille.
  - **Responsable**: le responsable de la personne. Le responsable reçoit les communications d'escalade de cette personne.
  
- Informations d'emplacement

  - **Ville**: ville dans laquelle se trouve la personne.
  - **État**: département ou région où se trouve la personne.
  - **Pays/région**: pays/région où se trouve la personne; par exemple, «US» ou «UK».
  - **Office**: l'emplacement du Bureau de la personne.

- État de traitement

  - **État**de l'indexation: état de l'indexation profonde des sources de données
  - **Indexation de la dernière heure de mise à jour**: horodatage du dernier déclenchement du travail d'indexation approfondie.
  - **Sources de données**: affiche le nombre de boîtes aux lettres, de sites et d'équipes mappées à la personne

- Mettre à jour l'index
    - Vous pouvez réindexer les sources de données de cette personne. 

- Afficher l'activité 

    - Vous pouvez afficher et rechercher les journaux d'activité de l'utilisateur. Pour plus d'informations, consultez la rubrique [View People of Interest Activity](view-people-of-interest-activity.md) . 
