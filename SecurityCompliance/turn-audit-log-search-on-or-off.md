---
title: Activer ou désactiver la recherche dans un journal d’audit Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Vous pouvez activer la fonctionnalité de recherche du journal d’Audit de sécurité Office 365 &amp; centre de conformité. Si vous changez d’avis, vous pouvez activer if désactiver à tout moment. Lors de la recherche du journal d’Audit est désactivé, administrateurs ne peuvent pas rechercher le journal d’audit de Office 365 pour l’activité utilisateur et d’administration dans votre organisation.
ms.openlocfilehash: 4fa6ac095222addce578294813cbd22dfc50a2ab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528117"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="631ce-105">Activer ou désactiver la recherche dans un journal d’audit Office 365</span><span class="sxs-lookup"><span data-stu-id="631ce-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="631ce-p102">Vous (ou un autre administrateur) devez activer l’enregistrement d’audit avant de commencer la recherche dans le journal d’audit de Office 365. Lorsque d’audit de recherche de journal de sécurité Office 365 &amp; centre de conformité est activée, les activités d’utilisateur et d’administration à partir de votre organisation sont enregistrée dans le journal d’audit et conservées pendant 90 jours. Toutefois, votre organisation ne peut pas souhaite enregistrer et conserver les données du journal d’audit. Ou vous pouvez utiliser une application de gestion (SIEM) des informations et des événements de sécurité tiers à accéder à vos données d’audit. Dans ce cas, un administrateur global peut désactiver la recherche de journal d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="631ce-p102">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log. When audit log search in the Office 365 Security &amp; Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days. However, your organization might not want to record and retain audit log data. Or you might be using a third-party security information and event management (SIEM) application to access your auditing data. In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="631ce-111">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="631ce-111">Before you begin</span></span>

- <span data-ttu-id="631ce-p103">Vous devez être affecté le rôle journaux d’Audit dans Exchange Online à activer ou désactiver la recherche des journaux d’audit dans votre organisation Office 365. Par défaut, ce rôle est attribué aux groupes de rôle de gestion de la conformité et de gestion de l’organisation dans la page **autorisations** , dans le centre d’administration Exchange. Les administrateurs globaux dans Office 365 sont membres du groupe de rôles de gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="631ce-p103">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization. By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="631ce-p104">Les utilisateurs doivent être affectées des autorisations dans Exchange Online pour activer ou désactiver la recherche des journaux d’audit. Si vous affectez le rôle journaux d’Audit dans la page **autorisations** de sécurité des utilisateurs &amp; centre de conformité, ils ne pourront activer ou désactiver la recherche des journaux d’audit. Il s’agit de l’applet de commande sous-jacente étant une applet de commande Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="631ce-p104">Users have to be assigned permissions in Exchange Online to turn audit log search on or off. If you assign users the Audit Logs role on the **Permissions** page in the Security &amp; Compliance Center, they won't be able to turn audit log search on or off. This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="631ce-p105">Si vous désactivez la recherche des journaux d’audit dans Office 365, vous pouvez toujours utiliser l’API d’activité de gestion Office 365 pour accéder aux données d’audit pour votre organisation. Désactivation de la recherche des journaux d’audit en suivant les étapes décrites dans cet article signifie qu’aucun résultat n’est renvoyés lorsque vous recherchez dans le journal d’audit à l’aide de la sécurité &amp; centre de conformité ou lorsque vous exécutez l’applet de commande **Search-UnifiedAuditLog** dans Exchange Online PowerShell. Toutefois, si vous avez autorisé n’importe quelle application pour accéder aux données d’audit de votre organisation par le biais de l’API d’activité de gestion Office 365, ces applications continueront de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="631ce-p105">If you turn off audit log search in Office 365, you can still use the Office 365 Management Activity API to access auditing data for your organization. Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security &amp; Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell. However, if you've authorized any application to access your organization's auditing data via the Office 365 Management Activity API , those applications will continue to work.</span></span> 
    
