---
title: Présentation du gestionnaire de conformité Microsoft
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Le gestionnaire de conformité Microsoft est un outil d'évaluation des risques gratuit basé sur un flux de travail dans le portail d'approbation de service Microsoft. Le gestionnaire de conformité vous permet de suivre, d'affecter et de vérifier les activités de conformité réglementaire liées aux services Cloud de Microsoft.
ms.openlocfilehash: a2f59eac63f8bbef98da09c2149e49ec32e56b77
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473076"
---
# <a name="microsoft-compliance-manager-preview"></a>Gestionnaire de conformité Microsoft (aperçu)

> [!IMPORTANT]
> Le Gestionnaire de conformité n’est pas disponible dans Office 365 géré par 21Vianet, Office 365 Germany, Office 365 U.S. GCC High ou Office 365 Department of Defense.

[Microsoft Compliance Manager (Preview)](https://servicetrust.microsoft.com/ComplianceManager) est un outil d'évaluation des risques gratuit basé sur un flux de travail, qui vous permet de suivre, d'affecter et de vérifier les activités de conformité réglementaire liées aux services Cloud de Microsoft. Partie de votre abonnement Microsoft 365, Office 365 ou Azure Active Directory, le gestionnaire de conformité vous aide à gérer la conformité réglementaire dans le cadre du modèle de responsabilité partagé pour les services Cloud de Microsoft. Le gestionnaire de conformité offre un tableau de bord centralisé pour l'affichage des normes, les réglementations et les détails de l'implémentation des contrôles, ainsi que les résultats des tests pour les évaluations de service Microsoft. Il inclut également des outils qui vous permettent de gérer les implémentations de contrôles personnalisés et le suivi de la conformité propres à votre organisation.

Avec le gestionnaire de conformité, votre organisation peut:
  
- Combinez les informations de conformité détaillées fournies aux auditeurs et aux autorités de réglementation concernant ses services Cloud avec votre auto-évaluation de conformité pour les normes et réglementations applicables à votre organisation. Il s'agit des normes et réglementations définies par l'Organisation internationale de normalisation (ISO), le NIST (National Institute of Standards and Technology), le HIPAA (Health Insurance Portability and Accountability Act), les données générales Règlement sur la protection (RGPD), et bien d'autres.
- Vous permet d'affecter, de suivre et d'enregistrer les activités de conformité et d'évaluation, qui peuvent aider votre organisation à atteindre vos objectifs de conformité.
- Fournir un score de conformité pour vous aider à suivre votre progression et à hiérarchiser les contrôles d'audit qui permettent de réduire l'exposition aux risques de votre organisation.
- Fournir un référentiel sécurisé pour le téléchargement et la gestion des preuves et d'autres artefacts liés à vos activités de conformité.
- Produire des rapports Microsoft Excel détaillés pour documenter les activités de conformité effectuées par Microsoft et votre organisation pour les auditeurs, les organismes de réglementation et d'autres vérificateurs de conformité.

> [!NOTE]
> Les actions client fournies dans le gestionnaire de conformité sont des recommandations; Il revient à votre organisation d'évaluer l'efficacité de ces recommandations dans son environnement réglementaire respectif avant la mise en œuvre. Les recommandations figurant dans le gestionnaire de conformité ne doivent pas être interprétées comme garantie de conformité.

## <a name="compliance-manager-relationships"></a>Relations du gestionnaire de conformité

Le gestionnaire de conformité utilise plusieurs composants pour vous aider dans vos activités de gestion de la conformité. Ces composants fonctionnent ensemble pour fournir un flux de travail de gestion complet et des rapports de conformité sans tracas pour les auditeurs.

Le diagramme illustre les relations entre les principaux composants du gestionnaire de conformité:

![Relations dans le gestionnaire de conformité version 3](media/compliance-manager-relationships.png)

## <a name="groups"></a>Groupes

Les [groupes](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#groups) sont des conteneurs qui vous permettent d'organiser des évaluations et de partager des informations communes et des tâches de flux de travail entre les évaluations qui ont le même ou les mêmes contrôles gérés par le client. Lorsque deux évaluations différentes dans le même groupe partagent le contrôle géré par le client, l'exécution des détails de l'implémentation, des tests et de l'état du contrôle est automatiquement synchronisée avec le même contrôle dans n'importe quelle autre évaluation dans le groupe. Cette opération unifie les éléments d'action attribués pour chaque contrôle au sein du groupe et réduit le travail de duplication. Vous pouvez également choisir d'utiliser des groupes pour organiser. Évaluations par année, zone, norme de conformité ou autres groupements pour faciliter l'organisation de votre travail de conformité.

## <a name="assessments"></a>Évaluations

Les [évaluations](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#assessments) sont des conteneurs qui vous permettent d'organiser les contrôles en fonction des responsabilités partagées entre Microsoft et votre organisation pour évaluer les risques de sécurité et de conformité du service Cloud. Les évaluations vous aident à implémenter les mesures de protection des données spécifiées par une norme de conformité et des normes, réglementations ou législations applicables en matière de protection des données. Elles vous aident à cerner votre position de protection et de conformité des données par rapport à la norme sélectionnée pour le service Cloud Microsoft sélectionné. Les évaluations sont effectuées par l'implémentation de contrôles inclus dans l'évaluation qui correspond à une norme de certification.

Par défaut, le gestionnaire de conformité crée les évaluations suivantes pour votre organisation:

- Office 365 ISO 27001
- Office 365 NIST 800-53
- Office 365 RGPD

Les évaluations incluent plusieurs composants:
  
- **Services dans l'étendue**: chaque évaluation s'applique à un ensemble spécifique de services Microsoft.
- **Contrôles gérés par Microsoft**: pour chaque service Cloud, Microsoft implémente et gère un ensemble de contrôles de conformité pour les normes et réglementations applicables.
- **Contrôles gérés**par le client: il s'agit de la collection de contrôles implémentée par votre organisation lorsque vous effectuez des actions pour chaque contrôle.
- **Score d'évaluation**: pourcentage de la note totale possible pour les contrôles gérés par le client dans l'évaluation. Cela vous aide à effectuer le suivi de l'implémentation des actions affectées à chaque contrôle.

## <a name="controls"></a>Contrôles

Les [contrôles](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#controls-and-actions) sont des conteneurs de processus de conformité dans le gestionnaire de conformité qui définissent la manière dont vous gérez les activités de conformité. Ces contrôles sont organisés en familles de contrôle qui s'alignent sur la structure d'évaluation des certifications ou réglementations correspondantes.

- **ID de contrôle**: nom du contrôle sélectionné à partir de la certification ou de la réglementation correspondante.
- **Titre du contrôle**: titre de l'ID de contrôle de la certification ou de la réglementation correspondante.
- **ID d'article**: ce champ est uniquement destiné aux évaluations RGPD et spécifie le numéro d'article RGPD correspondant.
- **Description**: texte de contrôle à partir de la certification ou de la réglementation correspondante. En raison des restrictions de copyright, un lien vers des informations pertinentes est affiché pour les normes ISO.

![Contrôles dans le gestionnaire de conformité version 3](media/compliance-manager-controls.png)

Il existe trois types de contrôles dans le gestionnaire de conformité, les **contrôles gérés par Microsoft**, les **contrôles gérés par le client**et les **contrôles de gestion partagés**

### <a name="microsoft-managed-controls"></a>Contrôles gérés par Microsoft

Pour chaque service Cloud, Microsoft implémente et gère un ensemble de contrôles dans le cadre de la conformité de Microsoft avec les différentes normes et réglementations. Chaque contrôle fournit des détails sur la façon dont Microsoft a implémenté le contrôle, ainsi que sur la manière et le moment où cette implémentation a été testée et validée par Microsoft et/ou par un auditeur tiers indépendant.

### <a name="customer-managed-controls"></a>Contrôles gérés par le client

Il s'agit de la collection de contrôles gérés par votre organisation. Votre organisation est responsable de l'implémentation des contrôles gérés par le client dans le cadre de votre processus de conformité pour une norme ou une réglementation donnée. Les contrôles gérés par le client sont organisés en familles de contrôle pour la certification ou la réglementation correspondante. Utilisez les contrôles gérés par le client pour mettre en œuvre les actions recommandées suggérées par Microsoft dans le cadre de vos activités de conformité. Votre organisation peut utiliser les instructions et les actions client recommandées dans chaque contrôle géré par le client pour gérer le processus d'implémentation et d'évaluation de ce contrôle.

Les contrôles gérés par le client dans les évaluations disposent également de fonctionnalités de gestion de flux de travail intégrées que vous pouvez utiliser pour gérer et suivre la progression de l'évaluation. Avec cette fonctionnalité de flux de travail, vous pouvez:

- Affecter des éléments d'action pour chaque contrôle
- Suivi des éléments d'action affectés
- Charger une preuve de l'implémentation du contrôle
- Documenter les tests et la validation du contrôle
- Marquer les éléments d'action comme étant mis en œuvre et testés

Par exemple, un responsable de la mise en conformité de votre organisation affecte un élément d'action à un administrateur informatique avec les autorisations nécessaires pour effectuer l'action recommandée. L'administrateur informatique télécharge la preuve des tâches d'implémentation (captures d'écran de paramètres de configuration ou de stratégie) et réaffecte l'élément d'action au responsable de la conformité une fois terminé. L'officier de conformité évalue la preuve collectée, teste l'implémentation du contrôle, puis enregistre la date de mise en œuvre et les résultats des tests dans le gestionnaire de conformité.

### <a name="shared-management-controls"></a>Contrôles de gestion partagés

Un contrôle partagé fait référence à tout contrôle dans lequel Microsoft et les clients partagent des responsabilités pour l'implémentation. Par exemple, les contrôles liés au filtrage du personnel, à la gestion des comptes et des mots de passe, ainsi qu'au chiffrement nécessitent des actions de la sorte de Microsoft et des clients.

## <a name="action-items"></a>points d'action

Les [éléments actions](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#controls-and-actions) sont inclus dans les contrôles gérés par le client dans le cadre de la fonctionnalité de gestion de flux de travail intégrée que vous pouvez utiliser pour gérer et suivre la progression de l'évaluation.

Les membres de votre organisation peuvent utiliser le gestionnaire de conformité pour examiner les contrôles gérés par le client à partir de toutes les évaluations pour lesquelles ils sont affectés. Lorsqu'un utilisateur se connecte au gestionnaire de conformité et ouvre le tableau de bord des **éléments d'action** , une liste d'actions qui leur sont affectées s'affiche. Selon le rôle du gestionnaire de conformité attribué à l'utilisateur, ils peuvent fournir des informations sur l'implémentation ou les tests, mettre à jour l'État ou affecter des éléments d'action.

Les contrôles de certification sont généralement mis en œuvre par une personne et testés par un autre. Par exemple, après l'exécution des éléments d'action initialement affectés à une personne pour l'implémentation, les éléments d'action sont affectés à la personne suivante pour le test et le chargement des preuves. Tout utilisateur disposant des autorisations suffisantes pour les affectations de contrôle peut affecter et réaffecter des éléments d'action. Cela permet la gestion centrale des affectations de contrôle et le routage décentralisé des éléments d'action entre les implémenteurs et les testeurs.

## <a name="permissions"></a>Autorisations

Le gestionnaire de conformité utilise un [modèle d'autorisation](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#permissions)de contrôle d'accès basé sur un rôle. Par défaut, toutes les personnes de votre organisation disposant d'un compte Azure Active Directory (Azure AD) ont un accès total et peuvent effectuer n'importe quelle action dans le gestionnaire de conformité. Une fois le contrôle d'accès basé sur un rôle implémenté par votre organisation, les utilisateurs non affectés à un rôle de gestionnaire de conformité défini reçoivent un accès invité. Le personnel de service Microsoft ne dispose pas d'un accès permanent aux données que vous entrez ou téléchargez.

Pour modifier les autorisations par défaut et implémenter un modèle de contrôle d'accès basé sur un rôle, au moins un utilisateur doit être ajouté à chaque rôle de gestionnaire de conformité. Une fois qu'un utilisateur est ajouté à un rôle, les autorisations permettant d'effectuer les actions affectées à ce rôle sont supprimées de l'ensemble d'autorisations par défaut disponible pour tous les utilisateurs. Seuls les utilisateurs configurés avec le rôle seront en mesure d'accéder au gestionnaire de conformité et d'effectuer les actions autorisées par ce rôle.

Par exemple, si vous ajoutez un utilisateur au rôle pour gérer les évaluations, seuls les membres de ce rôle peuvent gérer les évaluations. Si vous n'ajoutez pas d'utilisateur au rôle qui permet aux utilisateurs de lire les données dans les évaluations, tous les utilisateurs de votre organisation peuvent accéder au gestionnaire de conformité et lire les données dans n'importe quelle évaluation.
  
## <a name="manage-evidence"></a>Gérer les preuves

Le gestionnaire de conformité peut stocker des preuves de vos tâches d'implémentation pour tester et valider les contrôles gérés par le client. Les preuves incluent des documents, des feuilles de calcul, des captures d'écran, des images, des scripts, des fichiers de sortie de script et d'autres fichiers. Le gestionnaire de conformité reçoit automatiquement la télémétrie et crée un enregistrement de preuve pour les éléments d'action intégrés avec le score sécurisé. Toutes les données téléchargées sous forme de preuves dans le gestionnaire de conformité sont stockées aux États-Unis sur les sites de stockage cloud de Microsoft. Ces données sont répliquées dans les régions Azure situées en Asie du sud-est et en Europe de l'Ouest.

## <a name="templates"></a>Modèles

Le gestionnaire de conformité fournit des [modèles](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#templates) préconfigurés pour les évaluations et vous permet de créer des modèles personnalisés pour les contrôles gérés par le client pour vos besoins en matière de conformité. Les nouveaux modèles sont créés en important des informations de contrôles à partir d'un fichier Excel, ou vous pouvez créer un modèle à partir d'une copie d'un modèle existant.

Les modèles préconfigurés inclus dans le gestionnaire de conformité sont les suivants:
 
- [ISO 27001:2013](https://www.iso.org/obp/ui/#iso:std:iso-iec:27001:ed-2:v1:en)
- [ISO 27018:2019](https://www.iso.org/obp/ui/#iso:std:iso-iec:27018:ed-2:v1:en)
- [NIST 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-4/final)
- [NIST 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)
- [Infrastructure NIST Cybersecurity (CSF)](https://www.nist.gov/cyberframework)
- [Matrice de contrôle Cloud CSA (Cloud Security Alliance) 3.0.1](https://cloudsecurityalliance.org/working-groups/cloud-controls-matrix/#_overview)
- [Livret de sécurité des informations sur les institutions financières fédérales (FFIEC)](https://ithandbook.ffiec.gov/it-booklets/information-security.aspx) 
- [HIPAA](https://www.hhs.gov/hipaa/for-professionals/index.html) / [Hi-Tech](https://www.hhs.gov/hipaa/for-professionals/special-topics/hitech-act-enforcement-interim-final-rule/index.html)
- [FedRAMP modéré](https://www.fedramp.gov/documents/)
- [RGPD de l'Union européenne](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32016R0679&from=EN)

## <a name="compliance-score"></a>Score de conformité

Le [score de conformité](compliance-score-methodology.md) est un composant essentiel du gestionnaire de conformité qui permet à votre organisation de comprendre et de gérer la conformité. Comme le [score de sécurité Microsoft](microsoft-secure-score.md), le score de conformité est un système de score basé sur un comportement pour les activités liées à la protection des données, à la confidentialité et à la sécurité dans votre organisation. Le score de conformité pour une évaluation est une expression de conformité avec une norme ou une réglementation donnée. Plus le score numérique est élevé, plus la position de conformité pour l'évaluation est bonne. Comprendre la méthodologie de notation de conformité est cruciale pour définir la priorité des actions de contrôle gérées par le client.
  
> [!IMPORTANT]
> Le Score de conformité ne reflète pas forcément la conformité absolue de l’organisation avec une norme ou une réglementation spécifique. Il indique les contrôles que vous avez adoptés pour réduire les risques liés à la protection des données personnelles. Aucun service ne peut garantir que vous êtes en conformité avec une norme ou une réglementation. Le Score de conformité ne doit donc en aucun cas être considéré comme une garantie du respect des réglementations en vigueur.

## <a name="secure-score-integration"></a>Intégration de la note sécurisée

Le gestionnaire de conformité est intégré à [Microsoft Secure score](microsoft-secure-score.md) pour appliquer automatiquement un crédit de score sécurisé au score de conformité pour les éléments d'action synchronisés. Cette opération peut être configurée pour des éléments d'action individuels et fournit une mise à jour continue entre les éléments.

Par exemple, vous avez une exigence relative à la sécurité pour activer Azure Rights Management dans votre organisation, qui s'applique également à un élément d'action de conformité. Lorsque Azure Rights Management est activé et traité par le score sécurisé, le gestionnaire de conformité reçoit la notification de la mise à jour et le score de l'élément d'action est automatiquement mis à jour avec le crédit d'achèvement.

## <a name="ready-to-get-started"></a>Vous êtes prêt ?

Commencez à [utiliser le gestionnaire de conformité](working-with-compliance-manager.md) pour gérer les activités de conformité réglementaire de votre organisation.

## <a name="resources"></a>Ressources

- [Guide interactif: évaluer et améliorer vos contrôles de protection des données avec le gestionnaire de conformité](https://content.cloudguides.com/guides/Compliance%20Manager)
- [Communauté technique Microsoft sur la sécurité, la confidentialité et la conformité](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/ct-p/SecurityPrivacyCompliance)
