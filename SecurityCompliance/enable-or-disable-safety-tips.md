---
title: Activer ou désactiver les conseils de sécurité dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
description: Indique comment activer et désactiver les astuces de sécurité dans les messages électroniques à des administrateurs Office 365 et EOP.
ms.openlocfilehash: 8e5d8bf1d2f831b5d74ca3accd8b434519bfeaab
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180854"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a>Activer ou désactiver les conseils de sécurité dans Office 365

Exchange Online Protection (EOP) ajoute ou marquages, Conseil de sécurité pour les messages électroniques qu’il fournit. Ces conseils de sécurité fournissent des destinataires avec un moyen rapide pour déterminer si un message provient d’un coffre-fort, visual vérifié expéditeur, si le message a été marqué comme courrier indésirable par Office 365, si le message contient un élément suspect comme un hameçonnage semblant, ou si les images externes ont été bloqué. Office 365 et EOP autonome administrateurs peuvent modifier un paramètre de stratégie de courrier indésirable pour activer ou désactiver les conseils de sécurité s’affiche dans le message électronique dans Outlook et d’autres clients de messagerie de bureau. 
  
Office 365 Active les conseils de sécurité par défaut pour votre organisation et nous vous conseillons de laisser les activé afin de lutter contre les attaques de courrier indésirable et l’hameçonnage. Vous ne pouvez pas désactiver les conseils de sécurité pour Outlook sur le web.
  
Pour consulter des exemples et pour en savoir plus sur les informations affichées dans les conseils de sécurité, voir [conseils de sécurité dans les messages électroniques dans Office 365.](safety-tips-in-office-365.md)
  
Contenu de cet article :
  
- [Pour activer ou désactiver les conseils de sécurité à l’aide de la sécurité de 365 Office &amp; centre de conformité](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [Pour activer ou désactiver les conseils de sécurité à l’aide de PowerShell](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a>Pour activer ou désactiver les conseils de sécurité à l’aide de la sécurité de 365 Office &amp; centre de conformité
<a name="SandCCsafetytip"> </a>

1. Accédez à [https://protection.office.com](https://protection.office.com).
    
2. Connectez-vous à Office 365 à l'aide de votre compte professionnel ou scolaire.
    
3. Cliquez sur **Gestion des menaces** \> **stratégie**. 
    
4. Dans la page **stratégie** , choisissez **Anti-Spam**.
    
    ![Cette capture d’écran montre comment accéder à la page de paramètres de blocage du courrier indésirable dans la sécurité &amp; centre de conformité.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. Dans la page **paramètres de blocage du courrier indésirable** , choisissez l’onglet **personnalisé** . 
    
    ![Cette capture d’écran montre l’emplacement de l’onglet personnalisé dans la page Paramètres de blocage du courrier indésirable dans la sécurité &amp; centre de conformité.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. Si nécessaire, choisissez le commutateur des **paramètres personnalisés** pour activer les paramètres personnalisés. Si le commutateur des paramètres personnalisés est défini sur **désactivé**, vous ne pourrez pas modifier les stratégies de filtrage du courrier indésirable.
    
    ![Cette capture d’écran montre filtre anti-courrier indésirable personnalisé désactivés des paramètres de stratégie.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. Développez la stratégie anti-courrier indésirable que vous souhaitez modifier, puis choisissez **Modifier la stratégie**. Par exemple, choisissez la flèche vers le bas en regard de **courrier indésirable par défaut filtrer la stratégie**. Ou, si vous le souhaitez, vous pouvez créer une nouvelle stratégie, cliquez sur **Ajouter une stratégie**.
    
8. Développez actions **en bloc et courrier indésirable** . 
    
9. Pour activer les conseils de sécurité, sous **Les conseils de sécurité**, activez la case à cocher **sur** . Pour désactiver les conseils de sécurité, désactivez la case à cocher **sur** . 
    
10. Sélectionnez **Save (Enregistrer)**.
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a>Pour activer ou désactiver les conseils de sécurité à l’aide de PowerShell
<a name="pshellsafetytip"> </a>

Administrateurs peuvent utiliser Exchange Online PowerShell pour activer ou désactiver les conseils de sécurité. Utilisez l’applet de commande Set-HostedContentFilterPolicy pour activer ou désactiver les conseils de sécurité dans une stratégie de filtrage du courrier indésirable.
  
1. Connexion à Exchange Online PowerShell. Pour plus d’informations, consultez la rubrique [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Exécutez l’applet de commande Set-HostedContentFilterPolicy pour activer ou désactiver les conseils de sécurité :
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

Où :
    
  -  *nom de la stratégie* est le nom de la stratégie que vous souhaitez modifier, par exemple **par défaut**.
    
  -  `$true`permet de conseils de sécurité pour la stratégie de filtrage du courrier indésirable. 
    
  -  `$false`désactive les conseils de sécurité pour la stratégie de filtrage du courrier indésirable. 
    
    Par exemple, pour désactiver les conseils de sécurité pour la stratégie de filtrage du courrier indésirable par défaut, exécutez la commande suivante :
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

Pour plus d’informations sur cette applet de commande, voir [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).
    
## <a name="still-need-help"></a>Vous avez encore besoin d'aide ?
<a name="pshellsafetytip"> </a>

Si vous désactivé les conseils de sécurité, mais sont toujours les voir dans vos courriers électroniques, vérifiez ces éléments :
  
- Vous ne pouvez pas désactiver les conseils de sécurité pour Outlook sur le web. Essayez d’afficher la même messagerie électronique dans un autre client, tel que Outlook.
    
- Conseils de sécurité sont activées par défaut pour chacune de celles-ci qui utilise EOP, cela inclut tous les utilisateurs Office 365. Afin de désactiver les conseils de sécurité d’apparaître dans le message électronique, vous devez les désactiver à l’aide d’une stratégie de filtrage du courrier indésirable comme décrit dans cette rubrique. Une fois que vous avez configuré la stratégie, assurez-vous qu’il est activé. Pour plus d’informations sur l’activation des stratégies de filtrage du courrier indésirable, consultez [configurer vos stratégies de filtrage du courrier indésirable](https://technet.microsoft.com/library/jj200684.aspx).
    
Pour les autres méthodes permettent de lutter contre le courrier indésirable et l’hameçonnage, voir [Office 365 messagerie Anti-Spam Protection](anti-spam-protection.md).
  

