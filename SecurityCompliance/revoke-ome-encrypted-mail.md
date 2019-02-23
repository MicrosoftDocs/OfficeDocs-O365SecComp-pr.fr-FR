---
title: Révoquer des e-mails chiffrés par le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: En tant qu'administrateur Office 365, vous pouvez révoquer certains courriers électroniques chiffrés avec le chiffrement de messages Office 365.
ms.openlocfilehash: 75b5e46e25f447ddac0de5a7911d0df8385da6b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214894"
---
# <a name="office-365-message-encryption-email-revocation"></a>Révocation de courrier de chiffrement de messages Office 365

Cet article fait partie d'une série d'articles plus large sur le chiffrement de [messages Office 365](ome.md). Pour l'instant, la révocation des messages chiffrés est en préversion. Prévoyez des mises à jour et des modifications apportées à la fonctionnalité et au contenu pour améliorer notre offre.

Il peut s'avérer nécessaire de révoquer un e-mail qui a déjà été envoyé. Si le courrier électronique a été chiffré à l'aide du chiffrement de messages Office 365 et que vous êtes un administrateur d'Office 365, vous pouvez le faire pour le courrier électronique dans certaines conditions. Cet article décrit les circonstances dans lesquelles cela est possible et comment procéder.
  
## <a name="encrypted-emails-that-you-can-revoke"></a>Messages chiffrés que vous pouvez révoquer

Vous pouvez révoquer les messages électroniques chiffrés si le destinataire a reçu un message électronique chiffré, basé sur une liaison. Si le destinataire a reçu une expérience Inline native dans un client Outlook pris en charge, ces messages électroniques ne peuvent pas être révoqués.

Si un destinataire reçoit une expérience basée sur la liaison ou si une expérience en ligne dépend du type d'identité du destinataire: Office 365 et les destinataires de comptes Microsoft (par exemple, les utilisateurs outlook.com) obtiennent une expérience inline dans les clients Outlook pris en charge. Tous les autres types de destinataires, tels que les destinataires Gmail, bénéficient d'une expérience basée sur les liens.

Bientôt, les organisations pourront forcer une expérience basée sur la liaison indépendamment de l'identité du destinataire. De cette manière, tous les destinataires recevront un message électronique avec un lien vers le portail de chiffrement des messages Office 365 où ils pourront lire et répondre à des messages chiffrés. Tous les messages électroniques chiffrés seront révocables.
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a>Expérience de destinataire pour les messages électroniques chiffrés révoqués

Une fois qu'un e-mail a été révoqué, le destinataire obtiendra une erreur lors de la tentative d'accès au courrier chiffré via le portail de chiffrement des messages Office 365: «le message a été révoqué par l'expéditeur».

![Capture d'écran illustrant un message électronique chiffré révoqué.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a>Procédure de révocation d'un message électronique chiffré

### <a name="step-1-obtain-the-message-id-of-the-email"></a>Étape 1. Obtenir l'ID de message de l'e-mail

Avant de pouvoir révoquer un courrier chiffré, vous devez recueillir l'ID du message. Le MessageId se présente généralement au format suivant:

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

Il existe plusieurs façons de trouver l'ID de message de l'e-mail à révoquer. Cette section décrit quelques options, mais vous pouvez utiliser n'importe quelle méthode qui fournit l'ID.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a>Pour identifier l'ID de message du courrier électronique à révoquer à l'aide du suivi des messages &amp; dans le centre de sécurité conformité

1. Recherchez le courrier électronique envoyé par l'expéditeur ou le destinataire à l'aide du [nouveau suivi des messages dans le centre de sécurité & de la sécurité d'Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).
2. Une fois que vous avez trouvé le message, sélectionnez-le pour afficher le volet **Détails du suivi des messages** . Pour **plus d'informations** , reportez-vous à l'ID du message.

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a>Pour identifier l'ID de message du courrier électronique à révoquer à l'aide des rapports de chiffrement de &amp; messages Office dans le centre de sécurité conformité

1. Dans le centre &amp; de sécurité conformité, accédez au **rapport**de chiffrement des messages.
2. Sélectionnez le tableau **afficher les détails** et identifiez le message à révoquer.
3. Double-cliquez sur le message pour afficher les détails qui incluent l'ID du message.

### <a name="step-2-verify-that-the-mail-is-revocable"></a>Étape 2. Vérifier que le message est révocable

Pour vérifier si vous pouvez ou non révoquer un message électronique particulier, procédez comme suit.

1. À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-OMEMessageStatus comme suit:
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   Cette valeur renvoie l'objet du message et indique si le message est révocable. Par exemple,

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a>Étape 3. Révoquer le courrier  

Une fois que vous avez identifié l'ID du message que vous souhaitez révoquer, et que vous avez vérifié que le message est révocable, vous pouvez le révoquer à l'aide de la cmdlet Set-OMEMessageRevocation.

1. [Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Exécutez la cmdlet Set-OMEMessageRevocation comme suit:

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. Pour vérifier si l'e-mail a été révoqué, exécutez la cmdlet Get-OMEMessageStatus comme suit:

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    Si la révocation a réussi, l'applet de commande renvoie le résultat suivant:  

    `Revoked: True`
