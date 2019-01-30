---
title: Révoquer des e-mails chiffrés par le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/29/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: En tant qu’un administrateur Office 365, vous pouvez retirer certains messages électroniques chiffrés avec Office 365 Message Encryption.
ms.openlocfilehash: a3f5c08d2c8660e56c378fc5fa7a850ff2c12eb5
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614388"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="aaa3d-103">Révocation de courrier électronique de chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="aaa3d-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="aaa3d-p101">Cet article fait partie d’une plus grande série d’articles sur [Office 365 Message Encryption](ome.md). Révocation de messagerie chiffrée maintenant droite est en mode Aperçu. Prévoient des mises à jour et les modifications apportées à la fonctionnalité et le contenu afin d’améliorer notre offre.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="aaa3d-p102">Vous serez peut-être amené à révoquer un courrier électronique qui a déjà été envoyé. Si le message électronique a été chiffré à l’aide du chiffrement de messages Office 365 et que vous êtes un administrateur Office 365, vous pouvez le faire pour le courrier électronique sous certaines conditions. Cet article décrit sous quelles conditions cela est possible et comment le faire.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="aaa3d-110">Messages électroniques chiffrés que vous pouvez annuler</span><span class="sxs-lookup"><span data-stu-id="aaa3d-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="aaa3d-p103">Vous pouvez annuler les messages électroniques chiffrés si le destinataire a reçu une base de liens, marque électroniques chiffrés. Si le destinataire a reçu une expérience native insérée dans un client Outlook pris en charge, les messages électroniques ne peut pas être révoqués.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="aaa3d-p104">Si un destinataire reçoit une expérience basée sur un lien ou une expérience en ligne varie selon le type de destinataire d’identité : Office 365 et Microsoft Account destinataires (par exemple, les utilisateurs outlook.com) obtenir une expérience en ligne dans les clients Outlook pris en charge. Tous les autres types destinataires, tel que Gmail destinataires, obtenez une expérience basée sur le lien.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="aaa3d-p105">Bientôt disponible, organisations auront la possibilité de forcer une expérience basée sur le lien quel que soit l’identité du destinataire. De cette manière, tous les destinataires recevront un message électronique personnalisé avec un lien vers le portail Office 365 Message Encryption où ils seront en mesure de lire et répondre aux messages électroniques chiffrés. Ces messages électroniques chiffrés sera révocables.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="aaa3d-118">Expérience de destinataire pour les messages électroniques chiffrés révoquées</span><span class="sxs-lookup"><span data-stu-id="aaa3d-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="aaa3d-119">Une fois qu’un message électronique a été révoqué, le destinataire obtenez une erreur lorsque vous essayez d’accéder à du message électronique chiffré via le portail Office 365 Message Encryption : « le message a été révoqué par l’émetteur ».</span><span class="sxs-lookup"><span data-stu-id="aaa3d-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Capture d’écran montrant une révoquées de messages électroniques chiffrés.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="aaa3d-121">Comment révoquer un message électronique chiffré</span><span class="sxs-lookup"><span data-stu-id="aaa3d-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="aaa3d-p106">Étape 1. Obtenir l’ID de Message du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="aaa3d-p107">Avant que vous pouvez retirer un message chiffré, vous devez recueillir l’ID de Message du courrier électronique. L’ID du message est généralement au format :</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="aaa3d-p108">Il existe plusieurs manières pour trouver l’ID de Message du courrier électronique que vous souhaitez révoquer. Cette section décrit quelques options, mais vous pouvez utiliser une méthode qui fournit le code.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="aaa3d-128">Pour identifier l’ID de Message du courrier électronique que vous souhaitez révoquer à l’aide de suivi des messages dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="aaa3d-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="aaa3d-129">Recherchez le courrier électronique par l’expéditeur ou destinataire utilisant le [Nouveau suivi des messages dans Office 365 sécurité & centre de conformité](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="aaa3d-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="aaa3d-p109">Une fois que vous avez trouvé le courrier électronique sélectionner pour afficher le volet de **Détails de suivi des messages** . Développez **Plus d’informations** pour localiser l’ID du Message.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="aaa3d-132">Pour identifier l’ID de Message du courrier électronique que vous souhaitez révoquer à l’aide de rapports de chiffrement de messages Office dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="aaa3d-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="aaa3d-133">Dans la sécurité &amp; centre de conformité, accédez au **Rapport de chiffrement des messages**.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="aaa3d-134">Choisissez la table **d’Afficher les détails** et d’identifier le message que vous souhaitez révoquer.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="aaa3d-135">Double-cliquez sur le message pour afficher les détails qui incluent l’ID de Message.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-revoke-the-mail"></a><span data-ttu-id="aaa3d-p110">Étape 2. Révoquer le courrier</span><span class="sxs-lookup"><span data-stu-id="aaa3d-p110">Step 2. Revoke the mail</span></span>  

<span data-ttu-id="aaa3d-138">Une fois que vous connaissez l’ID de Message du courrier électronique que vous souhaitez révoquer, vous pouvez annuler le courrier électronique à l’aide de l’applet de commande Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="aaa3d-138">Once you know the Message ID of the email you want to revoke, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="aaa3d-139">[Se connecter à Exchange Online à l’aide de PowerShell à distance](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="aaa3d-139">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="aaa3d-140">Exécutez l’applet de commande Set-OMEMessageRevocation comme suit :</span><span class="sxs-lookup"><span data-stu-id="aaa3d-140">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```  

3. <span data-ttu-id="aaa3d-141">Pour vérifier si le message électronique a été révoqué, exécutez l’applet de commande Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="aaa3d-141">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | fl Revoked
    ```  
    <span data-ttu-id="aaa3d-142">Si la révocation a réussi, l’applet de commande renvoie le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="aaa3d-142">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
