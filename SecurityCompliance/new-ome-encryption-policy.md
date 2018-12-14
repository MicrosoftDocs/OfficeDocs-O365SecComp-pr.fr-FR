---
title: Nouvelle stratégie de chiffrement de messages Office 365 pour les informations sensibles
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 12/13/2018
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Nouvelle Office 365 Message Encryption stratégie pour plus d’informations sensibles.'
ms.openlocfilehash: 180050d1bf9303f6d29bc126e66ac53211c2fb34
ms.sourcegitcommit: 3aae959ea1ac5ef61a9942c681d334831e6b6038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2018
ms.locfileid: "27271090"
---
# <a name="new-office-365-message-encryption-policy-for-sensitive-information"></a>Nouvelle stratégie de chiffrement de messages Office 365 pour les informations sensibles

Nous allons créer une nouvelle stratégie automatique dans les clients Office 365 qui seront appliqueront chiffrement de messages Office 365 pour tous les messages électroniques qui contiennent des informations sensibles et qui sont envoyées à l’extérieur de votre organisation. Cette nouvelle règle de flux de messagerie Exchange sera automatiquement créée dans votre organisation cliente Office 365 afin que votre organisation est protégée par défaut.

## <a name="how-will-this-work"></a>Comment fonctionnera-t-il ?

Votre organisation reçoit une notification dans le centre de messages Office 365 pour vous avertir de la date à laquelle cette stratégie automatique sera créée dans votre client. Vous avez au moins un avis de 30 jours et vous aurez également l’option Annuler l’abonnement. Un scénario dans lequel vous souhaitez pouvez potentiellement exclure est si vous disposez d’une solution de protection contre la perte de données 3 rd tiers qui analyse déjà pour les types de sensibles.

## <a name="new-policy-details"></a>Détails de la nouvelle stratégie

Une nouvelle règle de flux de messagerie Exchange sera créée dans votre organisation qui sera chiffrer automatiquement sur le point à l’extérieur de votre organisation avec les messages électroniques le *Chiffrer seule* stratégie s’ils contiennent les informations sensibles suivants :

- Numéro de routage ABA
- Numéro de carte de crédit
- Numéro de l’application Agency (DEA) Drug Enforcement
- US / numéro de passeport britannique
- Numéro de compte bancaire US
- Numéro d'identification fiscale individuel (ITIN) États-Unis
- Numéro de sécurité sociale (SSN) États-Unis

> [!Note]
> Les types sensibles exactes peuvent varier par les paramètres régionaux de votre organisation et communiquées dans la notification de centre de messages.

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a>Que dois-je faire pour préparer pour que cette modification ?

Il est inutile de mettre à jour ou modifier les paramètres de configuration d’Office 365 existants avant cette modification nouveau. Toutefois, vous souhaiterez peut-être mettre à jour de n’importe quel utilisateur final applicable documentation et des supports de formation pour préparer les personnes dans votre organisation pour que cette modification.

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a>Comment ce changement est représenté dans le journal d’Audit ?

Cette activité est analysée et est disponible pour les clients.  L’opération est 'New-TransportRule' et un extrait d’un exemple d’entrée d’audit à partir de la recherche dans le centre de conformité et de sécurité du journal d’Audit est ci-dessous :

|     |
| --- |
| *{« CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 », « RecordType » : 1, « ResultStatus » : « True », « UserKey » : « Opérateur Microsoft », » UserType » : 3, « Version » : 1, « charges de travail » : « Exchange », « ClientIP » : « 123.456.147.68:17584 », « ObjectId » : « UserId «, » » : « Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX () 15.20.1382.008)","Parameters » : {« Name » : « Organisation », « Valeur » : « d 123456-221-12346"{« Name » : « ApplyRightsProtectionTemplate », « Valeur » : « Chiffrer »}, {« Name » : « Nom », « Valeur » : « Chiffrer les messages électroniques sensibles sortants (hors de règle de zone) »}, {« Name » : » MessageContainsDataClassifications »... etc..*
 |

## <a name="how-do-i-opt-out"></a>Comment I annulations ?

Si vous souhaitez les annulations de ce changement, procédez comme suit :

1. Connectez-vous à [Exchange Online PowerShell](https://aka.ms/exopowershell) en tant qu’utilisateur doté du rôle Administrateur général.
2.  Exécutez le code suivant après l’authentification :

    ```
    Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
    ```

## <a name="how-do-i-disable-the-automatic-policy"></a>Comment désactiver la stratégie automatique ?

Si vous n’avez pas annulations de ce changement et la règle de courrier Exchange a déjà été créée, vous pouvez [désactiver la règle](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) à partir de **flux de messagerie** > **règles** dans Exchange admin center (EAC) et désactiver la règle «*chiffrer sortant les messages électroniques sensibles (hors de règle de zone)*».
