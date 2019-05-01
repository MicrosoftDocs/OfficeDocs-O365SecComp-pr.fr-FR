---
title: Définir une date d'expiration pour les messages chiffrés par le chiffrement de messages avancé Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f87cb016-7876-4317-ae3c-9169b311ff8a
description: Avec les fonctionnalités de chiffrement de messages avancé Office 365 sur Office 365 message enCryption (OME), vous pouvez étendre votre sécurité de messagerie en définissant une date d'expiration pour les e-mails via un modèle personnalisé.
ms.openlocfilehash: c1fb876724bed970095e950906500ff551d93cee
ms.sourcegitcommit: 8eb3cb4ec45ae0bb75fde249e35c4bc3d263b84f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2019
ms.locfileid: "33506714"
---
# <a name="set-an-expiration-date-for-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="fb8a6-103">Définir une date d'expiration pour les messages chiffrés par le chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="fb8a6-103">Set an expiration date for email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="fb8a6-104">Le chiffrement de messages avancé Office 365 est disponible en haut du chiffrement des messages Office 365 dans certains abonnements.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-104">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="fb8a6-105">Le chiffrement de messages avancé est inclus dans [Microsoft 365 entreprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 entreprise E5 et Office 365 éducation a5.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-105">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="fb8a6-106">Si votre organisation possède un abonnement Office 365 qui n'inclut pas le chiffrement de messages avancé Office 365, vous pouvez acheter le chiffrement de messages avancé comme module complémentaire avec E5 conformité de la référence SKU de conformité avancée.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-106">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="fb8a6-107">Vous pouvez utiliser l'expiration des messages envoyés par vos utilisateurs à des destinataires externes qui utilisent le portail OME pour accéder à des e-mails chiffrés.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-107">You can use message expiration on emails that your users send to external recipients who use the OME Portal to access encrypted emails.</span></span> <span data-ttu-id="fb8a6-108">Vous obligez les destinataires à utiliser le portail OME pour afficher et répondre à des messages électroniques chiffrés envoyés par votre organisation à l'aide d'un modèle personnalisé qui spécifie une date d'expiration dans Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-108">You force recipients to use the OME portal to view and reply to encrypted emails sent by your organization by using a custom branded template that specifies an expiration date in Windows Powershell.</span></span>

<span data-ttu-id="fb8a6-109">En tant qu'administrateur général d'Office 365, lorsque vous appliquez la personnalisation de votre entreprise pour personnaliser l'apparence des messages électroniques de votre organisation Office 365, vous pouvez également spécifier une expiration pour ces messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-109">As an O365 global administrator, when you apply your company branding to customize the look of your Office 365 organization's email messages, you can also specify an expiration for these email messages.</span></span> <span data-ttu-id="fb8a6-110">Avec le chiffrement de messages avancé Office 365, vous pouvez créer plusieurs modèles pour les messages électroniques chiffrés provenant de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-110">With Office 365 Advanced Message Encryption, you can create multiple templates for encrypted emails originating from your organization.</span></span> <span data-ttu-id="fb8a6-111">À l'aide d'un modèle, vous pouvez contrôler la durée pendant laquelle les destinataires ont accès aux messages envoyés par vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-111">Using a template, you can control how long recipients have access to mail sent by your users.</span></span>

<span data-ttu-id="fb8a6-112">Lorsqu'un utilisateur final reçoit un message dont la date d'expiration est définie, l'utilisateur voit la date d'expiration dans le message du wrapper.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-112">When an end user receives mail that has an expiration date set, the user sees the expiration date in the wrapper email.</span></span> <span data-ttu-id="fb8a6-113">Si un utilisateur tente d'ouvrir un message expiré, une erreur s'affiche dans le portail OME.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-113">If a user tries to open an expired mail, an error appears in the OME portal.</span></span>

<span data-ttu-id="fb8a6-114">Seuls les courriers électroniques adressés à des destinataires externes sont Expires.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-114">Only emails to external recipients are expirable.</span></span>

<span data-ttu-id="fb8a6-115">Avec le chiffrement de messages avancé Office 365, chaque fois que vous appliquez une personnalisation personnalisée, Office 365 applique le wrapper aux messages électroniques correspondant à la règle de flux de messagerie à laquelle vous appliquez le modèle.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-115">With Office 365 Advanced Message Encryption, any time you apply custom branding, the Office 365 applies the wrapper to email that fits the mail flow rule to which you apply the template.</span></span> <span data-ttu-id="fb8a6-116">De plus, l'expiration ne peut être utilisée que si la personnalisation personnalisée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-116">In addition, expiration can only be used if custom branding is used.</span></span>

## <a name="create-a-custom-branding-template-to-force-mail-expiration-by-using-powershell"></a><span data-ttu-id="fb8a6-117">Créer un modèle de personnalisation pour forcer l'expiration du courrier à l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="fb8a6-117">Create a custom branding template to force mail expiration by using PowerShell</span></span>

1. <span data-ttu-id="fb8a6-118">[Connectez-vous à Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) à l'aide d'un compte disposant d'autorisations d'administrateur général dans votre client Office 365.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-118">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="fb8a6-119">Exécutez la cmdlet New-OMEConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-119">Run the New-OMEConfiguration cmdlet.</span></span>

     ```powershell
     New-OMEConfiguration -Identity "Expire in 7 days" ExternalMailExpiryInDays 7
     ```

<span data-ttu-id="fb8a6-120">Où :</span><span class="sxs-lookup"><span data-stu-id="fb8a6-120">Where:</span></span>

- <span data-ttu-id="fb8a6-121">Identity est le nom du modèle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-121">Identity is the name of the custom template.</span></span>

- <span data-ttu-id="fb8a6-122">ExternalMailExpiryInDays identifie le nombre de jours pendant lesquels vous souhaitez que les destinataires puissent conserver le courrier avant qu'il n'expire.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-122">ExternalMailExpiryInDays identifies the number of days you want recipients to be able to keep mail before it expires.</span></span> <span data-ttu-id="fb8a6-123">Vous pouvez utiliser n'importe quelle valeur comprise entre 1 et 730 jours.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-123">You can use any value between 1 to 730 days.</span></span>

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="fb8a6-124">Plus d'informations sur le chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="fb8a6-124">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="fb8a6-125">Chiffrement avancé des messages Office 365</span><span class="sxs-lookup"><span data-stu-id="fb8a6-125">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="fb8a6-126">Révoquer le courrier électronique chiffré par le chiffrement de messages avancé Office 365</span><span class="sxs-lookup"><span data-stu-id="fb8a6-126">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>](revoke-ome-encrypted-mail.md)

- [<span data-ttu-id="fb8a6-127">Description du service de conformité et de stratégie de message</span><span class="sxs-lookup"><span data-stu-id="fb8a6-127">Message policy and compliance service description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)