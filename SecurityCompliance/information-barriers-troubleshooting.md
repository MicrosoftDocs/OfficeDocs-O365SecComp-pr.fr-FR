---
title: Résolution des problèmes liés aux informations
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 07/08/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Utilisez cet article pour résoudre les problèmes liés aux barrières relatives aux informations.
ms.openlocfilehash: 251fc1775318e2ed7cbda9a56e2c82db527082f6
ms.sourcegitcommit: a6f046f1529b0515f4f0e918a19ec83f4138b871
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2019
ms.locfileid: "35587053"
---
# <a name="troubleshooting-information-barriers"></a>Résolution des problèmes liés aux informations

Les [barrières d’informations](information-barriers.md) peuvent aider votre organisation à rester conforme aux exigences légales et aux réglementations sectorielles. Par exemple, avec des barrières d’informations, vous pouvez restreindre la communication entre des groupes spécifiques d’utilisateurs afin d’éviter un conflit d’intérêt ou d’autres problèmes. (Pour en savoir plus sur la configuration des barrières d’informations, consultez la rubrique [define Policies for information barrières](information-barriers-policies.md).)

Au cas où des personnes rencontreraient des problèmes inattendus après la mise en place de barrières d’informations, vous pouvez suivre certaines étapes pour résoudre ces problèmes. Utilisez cet article comme guide.

