---
title: Résolution des problèmes liés aux informations
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Utilisez cet article pour résoudre les problèmes liés aux barrières relatives aux informations.
ms.openlocfilehash: b37585469ec8bb299b7976f8a330f4c6b29e3f95
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668293"
---
# <a name="troubleshooting-information-barriers-preview"></a>Dépannage des barrières relatives aux informations (aperçu)

Les barrières d’informations peuvent aider votre organisation à rester conforme aux exigences légales et aux réglementations sectorielles. Par exemple, avec des barrières d’informations, vous pouvez restreindre la communication entre des groupes spécifiques d’utilisateurs afin d’éviter un conflit d’intérêt ou d’autres problèmes. Pour en savoir plus, consultez la rubrique barrières de l' [information (aperçu)](information-barriers.md).

Cet article fournit des instructions que vous pouvez utiliser pour obtenir des réponses à des questions ou résoudre des problèmes qui peuvent survenir avec des barrières d’information.  

## <a name="before-you-begin"></a>Avant de commencer...

Pour effectuer les tâches décrites dans cet article, vous devez disposer d’un rôle approprié, par exemple:
- Administrateur global Microsoft 365 entreprise
- Administrateur général Office 365
- Administrateur de conformité
- IB gestion de la conformité (il s’agit d’un nouveau rôle!)

Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations dans le centre de sécurité & conformité d’Office 365](permissions-in-the-security-and-compliance-center.md).

Pour en savoir plus sur les conditions préalables pour les barrières d’informations, reportez-vous à la rubrique [conditions préalables (pour les stratégies de barrière des informations)](information-barriers-policies.md#prerequisites).

Assurez-vous également de [vous connecter au centre de sécurité Office 365 Security & PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a>Problème: les personnes sont bloquées de manière inattendue dans Microsoft teams 

Dans ce cas, les personnes signalent des problèmes inattendus de communication dans Microsoft Teams. Exemples :
- Un utilisateur ne peut pas trouver ou communiquer avec un autre utilisateur dans Microsoft Teams.
- Un utilisateur ne peut pas voir ou sélectionner un autre utilisateur dans Microsoft Teams.
- Un utilisateur peut voir, mais ne peut pas envoyer de messages à un autre utilisateur de Microsoft Teams.

### <a name="what-to-do"></a>Procédure

1. Déterminez si les utilisateurs sont affectés par une stratégie de barrière des informations. Pour ce faire, utilisez la cmdlet **Get-InformationBarrierRecipientStatus** avec le paramètre Identity. 

    La syntaxe est`Get-InformationBarrierRecipientStatus -Identity`

    Vous pouvez utiliser n’importe quelle valeur d’identité qui identifie de façon unique chaque destinataire, comme le nom, l’alias, le nom unique (DN), le DN canonique, l’adresse de messagerie ou le GUID.

    Exemple : `Get-InformationBarrierRecipientStatus -Identity meganb`

    Dans cet exemple, nous utilisons un alias (*meganb*) pour le paramètre Identity. Cette applet de commande renvoie des informations qui indiquent si l’utilisateur est concerné par une stratégie de barrière des informations. (Recherchez * ExoPolicyId: \<GUID>.)

    Si les utilisateurs ne sont pas inclus dans les stratégies de barrière des informations, contactez le support technique. Sinon, passez à l’étape suivante.

2. Découvrez quels segments sont inclus dans une stratégie de barrière des informations. Pour ce faire, utilisez l' `Get-InformationBarrierPolicy` applet de commande avec le paramètre Identity. Utilisez des détails, tels que le GUID de stratégie (ExoPolicyId) que vous avez reçu au cours de l’étape précédente, en tant que valeur d’identité.

    Exemple : `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`

    Dans cet exemple, nous obtenons des informations détaillées sur la stratégie de barrière des informations qui comporte ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.
    
    Une fois que vous avez exécuté l’applet de commande, recherchez les valeurs **AssignedSegment**, **SegmentsAllowed**et **SegmentsBlocked** dans les résultats.

    Exemple: après avoir exécuté `Get-InformationBarrierPolicy` l’applet de commande, nous avons vu les éléments suivants dans notre liste de résultats:

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    Dans ce cas, nous pouvons voir qu’une stratégie de barrière des informations affecte les personnes qui se trouvent dans les segments de ventes et de recherche. Dans ce cas, les personnes dans les ventes ne peuvent pas communiquer avec les personnes de la recherche. Si cela semble correct, les barrières de l’information fonctionnent comme prévu. Si ce n’est pas le cas, passez à l’étape suivante.

4. Assurez-vous que vos segments sont correctement définis. Pour ce faire, utilisez l' `Get-OrganizationSegment` applet de commande et passez en revue la liste des résultats. 

    Pour afficher les détails d’un segment spécifique, utilisez `Get-OrganizationSegment` l’applet de commande avec un paramètre Identity. 

    Exemple : `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`

    Dans cet exemple, nous obtenons des informations sur le segment qui a le GUID *c96e0837-C232-4A8A-841e-ef45787d8fcd*.

    Passez en revue les détails du segment. Si nécessaire, [modifiez un segment](information-barriers-policies.md#edit-a-segment), puis réutilisez l' `Start-InformationBarrierPoliciesApplication` applet de commande.

    Si vous rencontrez toujours des problèmes avec votre stratégie de barrière des informations, contactez le support technique.
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a>Problème: le processus de l’application de barrière des informations prend trop de temps

Après avoir exécuté l’applet de commande **Start-InformationBarrierPoliciesApplication** , le processus prend beaucoup de temps.

### <a name="what-to-do"></a>Procédure

1. Gardez à l’esprit que lorsque vous exécutez la cmdlet application de stratégie, les stratégies de barrière des informations sont appliquées (ou supprimées), utilisateur par utilisateur, pour tous les comptes de votre organisation. Si vous avez un grand nombre d’utilisateurs, le traitement peut prendre un certain temps. (En règle générale, il faut environ une heure pour traiter les comptes d’utilisateur 5 000.) 

2. Utilisez la cmdlet **Get-InformationBarrierPoliciesApplicationStatus** pour vérifier l’État.

    Syntaxe`Get-InformationBarrierPoliciesApplicationStatus`

    Pour afficher l’état de toutes les applications de stratégie de barrière des informations, utilisez`Get-InformationBarrierPoliciesApplicationStatus -All $true`

    Cela permet d’afficher des informations indiquant si l’application de stratégie a été exécutée, si elle a échoué ou est en cours d’exécution...

3. En fonction des résultats de l’étape 2, effectuez l’une des opérations suivantes:

    - Si l’application n’a pas démarré et qu’elle a été supérieure à 45 minutes depuis l’exécution de la cmdlet **Start-InformationBarrierPoliciesApplication** , passez en revue votre journal d’audit pour voir s’il existe des erreurs dans les définitions de stratégie, ou pour toute autre raison pour laquelle le l’application n’a pas démarré.

    - Si l’application a échoué, passez en revue vos segments et stratégies. Si nécessaire, [modifiez des segments](information-barriers-policies.md#edit-a-segment) et/ou [modifiez des stratégies](information-barriers-policies.md#edit-a-policy), puis exécutez à nouveau l’applet de commande **Start-InformationBarrierPoliciesApplication** .

    - Si l’application est toujours en cours d’exécution, patientez plus de temps pour qu’elle se termine. S’il y a eu plusieurs jours, contactez le support technique.

## <a name="related-topics"></a>Sujets associés

[Définir des stratégies pour les barrières d’informations dans Microsoft Teams (aperçu)](information-barriers-policies.md)

[Barrières des informations (aperçu)](information-barriers.md)



