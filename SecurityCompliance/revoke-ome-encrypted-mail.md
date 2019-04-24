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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264820"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="c2739-103">Révocation de courrier de chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="c2739-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="c2739-104">Cet article fait partie d'une série d'articles plus large sur le chiffrement de [messages Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="c2739-104">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span> <span data-ttu-id="c2739-105">Pour l'instant, la révocation des messages chiffrés est en préversion.</span><span class="sxs-lookup"><span data-stu-id="c2739-105">Right now, encrypted email revocation is in preview.</span></span> <span data-ttu-id="c2739-106">Prévoyez des mises à jour et des modifications apportées à la fonctionnalité et au contenu pour améliorer notre offre.</span><span class="sxs-lookup"><span data-stu-id="c2739-106">Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="c2739-107">Il peut s'avérer nécessaire de révoquer un e-mail qui a déjà été envoyé.</span><span class="sxs-lookup"><span data-stu-id="c2739-107">You may find it necessary to revoke an email that has already been sent.</span></span> <span data-ttu-id="c2739-108">Si le courrier électronique a été chiffré à l'aide du chiffrement de messages Office 365 et que vous êtes un administrateur d'Office 365, vous pouvez le faire pour le courrier électronique dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="c2739-108">If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions.</span></span> <span data-ttu-id="c2739-109">Cet article décrit les circonstances dans lesquelles cela est possible et comment procéder.</span><span class="sxs-lookup"><span data-stu-id="c2739-109">This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="c2739-110">Messages chiffrés que vous pouvez révoquer</span><span class="sxs-lookup"><span data-stu-id="c2739-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="c2739-111">Vous pouvez révoquer les messages électroniques chiffrés si le destinataire a reçu un message électronique chiffré, basé sur une liaison.</span><span class="sxs-lookup"><span data-stu-id="c2739-111">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="c2739-112">Si le destinataire a reçu une expérience Inline native dans un client Outlook pris en charge, ces messages électroniques ne peuvent pas être révoqués.</span><span class="sxs-lookup"><span data-stu-id="c2739-112">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="c2739-113">Si un destinataire reçoit une expérience basée sur la liaison ou si une expérience en ligne dépend du type d'identité du destinataire: Office 365 et les destinataires de comptes Microsoft (par exemple, les utilisateurs outlook.com) obtiennent une expérience inline dans les clients Outlook pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c2739-113">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="c2739-114">Tous les autres types de destinataires, tels que les destinataires Gmail, bénéficient d'une expérience basée sur les liens.</span><span class="sxs-lookup"><span data-stu-id="c2739-114">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="c2739-115">Bientôt, les organisations pourront forcer une expérience basée sur la liaison indépendamment de l'identité du destinataire.</span><span class="sxs-lookup"><span data-stu-id="c2739-115">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity.</span></span> <span data-ttu-id="c2739-116">De cette manière, tous les destinataires recevront un message électronique avec un lien vers le portail de chiffrement des messages Office 365 où ils pourront lire et répondre à des messages chiffrés.</span><span class="sxs-lookup"><span data-stu-id="c2739-116">This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails.</span></span> <span data-ttu-id="c2739-117">Tous les messages électroniques chiffrés seront révocables.</span><span class="sxs-lookup"><span data-stu-id="c2739-117">All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="c2739-118">Expérience de destinataire pour les messages électroniques chiffrés révoqués</span><span class="sxs-lookup"><span data-stu-id="c2739-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="c2739-119">Une fois qu'un e-mail a été révoqué, le destinataire obtiendra une erreur lors de la tentative d'accès au courrier chiffré via le portail de chiffrement des messages Office 365: «le message a été révoqué par l'expéditeur».</span><span class="sxs-lookup"><span data-stu-id="c2739-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Capture d'écran illustrant un message électronique chiffré révoqué.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="c2739-121">Procédure de révocation d'un message électronique chiffré</span><span class="sxs-lookup"><span data-stu-id="c2739-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="c2739-122">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="c2739-122">Step 1.</span></span> <span data-ttu-id="c2739-123">Obtenir l'ID de message de l'e-mail</span><span class="sxs-lookup"><span data-stu-id="c2739-123">Obtain the Message ID of the email</span></span>

<span data-ttu-id="c2739-124">Avant de pouvoir révoquer un courrier chiffré, vous devez recueillir l'ID du message.</span><span class="sxs-lookup"><span data-stu-id="c2739-124">Before you can revoke an encrypted mail you need to gather the Message ID of the mail.</span></span> <span data-ttu-id="c2739-125">Le MessageId se présente généralement au format suivant:</span><span class="sxs-lookup"><span data-stu-id="c2739-125">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="c2739-126">Il existe plusieurs façons de trouver l'ID de message de l'e-mail à révoquer.</span><span class="sxs-lookup"><span data-stu-id="c2739-126">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="c2739-127">Cette section décrit quelques options, mais vous pouvez utiliser n'importe quelle méthode qui fournit l'ID.</span><span class="sxs-lookup"><span data-stu-id="c2739-127">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="c2739-128">Pour identifier l'ID de message du courrier électronique à révoquer à l'aide du suivi des messages &amp; dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="c2739-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="c2739-129">Recherchez le courrier électronique envoyé par l'expéditeur ou le destinataire à l'aide du [nouveau suivi des messages dans le centre de sécurité & de la sécurité d'Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="c2739-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="c2739-130">Une fois que vous avez trouvé le message, sélectionnez-le pour afficher le volet **Détails du suivi des messages** .</span><span class="sxs-lookup"><span data-stu-id="c2739-130">Once you've located the email select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="c2739-131">Pour **plus d'informations** , reportez-vous à l'ID du message.</span><span class="sxs-lookup"><span data-stu-id="c2739-131">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="c2739-132">Pour identifier l'ID de message du courrier électronique à révoquer à l'aide des rapports de chiffrement de &amp; messages Office dans le centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="c2739-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="c2739-133">Dans le centre &amp; de sécurité conformité, accédez au **rapport**de chiffrement des messages.</span><span class="sxs-lookup"><span data-stu-id="c2739-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="c2739-134">Sélectionnez le tableau **afficher les détails** et identifiez le message à révoquer.</span><span class="sxs-lookup"><span data-stu-id="c2739-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="c2739-135">Double-cliquez sur le message pour afficher les détails qui incluent l'ID du message.</span><span class="sxs-lookup"><span data-stu-id="c2739-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="c2739-136">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="c2739-136">Step 2.</span></span> <span data-ttu-id="c2739-137">Vérifier que le message est révocable</span><span class="sxs-lookup"><span data-stu-id="c2739-137">Verify that the mail is revocable</span></span>

<span data-ttu-id="c2739-138">Pour vérifier si vous pouvez ou non révoquer un message électronique particulier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="c2739-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="c2739-139">À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c2739-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c2739-140">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="c2739-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="c2739-141">Exécutez la cmdlet Set-OMEMessageStatus comme suit:</span><span class="sxs-lookup"><span data-stu-id="c2739-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="c2739-142">Cette valeur renvoie l'objet du message et indique si le message est révocable.</span><span class="sxs-lookup"><span data-stu-id="c2739-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="c2739-143">For example,</span><span class="sxs-lookup"><span data-stu-id="c2739-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="c2739-144">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="c2739-144">Step 3.</span></span> <span data-ttu-id="c2739-145">Révoquer le courrier</span><span class="sxs-lookup"><span data-stu-id="c2739-145">Revoke the mail</span></span>  

<span data-ttu-id="c2739-146">Une fois que vous avez identifié l'ID du message que vous souhaitez révoquer, et que vous avez vérifié que le message est révocable, vous pouvez le révoquer à l'aide de la cmdlet Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="c2739-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="c2739-147">[Connectez-vous à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="c2739-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="c2739-148">Exécutez la cmdlet Set-OMEMessageRevocation comme suit:</span><span class="sxs-lookup"><span data-stu-id="c2739-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="c2739-149">Pour vérifier si l'e-mail a été révoqué, exécutez la cmdlet Get-OMEMessageStatus comme suit:</span><span class="sxs-lookup"><span data-stu-id="c2739-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="c2739-150">Si la révocation a réussi, l'applet de commande renvoie le résultat suivant:</span><span class="sxs-lookup"><span data-stu-id="c2739-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
