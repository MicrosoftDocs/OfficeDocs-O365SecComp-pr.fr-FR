---
title: Informations sur les règles de flux de messagerie lent
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 5/3/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
description: Les administrateurs peuvent en savoir plus sur les règles de flux de messagerie lentes dans le tableau de bord de flux de messagerie dans le centre de sécurité & de sécurité Office 365.
ms.openlocfilehash: 8188ee0da15ac337499866783ca4f2d893062d5b
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454876"
---
# <a name="slow-mail-flow-rules-insight"></a><span data-ttu-id="9d742-103">Informations sur les règles de flux de messagerie lent</span><span class="sxs-lookup"><span data-stu-id="9d742-103">Slow mail flow rules insight</span></span>

<span data-ttu-id="9d742-104">Des règles inefficaces de flux de messagerie (également appelées règles de transport) peuvent entraîner des retards de flux de messagerie pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9d742-104">Inefficient mail flow rules (also known as transport rules) can lead to mail flow delays for your organization.</span></span> <span data-ttu-id="9d742-105">Cette vue d'État indique les règles de flux de messagerie qui ont un impact sur le flux de messagerie de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9d742-105">This insight reports mail flow rules that have an impact on your organization's mail flow.</span></span> <span data-ttu-id="9d742-106">Voici des exemples de ces types de règles:</span><span class="sxs-lookup"><span data-stu-id="9d742-106">Examples of these types of rules are:</span></span>

- <span data-ttu-id="9d742-107">Conditions utilisées par **est membre de** pour les grands groupes.</span><span class="sxs-lookup"><span data-stu-id="9d742-107">Conditions that use **Is member of** for large groups.</span></span>

- <span data-ttu-id="9d742-108">Conditions qui utilisent des critères de correspondance des expressions régulières complexes (Regex).</span><span class="sxs-lookup"><span data-stu-id="9d742-108">Conditions that use complex regular expression (regex) pattern matching.</span></span>

- <span data-ttu-id="9d742-109">Conditions d'utilisation de l'archivage de contenu dans les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="9d742-109">Conditions that use content checking in attachments.</span></span>

<span data-ttu-id="9d742-110">Le centre d'analyse vous aidera à identifier et à ajuster les règles de flux de messagerie afin de réduire les délais de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9d742-110">The insight will help you to identify and fine-tune mail flow rules to help reduce mail flow delays.</span></span>

![Des règles de flux de messagerie lentes dans le tableau de bord de flux de messagerie dans le centre de sécurité & de sécurité Office 365](media/1dd90faa-f065-4b10-8b47-d35dc127fc26.png)

<span data-ttu-id="9d742-112">Lorsque vous cliquez sur **afficher les détails**, un volet flyout apparaît dans lequel vous pouvez examiner la règle.</span><span class="sxs-lookup"><span data-stu-id="9d742-112">When you click **View details**, a flyout pane appears where you can review the rule.</span></span> <span data-ttu-id="9d742-113">Dans le volet flyout, peut également cliquer sur **afficher les exemples de messages** pour voir les types de messages concernés par la règle.</span><span class="sxs-lookup"><span data-stu-id="9d742-113">In the flyout pane, can also click **view sample messages** to see what kind of messages are impacted by the rule.</span></span>

![Volet flyout après avoir cliqué sur Afficher les détails dans une règle de flux de messagerie lente vue d'ensemble du tableau de bord de flux de messagerie](media/2cbd43b7-1f21-4338-a70c-7b50de5c69cd.png)
