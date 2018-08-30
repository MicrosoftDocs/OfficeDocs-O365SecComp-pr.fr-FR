---
title: Contrôles d’Isolation Office 365
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
description: 'Résumé : Explication des contrôles d’isolation dans Office 365.'
ms.openlocfilehash: 3a5c06d0675a4503d9f5e5edd58535688fb9180a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528762"
---
# <a name="office-365-isolation-controls"></a>Contrôles d’Isolation Office 365 

Microsoft fonctionne en continu pour vous assurer que l’architecture mutualisée d’Office 365 prend en charge la sécurité au niveau de l’entreprise, confidentialité, confidentialité, l’intégrité et la disponibilité des [normes](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons), ainsi que des normes locales et internationales. Si l’échelle et l’étendue des services fournis par Microsoft, il est difficile et non économique pour gérer Office 365 si importante intervention humaine requise. Services Office 365 sont fournies par le biais de plusieurs globalement distribué centres de données, de manière très automatisée, où très peu d’opérations centre de données nécessite une touche humaine, et même moins d’opérations ont besoin d’accéder au contenu du client. Notre équipe prend en charge ces services et les centres de données à l’aide des outils automatisés et hautement sécuriser l’accès à distance. Pour des informations sur la façon services à grande échelle sont effectués dans Office 365, voir [un behind qu'arrière-plan examinez Office 365 pour professionnels de l’informatique](https://channel9.msdn.com/Events/SharePoint-Conference/2014/SPC202).

Office 365 est composée de plusieurs services qui fournissent des fonctionnalités importantes de l’entreprise et de collaborer à toute l’expérience Office 365. Chacun de ces services est conçu pour être autonome et à intégrer à l’autre. Office 365 est conçu avec les principes d’une [Architecture orientée service](https://msdn.microsoft.com/library/aa480021.aspx), qui est définie comme la conception et développement de logiciels sous la forme de services interopérables fournissant des fonctionnalités d’entreprise bien définies et [sécurité opérationnelle Assurance](http://www.microsoft.com/download/details.aspx?id=40872), une infrastructure qui intègre les connaissances acquises par une variété de fonctionnalités qui sont spécifiques à Microsoft, y compris le [Cycle de développement de sécurité](https://www.microsoft.com/sdl/default.aspx)de Microsoft, le [Centre de sécurité Microsoft](https://technet.microsoft.com/library/dn440717.aspx)et profond sensibilisation les menaces de sécurité.

Services Office 365 communiquer entre eux, mais ils sont conçus et implémentés afin qu’ils peuvent être déployés et fonctionner en tant que services autonomes, indépendamment de l’autre. Microsoft sépare les droits et les domaines de responsabilité pour Office 365 réduire les possibilités de modification non autorisée ou involontaire ou d’une mauvaise utilisation des ressources de l’entreprise. Les équipes Office 365 ont des rôles définis dans le cadre d’un mécanisme de contrôle d’accès basé sur un rôle complet.

## <a name="customer-content-isolation"></a>Isolation de contenu client
Tout le contenu client appartenant à un client est isolé à partir d’autres clients, à partir des données d’opérations et systèmes utilisées dans la gestion d’Office 365. Plusieurs formulaires de protection ont été implémentées dans Office 365 pour réduire le risque de compromission de n’importe quel service Office 365 ou application ou tout accès non autorisés aux informations des clients ou le système Office 365 au final. Pour plus d’informations sur comment Microsoft implémente l’isolation logique des données client dans Office 365, voir [Isolation du locataire dans Office 365](office-365-tenant-isolation-overview.md).
