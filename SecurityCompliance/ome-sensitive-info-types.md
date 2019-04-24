---
title: Stratégie de chiffrement des messages Office 365 pour les informations sensibles
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: "Résumé: la stratégie de chiffrement des messages Office 365 pour les types d'informations sensibles est désormais disponible."
ms.openlocfilehash: 99cb7a9f94c9cf4036c11b74a5208ddf0e819ceb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261262"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>Stratégie de chiffrement des messages Office 365 pour les informations sensibles

Mise à jour (1/30/19): en octobre 2018, nous avons utilisé un petit échantillon de clients pour comprendre si nous pouvons simplifier la protection en chiffrant automatiquement les messages électroniques sensibles en fonction de certains types d'informations sensibles. En fonction des commentaires positifs de cet exemple, nous avons décidé de développer vers un profil plus diversifié de clients en décembre 2018. Après avoir communiqué le déploiement suivant pour sélectionner des clients, nous avons écouté vos commentaires et déterminé que les clients avec des environnements plus complexes souhaitaient implémenter les règles plus facilement et nous ajustons donc nos offres.

Si votre organisation a été sélectionnée pour le lancement du 15 janvier 2019, nous n'allons pas déployer la stratégie automatique. Au lieu de cela, nous fournissons des instructions dans cet article expliquant comment effectuer le déploiement. Poursuivez votre lecture pour en savoir plus.

||
|:-----|
|Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins. |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a>Procédure de création de la stratégie de type d'informations sensibles pour votre client

Vous pouvez utiliser les règles de flux de messagerie Exchange ou la protection contre la perte de données (DLP) d'Office 365 pour créer la stratégie de type d'informations sensibles. Pour créer une règle de flux de messagerie Exchange, vous pouvez utiliser le centre d'administration Exchange ou PowerShell.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>Pour créer la stratégie à l'aide de règles de flux de messagerie dans le centre d'administration Exchange

Connectez-vous au centre d'administration Exchange et accédez à **mail Flow** > **Rules**. Il s'agit de créer une règle qui applique le chiffrement de messages Office 365 en fonction de conditions telles que la présence de certains mots clés ou types d'informations sensibles dans le message ou la pièce jointe.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>Pour créer la stratégie à l'aide de règles de flux de messagerie dans PowerShell

À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell). Utilisez les cmdlets Set-IRMConfiguration et New-TransporRule pour créer la stratégie.

### <a name="example-mail-flow-rule-created-with-powershell"></a>Exemple de règle de flux de messagerie créée avec PowerShell

L'exécution des commandes suivantes dans PowerShell crée une règle de flux de messagerie Exchange qui chiffre automatiquement les messages électroniques en dehors de votre organisation à l'aide de la stratégie de *chiffreMent uniquement* si les messages électroniques ou leurs pièces jointes contiennent les éléments sensibles suivants. types d'informations:

- Numéro d'acheminement ABA
- Numéro de carte de crédit
- Numéro de la Loi sur la mise en œuvre du médicament (DEA)
- ANGLAIS (ÉTATS-UNIS) numéro de passeport
- Numéro de compte bancaire américain
- Numéro d’identification fiscale individuel (ITIN) États-Unis
- Numéro de sécurité sociale (SSN) États-Unis

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a>Comment les destinataires accèdent aux pièces jointes

Une fois qu'un message est chiffré, les destinataires ont un accès illimité aux pièces jointes une fois qu'ils ont accès et ouvert leur courrier électronique chiffré.

## <a name="to-prepare-for-this-change"></a>Pour préparer cette modification

Vous souhaiterez peut-être mettre à jour les documents de formation et la documentation utilisateur final applicables pour préparer les personnes de votre organisation à ce changement. Partagez ces ressources de chiffrement de messages Office 365 avec vos utilisateurs selon vos besoins:

- [Envoyer, afficher et répondre à des messages chiffrés dans Outlook pour PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Vidéo Office 365 Essentials: chiffrement de messages Office](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>Afficher ces modifications dans le journal d'audit

Cette activité est auditée et disponible pour les administrateurs d'Office 365. L'opération est «New-TransportRule» et un extrait d'un exemple d'entrée d'audit de la recherche de journal d'audit dans Security & Compliance Center est inférieur à:

|     |
| --- |
| *{"CreationTime": "2018-11-28T23:35:01", "ID": "A1b2C3d4-DAA0-4c4f-A019-03a1234a1b0c", "Operation": "New-TransportRule", "": "123456-221d-12345", "RecordType": 1, "ResultStatus": "true", "UserKey": "opérateur Microsoft", " UserType ": 3," version ": 1," Workload ":" Exchange "," ClientIP ":" 123.456.147.68:17584 "," ObjectId ":" "," UserId ":" Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso. onmicrosoft. com "," OriginatingServer ":" CY4PR13MBXXXX ( 15.20.1382.008) "," paramètres ": {" Name ":" Organization "," value ":" 123456-221d-12346 "{" Name ":" ApplyRightsProtectionTemplate "," value ":" Encrypt "}, {" Name ":" Name "," value ":" chiffrer les messages électroniques sensibles sortants (règle de non-boîte) "}, {" nom ":" MessageContainsDataClassifications "... etc.* |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>Pour désactiver ou personnaliser la stratégie de types d'informations sensibles

Une fois que vous avez créé la règle de flux de messagerie Exchange, vous pouvez [désactiver ou modifier la règle](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) en accédant aux**règles** de **flux** > de messagerie dans le centre d'administration Exchange et désactiver la règle «*chiffrement des messages électroniques sensibles sortants (règle de désactivation de la case)* . ".
