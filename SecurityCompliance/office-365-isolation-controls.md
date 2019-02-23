---
title: Contrôles d’isolation Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: "Résumé: explication des contrôles d'isolation dans Office 365."
ms.openlocfilehash: a6ff2b11ea02334a6c47317cbb77b8d47207b552
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217314"
---
# <a name="office-365-isolation-controls"></a>Contrôles d’isolation Office 365 

Microsoft travaille en continu pour s'assurer que l'architecture mutualisée d'Office 365 prend en charge les [normes](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)de sécurité, de confidentialité, de confidentialité, d'intégrité et de disponibilité au niveau de l'entreprise, ainsi que les normes locales et internationales. Étant donné l'échelle et l'étendue des services fournis par Microsoft, il serait difficile et non économique de gérer Office 365 si une interaction humaine importante était nécessaire. Les services Office 365 sont fournis par le biais de plusieurs centres de données répartis globalement, de manière très automatisée, lorsque les opérations de centre de données requièrent très peu d'opérations de centre de données, et même moins d'opérations nécessitent un accès au contenu du client. Notre équipe prend en charge ces services et centres de ressources à l'aide d'outils automatisés et d'accès à distance hautement sécurisé. Pour obtenir des informations détaillées sur la façon dont les services à grande échelle sont utilisés dans Office 365, voir [une présentation en arrière-plan de office 365 pour les professionnels de l'informatique](https://channel9.msdn.com/Events/SharePoint-Conference/2014/SPC202).

Office 365 est composé de plusieurs services qui fournissent des fonctionnalités métier importantes et contribuent à l'intégralité de l'expérience d'Office 365. Chacun de ces services est conçu pour être autonome et s'intégrer les uns avec les autres. Office 365 est conçu avec les principes d'une [architecture orientée service](https://msdn.microsoft.com/library/aa480021.aspx), qui est définie comme la conception et le développement de logiciels sous la forme de services interopérables qui fournissent une fonctionnalité métier et une sécurité opérationnelle bien définies. [ Assurance](http://www.microsoft.com/download/details.aspx?id=40872), une infrastructure qui incorpore les connaissances acquises par le biais de différentes fonctionnalités qui sont propres à Microsoft, y compris le [cycle de vie de développement](https://www.microsoft.com/sdl/default.aspx)de la sécurité Microsoft, le centre de réponse à la [sécurité Microsoft](https://technet.microsoft.com/library/dn440717.aspx)et la profonde sensibilisation au paysage des menaces Cybersecurity.

Les services Office 365 interagissent les uns avec les autres, mais ils sont conçus et implémentés de sorte qu'ils puissent être déployés et exploités en tant que services autonomes, indépendamment les uns des autres. Microsoft isole les responsabilités et domaines de responsabilité pour Office 365 afin de réduire les possibilités de modification non autorisée ou involontaire des ressources de l'organisation. Les équipes Office 365 disposent de rôles définis dans le cadre d'un mécanisme de contrôle d'accès basé sur un rôle complet.

## <a name="customer-content-isolation"></a>Isolation du contenu client
Tout le contenu client appartenant à un client est isolé des autres clients et des données des opérations et systèmes utilisées dans la gestion d'Office 365. Plusieurs formes de protection ont été mises en œuvre partout dans Office 365 afin de réduire le risque de compromission de n'importe quel service ou application Office 365, ou tout accès non autorisé à des informations sur les clients ou le système Office 365 lui-même. Pour plus d'informations sur la façon dont Microsoft implémente l'isolation logique des données client dans Office 365, consultez la rubrique [isolation du client dans office 365](office-365-tenant-isolation-overview.md).
