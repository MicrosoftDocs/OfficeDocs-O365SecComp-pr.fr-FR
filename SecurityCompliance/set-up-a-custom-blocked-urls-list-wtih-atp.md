---
title: Configurer une liste d’URL bloquées personnalisée à l’aide de liens fiables Office 365 ATP
ms.author: tracyp
author: msfttracyp
manager: dansimp
audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
ms.collection:
- M365-security-compliance
description: Découvrez comment configurer une liste d’URL bloquées pour votre organisation à l’aide d’Office 365 Advanced Threat Protection. Les URL bloquées s’appliquent aux messages électroniques et aux documents Office en fonction de vos stratégies de liens fiables ATP.
ms.openlocfilehash: 8d2b93fca599359ec1c6f4b4b3794ee2ccb466fe
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230328"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a>Configurer une liste d’URL bloquées personnalisée à l’aide de liens fiables Office 365 ATP

> [!IMPORTANT]
> Cet article est destiné aux clients professionnels qui disposent d' [Office 365 Advanced Threat Protection](office-365-atp.md). Si vous êtes un utilisateur à domicile et que vous recherchez des informations sur les liens fiables dans Outlook, consultez la rubrique [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Avec [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), votre organisation peut avoir une liste personnalisée d’adresses de sites Web (URL) bloquées. Lorsqu’une URL est bloquée, les personnes qui cliquent sur les liens vers l’URL bloquée sont dirigées vers une [page d’avertissement](atp-safe-links-warning-pages.md) semblable à l’image suivante: 
  
![Ce site est bloqué](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
La liste des URL bloquées est définie par l’équipe de sécurité Office 365 de votre organisation et s’applique à tous les membres de l’organisation qui sont couverts par les stratégies de liens approuvés Office 365 ATP. 
  
Lisez cet article pour découvrir comment configurer la liste des URL bloquées personnalisées de votre organisation pour les [liens fiables ATP dans Office 365](atp-safe-links.md).
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a>Afficher ou modifier une liste personnalisée d’URL bloquées

Les [liens approuvés ATP dans Office 365](atp-safe-links.md) utilisent plusieurs listes, y compris la liste des URL bloquées personnalisées de votre organisation. Si vous disposez des autorisations nécessaires, vous pouvez configurer la liste personnalisée de votre organisation. Pour ce faire, vous devez modifier la stratégie de liens approuvés par défaut de votre organisation.

Pour modifier (ou définir) des stratégies ATP, vous devez disposer de l’un des rôles décrits dans le tableau suivant: 

|Role  |WHERE/How Assigned  |
|---------|---------|
|Administrateur général Office 365 |La personne qui s’inscrit pour acheter Office 365 est un administrateur global par défaut. (Pour en savoir plus, consultez la rubrique [à propos des rôles d’administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Administrateur de sécurité |Centre d’administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()|
|Gestion de l’organisation Exchange Online |Centre d’administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>ou <br>  Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations &amp; dans le centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).

### <a name="to-view-or-edit-a-custom-blocked-urls-list"></a>Pour afficher ou modifier une liste d’URL bloquées personnalisée
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou scolaire. 
    
2. Dans le volet de navigation de gauche, sous **gestion des menaces**, sélectionnez **liens approuvés**de **stratégie** \> .
    
3. Dans la section **stratégies qui s’appliquent à l’ensemble de l’organisation** , sélectionnez **par défaut**, puis **modifier** (le bouton modifier ressemble à un crayon).<br/>![Cliquez sur modifier pour modifier votre stratégie par défaut pour la protection des liens fiables.](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)<br/>Cela vous permet d’afficher la liste des URL bloquées. Dans un premier temps, il se peut que vous n’ayez aucune URL répertoriée ici.<br/>![Liste des URL bloquées dans la stratégie de liens approuvés par défaut](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. Sélectionnez la zone **Entrez une URL valide** , tapez une URL, puis choisissez le signe plus (**+**). 

5. Lorsque vous avez terminé d’ajouter des URL, dans le coin inférieur droit de l’écran, sélectionnez **Enregistrer**.
    
## <a name="a-few-things-to-keep-in-mind"></a>Quelques éléments à garder à l’esprit

Lorsque vous ajoutez des URL à votre liste, gardez les points suivants à l’esprit: 

- N’incluez pas une barre oblique **/**() à la fin de l’URL. Par exemple, au lieu de `http://www.contoso.com/`taper, `http://www.contoso.com`entrez.
    
- Vous pouvez spécifier une URL de domaine uniquement (par `contoso.com` exemple `tailspintoys.com`, ou). Cette opération bloque les clics sur les URL qui contiennent le domaine.

- Vous pouvez spécifier un sous-domaine ( `toys.contoso.com*`par exemple) sans bloquer un domaine complet `contoso.com`(par exemple,). Cette opération bloque le clic sur toute URL qui contient le sous-domaine, mais ne bloque pas les clics vers une URL qui contient le domaine complet.  
    
- Vous pouvez inclure jusqu’à trois astérisques génériques (\*) par URL. Le tableau suivant répertorie quelques exemples de ce que vous pouvez entrer et de l’effet de ces entrées.
    
|**Exemple d’entrée**|**Ce qu’il fait**|
|:-----|:-----|
|`contoso.com` ou `*contoso.com*`  <br/> |Bloque le domaine, les sous-domaines et les chemins d' `https://www.contoso.com`accès `http://sub.contoso.com`, par exemple, et`http://contoso.com/abc`  <br/> |
|`http://contoso.com/a`  <br/> |Bloque un `http://contoso.com/a` site, mais pas les sous-chemins supplémentaires comme`http://contoso.com/a/b`  <br/> |
|`http://contoso.com/a*`  <br/> |Bloque un `http://contoso.com/a` site et des sous-chemins supplémentaires comme`http://contoso.com/a/b`  <br/> |
|`http://toys.contoso.com*`  <br/> |Bloque un sous-domaine («jouets» dans ce cas) tout en permettant de cliquer sur d' `http://contoso.com` autres `http://home.contoso.com`URL de domaine (par exemple, ou).  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a>Procédure de définition des exceptions pour certains utilisateurs d’une organisation

Si vous souhaitez que certains groupes puissent afficher les URL susceptibles d’être bloquées pour d’autres, vous pouvez spécifier une stratégie de liens approuvés ATP qui s’applique à des destinataires spécifiques. Consultez [la rubrique Configurer une liste d’URL personnalisée «ne pas réécrire» à l’aide des liens fiables ATP](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
  

