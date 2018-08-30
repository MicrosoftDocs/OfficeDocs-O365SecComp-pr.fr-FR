---
title: Groupe vos adresses IP pour simplifier la gestion de sécurité d’application Office 365 dans le nuage
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: b5e1471c-1ad6-4bc5-9e75-ce791aee283c
description: Pour facilement identifier les ensembles d’adresses IP que vous utiliserez dans Office 365 Cloud application sécurité, telles que vos adresses IP office physiques, vous pouvez définir des groupes de plages d’adresses IP.
ms.openlocfilehash: 76cb9625a46d1f5eceaab696de5dcbb72f4d2b47
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527523"
---
# <a name="group-your-ip-addresses-to-simplify-management-in-office-365-cloud-app-security"></a><span data-ttu-id="0b591-103">Groupe vos adresses IP pour simplifier la gestion de sécurité d’application Office 365 dans le nuage</span><span class="sxs-lookup"><span data-stu-id="0b591-103">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="0b591-104">Évaluation **\>**</span><span class="sxs-lookup"><span data-stu-id="0b591-104">****Evaluation** \>**</span></span>|<span data-ttu-id="0b591-105">Planification **\>**</span><span class="sxs-lookup"><span data-stu-id="0b591-105">****Planning** \>**</span></span>|<span data-ttu-id="0b591-106">Déploiement **\>**</span><span class="sxs-lookup"><span data-stu-id="0b591-106">****Deployment** \>**</span></span>|<span data-ttu-id="0b591-107">Utilisation du \*\*\*</span><span class="sxs-lookup"><span data-stu-id="0b591-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="0b591-108">Commencer à évaluer</span><span class="sxs-lookup"><span data-stu-id="0b591-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="0b591-109">Commencer à planifier</span><span class="sxs-lookup"><span data-stu-id="0b591-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="0b591-110">Vous êtes ici !</span><span class="sxs-lookup"><span data-stu-id="0b591-110">You are here!</span></span>  <br/> [<span data-ttu-id="0b591-111">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0b591-111">Next steps</span></span>](#next-steps) <br/> |[<span data-ttu-id="0b591-112">Commencer à utiliser</span><span class="sxs-lookup"><span data-stu-id="0b591-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="0b591-p101">Pour facilement identifier les ensembles d’adresses IP que vous utiliserez dans Office 365 Cloud application sécurité, telles que vos adresses IP office physiques, vous pouvez définir des groupes de plages d’adresses IP. Définition permet de ces plages de balise et de les classer et puis vous pouvez utiliser des balises et catégories pour personnaliser la façon dont votre activité de journaux et alertes sont affichés et examinés.</span><span class="sxs-lookup"><span data-stu-id="0b591-p101">To easily identify sets of IP addresses that you'll use in Office 365 Cloud App Security, such as your physical office IP addresses, you can set up groups of IP address ranges. Defining these ranges lets you tag and categorize them, and then you can use tags and categories to customize how your activity logs and alerts are displayed and investigated.</span></span>
  
