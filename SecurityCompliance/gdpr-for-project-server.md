---
title: RGPD pour Project Server
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Découvrez comment satisfaire aux exigences du RGPD dans l’environnement Project Server local.
ms.openlocfilehash: 67097cdab4fdab31537cf4b6dd27ce17234c2bdc
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219014"
---
# <a name="gdpr-for-project-server"></a>RGPD pour Project Server

Project Server utilise des scripts personnalisés pour exporter et supprimer des données utilisateur dans Project Web App. Le processus de base est le suivant :

1.  Recherchez les sites Project Web App dans votre batterie de serveurs.

2.  Recherchez les projets dans chaque site contenant l’utilisateur.

3.  Exportez et passez en revue les types de données que vous voulez examiner.

4.  Supprimez des données si nécessaire.

Ces étapes sont expliquées en détail dans les articles suivants :

- [Exportation de données utilisateur depuis Project Server](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Suppression de données utilisateur de Project Server](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Notez que Project Server est basé sur SharePoint Server et consigne les événements dans les journaux ULS de SharePoint et dans la base de données d’utilisation. Pour en savoir plus, consultez l’article qui traite du [RGPD dans SharePoint Server](gdpr-for-sharepoint-server.md).
