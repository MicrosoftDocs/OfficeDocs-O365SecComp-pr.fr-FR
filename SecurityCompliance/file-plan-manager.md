---
title: Vue d’ensemble du gestionnaire de plan de gestion de fichiers
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Le gestionnaire de plan de gestion de fichiers offre des fonctionnalités de gestion avancées pour les étiquettes et les stratégies de conservation, et fournit un moyen intégré de parcourir l’activité d’étiquette et d’étiquette vers le contenu pour l’intégralité du cycle de vie de votre contenu, de la création à la destruction finale, en passant par la collaboration, la déclaration d’enregistrement et la conservation.
ms.openlocfilehash: 377589ab0a8fd2f4c5e73a21eac3988091fa3ed3
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152896"
---
# <a name="overview-of-file-plan-manager"></a>Vue d’ensemble du gestionnaire de plan de gestion de fichiers

Le gestionnaire de plan de gestion de fichiers offre des fonctionnalités de gestion avancées pour les étiquettes et les stratégies de conservation, et fournit un moyen intégré de parcourir l’activité d’étiquette et d’étiquette vers le contenu pour l’intégralité du cycle de vie de votre contenu, de la création à la destruction finale, en passant par la collaboration, la déclaration d’enregistrement et la conservation.

![Page de plan de gestion de fichiers](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a>Accès au gestionnaire de plan de fichiers

Les deux conditions requises pour accéder au gestionnaire de plan de gestion de fichiers sont les suivantes :
- Un abonnement Office 365 Entreprise E5.
- L’affectation de l’un des rôles suivants du centre de sécurité et de conformité à l’utilisateur :
    - Gestionnaire de conservation
    - Gestionnaire de conservation en lecture seule

## <a name="default-retention-labels-and-label-policy"></a>Étiquettes de rétention par défaut et stratégie d’étiquette

S’il n’existe aucune des étiquettes de rétention dans le centre de sécurité et conformité, la première fois que vous sélectionnez **Offre Fichier** dans le volet de navigation gauche, cela crée une stratégie d’étiquette appelée **Stratégie de Publication de Gouvernance des Données par défaut**. 

Cette stratégie d’étiquette contient trois étiquettes de rétention :

- **Processus opérationnels**
- **Entreprise générale**
- **Accord Contrat**

Ces étiquettes de rétention sont uniquement configurées pour conserver le contenu, et non supprimer le contenu. Cette stratégie d’étiquette peut être publiée dans l’ensemble de votre organisation et peut être désactivée ou supprimée. 

Vous pouvez déterminer qui a ouvert le Gestionnaire d’Offre de fichiers et désactivé l’expérience de première exécution en passant en revue le journal d’audit pour les activités **Créé la stratégie de rétention** et **Créé la configuration de rétention pour une stratégie de rétention**.

> [!NOTE]
> En raison des commentaires des clients, nous avons supprimé cette fonctionnalité qui crée les étiquettes de rétention par défaut et la stratégie d’étiquette mentionnées ci-dessus. Vous seulement verrez cette stratégie et les étiquettes si vous avez utilisé le Gestionnaire d’Offre de fichiers avant le 11 avril 2019.

## <a name="navigating-your-file-plan"></a>Navigation dans votre plan de gestion de fichiers

Le gestionnaire de plan de gestion de fichiers permet d’afficher tous les paramètres de vos étiquettes et stratégies de conservation sur un même écran, en toute simplicité.

Notez que les étiquettes de conservation créées en dehors du plan de gestion de fichiers seront disponibles dans le plan de gestion de fichiers, et inversement.

Sur l’onglet des **étiquettes du plan de gestion de fichiers**, les informations et fonctionnalités supplémentaires suivantes sont disponibles :

### <a name="label-settings-columns"></a>Colonnes de paramètres des étiquettes

- **Basé sur** identifie le type de déclencheur qui marque le début de la période de conservation. Les valeurs valides sont :
    - Événement
    - Date de création
    - Dernière modification
    - Date d’étiquetage
- **Enregistrement** identifie si l’élément devient un enregistrement déclaré lorsque l’étiquette est appliquée. Les valeurs valides sont les suivantes :
    - Non
    - Oui
    - Oui (réglementaire)
- **Conservation** identifie le type de conservation. Les valeurs valides sont les suivantes :
    - Conserver
    - Conserver et supprimer
    - Supprimer
- **Destination** détermine ce qu’il advient du contenu à la fin de la période de conservation. Les valeurs valides sont les suivantes :
    - null
    - Aucune action
    - Suppression automatique
    - Examen requis (également appelé Examen de destination)

![Paramètres des étiquettes dans le plan de gestion de fichiers](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a>Colonnes des descripteurs de plan de gestion de fichiers pour les étiquettes

Vous pouvez désormais inclure plus d’informations dans la configuration de vos étiquettes de conservation. L’insertion de descripteurs de plan de gestion de fichiers dans les étiquettes permet de gérer et d’organiser plus facilement votre plan.

Pour vous aider à démarrer, le gestionnaire de plan de gestion de fichiers fournit des valeurs prédéfinies prêtes à être utilisées pour : Fonction/service, Catégorie, Type d’autorité et Mise en service/citation. Vous pouvez ajouter de nouvelles valeurs de descripteur de plan de gestion de fichiers lorsque vous créez ou modifiez une étiquette de conservation.

Voici une vue de l’étape des descripteurs de plan de gestion des fichiers lors de la création ou de la modification d’une étiquette de conservation.

![Descripteurs de plan de gestion de fichiers](media/file-plan-descriptors.png)

Voici une vue des colonnes de descripteurs du plan de gestion de fichiers dans l’onglet des étiquettes du gestionnaire de plan gestion de fichiers.

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a>Export d’étiquettes depuis votre plan de gestion de fichiers

Depuis le gestionnaire de plan de gestion de fichiers, vous pouvez exporter les détails de toutes les étiquettes de conservation dans un fichier .csv pour vous aider à fournir des évaluations périodiques de conformité aux responsables de la gouvernance des données de votre organisation.

Pour exporter toutes les étiquettes de conservation, accédez au **gestionnaire de plan de gestion de fichiers** \> **Actions de plan de gestion de fichiers** \> **Exporter les étiquettes**.

![Option d’export de plan de gestion de fichiers](media/file-plan-export-labels-option.png)

Un fichier *.csv contenant toutes les étiquettes de conservation existantes s’ouvre.

![Fichier CSV affichant toutes les étiquettes de conservation](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a>Import d’étiquettes dans votre plan de gestion de fichiers

Dans le gestionnaire de plan de gestion de fichiers, vous pouvez importer de nouvelles étiquettes en bloc mais aussi modifier des étiquettes de conservation existantes.

Pour importer de nouvelles étiquettes de conservation et mettre à jour des étiquettes de conservation existantes, accédez au **gestionnaire de plan de gestion de fichiers** \> **Actions de plan de gestion de fichiers** \> **Importer les étiquettes**.

![Option d’import de plan de gestion de fichiers](media/file-plan-import-labels-option.png)

![Option de téléchargement d’un modèle de plan de gestion de fichiers vide](media/file-plan-blank-template-option.png)

Téléchargez un modèle vide (ou démarrez à partir d’un export de votre plan de gestion de fichiers actuel).

![Modèle de plan de gestion de fichiers vide ouvert dans Excel](media/file-plan-blank-template.png)

Complétez le modèle (des informations de référence sur les valeurs valides pouvant être saisies seront bientôt disponibles).

![Modèle de plan de gestion de fichiers complété](media/file-plan-filled-out-template.png)

Chargez le modèle complété et le gestionnaire de plan de gestion de fichiers validera les entrées et affichera les statistiques d’importation.

![Statistiques d’importation de plan de gestion de fichiers](media/file-plan-import-statistics.png)

Une fois l’importation terminée, accédez à nouveau au gestionnaire de plan de gestion de fichiers pour attribuer de nouvelles étiquettes aux stratégies nouvelles ou existantes.

![Option de publication d’étiquettes](media/file-plan-publish-labels-option.png)

