---
title: Activer ou désactiver les conseils de sécurité dans Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/6/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
description: Indique comment activer et désactiver les astuces de sécurité dans les messages électroniques à des administrateurs Office 365 et EOP.
ms.openlocfilehash: 3a8257f9d34ec5def54e2b9c9e919172366d023f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528204"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a><span data-ttu-id="ee9ac-103">Activer ou désactiver les conseils de sécurité dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ee9ac-103">Enable or disable safety tips in Office 365</span></span>

<span data-ttu-id="ee9ac-p101">Exchange Online Protection (EOP) ajoute ou marquages, Conseil de sécurité pour les messages électroniques qu’il fournit. Ces conseils de sécurité fournissent des destinataires avec un moyen rapide pour déterminer si un message provient d’un coffre-fort, visual vérifié expéditeur, si le message a été marqué comme courrier indésirable par Office 365, si le message contient un élément suspect comme un hameçonnage semblant, ou si les images externes ont été bloqué. Office 365 et EOP autonome administrateurs peuvent modifier un paramètre de stratégie de courrier indésirable pour activer ou désactiver les conseils de sécurité s’affiche dans le message électronique dans Outlook et d’autres clients de messagerie de bureau.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p101">Exchange Online Protection (EOP) adds, or stamps, a safety tip to email messages that it delivers. These safety tips provide recipients with a quick, visual way to determine if a message is from a safe, verified sender, if the message has been marked as spam by Office 365, if the message contains something suspicious such as a phishing scam, or if external images have been blocked. Office 365 and EOP-standalone admins can edit a spam policy setting to enable or disable safety tips from being displayed in email in Outlook and other desktop email clients.</span></span> 
  
<span data-ttu-id="ee9ac-p102">Office 365 Active les conseils de sécurité par défaut pour votre organisation et nous vous conseillons de laisser les activé afin de lutter contre les attaques de courrier indésirable et l’hameçonnage. Vous ne pouvez pas désactiver les conseils de sécurité pour Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p102">Office 365 enables safety tips by default for your organization and we recommend that you leave them enabled to help combat spam and phishing attacks. You can't disable safety tips for Outlook on the web.</span></span>
  