- <span data-ttu-id="631ce-121">Pour le journal d’audit dans des instructions détaillées sur la recherche Office 365, voir [recherche dans le journal d’audit de sécurité Office 365 &amp; centre de conformité](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="631ce-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="631ce-122">Activer la recherche des journaux d’audit</span><span class="sxs-lookup"><span data-stu-id="631ce-122">Turn on audit log search</span></span>

<span data-ttu-id="631ce-p106">Vous pouvez utiliser la sécurité &amp; centre de conformité ou PowerShell pour activer la recherche des journaux d’audit dans Office 365. Cela peut prendre plusieurs heures après l’activation de la recherche du journal d’audit avant de résultats lorsque vous recherchez le journal d’audit. Vous devez être affecté le rôle journaux d’Audit dans Exchange Online pour activer la recherche des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="631ce-p106">You can use the Security &amp; Compliance Center or PowerShell to turn on audit log search in Office 365. It might take several hours after you turn on audit log search before you can return results when you search the audit log. You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="631ce-126">Utilisez la sécurité &amp; centre de conformité pour activer la recherche des journaux d’audit</span><span class="sxs-lookup"><span data-stu-id="631ce-126">Use the Security &amp; Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="631ce-127">Dans la sécurité &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche des journaux d’Audit**.</span><span class="sxs-lookup"><span data-stu-id="631ce-127">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="631ce-128">Cliquez sur **Démarrer l’enregistrement d’utilisateur et des activités d’administration**.</span><span class="sxs-lookup"><span data-stu-id="631ce-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Cliquez sur Démarrer l’enregistrement d’utilisateur et des activités d’administration pour activer l’audit](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="631ce-130">Une boîte de dialogue s’affiche indiquant qu’utilisateur et l’activité d’administration dans votre organisation seront enregistrés dans le journal d’audit d’Office 365 et disponible pour l’affichage dans un rapport.</span><span class="sxs-lookup"><span data-stu-id="631ce-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="631ce-131">Cliquez sur **Activer**.</span><span class="sxs-lookup"><span data-stu-id="631ce-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="631ce-132">Un message s’affiche indiquant que le journal d’audit est préparé et que vous pouvez exécuter une recherche en quelques heures après que la préparation est terminée.</span><span class="sxs-lookup"><span data-stu-id="631ce-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="631ce-133">Utilisation de PowerShell pour activer la recherche des journaux d’audit</span><span class="sxs-lookup"><span data-stu-id="631ce-133">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="631ce-134">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="631ce-134">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="631ce-135">Exécutez la commande PowerShell suivante pour activer la recherche des journaux d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="631ce-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="631ce-136">Un message s’affiche indiquant qu’il peut prendre jusqu'à 60 minutes pour que les modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="631ce-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="631ce-137">Désactiver la recherche du journal d’audit</span><span class="sxs-lookup"><span data-stu-id="631ce-137">Turn off audit log search</span></span>

<span data-ttu-id="631ce-p107">Vous devez utiliser PowerShell distant connecté à votre organisation Exchange Online pour désactiver la recherche des journaux d’audit. Similaire à l’activation de la recherche des journaux d’audit, vous devez être affecté le rôle journaux d’Audit dans Exchange Online pour désactiver la recherche des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="631ce-p107">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search. Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="631ce-140">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="631ce-140">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="631ce-141">Exécutez la commande PowerShell suivante pour désactiver la recherche des journaux d’audit dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="631ce-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="631ce-p108">Après un certain temps, vérifiez que recherche des journaux d’audit est activée (désactivé). Il existe deux façons de procéder :</span><span class="sxs-lookup"><span data-stu-id="631ce-p108">After a while, verify that audit log search is turned off (disabled). There are two ways to do this:</span></span>
    
    - <span data-ttu-id="631ce-144">Dans PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="631ce-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="631ce-145">La valeur de `False` pour _UnifiedAuditLogIngestionEnabled_ propriété indique que recherche des journaux d’audit est désactivée.</span><span class="sxs-lookup"><span data-stu-id="631ce-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="631ce-146">Dans la sécurité &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche des journaux d’Audit**, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="631ce-146">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="631ce-147">Un message s’affiche indiquant que recherche des journaux d’audit n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="631ce-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![Un message est dispayed si l’audit est désactivé](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
