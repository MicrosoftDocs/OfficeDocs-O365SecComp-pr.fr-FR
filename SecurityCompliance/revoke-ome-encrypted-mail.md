---
title: Révoquer les e-mails chiffrés par le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: En tant qu’administrateur Office 365, vous pouvez révoquer certains courriers électroniques chiffrés avec Office 365 Advanced message Encryption.
ms.openlocfilehash: 098ce50791152c8bbb4e4692d6fb85e4c2c7cb58
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156786"
---
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a>Révoquer les e-mails chiffrés par le chiffrement de messages Office 365

La révocation de messagerie est proposée dans le cadre du chiffrement avancé des messages Office 365. Le chiffrement de messages avancé Office 365 est disponible en haut du chiffrement des messages Office 365 dans certains abonnements. Le chiffrement de messages avancé est inclus dans [Microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 entreprise E5 et Office 365 éducation a5. Si votre organisation possède un abonnement Office 365 qui n’inclut pas le chiffrement de messages avancé Office 365, vous pouvez acheter le chiffrement de messages avancé comme module complémentaire avec E5 conformité de la référence SKU de conformité avancée.

Cet article fait partie d’une série d’articles plus large sur le chiffrement de [messages Office 365](ome.md).

Il peut s’avérer nécessaire de révoquer un e-mail qui a déjà été envoyé. Si le courrier électronique a été chiffré à l’aide du chiffrement de messages avancé Office 365 et que vous êtes un administrateur d’Office 365, vous pouvez le faire pour le courrier électronique dans certaines conditions. Cet article décrit les circonstances dans lesquelles cela est possible et comment procéder.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>Messages chiffrés que vous pouvez révoquer

Vous pouvez révoquer les messages électroniques chiffrés si le destinataire a reçu un message électronique chiffré, basé sur une liaison. Si le destinataire a reçu une expérience Inline native dans un client Outlook pris en charge, ces messages électroniques ne peuvent pas être révoqués.

Si un destinataire reçoit une expérience basée sur la liaison ou si une expérience en ligne dépend du type d’identité du destinataire: Office 365 et les destinataires de comptes Microsoft (par exemple, les utilisateurs outlook.com) obtiennent une expérience inline dans les clients Outlook pris en charge. Tous les autres types de destinataires, tels que les destinataires Gmail, bénéficient d’une expérience basée sur les liens.

## <a name="recipient-experience-for-revoked-encrypted-emails"></a>Expérience de destinataire pour les messages électroniques chiffrés révoqués

Une fois qu’un e-mail a été révoqué, le destinataire obtiendra une erreur lors de la tentative d’accès au courrier chiffré via le portail de chiffrement des messages Office 365: «le message a été révoqué par l’expéditeur».

![Capture d’écran illustrant un message électronique chiffré révoqué.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a>Procédure de révocation d’un message électronique chiffré

### <a name="step-1-obtain-the-message-id-of-the-email"></a>Étape 1. Obtenir l’ID de message de l’e-mail

Avant de pouvoir révoquer un courrier chiffré, vous devez recueillir l’ID du message. Le MessageId se présente généralement au format suivant:

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

Il existe plusieurs façons de trouver l’ID de message de l’e-mail à révoquer. Cette section décrit quelques options, mais vous pouvez utiliser n’importe quelle méthode qui fournit l’ID.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>Pour identifier l’ID de message du courrier électronique à révoquer à l’aide du suivi des messages &amp; dans le centre de sécurité conformité

1. Recherchez le courrier électronique envoyé par l’expéditeur ou le destinataire à l’aide du [nouveau suivi des messages dans le centre de sécurité & de la sécurité d’Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).

2. Une fois que vous avez localisé l’e-mail, sélectionnez-le pour afficher le volet **Détails du suivi des messages** . Pour **plus d’informations** , reportez-vous à l’ID du message.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>Pour identifier l’ID de message du courrier électronique à révoquer à l’aide des rapports de chiffrement de &amp; messages Office dans le centre de sécurité conformité

1. Dans le centre &amp; de sécurité conformité, accédez au **rapport**de chiffrement des messages.

2. Sélectionnez le tableau **afficher les détails** et identifiez le message à révoquer.

3. Double-cliquez sur le message pour afficher les détails qui incluent l’ID du message.

### <a name="step-2-verify-that-the-mail-is-revocable"></a>Étape 2. Vérifier que le message est révocable

Pour vérifier si vous pouvez révoquer un message électronique particulier, vérifiez si le champ État de révocation est visible **** dans le tableau des détails &amp; du centre de sécurité et de conformité.

Pour vérifier si vous pouvez ou non révoquer un message électronique particulier à l’aide de Windows PowerShell, procédez comme suit.

1. À l’aide d’un compte professionnel ou scolaire doté d’autorisations d’administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-OMEMessageStatus comme suit:

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   Cette valeur renvoie l’objet du message et indique si le message est révocable. For example,

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a>Étape 3. Révoquer le courrier  

Une fois que vous avez identifié l’ID du message que vous souhaitez révoquer, et que vous avez vérifié que le message est révocable, vous pouvez révoquer le courrier électronique.

Pour révoquer le message électronique dans &amp; le centre de sécurité conformité, dans le tableau des **Détails** , sélectionnez **révoquer**.

Vous pouvez révoquer un courrier électronique à l’aide de Windows PowerShell à l’aide de la cmdlet Set-OMEMessageRevocation.

1. [Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-OMEMessageRevocation comme suit:

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. Pour vérifier si l’e-mail a été révoqué, exécutez la cmdlet Get-OMEMessageStatus comme suit:

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    Si la révocation a réussi, l’applet de commande renvoie le résultat suivant:  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a>Plus d’informations sur le chiffrement de messages avancé Office 365

- [Chiffrement de messages avancé Office 365](ome-advanced-message-encryption.md)

- [Office 365 Advanced message Encryption: expiration du courrier électronique](ome-advanced-expiration.md)

- [Description du service de conformité et de stratégie de message](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)