<span data-ttu-id="ee9ac-109">Pour consulter des exemples et pour en savoir plus sur les informations affichées dans les conseils de sécurité, voir [conseils de sécurité dans les messages électroniques dans Office 365.](safety-tips-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="ee9ac-109">To see examples and to learn about the information displayed in safety tips, see [Safety tips in email messages in Office 365.](safety-tips-in-office-365.md)</span></span>
  
<span data-ttu-id="ee9ac-110">Contenu de cet article :</span><span class="sxs-lookup"><span data-stu-id="ee9ac-110">In this topic:</span></span>
  
- [<span data-ttu-id="ee9ac-111">Pour activer ou désactiver les conseils de sécurité à l’aide de la sécurité de 365 Office &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="ee9ac-111">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [<span data-ttu-id="ee9ac-112">Pour activer ou désactiver les conseils de sécurité à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee9ac-112">To enable or disable safety tips by using PowerShell</span></span>](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="ee9ac-113">Pour activer ou désactiver les conseils de sécurité à l’aide de la sécurité de 365 Office &amp; centre de conformité</span><span class="sxs-lookup"><span data-stu-id="ee9ac-113">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>
<span data-ttu-id="ee9ac-114"><a name="SandCCsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="ee9ac-114"></span></span>

1. <span data-ttu-id="ee9ac-115">Accédez à [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="ee9ac-115">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ee9ac-116">Connectez-vous à Office 365 avec votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-116">Sign in to Office 365 with your work or school account.</span></span>
    
3. <span data-ttu-id="ee9ac-117">Cliquez sur **Gestion des menaces** \> **stratégie**.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-117">Choose **Threat Management** \> **Policy**.</span></span> 
    
4. <span data-ttu-id="ee9ac-118">Dans la page **stratégie** , choisissez **Anti-Spam**.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-118">On the **Policy** page, choose **Anti-Spam**.</span></span>
    
    ![Cette capture d’écran montre comment accéder à la page de paramètres de blocage du courrier indésirable dans la sécurité &amp; centre de conformité.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. <span data-ttu-id="ee9ac-120">Dans la page **paramètres de blocage du courrier indésirable** , choisissez l’onglet **personnalisé** .</span><span class="sxs-lookup"><span data-stu-id="ee9ac-120">On the **Anti-spam settings** page choose the **Custom** tab.</span></span> 
    
    ![Cette capture d’écran montre l’emplacement de l’onglet personnalisé dans la page Paramètres de blocage du courrier indésirable dans la sécurité &amp; centre de conformité.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. <span data-ttu-id="ee9ac-p103">Si nécessaire, choisissez le commutateur des **paramètres personnalisés** pour activer les paramètres personnalisés. Si le commutateur des paramètres personnalisés est défini sur **désactivé**, vous ne pourrez pas modifier les stratégies de filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p103">If necessary, choose the **Custom settings** switch to turn on custom settings. If the custom settings switch is set to **Off**, you won't be able to modify spam filter policies.</span></span>
    
    ![Cette capture d’écran montre filtre anti-courrier indésirable personnalisé désactivés des paramètres de stratégie.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. <span data-ttu-id="ee9ac-p104">Développez la stratégie anti-courrier indésirable que vous souhaitez modifier, puis choisissez **Modifier la stratégie**. Par exemple, choisissez la flèche vers le bas en regard de **courrier indésirable par défaut filtrer la stratégie**. Ou, si vous le souhaitez, vous pouvez créer une nouvelle stratégie, cliquez sur **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p104">Expand the spam policy you want to modify and then choose **Edit policy**. For example, choose the down arrow next to **Default spam filter policy**. Or, if you want, you can create a new policy by choosing **Add a policy**.</span></span>
    
8. <span data-ttu-id="ee9ac-128">Développez actions **en bloc et courrier indésirable** .</span><span class="sxs-lookup"><span data-stu-id="ee9ac-128">Expand **Spam and bulk** actions.</span></span> 
    
9. <span data-ttu-id="ee9ac-p105">Pour activer les conseils de sécurité, sous **Les conseils de sécurité**, activez la case à cocher **sur** . Pour désactiver les conseils de sécurité, désactivez la case à cocher **sur** .</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p105">To enable safety tips, under **Safety Tips**, check the **On** checkbox. To disable safety tips, clear the **On** checkbox.</span></span> 
    
10. <span data-ttu-id="ee9ac-131">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-131">Choose **Save**.</span></span>
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a><span data-ttu-id="ee9ac-132">Pour activer ou désactiver les conseils de sécurité à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee9ac-132">To enable or disable safety tips by using PowerShell</span></span>
<span data-ttu-id="ee9ac-133"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="ee9ac-133"></span></span>

<span data-ttu-id="ee9ac-p106">Administrateurs peuvent utiliser Exchange Online PowerShell pour activer ou désactiver les conseils de sécurité. Utilisez l’applet de commande Set-HostedContentFilterPolicy pour activer ou désactiver les conseils de sécurité dans une stratégie de filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p106">Admins can use Exchange Online PowerShell to enable or disable safety tips. Use the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips in a spam filter policy.</span></span>
  
1. <span data-ttu-id="ee9ac-p107">Connexion à Exchange Online PowerShell. Pour plus d’informations, consultez la rubrique [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p107">Connect to Exchange Online PowerShell. For information, see [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="ee9ac-138">Exécutez l’applet de commande Set-HostedContentFilterPolicy pour activer ou désactiver les conseils de sécurité :</span><span class="sxs-lookup"><span data-stu-id="ee9ac-138">Run the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips:</span></span>
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

    <span data-ttu-id="ee9ac-139">Où :</span><span class="sxs-lookup"><span data-stu-id="ee9ac-139">Where:</span></span>
    
  -  <span data-ttu-id="ee9ac-140">*nom de la stratégie* est le nom de la stratégie que vous souhaitez modifier, par exemple **par défaut**.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-140">*policy name*  is the name of the policy you want to modify, for example **default**.</span></span>
    
  -  <span data-ttu-id="ee9ac-141">`$true`permet de conseils de sécurité pour la stratégie de filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-141">`$true` enables safety tips for the spam filter policy.</span></span> 
    
  -  <span data-ttu-id="ee9ac-142">`$false`désactive les conseils de sécurité pour la stratégie de filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-142">`$false` disables safety tips for the spam filter policy.</span></span> 
    
    <span data-ttu-id="ee9ac-143">Par exemple, pour désactiver les conseils de sécurité pour la stratégie de filtrage du courrier indésirable par défaut, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ee9ac-143">For example, to disable safety tips for the default spam filter policy, run the following command:</span></span>
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

    <span data-ttu-id="ee9ac-144">Pour plus d’informations sur cette applet de commande, voir [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span><span class="sxs-lookup"><span data-stu-id="ee9ac-144">For more information about this cmdlet, see [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span></span>
    
## <a name="still-need-help"></a><span data-ttu-id="ee9ac-145">Besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="ee9ac-145">Still need help?</span></span>
<span data-ttu-id="ee9ac-146"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="ee9ac-146"></span></span>

<span data-ttu-id="ee9ac-147">Si vous désactivé les conseils de sécurité, mais sont toujours les voir dans vos courriers électroniques, vérifiez ces éléments :</span><span class="sxs-lookup"><span data-stu-id="ee9ac-147">If you disabled safety tips but are still seeing them in your email messages, check these things:</span></span>
  
- <span data-ttu-id="ee9ac-p108">Vous ne pouvez pas désactiver les conseils de sécurité pour Outlook sur le web. Essayez d’afficher la même messagerie électronique dans un autre client, tel que Outlook.</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p108">You can't disable safety tips for Outlook on the web. Try viewing the same email in another client, such as Outlook.</span></span>
    
- <span data-ttu-id="ee9ac-p109">Conseils de sécurité sont activées par défaut pour chacune de celles-ci qui utilise EOP, cela inclut tous les utilisateurs Office 365. Afin de désactiver les conseils de sécurité d’apparaître dans le message électronique, vous devez les désactiver à l’aide d’une stratégie de filtrage du courrier indésirable comme décrit dans cette rubrique. Une fois que vous avez configuré la stratégie, assurez-vous qu’il est activé. Pour plus d’informations sur l’activation des stratégies de filtrage du courrier indésirable, consultez [configurer vos stratégies de filtrage du courrier indésirable](https://technet.microsoft.com/library/jj200684.aspx).</span><span class="sxs-lookup"><span data-stu-id="ee9ac-p109">Safety tips are on by default for every one who uses EOP, this includes everyone who has Office 365. In order to disable safety tips from showing up in email, you must disable them by using a spam filter policy as described in this topic. Once you've set up the policy, ensure that it is enabled. For information on enabling spam filter policies, see [Configure your spam filter policies](https://technet.microsoft.com/library/jj200684.aspx).</span></span>
    
<span data-ttu-id="ee9ac-154">Pour les autres méthodes permettent de lutter contre le courrier indésirable et l’hameçonnage, voir [Office 365 messagerie Anti-Spam Protection](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="ee9ac-154">For more ways to combat spam and phishing, see [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span></span>
  

