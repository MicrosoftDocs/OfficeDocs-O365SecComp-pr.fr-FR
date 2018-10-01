---
title: Protéger les fichiers SharePoint Online avec Azure Information Protection
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/08/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 5b9c8e41-25d2-436d-89bb-9aecb9ec2b80
description: 'Résumé : Découvrez comment appliquer la protection Azure Information Protection pour protéger les fichiers d’un site d’équipe SharePoint Online hautement confidentiel.'
ms.openlocfilehash: 738e64784de20af46050413985fb7932000f864e
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345796"
---
# <a name="protect-sharepoint-online-files-with-azure-information-protection"></a><span data-ttu-id="c4e2d-103">Protéger les fichiers SharePoint Online avec Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="c4e2d-103">Protect SharePoint Online files with Azure Information Protection</span></span>

 <span data-ttu-id="c4e2d-104">**Résumé :** Découvrez comment appliquer la protection Azure Information Protection pour protéger les fichiers d’un site d’équipe SharePoint Online hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-104">**Summary:** Apply Azure Information Protection to protect files in a highly confidential SharePoint Online team site.</span></span>
  
<span data-ttu-id="c4e2d-p101">Suivez les étapes décrites dans cet article pour configurer Azure Information Protection afin de configurer le chiffrement et les autorisations des fichiers. Ces fichiers peuvent être ajoutés à une bibliothèque SharePoint configurée pour une protection hautement confidentielle. Sinon, ouvrez un fichier directement à partir du site et utilisez le client Azure Information Protection pour ajouter le chiffrement. La protection du chiffrement et des autorisations accompagne un fichier même lorsqu’il est téléchargé à partir du site.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p101">Use the steps in this article to configure Azure Information Protection to provide encryption and permissions for files. These files can be added to a SharePoint library configured for highly confidential protection. Or, you can open a file directly from the site and use the Azure Information Protection client to add encryption. The encryption and permissions protection travels with a file even when it is downloaded from the site.</span></span> 

