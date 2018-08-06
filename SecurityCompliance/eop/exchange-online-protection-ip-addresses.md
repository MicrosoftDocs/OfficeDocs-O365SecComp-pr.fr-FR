---
title: Adresses IP d'Exchange Online Protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 8/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: eb14f38b-7b55-4a47-84a0-4a56a59e4111
description: Les adresses IP de centre de données Microsoft suivantes sont utilisées par Microsoft Exchange Online Protection (EOP) lors de l'envoi et de la réception d'e-mails, ou pour les services d'administration et de portail Exchange Online Protection. Pour envoyer et recevoir des messages à partir d'EOP ou utiliser les services d'administration, vérifiez que votre réseau autorise les connexions à partir de ces adresses IP.
ms.openlocfilehash: 1b5dad69fb300f36bc94c9d264492f9c9be8948f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026321"
---
# <a name="exchange-online-protection-ip-addresses"></a>Adresses IP d'Exchange Online Protection

Les adresses IP de centre de données Microsoft suivantes sont utilisées par Microsoft Exchange Online Protection (EOP) lors de l'envoi et de la réception d'e-mails, ou pour les services d'administration et de portail Exchange Online Protection. Pour envoyer et recevoir des messages à partir d'EOP ou utiliser les services d'administration, vérifiez que votre réseau autorise les connexions à partir de ces adresses IP.
 
> [!NOTE]
> Microsoft développe un service web basée sur REST pour l’adresse IP et les entrées de nom de domaine complet de cette page. Ce nouveau service vous aideront à configurer et mettre à jour des périphériques de périmètre de réseau tels que des pare-feu et des serveurs proxy. Vous pouvez télécharger la liste des points de terminaison, la version actuelle de la liste, ou les modifications spécifiques. Ce service remplacera le document XML, flux RSS et l’adresse IP et les entrées de nom de domaine complet de cette page. Pour essayer ce nouveau service, accédez au [service Web](https://support.office.com/article/managing-office-365-endpoints-99cab9d4-ef59-4207-9f2b-3728eb46bf9a#webservice). 
 
## <a name="eop-ip-address-ranges"></a>Plages d'adresses IP EOP

Voici la liste complète des plages d’adresses IP EOP à compter de **7/2/2018**. 

||||
|:-----|:-----|:-----|
|**Plages d’adresses IPv4** <br/> |**Plages d’adresses IPv6** <br/> |
| 23.103.132.0/22 | c 2a01:111:f400:7 00 :: / 54 |
| 23.103.136.0/21 | 2a01:111:f400:fc00 :: / 54 |
| 23.103.144.0/20 | 2a01:111:f403 :: / 48 |
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
> Les plages d’adresses IP fournies ici sont uniquement utilisés pour le relais par le biais de connecteurs de client. Modifications apportées à la liste des adresses IP sont rares et sont communiquées à l’avance. Pour vous assurer que les messages que vous envoyez à vos partenaires commerciaux, un hôte actif ou une gamme d’environnement sur site par le biais du service publié plage d’adresses IP, vous devez configurer le connecteur correct pour le routage vers chaque destination. Pour plus d’informations sur les connecteurs, voir [Déterminer lequel connecteur à utiliser](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/set-up-connectors-to-route-mail). les adresses IP dans cette rubrique peuvent changer au fil du temps. Pour un enregistrement de IP toutes les adresses qui ont été ajoutées, modifiées ou déconseillées dans l’année dernière, voir [notification de modification pour les adresses IP EOP](change-notification-for-eop-ip-addresses.md). 
 
Pour plus d'informations sur les adresses IP utilisées par Microsoft Office 365, consultez la rubrique [URL et plages d'adresses IP Office 365](https://go.microsoft.com/fwlink/p/?LinkId=324165).
 
## <a name="ip-ranges-by-region"></a>Plages d'adresses IP par région

Exchange Online Protection achemine le courrier de la manière la plus efficace qu'il soit tout en garantissant la conformité avec nos obligations contractuelles envers nos clients. Dans cette optique, les points de terminaison EOP ci-dessous correspondent à la liste actuelle des plages IPv4 régionales. Toutefois, ces adresses IP peuvent être reconfigurées sans préavis pour une autre fonction dans EOP afin d'optimiser ses capacités et son efficacité. Dans ce cas, le courrier continuera d'être acheminé conformément à nos obligations contractuelles et la liste de points de terminaison sera mise à jour au plus vite une fois les modifications apportées. Pour l'instant, nous ne tenons pas de liste des points de terminaison régionaux pour d'autres parties d'Office 365.
 
||||
|:-----|:-----|:-----|
|**Amériques** <br/> |**EMEA** <br/> |**APAC** <br/> |
| 23.103.132.0/22 | 23.103.132.0/22 |23.103.136.0/21 |
| 23.103.136.0/21 | 23.103.144.0/22 |23.103.152.0/22 |
| 23.103.148.0/22 | 40.92.0.0/18 |40.92.128.0/17 |
| 23.103.152.0/21 | 40.93.0.0/18 |40.93.128.0/17 |
| 23.103.156.0/22 | 40.94.0.0/18 |40.94.128.0/17 |
| 23.103.198.0/24 | 40.95.0.0/18 |40.95.128.0/17 |
| 23.103.200.0/22 | 40.107.0.0/18 |52.100.128.0/17 |
| 40.92.64.0/18 | 52.100.0.0/18 |52.101.128.0/17 |
| 40.93.64.0/18 | 52.101.0.0/18 |52.102.128.0/17 |
| 40.94.64.0/18 | 52.102.0.0/18 |52.103.128.0/17 |
| 40.95.64.0/18 | 52.103.0.0/18 |65.55.88.0/24 |
| 40.107.64.0/18 | 94.245.120.64/27 |104.47.64.0/18 |
| 52.100.64.0/18 | 104.47.0.0/19 |c 2a01:111:f400:7 00 :: / 54 |
| 52.101.64.0/18 | 157.55.234.0/24 |  |
| 52.102.64.0/18 | 157.56.112.0/24 | |
| 52.103.64.0/18 | 213.199.154.0/24 | |
| 65.55.169.0/24 | 213.199.180.128/26 | |
| 104.47.32.0/19 | 2a01:111:f400:7e00 :: / 56 | |
| 157.56.110.0/23 | 2a01:111:f400:fe00 :: / 56 | |
| 207.46.100.0/24 |  | |
| 207.46.163.0/24 |  | |
| 216.32.180.0/23 |  | |
| c 2a01:111:f400:7 00 :: / 54 |  | |
||||
