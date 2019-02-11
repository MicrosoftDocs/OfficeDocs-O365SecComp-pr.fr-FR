---
title: Révoquer des e-mails chiffrés par le chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: En tant qu’un administrateur Office 365, vous pouvez retirer certains messages électroniques chiffrés avec Office 365 Message Encryption.
ms.openlocfilehash: 018f12105e19382372a8a4b3a91248bb60b228be
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696238"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="59a22-103">Révocation de courrier électronique de chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="59a22-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="59a22-p101">Cet article fait partie d’une plus grande série d’articles sur [Office 365 Message Encryption](ome.md). Révocation de messagerie chiffrée maintenant droite est en mode Aperçu. Prévoient des mises à jour et les modifications apportées à la fonctionnalité et le contenu afin d’améliorer notre offre.</span><span class="sxs-lookup"><span data-stu-id="59a22-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="59a22-p102">Vous serez peut-être amené à révoquer un courrier électronique qui a déjà été envoyé. Si le message électronique a été chiffré à l’aide du chiffrement de messages Office 365 et que vous êtes un administrateur Office 365, vous pouvez le faire pour le courrier électronique sous certaines conditions. Cet article décrit sous quelles conditions cela est possible et comment le faire.</span><span class="sxs-lookup"><span data-stu-id="59a22-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="59a22-110">Messages électroniques chiffrés que vous pouvez annuler</span><span class="sxs-lookup"><span data-stu-id="59a22-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="59a22-p103">Vous pouvez annuler les messages électroniques chiffrés si le destinataire a reçu une base de liens, marque électroniques chiffrés. Si le destinataire a reçu une expérience native insérée dans un client Outlook pris en charge, les messages électroniques ne peut pas être révoqués.</span><span class="sxs-lookup"><span data-stu-id="59a22-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="59a22-p104">Si un destinataire reçoit une expérience basée sur un lien ou une expérience en ligne varie selon le type de destinataire d’identité : Office 365 et Microsoft Account destinataires (par exemple, les utilisateurs outlook.com) obtenir une expérience en ligne dans les clients Outlook pris en charge. Tous les autres types destinataires, tel que Gmail destinataires, obtenez une expérience basée sur le lien.</span><span class="sxs-lookup"><span data-stu-id="59a22-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="59a22-p105">Bientôt disponible, organisations auront la possibilité de forcer une expérience basée sur le lien quel que soit l’identité du destinataire. De cette manière, tous les destinataires recevront un message électronique personnalisé avec un lien vers le portail Office 365 Message Encryption où ils seront en mesure de lire et répondre aux messages électroniques chiffrés. Ces messages électroniques chiffrés sera révocables.</span><span class="sxs-lookup"><span data-stu-id="59a22-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="59a22-118">Expérience de destinataire pour les messages électroniques chiffrés révoquées</span><span class="sxs-lookup"><span data-stu-id="59a22-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="59a22-119">Une fois qu’un message électronique a été révoqué, le destinataire obtenez une erreur lorsque vous essayez d’accéder à du message électronique chiffré via le portail Office 365 Message Encryption : « le message a été révoqué par l’émetteur ».</span><span class="sxs-lookup"><span data-stu-id="59a22-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Capture d’écran montrant une révoquées de messages électroniques chiffrés.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="59a22-121">Comment révoquer un message électronique chiffré</span><span class="sxs-lookup"><span data-stu-id="59a22-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="59a22-p106">Étape 1. Obtenir l’ID de Message du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="59a22-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="59a22-p107">Avant que vous pouvez retirer un message chiffré, vous devez recueillir l’ID de Message du courrier électronique. L’ID du message est généralement au format :</span><span class="sxs-lookup"><span data-stu-id="59a22-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="59a22-p108">Il existe plusieurs manières pour trouver l’ID de Message du courrier électronique que vous souhaitez révoquer. Cette section décrit quelques options, mais vous pouvez utiliser une méthode qui fournit le code.</span><span class="sxs-lookup"><span data-stu-id="59a22-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="59a22-128">Pour identifier l’ID de Message du courrier électronique que vous souhaitez révoquer à l’aide de suivi des messages dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="59a22-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="59a22-129">Recherchez le courrier électronique par l’expéditeur ou destinataire utilisant le [Nouveau suivi des messages dans Office 365 sécurité & centre de conformité](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="59a22-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="59a22-p109">Une fois que vous avez trouvé le courrier électronique sélectionner pour afficher le volet de **Détails de suivi des messages** . Développez **Plus d’informations** pour localiser l’ID du Message.</span><span class="sxs-lookup"><span data-stu-id="59a22-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="59a22-132">Pour identifier l’ID de Message du courrier électronique que vous souhaitez révoquer à l’aide de rapports de chiffrement de messages Office dans la sécurité &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="59a22-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="59a22-133">Dans la sécurité &amp; centre de conformité, accédez au **Rapport de chiffrement des messages**.</span><span class="sxs-lookup"><span data-stu-id="59a22-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="59a22-134">Choisissez la table **d’Afficher les détails** et d’identifier le message que vous souhaitez révoquer.</span><span class="sxs-lookup"><span data-stu-id="59a22-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="59a22-135">Double-cliquez sur le message pour afficher les détails qui incluent l’ID de Message.</span><span class="sxs-lookup"><span data-stu-id="59a22-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="59a22-p110">Étape 2. Vérifiez que le courrier est révocable</span><span class="sxs-lookup"><span data-stu-id="59a22-p110">Step 2. Verify that the mail is revocable</span></span>

<span data-ttu-id="59a22-138">Pour vérifier si vous pouvez révoquer un message électronique particulier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="59a22-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="59a22-p111">À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="59a22-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="59a22-141">Exécutez l’applet de commande Set-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="59a22-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="59a22-p112">Cette propriété renvoie l’objet du message et indique si le message est révocable. Par exemple,</span><span class="sxs-lookup"><span data-stu-id="59a22-p112">This returns the subject of the message and whether the message is revocable. For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="59a22-p113">Étape 3. Révoquer le courrier</span><span class="sxs-lookup"><span data-stu-id="59a22-p113">Step 3. Revoke the mail</span></span>  

<span data-ttu-id="59a22-146">Une fois que vous connaissez l’ID de Message du courrier électronique que vous souhaitez révoquer, et que vous avez vérifié que le message est révocable, vous pouvez annuler le courrier électronique à l’aide de l’applet de commande Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="59a22-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="59a22-147">[Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="59a22-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="59a22-148">Exécutez l’applet de commande Set-OMEMessageRevocation comme suit :</span><span class="sxs-lookup"><span data-stu-id="59a22-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="59a22-149">Pour vérifier si le message électronique a été révoqué, exécutez l’applet de commande Get-OMEMessageStatus comme suit :</span><span class="sxs-lookup"><span data-stu-id="59a22-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="59a22-150">Si la révocation a réussi, l’applet de commande renvoie le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="59a22-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
