---
title: Adresses IP d'Exchange Online Protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: eb14f38b-7b55-4a47-84a0-4a56a59e4111
description: Les adresses IP de centre de données Microsoft suivantes sont utilisées par Microsoft Exchange Online Protection (EOP) lors de l'envoi et de la réception d'e-mails, ou pour les services d'administration et de portail Exchange Online Protection. Pour envoyer et recevoir des messages à partir d'EOP ou utiliser les services d'administration, vérifiez que votre réseau autorise les connexions à partir de ces adresses IP.
ms.openlocfilehash: 6c7d8c78a012be3928317eac1e9b6fcdeab64a24
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222823"
---
# <a name="exchange-online-protection-ip-addresses"></a>Adresses IP d'Exchange Online Protection

Les adresses IP de centre de données Microsoft suivantes sont utilisées par Microsoft Exchange Online Protection (EOP) lors de l'envoi et de la réception d'e-mails, ou pour les services d'administration et de portail Exchange Online Protection. Pour envoyer et recevoir des messages à partir d'EOP ou utiliser les services d'administration, vérifiez que votre réseau autorise les connexions à partir de ces adresses IP.
 
> [!NOTE]
> Microsoft a développé un service Web basé sur REST pour les entrées d'adresse IP et de nom de domaine complet sur cette page. Ce nouveau service vous permet de configurer et de mettre à jour les périphériques de périmètre réseau, tels que les pare-feu et les serveurs proxy. Vous pouvez télécharger la liste des points de terminaison, la version actuelle de la liste ou des modifications spécifiques. Ce service remplace le document XML, le flux RSS, ainsi que les entrées d'adresse IP et de nom de domaine complet (FQDN) sur cette page. Pour tester ce nouveau service, accédez à l' [adresse IP d'Office 365 et à l'URL du service Web](https://docs.microsoft.com/office365/enterprise/office-365-ip-web-service). 
 
## <a name="eop-ip-address-ranges"></a>Plages d'adresses IP EOP

||||
|:-----|:-----|:-----|
|**Plages d'adresses IPv4** <br/> |**Plages d'adresses IPv6** <br/> |
| 23.103.132.0/22 | 2a01:111: F400:7c00::/54 |
| devenue 23.103.136.0/21 | 2a01:111: F400: fc00::/54 |
| 23.103.144.0/20 | 2a01:111: f403::/48 |
| 23.103.198.0/23 |  |
| 23.103.200.0/22 |  |
| 40.92.0.0/14 |  |
| 40.107.0.0/17 |  |
| 52.100.0.0/14 |  |
| 52.238.78.88/32 |  |
| 65.55.88.0/24 |  |
| 65.55.169.0/24 |  |
| 94.245.120.64/26 |  |
| 104.47.0.0/17 |  |
| 157.55.234.0/24 |  |
| 157.56.110.0/23 |  |
| 157.56.112.0/24 |  |
| 207.46.100.0/24 |  |
| 207.46.163.0/24 |  |
| 213.199.154.0/24 |  |
| 213.199.180.128/26 |  |
| 216.32.180.0/23 |  |
||||
 
> [!IMPORTANT]
> Les plages d'adresses IP fournies ici ne sont utilisées que pour les relais via les connecteurs des clients. Les modifications apPortées à la liste des adresses IP sont rares et sont communiquées à l'avance. Pour vous assurer que les messages que vous envoyez à vos partenaires professionnels, un hôte actif ou un environnement local transitent par le biais de la plage d'adresses IP publiée du service, vous devez configurer le connecteur approprié pour le routage vers chaque destination. Pour plus d'informations sur les connecteurs, voir [choisir le connecteur à utiliser](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail). les adresses IP de cette rubrique peuvent changer au fil du temps.  
 
Pour plus d'informations sur les adresses IP utilisées par Microsoft Office 365, consultez la rubrique [URL et plages d'adresses IP Office 365](https://go.microsoft.com/fwlink/p/?LinkId=324165).

