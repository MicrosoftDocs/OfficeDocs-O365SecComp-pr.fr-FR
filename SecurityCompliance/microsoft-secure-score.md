---
title: Degré de sécurisation Microsoft
description: Décrit le score sécurisé de Microsoft 365, le mode de calcul des détails et les administrateurs de sécurité qui peuvent l'utiliser.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, Secure score, centre de sécurité, actions d'amélioration
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: fa76e2edd3f66595a47fb511881f15c07b441c77
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252304"
---
# <a name="microsoft-secure-score"></a>Degré de sécurisation Microsoft

Avec le score de sécurité Microsoft dans le centre de sécurité Microsoft 365, vous pouvez augmenter la visibilité et contrôler la position de sécurité de votre organisation. À partir d'un tableau de bord centralisé, vous pouvez surveiller et améliorer la sécurité pour vos identités, données, applications, périphériques et infrastructure Microsoft 365.

Microsoft Secure score vous offre des visualisations robustes, l'intégration à d'autres produits Microsoft, la comparaison de votre score avec d'autres sociétés, le filtrage par catégorie, et bien plus encore. Avec cet outil, vous pouvez effectuer des actions d'amélioration de la sécurité au sein de votre organisation et suivre l'historique de votre score. Le score peut également indiquer quand les solutions tierces ont résolu les actions d'amélioration recommandées.  

## <a name="how-it-works"></a>Mode de fonctionnement

