---
title: Nouvelle stratégie de chiffrement de messages Office 365 pour les informations sensibles
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/16/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Appliqué automatiquement la stratégie de chiffrement de messages Office 365 pour les types d’informations sensibles présentant à tous les clients.'
ms.openlocfilehash: f83bf0fe572586b3becf2dd53395e611bdaaea24
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614378"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="2737c-103">Stratégie de chiffrement de messages Office 365 pour les informations sensibles</span><span class="sxs-lookup"><span data-stu-id="2737c-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="2737c-p101">Pour un groupe de clients, en fonction de leur taille de l’organisation et la complexité des flux de messagerie, nous effectuons un déploiement lente d’une nouvelle stratégie automatique dans les clients Office 365 qui s’appliqueront chiffrement de messages Office 365 pour les messages électroniques contenant certains types de critiques plus d’informations. Nous sommes le test avec un petit groupe de clients. Cette stratégie sera déployée pas toutes les organisations et des considérations comme taille de l’organisation et la complexité du flux de messagerie sera utilisée pour déterminer le droit à ce déploiement. Si votre organisation est activée pour ce déploiement, vous recevrez une notification dans le centre de messages Office 365 pour vous avertir de la date à laquelle cette stratégie automatique sera créée et vous aurez au moins un avis de 30 jours et l’option Annuler l’abonnement. Si vous ne souhaitez pas attendre que Microsoft créer cette stratégie et que vous souhaitez faire vous-même, vous pouvez créer cette stratégie automatique à l’aide de règles de flux de messagerie Exchange.</span><span class="sxs-lookup"><span data-stu-id="2737c-p101">For a select group of tenants, based on their organization size and complexity of mail flow, we are doing a slow roll-out of a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to emails that contain certain types of sensitive information. We are testing this with a small group of tenants. This policy will not be rolled out to all organizations and considerations such as organization size and complexity of mail flow will be used to determine the eligibility for this roll-out. If your organization is selected for this roll-out, you will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created and you will be given at least a 30-day notice and the option to opt-out. If you don't want to wait for Microsoft to create this policy and would like to do so yourselves, you can create this automatic policy using Exchange Mail Flow rules.</span></span>

## <a name="when-to-expect-the-update-for-your-tenant"></a><span data-ttu-id="2737c-107">Quand la mise à jour pour votre client</span><span class="sxs-lookup"><span data-stu-id="2737c-107">When to expect the update for your tenant</span></span>

<span data-ttu-id="2737c-p102">Votre organisation reçoit une notification dans le centre de messages Office 365 pour vous avertir de la date à laquelle cette stratégie automatique sera créée dans votre client. Vous avez au moins un avis de 30 jours et vous aurez également l’option Annuler l’abonnement. Un scénario dans lequel vous souhaitez pouvez potentiellement exclure est si vous disposez d’une solution de protection contre la perte de données 3 rd tiers qui analyse déjà pour les types de sensibles. Plus d’informations sur la façon d’annulations sont disponibles plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="2737c-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types. More details on how to opt-out are available later in this article.</span></span>

## <a name="sensitive-information-type-policy-details"></a><span data-ttu-id="2737c-111">Détails de la stratégie type des informations sensibles</span><span class="sxs-lookup"><span data-stu-id="2737c-111">Sensitive information type policy details</span></span>

