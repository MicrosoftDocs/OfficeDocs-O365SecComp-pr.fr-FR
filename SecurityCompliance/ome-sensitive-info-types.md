---
title: Nouvelle stratégie de chiffrement de messages Office 365 pour les informations sensibles
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/16/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Appliqué automatiquement la stratégie de chiffrement de messages Office 365 pour les types d’informations sensibles présentant à tous les clients.'
ms.openlocfilehash: f83bf0fe572586b3becf2dd53395e611bdaaea24
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614378"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>Stratégie de chiffrement de messages Office 365 pour les informations sensibles

Pour un groupe de clients, en fonction de leur taille de l’organisation et la complexité des flux de messagerie, nous effectuons un déploiement lente d’une nouvelle stratégie automatique dans les clients Office 365 qui s’appliqueront chiffrement de messages Office 365 pour les messages électroniques contenant certains types de critiques plus d’informations. Nous sommes le test avec un petit groupe de clients. Cette stratégie sera déployée pas toutes les organisations et des considérations comme taille de l’organisation et la complexité du flux de messagerie sera utilisée pour déterminer le droit à ce déploiement. Si votre organisation est activée pour ce déploiement, vous recevrez une notification dans le centre de messages Office 365 pour vous avertir de la date à laquelle cette stratégie automatique sera créée et vous aurez au moins un avis de 30 jours et l’option Annuler l’abonnement. Si vous ne souhaitez pas attendre que Microsoft créer cette stratégie et que vous souhaitez faire vous-même, vous pouvez créer cette stratégie automatique à l’aide de règles de flux de messagerie Exchange.

## <a name="when-to-expect-the-update-for-your-tenant"></a>Quand la mise à jour pour votre client

Votre organisation reçoit une notification dans le centre de messages Office 365 pour vous avertir de la date à laquelle cette stratégie automatique sera créée dans votre client. Vous avez au moins un avis de 30 jours et vous aurez également l’option Annuler l’abonnement. Un scénario dans lequel vous souhaitez pouvez potentiellement exclure est si vous disposez d’une solution de protection contre la perte de données 3 rd tiers qui analyse déjà pour les types de sensibles. Plus d’informations sur la façon d’annulations sont disponibles plus loin dans cet article.

## <a name="sensitive-information-type-policy-details"></a>Détails de la stratégie type des informations sensibles

Une règle de flux de messagerie Exchange sera créée dans votre organisation qui sera chiffrer automatiquement sur le point à l’extérieur de votre organisation avec les messages électroniques le *Chiffrer seule* stratégie si les e-mails ou les pièces jointes contient les types d’informations sensibles suivants :

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

Il est inutile de mettre à jour ou modifier les paramètres de configuration d’Office 365 existants avant cette modification nouveau. Toutefois, vous souhaiterez peut-être mettre à jour de n’importe quel utilisateur final applicable documentation et des supports de formation pour préparer les personnes dans votre organisation pour que cette modification. Partager ces ressources Office 365 Message Encryption avec vos utilisateurs selon le cas :

- [Envoyer, consulter et répondre aux messages chiffrés dans Outlook pour PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Office 365 Essentials vidéo : Chiffrement de messages Office](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a>Comment ce changement est représenté dans le journal d’Audit ?

Cette activité est analysée et est disponible pour les clients.  L’opération est 'New-TransportRule' et un extrait d’un exemple d’entrée d’audit à partir de la recherche du journal d’Audit de sécurité & centre de conformité est ci-dessous :

|     |
| --- |
| *{« CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 », « RecordType » : 1, « ResultStatus » : « True », « UserKey » : « Opérateur Microsoft », » UserType » : 3, « Version » : 1, « charges de travail » : « Exchange », « ClientIP » : « 123.456.147.68:17584 », « ObjectId » : « UserId «, » » : « Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX () 15.20.1382.008)","Parameters » : {« Name » : « Organisation », « Valeur » : « d 123456-221-12346"{« Name » : « ApplyRightsProtectionTemplate », « Valeur » : « Chiffrer »}, {« Name » : « Nom », « Valeur » : « Chiffrer les messages électroniques sensibles sortants (hors de règle de zone) »}, {« Name » : » MessageContainsDataClassifications »... etc..*
 |

## <a name="how-do-i-opt-out"></a>Comment I annulations ?

Si vous souhaitez les annulations de ce changement, procédez comme suit :

1. À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).
2. Exécutez l’applet de commande Set-IRMConfiguration comme suit :

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-or-customize-the-automatic-policy"></a>Comment désactiver ou personnaliser la stratégie automatique ?

Si vous n’avez pas annulations de ce changement et la règle de flux de messagerie Exchange a déjà été créée, vous pouvez [désactiver ou modifier la règle](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) à partir de **flux de messagerie** > **règles** dans Exchange admin center (EAC) et désactiver la règle «*chiffrer les messages électroniques sensibles sortants (hors de règle de zone)*».
