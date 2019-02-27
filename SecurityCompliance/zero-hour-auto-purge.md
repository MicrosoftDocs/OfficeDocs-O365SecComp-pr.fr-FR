---
title: Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: La suppression automatique de zéro heure (ZAP) est une fonctionnalité de protection de la messagerie qui détecte les messages contenant du courrier indésirable ou des programmes malveillants qui ont déjà été remis dans la boîte de réception de vos utilisateurs, puis rend le contenu malveillant inoffensif. Le mode de fonctionnement de ZAP dépend du type de contenu malveillant détecté.
ms.openlocfilehash: 84d9c1dc12c3caf0630d25a3980cdaea1830a4c0
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295637"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants

## <a name="overview"></a>Vue d’ensemble

La suppression automatique de zéro heure (ZAP) est une fonctionnalité de protection de la messagerie qui détecte les messages contenant des messages hameçons, des courriers indésirables ou des programmes malveillants qui ont déjà été remis dans la boîte de réception de vos utilisateurs, puis rend le contenu malveillant inoffensif. Le mode de fonctionnement de ZAP dépend du type de contenu malveillant détecté; les messages peuvent être zapped en raison du contenu, des URL ou des pièces jointes du courrier.
  
ZAP est disponible avec la protection Exchange Online par défaut incluse avec tout abonnement Office 365 qui contient des boîtes aux lettres Exchange Online.

L'option ZAP est activée par défaut, mais les conditions suivantes doivent être remplies:
  
- L' **action de courrier** indésirable est définie sur déplacer le **message vers le dossier**courrier indésirable. <br/>Vous pouvez également créer une stratégie de filtrage du courrier indésirable qui s'applique uniquement à un ensemble d'utilisateurs si vous ne voulez pas que toutes les boîtes aux lettres soient filtrées par la méthode ZAP.

- Les utilisateurs ont conservé leurs paramètres de courrier indésirable par défaut et n'ont pas désactivé la protection contre le courrier indésirable. (Pour plus d'informations sur les options utilisateur dans Outlook, consultez [la rubrique modifier le niveau de protection dans le filtre Courrier](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) indésirable.) 
  
## <a name="how-does-zap-work"></a>Comment l'opération ZAP fonctionne-t-elle?

Office 365 met à jour quotidiennement les signatures du moteur de blocage du courrier indésirable et des programmes malveillants en temps réel. Toutefois, vos utilisateurs peuvent toujours recevoir des messages malveillants dans leur boîte de réception pour diverses raisons, notamment si le contenu est arme après remise aux utilisateurs. ZAP les résout en surveillant en continu les mises à jour des signatures Office 365 courrier indésirable et anti-programme malveillant. ZAP peut rechercher et supprimer les messages précédemment remis qui se trouvent déjà dans les boîtes de réception des utilisateurs. 

- Pour les messages identifiés comme courrier indésirable, la méthode ZAP déplace les messages non lus dans le dossier courrier inDésirable des utilisateurs. 

- Pour les messages identifiés comme courrier indésirable, la méthode ZAP déplace les messages vers le dossier courrier inDésirable des utilisateurs, que l'e-mail ait été lu ou non.

- Pour les programmes malveillants nouvellement détectés, ZAP supprime les pièces jointes des messages électroniques, que l'e-mail ait été lu ou non. 
  
L'action ZAP est transparente pour l'utilisateur de boîte aux lettres; elles ne sont pas notifiées en cas de déplacement d'un message électronique.
  
Les listes d'autorisation, les [règles de flux de messagerie](https://go.microsoft.com/fwlink/p/?LinkId=722755)et les règles de l'utilisateur final ou les filtres supplémentaires prévalent sur zap.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>Pour examiner ou configurer une stratégie de filtrage du courrier indésirable
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l'aide de votre compte professionnel ou scolaire pour Office 365.

2. Sous **gestion des menaces**, sélectionnez **blocage du courrier**indésirable.

3. Passez en revue les paramètres standard. 

4. Si vous souhaitez personnaliser vos paramètres, sélectionnez l'onglet **personnalisé** et activez **paramètres personnalisés**. Modifiez vos paramètres et, si vous le souhaitez, cliquez sur **+ créer une stratégie** pour ajouter une nouvelle stratégie. 
    
## <a name="to-see-if-zap-moved-your-message"></a>Pour savoir si ZAP a déplacé votre message

Si vous voulez savoir si ZAP a déplacé votre message, vous pouvez utiliser le [rapport d'état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report) (ou l'Explorateur de [menaces](use-explorer-in-security-and-compliance.md)).
    
## <a name="to-disable-zap"></a>Pour désactiver ZAP
  
Si vous souhaitez désactiver ZAP pour votre client 365 Office ou un ensemble d'utilisateurs, utilisez le paramètre **ZapEnabled** de la cmdlet [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), une applet de commande EOP.
    
Dans l'exemple suivant, ZAP est désactivé pour une stratégie de filtrage de contenu nommée «test».
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>FAQ

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>Que se passe-t-il si un message légitime est déplacé vers le dossier courrier indésirable?
  
Vous devez suivre le processus de création de rapports normal pour les faux positifs. La seule raison pour laquelle le message est déplacé de la boîte de réception vers le dossier de courrier indésirable est que le service a déterminé que le message était du courrier indésirable ou malveillant.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>Que faire en cas d'utilisation de la mise en quarantaine Office 365 au lieu du dossier courrier indésirable?
  
ZAP ne déplace pas les messages en quarantaine dans la boîte de réception pour le moment.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>Que se passe-t-il si j'utilise une règle de flux de messagerie personnalisée (règle bloquer/autoriser)?
  
Les règles créées par les administrateurs (règles de flux de messagerie) ou les règles de blocage et d'autorisation sont prioritaires. Ces messages sont exclus des critères de fonctionnalité.
  
## <a name="related-topics"></a>Voir aussi

[Protection contre le courrier indésirable pour Office 365](anti-spam-protection.md)
  
[Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](reduce-spam-email.md)
  

