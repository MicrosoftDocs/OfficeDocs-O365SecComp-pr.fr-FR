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
description: Les administrateurs peuvent apprendre à acheminer le courrier indésirable vers les dossiers de courrier inDésirable de l'utilisateur dans Exchange Online Protection.
ms.openlocfilehash: aada143944acf594e3ec0e873d022d7e2d45b003
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670549"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Vérification de l'acheminement du courrier indésirable vers le dossier Courrier indésirable de chaque utilisateur

> [!IMPORTANT]
> Cette rubrique s'applique uniquement aux clients Exchange Online Protection (EOP) qui hébergent des boîtes aux lettres localement dans un déploiement hybride. Les clients Exchange Online dont les boîtes aux lettres sont entièrement hébergées dans Office 365 n'ont pas besoin d'exécuter ces commandes. 
  
L'action anti-courrier indésirable par défaut pour les clients EOP consiste à déplacer les messages identifiés comme tels vers le dossier Courrier indésirable des destinataires. Pour que cette action fonctionne avec les boîtes aux lettres locales, vous devez configurer des règles de flux de messagerie Exchange (également appelées règles de transport) sur vos serveurs Edge ou Hub sur site afin de détecter les en-têtes de courrier indésirable ajoutés par EOP. Ces règles de flux de messagerie définissent le seuil de probabilité de courrier indésirable (SCL) utilisé par la propriété SclJunkThreshold de l'applet de commande Set-OrganizationConfig pour déplacer le courrier indésirable dans le dossier courrier inDésirable de chaque boîte aux lettres. 
  
### <a name="to-add-mail-flow-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>Pour ajouter des règles de flux de messagerie afin de vous assurer que le courrier inDésirable est déplacé vers le dossier courrier inDésirable à l'aide de Windows PowerShell

1. Accédez au Environnement de ligne de commande Exchange Management Shell de votre serveur Exchange local. Pour apprendre à ouvrir l'environnement de ligne de commande Environnement de ligne de commande Exchange Management Shell dans votre organisation Exchange locale, reportez-vous à **Open the Shell**.
    
2. Exécutez la commande suivante pour router le courrier indésirable filtré sur le contenu dans le dossier Courrier indésirable :
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkContentFilteredMail. 
    
3. Exécutez la commande suivante pour router les messages marqués en tant que courrier indésirable avant qu'ils atteignent le filtre de contenu dans le dossier Courrier indésirable :
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkMailBeforeReachingContentFilter. 
    
4. Exécutez la commande suivante pour vous assurer que les messages provenant des expéditeurs d'une liste rouge dans la stratégie de filtre de courrier indésirable, telle que la liste d' **expéditeurs bloqués**, sont acheminés vers le dossier Courrier indésirable : 
    
  ```Powershell
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    Où  _NameForRule_ est le nom de la nouvelle règle, par exemple JunkMailInSenderBlockList. 
    
Si vous ne souhaitez pas utiliser l'action **Déplacer le message dans le dossier Courrier indésirable**, vous pouvez choisir une autre action parmi vos stratégies de filtrage de contenu dans le Centre d'administration Exchange. Pour plus d'informations, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Pour plus d'informations sur ces champs dans l'en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md).
  

> [!TIP]
> Si vous ne souhaitez pas utiliser l'action **déplacer le message vers le dossier** courrier indésirable, vous pouvez choisir une autre action dans vos stratégies de filtrage de contenu dans le centre d'administration Exchange. Pour plus d'informations, voir [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md). Pour plus d'informations sur ces champs dans l'en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md).
> 
## <a name="see-also"></a>Voir aussi

[Cmdlet New-TransportRule](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

