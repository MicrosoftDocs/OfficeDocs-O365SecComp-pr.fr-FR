---
title: Contrôles du personnel Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: "Résumé: vue d'ensemble des pratiques de filtrage du personnel de Microsoft pour Office 365."
ms.openlocfilehash: 126be117c790e4d8fc0328ee2dab6b97d516ab88
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2019
ms.locfileid: "30091076"
---
# <a name="office-365-personnel-controls"></a>Contrôles du personnel Office 365 

Le filtrage du personnel, qui est le processus de révision et de validation du comportement et de l'État antérieurs d'une personne, est un contrôle de limitation important pour empêcher le compromis du service Office 365. Tandis que le comportement antérieur n'est pas un Predictor parfait du comportement futur d'une personne, il permet d'identifier les acteurs potentiels. La norme de filtrage du personnel de Microsoft s'applique à tous les employés de Microsoft, les apprentis et le personnel concerné impliqué dans le développement, l'exploitation ou la livraison de services en ligne à des clients du secteur public ou du secteur public. Les normes de filtrage pour les environnements nationaux de Cloud qui ne sont pas gérés par Microsoft sont définies par le personnel du partenaire d'exploitation pour chaque environnement spécifique.

## <a name="microsofts-personnel-screening-standard"></a>Norme de filtrage du personnel de Microsoft

Les pratiques de dépistage du personnel de Microsoft pour Office 365 sont alignées sur les contrôles des normes de l'entreprise et de l'Institut NIST (National Institute of Standards and Technology) pour le filtrage du personnel. Le personnel Microsoft qui a besoin d'accéder aux éléments suivants est soumis à la norme de filtrage du personnel de Microsoft:
- Accès physique aux centres de donnés, aux lieux de connexion, aux salles sécurisées, aux cages, aux racks de serveurs ou aux sites de périphérie qui fournissent l'infrastructure qui prend en charge les services en ligne pour les clients du secteur public ou du nuage.
- Accès logique aux données client du Cloud ou du secteur commercial fourni par des environnements gérés spécifiques.
    - Accès de gestion réseau aux appareils et services qui transportent ou stockent des données client dans le cloud public ou commercial.

Les événements spécifiques au personnel qui déclenchent des exigences de filtrage sont les suivants:
- Nouveau personnel Microsoft placé dans les rôles où le filtrage est une exigence définie.
- Le personnel Microsoft interne transfère ou passe à un rôle existant qui inclut actuellement le filtrage en tant que Configuration requise.
- Les rôles existants qui modifient l'étendue pour inclure le filtrage en tant que spécification définie.

## <a name="screening-enforcement-criteria"></a>Critères d'application du filtrage

Pour vous assurer que seul le personnel approuvé a accès aux données du client ou aux environnements qui nécessitent un filtrage, les critères de contrainte suivants s'appliquent:

**Environnements Cloud pour les États-Unis uniquement**:
- L'accès aux données du client ou aux environnements qui nécessitent un filtrage ne doit être autorisé qu'une fois la finalisation terminée et les exigences de filtrage transmises.
- Les membres du personnel Microsoft qui n'ont plus besoin d'accéder aux données du client ou aux environnements connexes doivent avoir accès supprimé lors de la fermeture de Microsoft ou de la migration vers un nouveau rôle.
- Les employés de Microsoft doivent laisser des cartes à puce d'environnement à écran avec gestion avant de quitter les États-Unis.

**Environnements nationaux de Cloud**:
- Un opérateur tiers ou un personnel de confiance des données est responsable de la gestion et de l'application de l'accès aux environnements nationaux de Cloud.

Dans les environnements de services Cloud de Microsoft, l'accès est restreint en fonction du rôle d'une personne et du type de données impliquées, comme indiqué dans le tableau ci-dessous. Le personnel qualifié ou non qualifié qui se trouve physiquement en dehors des États-Unis n'est pas autorisé à avoir accès aux données du client au sein d'un Cloud américain. L'accès aux environnements de Cloud nationaux est restreint de sorte que le personnel de Microsoft ne dispose pas d'un accès technique aux données client, ni aux systèmes contenant des données client, sans approbation de l'opérateur tiers ou du groupe de confiance des données.

