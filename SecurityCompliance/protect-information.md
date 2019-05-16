---
title: Protéger les informations
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 4/26/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Page d’accueil pour la protection des informations
ms.openlocfilehash: 696684778604f4259166bdc3059944285833cba1
ms.sourcegitcommit: 4eb4ca899adcf4d86501530f875eb49af8cdaeb7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/16/2019
ms.locfileid: "34083177"
---
# <a name="protect-information"></a>Protéger les informations

Microsoft 365 et Office 365 incluent des fonctionnalités qui peuvent être appliquées à des types de données spécifiques pour protéger les informations.


|**Fonctionnalité**|**Plus d’informations**|
|:-----|:-----|
|[Étiquettes de niveau de confidentialité](sensitivity-labels.md) <br/> |Avec des étiquettes de confidentialité, vous pouvez classer et protéger votre contenu sensible. Les options de protection incluent les étiquettes, les filigranes et le chiffrement. Les étiquettes de sensibilité utilisent Azure information protection. Si vous utilisez des étiquettes Azure information protection, nous vous recommandons, pour l’instant, de créer de nouvelles étiquettes dans d’autres centres d’administration jusqu’à ce que vous ayez terminé la migration. Consultez la rubrique [migration Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-migrate-labels). <br/> Les [étiquettes](retention-policies.md) de rétention sont différentes des étiquettes de sensibilité. Les étiquettes de rétention vous permettent de conserver ou de supprimer du contenu en fonction des stratégies que vous définissez. Ces organismes aident les organisations à se conformer aux réglementations sectorielles et aux politiques internes.|
|[Protection contre la perte de données](data-loss-prevention-policies.md) TECHNOLOGIE  <br/> |Avec les stratégies DLP, vous pouvez identifier, surveiller et protéger automatiquement les informations sensibles dans Office 365. Les stratégies de protection contre la perte de données peuvent utiliser des étiquettes de confidentialité et des types d’informations sensibles pour identifier les informations sensibles. <br/> |
|[Types d’informations sensibles](what-the-sensitive-information-types-look-for.md) <br/> |Microsoft 365 inclut de nombreux types d’informations sensibles que vous pouvez utiliser dans les stratégies DLP et pour une classification automatique avec des étiquettes de sensibilité et de rétention. Les types d’informations sensibles peuvent également être utilisés avec le [scanneur Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) pour classer et protéger des fichiers sur site. Les types d’informations sensibles définissent la façon dont le processus automatisé reconnaît des types d’informations spécifiques, tels que les numéros de service d’intégrité et les numéros de carte de crédit.   <br/> |
|[Chiffrement de messages Office 365](ome.md) OME  <br/> |Avec le chiffrement de messages Office 365, votre organisation peut envoyer et recevoir des messages électroniques chiffrés entre des personnes à l’intérieur et à l’extérieur de votre organisation. Le chiffrement de messages Office 365 fonctionne avec Outlook.com, Yahoo!, Gmail et d’autres services de messagerie. Le chiffrement des messages électroniques permet de s’assurer que seuls les destinataires prévus peuvent afficher le contenu du message. <br/> |
|[Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/)<br/> |Azure information protection (parfois appelé AIP) permet à une organisation de classer, d’étiqueter et, éventuellement, de protéger des documents et des e-mails. Les administrateurs peuvent appliquer automatiquement des étiquettes en définissant des règles et des conditions. Les utilisateurs peuvent appliquer manuellement des étiquettes aux fichiers et aux messages. Vous pouvez également donner aux utilisateurs des recommandations sur le moment où appliquer des étiquettes.<br/> Si vous utilisez des étiquettes de sensibilité ou le chiffrement de messages Office, vous utilisez déjà des fonctionnalités de classification et de protection. Si vous n’avez pas encore migré les étiquettes Azure information protection vers Office 365, continuez à les gérer dans Azure information protection.  <br/>Vous pouvez exécuter le [scanneur Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) sur site pour classer et protéger des fichiers sur Windows Server, les partages réseau et les bibliothèques et les sites SharePoint Server. Il peut s’agir d’une première étape vers l’identification des données à migrer vers Office 365.
|Azure information protection avec la clé de chiffrement gérée du client <br/> |Certaines organisations ont besoin d’une exigence d’entreprise ou de conformité pour conserver le contrôle d’une clé de chiffrement. Cela n’est pas courant. Azure information protection permet aux organisations de mettre votre propre clé (BYOK) au service. Pour plus d’informations, reportez-vous à [la rubrique mettre votre propre clé (BYOK) pour Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/byok-price-restrictions). Une autre option plus complexe est proposée aux clients qui ont besoin de conserver une clé de chiffrement sur site, appelée conservation de votre propre clé (HYOK).  Pour plus d’informations, consultez [la rubrique conserver votre propre clé (hyok) pour Azure information protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-adrms-restrictions). <br/> |
    

