---
title: Stratégie de chiffrement des messages Office 365 pour les informations sensibles
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: "Résumé: la stratégie de chiffrement des messages Office 365 pour les types d'informations sensibles est désormais disponible."
ms.openlocfilehash: e2a72ee85ca65a2fe8ae1543979b51915ff0a88f
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2019
ms.locfileid: "29696198"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="5a4ba-103">Stratégie de chiffrement des messages Office 365 pour les informations sensibles</span><span class="sxs-lookup"><span data-stu-id="5a4ba-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="5a4ba-p101">Mise à jour (1/30/19): en octobre 2018, nous avons utilisé un petit échantillon de clients pour comprendre si nous pouvons simplifier la protection en chiffrant automatiquement les messages électroniques sensibles en fonction de certains types d'informations sensibles. En fonction des commentaires positifs de cet exemple, nous avons décidé de développer vers un profil plus diversifié de clients en décembre 2018. Après avoir communiqué le déploiement suivant pour sélectionner des clients, nous avons écouté vos commentaires et déterminé que les clients avec des environnements plus complexes souhaitaient implémenter les règles plus facilement et nous ajustons donc nos offres.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p101">Update (1/30/19): In October 2018, we worked with a small sample of customers to understand if we can simplify protection by automatically encrypting sensitive emails based on certain sensitive information types. Based on positive feedback from this sample, we decided to expand to a more diverse profile of tenants in December 2018. After communicating the next roll-out to select tenants, we listened to your feedback and determined that customers with more complex environments wanted to implement the rules more cautiously, and we are therefore adjusting our plans.</span></span>

<span data-ttu-id="5a4ba-p102">Si votre organisation a été sélectionnée pour le lancement du 15 janvier 2019, nous n'allons pas déployer la stratégie automatique. Au lieu de cela, nous fournissons des instructions dans cet article expliquant comment effectuer le déploiement. Poursuivez votre lecture pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p102">If your organization was selected for the roll-out starting January 15, 2019, we will not roll out the automatic policy. Instead, we are providing instructions in this article on how you can complete the roll-out yourselves. Keep reading to find out how.</span></span>

||
|:-----|
|<span data-ttu-id="5a4ba-p103">Cet article fait partie d'une série d'articles plus large sur le chiffrement de messages Office 365. Cet article est destiné aux administrateurs et ITPros. Si vous recherchez simplement des informations sur l'envoi ou la réception d'un message chiffré, consultez la liste des articles dans [Office 365 message Encryption (OME)](ome.md) et recherchez l'article qui répond le mieux à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a><span data-ttu-id="5a4ba-113">Procédure de création de la stratégie de type d'informations sensibles pour votre client</span><span class="sxs-lookup"><span data-stu-id="5a4ba-113">How to create the sensitive information type policy for your tenant</span></span>