| Rôle | Accès aux données client | Accès aux données système |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|---------------------------------|
| Personnel qualifié situé physiquement aux États-Unis | Tolérance | Tolérance |
| Personnel qualifié physiquement situé en dehors des États-Unis | Non autorisé | Tolérance |
| Accès aux exceptions internationales pour le personnel de Microsoft: permet un accès logique au personnel de Microsoft qui ne réside pas dans le pays où les données du gouvernement ou du client commercial sont inActives. | Non autorisé | Tolérance |
| Personnel non qualifié (personnel non-filtré qui requiert une escorte par le personnel qualifié) | Autorisé avec autorisation | Autorisé avec supervision de l'escorte |


## <a name="microsoft-pre-employment-screening"></a>Filtrage avant l'emploi de Microsoft

Lorsque la loi locale le permet, le service de sécurité global de Microsoft effectue un filtrage avant l'emploi. Il s'agit d'une enquête en arrière-plan formelle qui inclut les critères suivants:
- Une vérification (par exemple, pour une précision et une exactitude) du curriculum vitae du demandeur.
- Confirmation des qualifications académiques et professionnelles
- Enquête sur toute perte d'informations d'identification professionnelles
- Vérification des trois employeurs précédents
- Vérification des enregistrements de police pour la conviction crimes
- Confirmation de l'identité auprès d'une identification publiée par un gouvernement
- Vérification du crédit, le cas échéant

La redirection périodique et/ou des vérifications d'arrière-plan supplémentaires peuvent être nécessaires pour certaines fonctions de gestion, de sécurité ou d'autres rôles, y compris mais sans s'y limiter, les employés basés aux États-Unis dans les rôles qui nécessitent un accès aux données client. Pour le personnel éventuel, le contrat avec le tiers spécifie les exigences de Microsoft en matière de filtrage qui doit être effectuée par le tiers. Pour les vérifications en arrière-plan, la société tierce est chargée de vérifier qu'un contrôle d'arrière-plan a été effectué. Les résultats de la vérification en arrière-plan sont généralement reçus par courrier électronique auprès du service des ressources humaines de tiers. Les employés de l'équipe internationale peuvent être exemptés du processus de filtrage en arrière-plan en raison de la législation en vigueur dans les pays qui interdisent les contrôles en arrière-plan.

## <a name="microsoft-employment-screening"></a>Dépistage de l'emploi Microsoft
Depuis 2004, Microsoft a demandé aux personnes de transmettre un écran de l'enregistrement pénal sur sept ans pour felonies et Misdemeanors, et de vérifier leur histoire de l'éducation et de l'emploi, dans le cadre de l'inspection préalable à l'emploi aux États-Unis pour les employés et les apprentis.

Aux États-Unis, avant d'affecter un employé Microsoft ou un sous-traitant affecté par Microsoft pour fournir des services associés à Office 365, Microsoft mènera et fera en sorte que son sous-traitant effectue une vérification en arrière-plan consistant en une sécurité sociale. suivi numérique et vérification d'enregistrement criminel. Les données de cette vérification en arrière-plan sont utilisées comme facteur dans la décision d'embauche. Le contrôle des enregistrements criminelles comprend un contrôle d'enregistrement fédéral, de l'État et du comté de sept ans crimes et délits (le cas échéant).

En tant que condition d'emploi, au moment de la location, tous les employés de Microsoft sont tenus de signer la confidentialité et les contrats de non-divulgation, et de vérifier qu'ils ont examiné le Guide de l'employé Microsoft.