<span data-ttu-id="2737c-112">Une règle de flux de messagerie Exchange sera créée dans votre organisation qui sera chiffrer automatiquement sur le point à l’extérieur de votre organisation avec les messages électroniques le *Chiffrer seule* stratégie si les e-mails ou les pièces jointes contient les types d’informations sensibles suivants :</span><span class="sxs-lookup"><span data-stu-id="2737c-112">An Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="2737c-113">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="2737c-113">ABA routing number</span></span>
- <span data-ttu-id="2737c-114">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="2737c-114">Credit card Number</span></span>
- <span data-ttu-id="2737c-115">Numéro de l’application Agency (DEA) Drug Enforcement</span><span class="sxs-lookup"><span data-stu-id="2737c-115">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="2737c-p103">US / numéro de passeport britannique</span><span class="sxs-lookup"><span data-stu-id="2737c-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="2737c-118">Numéro de compte bancaire US</span><span class="sxs-lookup"><span data-stu-id="2737c-118">U.S. bank account number</span></span>
- <span data-ttu-id="2737c-119">Numéro d'identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="2737c-119">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="2737c-120">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="2737c-120">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="2737c-121">Les types sensibles exactes peuvent varier par les paramètres régionaux de votre organisation et communiquées dans la notification de centre de messages.</span><span class="sxs-lookup"><span data-stu-id="2737c-121">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="2737c-122">Que dois-je faire pour préparer pour que cette modification ?</span><span class="sxs-lookup"><span data-stu-id="2737c-122">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="2737c-p104">Il est inutile de mettre à jour ou modifier les paramètres de configuration d’Office 365 existants avant cette modification nouveau. Toutefois, vous souhaiterez peut-être mettre à jour de n’importe quel utilisateur final applicable documentation et des supports de formation pour préparer les personnes dans votre organisation pour que cette modification. Partager ces ressources Office 365 Message Encryption avec vos utilisateurs selon le cas :</span><span class="sxs-lookup"><span data-stu-id="2737c-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="2737c-126">Envoyer, consulter et répondre aux messages chiffrés dans Outlook pour PC</span><span class="sxs-lookup"><span data-stu-id="2737c-126">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="2737c-127">Office 365 Essentials vidéo : Chiffrement de messages Office</span><span class="sxs-lookup"><span data-stu-id="2737c-127">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="2737c-128">Comment ce changement est représenté dans le journal d’Audit ?</span><span class="sxs-lookup"><span data-stu-id="2737c-128">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="2737c-p105">Cette activité est analysée et est disponible pour les clients.  L’opération est 'New-TransportRule' et un extrait d’un exemple d’entrée d’audit à partir de la recherche du journal d’Audit de sécurité & centre de conformité est ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="2737c-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="2737c-131">*{« CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 », « RecordType » : 1, « ResultStatus » : « True », « UserKey » : « Opérateur Microsoft », » UserType » : 3, « Version » : 1, « charges de travail » : « Exchange », « ClientIP » : « 123.456.147.68:17584 », « ObjectId » : « UserId «, » » : « Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX () 15.20.1382.008)","Parameters » : {« Name » : « Organisation », « Valeur » : « d 123456-221-12346"{« Name » : « ApplyRightsProtectionTemplate », « Valeur » : « Chiffrer »}, {« Name » : « Nom », « Valeur » : « Chiffrer les messages électroniques sensibles sortants (hors de règle de zone) »}, {« Name » : » MessageContainsDataClassifications »... etc..*</span><span class="sxs-lookup"><span data-stu-id="2737c-131">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="2737c-132">Comment I annulations ?</span><span class="sxs-lookup"><span data-stu-id="2737c-132">How do I opt-out?</span></span>

<span data-ttu-id="2737c-133">Si vous souhaitez les annulations de ce changement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2737c-133">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="2737c-p106">À l’aide d’un compte qui dispose des autorisations d’administrateur global dans votre organisation Office 365 Professionnel ou de l’école, démarrer une session Windows PowerShell et se connecter à Exchange Online. Pour plus d’informations, voir [se connecter à Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="2737c-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>
2. <span data-ttu-id="2737c-136">Exécutez l’applet de commande Set-IRMConfiguration comme suit :</span><span class="sxs-lookup"><span data-stu-id="2737c-136">Run the Set-IRMConfiguration cmdlet as follows:</span></span>

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-or-customize-the-automatic-policy"></a><span data-ttu-id="2737c-137">Comment désactiver ou personnaliser la stratégie automatique ?</span><span class="sxs-lookup"><span data-stu-id="2737c-137">How do I disable or customize the automatic policy?</span></span>

<span data-ttu-id="2737c-138">Si vous n’avez pas annulations de ce changement et la règle de flux de messagerie Exchange a déjà été créée, vous pouvez [désactiver ou modifier la règle](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) à partir de **flux de messagerie** > **règles** dans Exchange admin center (EAC) et désactiver la règle «*chiffrer les messages électroniques sensibles sortants (hors de règle de zone)*».</span><span class="sxs-lookup"><span data-stu-id="2737c-138">If you didn’t opt-out of this change and the Exchange mail flow rule has already been created, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
