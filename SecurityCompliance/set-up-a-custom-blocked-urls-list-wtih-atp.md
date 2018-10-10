---
title: Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Lisez cet article pour apprendre à configurer une liste d’URL bloqués pour votre organisation à l’aide d’Office 365 avancée protection contre les menaces. Les URL bloquées s’appliquera aux messages électroniques et des documents Office en fonction de vos stratégies de liens fiables DAV.
ms.openlocfilehash: 0429546e521bf3f6b7144342ab0997e924c2f616
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454361"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Configurer une liste d’URL bloquée personnalisée à l’aide d’Office 365 DAV fiables liens

Avec [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), votre organisation peut avoir une liste personnalisée d’adresses de site Web (URL) qui sont bloqués. Lorsqu’une URL est bloquée, les personnes qui cliquent sur des liens vers l’URL bloqué sont dirigés vers une [page d’avertissement](atp-safe-links-warning-pages.md) qui ressemble à l’image suivante : 
  
![Ce site est bloqué.](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
La liste des URL bloquée est définie par l’équipe de sécurité de votre organisation Office 365, et cette liste s’applique à tout le monde dans l’organisation qui est couvert par les stratégies de liaisons sans échec de Office 365 DAV. 
  
Lisez cet article pour apprendre à configurer la liste des URL bloqué personnalisé de votre organisation pour les [Liens sécurisés DAV dans Office 365](atp-safe-links.md).
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>Afficher ou modifier une liste personnalisée d’URL bloquées

[Liens approuvés DAV dans Office 365](atp-safe-links.md) utilise plusieurs listes, y compris la liste des URL bloqué personnalisé de votre organisation. Si vous disposez des autorisations nécessaires, vous pouvez configurer la liste personnalisée de votre organisation. Pour cela, en modifiant la stratégie de liens fiables par défaut de votre organisation.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie** \> **Liens fiables**.
    
3. Dans la section **stratégies qui s’appliquent à toute l’organisation** , sélectionnez **par défaut**, puis choisissez **Modifier** (le bouton Modifier ressemble à un crayon). 
    
    ![Cliquez sur Modifier pour modifier votre stratégie par défaut pour la protection des liens fiables](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
    C’est là vous permet d’afficher la liste des URL bloquées. Notez que dans un premier temps, vous n’avez aucune URL répertoriées.
    
    ![La liste des URL bloqués est par défaut stratégie liens fiables qui s’applique à toute votre organisation.](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. Sélectionnez la zone **Tapez une URL valide** et tapez une URL, puis cliquez sur le signe plus (+). Voici quelques points à prendre en compte : 
    
  - Vous pouvez spécifier une URL de domaine (comme `contoso.com` ou `tailspintoys.com`). Cela empêchera clics sur n’importe quelle URL qui contient le domaine.
    
  - N’incluez pas une barre oblique ( **/**) à la fin de l’URL. Par exemple, au lieu de saisir `http://www.contoso.com/`, entrez `http://www.contoso.com`.
    
  - Vous pouvez inclure jusqu'à trois astérisques générique (\*) par l’URL. Le tableau suivant répertorie quelques exemples de ce que vous pouvez entrer et les effets que ces entrées ont.
    
|**Exemple d’entrée**|**Fonction**|
|:-----|:-----|
|`contoso.com`ou`*contoso.com*`  <br/> |Bloque le domaine, les sous-domaines et les chemins d’accès, tel que `https://www.contoso.com`, `http://sub.contoso.com`, et`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |Bloque un site `http://contoso.com/a` mais pas les autres sections`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Bloque un site `http://contoso.com/a` et sections supplémentaires`http://contoso.com/a/b`  <br/> |
   
5. Lorsque vous avez terminé d’ajouter des URL, dans le coin inférieur droit de l’écran, cliquez sur **Enregistrer**.
    
## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a>Comment définir des exceptions pour certains utilisateurs dans une organisation

Si vous souhaitez que certains groupes pour être en mesure d’afficher les URL qui peuvent être bloquées pour d’autres personnes, vous pouvez spécifier une stratégie de liens fiables DAV qui s’applique à des destinataires spécifiques. Voir [configurer une liste d’URL personnalisée du « pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
  
## <a name="related-topics"></a>Voir aussi

[Protection avancée contre les menaces dans Office 365](office-365-atp.md)
  
[Liens DAV Safe dans Office 365](atp-safe-links.md)
  
[Définir des stratégies de liens fiables DAV dans Office 365](set-up-atp-safe-links-policies.md)
  
[Pièces jointes DAV Safe dans Office 365](atp-safe-attachments.md)

[Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)
  

