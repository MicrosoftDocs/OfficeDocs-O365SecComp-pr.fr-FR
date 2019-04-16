---
title: Afficher l’utilisation d’étiquette grâce à la page Analyse des étiquettes
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Après avoir créé vos étiquettes de rétention et vos étiquettes de sensibilité, vous souhaiterez voir comment ils sont utilisés au sein de votre client. Les portails Centre de conformité Microsoft 365 et Centre de sécurité Microsoft 365 sont dotés d’une page intitulée Analyse des étiquettes. Elle indique les étiquettes les plus utilisées et leurs types d’applications.
ms.openlocfilehash: d0289eb79dca04262ef61d58a8e622ae6d7cbe93
ms.sourcegitcommit: 54d58da1777eb83adb82826d1bb1adb94903c8e1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "30994840"
---
# <a name="view-label-usage-with-label-analytics"></a>Afficher l’utilisation d’étiquette grâce à la page Analyse des étiquettes

Après avoir créé vos étiquettes de rétention et vos étiquettes de sensibilité, vous souhaiterez voir comment ils sont utilisés au sein de votre client. Les portails Centre de conformité Microsoft 365 et Centre de sécurité Microsoft 365 sont dotés d’une page intitulée Analyse des étiquettes. Elle indique les étiquettes les plus utilisées et leurs types d’applications.

Par exemple, avec analytique étiquette, vous pouvez afficher:

- Le nombre total de rétention étiquettes et les étiquettes de sensibilité appliquées au contenu.
- Les étiquettes supérieures et le nombre de compte pour lequel chaque étiquette a été appliquée.
- Les emplacements où les étiquettes sont appliquées et le nombre pour chaque emplacement.
- Compter le nombre de fichiers et des dossiers pour lesquels l’étiquette de rétention a été modifiée ou supprimée.

Vous trouverez analytique étiquette dans la [centre de conformité de Microsoft 365](https://compliance.microsoft.com/labelanalytics) ou [centre de sécurité Microsoft 365](https://security.microsoft.com/labelanalytics) > **Classification**  >  ** Étiquettes analytique**.

![Page analytique étiquette](media/label-analytics-page.png)

## <a name="sensitivity-label-usage"></a>Étiquettes de niveau de confidentialité

Les données sur l’utilisation de la sensibilité étiquette sont extraite des rapports pour Azure Information Protection-pour plus d’informations, voir [Central de création de rapports de Protection Informations Azure](https://docs.microsoft.com/fr-FR/azure/information-protection/reports-aip).

Notez que les rapports de Protection d’Informations Azure Information ont des[conditions préalables](https://docs.microsoft.com/fr-FR/azure/information-protection/reports-aip#prerequisites-for-azure-information-protection-analytics) qui s’appliquent également à l’analytique d’étiquette sur les étiquettes de niveau de confidentialité dans le centre de conformité de Microsoft 365 et centre de sécurité Microsoft 365. Par exemple, vous avez besoin d’un abonnement Azure qui inclut le journal Analytique, car ces rapports sont le résultat de l’envoi d’informations d’événements d’audit d’une protection à partir de scanneurs et Azure Information Protection clients vers un emplacement centralisé basé sur Azure journal Service Analytique.

Usage d’étiquettes de niveau de confidentialité:

- Il n’existe aucune latence dans les données. Il s’agit d’un rapport en temps réel.
- Pour afficher le nombre de chaque étiquette supérieure, pointez sur le graphique à barres et lire l’info-bulle qui s’affiche.
- Le rapport indique où les étiquettes de niveau de confidentialité sont appliquées par application (tandis que les étiquettes de rétention sont affichées par emplacement).

![Rapport d’usage d’étiquettes de niveau de confidentialité](media/sensitivity-label-usage-report.png)

## <a name="retention-label-usage"></a>Usage d’étiquette de rétention

Ce rapport affiche un aperçu rapide de ce que sont les étiquettes supérieures et où elles sont appliquées. Pour plus d’informations sur l’intitulé de contenu dans SharePoint et OneDrive, voir [Afficher l’activité des étiquettes pour les documents](view-label-activity-for-documents.md).

Usage d’étiquette de rétention:

- Les données sont regroupées de manière hebdomadaire, aussi cela peut prendre jusqu'à sept jours pour que les données s’affichent dans le rapport.
- Pour afficher le nombre de chaque étiquette supérieure, pointez sur le graphique à barres et lire l’info-bulle qui s’affiche.
- Le rapport indique où les étiquettes de rétention sont appliquées par emplacement (tandis que les étiquettes de sensibilité sont affichées par application).
- Pour les étiquettes de rétention, il s’agit d’une synthèse des données à tout-moment dans votre client ; elles ne sont pas filtrées pour une plage de dates spécifique. En revanche, l’[étiquette d’activité Explorer](view-label-activity-for-documents.md) affiche les données 30 derniers jours uniquement.

![Rapport d’usage d’étiquette de rétention](media/retention-label-usage-report.png)

## <a name="view-all-content-with-a-specific-retention-label"></a>Afficher tout le contenu portant une étiquette de rétention spécifique

Dans le rapport d’utilisation d’étiquette de rétention, vous pouvez rapidement explorer tout le contenu associé à cette étiquette appliquée. (Notez que nous travaillons actuellement sur cette fonctionnalité, afin que le processus prenne plus d’étapes pour afficher tout le contenu étiqueté).

Tout d’abord, choisissez **Afficher les détails** en bas du rapport.

![Option Afficher les détails en bas de rapport d’utilisation d’étiquette de rétention](media/retention-label-usage-view-details.png)

Puis choisissez une étiquette de rétention > **Explorer les éléments** dans le volet droit.

![Explorer l’option éléments dans le volet droit](media/retention-label-usage-explore-items.png)

Pour cette étiquette, vous pouvez choisir l’onglet**activité**pour consulter un nombre d’éléments associé à cette étiquette selon l’emplacement.

![Onglet activité pour une étiquette de rétention](media/retention-label-usage-activity-tab.png)

Vous pouvez également choisir l’onglet**éléments avec cette étiquette**. Ensuite, vous pouvez explorer des emplacements spécifiques :

- Pour Exchange Online, consultez la liste de boîtes aux lettres avec le nombre d’éléments étiquetés dans chaque boîte aux lettres.
- Pour SharePoint Online et OneDrive Entreprise, vous voyez une liste de collections de sites et les comptes OneDrive avec le nombre d’éléments étiquetés dans chaque emplacement.

Lorsque vous choisissez une collection de boîte aux lettres ou un site, vous pouvez afficher une liste d’éléments associé à cette étiquette rétention dans cet emplacement.

![Les éléments de cet onglet d’étiquette affichant tous les éléments comportant cette étiquette rétention](media/retention-label-usage-content-explorer.png)

## <a name="permissions"></a>Autorisations

Pour afficher analytique étiquette, vous devez être affecté parmi les rôles suivants dans Azure Active Directory :

- Administrateur général
- Administrateur de conformité
- Administrateur de sécurité
- Lecteur Sécurité

Par ailleurs, notez que ces rapports utilisent Azure Monitor pour stocker les données dans un espace de travail journal Analytique appartenant à votre organisation. Par conséquent, l’utilisateur doit être ajouté en tant qu’un lecteur d’à l’espace de travail Azure surveillance que suspensions données-pour plus d’informations, voir [Autorisations nécessaires à analytique Protection Informations Azure](https://docs.microsoft.com/fr-FR/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).

