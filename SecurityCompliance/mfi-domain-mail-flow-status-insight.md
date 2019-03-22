---
title: Aperçu de l'état du flux de messagerie de domaine supérieur
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent en savoir plus sur l'état du flux de messagerie de domaine supérieur dans le tableau de bord de flux de messagerie dans le centre de sécurité & de la sécurité d'Office 365.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 04aa986982465a4c66fbf99f517fb34622d65e19
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30722848"
---
# <a name="top-domain-mail-flow-status-insight"></a><span data-ttu-id="4dea3-103">Aperçu de l'état du flux de messagerie de domaine supérieur</span><span class="sxs-lookup"><span data-stu-id="4dea3-103">Top domain mail flow status insight</span></span>

> [!NOTE]
> <span data-ttu-id="4dea3-104">Les fonctionnalités décrites dans cette rubrique n'ont pas été déployées sur toutes les organisations Office 365 et peuvent faire l'objet de modifications.</span><span class="sxs-lookup"><span data-stu-id="4dea3-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="4dea3-105">La vue d' **État du flux de messagerie de domaine supérieur** vous permet d'obtenir l'état actuel des domaines de votre organisation en termes de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4dea3-105">The **Top domain mail flow status** insight gives you the current status for your organization's domains in terms of mail flow.</span></span> <span data-ttu-id="4dea3-106">Cette vue vous permet d'identifier et de résoudre les problèmes de ***flux de messagerie*** (par exemple, impossible de recevoir des messages électroniques externes), notamment les expirations de domaine ou les domaines avec des enregistrements MX incorrects.</span><span class="sxs-lookup"><span data-stu-id="4dea3-106">This insight helps you identify and troubleshoot domains that are experiencing ***mail flow impacting*** issues (for example, unable to receive external email), especially domain expirations or domains with incorrect MX records.</span></span>

![Vue d'État du flux de domaine supérieur dans le tableau de bord de flux de messagerie dans le centre de sécurité & de sécurité Office 365](media/domain-mail-flow-status-selected.png)

<span data-ttu-id="4dea3-108">Lorsque vous cliquez sur **afficher les détails** dans le volet de visualisation, une fenêtre mobile s'affiche pour vous donner des détails supplémentaires sur l'état de chaque domaine.</span><span class="sxs-lookup"><span data-stu-id="4dea3-108">When you click **View details** in the insight, a flyout appears that shows you more details for the status of each domain.</span></span>

<span data-ttu-id="4dea3-109">Une coche verte pour un domaine indique que l'enregistrement MX actuel (lorsque vous avez parcouru le tableau de bord informations sur le flux de messagerie) correspond à la valeur que nous avons sur l'enregistrement et que le domaine a reçu la messagerie au cours des deux dernières heures.</span><span class="sxs-lookup"><span data-stu-id="4dea3-109">A green check mark for a domain indicates the current MX record (when you browsed to the mail flow insights dashboard) matches the value we have on record, and that the domain has received email during the past two hours.</span></span>

<span data-ttu-id="4dea3-110">Un x rouge pour un domaine indique que l'enregistrement MX a été modifié et que le domaine n'a pas reçu de courrier au cours des 6 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="4dea3-110">A red x for a domain indicates the MX record has been changed, and that the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="4dea3-111">Cela indique probablement que votre domaine a expiré ou que l'enregistrement MX a été mis à jour de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="4dea3-111">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="4dea3-112">Vérifiez auprès de votre bureau d'enregistrement de domaines ou de votre service d'hébergement DNS si le domaine a expiré ou si l'enregistrement MX du domaine est incorrect.</span><span class="sxs-lookup"><span data-stu-id="4dea3-112">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

![La fenêtre mobile détails dans la vue d'État du flux de domaine supérieur](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a><span data-ttu-id="4dea3-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dea3-114">See also</span></span>

<span data-ttu-id="4dea3-115">Pour plus d'informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security _AMP_ Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="4dea3-115">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
