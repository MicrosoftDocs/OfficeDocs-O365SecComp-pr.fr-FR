---
title: Isolation du locataire dans Office 365
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
description: Résumé de la façon dont Microsoft met en œuvre isolation du locataire pour Office 365.
ms.openlocfilehash: fcf66ee65c2a4cfdf73ae0eac77f54bd555d059d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528165"
---
# <a name="tenant-isolation-in-office-365"></a>Isolation du locataire dans Office 365

Un des principaux avantages du cloud computing est le concept d’une infrastructure partagée commune entre les clients de nombreuses simultanément, conduisant à des économies d’échelle. Ce concept est appelé *à plusieurs clients*. Microsoft fonctionne en continu pour vous assurer que les architectures de plusieurs clients des services en nuage prennent en charge des normes de sécurité, la confidentialité, la confidentialité, l’intégrité et la disponibilité au niveau de l’entreprise.

En fonction de l’expérience collectées à partir de [Trustworthy Computing](https://www.microsoft.com/en-us/twc/default.aspx) et le [Cycle de développement de sécurité](http://www.microsoft.com/security/sdl/default.aspx)et les investissements importants, services de cloud Microsoft ont été conçus en partant du principe que tous les clients sont potentiellement dangereux à tous autres clients et nous avons implémenté des mesures de sécurité pour empêcher les actions d’un client à partir d’affecter la sécurité ou le service d’un autre client ou l’accès au contenu d’un autre client.

Les deux principaux objectifs de gestion d’isolation du locataire dans un environnement de plusieurs client sont les suivants :
1.  Prévention contre les fuites ou contre les accès au contenu client dans clients ; et
2.  Empêcher les actions d’un client d’incidence négative sur le service pour un autre client

Plusieurs formulaires de protection ont été implémentées dans Office 365 pour empêcher les clients à partir des services Office 365 compromettre ou applications ou accède aux informations d’autres clients ou système Office 365, notamment :
- Isolation logique du contenu de client de chaque client pour les services Office 365 est effectuée par le biais de l’autorisation d’Azure Active Directory et contrôle d’accès basé sur un rôle.
- SharePoint Online fournit des mécanismes d’isolation des données au niveau du stockage.
- Microsoft utilise rigoureuse sécurité physique, filtrage d’arrière-plan et une stratégie de cryptage multiniveau pour protéger la confidentialité et l’intégrité du contenu de client. Tous les centres de données Office 365 possèdent des contrôles d’accès biométrique, avec palmaires nécessitant plus accès physique. En outre, les employés de Microsoft tous les basée aux États-Unis sont requis pour terminer une vérification en arrière-plan standard dans le cadre du processus de recrutement. Pour plus d’informations sur les contrôles d’accès administratif dans Office 365, voir [Contrôles d’accès d’administration Office 365](office-365-administrative-access-controls-overview.md).
- Office 365 utilise des technologies côté service chiffrer le contenu de client au repos et en transit, y compris BitLocker, chiffrement par fichier, Transport Layer Security (TLS) et Internet Protocol Security (IPsec). Pour plus d’informations spécifiques à propos du chiffrement dans Office 365, voir [Technologies de chiffrement des données dans Office 365](office-365-encryption-in-the-microsoft-cloud-overview.md).

Ensemble, les protections mentionnés ci-dessus fournissent des contrôles fiables d’isolation logique qui fournissent la protection contre les menaces et atténuation équivalente à celui fourni par l’isolement physique uniquement.

## <a name="related-links"></a>Liens connexes
- [Isolation et au contrôle d’accès dans Azure Active Directory](office-365-isolation-in-azure-active-directory.md)
- [Isolation du bureau des clients du graphique et étudier](office-365-isolation-in-graph-and-delve.md)
- [Isolation du locataire de la recherche Office 365](office-365-isolation-in-office-365-search.md)
- [Isolation du locataire dans Office 365 vidéo](office-365-isolation-in-office-365-video.md)
- [Limites des ressources](office-365-resource-limits.md)
- [Surveillance et test des limites de client](office-365-monitoring-and-testing.md)
- [Isolation et au contrôle d’accès dans Office 365](office-365-isolation-in-office-365.md)