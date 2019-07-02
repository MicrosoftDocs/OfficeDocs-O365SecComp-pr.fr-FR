---
title: Migrations de boîtes aux lettres Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Bref résumé des applets de commande utilisées pour les migrations de boîtes aux lettres Office 365.
ms.openlocfilehash: 3858af0c246cdef07164b6414a87cf110cf65055
ms.sourcegitcommit: aa60a6cdf83c67576e858668d1182cd4fffeb5e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "33622424"
---
# <a name="office-365-mailbox-migrations"></a><span data-ttu-id="3e368-103">Migrations de boîtes aux lettres Office 365</span><span class="sxs-lookup"><span data-stu-id="3e368-103">Office 365 Mailbox Migrations</span></span>
<span data-ttu-id="3e368-104">Avec un déploiement hybride basé sur Exchange, les clients peuvent choisir de déplacer des boîtes aux lettres Exchange locales vers une organisation [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) ou de déplacer des boîtes aux lettres Exchange Online vers une organisation [Exchange locale](https://docs.microsoft.com/Exchange/exchange-server) .</span><span class="sxs-lookup"><span data-stu-id="3e368-104">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization.</span></span> <span data-ttu-id="3e368-105">Les lots de migration sont utilisés lors du déplacement de boîtes aux lettres entre des organisations locales et Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3e368-105">Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations.</span></span>

<span data-ttu-id="3e368-106">Les clients peuvent consulter les statistiques et d’autres informations sur les migrations de boîtes aux lettres avec les cmdlets suivantes:</span><span class="sxs-lookup"><span data-stu-id="3e368-106">Customers can review statistics and other information about mailbox migrations with the following cmdlets:</span></span>

- <span data-ttu-id="3e368-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps): fournit des statistiques par défaut pour une boîte aux lettres d’utilisateur, qui inclut l’État, la taille de boîte aux lettres, la taille de boîte aux lettres d’archivage et le pourcentage d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="3e368-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps): Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size, and percentage complete.</span></span>
- <span data-ttu-id="3e368-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
): fournit une liste récapitulative des objets et des attributs de boîte aux lettres dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3e368-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
): Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="3e368-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps): fournit une liste des objets à extension messagerie existants, tels que les boîtes aux lettres, les utilisateurs de messagerie, les contacts et les groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="3e368-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps): Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts, and distribution groups.</span></span>
- <span data-ttu-id="3e368-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps): fournit un état détaillé de la migration de boîte aux lettres en cours.</span><span class="sxs-lookup"><span data-stu-id="3e368-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps): Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="3e368-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps): fournit des informations sur les utilisateurs de migration et de déplacement de boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3e368-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps): Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="3e368-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps): fournit des informations sur l’état du lot de migration actuel.</span><span class="sxs-lookup"><span data-stu-id="3e368-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps): Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="3e368-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps): fournit des informations détaillées sur l’état de la migration pour un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="3e368-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps): Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="3e368-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps): fournit des informations sur les boîtes aux lettres, telles que la taille, le nombre de messages et l’heure du dernier accès.</span><span class="sxs-lookup"><span data-stu-id="3e368-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps): Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="3e368-115">Pour plus d’informations sur les applets de commande, voir [Move and migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="3e368-115">For more information about cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
