---
title: Nouvelle stratégie de chiffrement de messages Office 365 pour les informations sensibles
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 12/13/2018
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Nouvelle Office 365 Message Encryption stratégie pour plus d’informations sensibles.'
ms.openlocfilehash: 180050d1bf9303f6d29bc126e66ac53211c2fb34
ms.sourcegitcommit: 3aae959ea1ac5ef61a9942c681d334831e6b6038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2018
ms.locfileid: "27271090"
---
# <a name="new-office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="80ae9-103">Nouvelle stratégie de chiffrement de messages Office 365 pour les informations sensibles</span><span class="sxs-lookup"><span data-stu-id="80ae9-103">New Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="80ae9-p101">Nous allons créer une nouvelle stratégie automatique dans les clients Office 365 qui seront appliqueront chiffrement de messages Office 365 pour tous les messages électroniques qui contiennent des informations sensibles et qui sont envoyées à l’extérieur de votre organisation. Cette nouvelle règle de flux de messagerie Exchange sera automatiquement créée dans votre organisation cliente Office 365 afin que votre organisation est protégée par défaut.</span><span class="sxs-lookup"><span data-stu-id="80ae9-p101">We will be creating a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to all emails that contain sensitive information and that are being sent outside your organization. This new Exchange mail flow rule will be automatically created in your Office 365 tenant so that your organization will be protected by default.</span></span>

## <a name="how-will-this-work"></a><span data-ttu-id="80ae9-106">Comment fonctionnera-t-il ?</span><span class="sxs-lookup"><span data-stu-id="80ae9-106">How will this work?</span></span>

<span data-ttu-id="80ae9-p102">Votre organisation reçoit une notification dans le centre de messages Office 365 pour vous avertir de la date à laquelle cette stratégie automatique sera créée dans votre client. Vous avez au moins un avis de 30 jours et vous aurez également l’option Annuler l’abonnement. Un scénario dans lequel vous souhaitez pouvez potentiellement exclure est si vous disposez d’une solution de protection contre la perte de données 3 rd tiers qui analyse déjà pour les types de sensibles.</span><span class="sxs-lookup"><span data-stu-id="80ae9-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types.</span></span>

## <a name="new-policy-details"></a><span data-ttu-id="80ae9-109">Détails de la nouvelle stratégie</span><span class="sxs-lookup"><span data-stu-id="80ae9-109">New policy details</span></span>

<span data-ttu-id="80ae9-110">Une nouvelle règle de flux de messagerie Exchange sera créée dans votre organisation qui sera chiffrer automatiquement sur le point à l’extérieur de votre organisation avec les messages électroniques le *Chiffrer seule* stratégie s’ils contiennent les informations sensibles suivants :</span><span class="sxs-lookup"><span data-stu-id="80ae9-110">A new Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if they contain the following sensitive information types:</span></span>

- <span data-ttu-id="80ae9-111">Numéro de routage ABA</span><span class="sxs-lookup"><span data-stu-id="80ae9-111">ABA routing number</span></span>
- <span data-ttu-id="80ae9-112">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="80ae9-112">Credit card Number</span></span>
- <span data-ttu-id="80ae9-113">Numéro de l’application Agency (DEA) Drug Enforcement</span><span class="sxs-lookup"><span data-stu-id="80ae9-113">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="80ae9-p103">US / numéro de passeport britannique</span><span class="sxs-lookup"><span data-stu-id="80ae9-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="80ae9-116">Numéro de compte bancaire US</span><span class="sxs-lookup"><span data-stu-id="80ae9-116">U.S. bank account number</span></span>
- <span data-ttu-id="80ae9-117">Numéro d'identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="80ae9-117">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="80ae9-118">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="80ae9-118">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="80ae9-119">Les types sensibles exactes peuvent varier par les paramètres régionaux de votre organisation et communiquées dans la notification de centre de messages.</span><span class="sxs-lookup"><span data-stu-id="80ae9-119">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="80ae9-120">Que dois-je faire pour préparer pour que cette modification ?</span><span class="sxs-lookup"><span data-stu-id="80ae9-120">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="80ae9-p104">Il est inutile de mettre à jour ou modifier les paramètres de configuration d’Office 365 existants avant cette modification nouveau. Toutefois, vous souhaiterez peut-être mettre à jour de n’importe quel utilisateur final applicable documentation et des supports de formation pour préparer les personnes dans votre organisation pour que cette modification.</span><span class="sxs-lookup"><span data-stu-id="80ae9-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span>

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="80ae9-123">Comment ce changement est représenté dans le journal d’Audit ?</span><span class="sxs-lookup"><span data-stu-id="80ae9-123">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="80ae9-p105">Cette activité est analysée et est disponible pour les clients.  L’opération est 'New-TransportRule' et un extrait d’un exemple d’entrée d’audit à partir de la recherche dans le centre de conformité et de sécurité du journal d’Audit est ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="80ae9-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="80ae9-126">*{« CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 », « RecordType » : 1, « ResultStatus » : « True », « UserKey » : « Opérateur Microsoft », » UserType » : 3, « Version » : 1, « charges de travail » : « Exchange », « ClientIP » : « 123.456.147.68:17584 », « ObjectId » : « UserId «, » » : « Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX () 15.20.1382.008)","Parameters » : {« Name » : « Organisation », « Valeur » : « d 123456-221-12346"{« Name » : « ApplyRightsProtectionTemplate », « Valeur » : « Chiffrer »}, {« Name » : « Nom », « Valeur » : « Chiffrer les messages électroniques sensibles sortants (hors de règle de zone) »}, {« Name » : » MessageContainsDataClassifications »... etc..*</span><span class="sxs-lookup"><span data-stu-id="80ae9-126">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="80ae9-127">Comment I annulations ?</span><span class="sxs-lookup"><span data-stu-id="80ae9-127">How do I opt-out?</span></span>

<span data-ttu-id="80ae9-128">Si vous souhaitez les annulations de ce changement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="80ae9-128">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="80ae9-129">Connectez-vous à [Exchange Online PowerShell](https://aka.ms/exopowershell) en tant qu’utilisateur doté du rôle Administrateur général.</span><span class="sxs-lookup"><span data-stu-id="80ae9-129">Connect to [Exchange Online PowerShell](https://aka.ms/exopowershell) as a user with the global administrator role.</span></span>
2.  <span data-ttu-id="80ae9-130">Exécutez le code suivant après l’authentification :</span><span class="sxs-lookup"><span data-stu-id="80ae9-130">Run the following code after authenticating:</span></span>

    ```
    Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
    ```

## <a name="how-do-i-disable-the-automatic-policy"></a><span data-ttu-id="80ae9-131">Comment désactiver la stratégie automatique ?</span><span class="sxs-lookup"><span data-stu-id="80ae9-131">How do I disable the automatic policy?</span></span>

<span data-ttu-id="80ae9-132">Si vous n’avez pas annulations de ce changement et la règle de courrier Exchange a déjà été créée, vous pouvez [désactiver la règle](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) à partir de **flux de messagerie** > **règles** dans Exchange admin center (EAC) et désactiver la règle «*chiffrer sortant les messages électroniques sensibles (hors de règle de zone)*».</span><span class="sxs-lookup"><span data-stu-id="80ae9-132">If you didn’t opt-out of this change and the Exchange mail rule has already been created, you can [disable the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
