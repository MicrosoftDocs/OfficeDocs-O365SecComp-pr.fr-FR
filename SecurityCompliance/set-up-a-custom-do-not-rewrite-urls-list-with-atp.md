---
title: Configurer une liste d’URL non--réécriture personnalisée à l’aide d’Office 365 DAV fiables liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
ms.collection: M365-security-compliance
description: Lorsque vous configurez vos stratégies de liens fiables DAV, vous pouvez inclure une réécriture non ' liste d’URL pour activer certaines personnes de votre organisation à visiter des sites que vous incluez dans votre liste.
ms.openlocfilehash: 87a245e2f21408cd06d483ec5fdcdac47ce7e317
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995375"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a>Configurer une liste d’URL non--réécriture personnalisée à l’aide d’Office 365 DAV fiables liens

> [!IMPORTANT]
> Cet article est destiné aux entreprises. Si vous êtes un utilisateur vous recherchez des informations sur les liens sécurisés dans Outlook, voir [sécurité Outlook.com avancés](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Avec [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), votre organisation peut avoir une [URL bloqués personnalisées](set-up-a-custom-blocked-urls-list-wtih-atp.md), telles que les adresses de lorsque les utilisateurs cliquent sur le web (URL) dans les messages électroniques ou certains documents Office, ils ne peuvent pas d’accéder à ces URL. Votre organisation peut également disposer des listes personnalisées « pas de rewrite » pour des groupes spécifiques dans votre organisation. Une liste « pas de rewrite » permet à certaines personnes de visiter URL sinon bloqués par des [Liaisons fiables DAV dans Office 365](atp-safe-links.md). 
  
Cet article décrit comment spécifier une liste d’URL qui sont exclus de l’analyse des liens fiables DAV et quelques points importants à prendre en compte.

## <a name="set-up-a-do-not-rewrite-list"></a>Définir une liste « pas de rewrite »

Protection des liens fiables DAV utilise plusieurs listes, y compris la liste des URL de votre organisation bloqué et les listes de « pas de rewrite » pour les exceptions. Si vous disposez des autorisations nécessaires, vous pouvez configurer vos listes personnalisées « pas de rewrite ». Cela lorsque vous ajoutez ou modifiez des stratégies de liens fiables qui s’appliquent à des destinataires spécifiques dans votre organisation. 

Pour modifier (ou définir) stratégies DAV, vous devez posséder un des rôles décrits dans le tableau suivant :

|Rôle  |Où/procédure affecté  |
|---------|---------|
|Administrateur Global d’Office 365 |La personne qui s’inscrit à acheter Office 365 est un administrateur global par défaut. (Voir [les rôles d’administration sur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) pour en savoir plus).         |
|Administrateur de sécurité |Centre d’administration Active Directory Azure ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Gestion de l’organisation en ligne Exchange |Centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Pour en savoir plus sur les rôles et autorisations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).

### <a name="to-view-or-edit-a-custom-do-not-rewrite-urls-list"></a>Pour afficher ou modifier une liste d’URL personnalisée « pas de rewrite »
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces** \> **stratégie** \> **Liens fiables**.
    
3. Dans la section **stratégies qui s’appliquent à des destinataires spécifiques** , choisissez **Nouveau** (nouveau bouton ressemble à un signe plus ( **+**)) pour créer une nouvelle stratégie. (Vous pouvez également, vous pouvez modifier une stratégie existante).<br/>![Cliquez sur Nouveau pour ajouter une stratégie de liens sécurisés pour les destinataires de messages électroniques spécifique](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. Spécifiez un nom et une description pour votre stratégie.
    
5. Dans la section **ne pas réécrire les URL suivantes** , sélectionnez la zone **Tapez une URL valide** et tapez une URL, puis cliquez sur le signe plus (+). 
    
6. Dans la section **Appliquée à** , sélectionnez **le destinataire est un membre du**, puis les groupes que vous souhaitez inclure dans votre stratégie de. Cliquez sur **Ajouter**, puis cliquez sur **OK**.
    
7. Lorsque vous avez terminé d’ajouter des URL, dans le coin inférieur droit de l’écran, cliquez sur **Enregistrer**.
    
> [!NOTE]
> Veillez à consulter la liste personnalisée de votre organisation d’URL bloquées. Voir [configurer une liste d’URL bloquée personnalisée à l’aide de liens fiables DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md). 
  
## <a name="important-points-to-keep-in-mind"></a>Points importants à prendre en compte

- Les URL que vous spécifiez dans la liste « pas de rewrite » sont exclues liens sécurisés DAV pour les destinataires d’analyse que vous spécifiez.
 
- Lorsque vous spécifiez une liste « pas de rewrite » pour une stratégie de liens fiables DAV, vous pouvez inclure jusqu'à trois astérisques générique (\*). Des caractères génériques (\*) sont considérées comme tels que pour les entrées de `contoso.com`, qui ne pas explicitement incluez les préfixes ou sous-domaines, comme `http://` ou `https://`. Cela signifie que l’entrée, tel que `contoso.com` est similaire à `*contoso.com*` pour votre liste « pas de rewrite ».

- Si vous avez déjà une liste d’URL dans votre liste des « pas de rewrite », veillez à consulter cette liste et ajouter des caractères génériques comme il convient. Par exemple, si votre liste existante a une entrée comme `http://contoso.com/a` et que vous souhaitez inclure plusieurs comme `http://contoso.com/a/b` dans votre stratégie, ajoutez un caractère générique à votre entrée afin qu’il ressemble à `http://contoso.com/a*`.
    
- N’incluez pas une barre oblique (/) dans les URL que vous spécifiez dans votre liste des « pas de rewrite ». Par exemple, plutôt que d’entrer `contoso.com/` dans votre liste des « pas de rewrite », entrez `contoso.com`.
    
Les tableau Voici des exemples de ce que vous pouvez entrer et les effets que ces entrées ont.
    
|**Exemple d’entrée**|**Fonction**|
|:-----|:-----|
|`*contoso.com*`  <br/> |Permet à des destinataires spécifiques à un domaine, des sous-domaines et des chemins d’accès, tel que `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, ou`http://www.contoso.com/a`  <br/> |
|`http://contoso.com/a`  <br/> |Permet à des destinataires spécifiques à visiter un site comme `http://contoso.com/a`, mais pas les sections que`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Permet à des destinataires spécifiques à visiter un site comme `http://contoso.com/a` et sections`http://contoso.com/a/b`  <br/> |
   
 