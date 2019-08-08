---
title: Modifier les stratégies de barrière des informations
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/08/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Découvrez comment modifier ou supprimer des stratégies pour les barrières d’informations.
ms.openlocfilehash: 20a1dd62fa80469a7a31db9b5541064ae16b4e02
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230588"
---
# <a name="edit-or-remove-information-barrier-policies"></a>Modifier (ou supprimer) des stratégies de barrière des informations

Une fois que vous avez [défini des stratégies de barrière des informations](information-barriers-policies.md), vous devrez peut-être modifier ces stratégies ou vos segments d’utilisateur, dans le cadre de la [résolution des problèmes](information-barriers-troubleshooting.md) ou de la maintenance normale. Utilisez cet article comme guide.

## <a name="what-do-you-want-to-do"></a>Que souhaitez-vous faire ?

|Opération  |Description |
|---------|---------|
|[Modifier les attributs de compte d’utilisateur](#edit-user-account-attributes)     |Renseignez les attributs d’Azure Active Directory qui peuvent être utilisés pour définir des segments.<br/>Modifier les attributs de compte d’utilisateur lorsque les utilisateurs ne sont pas inclus dans les segments, pour modifier les segments dans lesquels ils se trouvent ou pour définir des segments à l’aide de différents attributs.         |
|[Modifier un segment](#edit-a-segment)     |Modifiez les segments lorsque vous souhaitez modifier le mode de définition d’un segment. <br/>Par exemple, vous avez peut-être défini des segments à l’origine à l’aide de *Department* et vous voulez maintenant utiliser un autre attribut, tel que *memberOf*.         |
|[Modifier une stratégie](#edit-a-policy)     |Modifiez une stratégie de barrière des informations lorsque vous souhaitez modifier le fonctionnement d’une stratégie.<br/>Par exemple, au lieu de bloquer les communications entre deux segments, vous pouvez décider de n’autoriser que les communications entre certains segments.         |
|[Définir une stratégie sur état inactif](#set-a-policy-to-inactive-status)     |Définissez une stratégie sur état inactif lorsque vous voulez modifier une stratégie ou si vous ne souhaitez pas qu’une stratégie soit appliquée.         |
|[Supprimer une stratégie](#remove-a-policy)     |Supprimez une stratégie de barrière des informations lorsque vous n’avez plus besoin d’une stratégie particulière en place.         |
|[Arrêter une application de stratégie](#stop-a-policy-application)     |Procédez comme suit pour arrêter le processus d’application des stratégies de barrière des informations.<br/>Notez que l’arrêt d’une application de stratégie n’est pas instantané et qu’elle n’annule pas les stratégies déjà appliquées aux utilisateurs.         |
|[Définir des stratégies pour les barrières des informations](information-barriers-policies.md)     |Définissez une stratégie de barrière des informations lorsque vous n’avez pas déjà de telles stratégies, et vous devez limiter ou limiter les communications entre des groupes d’utilisateurs spécifiques.         |
|[Résolution des problèmes liés aux informations](information-barriers-troubleshooting.md)     |Reportez-vous à cet article lorsque vous rencontrez des problèmes inattendus avec des barrières d’informations.         |

> [!IMPORTANT]
> Pour effectuer les tâches décrites dans cet article, vous devez disposer d’un rôle approprié, par exemple:<br/>-Administrateur général de Microsoft 365 entreprise<br/>-Administrateur général Office 365<br/>-Administrateur de conformité<br/>-IB gestion de la conformité (il s’agit d’un nouveau rôle!)<p>Pour en savoir plus sur les conditions préalables pour les barrières d’informations, reportez-vous à la rubrique [conditions préalables (pour les stratégies de barrière des informations)](information-barriers-policies.md#prerequisites).<p>Assurez [-vous de vous connecter au centre de sécurité & de sécurité Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

## <a name="edit-user-account-attributes"></a>Modifier les attributs de compte d’utilisateur

Utilisez cette procédure pour modifier les attributs utilisés pour segmenter les utilisateurs. 

Par exemple, si vous utilisez un attribut de service et qu’un ou plusieurs comptes d’utilisateur n’ont pas de valeurs répertoriées pour le service, vous devez modifier ces comptes d’utilisateur pour inclure les informations de service. 

Les attributs de compte d’utilisateur sont utilisés pour définir des segments afin que les stratégies de barrière des informations puissent être affectées.

1. Pour afficher les détails d’un compte d’utilisateur spécifique, tels que les valeurs d’attribut et les segments affectés, utilisez la cmdlet **Get-InformationBarrierRecipientStatus** avec les paramètres d’identité. 

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` <p>   Vous pouvez utiliser n’importe quelle valeur qui identifie de façon unique chaque utilisateur, comme le nom, l’alias, le nom unique, le nom de domaine canonique, l’adresse de messagerie ou le GUID. <p>   (Vous pouvez également utiliser cette applet de commande pour un seul `Get-InformationBarrierRecipientStatus -Identity <value>`utilisateur:)      |`Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`  <p>   Dans cet exemple, nous faisons référence à deux comptes d’utilisateur dans Office 365: *meganb* pour *Megan*, et *Alexw* pour *Alex*.         |

2. Déterminez l’attribut que vous souhaitez modifier pour vos profils de compte d’utilisateur. Pour plus d’informations, reportez-vous à la rubrique [attributs pour les stratégies de barrière des informations](information-barriers-attributes.md) . 

3. Modifiez un ou plusieurs comptes d’utilisateur pour inclure des valeurs pour l’attribut que vous avez sélectionné à l’étape précédente. Pour ce faire, utilisez l’une des procédures suivantes:

    - Pour modifier un seul compte, voir [Ajouter ou mettre à jour les informations de profil d’un utilisateur à l’aide d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).

    - Pour modifier plusieurs comptes (ou utiliser PowerShell pour modifier un seul compte), voir [configure User Account Properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).

## <a name="edit-a-segment"></a>Modifier un segment

Utilisez cette procédure pour modifier la définition d’un segment d’utilisateur. Par exemple, vous pouvez modifier le nom d’un segment ou le filtre utilisé pour déterminer qui est inclus dans le segment.

1. Pour afficher tous les segments existants, utilisez la cmdlet **Get-OrganizationSegment** .
    
    Syntaxe`Get-OrganizationSegment`

    Vous verrez une liste de segments et des détails pour chacune d’elles, comme le type de segment, sa valeur UserGroupFilter, l’auteur ou la dernière modification, GUID, etc.

    > [!TIP]
    > Imprimez ou enregistrez votre liste de segments pour référence ultérieure. Par exemple, si vous souhaitez modifier un segment, vous devez connaître son nom ou identifier la valeur (utilisée avec le paramètre Identity).

2. Pour modifier un segment, utilisez la cmdlet **Set-OrganizationSegment** avec le paramètre **Identity** et les détails pertinents. 

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`     |`Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"` <p>Dans cet exemple, pour le segment qui a le GUID *c96e0837-C232-4A8A-841e-ef45787d8fcd*, nous avons mis à jour le nom du service en «hrdept».         |

Une fois que vous avez terminé de modifier les segments de votre organisation, vous pouvez [définir](information-barriers-policies.md#part-2-define-information-barrier-policies) ou [modifier](#edit-a-policy) des stratégies de barrière des informations.

## <a name="edit-a-policy"></a>Modifier une stratégie

1. Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .

    Syntaxe`Get-InformationBarrierPolicy`

    Dans la liste des résultats, identifiez la stratégie à modifier. Notez le GUID et le nom de la stratégie.

2. Utilisez la cmdlet **Set-InformationBarrierPolicy** avec un paramètre **Identity** et spécifiez les modifications que vous souhaitez effectuer.

    Exemple: Supposons qu’une stratégie a été définie pour empêcher le segment de *recherche* de communiquer avec les segments de *ventes* et de *marketing* . La stratégie a été définie à l’aide de cette applet de commande:`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`
    
    Supposons que nous voulons la modifier afin que les membres du segment de *recherche* puissent uniquement communiquer avec des personnes dans le segment *RH* . Pour effectuer cette modification, nous utilisons cette applet de commande:`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`

    Dans cet exemple, nous avons modifié «SegmentsBlocked» en «SegmentsAllowed» et spécifié le segment *HR* .

3. Lorsque vous avez terminé de modifier une stratégie, veillez à appliquer vos modifications. (Voir [appliquer des stratégies de barrière des informations](information-barriers-policies.md#part-3-apply-information-barrier-policies).)

## <a name="set-a-policy-to-inactive-status"></a>Définir une stratégie sur état inactif

1. Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .

    Syntaxe`Get-InformationBarrierPolicy`

    Dans la liste des résultats, identifiez la stratégie que vous souhaitez modifier (ou supprimer). Notez le GUID et le nom de la stratégie.

2. Pour définir l’état de la stratégie sur inactive, utilisez la cmdlet **Set-InformationBarrierPolicy** avec un paramètre Identity et le paramètre State défini sur inactive.

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Set-InformationBarrierPolicy -Identity GUID -State Inactive`     |`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive` <p>Dans cet exemple, nous définissons une stratégie de barrière des informations qui a un GUID *43c37853-EA10-4b90-A23D-ab8c9377247* à un état inactif.         |

3. Pour appliquer vos modifications, utilisez l’applet de commande **Start-InformationBarrierPoliciesApplication** .

    Syntaxe`Start-InformationBarrierPoliciesApplication`

    Les modifications sont appliquées, utilisateur par utilisateur, pour votre organisation. Si votre organisation est volumineuse, cette opération peut prendre 24 heures (ou plus). (En règle générale, il faut environ une heure pour traiter les comptes d’utilisateur 5 000.)

À ce stade, une ou plusieurs stratégies de barrière des informations sont définies sur l’état inactif. À partir de là, vous pouvez effectuer l’une des opérations suivantes:
- Conservez-la telle quelle (une stratégie définie sur l’état inactif n’a aucun effet sur les utilisateurs)
- [Modifier une stratégie](#edit-a-policy) 
- [Supprimer une stratégie](#remove-a-policy)

## <a name="remove-a-policy"></a>Supprimer une stratégie

1. Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .

    Syntaxe`Get-InformationBarrierPolicy`

    Dans la liste des résultats, identifiez la stratégie à supprimer. Notez le GUID et le nom de la stratégie. Assurez-vous que la stratégie est définie sur état inactif.

2. Utilisez la cmdlet **Remove-InformationBarrierPolicy** avec un paramètre Identity.

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Remove-InformationBarrierPolicy -Identity GUID`     |`Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471` <p>Dans cet exemple, nous supprimons la stratégie qui a le GUID *43c37853-EA10-4b90-A23D-ab8c93772471*.          |

    Lorsque vous y êtes invité, confirmez la modification.

3. Répétez les étapes 1-2 pour chaque stratégie que vous souhaitez supprimer.

4. Lorsque vous avez terminé de supprimer des stratégies, appliquez vos modifications. Pour ce faire, utilisez l’applet de commande **Start-InformationBarrierPoliciesApplication** .

    Syntaxe`Start-InformationBarrierPoliciesApplication`

    Les modifications sont appliquées, utilisateur par utilisateur, pour votre organisation. Si votre organisation est volumineuse, cette opération peut prendre 24 heures (ou plus).

## <a name="stop-a-policy-application"></a>Arrêter une application de stratégie

Si, après avoir commencé à appliquer des stratégies de barrière des informations, vous souhaitez arrêter l’application de ces stratégies, utilisez la procédure suivante. N’oubliez pas que le processus doit durer environ 30-35 minutes.

1. Pour afficher l’état de l’application de stratégie de barrière des informations la plus récente, utilisez la cmdlet **Get-InformationBarrierPoliciesApplicationStatus** .

    Syntaxe`Get-InformationBarrierPoliciesApplicationStatus`

    Notez le GUID de l’application.

2. Utilisez la cmdlet **Stop-InformationBarrierPoliciesApplication** avec un paramètre Identity.

    |Syntaxe  |Exemple  |
    |---------|---------|
    |`Stop-InformationBarrierPoliciesApplication -Identity GUID`     |`Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1` <p>Dans cet exemple, nous arrêtons l’application des stratégies de barrière des informations.         |

## <a name="related-articles"></a>Articles connexes

[Obtenir une vue d’ensemble des barrières d’informations](information-barriers.md)

[Définir des stratégies pour les barrières des informations](information-barriers-policies.md)

[En savoir plus sur les barrières d’informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[Attributs des stratégies de barrière des informations](information-barriers-attributes.md)

[Résolution des problèmes liés aux informations](information-barriers-troubleshooting.md)
