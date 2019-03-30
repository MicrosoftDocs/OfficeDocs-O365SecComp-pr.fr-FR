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
description: Les administrateurs peuvent en savoir plus sur l'état du flux de messagerie du domaine le plus approfondi dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: baa69c3373623d4742d6d957a5022012fb60f7e7
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000667"
---
# <a name="top-domain-mail-flow-status-insight"></a>Aperçu de l'état du flux de messagerie de domaine supérieur

> [!NOTE]
> Les fonctionnalités décrites dans cette rubrique n'ont pas été déployées sur toutes les organisations Office 365 et peuvent faire l'objet de modifications.

La vue d' **État du flux de messagerie de domaine supérieur** vous permet d'obtenir l'état actuel des domaines de votre organisation en termes de flux de messagerie. Cette vue vous permet d'identifier et de résoudre les problèmes de ***flux de messagerie*** (par exemple, impossible de recevoir des messages électroniques externes), notamment les expirations de domaine ou les domaines avec des enregistrements MX incorrects.

![Vue d'État du flux de domaine supérieur dans le tableau de bord de flux de messagerie dans le centre de sécurité & Compliance Center](media/domain-mail-flow-status-selected.png)

Lorsque vous cliquez sur **afficher les détails** dans le volet de visualisation, une fenêtre mobile s'affiche pour vous donner des détails supplémentaires sur l'état de chaque domaine.

Une coche verte pour un domaine indique que l'enregistrement MX actuel (lorsque vous avez parcouru le tableau de bord informations sur le flux de messagerie) correspond à la valeur que nous avons sur l'enregistrement et que le domaine a reçu la messagerie au cours des deux dernières heures.

Un x rouge pour un domaine indique que l'enregistrement MX a été modifié et que le domaine n'a pas reçu de courrier au cours des 6 dernières heures. Cela indique probablement que votre domaine a expiré ou que l'enregistrement MX a été mis à jour de manière incorrecte. Vérifiez auprès de votre bureau d'enregistrement de domaines ou de votre service d'hébergement DNS si le domaine a expiré ou si l'enregistrement MX du domaine est incorrect.

![La fenêtre mobile détails dans la vue d'État du flux de domaine supérieur](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a>Voir aussi

Pour plus d'informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security _AMP_ Compliance Center](mail-flow-insights-v2.md).
