---
title: Détecter et résoudre les problèmes d’octroi illégal de consentement dans Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/23/2018
ms.audience: ITPro
ms.topic: article
ms.collection:
- o365_security_incident_response
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Découvrez comment reconnaître et corriger le consentement illicite accorde une attaque dans Office 365.
ms.openlocfilehash: 454b1b0dcf7a6182895dcc97889286f3000c9626
ms.sourcegitcommit: 8657e003ab1ff49113f222d1ee8400eff174cb54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2019
ms.locfileid: "30656070"
---
# <a name="detect-and-remediate-illicit-consent-grants-in-office-365"></a>Détecter et résoudre les problèmes d’octroi illégal de consentement dans Office 365

**Résumé**  Découvrez comment reconnaître et corriger le consentement illicite accorde une attaque dans Office 365.

## <a name="what-is-the-illicit-consent-grant-attack-in-office-365"></a>Qu'est-ce que l'attaque d'octroi de consentement illicite dans Office 365?
Dans le cadre d'une attaque d'octroi de consentement illicite, l'agresseur crée une application inscrite à Azure qui demande l'accès à des données, telles que des informations de contact, des courriers électroniques ou des documents. L'agresseur examine ensuite un utilisateur final pour lui accorder l'autorisation d'accéder à ses données par le biais d'une attaque par hameçonnage ou en injectant du code illicite dans un site Web de confiance. Une fois que l'application illicite a reçu l'autorisation, elle dispose d'un accès aux données au niveau du compte sans avoir besoin d'un compte organisationnel. Les étapes de correction normales, comme la réinitialisation des mots de passe pour les comptes violés ou la nécessité d'une authentification multiFacteur (MFA) sur les comptes, ne sont pas efficaces contre ce type d'attaque, car il s'agit d'applications tierces qui sont externes à l'organisation. Ces attaques exploitent un modèle d'interaction qui suppose que l'entité qui appelle les informations est Automation et non humain.

## <a name="what-does-an-illicit-consent-grant-attack-look-like-in-office-365"></a>À quoi ressemble une attaque d'octroi de consentement illicite dans Office 365?
Vous devez rechercher dans le **Journal d'audit** Office 365 pour rechercher des signes, également appelés indicateurs de compromission (IOC) de cette attaque. Pour les organisations avec de nombreuses applications Azure enregistrées et une base d'utilisateurs volumineuses, la meilleure pratique consiste à examiner les subventions accordées par vos organisations chaque semaine.
### <a name="steps-for-finding-signs-of-this-attack"></a>Étapes à suivre pour trouver des signes de cette attaque
1. Ouvrez le **Centre de sécurité et conformité** dans votre client Office 365.
2. Naviguez jusqu'au nœud d' **enquête & de recherche** et sélectionnez recherche du **Journal d'audit** .
3. Créez une recherche (toutes les activités et tous les utilisateurs) et filtrez les résultats pour le consentement à l'application, puis ajoutez OAuth2PermissionGrant.
4. Examinez les propriétés étendues et vérifiez si IsAdminContent est défini sur true.


