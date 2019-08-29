---
title: Créer une stratégie de type d’informations sensibles pour votre entreprise à l’aide du chiffrement de messages Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/28/2019
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
ms.openlocfilehash: d74712798ba9d46614b5fc916e4b1ce111582304
ms.sourcegitcommit: 73f1db241c0686020167d43442e7b07a2199ea3a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "36658120"
---
# <a name="create-a-sensitive-information-type-policy-for-your-organization-using-office-365-message-encryption"></a><span data-ttu-id="6203d-103">Créer une stratégie de type d’informations sensibles pour votre entreprise à l’aide du chiffrement de messages Office 365</span><span class="sxs-lookup"><span data-stu-id="6203d-103">Create a sensitive information type policy for your organization using Office 365 Message Encryption</span></span>

<span data-ttu-id="6203d-104">Vous pouvez utiliser les règles de flux de messagerie Exchange ou la protection contre la perte de données (DLP) d’Office 365 pour créer une stratégie de type d’informations sensibles avec le chiffrement de messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="6203d-104">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create a sensitive information type policy with Office 365 Message Encryption.</span></span> <span data-ttu-id="6203d-105">Pour créer une règle de flux de messagerie Exchange, vous pouvez utiliser le centre d’administration Exchange ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6203d-105">To create an Exchange mail flow rule, you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="6203d-106">Pour créer la stratégie à l’aide de règles de flux de messagerie dans le centre d’administration Exchange</span><span class="sxs-lookup"><span data-stu-id="6203d-106">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="6203d-107">Connectez-vous au centre d’administration Exchange et accédez à **mail Flow** > **Rules**.</span><span class="sxs-lookup"><span data-stu-id="6203d-107">Sign in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**.</span></span> <span data-ttu-id="6203d-108">Sur la page règles, créez une règle qui applique le chiffrement de messages Office 365.</span><span class="sxs-lookup"><span data-stu-id="6203d-108">On the Rules page, create a rule that applies Office 365 Message Encryption.</span></span> <span data-ttu-id="6203d-109">Vous pouvez créer une règle basée sur des conditions telles que la présence de certains mots clés ou types d’informations sensibles dans le message ou la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6203d-109">You can create a rule based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="6203d-110">Pour créer la stratégie à l’aide de règles de flux de messagerie dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="6203d-110">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="6203d-111">Utiliser un compte professionnel ou scolaire disposant d’autorisations d’administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="6203d-111">Use a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="6203d-112">Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="6203d-112">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span> <span data-ttu-id="6203d-113">Utilisez les cmdlets Set-IRMConfiguration et New-TransportRule pour créer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6203d-113">Use the Set-IRMConfiguration and New-TransportRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="6203d-114">Exemple de règle de flux de messagerie créée avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="6203d-114">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="6203d-115">Exécutez les commandes suivantes dans PowerShell pour créer une règle de flux de messagerie Exchange qui chiffre automatiquement les courriers électroniques envoyés à l’extérieur de votre organisation à l’aide de la stratégie de *chiffrement uniquement* si les messages électroniques ou leurs pièces jointes contiennent les informations sensibles suivantes. catégories</span><span class="sxs-lookup"><span data-stu-id="6203d-115">Run the following commands in PowerShell to create an Exchange mail flow rule that automatically encrypts emails sent outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="6203d-116">Numéro d’acheminement ABA</span><span class="sxs-lookup"><span data-stu-id="6203d-116">ABA routing number</span></span>
- <span data-ttu-id="6203d-117">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="6203d-117">Credit card Number</span></span>
- <span data-ttu-id="6203d-118">Numéro de la Loi sur la mise en œuvre du médicament (DEA)</span><span class="sxs-lookup"><span data-stu-id="6203d-118">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="6203d-119">ANGLAIS (ÉTATS-UNIS)</span><span class="sxs-lookup"><span data-stu-id="6203d-119">U.S. / U.K.</span></span> <span data-ttu-id="6203d-120">numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="6203d-120">passport number</span></span>
- <span data-ttu-id="6203d-121">Numéro de compte bancaire américain</span><span class="sxs-lookup"><span data-stu-id="6203d-121">U.S. bank account number</span></span>
- <span data-ttu-id="6203d-122">Numéro d’identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="6203d-122">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="6203d-123">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="6203d-123">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

<span data-ttu-id="6203d-124">Pour plus d’informations, voir [Set-IRMConfiguration](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-irmconfiguration?view=exchange-ps) et [New-TransportRule](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance/New-TransportRule?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="6203d-124">For more information, see [Set-IRMConfiguration](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-irmconfiguration?view=exchange-ps) and [New-TransportRule](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance/New-TransportRule?view=exchange-ps).</span></span>

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="6203d-125">Comment les destinataires accèdent aux pièces jointes</span><span class="sxs-lookup"><span data-stu-id="6203d-125">How recipients access attachments</span></span>

<span data-ttu-id="6203d-126">Après qu’Office 365 a chiffré un message, les destinataires ont un accès illimité aux pièces jointes lorsqu’ils accèdent à leur message chiffré et l’ouvrent.</span><span class="sxs-lookup"><span data-stu-id="6203d-126">After Office 365 encrypts a message, recipients have unrestricted access to attachments when they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="6203d-127">Pour préparer cette modification</span><span class="sxs-lookup"><span data-stu-id="6203d-127">To prepare for this change</span></span>

<span data-ttu-id="6203d-128">Vous souhaiterez peut-être mettre à jour les documents de formation et la documentation utilisateur final applicables pour préparer les personnes de votre organisation à ce changement.</span><span class="sxs-lookup"><span data-stu-id="6203d-128">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span> <span data-ttu-id="6203d-129">Partagez ces ressources de chiffrement de messages Office 365 avec vos utilisateurs selon vos besoins:</span><span class="sxs-lookup"><span data-stu-id="6203d-129">Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="6203d-130">Envoyer, afficher et répondre à des messages chiffrés dans Outlook pour PC</span><span class="sxs-lookup"><span data-stu-id="6203d-130">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="6203d-131">Vidéo Office 365 Essentials: chiffrement de messages Office</span><span class="sxs-lookup"><span data-stu-id="6203d-131">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="6203d-132">Afficher ces modifications dans le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="6203d-132">View these changes in the Audit log</span></span>

<span data-ttu-id="6203d-133">Office 365 audite cette activité et la rend accessible aux administrateurs d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="6203d-133">Office 365 audits this activity and makes it available to Office 365 administrators.</span></span> <span data-ttu-id="6203d-134">L’opération est «New-TransportRule» et un extrait d’un exemple d’entrée d’audit de la recherche de journal d’audit dans Security & Compliance Center est inférieur à:</span><span class="sxs-lookup"><span data-stu-id="6203d-134">The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

```text
*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*
```

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="6203d-135">Pour désactiver ou personnaliser la stratégie de types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="6203d-135">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="6203d-136">Une fois que vous avez créé la règle de flux de messagerie Exchange, vous pouvez [désactiver ou modifier la règle](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) en accédant aux**règles** de **flux** > de messagerie dans le centre d’administration Exchange et désactiver la règle «*chiffrement des messages électroniques sensibles sortants (règle de désactivation de la case)* . ".</span><span class="sxs-lookup"><span data-stu-id="6203d-136">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
