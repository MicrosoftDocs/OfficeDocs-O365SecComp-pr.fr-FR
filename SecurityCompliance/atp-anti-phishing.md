---
title: Fonctionnalités anti-hameçonnage ATP dans Office 365
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
ms.collection:
- M365-security-compliance
description: La protection anti-hameçonnage ATP fait partie de la protection avancée contre les menaces d'Office 365. La protection anti-hameçonnage ATP applique un ensemble de modèles d'apprentissage automatique avec des algorithmes de détection d'emprunt d'identité aux messages entrants pour assurer la protection contre les attaques par hameçonnage et les attaques par hameçonnage. Tous les messages sont soumis à un ensemble complet de modèles d'apprentissage automatique formés pour détecter les messages de hameçonnage, ainsi qu'un ensemble d'algorithmes avancés permettant de se protéger contre diverses attaques par emprunt d'identité d'utilisateur et de domaine.
ms.openlocfilehash: 25e7845ab7d16b0766636006f2c55debfee2f9f9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32249564"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a>Fonctionnalités anti-hameçonnage ATP dans Office 365

La protection anti-hameçonnage ATP fait partie de la [protection avancée contre les menaces d'Office 365](office-365-atp.md). La protection anti-hameçonnage ATP applique un ensemble de modèles d'apprentissage automatique avec des algorithmes de détection d'emprunt d'identité aux messages entrants pour assurer la protection contre les attaques par hameçonnage et les attaques par hameçonnage. Tous les messages sont soumis à un ensemble complet de modèles d'apprentissage automatique formés pour détecter les messages de hameçonnage, ainsi qu'un ensemble d'algorithmes avancés permettant de se protéger contre diverses attaques par emprunt d'identité d'utilisateur et de domaine. La protection anti-hameçonnage ATP protège votre organisation en fonction des stratégies définies par vos administrateurs Office 365 global ou de sécurité.
  
Pour plus d'informations, consultez la rubrique [configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).
  
> [!NOTE]
> La protection contre le hameçonnage (ATP) est disponible uniquement dans la protection avancée contre les menaces, qui est incluse dans les abonnements, tels que [microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation a5, etc. Si votre organisation dispose d'un abonnement Office 365 qui n'inclut pas Office 365 ATP, vous pouvez acheter l'ATP en tant que module complémentaire. Pour plus d'informations, consultez la rubrique [offres et tarifs de protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection) , ainsi que la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).

## <a name="how-atp-anti-phishing-works"></a>Fonctionnement de la protection anti-hameçonnage ATP

La protection contre le hameçonnage (ATP) vérifie les messages entrants pour les indicateurs que le message peut être un hameçonnage. Chaque fois qu'un utilisateur est couvert par une stratégie de protection avancée contre les menaces (pièces jointes fiables, liens fiables ou anti-hameçonnage), le message entrant est évalué par plusieurs modèles d'apprentissage automatique qui analysent le message afin de déterminer si la stratégie s'applique au message et si l'action appropriée est prises, en fonction de la stratégie configurée.
  
La protection contre le hameçonnage (ATP) permet aux administrateurs globaux d'Office 365 ou aux administrateurs de sécurité de définir des stratégies qui fournissent une protection contre les attaques par hameçonnage qui incluent l'emprunt d'identité des utilisateurs ou des domaines. (ou les deux). Les administrateurs globaux d'Office 365 ou les administrateurs de sécurité définissent, dans la stratégie, les utilisateurs et les domaines qui doivent être protégés contre les attaques par emprunt d'identité en utilisant une liste fixe d'utilisateurs ou de domaines ou en utilisant l'intelligence des boîtes aux lettres. La boîte aux lettres est une compréhension approfondie des habitudes de messagerie et des contacts personnels d'un utilisateur. La fonctionnalité ATP apprend comment chaque utilisateur individuel communique avec d'autres utilisateurs à l'intérieur et à l'extérieur de l'organisation et crée un plan de ces relations. Cette carte permet à l'ATP de comprendre plus de détails sur la façon de s'assurer que les messages corrects sont identifiés comme emprunt d'identité.
  
Les stratégies anti-hameçonnage ATP peuvent être appliquées à un ensemble spécifique de personnes ou de groupes dans votre organisation, ou à un domaine entier ou à tous vos domaines personnalisés. Pour plus d'informations, consultez la rubrique [configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).
  
## <a name="how-to-get-atp-anti-phishing"></a>Comment obtenir une protection contre le hameçonnage

Les fonctionnalités anti-hameçonnage ATP font partie de la [protection avancée contre les menaces](office-365-atp.md); Toutefois, la protection contre le hameçonnage ATP s'applique lorsque les stratégies anti-hameçonnage sont définies. (Par exemple, une stratégie basée sur l'emprunt d'identité.) Consultez la rubrique [configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a>Comment savoir si la protection contre le hameçonnage est mise en place

Les stratégies anti-hameçonnage ATP doivent être définies afin que la protection soit effective. Consultez-la tout d'abord pour vérifier que la protection est en place.

De plus, des rapports sont disponibles pour illustrer le fonctionnement du service pour votre organisation. Pour en savoir plus, consultez la rubrique [afficher les rapports pour Office 365 Advanced Threat Protection](view-reports-for-atp.md).

Pour que les modèles d'apprentissage de l'anti-hameçonnage ATP soient actifs pour un utilisateur particulier, cet utilisateur doit faire partie d'une stratégie de [pièces jointEs approuvéEs ATP](atp-safe-attachments.md)définie, de [liens approuvés ATP](atp-safe-links.md)ou d'une stratégie anti-hameçonnage ATP. 

Le tableau suivant décrit quelques exemples de scénarios. Dans chacun de ces exemples, l'organisation utilise Office 365 entreprise E5, qui inclut la protection avancée contre les menaces.
  
|**Exemple de scénario**|**Est-ce que la protection contre le hameçonnage ATP s'applique dans ce cas?**|
|:-----|:-----|
|L'organisation de Pat a Office 365 entreprise E5, mais personne n'a défini de stratégie pour les pièces jointes approuvées pour la protection avancée contre les menaces, les liens fiables ATP ou l'hameçonnage avancé ATP.|Non. Bien que la fonctionnalité soit disponible, au moins une stratégie ATP doit être définie pour que les modèles d'apprentissage de l'ordinateur ATP fonctionnent. Pour l'emprunt d'identité, une stratégie anti-hameçonnage de protection avancée contre les menaces doit également être mise en place.|
|Lee est un employé du service des ventes de contoso. L'organisation de Lee a une stratégie anti-hameçonnage ATP qui s'applique uniquement aux employés financiers.|Non. Dans ce cas, la protection contre le hameçonnage ATP (modèles d'ordinateur et protection contre l'usurpation d'identité) s'applique aux employés financiers, mais ce n'est pas le cas pour d'autres employés, y compris le service des ventes.|
|Hier, un administrateur Office 365 de la société Jean a configuré une stratégie anti-hameçonnage ATP qui s'applique à tous les employés. Plus tôt aujourd'hui, Jean a reçu un message électronique qui inclut un emprunt d'identité couvert par la stratégie.|Oui. Dans cet exemple, Jean a une licence pour la protection avancée contre les menaces, et une stratégie anti-hameçonnage ATP incluant Jean a été définie. Il faut environ 30 minutes pour qu'une nouvelle stratégie prenne effet sur l'ensemble des centres de communication; étant donné qu'un jour a passé dans ce cas, la stratégie doit être en vigueur.|

## <a name="related-topics"></a>Voir aussi

[Office 365-Protection avancée contre les menaces](office-365-atp.md)
  
[Protection anti-hameçonnage dans Office 365](anti-phishing-protection.md)
  
[Configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md)
  
[Liens approuvés ATP dans Office 365](atp-safe-links.md)
  
[Configurer des stratégies de liens fiables ATP dans Office 365](set-up-atp-safe-links-policies.md)
  
[Pièces jointes approuvées ATP dans Office 365](atp-safe-attachments.md)
  
[Configuration des stratégies de pièces jointes approuvées ATP dans Office 365](set-up-atp-safe-attachments-policies.md)
  
[Afficher les rapports de protection contre les menaces avancées](view-reports-for-atp.md)
