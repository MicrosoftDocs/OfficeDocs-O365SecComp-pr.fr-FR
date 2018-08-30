---
title: Migrations de boîtes aux lettres Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Récapitulatif des applets de commande utilisé pour les migrations de boîtes aux lettres Office 365.
ms.openlocfilehash: 86896d956072b5c11e3b3292363bb32312ff1187
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528356"
---
# <a name="office-365-mailbox-migrations"></a>Migrations de boîtes aux lettres Office 365
Avec un déploiement hybride d’Exchange, les clients peuvent choisir déplacer les boîtes aux lettres Exchange locale vers une organisation [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) ou déplacer des boîtes aux lettres Exchange Online vers une organisation [Exchange locale](https://docs.microsoft.com/Exchange/exchange-server) . Lots de migration sont utilisés lors du déplacement de boîtes aux lettres entre des organisations Exchange Online et de locaux. Les clients peuvent consulter des statistiques et autres informations sur les migrations de boîtes aux lettres à l’aide des applets de commande suivantes :

- [Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - fournit les statistiques par défaut pour une boîte aux lettres utilisateur, qui inclut le statut, la taille de boîte aux lettres, archiver taille de boîte aux lettres et d’effectuer de pourcentage.
- [Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - fournit une liste récapitulative des objets de boîte aux lettres et les attributs dans l’organisation.
- [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - fournit une liste d’objets à extension messagerie existants tels que les boîtes aux lettres, les utilisateurs de messagerie, contacts et groupes de distribution.
- [Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - fournit un état détaillé d’une migration de boîtes aux lettres en cours.
- [Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - fournit des informations sur la boîte aux lettres de déplacement et migration des utilisateurs.
- [Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - fournit des informations sur l’état du lot de migration actuel.
- [Get-migrationuserstatistics vous](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - fournit des informations détaillées sur l’état de la migration pour un utilisateur spécifique.
- [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - fournit des informations sur les boîtes aux lettres, telles que la taille, le nombre de messages et l’heure du dernier accès.

Pour plus d’informations sur les applets de commande supplémentaires, voir [applets de commande de déplacement et Migration dans Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
