---
title: Secure Score Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Vous avez jamais étonnant quelle est la sécurisation de votre organisation dans Office 365? Le score de sécurité est là pour vous aider. Le score sécurisé analyse la sécurité de votre organisation en fonction de vos activités normales et des paramètres de sécurité dans Office 365 et affecte un score.
ms.openlocfilehash: dd0dc87910853eba9f2ec3ec6752e857462b46e5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220354"
---
# <a name="office-365-secure-score"></a>Secure Score Office 365

**Résumé** Vous avez jamais étonnant quelle est la sécurisation de votre organisation dans Office 365? Le score de sécurité est là pour vous aider. Le score sécurisé analyse la sécurité de votre organisation en fonction de vos activités normales et des paramètres de sécurité dans Office 365 et affecte un score. Lisez cet article pour obtenir une vue d'ensemble du score sécurisé et de la façon dont vous pouvez l'utiliser.
  
## <a name="how-to-get-to-secure-score"></a>Comment obtenir le score sécurisé

Si votre organisation dispose d'un abonnement qui inclut [office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 business](https://docs.microsoft.com/microsoft-365/business/)ou Office 365 Business Premium, et que vous disposez des [autorisations nécessaires](#required-permissions), vous pouvez afficher le score de sécurité de votre organisation en visitant le site [https://securescore.office.com](https://securescore.office.com). 

Vous pouvez également visiter le centre de sécurité & Compliance Center ([https://protection.office.com](https://protection.office.com)), où vous trouverez un widget de score sécurisé qui vous fournit votre score actuel.

![Widget de score sécurisé](media/SecureScoreWidget-o365.png)

Le widget inclut un lien vers votre tableau de bord de score sécurisé.

![Tableau de bord de score sécurisé](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a>Fonctionnement

Le score de sécurité détermine les services Office 365 que vous utilisez (par exemple, OneDrive, SharePoint et Exchange), puis compare vos paramètres et activités à une base établie par Microsoft. Vous obtiendrez un score en fonction de la manière dont votre organisation est bien alignée sur les meilleures pratiques en matière de sécurité. Vous obtiendrez également des recommandations sur les étapes que vous pouvez suivre pour améliorer le score de votre organisation. 
  
![File d'attente des actions dans l'outil de score sécurisé Office 365](media/SecureScore-ActionsToTake.png)
  
Le score de sécurité calcule votre score en fonction des services que vous avez achetés. Par exemple, si vous avez acheté uniquement un plan Exchange Online, vous ne serez pas remarqué pour les fonctionnalités de sécurité de SharePoint Online. Le dénominateur du score est la somme de toutes les lignes de base pour les contrôles qui s'appliquent aux produits que vous avez achetés. Le numérateur est la somme de tous les contrôles pour lesquels vous avez terminé, ou partiellement terminé, les actions à effectuer pour répondre à ce contrôle.

Développez une action pour découvrir les étapes à suivre, les menaces qui vous aideront à vous protéger et le nombre de points que votre score augmentera une fois que vous aurez suivi la recommandation.
  
![Action étendue dans l'outil de score de sécurité d'Office 365](media/SecureScore-DetailedActionToTake.png)
  
Pour voir l'impact de vos actions sur la sécurité de votre organisation, sélectionnez l'onglet analyseur de **score** et examinez votre historique. 
  
![Onglet analyseur de score de l'outil de score sécurisé Office 365](media/SecureScore-ScoreAnalyzer-7days.png)
  
Sous le graphique, vous verrez une liste de scores et d'actions par catégorie. 
  
![Graphique sous l'onglet analyseur de score avec un point de données sélectionné](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
Les actions étiquetées **[non score]** sont celles que vous pouvez effectuer pour votre organisation, mais comme elles ne sont pas connectées au score de sécurité, elles ne sont pas évaluées.  

Sur la page analyseur de **score** , cliquez sur un point de données pour un jour spécifique, puis faites défiler la liste pour voir les actions terminées et incomplètes pour ce jour afin de déterminer ce qui a changé. Le score est calculé une fois par jour (environ 1:00 PST). Si vous modifiez une action mesurée, le score est automatiquement mis à jour le jour suivant. Il faut jusqu'à 48 heures pour qu'une modification soit reflétée dans votre score.

Le score de sécurité n'exprime pas une mesure absolue de la probabilité d'obtenir une violation. Elle exprime la mesure dans laquelle vous avez adopté des fonctionnalités qui peuvent décaler le risque d'être enfreintes. Aucun service ne peut garantir que vous ne serez pas violé, et le score sécurisé ne doit pas être interprété comme une garantie de quelque façon que ce soit.
 
## <a name="how-secure-score-helps"></a>Aide du score de sécurité

Avec la fonction de chiffrement sécurisé, vous pouvez améliorer la sécurité de votre organisation en utilisant les fonctionnalités de sécurité intégrées dans Office 365 (un grand nombre d'entre vous avez déjà acheté, mais cela n'est peut-être pas conscient). Pour en savoir plus sur ces fonctionnalités, vous pouvez vous assurer que vous prenez les mesures appropriées pour protéger votre organisation contre les menaces.
  
Mais ne suivez pas seulement notre mot pour le service informatique. Les clients qui utilisent le score de sécurité ont vu leur score augmenter cinq fois de plus que les clients qui ne l'utilisent pas. (L'augmentation de leur score correspond aux fonctionnalités de sécurité utilisées dans leur organisation.)
  
> [!NOTE]
> Le score de sécurité n'exprime pas une mesure absolue de la probabilité d'obtenir une violation. Elle exprime la mesure dans laquelle vous avez adopté des contrôles pouvant dépenser le risque d'être compromis. Aucun service ne peut garantir que vous ne serez pas violé, et le score de sécurité ne doit pas être interprété comme une garantie de quelque façon que ce soit. 
  
## <a name="required-permissions"></a>Autorisations requises

Pour afficher et utiliser votre tableau de bord de score sécurisé, vous devez disposer de l'un des rôles suivants dans [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):
- Administrateur général
- Administrateur de facturation
- Administrateur d'utilisateur
- Administrateur de mots de passe
- Administrateur de sécurité
- Lecteur de sécurité
- Administrateur Exchange
- Administrateur SharePoint

 Les utilisateurs qui ne sont pas affectés à un rôle d'administrateur ne peuvent pas accéder au score sécurisé.

## <a name="related-topics"></a>Voir aussi

[Vue d'ensemble du tableau de bord de sécurité](security-dashboard.md)

[Quel abonnement ai-je ?](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
