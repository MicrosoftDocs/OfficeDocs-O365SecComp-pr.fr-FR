---
title: Gestion des dépositaires dans un cas avancé eDiscovery
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
ms.openlocfilehash: d9806ecbc23f46ee2d39f8d7e6be07af0d6a83e8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151616"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-case"></a>Gestion des dépositaires dans un cas avancé eDiscovery

L’onglet dépositaires dans Advanced eDiscovery contient la liste de tous les dépositaires qui ont été ajoutés à l’incident. Une fois que vous avez ajouté des dépositaires à un cas, les détails de chaque dépositaire sont automatiquement collectés à partir d’Azure Active Directory et peuvent être consultés dans Advanced eDiscovery.

![Gestion des dépositaires](../media/CustodianDetails.PNG)

## <a name="view-custodian-details"></a>Afficher les détails du dépositaire

Pour afficher les détails relatifs à un dépositaire, cliquez sur celui-ci dans la **** liste sous l’onglet dépositaires. Une page de menu volant s’affiche et contient les informations suivantes sur le dépositaire:

- Informations de contact

  - **Nom d’affichage** : nom affiché dans le carnet d’adresses pour le dépositaire. Il s’agit généralement de la combinaison du prénom du dépositaire, de l’initiale du deuxième prénom et du nom de famille.
  
   - **Mail/SMTP** : adresse SMTP principale pour le dépositaire, par exemple, brianj@contoso.onmicrosoft.com. Notez que le nom d’utilisateur principal (UPN) du dépositaire est également indiqué.

  - **Title** -fonction du dépositaire.

  - **Department** : nom du service dans lequel le dépositaire travaille.

  - **Responsable** : le responsable du dépositaire. Le responsable désigné recevra toutes les communications d’escalade de ce dépositaire.
  
- Informations d’emplacement

  - **Ville** -ville où se trouve le dépositaire.

  - **Département** : État ou province dans l’adresse du dépositaire.

  - **Pays/région** : pays/région où se trouve le dépositaire.

  - **Office** : l’emplacement de l’Office dans le lieu d’activité du dépositaire.

- Informations sur les cas

  - **Hold Status** : indique si le dépositaire a été mis en attente. 

  - **Statut**de la communication: indique si un avis de mise en attente a été émis pour le dépositaire. Si le dépositaire a reçu une notification, la valeur de cette propriété est **publiée**. Si le dépositaire n’a pas reçu de notification, son statut est non **publié**. 

  - **Status** : état du dépositaire dans le cas. L’état **actif** indique que le dépositaire fait partie de l’affaire. Si un dépositaire est émis à partir d’un incident, le statut passe à **lancé**. 

- Sources de données et informations d’indexation

    - **Sources de données** : affiche le nombre et le type de sources de données (boîtes aux lettres, sites et équipes) qui sont associées au dépositaire et font partie de la demande.

    - Date et heure de **mise à jour** de l’index: indique l’heure et la date de la dernière déclenchement du travail d’indexation avancé. Cette propriété indique également quand le processus d’indexation avancé est en cours.


## <a name="edit-a-custodian"></a>Modifier un dépositaire

Lors de l’évolution de votre cas, vous pouvez découvrir qu’il peut y avoir des sources de données supplémentaires pertinentes pour un dépositaire spécifique & votre cas. Dans d’autres scénarios, vous souhaiterez peut-être supprimer certaines sources de données qui ont été vérifiées et considérées comme non pertinentes.

Pour mettre à jour les sources de données associées à un dépositaire, procédez comme suit:

1. Accédez à **eDiscovery _GT_ Advanced eDiscovery** et ouvrez le cas.
  
2. Cliquez sur **** l’onglet dépositaires.
  
3. Sélectionnez un dépositaire dans la liste, puis cliquez sur **modifier** sur la page de menu volant.

    ![Modifier des sources de données](../media/EditCustodianDataSource.PNG)
  
4. Cliquez sur l’onglet **choisir les sources de données** pour modifier les paramètres de la boîte aux lettres Exchange du dépositaire et du compte OneDrive, puis cliquez sur choisir les sources de **données**.
  