Si cette valeur est true, cela signifie qu'une personne disposant d'un accès administrateur général peut avoir accordé un accès étendu aux données. Si cette opération est inattendue, prenez les mesures nécessaires pour [confirmer une attaque](detect-and-remediate-illicit-consent-grants.md#confirmattack).

<a name="confirmattack"> </a>
## <a name="how-to-confirm-an-attack"></a>Procédure de confirmation d'une attaque
Si vous avez une ou plusieurs instances de l'IOCs mentionnées ci-dessus, vous devez procéder à une nouvelle enquête afin de confirmer que l'attaque a eu lieu. Vous pouvez utiliser l'une des trois méthodes suivantes pour confirmer l'attaque.
- Inventorier les applications et leurs autorisations à l'aide du portail Azure Active Directory. Cette méthode est complète, mais vous ne pouvez vérifier qu'un seul utilisateur à la fois, ce qui peut prendre beaucoup de temps si vous avez un grand nombre d'utilisateurs à vérifier.
- Inventorier les applications et leurs autorisations à l'aide de PowerShell. Il s'agit de la méthode la plus rapide et la plus complète, avec moins de surcharges.
- Demandez à vos utilisateurs de vérifier individuellement leurs applications et leurs autorisations et de signaler les résultats aux administrateurs pour la correction.

## <a name="inventory-apps-with-access-in-your-organization"></a>Inventorier les applications avec Access dans votre organisation
Vous pouvez effectuer cette opération pour vos utilisateurs avec le portail Azure Active Directory ou PowerShell ou faire en sorte que vos utilisateurs énumèrent individuellement leur accès aux applications.

### <a name="steps-for-using-the-azure-active-directory-portal"></a>Procédure d'utilisation du portail Azure Active Directory
Vous pouvez rechercher les applications auxquelles un utilisateur individuel a accordé des autorisations à l'aide du [portail Azure Active Directory](https://portal.azure.com/). 
1. Connectez-vous au portail Azure avec des droits d'administration.
2. Sélectionnez le panneau Azure Active Directory.
3. Sélectionnez **utilisateurs**.
4. Sélectionnez l'utilisateur que vous souhaitez examiner.
5. Sélectionnez **applications**.

Cela vous indiquera les applications qui sont affectées à l'utilisateur et les autorisations dont disposent les applcations.

### <a name="steps-for-having-your-users-enumerate-their-application-access"></a>Étapes à suivre pour faire en sorte que vos utilisateurs énumèrent leur accès aux applications
Demandez à vos utilisateurs d' https://myapps.microsoft.com accéder à leur propre application. Ils doivent être en mesure de voir toutes les applications avec Access, d'afficher des détails les concernant (y compris l'étendue d'Access) et de pouvoir révoquer des privilèges aux applications suspectes ou illicites.

### <a name="steps-for-doing-this-with-powershell"></a>Étapes à suivre avec PowerShell
Le moyen le plus simple de vérifier l'attaque d'octroi de consentement illicite consiste à exécuter [Get-AzureADPSPermissions. ps1](https://gist.github.com/psignoret/41793f8c6211d2df5051d77ca3728c09), qui videra toutes les autorisations OAuth et les applications OAuth pour tous les utilisateurs de votre location dans un fichier. csv. 

#### <a name="pre-requisites"></a>Conditions préalables
- Bibliothèque Azure AD PowerShell installée.
- Droits d'administrateur général sur le client sur lequel le script sera exécuté.
- Administrateur local sur l'ordinateur à partir duquel exécutera les scripts.

> [!IMPORTANT]
> Nous vous recommandons vivement de demander une authentification multifacteur sur votre compte d'administrateur.  Ce script prend en charge l'authentification MFA.

1. Connectez-vous à l'ordinateur à partir duquel vous allez exécuter le script avec des droits d'administrateur local.
2. Téléchargez ou copiez le script [Get-AzureADPSPermissions. ps1](https://gist.github.com/psignoret/41793f8c6211d2df5051d77ca3728c09) depuis Github vers un dossier à partir duquel vous allez exécuter l'scruipt.  Il s'agit du dossier dans lequel le fichier de sortie «Permissions. csv» sera écrit.
3. Ouvrez une instance PowerShell en tant qu'administrateur et ouvrez le dossier dans lequel vous avez enregistré le script.
4. Connectez-vous à votre annuaire à l'aide de la cmdlet [Connect-AzureAD](https://docs.microsoft.com/powershell/module/azuread/connect-azuread?view=azureadps-2.0) .
5. Exécutez la commande PowerShell suivante:`Get-AzureADPSPermissions.ps1 | Export-csv -path "Permissions.csv" -NoTypeInformation`

Le script génère un fichier nommé perMissions. csv. Procédez comme suit pour rechercher les octrois d'autorisations d'application illicites: 
1. Dans la colonne ConsentType (colonne G), recherchez la valeur «AllPrinciples». L'autorisation AllPrincipals permet à l'application cliente d'accéder au contenu de tout le monde dans la location. Les applications Office 365 natives ont besoin de cette autorisation pour fonctionner correctement. Toutes les applications non-Microsoft disposant de cette autorisation doivent être revues attentivement.
2.  Dans la colonne autorisation (colonne F), examinez les autorisations dont dispose chaque application déléguée pour le contenu. Recherchez les autorisations «lecture» et «écriture» ou «*. All», et examinez attentivement ces éléments, car ils ne sont pas appropriés.
3.  Examinez les utilisateurs spécifiques qui ont des autorisations accordées. Si des utilisateurs ayant un profil élevé ou un impact élevé ont reçu des autorisations inappropriées, vous devez approfondir votre enquête.
4.  Dans la colonne ClientDisplayName (colonne C), recherchez les applications qui semblent suspectes. Les applications dont les noms sont mal orthographiés, les noms de Super Bland ou les noms de pirate doivent être soigneusement revues.

## <a name="determine-the-scope-of-the-attack"></a>Déterminer l'étendue de l'attaque
Après avoir terminé l'inventaire de l'accès aux applications, consultez le **Journal d'audit** Office 365 pour déterminer l'étendue complète de la violation.  Rechercher sur les utilisateurs concernés, les périodes auxquelles l'application illicite a eu accès à votre organisation, ainsi que les autorisations de l'application. Vous pouvez effectuer une recherche dans le **Journal d'audit** dans le [Centre de sécurité et de conformité Office 365](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c). 

> [!IMPORTANT]
> L'audit des [boîtes aux lettres](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918) et l' [audit des activités pour les administrateurs et les utilisateurs](https://support.office.com/article/turn-office-365-audit-log-search-on-or-off-e893b19a-660c-41f2-9074-d3631c95a014) doivent avoir été activés avant l'attaque pour obtenir ces informations.

## <a name="how-to-stop-and-remediate-an-illicit-consent-grant--attack"></a>Comment arrêter et corriger une attaque d'octroi de consentement illicite
Une fois que vous avez identifié une application avec des autorisations illégales, vous disposez de plusieurs méthodes pour supprimer cet accès.
- Vous pouvez révoquer l'autorisation de l'application dans le portail Azure Active Directory en procédant comme suit:
    - Accédez à l'utilisateur affecté dans le panneau **utilisateur Azure Active Directory** .
    - Sélectionnez **applications**.
    - Sélectionnez l'application illicite.
    - Cliquez sur **supprimer** dans le détail.
- Vous pouvez révoquer l'autorisation d'acceptation OAuth avec PowerShell en suivant les étapes décrites dans [Remove-AzureADOAuth2PermissionGrant](https://docs.microsoft.com/powershell/module/azuread/Remove-AzureADOAuth2PermissionGrant?view=azureadps-2.0).
- Vous pouvez révoquer l'attribution de rôle d'application de service avec PowerShell en suivant les étapes décrites dans [Remove-AzureADServiceAppRoleAssignment](https://docs.microsoft.com/powershell/module/azuread/Remove-AzureADServiceAppRoleAssignment?view=azureadps-2.0).
- Vous pouvez également désactiver la connexion pour le compte affecté, ce qui désactive l'accès de l'application aux données de ce compte. Ceci n'est bien évidemment pas idéal pour la productivité de l'utilisateur final, mais si vous travaillez pour limiter l'impact rapidement, il peut s'agir d'une correction à court terme viable.
- Vous pouvez désactiver les applications intégrées pour votre client. Il s'agit d'une étape importante qui empêche les utilisateurs finaux d'accorder leur consentement à l'échelle du client. Cela empêche vos utilisateurs d'accorder par inadvertance l'accès à une application malveillante. Cette opération n'est pas fortement recommandée car elle affaiblit gravement la capacité de vos utilisateurs à être productifs avec des applications tierces.  Pour ce faire, procédez comme suit: [activation ou](https://support.office.com/article/Turning-Integrated-Apps-on-or-off-7e453a40-66df-44ab-92a1-96786cb7fb34)désActivation des applications intégrées.

## <a name="secure-office-365-like-a-cybersecurity-pro"></a>Sécuriser Office 365 comme un Cybersecurity Pro
Votre abonnement Office 365 est fourni avec un ensemble de fonctionnalités de sécurité puissantes que vous pouvez utiliser pour protéger vos données et vos utilisateurs.  Utilisez la feuille de [route de sécurité Office 365: les principales priorités pour les 30 jours, 90 jours et au-delà](https://support.office.com/article/office-365-security-roadmap-top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) pour implémenter les meilleures pratiques recommandées par Microsoft pour la sécurisation de votre client Office 365.
- Tâches à accomplir dans les 30 premiers jours.  Ceux-ci ont des effets immédiats et ont un faible impact sur vos utilisateurs.
- Tâches à effectuer dans les 90 jours. La planification et l'implémentation de ces deux éléments prennent un peu plus de temps, mais améliorent grandement votre position de sécurité.
- Au-delà de 90 jours. Ces améliorations s'appuient sur vos premiers 90 jours de travail.

## <a name="see-also"></a>Voir aussi :
- [Application inattendue dans ma liste d'applications](https://docs.microsoft.com/azure/active-directory/application-access-unexpected-application) guide les administrateurs à travers les diverses actions qu'il peut vouloir effectuer après avoir réalisé qu'il existe des applications inattendues ayant accès aux données.
- [Intégration d'applications avec Azure Active Directory]  (https://docs.microsoft.com/azure/active-directory/active-directory-apps-permissions-consent) est une vue d'ensemble de haut niveau du consentement et des autorisations.  Prêtez une attention particulière à la section [vue d'ensemble de la structure de consentement](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#overview-of-the-consent-framework) .
- [Problèmes de développement de mon application](https://docs.microsoft.com/azure/active-directory/active-directory-application-dev-development-content-map) fournit des liens vers différents Articles liés au consentement.
- Les [objets principal d'application et de service dans Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/develop/active-directory-application-objects) fournissent une vue d'ensemble des objets principaux d'application et de service qui sont essentiels au modèle d'application.
- [Gérer l'accès aux applications](https://docs.microsoft.com/azure/active-directory/active-directory-managing-access-to-apps) est une vue d'ensemble des fonctionnalités dont les administrateurs ont besoin pour gérer l'accès des utilisateurs aux applications.
