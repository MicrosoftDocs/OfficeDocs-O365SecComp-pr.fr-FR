---
title: Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/23/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: Purge automatique zéro heures (ZAP) est une fonctionnalité de protection de messagerie qui détecte les messages qui ont déjà été remis aux boîtes aux lettres des utilisateurs avec le courrier indésirable ou un programme malveillant, puis affiche le contenu malveillant sans conséquence. Comment ZAP cela dépend du type de contenu malveillant détecté.
ms.openlocfilehash: ac181a7c57b4b16a952ff9c046edbff1380828d1
ms.sourcegitcommit: 791d23e1c2dea622b6ef77a6e2bde32e1d31a41b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999973"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants

## <a name="overview"></a>Vue d’ensemble

Purge automatique zéro heures (ZAP) est une fonctionnalité de protection de messagerie qui détecte les messages qui ont déjà été remis aux boîtes aux lettres des utilisateurs avec le courrier indésirable ou un programme malveillant, puis affiche le contenu malveillant sans conséquence. Comment ZAP cela dépend du type de contenu malveillant détecté.
  
ZAP est disponible avec la valeur par défaut Exchange Online Protection est fourni avec un abonnement à Office 365 qui contient les boîtes aux lettres Exchange Online.

ZAP est activée par défaut, mais les conditions suivantes doivent être remplies :
  
- **Action du courrier indésirable** est défini sur **déplacer le message vers le dossier courrier indésirable**. <br/>Vous pouvez également créer une stratégie de filtrage du courrier indésirable qui s’applique uniquement à un ensemble d’utilisateurs si vous ne voulez pas que toutes les boîtes aux lettres à être filtré par ZAP.

- Les utilisateurs ont conservé leur valeur par défaut des paramètres de courrier indésirable et n’ont pas activé la protection contre le courrier indésirable. (Pour plus d’informations sur les options de l’utilisateur dans Outlook, voir [Modifier le niveau de protection dans le filtre de courrier indésirable](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) .) 
  
## <a name="how-does-zap-work"></a>Comment fonctionne la ZAP ?

Met à jour les signatures de moteur et des programmes malveillants contre le courrier indésirable dans Office 365 en temps réel au quotidien. Toutefois, les utilisateurs peuvent encore avoir malveillants messages remis dans leur boîte de réception pour plusieurs raisons, notamment si le contenu est weaponized après avoir fourni aux utilisateurs. SUPPRIMER les adresses de cette en surveillant en permanence des mises à jour pour les signatures de courrier indésirable et les programmes malveillants Office 365. ZAP permettre rechercher et supprimer des messages livrés qui figurent déjà dans la boîte de réception des utilisateurs. 
- Pour le courrier électronique identifié comme courrier indésirable, ZAP déplace les messages non lus pour le dossier de courrier indésirable des utilisateurs. 
- Pour les logiciels malveillants nouvellement détecté, ZAP supprime les pièces jointes des messages électroniques, quelle que soit ou non le courrier électronique a été lu. 
  
L’action ZAP est transparente pour l’utilisateur de boîte aux lettres ; ils ne sont pas avertis si un message électronique est déplacé.
  
Autoriser les listes, [les règles de flux de messagerie](https://go.microsoft.com/fwlink/p/?LinkId=722755)et les règles de l’utilisateur final ou des filtres supplémentaires sont prioritaires sur ZAP.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>Pour vérifier ou configurer une stratégie de filtrage du courrier indésirable
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365.
2. Sous **Gestion des menaces**, choisissez le **blocage du courrier indésirable**.
3. Passez en revue les paramètres standards. 
4. Si vous souhaitez personnaliser vos paramètres, sélectionnez l’onglet **personnalisé** et activer **les paramètres personnalisés**. Modifier vos paramètres et si vous le souhaitez, choisissez **+ créer une stratégie** pour ajouter une nouvelle stratégie. 
    
## <a name="to-see-if-zap-moved-your-message"></a>Pour voir si ZAP déplacé votre message

Si vous souhaitez voir si ZAP déplacé votre message, vous pouvez utiliser le [rapport d’état de Protection de menace](view-email-security-reports.md#threat-protection-status-report-new) (ou du [Threat Explorer](use-explorer-in-security-and-compliance.md)).
    
## <a name="to-disable-zap"></a>Pour désactiver ZAP
  
Si vous souhaitez désactiver supprimer pour votre client Office 365, ou un ensemble d’utilisateurs, utilisez le paramètre **ZapEnabled** de [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), une applet de commande EOP.
    
Dans l’exemple suivant, ZAP est désactivé pour une stratégie de filtrage de contenu nommée « Test ».
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>FAQ

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>Que se passe-t-il si un message légitime est déplacé vers le dossier courrier indésirable ?
  
Vous devez suivre le processus de création de rapports normal de faux positifs. La seule raison pour laquelle le message est déplacé vers le dossier courrier indésirable à partir de la boîte de réception serait parce que le service a déterminé que le message a été le courrier indésirable ou malveillant.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>Que se passe-t-il si utiliser la mise en quarantaine Office 365 au lieu du dossier courrier indésirable ?
  
ZAP ne déplacer des messages en quarantaine à partir de la boîte de réception à ce stade.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>Que se passe-t-il si j’ai une règle de flux de messagerie personnalisé (bloquer / règle Autoriser) ?
  
Règles créées par des administrateurs (règles de flux de messagerie) ou bloquer et autoriser les règles sont prioritaires. Ces messages sont exclues les critères de fonctionnalité.
  
## <a name="related-topics"></a>Voir aussi

[Protection contre le courrier indésirable pour Office 365](anti-spam-protection.md)
  
[Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](block-email-spam-to-prevent-false-negatives.md)
  