## <a name="microsoft-cloud-background-check"></a>Vérification en arrière-plan Microsoft Cloud
Une vérification en arrière-plan de Microsoft Cloud est requise pour que les candidats soient embauchés en tant qu'employés fournissant des services Office 365 aux États-Unis. Les employés Microsoft aux États-Unis ayant accès aux données client doivent suivre le processus de vérification en arrière-plan de Microsoft Cloud, qui est requis par tous les services Office 365. En dehors des États-Unis, le processus varie. Par exemple, le Cloud Microsoft pour l'Allemagne utilise un modèle d'approbation de tiers de données, qui est conçu pour s'assurer que le tiers de confiance des données (une société allemande), et non Microsoft, contrôle l'accès aux données client. Le Cloud Microsoft en Allemagne est fourni par des centres de données en Allemagne, et les centres d'opérations (OC) contenant le personnel technique du client tiers de données sont également en Allemagne. Les installations de centre de données et OC sont gérées, gérées et contrôlées par le tiers de confiance.

Le tableau suivant répertorie les vérifications effectuées dans le cadre de la vérification en arrière-plan de Microsoft Cloud.

| Analyser | Description |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recherche de numéro de sécurité sociale | Vérifie que le numéro de sécurité sociale fourni est valide. |
| Vérification du casier judiciaire | Les enregistrements criminels sur sept ans vérifient la crimes et délits infractions aux niveaux État, comté et local, selon le cas, au niveau fédéral. |
| Liste de contrôle des avoirs étrangers | Département de la liste de trésorerie des personnes et organisations avec lesquelles les citoyens des États-Unis et les résidents permanents ne sont pas autorisés à faire des affaires. |
| Liste du Bureau de l'industrie et de la sécurité | Département de commerce des individus et des entités exclus de la vente d'activités d'exportation. |
| Le Bureau des contrôles commerciaux de la défense est débarré de la liste des personnes (*ajouté le 1er juillet 2010*) | Département d'état de la liste des individus et des entités exclus des activités d'exportation liées à l'industrie de la défense. |


Les résultats de la vérification en arrière-plan de Microsoft Cloud sont stockés dans notre base de données Employee, qui est connectée à nos systèmes de contrôle d'accès de centre de données. Si la vérification en arrière-plan de Microsoft Cloud expire et que l'employé ne le renouvelle pas, l'accès aux services Office 365 est révoqué et n'est plus disponible tant que la vérification en arrière-plan de Microsoft Cloud n'est pas terminée. Lorsque la relation d'embauche avec Microsoft se termine, tout accès au centre de contenu existant est immédiatement révoqué.

La citoyenneté des États-Unis est vérifiée pour tous les employés disposant d'un accès physique ou logique aux services publics Office 365 États-Unis. Pour vérifier la citoyenneté, les employés et/ou les candidats aux nouveaux employés se joignent à un délégué de citoyenneté américain formé pour vérifier la documentation de la citoyenneté américaine. Les employés ou les candidats à d'autres embauches doivent apporter la documentation requise et signer un formulaire d'attestation lors d'une réunion avec le délégué de citoyenneté pour leur région. La réunion doit être réalisée en personne. Une fois que la personne a rempli le délégué de citoyenneté et fourni la documentation et les signatures nécessaires, le délégué de citoyenneté transfère une copie des documents aux opérations de personnel Microsoft qui soumettent la copie à enregistrer.

Le personnel disposant d'un accès logique au Cloud communautaire du gouvernement américain d'Office 365 ou à un accès logique ou physique aux offres du gouvernement des États-Unis d'Azure doit être conforme aux exigences du gouvernement fédéral des [informations sur la justice pénale du FBI Services](https://www.fbi.gov/services/cjis) (CJIS), y compris le tri du personnel. Le filtrage CJIS dans la prise en charge du service de gouvernement américain Office 365 comprend un contrôle de fond pénal basé sur des empreintes digitales, lequel est jugé par le candidat à l'Agence de système CJIS dans les [États qui ont été](https://blogs.office.com/2013/10/23/california-and-microsoft-sign-cjis-security-policy-agreement/) inclus dans Microsoft Online. Services support CJIS.
