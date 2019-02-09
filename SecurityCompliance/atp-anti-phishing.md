---
title: Fonctionnalités anti-hameçonnage ATP dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
description: DAV anti-hameçonnage fait partie d’Office 365 avancée protection contre les menaces. DAV anti-hameçonnage applique un ensemble de modèles de formation machine ainsi que les algorithmes de détection de l’emprunt d’identité pour les messages entrants pour assurer la protection des marchandises et lance les attaques par hameçonnage. Tous les messages sont soumis à un ensemble de modèles d’apprentissage automatique formés pour détecter les messages de hameçonnage, avec un ensemble d’algorithmes utilisés pour protéger contre les attaques de l’emprunt d’identité utilisateur et de domaine différents.
ms.openlocfilehash: c3e44a313bf9c823fbfda138fc5a10294993d509
ms.sourcegitcommit: c1c41744c2de89c9e172f817c8f73bb0ada81a58
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2019
ms.locfileid: "29792269"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>Fonctionnalités anti-hameçonnage ATP dans Office 365

DAV anti-hameçonnage fait partie [d’Office 365 avancée protection contre les menaces](office-365-atp.md). DAV anti-hameçonnage applique un ensemble de modèles de formation machine ainsi que les algorithmes de détection de l’emprunt d’identité pour les messages entrants pour assurer la protection des marchandises et lance les attaques par hameçonnage. Tous les messages sont soumis à un ensemble de modèles d’apprentissage automatique formés pour détecter les messages de hameçonnage, avec un ensemble d’algorithmes utilisés pour protéger contre les attaques de l’emprunt d’identité utilisateur et de domaine différents. DAV anti-hameçonnage protège votre organisation conformément aux stratégies qui sont définies par des administrateurs de sécurité Office 365 globale.
  
Pour plus d’informations, voir [configurer les stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).
  
> [!NOTE]
> DAV anti-hameçonnage est uniquement disponible en contre les menaces avancées, qui est inclus dans un abonnement, telles que [Microsoft 365 pour entreprises](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation A5, etc.. Si votre organisation a un abonnement à Office 365 qui n’inclut pas d’Office 365 DAV, vous pouvez acheter potentiellement DAV comme module complémentaire. Pour plus d’informations, voir [plans Office 365 avancée protection contre les menaces et les prix](https://products.office.com/exchange/advance-threat-protection) et [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).

## <a name="how-atp-anti-phishing-works"></a>Fonctionne de DAV anti-hameçonnage

DAV anti-hameçonnage vérifie les messages entrants pour que le message peut être l’hameçonnage les indicateurs. Chaque fois qu’un utilisateur est couverte par une stratégie DAV (pièces jointes fiables, liens sans échec ou anti-hameçonnage) du message entrant est évalué par ordinateur plusieurs modèles qui analysent le message pour déterminer si la stratégie s’applique au message et l’action appropriée de la formation prise en fonction de la stratégie configurée.
  
DAV anti-hameçonnage permet à Office 365 les administrateurs globaux ou les administrateurs de sécurité définir des stratégies qui assurent une protection contre les attaques par phishing qui incluent l’emprunt d’identité des utilisateurs ou des domaines. (ou les deux). Les administrateurs globaux Office 365 ou administrateurs de sécurité définir une liste des utilisateurs ou des domaines ou à l’aide d’aide à la décision de boîte aux lettres au sein de la stratégie, les utilisateurs et les domaines doit être protégée contre les attaques de l’emprunt d’identité à l’aide. Aide à la décision de boîte aux lettres est une connaissance approfondie des habitudes de messagerie d’un utilisateur et les contacts personnels. DAV apprend comment chaque utilisateur communique avec d’autres utilisateurs à l’intérieur et à l’extérieur de l’organisation et crée un mappage de ces relations. Cette table permet DAV de comprendre plus de détails sur la façon de vérifier les messages sont identifiés comme l’emprunt d’identité.
  
Les stratégies anti-hameçonnage DAV peut être appliqué à un ensemble spécifique de personnes ou groupes de votre organisation, ou à un domaine entier ou tous vos domaines personnalisés. Pour plus d’informations, voir [configurer les stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).
  
## <a name="how-to-get-atp-anti-phishing"></a>Comment obtenir DAV anti-hameçonnage

Fonctionnalités Anti-hameçonnage ATP font partie de la [Protection contre les menaces avancées](office-365-atp.md); Toutefois, la protection anti-hameçonnage DAV s’applique lorsque des stratégies anti-hameçonnage sont définis. (Une stratégie de l’emprunt d’identité est un exemple). Consultez la rubrique [configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>Comment savoir si DAV anti-hameçonnage est en place

Les stratégies anti-hameçonnage DAV doivent être définis dans l’ordre de protection prenne effet. Vérifier pour vérifier la protection est en place.

En outre, les rapports sont disponibles pour afficher la façon dont le service fonctionne pour votre organisation. Pour plus d’informations, voir [View reports pour Office 365 avancée protection contre les menaces](view-reports-for-atp.md).

Pour DAV anti-hameçonnage apprentissage de l’ordinateur modèles pour être actif d’un utilisateur spécifique, cet utilisateur doit faire partie d’une stratégie de [Pièces jointes fiables DAV](atp-safe-attachments.md), [Liens fiables DAV](atp-safe-links.md)ou ATP Anti-hameçonnage définie. 

Le tableau suivant décrit quelques exemples de scénarios. Dans chacun de ces exemples, l’organisation utilise Office 365 entreprise E5, qui inclut la protection contre les menaces avancées.
  
|**Exemple de scénario**|**DAV anti-hameçonnage applicable dans ce cas ?**|
|:-----|:-----|
|Organisation de Pat a Office 365 entreprise E5, mais n’a défini des stratégies pour DAV pièces jointes sûres, liens fiables DAV ou DAV avancée phishing encore.|non. Bien que la fonctionnalité est disponible, au moins une stratégie de vente doit être définie dans l’ordre de l’ordinateur DAV modèles d’apprentissage pour travailler. Pour l’emprunt d’identité d’une stratégie d’anti-hameçonnage DAV doit également être en place.|
|Lee est un employé dans le service des ventes de Contoso. Organisation de Lee possède une stratégie d’anti-hameçonnage DAV en place qui s’applique aux employés finance uniquement.|non. Dans ce cas, DAV anti-hameçonnage (modèles ordinateur et protection de l’emprunt d’identité) s’appliquent à finance employés, mais les autres employés, y compris le service commercial, ne serait pas.|
|Hier, un administrateur Office 365 à l’organisation de Jean définir une stratégie anti-hameçonnage DAV qui s’applique à tous les employés. Journée, Jean a reçu un message électronique qui inclut un emprunt d’identité couvert par la stratégie.|Oui. Dans cet exemple, Jean possède une licence pour la protection contre les menaces avancées, et une stratégie anti-hameçonnage DAV incluant Jean a été définie. Il est généralement d’environ 30 minutes pour une nouvelle stratégie prennent effet sur les centres de données ; dans la mesure où un jour écoulé dans ce cas, la stratégie doit être en vigueur.|

## <a name="related-topics"></a>Voir aussi

[Protection avancée contre les menaces dans Office 365](office-365-atp.md)
  
[Protection anti-hameçonnage dans Office 365](anti-phishing-protection.md)
  
[Configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md)
  
[Liens approuvés DAV dans Office 365](atp-safe-links.md)
  
[Définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)
  
[Pièces jointes fiables de DAV dans Office 365](atp-safe-attachments.md)
  
[Définir des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)
  
[Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md)