<span data-ttu-id="5a4ba-p104">Vous pouvez utiliser les règles de flux de messagerie Exchange ou la protection contre la perte de données (DLP) d'Office 365 pour créer la stratégie de type d'informations sensibles. Pour créer une règle de flux de messagerie Exchange, vous pouvez utiliser le centre d'administration Exchange ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p104">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create the sensitive information type policy. To create an Exchange mail flow rule you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="5a4ba-116">Pour créer la stratégie à l'aide de règles de flux de messagerie dans le centre d'administration Exchange</span><span class="sxs-lookup"><span data-stu-id="5a4ba-116">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="5a4ba-p105">Connectez-vous au centre d'administration Exchange et accédez à **mail Flow** > **Rules**. Il s'agit de créer une règle qui applique le chiffrement de messages Office 365 en fonction de conditions telles que la présence de certains mots clés ou types d'informations sensibles dans le message ou la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p105">Sign-in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**. There, create a rule that applies Office 365 Message Encryption based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="5a4ba-119">Pour créer la stratégie à l'aide de règles de flux de messagerie dans PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a4ba-119">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="5a4ba-p106">À l'aide d'un compte professionnel ou scolaire doté d'autorisations d'administrateur globales dans votre organisation Office 365, démarrez une session Windows PowerShell et connectez-vous à Exchange Online. Pour obtenir des instructions, consultez la rubrique [connexion à Exchange Online PowerShell](https://aka.ms/exopowershell). Utilisez les cmdlets Set-IRMConfiguration et New-TransporRule pour créer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell). Use the Set-IRMConfiguration and New-TransporRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="5a4ba-123">Exemple de règle de flux de messagerie créée avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a4ba-123">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="5a4ba-124">L'exécution des commandes suivantes dans PowerShell crée une règle de flux de messagerie Exchange qui chiffre automatiquement les messages électroniques en dehors de votre organisation à l'aide de la stratégie de *chiffreMent uniquement* si les messages électroniques ou leurs pièces jointes contiennent les éléments sensibles suivants. types d'informations:</span><span class="sxs-lookup"><span data-stu-id="5a4ba-124">Running the following commands in PowerShell create an Exchange mail flow rule that automatically encrypts emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="5a4ba-125">Numéro d'acheminement ABA</span><span class="sxs-lookup"><span data-stu-id="5a4ba-125">ABA routing number</span></span>
- <span data-ttu-id="5a4ba-126">Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="5a4ba-126">Credit card Number</span></span>
- <span data-ttu-id="5a4ba-127">Numéro de la Loi sur la mise en œuvre du médicament (DEA)</span><span class="sxs-lookup"><span data-stu-id="5a4ba-127">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="5a4ba-p107">Numéro de passeport américain/Britannique</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p107">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="5a4ba-130">Numéro de compte bancaire américain</span><span class="sxs-lookup"><span data-stu-id="5a4ba-130">U.S. bank account number</span></span>
- <span data-ttu-id="5a4ba-131">Numéro d'identification fiscale individuel (ITIN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="5a4ba-131">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="5a4ba-132">Numéro de sécurité sociale (SSN) États-Unis</span><span class="sxs-lookup"><span data-stu-id="5a4ba-132">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="5a4ba-133">Comment les destinataires accèdent aux pièces jointes</span><span class="sxs-lookup"><span data-stu-id="5a4ba-133">How recipients access attachments</span></span>

<span data-ttu-id="5a4ba-134">Une fois qu'un message est chiffré, les destinataires ont un accès illimité aux pièces jointes une fois qu'ils ont accès et ouvert leur courrier électronique chiffré.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-134">Once a message is encrypted, recipients will have unrestricted access to attachments once they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="5a4ba-135">Pour préparer cette modification</span><span class="sxs-lookup"><span data-stu-id="5a4ba-135">To prepare for this change</span></span>

<span data-ttu-id="5a4ba-p108">Vous souhaiterez peut-être mettre à jour les documents de formation et la documentation utilisateur final applicables pour préparer les personnes de votre organisation à ce changement. Partagez ces ressources de chiffrement de messages Office 365 avec vos utilisateurs selon vos besoins:</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p108">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="5a4ba-138">Envoyer, afficher et répondre à des messages chiffrés dans Outlook pour PC</span><span class="sxs-lookup"><span data-stu-id="5a4ba-138">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="5a4ba-139">Vidéo Office 365 Essentials: chiffrement de messages Office</span><span class="sxs-lookup"><span data-stu-id="5a4ba-139">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="5a4ba-140">Afficher ces modifications dans le journal d'audit</span><span class="sxs-lookup"><span data-stu-id="5a4ba-140">View these changes in the Audit log</span></span>

<span data-ttu-id="5a4ba-p109">Cette activité est auditée et disponible pour les administrateurs d'Office 365. L'opération est «New-TransportRule» et un extrait d'un exemple d'entrée d'audit de la recherche de journal d'audit dans Security & Compliance Center est inférieur à:</span><span class="sxs-lookup"><span data-stu-id="5a4ba-p109">This activity is audited and is available to Office 365 administrators. The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="5a4ba-143">*{"CreationTime": "2018-11-28T23:35:01", "ID": "A1b2C3d4-DAA0-4c4f-A019-03a1234a1b0c", "Operation": "New-TransportRule", "": "123456-221d-12345", "RecordType": 1, "ResultStatus": "true", "UserKey": "opérateur Microsoft", " UserType ": 3," version ": 1," Workload ":" Exchange "," ClientIP ":" 123.456.147.68:17584 "," ObjectId ":" "," UserId ":" Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso. onmicrosoft. com "," OriginatingServer ":" CY4PR13MBXXXX ( 15.20.1382.008) "," paramètres ": {" Name ":" Organization "," value ":" 123456-221d-12346 "{" Name ":" ApplyRightsProtectionTemplate "," value ":" Encrypt "}, {" Name ":" Name "," value ":" chiffrer les messages électroniques sensibles sortants (règle de non-boîte) "}, {" nom ":" MessageContainsDataClassifications "... etc.*</span><span class="sxs-lookup"><span data-stu-id="5a4ba-143">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span> |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="5a4ba-144">Pour désactiver ou personnaliser la stratégie de types d'informations sensibles</span><span class="sxs-lookup"><span data-stu-id="5a4ba-144">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="5a4ba-145">Une fois que vous avez créé la règle de flux de messagerie Exchange, vous pouvez [désactiver ou modifier la règle](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) en accédant aux**règles** de **flux** > de messagerie dans le centre d'administration Exchange et désactiver la règle «*chiffrement des messages électroniques sensibles sortants (règle de désactivation de la case)* . ".</span><span class="sxs-lookup"><span data-stu-id="5a4ba-145">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
