---
title: Aperçu de l’état du flux de messagerie de domaine supérieur
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent en savoir plus sur l’état du flux de messagerie du domaine le plus approfondi dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center.
ms.openlocfilehash: 851ef1438f111a36f69563670bbd0835a9956edc
ms.sourcegitcommit: e05e83212e7ca4e84f2ddb0de0297895b995338d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2019
ms.locfileid: "33868589"
---
# <a name="top-domain-mail-flow-status-insight"></a><span data-ttu-id="1c96c-103">Aperçu de l’état du flux de messagerie de domaine supérieur</span><span class="sxs-lookup"><span data-stu-id="1c96c-103">Top domain mail flow status insight</span></span>

<span data-ttu-id="1c96c-104">La vue d' **État du flux de messagerie de domaine supérieur** vous permet d’obtenir l’état actuel des domaines de votre organisation en termes de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1c96c-104">The **Top domain mail flow status** insight gives you the current status for your organization's domains in terms of mail flow.</span></span> <span data-ttu-id="1c96c-105">Cette vue vous permet d’identifier et de résoudre les problèmes de ***flux de messagerie*** (par exemple, impossible de recevoir des messages électroniques externes), notamment les expirations de domaine ou les domaines avec des enregistrements MX incorrects.</span><span class="sxs-lookup"><span data-stu-id="1c96c-105">This insight helps you identify and troubleshoot domains that are experiencing ***mail flow impacting*** issues (for example, unable to receive external email), especially domain expirations or domains with incorrect MX records.</span></span>

![Vue d’État du flux de domaine supérieur dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center](media/domain-mail-flow-status-selected.png)

<span data-ttu-id="1c96c-107">Lorsque vous cliquez sur **afficher les détails** dans le volet de visualisation, une fenêtre mobile s’affiche pour vous donner des détails supplémentaires sur l’état de chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="1c96c-107">When you click **View details** in the insight, a flyout appears that shows you more details for the status of each domain.</span></span>

<span data-ttu-id="1c96c-108">Une coche verte pour un domaine indique que l’enregistrement MX actuel (lorsque vous avez parcouru le tableau de bord informations sur le flux de messagerie) correspond à la valeur que nous avons sur l’enregistrement et que le domaine a reçu la messagerie au cours des deux dernières heures.</span><span class="sxs-lookup"><span data-stu-id="1c96c-108">A green check mark for a domain indicates the current MX record (when you browsed to the mail flow insights dashboard) matches the value we have on record, and that the domain has received email during the past two hours.</span></span>

<span data-ttu-id="1c96c-109">Un x rouge pour un domaine indique que l’enregistrement MX a été modifié et que le domaine n’a pas reçu de courrier au cours des 6 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="1c96c-109">A red x for a domain indicates the MX record has been changed, and that the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="1c96c-110">Cela indique probablement que votre domaine a expiré ou que l’enregistrement MX a été mis à jour de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="1c96c-110">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="1c96c-111">Vérifiez auprès de votre bureau d’enregistrement de domaines ou de votre service d’hébergement DNS si le domaine a expiré ou si l’enregistrement MX du domaine est incorrect.</span><span class="sxs-lookup"><span data-stu-id="1c96c-111">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

![La fenêtre mobile détails dans la vue d’État du flux de domaine supérieur](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a><span data-ttu-id="1c96c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c96c-113">See also</span></span>

<span data-ttu-id="1c96c-114">Pour plus d’informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security _AMP_ Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="1c96c-114">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
