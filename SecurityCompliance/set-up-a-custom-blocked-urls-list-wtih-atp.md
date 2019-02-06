---
title: Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/05/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Découvrez comment configurer une liste d’URL bloqués pour votre organisation à l’aide d’Office 365 avancée protection contre les menaces. Les URL bloquées s’appliquera aux messages électroniques et des documents Office en fonction de vos stratégies de liens fiables DAV.
ms.openlocfilehash: 4146424056c9a5b30f51a58fd020df912fa048ef
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741017"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens

Avec [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), votre organisation peut avoir une liste personnalisée d’adresses de site Web (URL) qui sont bloqués. Lorsqu’une URL est bloquée, les personnes qui cliquent sur des liens vers l’URL bloqué sont dirigés vers une [page d’avertissement](atp-safe-links-warning-pages.md) qui ressemble à l’image suivante : 
  
![Ce site est bloqué.](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
La liste des URL bloquée est définie par l’équipe de sécurité de votre organisation Office 365, et cette liste s’applique à tout le monde dans l’organisation qui est couvert par les stratégies de liaisons sans échec de Office 365 DAV. 
  
Lisez cet article pour apprendre à configurer la liste des URL bloqué personnalisé de votre organisation pour les [Liens sécurisés DAV dans Office 365](atp-safe-links.md).
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>Afficher ou modifier une liste personnalisée d’URL bloquées

[Liens approuvés DAV dans Office 365](atp-safe-links.md) utilise plusieurs listes, y compris la liste des URL bloqué personnalisé de votre organisation. Si vous disposez des autorisations nécessaires, vous pouvez configurer la liste personnalisée de votre organisation. Pour cela, en modifiant la stratégie de liens fiables par défaut de votre organisation.

Pour modifier (ou définir) stratégies DAV, vous devez posséder un des rôles décrits dans le tableau suivant : 

|Rôle  |Où/procédure affecté  |
|---------|---------|
|Administrateur Global d’Office 365 |La personne qui s’inscrit à acheter Office 365 est un administrateur global par défaut. (Voir [les rôles d’administration sur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) pour en savoir plus).         |
|Administrateur de sécurité Office 365 |Centre d’administration ([https://aka.ms/admincenter](https://aka.ms/admincenter))|
|Gestion de l’organisation en ligne Exchange |Centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Liens fiables**.
    
3. Dans la section **stratégies qui s’appliquent à toute l’organisation** , sélectionnez **par défaut**, puis choisissez **Modifier** (le bouton Modifier ressemble à un crayon).<br/>![Cliquez sur Modifier pour modifier votre stratégie par défaut pour la protection des liens fiables](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)<br/>Cela vous permet d’afficher la liste des URL bloquées. Tout d’abord, vous ne disposez pas des URL répertoriées ici.<br/>![Liste des URL dans la stratégie de liens fiables par défaut bloqués](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. Sélectionnez la zone **Tapez une URL valide** , tapez une URL, puis cliquez sur le signe plus (**+**). 

5. Lorsque vous avez terminé d’ajouter des URL, dans le coin inférieur droit de l’écran, cliquez sur **Enregistrer**.
    
## <a name="a-few-things-to-keep-in-mind"></a>Quelques éléments à prendre en compte

Lorsque vous ajoutez à votre liste des URL, gardez les points suivants à l’esprit : 

- N’incluez pas une barre oblique ( **/**) à la fin de l’URL. Par exemple, au lieu de saisir `http://www.contoso.com/`, entrez `http://www.contoso.com`.
    
- Vous pouvez spécifier une URL de domaine (comme `contoso.com` ou `tailspintoys.com`). Cela empêchera clics sur n’importe quelle URL qui contient le domaine.

- Vous pouvez spécifier un sous-domaine (comme `toys.contoso.com*`) sans bloquer un domaine complet (comme `contoso.com`). Il est bloc clique sur une URL qui contient le sous-domaine, mais il ne bloque clique sur une URL qui contient le domaine complet.  
    
- Vous pouvez inclure jusqu'à trois astérisques générique (\*) par l’URL. Le tableau suivant répertorie quelques exemples de ce que vous pouvez entrer et les effets que ces entrées ont.
    
|**Exemple d’entrée**|**Fonction**|
|:-----|:-----|
|`contoso.com`ou`*contoso.com*`  <br/> |Bloque le domaine, les sous-domaines et les chemins d’accès, tel que `https://www.contoso.com`, `http://sub.contoso.com`, et`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |Bloque un site `http://contoso.com/a` mais pas les autres sections`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Bloque un site `http://contoso.com/a` et sections supplémentaires`http://contoso.com/a/b`  <br/> |
|`http://toys.contoso.com*`  <br/> |Bloque un sous-domaine (« toys » dans ce cas), mais autoriser les clics vers d’autres URL de domaine (comme `http://contoso.com` ou `http://home.contoso.com`).  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a>Comment définir des exceptions pour certains utilisateurs dans une organisation

Si vous souhaitez que certains groupes pour être en mesure d’afficher les URL qui peuvent être bloquées pour d’autres personnes, vous pouvez spécifier une stratégie de liens fiables DAV qui s’applique à des destinataires spécifiques. Voir [configurer une liste d’URL personnalisée du « pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
  