> [!IMPORTANT]
> Pour effectuer les tâches décrites dans cet article, vous devez disposer d’un rôle approprié, par exemple:<br/>-Administrateur général de Microsoft 365 entreprise<br/>-Administrateur général Office 365<br/>-Administrateur de conformité<br/>-IB gestion de la conformité (il s’agit d’un nouveau rôle!)<p>Pour en savoir plus sur les conditions préalables pour les barrières d’informations, reportez-vous à la rubrique [conditions préalables (pour les stratégies de barrière des informations)](information-barriers-policies.md#prerequisites).<p>Assurez [-vous de vous connecter au centre de sécurité & de sécurité Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

## <a name="issue-users-are-unexpectedly-blocked-from-communicating-with-others-in-microsoft-teams"></a>Problème: les utilisateurs sont bloqués de manière inattendue pour communiquer avec d’autres personnes dans Microsoft teams 

Dans ce cas, les personnes signalent des problèmes inattendants à la communication avec d’autres personnes dans Microsoft Teams. Exemples :
- Un utilisateur recherche, mais il ne peut pas trouver, un autre utilisateur de Microsoft Teams.
- Un utilisateur peut trouver, mais ne peut pas sélectionner, un autre utilisateur dans Microsoft Teams.
- Un utilisateur peut afficher un autre utilisateur, mais ne peut pas envoyer de messages à cet autre utilisateur dans Microsoft Teams.

### <a name="what-to-do"></a>Procédure

Déterminez si les utilisateurs sont affectés par une stratégie de barrière des informations. En fonction de la configuration des stratégies, les barrières d’informations peuvent fonctionner comme prévu. Sinon, vous devrez peut-être affiner les stratégies de votre organisation.

1. Utilisez la cmdlet **Get-InformationBarrierRecipientStatus** avec le paramètre Identity. 

    |Syntaxe  |Exemple  |
    |---------|---------|
    | `Get-InformationBarrierRecipientStatus -Identity` <p>Vous pouvez utiliser n’importe quelle valeur d’identité qui identifie de façon unique chaque destinataire, comme le nom, l’alias, le nom unique (DN), le DN canonique, l’adresse de messagerie ou le GUID.     |`Get-InformationBarrierRecipientStatus -Identity meganb` <p>Dans cet exemple, nous utilisons un alias (*meganb*) pour le paramètre Identity. Cette applet de commande renvoie des informations qui indiquent si l’utilisateur est concerné par une stratégie de barrière des informations. (Recherchez * ExoPolicyId: \<GUID>.)         |

    **Si les utilisateurs ne sont pas inclus dans les stratégies de barrière des informations, contactez le support technique**. Sinon, passez à l’étape suivante.

2. Découvrez quels segments sont inclus dans une stratégie de barrière des informations. Pour ce faire, utilisez l' `Get-InformationBarrierPolicy` applet de commande avec le paramètre Identity. 

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Get-InformationBarrierPolicy` <p>Utilisez des détails, tels que le GUID de stratégie (ExoPolicyId) que vous avez reçu au cours de l’étape précédente, en tant que valeur d’identité.     | `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f` <p>Dans cet exemple, nous obtenons des informations détaillées sur la stratégie de barrière des informations qui comporte ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.         |

    Une fois que vous avez exécuté l’applet de commande, recherchez les valeurs **AssignedSegment**, **SegmentsAllowed**et **SegmentsBlocked** dans les résultats.

    Par exemple, après avoir exécuté `Get-InformationBarrierPolicy` l’applet de commande, nous avons vu les éléments suivants dans notre liste de résultats:

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    Dans ce cas, nous pouvons voir qu’une stratégie de barrière des informations affecte les personnes qui se trouvent dans les segments de ventes et de recherche. Dans ce cas, les personnes dans les ventes ne peuvent pas communiquer avec les personnes de la recherche. 
    
    Si cela semble correct, les barrières de l’information fonctionnent comme prévu. Si ce n’est pas le cas, passez à l’étape suivante.

4. Assurez-vous que vos segments sont correctement définis. Pour ce faire, utilisez l' `Get-OrganizationSegment` applet de commande et passez en revue la liste des résultats. 

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Get-OrganizationSegment`<p>Utilisez cette applet de commande avec un paramètre Identity.     |`Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd` <p>Dans cet exemple, nous obtenons des informations sur le segment qui a le GUID *c96e0837-C232-4A8A-841e-ef45787d8fcd*.         |

    Passez en revue les détails du segment. Si nécessaire, [modifiez un segment](information-barriers-edit-segments-policies.md.md#edit-a-segment), puis réutilisez l' `Start-InformationBarrierPoliciesApplication` applet de commande.

    **Si vous rencontrez toujours des problèmes avec votre stratégie de barrière des informations, contactez le support technique**.

## <a name="issue-communications-are-allowed-between-users-who-should-be-blocked-in-microsoft-teams"></a>Problème: les communications sont autorisées entre les utilisateurs qui doivent être bloqués dans Microsoft teams

Dans ce cas, bien que les barrières d’informations soient définies, actives et appliquées, les personnes qui ne doivent pas pouvoir communiquer entre elles sont en mesure de converser les unes avec les autres dans Microsoft Teams.

### <a name="what-to-do"></a>Procédure

Vérifiez que les utilisateurs en question sont inclus dans une stratégie de barrière des informations. 

1. Utilisez la cmdlet **Get-InformationBarrierRecipientStatus** avec les paramètres d’identité.

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` <p>Vous pouvez utiliser n’importe quelle valeur qui identifie de façon unique chaque utilisateur, comme le nom, l’alias, le nom unique, le nom de domaine canonique, l’adresse de messagerie ou le GUID.     |`Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` <p>Dans cet exemple, nous faisons référence à deux comptes d’utilisateur dans Office 365: *meganb* pour *Megan*, et *Alexw* pour *Alex*.          |

    
    > [!TIP]
    > Vous pouvez également utiliser cette applet de commande pour un seul utilisateur:`Get-InformationBarrierRecipientStatus -Identity <value>`
    
2. Passez en revue les résultats. L’applet de commande **Get-InformationBarrierRecipientStatus** retourne des informations sur les utilisateurs, telles que les valeurs d’attribut et les stratégies de barrière des informations qui sont appliquées. 

    Passez en revue les résultats, puis effectuez les étapes suivantes, comme décrit dans le tableau suivant:
    
    |Résultats  |Étape suivante  |
    |---------|---------|
    |Aucun segment n’est répertorié pour le ou les utilisateurs sélectionnés     |Effectuez l’une des opérations suivantes :<br/>-Affecter des utilisateurs à un segment existant en modifiant leurs profils utilisateur dans Azure Active Directory. (Consultez la rubrique [configure User Account Properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).)<br/>-Définissez un segment à l’aide [d’un attribut pris en charge pour les barrières d’information](information-barriers-attributes.md). Ensuite, [définissez une nouvelle stratégie](information-barriers-policies.md#part-2-define-information-barrier-policies) ou [modifiez une stratégie existante](information-barriers-edit-segments-policies.md.md#edit-a-policy) pour inclure ce segment.  |
    |Les segments sont répertoriés, mais aucune stratégie de barrière des informations n’est affectée à ces segments     |Effectuez l’une des opérations suivantes :<br/>- [Définir une nouvelle stratégie de barrière des informations](information-barriers-policies.md#part-2-define-information-barrier-policies) pour chaque segment en question<br/>- [Modifier une stratégie de barrière des informations existante](information-barriers-edit-segments-policies.md.md#edit-a-policy) pour l’affecter au segment correct         |
    |Les segments sont répertoriés et chacun est inclus dans une stratégie de barrière des informations     |-Exécutez l' `Get-InformationBarrierPolicy` applet de commande pour vérifier que les stratégies de barrière des informations sont actives.<br/>-Exécutez l' `Get-InformationBarrierPoliciesApplicationStatus` applet de commande pour vérifier que les stratégies sont appliquées.<br/>-Exécutez l' `Start-InformationBarrierPoliciesApplication` applet de commande pour appliquer toutes les stratégies de barrière des informations actives.          |
    

## <a name="issue-i-need-to-remove-a-single-user-from-an-information-barrier-policy"></a>Problème: je dois supprimer un seul utilisateur d’une stratégie de barrière des informations

Dans ce cas, les stratégies de barrière des informations sont en vigueur et un ou plusieurs utilisateurs sont bloqués de manière inattendue avec d’autres personnes dans Microsoft Teams. Au lieu de supprimer toutes les stratégies de barrière des informations, vous pouvez supprimer un ou plusieurs utilisateurs individuels des stratégies de barrière des informations. 

### <a name="what-to-do"></a>Procédure

Les stratégies de barrière des informations sont affectées à des segments d’utilisateurs. Les segments sont définis à l’aide [de certains attributs dans les profils de comptes d’utilisateur](information-barriers-attributes.md). Si vous devez supprimer une stratégie d’un seul utilisateur, vous pouvez modifier le profil de cet utilisateur dans Azure Active Directory de sorte que l’utilisateur ne soit plus inclus dans un segment affecté par les barrières d’information.

1. Utilisez la cmdlet **Get-InformationBarrierRecipientStatus** avec les paramètres d’identité. Cette applet de commande retourne des informations sur les utilisateurs, telles que les valeurs d’attribut et les stratégies de barrière des informations qui sont appliquées.

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`<p>Vous pouvez utiliser n’importe quelle valeur qui identifie de façon unique chaque utilisateur, comme le nom, l’alias, le nom unique, le nom de domaine canonique, l’adresse de messagerie ou le GUID.     |`Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` <p>Dans cet exemple, nous faisons référence à deux comptes d’utilisateur dans Office 365: *meganb* pour *Megan*, et *Alexw* pour *Alex*.          |
    |`Get-InformationBarrierRecipientStatus -Identity <value>` <p>Vous pouvez utiliser n’importe quelle valeur qui identifie l’utilisateur de manière unique, par exemple le nom, l’alias, le nom unique, le nom de domaine canonique, l’adresse de messagerie ou le GUID.|`Get-InformationBarrierRecipientStatus -Identity jeanp`<p>Dans cet exemple, nous faisons référence à un compte unique dans Office 365: *jeanp*. |

2. Passez en revue les résultats pour voir si des stratégies de barrière des informations sont affectées et pour quels segments appartiennent à des utilisateurs. 

3. Pour supprimer un utilisateur d’un segment affecté par les barrières d’informations, [Mettez à jour les informations de profil de l’utilisateur dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).

4. Patientez environ 30 minutes avant que FwdSync se produise. Vous pouvez également exécuter `Start-InformationBarrierPoliciesApplication` l’applet de commande pour appliquer toutes les stratégies de barrière des informations actives.

## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a>Problème: le processus de l’application de barrière des informations prend trop de temps

Après avoir exécuté l’applet de commande **Start-InformationBarrierPoliciesApplication** , le processus prend beaucoup de temps.

### <a name="what-to-do"></a>Procédure

Gardez à l’esprit que lorsque vous exécutez la cmdlet application de stratégie, les stratégies de barrière des informations sont appliquées (ou supprimées), utilisateur par utilisateur, pour tous les comptes de votre organisation. Si vous avez un grand nombre d’utilisateurs, le traitement peut prendre un certain temps. (En règle générale, il faut environ une heure pour traiter les comptes d’utilisateur 5 000.)

1. Utilisez la cmdlet **Get-InformationBarrierPoliciesApplicationStatus** pour vérifier l’état de l’application de stratégie la plus récente.

    |Pour afficher l’application de stratégie la plus récente  |Pour afficher l’état de toutes les applications de stratégie  |
    |---------|---------|
    |`Get-InformationBarrierPoliciesApplicationStatus`     |`Get-InformationBarrierPoliciesApplicationStatus -All $true`         |


    Cela permet d’afficher des informations indiquant si l’application de stratégie a été exécutée, si elle a échoué ou est en cours d’exécution.

2. En fonction des résultats de l’étape précédente, effectuez l’une des opérations suivantes:
  
    |Statut  |Étape suivante  |
    |---------|---------|
    |**Non commencée**     |S’il a été plus de 45 minutes depuis l’exécution de la cmdlet **Start-InformationBarrierPoliciesApplication** , passez en revue votre journal d’audit pour voir s’il existe des erreurs dans les définitions de stratégie, ou pour toute autre raison pour laquelle l’application n’a pas démarré. |
    |**Échec**     |Si l’application a échoué, consultez votre journal d’audit. Consultez également vos segments et stratégies. Les utilisateurs sont-ils affectés à plusieurs segments? Est-ce qu’un segment est affecté à plusieurs poliicy? Si nécessaire, [modifiez des segments](information-barriers-edit-segments-policies.md.md#edit-a-segment) et/ou [modifiez des stratégies](information-barriers-edit-segments-policies.md.md#edit-a-policy), puis exécutez à nouveau l’applet de commande **Start-InformationBarrierPoliciesApplication** .  |
    |**En cours**     |Si l’application est toujours en cours d’exécution, patientez plus de temps pour qu’elle se termine. S’il y a eu plusieurs jours, rassemblez vos journaux d’audit, puis contactez le support technique. |

## <a name="issue-information-barrier-policies-are-not-being-applied-at-all"></a>Problème: les stratégies de barrière des informations ne sont pas appliquées du tout

Dans ce cas, vous avez défini des segments, défini des stratégies de barrière des informations, et vous avez tenté d’appliquer ces stratégies. Toutefois, lorsque vous exécutez l' `Get-InformationBarrierPoliciesApplicationStatus` applet de commande, vous pouvez constater que l’application de stratégie a échoué.

### <a name="what-to-do"></a>Procédure

Assurez-vous que votre organisation ne dispose pas des [stratégies de carnet d’adresses Exchange](https://docs.microsoft.com/exchange/address-books/address-book-policies/address-book-policies) en place. De telles stratégies empêchent l’application de stratégies de barrière des informations.

1. Connectez-vous à [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps). 

2. Exécutez la cmdlet [Get-AddressBookPolicy](https://docs.microsoft.com/powershell/module/exchange/email-addresses-and-address-books/get-addressbookpolicy?view=exchange-ps) et examinez les résultats.

    |Résultats  |Étape suivante  |
    |---------|---------|
    |Les stratégies de carnet d’adresses Exchange sont répertoriées     |[Supprimer des stratégies de carnet d’adresses](https://docs.microsoft.com/exchange/address-books/address-book-policies/remove-an-address-book-policy)         |
    |Aucune stratégie de carnet d’adresses n’existe |Consultez vos journaux d’audit pour savoir pourquoi l’application de stratégie est défectueuse. |

3. [Afficher l’état des comptes d’utilisateur, des segments, des stratégies ou de l’application de stratégie](information-barriers-policies.md#view-status-of-user-accounts-segments-policies-or-policy-application).

## <a name="related-topics"></a>Sujets associés

[Définir des stratégies pour les barrières d’informations dans Microsoft teams](information-barriers-policies.md)

[Barrières des informations](information-barriers.md)



