---
title: Créer une stratégie de type d’informations sensibles pour votre entreprise à l’aide du chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Résumé: stratégie de chiffrement des messages Office 365 pour les types d’informations sensibles.'
ms.openlocfilehash: 44966303ec7c58fdd82f733e1922073de848cf73
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834833"
---
# <a name="create-a-sensitive-information-type-policy-for-your-organization-using-office-365-message-encryption"></a>Créer une stratégie de type d’informations sensibles pour votre entreprise à l’aide du chiffrement de messages Office 365

Vous pouvez utiliser les règles de flux de messagerie Exchange ou la protection contre la perte de données (DLP) d’Office 365 pour créer une stratégie de type d’informations sensibles avec le chiffrement de messages Office 365. Pour créer une règle de flux de messagerie Exchange, vous pouvez utiliser le centre d’administration Exchange ou PowerShell.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>Pour créer la stratégie à l’aide de règles de flux de messagerie dans le centre d’administration Exchange

Connectez-vous au centre d’administration Exchange et accédez à **mail Flow** > **Rules**. Sur la page règles, créez une règle qui applique le chiffrement de messages Office 365. Vous pouvez créer une règle basée sur des conditions telles que la présence de certains mots clés ou types d’informations sensibles dans le message ou la pièce jointe.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>Pour créer la stratégie à l’aide de règles de flux de messagerie dans PowerShell

Utiliser un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell). Utilisez les cmdlets Set-IRMConfiguration et New-TransportRule pour créer la stratégie.

### <a name="example-mail-flow-rule-created-with-powershell"></a>Exemple de règle de flux de messagerie créée avec PowerShell

Exécutez les commandes suivantes dans PowerShell pour créer une règle de flux de messagerie Exchange qui chiffre automatiquement les courriers électroniques envoyés à l’extérieur de votre organisation à l’aide de la stratégie de *chiffrement uniquement* si les messages électroniques ou leurs pièces jointes contiennent les informations sensibles suivantes. catégories

- Numéro d’acheminement ABA
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

Après qu’Office 365 a chiffré un message, les destinataires ont un accès illimité aux pièces jointes lorsqu’ils accèdent à leur message chiffré et l’ouvrent.

## <a name="to-prepare-for-this-change"></a>Pour préparer cette modification

Vous souhaiterez peut-être mettre à jour les documents de formation et la documentation utilisateur final applicables pour préparer les personnes de votre organisation à ce changement. Partagez ces ressources de chiffrement de messages Office 365 avec vos utilisateurs selon vos besoins:

- [Envoyer, afficher et répondre à des messages chiffrés dans Outlook pour PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Vidéo Office 365 Essentials: chiffrement de messages Office](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>Afficher ces modifications dans le journal d’audit

Office 365 audite cette activité et la rend accessible aux administrateurs d’Office 365. L’opération est «New-TransportRule» et un extrait d’un exemple d’entrée d’audit de la recherche de journal d’audit dans Security & Compliance Center est inférieur à:

```text
*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*
```

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>Pour désactiver ou personnaliser la stratégie de types d’informations sensibles

Une fois que vous avez créé la règle de flux de messagerie Exchange, vous pouvez [désactiver ou modifier la règle](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) en accédant aux**règles** de **flux** > de messagerie dans le centre d’administration Exchange et désactiver la règle «*chiffrement des messages électroniques sensibles sortants (règle de désactivation de la case)* . ".
