---
title: Limites de ressources Office 365
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
description: 'Résumé : Informations sur les ressources limitant pour les différentes applications d’Office 365.'
ms.openlocfilehash: a2e7ef42f9bf224363f3b10a5e450d6127f11585
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528767"
---
# <a name="resource-limits"></a>Limites des ressources

Limites des ressources sont appliquées à l’aide des quotas (limites) et de limitation. Azure Active Directory et les services Office 365 individuels utilisent les deux. Limites sont propres au service et modifier au fil du temps, comme l’ajout de nouvelles fonctionnalités. Pour plus d’informations sur les limites pour les différents services, consultez les rubriques suivantes :
- [Limites du service Active Directory et les restrictions Azure](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [Limites d'Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [Limites d'Exchange Online Protection](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [Limitations et frontières logicielles SharePoint Online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype pour les limites de l’entreprise](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [API REST de Yammer et limites de débit](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Limites de taille de fichier dans balancement](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Outre ces limites, plusieurs mécanismes de limitation sont utilisées dans Azure Active Directory et Office 365. Limitation du service est particulièrement importante, étant donné que les ressources réseau dans des centres de données de Microsoft sont optimisées pour le large éventail de clients qui utilisent les services. Mécanismes de limitation sont les suivantes :
- Azure Active Directory et Office 365 fonctionnalité au niveau utilisateur limitation limiter le nombre de transactions ou d’appels simultanés (par script ou code) qui peuvent être effectuées par un utilisateur.
- Valeur par défaut PowerShell stratégie de limitation est assignée à chaque client lors de la création du client. Ces paramètres affectent les autres éléments, tels que le nombre maximal de sessions simultanées PowerShell pouvant être ouvert par un administrateur unique.
- Chaque client Exchange Online possède une stratégie Exchange Web Services (EWS) par défaut qui est réglée pour les opérations EWS du client et de limitation qui s’applique à tous les clients Outlook.