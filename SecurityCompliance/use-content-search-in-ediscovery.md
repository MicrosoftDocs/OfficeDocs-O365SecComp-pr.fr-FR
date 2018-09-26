---
title: Utilisation de la recherche de contenu dans votre flux de travail de découverte électronique
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'Utiliser un script PowerShell pour créer une recherche de découverte électronique locale dans Exchange Online basée sur une recherche créée dans l’Office 365 Security &amp; centre de conformité. '
ms.openlocfilehash: 42af94ce850736dede52e619c240bb9e0a6f7031
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038067"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="12603-103">Utilisation de la recherche de contenu dans votre flux de travail de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="12603-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="12603-p101">La fonctionnalité de recherche de contenu de sécurité Office 365 &amp; centre de conformité vous permet de rechercher toutes les boîtes aux lettres dans votre organisation. Contrairement à la découverte électronique locale dans Exchange Online (où vous pouvez rechercher jusqu'à 10 000 boîtes aux lettres), il n’existe aucune limite pour le nombre de boîtes aux lettres cible en une seule recherche. Pour les scénarios qui nécessitent que vous devez effectuer des recherches à l’échelle de l’organisation, vous pouvez utiliser la recherche de contenu pour rechercher toutes les boîtes aux lettres. Ensuite, vous pouvez utiliser les fonctionnalités de flux de travail de découverte électronique locale pour effectuer d’autres tâches liées à la découverte électronique, telles que le blocage de boîtes aux lettres mises sur et de résultats de recherche d’exportation. Par exemple, supposons que vous avez rechercher toutes les boîtes aux lettres pour identifier les dépositaires spécifiques qui réagissent à une affaire juridique. Vous pouvez utiliser la recherche de contenu de la sécurité &amp; centre de conformité pour rechercher toutes les boîtes aux lettres dans votre organisation pour identifier ceux qui sont sensible à la casse. Vous pouvez utiliser cette liste de boîtes aux lettres dépositaire en tant que les boîtes aux lettres source pour une recherche de découverte électronique locale dans Exchange Online. À l’aide de In-Place eDiscovery vous permet également à placer une suspension sur les boîtes aux lettres source, copier les résultats de recherche dans une boîte aux lettres de découverte et d’exporter les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-p101">The Content Search feature in the Office 365 Security &amp; Compliance Center allows you to search all mailboxes in your organization. Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search. For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes. Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results. For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case. You can use Content Search in the Security &amp; Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case. Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online. Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="12603-p102">Cette rubrique inclut un script que vous pouvez exécuter pour créer une recherche de découverte électronique locale dans Exchange Online à l’aide de la liste des boîtes aux lettres sources et de requête de recherche à partir d’une recherche créée dans la sécurité &amp; centre de conformité. Voici une vue d’ensemble du processus :</span><span class="sxs-lookup"><span data-stu-id="12603-p102">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security &amp; Compliance Center. Here's an overview of the process:</span></span>
  
[<span data-ttu-id="12603-114">Étape 1 : créer une recherche de contenu pour consulter toutes les boîtes aux lettres de votre organisation</span><span class="sxs-lookup"><span data-stu-id="12603-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="12603-115">Étape 2 : Se connecter à la sécurité &amp; centre de conformité et Exchange Online dans une seule session PowerShell distante</span><span class="sxs-lookup"><span data-stu-id="12603-115">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="12603-116">Étape 3 : exécuter le script pour créer une recherche de découverte électronique inaltérable à partir de la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="12603-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="12603-117">Étape 4 : démarrer la recherche de découverte électronique inaltérable</span><span class="sxs-lookup"><span data-stu-id="12603-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="12603-118">Étape 1 : créer une recherche de contenu pour consulter toutes les boîtes aux lettres de votre organisation</span><span class="sxs-lookup"><span data-stu-id="12603-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="12603-p103">La première étape consiste à utiliser la sécurité &amp; centre de conformité (ou sécurité & PowerShell du centre de conformité) pour créer une recherche de contenu qui recherche toutes les boîtes aux lettres dans votre organisation. Il n’existe aucune limite pour le nombre de boîtes aux lettres pour une recherche de contenu unique. Spécifiez une requête de mot clé approprié (ou une requête pour des types d’informations sensibles) afin que la recherche retourne uniquement les boîtes aux lettres sources qui sont pertinents pour votre investigation. Si nécessaire, affinez la requête de recherche pour limiter l’étendue des résultats de recherche et de boîtes aux lettres sources qui sont retournés.</span><span class="sxs-lookup"><span data-stu-id="12603-p103">The first step is to use the Security &amp; Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization. There's no limit for the number of mailboxes for a single Content Search. Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation. If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="12603-p104">Si la recherche de contenu source ne renvoie aucun résultat, aucune découverte électronique inaltérable n’est créée lorsque vous exécutez le script à l’étape 3. Il se peut que vous deviez modifier la requête de recherche, puis réexécuter la recherche de contenu pour renvoyer des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-p104">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3. You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="12603-125">Utilisez la sécurité &amp; centre de conformité pour rechercher toutes les boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="12603-125">Use the Security &amp; Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="12603-126">[De la sécurité Office 365 &amp; centre de conformité](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="12603-126">[Go to the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="12603-127">Cliquez sur **recherche &amp; enquête**et cliquez sur **recherche de contenu**, puis cliquez sur **Nouveau** ![icône Ajouter](media/O365-MDM-CreatePolicy-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="12603-127">Click **Search &amp; investigation**, click **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="12603-128">Sur la page **Nouvelle recherche**, saisissez un nom pour la recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="12603-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="12603-129">Sous **Dans quels emplacements voulez-vous effectuer la recherche ?**, cliquez sur **Rechercher dans toutes les boîtes aux lettres**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="12603-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="12603-p105">Dans la zone sous **que voulez-vous rechercher les ?**, tapez une requête de recherche dans la zone. Vous pouvez spécifier des mots clés, message propriétés telles qu’envoyés et reçus de dates, ou des propriétés de document telles que les noms de fichiers ou la date de dernière modification un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que AND, OR pas ou de proximité, ou vous pouvez également rechercher des informations sensibles (telles que les numéros de sécurité sociale) dans les messages. Pour plus d’informations sur la création de requêtes de recherche, voir [requêtes de mot clé pour la recherche de contenu](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="12603-p105">In the box under **What do you want us to look for?**, type a search query in the box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages. For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="12603-134">Cliquez sur **Rechercher** pour enregistrer les paramètres de recherche et commencer la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="12603-p106">Après un certain temps, une estimation des résultats de recherche affichés dans le volet détails. L’estimation inclut la taille totale et le nombre d’éléments des résultats de recherche. Une fois que la recherche est terminée, vous pouvez afficher les résultats de recherche. Si nécessaire, cliquez sur **Actualiser**![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations contenues dans le volet de détails.</span><span class="sxs-lookup"><span data-stu-id="12603-p106">After a while, an estimate of the search results displayed in the details pane. The estimate includes the total size and number of items for the search results. After the search is completed, you can preview the search results. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="12603-139">Si nécessaire, affinez la requête de recherche pour limiter l’étendue des résultats de recherche, puis redémarrez la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="12603-140">Utiliser PowerShell du centre de conformité et sécurité pour rechercher toutes les boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="12603-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="12603-p107">Vous pouvez également utiliser l’applet de commande **New-ComplianceSearch** pour rechercher toutes les boîtes aux lettres dans votre organisation. La première étape consiste à [se connecter à Office 365 sécurité &amp; PowerShell du centre de conformité](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span><span class="sxs-lookup"><span data-stu-id="12603-p107">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization. The first step is to [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="12603-p108">Voici un exemple d’utilisation de PowerShell pour rechercher toutes les boîtes aux lettres dans votre organisation. La requête de recherche renvoie tous les messages envoyés entre le 1er janvier 2015 et le 30 juin 2015 et qui contiennent la phrase « rapports financiers » dans la ligne d’objet. La première commande crée la recherche, et la deuxième commande s’exécute à la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-p108">Here's an example of using PowerShell to search all mailboxes in your organization. The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line. The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="12603-146">Pour plus d'informations, consultez la rubrique [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span><span class="sxs-lookup"><span data-stu-id="12603-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="12603-147">Vérifier le nombre de boîtes aux lettres source dans la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="12603-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="12603-p109">Une recherche de contenu retourne un maximum de 1 000 boîtes aux lettres sources qui contiennent des résultats de la recherche. S’il n’y a plus de 1 000 boîtes aux lettres qui contiennent du contenu qui correspond à la requête de recherche, uniquement haut 1 000 boîtes aux lettres avec les résultats de recherche la plupart sont inclus dans la recherche de contenu que vous avez créé à l’étape précédente. Ainsi, si plus de 1 000 boîtes aux lettres contient les résultats de la recherche, certains de ces boîtes aux lettres ne sont pas inclus dans la liste des boîtes aux lettres sources copiés à la nouvelle recherche de découverte sur Place créée à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="12603-p109">A Content Search returns a maximum of 1,000 source mailboxes that contain search results. If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step. So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="12603-151">Pour vous aider à créer une recherche de contenu avec pas plus de boîtes aux lettres sources 1 000, suivez ces étapes pour exécuter un script qui affiche le nombre de boîtes aux lettres source (qui contient les résultats de la recherche) renvoyé par la recherche de contenu que vous avez créé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="12603-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="12603-p110">Enregistrez le texte suivant dans un fichier de script PowerShell à l’aide d’un suffixe de nom de fichier de .ps1. Par exemple, vous pourriez enregistrer dans un fichier nommé `SourceMailboxes.ps1`.</span><span class="sxs-lookup"><span data-stu-id="12603-p110">Save the following text to a PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
                  "Please wait until the search finishes.";
                  break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
                  "The Content Search " + $SearchName + " didn't return any useful results.";
                  break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  "Number of mailboxes that have search hits: " + $mailboxes.Count
  ```

2. <span data-ttu-id="12603-154">Dans PowerShell de centre de conformité et de sécurité, accédez au dossier où se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="12603-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="12603-155">Lorsque vous y êtes invité par le script, entrez le nom de la recherche de contenu que vous avez créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="12603-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="12603-156">Le script affiche le nombre de boîtes aux lettres source contenant les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="12603-p111">S’il n’y a plus de 1 000 boîtes aux lettres source, essayez de créer des recherches de contenu de deux (ou plus). Par exemple, la moitié des boîtes aux lettres de votre organisation de recherche dans une recherche de contenu et l’autre moitié dans une autre recherche de contenu. Vous pouvez également modifier les critères de recherche pour réduire le nombre de boîtes aux lettres qui contiennent des résultats de la recherche. Par exemple, vous pourriez inclure une plage de dates ou d’affiner la requête de mot clé.</span><span class="sxs-lookup"><span data-stu-id="12603-p111">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches. For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search. You could also change the search criteria to reduce the number of mailboxes that contain search results. For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="12603-161">Étape 2 : Se connecter à la sécurité &amp; centre de conformité et Exchange Online dans une seule session PowerShell distante</span><span class="sxs-lookup"><span data-stu-id="12603-161">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="12603-p112">L’étape suivante consiste à connecter Windows PowerShell pour la sécurité &amp; centre de conformité et de votre organisation Exchange Online. Cela est nécessaire car le script que vous exécutez l’étape 3 nécessite un accès pour les applets de commande de recherche de contenu dans la sécurité &amp; centre de conformité et les applets de commande In-Place eDiscovery dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="12603-p112">The next step is to connect Windows PowerShell to both the Security &amp; Compliance Center and to your Exchange Online organization. This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security &amp; Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="12603-p113">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1. Par exemple, vous pourriez enregistrer dans un fichier nommé `ConnectEXO-CC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="12603-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="12603-166">Sur votre ordinateur local, ouvrez Windows PowerShell, accédez au dossier où se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="12603-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="12603-p114">Comment savoir si cela a fonctionné ? Après avoir exécuté le script, les applets de commande de la sécurité &amp; centre de conformité et Exchange Online sont importés dans votre session PowerShell locale. Si vous ne recevez des erreurs, vous connecté avec succès. Un test rapide consiste à exécuter une sécurité &amp; centre de conformité cmdlet — par exemple, **Install-UnifiedCompliancePrerequisite** et une applet de commande Exchange Online, telles que **Get-Mailbox**.</span><span class="sxs-lookup"><span data-stu-id="12603-p114">How do you know if this worked? After you run the script, cmdlets from the Security &amp; Compliance Center and Exchange Online are imported into your local PowerShell session. If you don't receive any errors, you connected successfully. A quick test is to run a Security &amp; Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="12603-171">Étape 3 : exécuter le script pour créer une recherche de découverte électronique inaltérable à partir de la recherche de contenu</span><span class="sxs-lookup"><span data-stu-id="12603-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="12603-p115">Après avoir créé la session PowerShell double à l’étape 2, l’étape suivante consiste à exécuter un script qui convertit une recherche de contenu existante à une recherche de découverte électronique locale. Voici ce que fait le script :</span><span class="sxs-lookup"><span data-stu-id="12603-p115">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search. Here's what the script does:</span></span>
  
- <span data-ttu-id="12603-174">Il vous invite à indiquer le nom de la recherche de contenu à convertir.</span><span class="sxs-lookup"><span data-stu-id="12603-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="12603-p116">Il vérifie que l’exécution de la recherche de contenu est terminée. Si la recherche de contenu ne renvoie aucun résultat, la découverte électronique inaltérable n’est pas créée.</span><span class="sxs-lookup"><span data-stu-id="12603-p116">Verifies that the Content Search has completed running. If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="12603-177">Il enregistre la liste des boîtes aux lettres source de la recherche de contenu comportant les résultats de recherche dans une variable.</span><span class="sxs-lookup"><span data-stu-id="12603-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="12603-p117">Il crée une recherche de découverte électronique inaltérable, avec les propriétés suivantes. Notez que la nouvelle recherche n’est pas démarrée. Vous le démarrerez à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="12603-p117">Creates a new In-Place eDiscovery search, with the following properties. Note that the new search isn't started. You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="12603-p118">**Nom** : le nom de la nouvelle recherche utilise ce format : \<nom de la recherche de contenu\>_MBSearch1. Si vous exécutez de nouveau le script et utilisez la même source de contenu de recherche, la recherche sera nommée \<nom de la recherche de contenu\>_MBSearch2.</span><span class="sxs-lookup"><span data-stu-id="12603-p118">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1. If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="12603-183">**Boîtes aux lettres sources** - toutes les boîtes aux lettres à partir de la recherche de contenu qui contiennent des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="12603-p119">**Requête de recherche** - la nouvelle recherche utilise la requête de recherche à partir de la recherche de contenu. Si la recherche de contenu inclut tout le contenu (où la requête de recherche est vide) la nouvelle recherche aura également une requête de recherche vide et inclut tout le contenu trouvé dans les boîtes aux lettres source.</span><span class="sxs-lookup"><span data-stu-id="12603-p119">**Search query** - The new search uses the search query from the Content Search. If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="12603-p120">**Estimer la recherche uniquement** - la nouvelle recherche est marqué comme une recherche estimate uniquement. Elle ne copie des résultats de la recherche à une boîte aux lettres de découverte après le démarrage.</span><span class="sxs-lookup"><span data-stu-id="12603-p120">**Estimate only search** - The new search is marked as an estimate-only search. It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="12603-p121">Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de ps1. Par exemple, vous pourriez enregistrer dans un fichier nommé `CreateMBSearchFromComplianceSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="12603-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1. For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName,
      [switch]$original,
      [switch]$restoreOriginal
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
    "Please wait until the search finishes";
    break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
    "The Content Search " + $SearchName + " didn't return any useful results";
    "A mailbox search object wasn't created";
    break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  $msPrefix = $SearchName + "_MBSearch";
  $I = 1;
  $mbSearches = Get-MailboxSearch;
  while ($true)
  {
      $found = $false;
      $mbsName = "$msPrefix$I";
      foreach ($mbs in $mbSearches)
      {
          if ($mbs.Name -eq $mbsName)
          {
              $found = $true;
              break;
          }
      }
      if (!$found)
      {
          break;
      }
      $I++;
  }
  $query = $search.KeywordQuery;
  if ([string]::IsNullOrWhiteSpace($query))
  {
      $query = $search.ContentMatchQuery;
  }
  if ([string]::IsNullOrWhiteSpace($query))
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -EstimateOnly;
  }
  else
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -SearchQuery $query -EstimateOnly;
  }
  
  ```

2. <span data-ttu-id="12603-190">Dans la session Windows PowerShell que vous avez créé à l’étape 2, accédez au dossier où se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="12603-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="12603-191">Lorsque vous y êtes invité par le script, tapez le nom de la recherche de contenu que vous souhaitez convertir en une-recherche de découverte électronique (par exemple, la recherche que vous avez créé à l’étape 1), puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="12603-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="12603-p122">Si le script réussit, une recherche de découverte électronique inaltérable est créée avec l'état **NotStarted**. Exécutez la commande  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` pour afficher les propriétés de la nouvelle recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-p122">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**. Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="12603-194">Étape 4 : démarrer la recherche de découverte électronique inaltérable</span><span class="sxs-lookup"><span data-stu-id="12603-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="12603-p123">Le script exécuté à l’étape 3 crée une recherche de découverte électronique inaltérable, mais ne la démarre pas. L’étape suivante consiste à démarrer la recherche afin d’obtenir une estimation des résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-p123">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it. The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="12603-197">Dans le centre d’administration Exchange (CAE), accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.</span><span class="sxs-lookup"><span data-stu-id="12603-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="12603-198">Dans l'affichage Liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3.</span><span class="sxs-lookup"><span data-stu-id="12603-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="12603-199">Cliquez sur **recherche** ![icône de recherche](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **estimation des résultats de recherche** pour lancer la recherche et de renvoyer une estimation de la taille totale et le nombre d’éléments renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="12603-p124">Les estimations sont affichées dans le volet détails. Cliquez sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations affichées dans le volet de détails.</span><span class="sxs-lookup"><span data-stu-id="12603-p124">The estimates are displayed in the details pane. Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="12603-202">Pour prévisualiser les résultats une fois la recherche terminée, cliquez sur **Aperçu des résultats de recherche** dans le volet d'informations.</span><span class="sxs-lookup"><span data-stu-id="12603-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="12603-203">Étapes suivantes après la création et l’exécution de la recherche de découverte électronique inaltérable</span><span class="sxs-lookup"><span data-stu-id="12603-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="12603-204">Après avoir créé et démarré la recherche de découverte électronique inaltérable créée par le script à l’étape 3, vous pouvez utiliser le flux de travail de découverte électronique inaltérable normal pour effectuer différentes actions de découverte électronique sur les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="12603-205">Créer une conservation inaltérable</span><span class="sxs-lookup"><span data-stu-id="12603-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="12603-206">Dans le CAE, accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.</span><span class="sxs-lookup"><span data-stu-id="12603-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="12603-207">Dans la liste affichée, sélectionnez la recherche de découverte électronique locale que vous avez créé à l’étape 3, puis cliquez sur **Modifier** ![icône Modifier](media/O365_MDM_CreatePolicy_EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="12603-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="12603-208">Dans la page **Conservation inaltérable**, cochez la case **Mettre en attente le contenu correspondant à la requête de recherche des boîtes aux lettres sélectionnées**, puis sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="12603-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="12603-p125">**Maintenez la touche indéfiniment** - choisissez cette option pour placer les éléments renvoyés par la recherche sur une durée indéterminée. Éléments en attente seront conservés jusqu'à ce que vous supprimez la boîte aux lettres de la recherche ou le supprimez de la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-p125">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold. Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="12603-p126">**Spécifiez le numéro de jours pendant lesquels conserver les éléments par rapport à leur date de réception** : sélectionnez cette option pour contenir les éléments pour une période spécifique. La durée est calculée à partir de la date d’un élément de boîte aux lettres est reçu ou créé.</span><span class="sxs-lookup"><span data-stu-id="12603-p126">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period. The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="12603-213">Cliquez sur **Enregistrer** pour créer la conservation inaltérable et relancer la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="12603-214">Return to top</span><span class="sxs-lookup"><span data-stu-id="12603-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="12603-215">Copier les résultats de recherche</span><span class="sxs-lookup"><span data-stu-id="12603-215">Copy the search results</span></span>

1. <span data-ttu-id="12603-216">Dans le CAE, accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.</span><span class="sxs-lookup"><span data-stu-id="12603-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="12603-217">Dans la vue de liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3.</span><span class="sxs-lookup"><span data-stu-id="12603-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="12603-218">Cliquez sur **recherche** ![icône de recherche](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), puis cliquez sur **Copier les résultats de recherche** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="12603-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="12603-219">Dans **Copier les résultats de recherche**, sélectionnez l'une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="12603-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="12603-220">**Inclure les éléments impossibles à rechercher** : Activez cette case à cocher pour inclure les éléments de boîte aux lettres qui n’ont pas pu être recherchés (par exemple, les messages avec pièces jointes des types de fichiers qui n’ont pas pu être indexés par la recherche Exchange).</span><span class="sxs-lookup"><span data-stu-id="12603-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="12603-p127">**Activer la déduplication** - Activez cette case à cocher pour exclure les messages en double. Une seule instance d’un message est copiée dans la boîte aux lettres de découverte.</span><span class="sxs-lookup"><span data-stu-id="12603-p127">**Enable de-duplication** - Select this check box to exclude duplicate messages. Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="12603-223">**Activer la journalisation complète** - Activez cette case à cocher pour inclure un journal complet dans les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="12603-224">**Envoyez-moi un courrier lorsque la copie est terminée** : Activez cette case à cocher pour obtenir une notification par courrier électronique lors de la recherche est terminée.</span><span class="sxs-lookup"><span data-stu-id="12603-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="12603-225">**Copier les résultats de cette boîte aux lettres de découverte** - cliquez sur **Parcourir** pour sélectionner la boîte aux lettres de découverte où vous souhaitez que les résultats de recherche copiés dans.</span><span class="sxs-lookup"><span data-stu-id="12603-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="12603-226">Cliquez sur **Copier** pour lancer le processus permettant de copier les résultats de la recherche vers la boîte aux lettres de découverte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="12603-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="12603-227">Cliquez sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations sur l’état de copie est affiché dans le volet détails.</span><span class="sxs-lookup"><span data-stu-id="12603-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="12603-228">Lorsque la copie est terminée, cliquez sur **Ouvrir** pour ouvrir la boîte aux lettres et afficher les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="12603-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="12603-229">Exporter les résultats de recherche</span><span class="sxs-lookup"><span data-stu-id="12603-229">Export the search results</span></span>

1. <span data-ttu-id="12603-230">Dans le CAE, accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.</span><span class="sxs-lookup"><span data-stu-id="12603-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="12603-231">Dans l'affichage Liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3, puis cliquez sur **Exporter vers un fichier PST**.</span><span class="sxs-lookup"><span data-stu-id="12603-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="12603-232">Dans la fenêtre **Outil d'exportation au format PST de la découverte électronique**, effectuez les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="12603-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="12603-233">Cliquez sur **Parcourir** pour spécifier l'emplacement où vous souhaitez télécharger le fichier PST.</span><span class="sxs-lookup"><span data-stu-id="12603-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="12603-p128">Cochez la case **Activer la déduplication** pour exclure les messages en double. Une seule instance d'un message sera incluse dans le fichier PST.</span><span class="sxs-lookup"><span data-stu-id="12603-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="12603-p129">Cochez la case **Inclure les éléments impossibles à rechercher** pour inclure les éléments de boîte aux lettres qu'il n'est pas possible de rechercher (par exemple, les messages avec des pièces jointes dans des types de fichiers qu'Exchange Search ne peut pas indexer). Les éléments impossibles à rechercher sont exportés dans un fichier PST distinct.</span><span class="sxs-lookup"><span data-stu-id="12603-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="12603-238">Cliquez sur **Démarrer** pour exporter les résultats de recherche vers un fichier PST.</span><span class="sxs-lookup"><span data-stu-id="12603-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="12603-239">Une fenêtre contenant des informations sur l'état du processus d'exportation s'affiche.</span><span class="sxs-lookup"><span data-stu-id="12603-239">A window is displayed that contains status information about the export process.</span></span>