<span data-ttu-id="c4e2d-p102">Cette procédure fait partie d’une solution plus globale de configuration d’une protection hautement confidentielle pour les sites SharePoint et les fichiers contenus dans ces sites. Pour plus d’informations, reportez-vous à l’article [Sécuriser des sites et des fichiers SharePoint Online](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p102">These steps are part of a larger solution for configuring highly confidential protection for SharePoint sites and the files within these sites. For more information, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span> 

<span data-ttu-id="c4e2d-111">L’utilisation d’Azure Information Protection pour les fichiers dans SharePoint Online n’est pas recommandée pour tous les clients, mais elle est proposée en option aux clients qui ont besoin de ce niveau de protection pour un sous-ensemble de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-111">Using Azure Information Protection for files in SharePoint Online is not recommended for all customers, but is an option for customers who need this level of protection for a subset of files.</span></span>

<span data-ttu-id="c4e2d-112">Voici quelques remarques importantes concernant cette solution :</span><span class="sxs-lookup"><span data-stu-id="c4e2d-112">Some important notes about this solution:</span></span>
- <span data-ttu-id="c4e2d-p103">Lorsque le chiffrement Azure Information Protection est appliqué aux fichiers stockés dans Office 365, le service ne peut pas traiter le contenu de ces fichiers. La co-création, eDiscovery, la recherche, Delve et d’autres fonctionnalités de collaboration ne fonctionnent pas. Les stratégies de protection contre la perte de données peuvent uniquement fonctionner avec les métadonnées (y compris les étiquettes Office 365), mais pas le contenu de ces fichiers (par exemple, des numéros de cartes de crédit au sein des fichiers).</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p103">When Azure Information Protection encryption is applied to files stored in Office 365, the service cannot process the contents of these files. Co-authoring, eDiscovery, search, Delve, and other collaborative features do not work. Data Loss Prevention (DLP) policies can only work with the metadata (including Office 365 labels) but not the contents of these files (such as credit card numbers within files).</span></span>
- <span data-ttu-id="c4e2d-p104">Cette solution implique qu’un utilisateur doit sélectionner une étiquette qui applique la protection à partir d’Azure Information Protection. Si vous avez besoin du chiffrement automatique et si vous souhaitez que SharePoint puisse indexer et inspecter les fichiers, pensez à utiliser les services RMS dans SharePoint Online. Lorsque vous configurez une bibliothèque SharePoint pour les services RMS, les fichiers sont chiffrés automatiquement lorsqu’ils sont téléchargés pour modification. Les services RMS SharePoint comportent des limites pouvant influencer votre décision. Pour plus d’informations, reportez-vous à l’article [Configurer la Gestion des droits relatifs à l’information (Information Rights Management, IRM) dans le Centre d’administration SharePoint](https://support.office.com/article/Set-up-Information-Rights-Management-IRM-in-SharePoint-admin-center-239CE6EB-4E81-42DB-BF86-A01362FED65C).</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p104">This solution requires a user to select a label that applies the protection from Azure Information Protection. If you require automatic encryption and the ability for SharePoint to index and inspect the files, consider using Information Rights Management (IRM) in SharePoint Online. When you configure a SharePoint library for IRM, files are automatically encrypted when they are downloaded for editing.  SharePoint IRM includes limitations that might influence your decision. For more information, see [Set up Information Rights Management (IRM) in SharePoint admin center](https://support.office.com/article/Set-up-Information-Rights-Management-IRM-in-SharePoint-admin-center-239CE6EB-4E81-42DB-BF86-A01362FED65C).</span></span>

## <a name="admin-setup"></a><span data-ttu-id="c4e2d-121">Configuration de l’administrateur</span><span class="sxs-lookup"><span data-stu-id="c4e2d-121">Admin setup</span></span>
<span data-ttu-id="c4e2d-122">Tout d’abord, suivez les instructions contenues dans [Activer Azure RMS avec le centre d’administration Office 365](https://docs.microsoft.com/information-protection/deploy-use/activate-office365) pour votre abonnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-122">First, use the instructions in [Activate Azure RMS with the Office 365 admin center](https://docs.microsoft.com/information-protection/deploy-use/activate-office365) for your Office 365 subscription.</span></span>
  
<span data-ttu-id="c4e2d-123">Ensuite, configurez Azure Information Protection avec une nouvelle sous-étiquette et une nouvelle stratégie étendue pour la protection et les autorisations de votre site d’équipe SharePoint Online hautement confidentiel.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-123">Next, configure Azure Information Protection with a new scoped policy and sub-label for protection and permissions of your highly confidential SharePoint Online team site.</span></span>
  
1. <span data-ttu-id="c4e2d-p105">Connectez-vous au portail Office 365 avec un compte disposant du rôle Administrateur de sécurité ou Administrateur d’entreprise. Pour obtenir de l’aide, consultez la rubrique [Se connecter à Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p105">Sign in to the Office 365 portal with an account that has the Security Administrator or Company Administrator role. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="c4e2d-126">Dans un nouvel onglet de votre navigateur, accédez au portail Azure ([https://portal.azure.com](https://portal.azure.com)).</span><span class="sxs-lookup"><span data-stu-id="c4e2d-126">In a separate tab of your browser, go to the Azure portal ([https://portal.azure.com](https://portal.azure.com)).</span></span>
    
3. <span data-ttu-id="c4e2d-127">Si vous configurez Azure Information Protection pour la première fois, consultez ces [instructions](https://docs.microsoft.com/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time).</span><span class="sxs-lookup"><span data-stu-id="c4e2d-127">If this is the first time you are configuring Azure Information Protection, see these [instructions](https://docs.microsoft.com/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time).</span></span>

4. <span data-ttu-id="c4e2d-128">Dans le volet Liste, cliquez sur **Tous les services**, saisissez **Informations**, puis cliquez sur **Azure Information Protection**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-128">In the list pane, click **All services**, type **information**, and then click **Azure Information Protection**.</span></span>

5. <span data-ttu-id="c4e2d-129">Cliquez sur **Étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-129">Click **Labels**.</span></span>
    
6. <span data-ttu-id="c4e2d-130">Cliquez avec le bouton droit de la souris sur l’étiquette **Hautement confidentiel**, puis sur **Ajouter une sous-étiquette**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-130">Right-click the **Highly Confidential** label, and then click **Add a sub-label**.</span></span>
    
7. <span data-ttu-id="c4e2d-131">Entrez le nom de la sous-étiquette dans**Nom** et sa description dans **Description**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-131">Type a name for the sub-label in **Name** and a description of the sub-label in **Description**.</span></span>
    
8. <span data-ttu-id="c4e2d-132">Dans**Définir les autorisations pour les documents et les e-mails contenant cette étiquette**, cliquez sur**Protéger**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-132">In **Set permissions for documents and emails containing this label**, click **Protect**.</span></span>
    
9. <span data-ttu-id="c4e2d-133">Dans la section **Protection**, cliquez sur**Azure (clé cloud)**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-133">In the **Protection** section, click **Azure (cloud key)**.</span></span>
    
10. <span data-ttu-id="c4e2d-134">Dans le panneau**Protection**, cliquez sur**Ajouter des autorisations** sous**Paramètres de protection**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-134">On the **Protection** blade, under **Protection settings**, click **Add permissions**.</span></span>
    
11. <span data-ttu-id="c4e2d-135">Dans le panneau **Ajouter des autorisations**, sous **Spécifier les utilisateurs et les groupes**, cliquez sur **+ Parcourir le répertoire**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-135">On the **Add permissions** blade, under **Specify users and groups**, click **Browse directory**.</span></span>
    
12. <span data-ttu-id="c4e2d-136">Dans le volet **Utilisateurs et groupes AAD**, sélectionnez le groupe d’accès Membres de votre site d’équipe SharePoint Online hautement sensible, puis cliquez sur **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-136">On the **AAD Users and Groups** pane, select the site members access group for your highly sensitive SharePoint Online team site, and then click **Select**.</span></span>
    
13. <span data-ttu-id="c4e2d-137">sSous **Choisir les autorisations parmi les autorisations personnalisées prédéfinies ou définies**, cliquez sur **Personnalisé**, puis sur les cases à cocher **Afficher les droits**, **Modifier le contenu**, **Enregistrer**, **Répondre** et **Répondre à tous**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-137">Under **Choose permissions from the preset or set custom**, click **Custom**, and then click the **View Rights**, **Edit Content**, **Save**, **Reply**, and **Reply all** check boxes.</span></span>
    
14. <span data-ttu-id="c4e2d-138">Cliquez deux fois sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-138">Click **OK** twice.</span></span>
    
15. <span data-ttu-id="c4e2d-139">Dans le panneau **Sous-étiquette**, cliquez sur **Enregistrer**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-139">On the **Sub-label** blade, click **Save**, and then click **OK**.</span></span>

16. <span data-ttu-id="c4e2d-140">Dans le panneau **Azure Information Protection**, cliquez sur **Stratégies > + Ajouter une nouvelle stratégie**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-140">On the **Azure Information protection** blade, click **Policies > + Add a new policy**.</span></span>
    
17. <span data-ttu-id="c4e2d-141">Saisissez le nom de la nouvelle stratégie dans**Nom de la stratégie** et une description dans**Description**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-141">Type a name for the new policy in **Policy name** and a description in **Description**.</span></span>
    
18. <span data-ttu-id="c4e2d-142">Cliquez sur **Sélectionnez les utilisateurs ou groupes devant recevoir cette stratégie > Utilisateur/Groupes**, puis sélectionnez le groupe d’accès des membres de votre site d’équipe SharePoint Online hautement sensible. </span><span class="sxs-lookup"><span data-stu-id="c4e2d-142">Click **Select which users or groups get this policy > User/Groups**, and then select the site members access group for your highly sensitive SharePoint Online team site.</span></span>
    
19. <span data-ttu-id="c4e2d-143">Cliquez sur**Sélectionner > OK**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-143">Click **Select > OK**.</span></span>

20. <span data-ttu-id="c4e2d-p106">Cliquez sur**Ajouter ou supprimer des étiquettes**. Dans le volet**Stratégie : Ajouter ou supprimer des étiquettes**, cliquez sur le nom de votre sous-étiquette puis cliquez sur**OK**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p106">Click **Add or remove labels**. In the **Policy: Add or remove labels** pane, click the name of your new sub-label, and then click **OK**.</span></span>   

21. <span data-ttu-id="c4e2d-146">Cliquez sur**Enregistrer**, puis cliquez sur**OK**.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-146">Click **Save**, and then click **OK**.</span></span>
 
## <a name="client-setup"></a><span data-ttu-id="c4e2d-147">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="c4e2d-147">Client setup</span></span>
<span data-ttu-id="c4e2d-148">Vous pouvez maintenant commencer à créer des documents et à les protéger avec Azure Information Protection et votre nouvelle étiquette.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-148">You are now ready to begin creating documents and protecting them with Azure Information Protection and your new label.</span></span>
  
<span data-ttu-id="c4e2d-p107">Vous devez [installer le client Azure Information Protection](https://docs.microsoft.com/information-protection/rms-client/install-client-app) sur votre périphérique ou votre ordinateur Windows. Vous pouvez créer un script et automatiser l’installation, ou les utilisateurs peuvent installer le client manuellement. Consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p107">You must [install the Azure Information Protection client](https://docs.microsoft.com/information-protection/rms-client/install-client-app) on your device or Windows-based computer. You can script and automate the installation, or users can install the client manually. See the following resources:</span></span>
  
- [<span data-ttu-id="c4e2d-152">Côté client d’Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="c4e2d-152">The client side of Azure Information Protection</span></span>](https://docs.microsoft.com/information-protection/rms-client/use-client)
    
- [<span data-ttu-id="c4e2d-153">Installation du client Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="c4e2d-153">Installing the Azure Information Protection client</span></span>](https://docs.microsoft.com/information-protection/rms-client/client-admin-guide)
    
- [<span data-ttu-id="c4e2d-154">Page de téléchargement de l’installation manuelle</span><span class="sxs-lookup"><span data-stu-id="c4e2d-154">Download page for manual installation</span></span>](https://www.microsoft.com/download/details.aspx?id=53018)
    
<span data-ttu-id="c4e2d-p108">Une fois l’installation effectuée, vos utilisateurs exécutent une application Office (par exemple, Microsoft Word) pour se connecter avec leur compte Office 365. Une nouvelle barre **Information Protection** permet aux utilisateurs de sélectionner la nouvelle étiquette. Assurez-vous que vos utilisateurs connaissent le site d’équipe SharePoint Online et savent quelle étiquette utiliser, afin de protéger leurs fichiers hautement confidentiels.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p108">Once installed, your users run and then sign-in from an Office application (such as Microsoft Word) with their Office 365 account. A new **Information Protection** bar allows users to select the new label. Make sure that your users know the SharePoint Online team site and which label to use, to protect their highly confidential files.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c4e2d-158">Si vous possédez plusieurs sites d’équipe SharePoint Online hautement sensibles, vous devez créer plusieurs stratégies étendues Azure Information Protection avec des sous-étiquettes et les paramètres ci-dessus. Les autorisations de chaque sous-étiquette doivent être définies pour le groupe d’accès des membres d’un site d’équipe SharePoint Online spécifique.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-158">If you have multiple highly sensitive SharePoint Online team sites, you should create multiple Azure Information Protection scoped policies with sub-labels with the above settings, with the permissions for each sub-label set to the site members access group of a specific SharePoint Online team site.</span></span> 
  
## <a name="adding-permissions-for-external-users"></a><span data-ttu-id="c4e2d-159">Ajout d’autorisations pour les utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="c4e2d-159">Adding permissions for external users</span></span>
<span data-ttu-id="c4e2d-p109">Il existe deux façons d’accorder à des utilisateurs externes un accès à des fichiers protégés par le service Azure Information Protection. Dans les deux cas, les utilisateurs externes doivent disposer d’un compte Azure AD. Si les utilisateurs externes ne sont pas membres d’une organisation qui utilise Azure AD, ils peuvent obtenir un compte Azure AD individuel via cette page d’inscription : [https://aka.ms/aip-signup](https://aka.ms/aip-signup).</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p109">There are two ways you can grant external users access to files protected with Azure Information Protection. In both cases, external users must have an Azure AD account. If external users aren't members of an organization that uses Azure AD, they can obtain an Azure AD account as an individual by using this signup page: [https://aka.ms/aip-signup](https://aka.ms/aip-signup).</span></span>

 - <span data-ttu-id="c4e2d-p110">Ajouter des utilisateurs externes à un groupe Azure AD qui est utilisé pour configurer la protection d’une étiquette. Vous devez tout d’abord ajouter le compte en tant qu’utilisateur B2B dans votre répertoire. La [mise en cache de l’appartenance au groupe par Azure Rights Management](https://docs.microsoft.com/azure/information-protection/plan-design/prepare#group-membership-caching-by-azure-information-protection) peut prendre quelques heures.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p110">Add external users to an Azure AD group that is used to configure protection for a label. You'll need to first add the account as a B2B user in your directory. It can take a couple of hours for [group memership caching by Azure Rights Management](https://docs.microsoft.com/azure/information-protection/plan-design/prepare#group-membership-caching-by-azure-information-protection).</span></span>  
 - <span data-ttu-id="c4e2d-p111">Ajouter des utilisateurs externes directement à la protection d’étiquette. Vous pouvez ajouter tous les utilisateurs d’une organisation (par exemple, Fabrikam.com), un groupe Azure AD (par exemple, un groupe financier au sein d’une organisation) ou un utilisateur individuel. Par exemple, vous pouvez ajouter une équipe externe de régulateurs à la protection d’une étiquette.</span><span class="sxs-lookup"><span data-stu-id="c4e2d-p111">Add external users directly to the label protection. You can add all users from an organization (e.g. Fabrikam.com), an Azure AD group (such as a finance group within an organization), or user. For example, you can add an external team of regulators to the protection for a label.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4e2d-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4e2d-169">See Also</span></span>

[<span data-ttu-id="c4e2d-170">Sécuriser les fichiers et sites SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c4e2d-170">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="c4e2d-171">Sécuriser les sites SharePoint Online dans un environnement de développement/test</span><span class="sxs-lookup"><span data-stu-id="c4e2d-171">Secure SharePoint Online sites in a dev/test environment</span></span>](secure-sharepoint-online-sites-in-a-dev-test-environment.md)
  
[<span data-ttu-id="c4e2d-172">Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles</span><span class="sxs-lookup"><span data-stu-id="c4e2d-172">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="c4e2d-173">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="c4e2d-173">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