<span data-ttu-id="0b591-p102">Chaque groupe de plages d’adresses IP permettre être marqué avec des noms de balise que vous choisissez, puis les balises peuvent être classées selon une liste par défaut des catégories IP (tels que l’entreprise, d’administration, Risky et VPN). Les adresses IPv4 et IPv6 sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0b591-p102">Each group of IP ranges can be tagged with tag names that you choose, and then the tags can be categorized based on a default list of IP categories (such as Corporate, Administrative, Risky, and VPN). Both IPv4 and IPv6 addresses are supported.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0b591-p103">Vous devez être un administrateur global ou un administrateur de sécurité pour effectuer les procédures dans cet article. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="0b591-p103">You must be a global administrator or security administrator to perform the procedures in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="to-set-up-an-ip-address-range-in-office-365-cloud-app-security"></a><span data-ttu-id="0b591-119">Pour configurer une plage d’adresses IP dans Office 365 Cloud Application Security</span><span class="sxs-lookup"><span data-stu-id="0b591-119">To set up an IP address range in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="0b591-p104">En tant qu’un administrateur global ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école. (Cela vous amène à la sécurité &amp; centre de conformité.)</span><span class="sxs-lookup"><span data-stu-id="0b591-p104">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="0b591-122">Dans la sécurité &amp; centre de conformité, sélectionnez **alertes** \> **Gestion avancée des alertes**.</span><span class="sxs-lookup"><span data-stu-id="0b591-122">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="0b591-123">Cliquez sur **Aller à la sécurité d’application Office 365 dans le nuage**.</span><span class="sxs-lookup"><span data-stu-id="0b591-123">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![Dans la sécurité &amp; centre de conformité, cliquez sur Gérer les alertes avancées pour accéder à la sécurité d’application dans le nuage Office 365](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="0b591-125">Dans l’angle supérieur droit de la page, cliquez sur **paramètres** \> **plages d’adresses IP**.</span><span class="sxs-lookup"><span data-stu-id="0b591-125">On the upper right of the page, click **Settings** \> **IP address ranges**.</span></span>
    
    ![Dans O365 Cloud application sécurité, choisissez Paramètres pour accéder à vos paramètres système et des données](media/f6c48ee3-39b4-4b5a-8252-b6493b7bcd3d.png)
  
5. <span data-ttu-id="0b591-127">Cliquez sur le bouton Nouveau, ce qui ressemble à un signe plus ( **+**).</span><span class="sxs-lookup"><span data-stu-id="0b591-127">Click the new button, which resembles a plus sign ( **+**).</span></span>
    
6. <span data-ttu-id="0b591-128">Dans la fenêtre de la **plage d’adresses IP nouveau** , spécifiez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b591-128">In the **New IP address range** window, specify the following values:</span></span> 
    
|<span data-ttu-id="0b591-129">**Champ ou une liste**</span><span class="sxs-lookup"><span data-stu-id="0b591-129">**Field or list**</span></span>|<span data-ttu-id="0b591-130">**Procédure**</span><span class="sxs-lookup"><span data-stu-id="0b591-130">**What to do**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b591-131">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0b591-131">**Name**</span></span> <br/> |<span data-ttu-id="0b591-p105">Ce champ permet de gérer votre plage d’adresses IP et les paramètres. (Vous ne verrez pas cette valeur dans les journaux d’activités).</span><span class="sxs-lookup"><span data-stu-id="0b591-p105">Use this field to manage your IP address range and settings. (You won't see this value in activities logs.)</span></span>  <br/> |
|<span data-ttu-id="0b591-134">**Plages d'adresses IP**</span><span class="sxs-lookup"><span data-stu-id="0b591-134">**IP address ranges**</span></span> <br/> |<span data-ttu-id="0b591-p106">Spécifiez une plage, en utilisant la notation de préfixe réseau (également appelé la notation CIDR). Par exemple, 192.168.1.0/27 inclut la plage de valeurs 192.168.1.0 via 192.168.1.31 (inclus).</span><span class="sxs-lookup"><span data-stu-id="0b591-p106">Specify a range, using network prefix notation (also known as CIDR notation). For example, 192.168.1.0/27 includes the range of values 192.168.1.0 through 192.168.1.31 (inclusive).</span></span>  <br/> |
|<span data-ttu-id="0b591-137">**Emplacement** et **inscrit le fournisseur de services Internet**</span><span class="sxs-lookup"><span data-stu-id="0b591-137">**Location** and **Registered ISP**</span></span> <br/> |<span data-ttu-id="0b591-p107">Pour la plage d’adresses IP, spécifiez l’emplacement et le fournisseur de services (Internet). Ce paramètre remplace les champs publics définis pour les adresses, qui est utile pour les cas, tel qu’une adresse IP est qui est considéré comme publiquement en Irlande mais est réellement aux États-Unis.</span><span class="sxs-lookup"><span data-stu-id="0b591-p107">Specify the location and Internet Service Provider (ISP) for the IP address range. This overrides the public fields defined for the addresses, which is helpful for cases, such as an IP address is that is considered publicly to be in Ireland but is actually in the U.S.</span></span>  <br/> |
|<span data-ttu-id="0b591-140">**Tags**</span><span class="sxs-lookup"><span data-stu-id="0b591-140">**Tags**</span></span> <br/> |<span data-ttu-id="0b591-p108">Utiliser des balises de nommer vos groupes d’adresses IP. (Contrairement au champ nom, vous verrez des balises aux journaux d’activité.) Tapez un mot ou expression que vous souhaitez utiliser pour une balise. Vous pouvez ajouter autant de balises que vous le souhaitez pour chaque plage d’adresses IP. Et si vous avez déjà configuré une balise et que vous souhaitez ajouter cette plage d’adresses IP, sélectionnez-le dans la liste des balises actives qui apparaissent lorsque vous commencez à taper.</span><span class="sxs-lookup"><span data-stu-id="0b591-p108">Use tags to name your groups of IP addresses. (Unlike the Name field, you will see Tags in activity logs.) Type a word or phrase that you want to use for a tag. You can add as many tags as you like for each IP address range. And if you've already set up a tag and you want to add this IP address range to it, choose it from the list of current tags that appear as you start typing.</span></span>  <br/> |
|<span data-ttu-id="0b591-145">**Catégorie**</span><span class="sxs-lookup"><span data-stu-id="0b591-145">**Category**</span></span> <br/> | <span data-ttu-id="0b591-p109">Assigner des catégories à vos balises pour faciliter l’accès à reconnaître les activités qui proviennent des adresses IP. Choisissez parmi les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b591-p109">Assign categories to your tags to make it easier to recognize activities that come from certain IP addresses. Choose from the following options:  </span></span><br/> <span data-ttu-id="0b591-148">**D’administration** Toutes les adresses IP de vos administrateurs.</span><span class="sxs-lookup"><span data-stu-id="0b591-148">**Administrative** All of the IP addresses of your admins.</span></span>  <br/> <span data-ttu-id="0b591-149">**Fournisseur de nuage** L’adresse IP de votre serveur proxy dans le nuage.</span><span class="sxs-lookup"><span data-stu-id="0b591-149">**Cloud provider** The IP address of your proxy in the cloud.</span></span>  <br/> <span data-ttu-id="0b591-150">**D’entreprise** Toutes l’adresses IP dans votre réseau interne, vos succursales et vos adresses itinérants Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="0b591-150">**Corporate** All of the IP addresses in your internal network, your branch offices, and your Wi-Fi roaming addresses.</span></span>  <br/> <span data-ttu-id="0b591-p110">**Risquée** Toutes les adresses IP que vous considérez à présenter des risques, tels que des adresses IP suspecte que vous ont indiqué dans le passé, les adresses IP dans les réseaux de vos concurrents et ainsi de suite. Par défaut, les catégories risquées inclut deux balises IP : **proxy anonyme** et **Tor**</span><span class="sxs-lookup"><span data-stu-id="0b591-p110">**Risky** Any IP addresses that you consider to be risky, such as suspicious IP addresses you've seen in the past, IP addresses in your competitors' networks, and so on. By default, the Risky categories includes two IP tags: **Anonymous proxy** and **Tor**</span></span> <br/> <span data-ttu-id="0b591-153">**Réseau privé virtuel** Toutes les adresses IP qui utilisent votre travailleurs à distance.</span><span class="sxs-lookup"><span data-stu-id="0b591-153">**VPN** Any IP addresses that your remote workers use.</span></span>  <br/> |
   
7. <span data-ttu-id="0b591-154">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="0b591-154">Choose **Save**.</span></span>
    
<span data-ttu-id="0b591-155">Après avoir configuré vos plages d’adresses IP, n’oubliez pas que les événements futurs uniquement sont affectés par ces modifications.</span><span class="sxs-lookup"><span data-stu-id="0b591-155">After you set up your IP address ranges, keep in mind that only future events are affected by these changes.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="0b591-156">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0b591-156">Next steps</span></span>

- [<span data-ttu-id="0b591-157">Alertes et des stratégies d’activité</span><span class="sxs-lookup"><span data-stu-id="0b591-157">Activity policies and alerts</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="0b591-158">Stratégies de détection des anomalies</span><span class="sxs-lookup"><span data-stu-id="0b591-158">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="0b591-159">Intégrer votre serveur SIEM</span><span class="sxs-lookup"><span data-stu-id="0b591-159">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="0b591-160">Passez en revue et effectuer une action sur les alertes de sécurité pour application Cloud Microsoft Office 365</span><span class="sxs-lookup"><span data-stu-id="0b591-160">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    

