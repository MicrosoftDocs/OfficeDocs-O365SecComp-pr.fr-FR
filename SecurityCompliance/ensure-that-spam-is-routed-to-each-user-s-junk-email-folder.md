---
title: Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
ms.collection:
- M365-security-compliance
description: L'action anti-courrier indésirable par défaut pour les clients EOP consiste à déplacer les messages identifiés comme tels vers le dossier Courrier indésirable des destinataires. Afin que cette action fonctionne sur des boîtes aux lettres locales, vous devez configurer des règles de transport Exchange sur vos serveurs Edge ou Hub locaux de manière à détecter les en-têtes de courrier indésirable ajoutés par EOP. Ces règles de transport définissent le seuil de probabilité de courrier indésirable (SCL) utilisé par la propriété SclJunkThreshold (de la cmdlet Set-OrganizationConfig) pour déplacer le courrier indésirable dans le dossier Courrier indésirable de chaque boîte aux lettres.
ms.openlocfilehash: d0ae9637ce95a1a8f0d4d241b3aef928c84ba3fa
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221024"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur

> [!IMPORTANT]
> Cette rubrique s'applique uniquement aux clients Exchange Online Protection (EOP) qui hébergent des boîtes aux lettres localement dans un déploiement hybride. Les clients Exchange Online dont les boîtes aux lettres sont entièrement hébergées dans Office 365 n'ont pas besoin d'exécuter ces commandes. 
  
L'action anti-courrier indésirable par défaut pour les clients EOP consiste à déplacer les messages identifiés comme tels vers le dossier Courrier indésirable des destinataires. Afin que cette action fonctionne sur des boîtes aux lettres locales, vous devez configurer des règles de transport Exchange sur vos serveurs Edge ou Hub locaux de manière à détecter les en-têtes de courrier indésirable ajoutés par EOP. Ces règles de transport définissent le seuil de probabilité de courrier indésirable (SCL) utilisé par la propriété SclJunkThreshold (de la cmdlet Set-OrganizationConfig) pour déplacer le courrier indésirable dans le dossier Courrier indésirable de chaque boîte aux lettres. 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>Pour ajouter des règles de transport afin d'assurer le déplacement du courrier indésirable vers le dossier Courrier indésirable à l'aide de Windows PowerShell, procédez comme suit :

1. Accédez au Environnement de ligne de commande Exchange Management Shell de votre serveur Exchange local. Pour apprendre à ouvrir l'environnement de ligne de commande Environnement de ligne de commande Exchange Management Shell dans votre organisation Exchange locale, reportez-vous à **Open the Shell**.
    
2. Exécutez la commande suivante pour router le courrier indésirable filtré sur le contenu dans le dossier Courrier indésirable :
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkContentFilteredMail. 
    
3. Exécutez la commande suivante pour router les messages marqués en tant que courrier indésirable avant qu'ils atteignent le filtre de contenu dans le dossier Courrier indésirable :
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkMailBeforeReachingContentFilter. 
    
4. Exécutez la commande suivante pour vous assurer que les messages provenant des expéditeurs d'une liste rouge dans la stratégie de filtre de courrier indésirable, telle que la liste d' **expéditeurs bloqués**, sont acheminés vers le dossier Courrier indésirable : 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkMailInSenderBlockList. 
    
Si vous ne souhaitez pas utiliser l'action **Déplacer le message dans le dossier Courrier indésirable**, vous pouvez choisir une autre action parmi vos stratégies de filtrage de contenu dans le Centre d'administration Exchange. Pour plus d'informations, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Pour plus d'informations sur ces champs dans l'en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md).
  
## <a name="see-also"></a>See also

[Cmdlet New-TransportRule](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

