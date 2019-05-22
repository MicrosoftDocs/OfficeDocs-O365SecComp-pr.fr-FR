---
title: Expéditeur non vérifié
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Pour empêcher les messages de hameçonnage d’atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l’expéditeur est bien ce qu’il dit, et marquez les messages suspects comme courrier indésirable.
ms.openlocfilehash: 92458a93a4da3e449061e4d2a4ba312d635c42cc
ms.sourcegitcommit: 7f00f765e8fa674ce1c8c66f5b89b6bea45e13ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/22/2019
ms.locfileid: "34341622"
---
# <a name="unverified-sender"></a>Expéditeur non vérifié

Pour empêcher les messages de hameçonnage d’atteindre votre boîte aux lettres, Outlook.com et Outlook sur le Web Vérifiez que l’expéditeur est bien ce qu’il dit, et marquez les messages suspects comme courrier indésirable.

> [!IMPORTANT]
> Lorsqu’un message est marqué comme frauduleux de hameçonnage, Outlook.com et Outlook sur le Web affichent un avertissement en haut de la page, mais vous pouvez toujours ouvrir les liens figurant dans le message.

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a>Comment puis-je identifier un message suspect dans ma boîte de réception?

Outlook.com et Outlook sur le Web affichent des indicateurs lorsque l’expéditeur d’un message ne peut pas être identifié ou que son identité est différente de ce que vous voyez dans l’adresse de l’expéditeur.

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a>Comment gérer les messages qui reçoivent le traitement de l’expéditeur non vérifié 

Si vous êtes un client Office 365, vous pouvez gérer cette fonctionnalité via le centre de sécurité & Compliance Center. 

- Dans le centre de sécurité & de la sécurité d’Office 365, les administrateurs du client peuvent activer ou désactiver la fonctionnalité de protection contre l’usurpation d’identité dans le cadre de la stratégie anti-hameçonnage. En outre, elle peut être gérée via la cmdlet «Set-Antiphishpolicy permet». Pour plus d’informations, consultez la rubrique anti-phishing protection in Office 365 et Set-Antiphishpolicy permet.

    ![Modification des expéditeurs non authentifiés dans l’interface graphique.](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- Si un administrateur a identifié un faux positif et qu’un expéditeur ne doit pas recevoir le traitement de l’expéditeur non vérifié, il peut effectuer l’une des actions suivantes pour ajouter l’expéditeur à la liste des usurpations d’identité usurpée:
        
    - Ajoutez la paire de domaines par le biais de la vue d’aide à la décision. Pour plus d’informations, voir procédure pas à pas: usurpation d’information
                
    - Ajoutez la paire de domaines via l’applet de commande PhishFilterPolicy. Pour plus d’informations, voir Set-PhishFilterPolicy et protection contre la falsification dans Office 365

En outre, nous n’appliquons pas le traitement de l’expéditeur non vérifié s’il a été remis à la boîte de réception via une liste verte d’administration, y compris les règles de transport de messagerie (ETR), la liste des domaines approuvés (stratégie anti-spam), la liste des expéditeurs approuvés ou un utilisateur a défini cet utilisateur comme «expéditeur approuvé» dans son utilitaire.

### <a name="you-see-a--in-the-sender-image"></a>Un «?» apparaît dans l’image de l’expéditeur

Lorsque Outlook.com et Outlook sur le Web ne peuvent pas vérifier l’identité de l’expéditeur à l’aide des techniques d’authentification de messagerie, ils affichent un «?» dans la photo de l’expéditeur. 

![Le message n’a pas passé la vérification](media/message-did-not-pass-verification.jpg)

Les messages qui ne parvient pas à s’authentifier ne sont pas tous malveillants. Toutefois, vous devez être prudent quant à l’interaction avec les messages qui ne sont pas authentifiés si vous ne reconnaissez pas l’expéditeur. Ou, si vous reconnaissez un expéditeur qui ne possède pas de «?» normalement dans l’image de l’expéditeur, mais que vous le voyez soudainement, cela peut être un signe que l’expéditeur est usurpé.

## <a name="frequently-asked-questions"></a>Questions fréquemment posées

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a>Quels critères les Outlook.com et Outlook sur le Web utilisent-ils pour ajouter les propriétés «?» et «via»?

Pour le «?» de l’image de l’expéditeur: Outlook.com requiert que le message passe l’authentification SPF ou DKIM. Pour plus d’informations, reportez-vous à la rubrique [set up SPF in Office 365 pour éviter l’usurpation](set-up-spf-in-office-365-to-help-prevent-spoofing.md) et l' [utilisation de DKIM pour valider les messages sortants envoyés à partir de votre domaine personnalisé dans Office 365](use-dkim-to-validate-outbound-email.md).

Pour la balise via: si le domaine de l’adresse de l’expéditeur est différent du domaine dans la signature DKIM ou SMTP MAIL FROM, Outlook.com affiche le domaine dans l’un de ces deux champs (en préférant la signature DKIM).

### <a name="how-do-i-remove-the-"></a>Comment supprimer le «?»?

Pour le «?» de l’image de l’expéditeur: en tant qu’expéditeur, vous devez authentifier votre message avec SPF ou DKIM.

Pour la balise via: en tant qu’expéditeur, vous devez vous assurer que le domaine dans la signature DKIM ou SMTP MAIL FROM est le même que le domaine de l’adresse de provenance ou qu’il s’agit d’un sous-domaine de celui-ci.

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a>Est-ce que Outlook.com et Outlook sur le Web s’affichent pour chaque message qui ne passe pas l’authentification?

Pas nécessairement. Outlook.com et Outlook sur le Web peuvent avoir d’autres propriétés dans le message pour authentifier l’expéditeur.

## <a name="related-topics"></a>Sujets associés

[Protéger votre compte de messagerie Outlook.com](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[Gérer les abus, le hameçonnage ou l’usurpation d’identité dans Outlook.com](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[Filtrage du courrier indésirable et du courrier indésirable dans Outlook sur le Web](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