5. Cliquez sur l’onglet **Sélectionner des sources de données supplémentaires** pour ajouter ou supprimer des équipes, des groupes SharePoint ou des boîtes aux lettres Exchange associées au dépositaire. 

    Pour plus d’informations sur les sources de données associées à un dépositaire, voir «étape 3: associer des sources de données supplémentaires à un dépositaire» dans [Ajouter des dépositaires à un cas](add-custodians-to-case.md#step-3-associate-additional-data-sources-to-a-custodian). 
  
6. Cliquez sur **Placer** des conservations privatives pour activer ou désactiver la conservation pour le dépositaire.

## <a name="resolve-custodian-processing-errors"></a>Résoudre les erreurs de traitement des dépositaires

Dans la plupart des flux de travail eDiscovery pour les enquêtes juridiques, un sous-ensemble des données d’un dépositaire est recherché une fois que le dépositaire est ajouté à un cas juridique. En raison de la taille des fichiers très volumineux ou d’une éventuelle altération des données, certains éléments des sources de données associées à un dépositaire peuvent être partiellement indexés. À l’aide de la fonctionnalité d' [indexation avancée](indexing-custodian-data.md) dans la découverte électronique avancée, la plupart des éléments indexés partiellement peuvent être automatiquement corrigés en réindexant ces éléments à la demande.

Lorsqu’un dépositaire est ajouté à un cas, les données situées dans les sources de données associées au dépositaire sont automatiquement réindexées (par le processus d’indexation avancé). Cela signifie que vous pouvez laisser les données sur place au lieu de devoir les télécharger et les corriger, puis les Rechercher hors connexion). Toutefois, pendant le cycle de vie d’un cas juridique, de nouvelles sources de données peuvent être associées à un dépositaire. Dans ce cas, vous réindexez les données du dépositaire en réexécutant le processus d’indexation avancé afin de corriger les éléments partiellement indexés et de mettre à jour l’index des données du dépositaire.

Pour déclencher le processus de réindexation afin d’adresser des éléments partiellement indexés:

1. Accédez à **eDiscovery _GT_ Advanced eDiscovery** et ouvrez le cas.

2. Cliquez sur l' **onglet dépositaires**, puis sélectionnez un dépositaire dont les données doivent être réindexées. 

3. Sur la page de la fenêtre volante, cliquez sur **mettre à jour l’index**.

   Une boîte de dialogue s’affiche, indiquant que le travail d’index a été créé.

La réindexation des données du dépositaire est un processus long; le travail correspondant créé est nommé réindexation des **données des dépositaires**. Vous pouvez suivre l’avancement sous l’onglet **travaux** ou sous l’onglet **dépositaires** en surveillant le statut dans la colonne État du travail d' **indexation** .

Pour plus d’informations, reportez-vous aux rubriques suivantes :

- [Utiliser les erreurs de traitement](processing-data-for-case.md)

- [Gérer les tâches](managing-jobs-ediscovery20.md)

## <a name="release-a-custodian-from-a-case"></a>Publication d’un dépositaire à partir d’un cas

Un dépositaire est publié dans les situations où un cas est fermé, le dépositaire n’est plus tenu de conserver le contenu d’un cas ou lorsque le dépositaire est considéré comme n’étant plus pertinent pour le cas. 

Si vous libérez un dépositaire après la publication d’une notification de mise en attente, un avis de publication est envoyé au dépositaire. De plus, toutes les suspensions placées sur les sources de données qui ont été associées au dépositaire sont supprimées. Si le dépositaire a été placé sur un *blocage silencieux*, où il n’a pas reçu de notifications de mise en attente légale, un avis de publication ne sera pas envoyé, mais les blocages placés sur les sources de données associées à ce dépositaire sont supprimés.

Pour libérer un dépositaire: 

1. Accédez à **eDiscovery _GT_ Advanced eDiscovery** et ouvrez le cas.

2.  Accédez à l' **** onglet dépositaires.

3.  Cliquez sur l' **onglet dépositaires**, puis sélectionnez le dépositaire qui est lancé à partir du cas.

4. Sur la page flyout, cliquez sur **libérer le dépositaire**.

   Une page d’avertissement s’affiche pour expliquer que si une conservation est placée sur une source de données associée au dépositaire, la conservation sera supprimée et les autres conservations associées à un autre cas de découverte électronique avancée continueront à s’appliquer. Cela inclut d’autres types de fonctionnalités de conservation et de rétention dans Office 365 (par exemple, une stratégie de rétention Office 365).

5. Cliquez sur **Oui** pour confirmer le lancement du dépositaire. 

    Notez que l’état de cet utilisateur dans **** l’onglet dépositaires est défini **** sur Released et que le **statut de blocage** sur la page flyout est modifié sur **false**. 

> [!NOTE]
> Un dépositaire peut être impliqué simultanément dans plusieurs cas juridiques. Lorsqu’un dépositaire est émis à partir d’un cas, les conservations et notifications dans les autres matières ne seront pas affectées.

## <a name="bulk-edit-custodians"></a>Modifier en bloc des dépositaires

Vous pouvez utiliser l’éditeur en bloc pour modifier plusieurs dépositaires en même temps. Pour ce faire, sélectionnez au moins deux dépositaires dans l’onglet **dépositaires** pour afficher l’éditeur en bloc, puis cliquez sur l’une des tâches.

![Page volante permettant de modifier les paramètres de plusieurs dépositaires](../media/AeDBulkEditCustodians.png)