Vous disposez de points pour configurer les fonctionnalités de sécurité recommandées, effectuer des tâches liées à la sécurité (telles que l'affichage des rapports) ou traiter l'action d'amélioration avec une application ou un logiciel tiers. Certaines actions sont évaluées pour une exécution partielle, comme l'activation de l'authentification multifacteur (MFA) pour vos utilisateurs. La sécurité doit toujours être équilibrée avec la convivialité et toutes les recommandations ne fonctionnent pas pour votre environnement.

## <a name="required-permissions"></a>Autorisations requises

Actuellement, pour afficher le score de sécurité Microsoft, vous devez disposer de l'un des rôles suivants dans Azure Active Directory:

* Administrateur général
* Administrateur de sécurité
* Lecteur de sécurité

## <a name="rich-experiences--additional-security-recommendations"></a>Expériences enrichies & des recommandations supplémentaires en matière de sécurité

Dans Microsoft Secure score, nous avons ajouté des recommandations d'Azure AD, de Intune et de la sécurité des applications Cloud, avec des recommandations d'Azure Security Center et de Windows Defender ATP bientôt disponibles. Nous avons également ajouté davantage de recommandations sur la sécurité Office 365. Avec des informations supplémentaires et une meilleure visibilité sur un ensemble plus large de produits et services Microsoft, vous pouvez être confiant en matière de gestion de l'intégrité de la sécurité de votre organisation. Vous pouvez également obtenir votre score à l'aide de l' [API Microsoft Graph](https://docs.microsoft.com/graph/api/resources/securescores?view=graph-rest-beta).

Pour vous aider à trouver plus rapidement les informations dont vous avez besoin, les recommandations de Microsoft sont organisées en groupes:

* Identity (état de protection de vos comptes et rôles Azure AD)
* Data (état de protection de vos documents Office 365)
* Appareil (état de protection de vos appareils; Les actions d'amélioration ATP de Windows Defender seront bientôt disponibles)
* Application (état de protection de vos applications de messagerie et de Cloud)
* Infrastructure (état de protection de vos ressources Azure; bientôt disponible)

Dans la page de présentation de Microsoft Secure score, vous pouvez voir la répartition des points entre ces groupes et les points disponibles. La page de vue d'ensemble est également l'endroit où vous pouvez obtenir une vue d'ensemble du score total, de la tendance historique de votre score de sécurité avec comparaisons de référence et des actions d'amélioration hiérarchisée qui peuvent être prises pour améliorer votre score. Vous pouvez utiliser ces données pour agir et faire des différences importantes en matière de sécurité.  

![](./media/secure-score/homepage-original.png)
*Page d'accueil M365 figure 1: page de présentation de Microsoft Secure score*

## <a name="take-action-to-improve-your-score"></a>Prendre des mesures pour améliorer votre score

L'onglet actions d'amélioration répertorie toutes les recommandations de sécurité applicables à votre client ainsi que son statut (terminé, non terminé, résolu par un tiers et ignoré). Vous pouvez rechercher, filtrer et regrouper tous les contrôles.  Le classement repose sur l'évaluation de Microsoft de la valeur de sécurité et des efforts à effectuer.

Les actions étiquetées [non notées] ne sont pas suivies par le score de sécurité Microsoft. Vous pouvez toujours prendre des mesures, mais ces dernières n'affecteront pas votre score. Si une action est suivie par le score de sécurité Microsoft à l'avenir et que vous l'avez déjà effectuée, votre score de sécurité reflète automatiquement le changement.

Lorsque vous cliquez sur une action d'amélioration, un survol s'affiche. Pour terminer l'action, vous disposez de plusieurs options:

1. Sélectionnez **afficher les paramètres** pour accéder à l'écran de configuration et effectuer les modifications. Vous obtiendrez ensuite les points que l'action vaut, visible en haut du volant. La mise à jour des points peut prendre jusqu'à 24 heures.

2. Sélectionnez **résoudre via un tiers** , car l'action d'amélioration a déjà été traitée par une application ou un logiciel tiers. Vous obtiendrez les points que l'action vaut, afin que votre score sécurisé reflète mieux votre position de sécurité globale. Si un tiers ne couvre plus le contrôle, vous pouvez marquer l'action d'amélioration comme non terminée. N'oubliez pas que Microsoft n'aura aucune visibilité quant à la satisfaction des exigences de score si l'action d'amélioration est marquée comme résolue via un tiers.

3. Sélectionnez **Ignorer** , car vous avez décidé d'accepter le risque et de ne pas appliquer l'action d'amélioration. Une fois que vous ignorez une action d'amélioration, le nombre total de points de score sécurisé que vous pouvez atteindre est réduit. Vous pouvez afficher cette action dans l'historique ou l'annuler à tout moment.

4. Sélectionnez **Review** , car l'action d'amélioration vous oblige à examiner régulièrement une partie de votre environnement pour gagner et conserver des points. Par exemple, les règles de transfert de boîtes aux lettres doivent être vérifiées chaque semaine afin de s'assurer que les données ne sont pas exportées à partir de votre réseau. Vous n'avez pas besoin d'effectuer des modifications, mais une action doit être effectuée. Si vous examinez régulièrement les règles, vous recevrez les points. Si ce n'est pas le cas, le score sera réduit.

![Page d'accueil M365](./media/secure-score/secure-score1x450.png) ![Page d'accueil M365](./media/secure-score/secure-score2x450.png)

*Figures 2 & 3: lanceurs d'actions d'amélioration*

## <a name="monitor-improvements-over-time"></a>Surveiller les améliorations au fil du temps

Vous pouvez afficher un graphique du score de votre organisation au fil du temps sous l'onglet **historique** . Cette vue inclut la moyenne globale, la moyenne du secteur et le nombre de sièges similaires, ainsi que toutes les actions effectuées dans la plage de temps sélectionnée. Vous pouvez également personnaliser une plage de dates et filtrer par catégorie.

Le score est calculé une fois par jour (environ 1:00 PST). Si vous modifiez une action mesurée, le score est automatiquement mis à jour le jour suivant. Il est également important de noter que d'autres portails indiquent des parties du score de sécurité Microsoft (par exemple, le centre de sécurité Windows Defender). Si vous effectuez une action d'amélioration et que le score augmente dans ces portails, il peut s'écouler jusqu'à 24 heures pour que le score mis à jour s'affiche dans le centre de sécurité Microsoft 365.  

## <a name="risk-awareness"></a>Sensibilisation aux risques

Microsoft Secure score est un résumé numérique de votre position de sécurité basée sur les configurations système, le comportement de l'utilisateur et d'autres mesures liées à la sécurité; il ne s'agit pas d'une mesure absolue de la probabilité de violation de votre système ou de vos données. Il représente plutôt la mesure dans laquelle vous avez adopté des contrôles de sécurité dans votre environnement Microsoft, ce qui peut vous aider à compenser le risque d'être compromis. Aucun service en ligne n'est totalement immunisé contre les violations de sécurité et le score sécurisé ne doit pas être interprété comme une garantie d'une violation de sécurité.

## <a name="we-want-to-hear-from-you"></a>Nous souhaitons être informés

Si vous rencontrez des problèmes, veuillez nous le signaler en publiant dans la communauté de [conformité Security, Privacy &](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) . Nous Surveillez la communauté et vous fournirons de l'aide.
