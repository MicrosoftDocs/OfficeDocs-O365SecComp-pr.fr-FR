---
title: Adresses IP d'Exchange Online Protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/2/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: eb14f38b-7b55-4a47-84a0-4a56a59e4111
description: Les adresses IP de centre de données Microsoft suivantes sont utilisées par Microsoft Exchange Online Protection (EOP) lors de l'envoi et de la réception d'e-mails, ou pour les services d'administration et de portail Exchange Online Protection. Pour envoyer et recevoir des messages à partir d'EOP ou utiliser les services d'administration, vérifiez que votre réseau autorise les connexions à partir de ces adresses IP.
ms.openlocfilehash: 5742c19f98f8515670150f69c421c19ffecc7668
ms.sourcegitcommit: b6473cd6ba3f9ac79dc6a2040fc148020dfbe464
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "25358363"
---
# <a name="exchange-online-protection-ip-addresses"></a>Adresses IP d'Exchange Online Protection

Les adresses IP de centre de données Microsoft suivantes sont utilisées par Microsoft Exchange Online Protection (EOP) lors de l'envoi et de la réception d'e-mails, ou pour les services d'administration et de portail Exchange Online Protection. Pour envoyer et recevoir des messages à partir d'EOP ou utiliser les services d'administration, vérifiez que votre réseau autorise les connexions à partir de ces adresses IP.
 
> [!NOTE]
> Microsoft a développé un service web basée sur REST pour l’adresse IP et les entrées de nom de domaine complet de cette page. Ce nouveau service permet de configurer et mettre à jour des périphériques de périmètre de réseau tels que des pare-feu et des serveurs proxy. Vous pouvez télécharger la liste des points de terminaison, la version actuelle de la liste, ou les modifications spécifiques. Ce service remplace le document XML, flux RSS et l’adresse IP et les entrées de nom de domaine complet de cette page. Pour essayer ce nouveau service, accédez au [service Web](https://support.office.com/article/managing-office-365-endpoints-99cab9d4-ef59-4207-9f2b-3728eb46bf9a#webservice). 
 
## <a name="eop-ip-address-ranges"></a>Plages d'adresses IP EOP

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

