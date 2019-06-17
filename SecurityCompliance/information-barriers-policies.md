---
title: Définir des stratégies de barrière des informations
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Découvrez comment définir des stratégies pour les barrières d’informations dans Microsoft Teams.
ms.openlocfilehash: 8d575d0cde4bfec7109cc302f68beaf1040cd894
ms.sourcegitcommit: eeb51470d8996e93fac28d7f12c6117e2aeb0cf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2019
ms.locfileid: "34935946"
---
# <a name="define-policies-for-information-barriers-preview"></a>Définir des stratégies pour les barrières d’information (aperçu)

## <a name="overview"></a>Vue d’ensemble

Avec les barrières d’informations, vous pouvez définir des stratégies conçues pour empêcher certains segments d’utilisateurs de communiquer les uns avec les autres ou d’autoriser des segments spécifiques à communiquer uniquement avec certains autres segments. Les stratégies de barrière des informations peuvent aider votre organisation à respecter les normes et réglementations pertinentes de l’industrie et éviter les conflits d’intérêt potentiels. Pour en savoir plus, consultez la rubrique barrières de l' [information (aperçu)](information-barriers.md). 

Cet article explique comment planifier, définir, implémenter et gérer les stratégies de barrière des informations. Plusieurs étapes sont impliquées et le flux de travail est divisé en plusieurs parties. Veillez à lire les [conditions préalables](#prerequisites) et l’ensemble du processus avant de commencer à définir (ou à modifier) des stratégies de barrière des informations.

> [!TIP]
> Cet article inclut un [exemple de scénario](#example-contosos-departments-segments-and-policies) et un [classeur Excel](https://github.com/MicrosoftDocs/OfficeDocs-O365SecComp/raw/public/SecurityCompliance/media/InfoBarriers-PowerShellGenerator.xlsx) téléchargeable pour vous aider à planifier et à définir vos stratégies de barrière des informations.

## <a name="concepts-of-information-barrier-policies"></a>Concepts des stratégies de barrière des informations

Il est utile de savoir quels sont les concepts sous-jacents des stratégies de barrière des informations:

- Les **attributs de compte d’utilisateur** sont définis dans Azure Active Directory (ou Exchange Online). Ces attributs peuvent inclure le service, la fonction, l’emplacement, le nom de l’équipe et d’autres détails du profil de travail. 

- Les **segments** sont des ensembles d’utilisateurs définis dans le centre de conformité & la sécurité d’Office 365 à l’aide d’un **attribut de compte d’utilisateur**sélectionné. (Reportez-vous à la [liste des attributs pris en charge](information-barriers-attributes.md).) 

- Les **stratégies de barrière des informations** déterminent les limites ou restrictions de communication. Lorsque vous définissez des stratégies de barrière des informations, vous avez le choix entre deux types de stratégies:
    - Stratégies «bloquer» qui empêchent un segment de communiquer avec un autre segment
    - Stratégies «autoriser» qui permettent à un segment de communiquer avec certains autres segments seulement

- Une **application de stratégie** est exécutée une fois toutes les stratégies de barrière des informations définies et vous êtes prêt à les appliquer dans votre organisation.

## <a name="the-work-flow-at-a-glance"></a>Flux de travail en un clin d’œil

|Phase    |Ce qui est impliqué  |
|---------|---------|
|[Vérifier que les conditions préalables sont remplies](#prerequisites)     |-Vérifiez que vous disposez des [autorisations et des licences requises](information-barriers.md#required-licenses-and-permissions)<br/>-Assurez-vous que l’annuaire de votre organisation inclut des données qui reflètent la structure de votre organisation.<br/>-Activer la recherche dans l’annuaire étendu pour Microsoft teams<br/>-Vérifiez que la journalisation d’audit est activée.<br/>-Utiliser PowerShell (des exemples sont fournis)<br/>-Fournir le consentement de l’administrateur pour Microsoft Teams (étapes incluses)          |
|[Partie 1: segmenter tous les utilisateurs de votre organisation](#part-1-segment-users)     |-Déterminer les stratégies nécessaires<br/>-Créer une liste de segments à définir<br/>-Identifier les attributs à utiliser<br/>-Définir des segments en fonction de filtres de stratégie        |
|[Partie 2: définir des stratégies de barrière des informations](#part-2-define-information-barrier-policies)     |-Définir vos stratégies (ne pas appliquer)<br/>-Choisir parmi deux types (bloquer ou autoriser) |
|[Partie 3: appliquer des stratégies de barrière des informations](#part-3-apply-information-barrier-policies)     |-Définir les stratégies sur le statut actif<br/>-Exécuter l’application de stratégie<br/>-Afficher le statut de la stratégie         |
|(Si nécessaire) [Modifier un segment ou une stratégie](#edit-a-segment-or-a-policy)     |-Modifier un segment<br/>-Modifier ou supprimer une stratégie<br/>-Exécuter l’application de stratégie<br/>-Afficher le statut de la stratégie         |
|(Si nécessaire) [Résolution des problèmes](information-barriers-troubleshooting.md)|Action à effectuer lorsque des choses ne fonctionnent pas comme prévu|

## <a name="prerequisites"></a>Conditions préalables

En plus des [licences et des autorisations requises](information-barriers.md#required-licenses-and-permissions), assurez-vous que les conditions suivantes sont remplies: 
     
- **Données d’annuaire**. Assurez-vous que la structure de votre organisation est reflétée dans les données d’annuaire. Pour ce faire, assurez-vous que les attributs de compte d’utilisateur, tels que l’appartenance au groupe, le nom du service, etc., sont correctement renseignés dans Azure Active Directory (ou Exchange Online). Pour en savoir plus, consultez les ressources suivantes:
  - [Attributs des stratégies de barrière des informations (aperçu)](information-barriers-attributes.md)
  - [Ajouter ou mettre à jour les informations de profil d’un utilisateur à l’aide d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)
  - [Configurer les propriétés des comptes d'utilisateur avec Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)

- **Recherche dans l’annuaire étendu**. Avant de définir la première stratégie de barrière des informations de votre organisation, vous devez [activer la recherche dans l’annuaire d’étendues dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/teams-scoped-directory-search). Attendez au moins 24 heures après l’activation de la recherche dans l’annuaire d’étendue avant de configurer ou de définir des stratégies de barrière des informations.

- **Journalisation d’audit**. Pour Rechercher l’état d’une application de stratégie, la journalisation d’audit doit être activée. Nous vous recommandons d’effectuer cette opération avant de commencer à définir des segments ou des stratégies. Pour en savoir plus, consultez la rubrique [activer ou désactiver la recherche dans le journal d’audit Office 365](turn-audit-log-search-on-or-off.md).

- **PowerShell**. Actuellement, les stratégies de barrière des informations sont définies et gérées dans le centre de conformité Office 365 Security & à l’aide d’applets de commande PowerShell. Bien que plusieurs exemples soient fournis dans cet article, vous devez être familiarisé avec les cmdlets et les paramètres PowerShell. [Connectez-vous au centre de sécurité & conformité d’Office 365 PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

- **Consentement de l’administrateur pour les barrières d’informations dans Microsoft teams**. Lorsque vos stratégies sont en place, les barrières d’informations peuvent supprimer des personnes des sessions de conversation auxquelles elles ne sont pas censées se trouver. Cela permet de s’assurer que votre organisation reste conforme aux stratégies et réglementations. Utilisez la procédure suivante pour permettre aux stratégies de barrière des informations de fonctionner comme prévu dans Microsoft Teams. 

   1. Exécutez les applets de commande PowerShell suivantes:

      ```
      Login-AzureRmAccount 
      $appId="bcf62038-e005-436d-b970-2a472f8c1982" 
      $sp=Get-AzureRmADServicePrincipal -ServicePrincipalName $appId
      if ($sp -eq $null) { New-AzureRmADServicePrincipal -ApplicationId $appId }
      Start-Process  "https://login.microsoftonline.com/common/adminconsent?client_id=$appId"
      ```

   2. Lorsque vous y êtes invité, connectez-vous à l’aide de votre compte professionnel ou scolaire pour Office 365.

   3. Dans la boîte de dialogue **autorisations demandées** , passez en revue les informations, puis choisissez **accepter**.

Lorsque toutes les conditions préalables sont remplies, passez à la section suivante.

> [!TIP]
> Pour vous aider à préparer votre plan, un exemple de scénario est inclus dans cet article. [Consultez la rubrique services, segments et stratégies de contoso](#example-contosos-departments-segments-and-policies).<p>En outre, un classeur Excel téléchargeable est disponible pour vous aider à planifier et à définir vos segments et stratégies (et à créer vos cmdlets PowerShell). [Obtenir le classeur](https://github.com/MicrosoftDocs/OfficeDocs-O365SecComp/raw/public/SecurityCompliance/media/InfoBarriers-PowerShellGenerator.xlsx). 

## <a name="part-1-segment-users"></a>Partie 1: utilisateurs de segment

Pendant cette phase, vous déterminez les stratégies de barrière des informations requises, créez une liste de segments à définir, puis définissez vos segments.

### <a name="determine-what-policies-are-needed"></a>Déterminer les stratégies nécessaires

Considérant les réglementations juridiques et industrielles, qui sont les groupes au sein de votre organisation qui auront besoin de stratégies de barrière des informations? Créer une liste. Existe-t-il des groupes qui ne doivent pas être autorisés à communiquer avec un autre groupe? Existe-t-il des groupes qui doivent être autorisés à communiquer avec un ou deux autres groupes? Réfléchissez aux stratégies dont vous avez besoin en tant que appartenant à l’un des deux groupes suivants:
- Les stratégies «bloquer» empêchent un groupe de communiquer avec un autre groupe.
- Les stratégies «autoriser» permettent à un groupe de communiquer avec certains autres groupes spécifiques.

Lorsque vous disposez de la liste initiale des groupes et des stratégies, passez à l’identification des segments dont vous aurez besoin. 

### <a name="identify-segments"></a>Identifier les segments

En plus de votre liste initiale de stratégies, créez une liste de segments pour votre organisation. Chaque utilisateur de votre organisation doit appartenir à un segment, et aucun utilisateur ne doit appartenir à deux ou plusieurs segments. Chaque segment ne peut avoir qu’une seule stratégie de barrière des informations appliquée. 

Déterminez les attributs des données d’annuaire de votre organisation que vous utiliserez pour définir des segments. Vous pouvez utiliser *Department*, *memberOf*ou l’un des attributs pris en charge. Assurez-vous que vous avez sélectionné des valeurs dans l’attribut que vous sélectionnez pour tous les utilisateurs. [Consultez la liste des attributs pris en charge pour les barrières d’informations (aperçu)](information-barriers-attributes.md).

> [!IMPORTANT]
> **Avant de passer à la section suivante, assurez-vous que vos données d’annuaire possèdent des valeurs pour les attributs que vous pouvez utiliser pour définir des segments**. Si vos données d’annuaire n’ont pas de valeurs pour les attributs que vous souhaitez utiliser, tous les comptes d’utilisateur doivent être mis à jour pour inclure ces informations avant de passer à des barrières d’informations. Pour obtenir de l’aide, consultez les ressources suivantes:<br/>- [Configurer les propriétés des comptes d’utilisateur avec Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell)<br/>- [Ajouter ou mettre à jour les informations de profil d’un utilisateur à l’aide d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)

### <a name="define-segments-using-powershell"></a>Définir des segments à l’aide de PowerShell

La définition de segments n’a pas d’effet sur les utilisateurs; Il définit simplement l’étape de définition des stratégies de barrière des informations, puis leur application.

1. Pour définir un segment d’organisation, utilisez la cmdlet **New-OrganizationSegment** avec le paramètre **UserGroupFilter** qui correspond à l' [attribut](information-barriers-attributes.md) que vous souhaitez utiliser. 

    Syntaxe`New-OrganizationSegment -Name "segmentname" -UserGroupFilter "attribute -eq 'attributevalue'"`

    Exemple : `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`

    Dans cet exemple, un segment appelé *HR* est défini à l’aide de *HR*, une valeur dans l’attribut Department.

2. Répétez l’étape 1 pour chaque segment que vous souhaitez définir.

    Une fois que vous avez exécuté chaque cmdlet, vous devez voir une liste de détails sur le nouveau segment. Les détails incluent le type du segment, qui a été créé ou modifié pour la dernière fois, et ainsi de suite. 

> [!IMPORTANT]
> Assurez **-vous que vos segments ne se chevauchent pas**. Chaque utilisateur de votre organisation doit appartenir à un seul segment. Aucun utilisateur ne doit appartenir à deux segments ou plus. Les segments doivent être définis pour tous les utilisateurs de votre organisation. (Voir l' [exemple: segments définis par Contoso](#contosos-defined-segments) dans cet article.)

Une fois que vous avez défini vos segments, passez à la définition des stratégies de barrière des informations.

## <a name="part-2-define-information-barrier-policies"></a>Partie 2: définir des stratégies de barrière des informations

Déterminez si vous devez empêcher les communications entre certains segments ou limiter les communications à certains segments. Idéalement, vous utiliserez le nombre minimal de stratégies pour vous assurer que votre organisation est conforme aux exigences légales et industrielles.

Avec votre liste de segments d’utilisateurs et les stratégies de barrière des informations que vous souhaitez définir, sélectionnez un scénario, puis suivez les étapes. 

- [Scénario 1: bloquer les communications entre les segments](#scenario-1-block-communications-between-segments)
- [Scénario 2: autoriser un segment à communiquer avec un seul autre segment](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment)

> [!IMPORTANT]
> Assurez **-vous que lorsque vous définissez des stratégies, vous n’affectez pas plusieurs stratégies à un segment**. Par exemple, si vous définissez une stratégie pour un segment appelé *ventes*, ne définissez pas de stratégie supplémentaire pour les *ventes*.<p>De plus, lorsque vous définissez des stratégies de barrière des informations, veillez à définir ces stratégies sur état inactif jusqu’à ce que vous soyez prêt à les appliquer. La définition (ou modification) de stratégies n’affecte pas les utilisateurs tant que ces stratégies n’ont pas le statut actif, puis appliquées.

(Voir l' [exemple: stratégies de barrière des informations de contoso](#contosos-information-barrier-policies) dans cet article.)

### <a name="scenario-1-block-communications-between-segments"></a>Scénario 1: bloquer les communications entre les segments

Lorsque vous souhaitez empêcher les segments de communiquer les uns avec les autres, définissez deux stratégies: une pour chaque direction. Chaque stratégie bloque la communication de manière unidirectionnelle.

Par exemple, supposons que vous souhaitez bloquer les communications entre le segment A et le segment B. Dans ce cas, vous définissez une stratégie empêchant le segment A de communiquer avec le segment B, puis vous définissez une deuxième stratégie pour empêcher le segment B de communiquer avec le segment A.

1. Pour définir votre première stratégie de blocage, utilisez la cmdlet **New-InformationBarrierPolicy** avec le paramètre **SegmentsBlocked** . 

    Syntaxe`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsBlocked "segmentname"`

    Exemple : `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive`

    Dans cet exemple, nous avons défini une stratégie appelée *Sales-Research* pour un segment appelé *Sales*. Lorsqu’elle est active et appliquée, cette stratégie empêche les personnes dans les *ventes* de communiquer avec des personnes dans un segment nommé *Research*.

2. Pour définir votre deuxième segment de blocage, utilisez à nouveau la cmdlet **New-InformationBarrierPolicy** avec le paramètre **SegmentsBlocked** , cette fois avec les segments contrepassés.

    Exemple : `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive`

    Dans cet exemple, nous avons défini une stratégie appelée *Research-Sales* pour empêcher les recherches de communiquer avec les ventes.
 
2. Passez à l’une des opérations suivantes:

   - (Si nécessaire) [Définir une stratégie pour permettre à un segment de communiquer avec un seul autre segment](#scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment) 
   - (Après avoir défini toutes vos stratégies) [Appliquer des stratégies de barrière des informations](#part-3-apply-information-barrier-policies)

### <a name="scenario-2-allow-a-segment-to-communicate-only-with-one-other-segment"></a>Scénario 2: autoriser un segment à communiquer avec un seul autre segment

1. Pour permettre à un segment de communiquer avec un seul autre segment, utilisez la cmdlet **New-InformationBarrierPolicy** avec le paramètre **SegmentsAllowed** . 

    Syntaxe`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname"`

    Exemple : `New-InformationBarrierPolicy -Name "Manufacturing-HR" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR" -State Inactive`

    Dans cet exemple, nous avons défini une stratégie appelée *Manufacturing-HR* pour un segment appelé *Manufacturing*. Lorsqu’il est actif et appliqué, cette stratégie permet aux personnes de *fabrication* de communiquer uniquement avec des personnes dans un segment appelé *RH*. (Dans ce cas, la fabrication ne peut pas communiquer avec des utilisateurs qui ne font pas partie de RH.)

    **Si nécessaire, vous pouvez spécifier plusieurs segments avec cette applet de commande, comme illustré dans les deux exemples suivants.**

    Syntaxe`New-InformationBarrierPolicy -Name "policyname" -AssignedSegment "segmentname" -SegmentsAllowed "segmentname, segmentname"`

    **Exemple 1: définition d’une stratégie pour permettre à plusieurs segments de communiquer avec un seul autre segment**

    `New-InformationBarrierPolicy -Name "ResearchManufacturing-HR" -AssignedSegment "Research, Manufacturing" -SegmentsAllowed "HR" -State Inactive`

    Dans cet exemple, nous avons défini une stratégie qui permet aux segments de *recherche* et de *fabrication* de communiquer uniquement avec *RH*.

    **Exemple 2: définition d’une stratégie pour permettre à plusieurs segments de communiquer avec certains autres segments uniquement**    

    `New-InformationBarrierPolicy -Name "SalesMarketing-HRManufacturing" -AssignedSegment "Sales, Marketing" -SegmentsAllowed "HR, Manufacturing" -State Inactive`

    Dans cet exemple, nous avons défini une stratégie qui permet aux segments de *ventes* et de *marketing* de communiquer avec les *RH* et la *fabrication*.

    Répétez cette étape pour chaque stratégie que vous souhaitez définir pour permettre à des segments spécifiques de communiquer avec certains autres segments spécifiques.

2. Passez à l’une des opérations suivantes:

   - (Si nécessaire) [Définir une stratégie pour bloquer les communications entre les segments](#scenario-1-block-communications-between-segments) 
   - (Après avoir défini toutes vos stratégies) [Appliquer des stratégies de barrière des informations](#part-3-apply-information-barrier-policies)

## <a name="part-3-apply-information-barrier-policies"></a>Partie 3: appliquer des stratégies de barrière des informations

Les stratégies de barrière des informations ne sont pas appliquées tant que vous n’avez pas activé l’état actif, puis appliqué les stratégies.

1. La cmdlet **Get-InformationBarrierPolicy** permet d’afficher la liste des stratégies qui ont été définies. Notez l’État et l’identité (GUID) de chaque stratégie.

    Syntaxe`Get-InformationBarrierPolicy`

2. Pour définir une stratégie sur état actif, utilisez la cmdlet **Set-InformationBarrierPolicy** avec un paramètre **Identity** et le paramètre **State** défini sur **active**. 

    Syntaxe`Set-InformationBarrierPolicy -Identity GUID -State Active`

    Exemple : `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -State Active`
    
    Dans cet exemple, nous définissons une stratégie de barrière des informations qui a le GUID *43c37853-EA10-4b90-A23D-ab8c93772471* à Active Status.

    Répétez cette étape en fonction de chaque stratégie.

3. Une fois que vous avez défini vos stratégies de barrière des informations sur le statut actif, utilisez la cmdlet **Start-InformationBarrierPoliciesApplication** dans le centre de sécurité & conformité Office 365.

    Syntaxe`Start-InformationBarrierPoliciesApplication`

    Après une demi-heure environ, les stratégies sont appliquées, utilisateur par utilisateur, pour votre organisation. Si votre organisation est volumineuse, cette opération peut prendre 24 heures (ou plus). (En règle générale, il faut environ une heure pour traiter les comptes d’utilisateur 5 000.)

## <a name="view-status-of-user-accounts-segments-policies-or-policy-application"></a>Afficher l’état des comptes d’utilisateurs, des segments, des stratégies ou de l’application de stratégie

Avec PowerShell, vous pouvez afficher l’état des comptes d’utilisateur, des segments, des stratégies et de l’application de stratégie, comme décrit dans le tableau suivant.

|Pour afficher cette  |Procédez comme suit  |
|---------|---------|
|Comptes d’utilisateur     |Utilisez la cmdlet **Get-InformationBarrierRecipientStatus** avec les paramètres d’identité. <p>Syntaxe`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>` <p>Vous pouvez utiliser n’importe quelle valeur qui identifie de façon unique chaque utilisateur, comme le nom, l’alias, le nom unique, le nom de domaine canonique, l’adresse de messagerie ou le GUID. <p>Exemple : `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw` <p>Dans cet exemple, nous faisons référence à deux comptes d’utilisateur dans Office 365: *meganb* pour *Megan*, et *Alexw* pour *Alex*. <p>(Vous pouvez également utiliser cette applet de commande pour un seul `Get-InformationBarrierRecipientStatus -Identity <value>`utilisateur:) <p>Cette applet de commande retourne des informations sur les utilisateurs, telles que les valeurs d’attribut et les stratégies de barrière des informations qui sont appliquées.|
|Pertinents     |Utilisez la cmdlet **Get-OrganizationSegment** .<p>Syntaxe`Get-OrganizationSegment` <p>Cette opération permet d’afficher la liste de tous les segments définis pour votre organisation.         |
|Stratégies de barrière des informations     |Utilisez la cmdlet **Get-InformationBarrierPolicy** . <p> Syntaxe`Get-InformationBarrierPolicy` <p>Cette opération affiche la liste des stratégies de barrière des informations qui ont été définies, ainsi que leur état.       |
|Application de stratégie de barrière des informations la plus récente     | Utilisez la cmdlet **Get-InformationBarrierPoliciesApplicationStatus** . <p>Syntaxe`Get-InformationBarrierPoliciesApplicationStatus`<p>    Cela permet d’afficher des informations indiquant si l’application de stratégie a été exécutée, si elle a échoué ou est en cours d’exécution.       |
|Toutes les applications de stratégie de barrière des informations|Utilisant`Get-InformationBarrierPoliciesApplicationStatus -All $true`<p>Cela permet d’afficher des informations indiquant si l’application de stratégie a été exécutée, si elle a échoué ou est en cours d’exécution.|

## <a name="stop-a-policy-application"></a>Arrêter une application de stratégie

Si, après avoir commencé à appliquer des stratégies de barrière des informations, vous souhaitez arrêter l’application de ces stratégies, utilisez la procédure suivante. N’oubliez pas que le processus doit durer environ 30-35 minutes.

1. Pour afficher l’état de l’application de stratégie de barrière des informations la plus récente, utilisez la cmdlet **Get-InformationBarrierPoliciesApplicationStatus** .

    Syntaxe`Get-InformationBarrierPoliciesApplicationStatus`

    Notez le GUID de l’application.

2. Utilisez la cmdlet **Stop-InformationBarrierPoliciesApplication** avec un paramètre Identity.

    Syntaxe`Stop-InformationBarrierPoliciesApplication -Identity GUID`

    Exemple : `InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`

## <a name="edit-a-segment-or-a-policy"></a>Modifier un segment ou une stratégie

### <a name="edit-a-segment"></a>Modifier un segment

1. Pour afficher tous les segments existants, utilisez la cmdlet **Get-OrganizationSegment** .
    
    Syntaxe`Get-OrganizationSegment`

    Vous verrez une liste de segments et des détails pour chacune d’elles, comme le type de segment, sa valeur UserGroupFilter, l’auteur ou la dernière modification, GUID, etc.

    > [!TIP]
    > Imprimez ou enregistrez votre liste de segments pour référence ultérieure. Par exemple, si vous souhaitez modifier un segment, vous devez connaître son nom ou identifier la valeur (utilisée avec le paramètre Identity).

2. Pour modifier un segment, utilisez la cmdlet **Set-OrganizationSegment** avec le paramètre **Identity** et les détails pertinents. 

    Syntaxe`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`

    Exemple : `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`

    Dans cet exemple, pour le segment qui a le GUID *c96e0837-C232-4A8A-841e-ef45787d8fcd*, nous avons mis à jour le nom du service en «hrdept».

Une fois que vous avez terminé de modifier les segments de votre organisation, vous pouvez passer à [définir](#part-2-define-information-barrier-policies) ou [modifier](#edit-a-policy) des stratégies de barrière des informations.

### <a name="edit-a-policy"></a>Modifier une stratégie

1. Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .

    Syntaxe`Get-InformationBarrierPolicy`

    Dans la liste des résultats, identifiez la stratégie à modifier. Notez le GUID et le nom de la stratégie.

2. Utilisez la cmdlet **Set-InformationBarrierPolicy** avec un paramètre **Identity** et spécifiez les modifications que vous souhaitez effectuer.

    Syntaxe (bloquant les segments de la communication avec d’autres segments): 

    `Set-InformationBarrierPolicy -Identity GUID -SegmentsBlocked "segmentname, segmentname"` 

    Syntaxe (permettant aux segments de communiquer uniquement avec certains autres segments):
    
    ``Set-InformationBarrierPolicy -Identity GUID -SegmentsAllowed "segmentname, segmentname"``

    Exemple: Supposons qu’une stratégie a été définie pour bloquer la recherche de la communication avec les ventes et le marketing. La stratégie a été définie à l’aide de cette applet de commande:`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales, Marketing"`
    
    Supposons que nous voulons la modifier afin que les personnes de la recherche puissent uniquement communiquer avec des personnes dans RH. Pour effectuer cette modification, nous utilisons cette applet de commande:`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`

3. Lorsque vous avez terminé de modifier une stratégie, veillez à appliquer vos modifications. (Voir [appliquer des stratégies de barrière des informations](#part-3-apply-information-barrier-policies).)

### <a name="remove-a-policy"></a>Supprimer une stratégie

1. Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .

    Syntaxe`Get-InformationBarrierPolicy`

    Dans la liste des résultats, identifiez la stratégie à supprimer. Notez le GUID et le nom de la stratégie. Assurez-vous que la stratégie est définie sur état inactif.

2. Utilisez la cmdlet **Remove-InformationBarrierPolicy** avec un paramètre Identity.

    Syntaxe`Remove-InformationBarrierPolicy -Identity GUID`

    Exemple: Supposons que nous voulons supprimer une stratégie qui a le GUID *43c37853-EA10-4b90-A23D-ab8c93772471*. Pour ce faire, nous utilisons cette applet de commande:
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    Lorsque vous y êtes invité, confirmez la modification.

3. Répétez les étapes 1-2 pour chaque stratégie que vous souhaitez supprimer.

4. Lorsque vous avez terminé de supprimer des stratégies, appliquez vos modifications. Pour ce faire, utilisez l’applet de commande **Start-InformationBarrierPoliciesApplication** .

    Syntaxe`Start-InformationBarrierPoliciesApplication`

    Les modifications sont appliquées, utilisateur par utilisateur, pour votre organisation. Si votre organisation est volumineuse, cette opération peut prendre 24 heures (ou plus).

### <a name="set-a-policy-to-inactive-status"></a>Définir une stratégie sur état inactif

1. Pour afficher la liste des stratégies de barrière des informations actuelles, utilisez la cmdlet **Get-InformationBarrierPolicy** .

    Syntaxe`Get-InformationBarrierPolicy`

    Dans la liste des résultats, identifiez la stratégie que vous souhaitez modifier (ou supprimer). Notez le GUID et le nom de la stratégie.

2. Pour définir l’état de la stratégie sur inactive, utilisez la cmdlet **Set-InformationBarrierPolicy** avec un paramètre Identity et le paramètre State défini sur inactive.

    Syntaxe`Set-InformationBarrierPolicy -Identity GUID -State Inactive`

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    Dans cet exemple, nous définissons une stratégie de barrière des informations qui a un GUID *43c37853-EA10-4b90-A23D-ab8c9377247* à un état inactif.

3. Pour appliquer vos modifications, utilisez l’applet de commande **Start-InformationBarrierPoliciesApplication** .

    Syntaxe`Start-InformationBarrierPoliciesApplication`

    Les modifications sont appliquées, utilisateur par utilisateur, pour votre organisation. Si votre organisation est volumineuse, cette opération peut prendre 24 heures (ou plus). (En règle générale, il faut environ une heure pour traiter les comptes d’utilisateur 5 000.)

À ce stade, une ou plusieurs stratégies de barrière des informations sont définies sur l’état inactif. À partir de là, vous pouvez effectuer l’une des opérations suivantes:
- Conservez-le tel quel (une stratégie définie sur état inactif n’a aucun effet sur les utilisateurs)
- [Modifier une stratégie](#edit-a-policy) 
- [Supprimer une stratégie](#remove-a-policy)

## <a name="example-contosos-departments-segments-and-policies"></a>Exemple: services, segments et stratégies de contoso

Pour voir comment une organisation peut aborder la définition des segments et des stratégies, prenez en compte l’exemple suivant.

### <a name="contosos-departments-and-plan"></a>Services et plan de contoso

Contoso dispose de cinq services: RH, ventes, marketing, recherche et fabrication. Pour rester conformes aux réglementations industrielles, les personnes de certains services ne sont pas censées communiquer avec d’autres services, comme indiqué dans le tableau suivant:

|Segment  |Peut parler à  |Ne peut pas communiquer avec  |
|---------|---------|---------|
|HR     |Tout le monde         |(aucune restriction)         |
|Ventes     |RH, marketing, fabrication         |Recherche         |
|Marketing     |Tout le monde         |(aucune restriction)         |
|Recherche     |RH, marketing, fabrication        |Ventes     |
|Fabrication |RH, marketing |Toute personne autre que RH ou marketing |

Dans ce souci, le plan de contoso comprend trois stratégies de barrière des informations:

1. Stratégie conçue pour empêcher les ventes de communiquer avec la recherche (et une autre stratégie pour empêcher les recherches de communiquer avec les ventes)
2. Une stratégie conçue pour permettre à la production de communiquer avec les ressources humaines et marketing uniquement 

Il n’est pas nécessaire de définir des stratégies pour RH ou marketing.

### <a name="contosos-defined-segments"></a>Segments définis par contoso

Contoso utilise l’attribut de service dans Azure Active Directory pour définir des segments, comme suit:

|Service  |Définition de segment  |
|---------|---------|
|HR     | `New-OrganizationSegment -Name "HR" -UserGroupFilter "Department -eq 'HR'"`        |
|Ventes     | `New-OrganizationSegment -Name "Sales" -UserGroupFilter "Department -eq 'Sales'"`        |
|Marketing     | `New-OrganizationSegment -Name "Marketing" -UserGroupFilter "Department -eq 'Marketing'"`        |
|Recherche     | `New-OrganizationSegment -Name "Research" -UserGroupFilter "Department -eq 'Research'"`        |
|Fabrication     | `New-OrganizationSegment -Name "Manufacturing" -UserGroupFilter "Department -eq 'Manufacturing'"`        |

Une fois les segments définis, contoso passe à définir des stratégies. 

### <a name="contosos-information-barrier-policies"></a>Stratégies de barrière des informations de contoso

Contoso définit trois stratégies, comme décrit dans le tableau suivant:

|Stratégie  |Définition de la stratégie  |
|---------|---------|
|Stratégie 1: empêcher les ventes de communiquer avec la recherche     | `New-InformationBarrierPolicy -Name "Sales-Research" -AssignedSegment "Sales" -SegmentsBlocked "Research" -State Inactive` <p> Dans cet exemple, la stratégie de barrière des informations est appelée *Sales-Research*. Lorsque cette stratégie est active et appliquée, cela permet d’empêcher les utilisateurs qui se trouvent dans le segment des ventes de communiquer avec les utilisateurs du segment de recherche. Il s’agit d’une stratégie à sens unique; Il n’empêchera pas la recherche de communiquer avec les ventes. Pour cela, la stratégie 2 est requise.      |
|Policy 2: empêcher les recherches de communiquer avec les ventes     | `New-InformationBarrierPolicy -Name "Research-Sales" -AssignedSegment "Research" -SegmentsBlocked "Sales" -State Inactive` <p> Dans cet exemple, la stratégie de barrière des informations est appelée *Research-Sales*. Lorsque cette stratégie est active et appliquée, cela permet d’empêcher les utilisateurs qui se trouvent dans le segment de recherche de communiquer avec les utilisateurs du segment de ventes.       |
|Stratégie 3: autoriser la fabrication à communiquer avec RH et marketing uniquement     | `New-InformationBarrierPolicy -Name "Manufacturing-HRMarketing" -AssignedSegment "Manufacturing" -SegmentsAllowed "HR, Marketing" -State Inactive` <p>Dans ce cas, la stratégie de barrière des informations est appelée *Manufacturing-HRMarketing*. Lorsque cette stratégie est active et appliquée, la fabrication ne peut communiquer qu’avec RH et marketing. Notez que les ressources RH et marketing ne sont pas limitées à la communication avec d’autres segments. |

Une fois les segments et les stratégies définis, contoso applique les stratégies en exécutant l’applet de commande **Start-InformationBarrierPoliciesApplication** . 

Une fois cette configuration terminée, contoso est conforme aux exigences légales et industrielles.

## <a name="related-articles"></a>Articles connexes

[Obtenir une vue d’ensemble des barrières d’informations](information-barriers.md)

[En savoir plus sur les barrières d’informations dans Microsoft teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[Attributs des stratégies de barrière des informations (aperçu)](information-barriers-attributes.md)

[Dépannage des barrières relatives aux informations (aperçu)](information-barriers-troubleshooting.md)
