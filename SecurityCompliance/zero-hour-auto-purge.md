---
title: Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
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
ms.openlocfilehash: dabe4caf8916d3f0de7a70cb3d056dd9a7fdcc3f
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857242"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Purge automatique zéro heure - protection contre le courrier indésirable et les programmes malveillants

Purge automatique zéro heures (ZAP) est une fonctionnalité de protection de messagerie qui détecte les messages qui ont déjà été remis aux boîtes aux lettres des utilisateurs avec le courrier indésirable ou un programme malveillant, puis affiche le contenu malveillant sans conséquence. Comment ZAP cela dépend du type de contenu malveillant détecté.
  
ZAP est disponible avec la valeur par défaut Exchange Online Protection est fourni avec un abonnement à Office 365 qui contient les boîtes aux lettres Exchange Online.
  
## <a name="how-does-zap-work"></a>Comment fonctionne la ZAP ?

Met à jour les signatures de moteur et des programmes malveillants contre le courrier indésirable dans Office 365 en temps réel au quotidien. Toutefois, les utilisateurs peuvent encore avoir des messages remis à leurs boîtes aux lettres pour différentes raisons, y compris lorsque le contenu a été weaponized une fois qu’il a été remis tout d’abord aux utilisateurs malveillants. SUPPRIMER les adresses cela en surveillant en permanence des mises à jour pour les signatures de courrier indésirable et les programmes malveillants Office 365, et peut par conséquent rechercher et supprimer des messages remis précédemment déjà dans la boîte de réception. Pour le courrier électronique qui a été déjà identifié comme courrier indésirable, ZAP déplace les messages non lus pour le dossier de courrier indésirable de l’utilisateur. Pour les logiciels malveillants nouvellement détecté, ZAP supprime les pièces jointes à partir du message électronique, quelle que soit la si le message a été lu ou non. L’inverse est vrai pour les messages qui ont été incorrectement classés comme malveillants.
  
L’action ZAP est transparente pour l’utilisateur de boîte aux lettres, qu’il n’est pas avertie que le message a été déplacé.
  
Autoriser les listes, [les règles de flux de messagerie](https://go.microsoft.com/fwlink/p/?LinkId=722755)et les règles de l’utilisateur final ou des filtres supplémentaires sont prioritaires sur ZAP.
  
 **Contenu de cet article :**
  
> [Définir la stratégie de filtrage du courrier indésirable](zero-hour-auto-purge.md#BK_SetSpam)
    
> [Voir si ZAP déplacé votre message](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [Désactiver ZAP](zero-hour-auto-purge.md#BK_Posh)
    
> [FAQ](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a>Utilisation de ZAP

ZAP est activée par défaut, mais vous avez pour vous assurer que les deux conditions sont remplies :
  
- Stratégie de filtrage du courrier indésirable est défini sur [déplacer le message vers le dossier courrier indésirable](zero-hour-auto-purge.md#BK_SetSpam).
    
    Vous pouvez également créer une stratégie de filtrage du courrier indésirable qui s’applique uniquement à un ensemble d’utilisateurs si vous ne voulez pas que toutes les boîtes aux lettres à être filtré par ZAP.
    
- L’utilisateur [Options \> courrier indésirable](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).
    
Si vous souhaitez [voir si ZAP déplacé votre message](zero-hour-auto-purge.md#BK_DidZAPMove), vous pouvez utiliser l’outil de suivi des messages Exchange Online.
  
Administrateurs peuvent également [désactiver ZAP](zero-hour-auto-purge.md#BK_Posh) à l’aide de PowerShell. 
  
 **Pour définir la stratégie de filtrage du courrier indésirable**
  
1. Se connecter à la [permettant de se connecter à Office 365 pour professionnels](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) et choisissez **protection** \> **filtre de courrier indésirable**. 
    
    ![Dans le CAE choisissez protection, puis de filtre de courrier indésirable](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. Choisissez la stratégie de filtrage que vous souhaitez ajuster, ou choisissez **Ajouter**![icône Ajouter](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) pour créer un nouveau. 
    
    Dans la capture d’écran précédente, la stratégie est nommée « Default », mais si vous créez des stratégies de filtrage du courrier indésirable supplémentaire vous pouvez leur donner un nom différent. Vous pouvez également appliquer la stratégie à un ensemble limité d’utilisateurs.
    
3. Dans la fenêtre de la stratégie, choisissez **actions en bloc et de courrier indésirable**et assurez-vous que **le courrier indésirable** est défini sur **déplacer le message vers le dossier courrier indésirable**. 
    
    Si vous choisissez **Enregistrer** à ce stade, la stratégie s’applique à votre organisation cliente Office 365. 
    
    ![Définir les actions en bloc et de courrier indésirable pour déplacer le message vers le dossier courrier indésirable](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. Si vous avez créé une nouvelle stratégie et que vous voulez appliquer la stratégie à un ensemble d’utilisateurs, faites défiler jusqu'à la section **Appliquée à** la fenêtre de filtre de stratégie et dans les contrôles de menu Choisir les **destinataires**, **domaine**ou les **appartenances aux groupes** , vous vous souhaitez appliquer la stratégie. Vous pouvez également définir des exceptions et conditions supplémentaires. 
    
    ![Dans la section appliquée à choisir les destinataires](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    Cliquez sur **Enregistrer** pour appliquer la stratégie aux utilisateurs sélectionnés. 
    
 **Pour voir si ZAP déplacé votre message**
  
- Vous pouvez utiliser [trouver et résoudre les problèmes de remise de courrier électronique comme un Office 365 pour professionnels admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) pour déterminer si le message a été déplacé par ZAP : 
    
    Rechercher le texte « heures zéro automatique Purge (ZAP) » dans vos informations de suivi pour identifier un message qui a été déplacé par ZAP.
    
 **Pour désactiver ZAP**
  
- Si vous souhaitez désactiver supprimer pour votre client Office 365, ou un ensemble d’utilisateurs, utilisez le paramètre **ZapEnabled** de [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), une applet de commande EOP.
    
    Dans l’exemple suivant, ZAP est désactivé pour une stratégie de filtrage de contenu nommée « Test ».
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a>FAQ
<a name="BK_FAQ"> </a>

 **Que se passe-t-il si un message légitime est déplacé vers le dossier courrier indésirable ?**
  
Vous devez suivre le processus de création de rapports normal de faux positifs. La seule raison pour laquelle le message est déplacé vers le dossier courrier indésirable à partir de la boîte de réception serait parce que le service a déterminé que le message a été le courrier indésirable ou malveillant.
  
 **Que se passe-t-il si utiliser la mise en quarantaine Office 365 au lieu du dossier courrier indésirable ?**
  
ZAP ne déplacer des messages en quarantaine à partir de la boîte de réception à ce stade.
  
 **Que se passe-t-il si j’ai une règle de flux de messagerie personnalisé (bloquer / règle Autoriser) ?**
  
Règles créées par des administrateurs (règles de flux de messagerie) ou bloquer et autoriser les règles sont prioritaires. Ces messages sont exclues les critères de fonctionnalité.
  
## <a name="related-topics"></a>Voir aussi
<a name="BK_FAQ"> </a>

[Protection contre le courrier indésirable pour Office 365](anti-spam-protection.md)
  
[Bloquer le courrier indésirable à l'aide du filtre d'Office 365 afin d'éviter les problèmes de faux négatifs](block-email-spam-to-prevent-false-negatives.md)
  

