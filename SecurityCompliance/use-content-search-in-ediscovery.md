---
title: Utilisation de la recherche de contenu dans votre flux de travail de découverte électronique
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: "Utilisez un script PowerShell pour créer une recherche de découverte électronique inaltérable dans Exchange Online, en fonction d'une recherche créée dans le centre &amp; de sécurité conformité Office 365. "
ms.openlocfilehash: 03df28094f29ced5a299aeb4f2140c3c3b0eba8c
ms.sourcegitcommit: 54a2cbe5d13f448e0c28655bdf88deb9e5434cac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2019
ms.locfileid: "30935249"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a>Utilisation de la recherche de contenu dans votre flux de travail de découverte électronique

La fonctionnalité de recherche de contenu dans le centre &amp; de sécurité et conformité Office 365 vous permet d'effectuer des recherches dans toutes les boîtes aux lettres de votre organisation. Contrairement à la découverte électronique inaltérable dans Exchange Online (où vous pouvez effectuer des recherches dans des boîtes aux lettres de 10 000), il n'existe aucune limite au nombre de boîtes aux lettres cibles dans une seule recherche. Pour les scénarios qui nécessitent d’effectuer des recherches à l’échelle de l’organisation, vous pouvez utiliser la recherche de contenu pour consulter toutes les boîtes aux lettres. Ensuite, vous pouvez utiliser les fonctionnalités de flux de travail de la découverte électronique inaltérable pour effectuer d'autres tâches relatives à la découverte électronique, telles que la conservation des boîtes aux lettres et l'exportation des résultats de la recherche. Par exemple, supposons que vous devez réaliser une recherche dans toutes les boîtes aux lettres pour identifier des responsables spécifiques impliqués dans une affaire judiciaire. Vous pouvez utiliser la recherche de contenu dans &amp; le centre de sécurité conformité pour rechercher toutes les boîtes aux lettres de votre organisation afin d'identifier celles qui répondent au cas. Vous pouvez ensuite utiliser cette liste de boîtes aux lettres de dépositaire comme boîtes aux lettres source pour une recherche de découverte électronique inaltérable dans Exchange Online. À l'aide de la découverte électronique inaltérable, vous pouvez suspendre ces boîtes aux lettres source, copier les résultats de la recherche dans une boîte aux lettres de découverte et exporter les résultats de la recherche.
  
Cette rubrique comprend un script que vous pouvez exécuter pour créer une recherche de découverte électronique inaltérable dans Exchange Online à l'aide de la liste des boîtes aux lettres source et de la requête de recherche à &amp; partir d'une recherche créée dans le centre de sécurité et de conformité. Voici une vue d’ensemble du processus :
  
[Étape 1 : créer une recherche de contenu pour consulter toutes les boîtes aux lettres de votre organisation](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[Étape 2: se connecter au centre \& de sécurité conformité et à Exchange Online en une seule session PowerShell à distance](#step-2-connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[Étape 3 : exécuter le script pour créer une recherche de découverte électronique inaltérable à partir de la recherche de contenu](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[Step 4: Start the In-Place eDiscovery search](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a>Étape 1 : créer une recherche de contenu pour consulter toutes les boîtes aux lettres de votre organisation

La première étape consiste à utiliser le centre &amp; de sécurité conformité (ou Security _AMP_ Compliance Center PowerShell) pour créer une recherche de contenu qui recherche toutes les boîtes aux lettres de votre organisation. Il n’existe aucune limite sur le nombre de boîtes aux lettres pour une recherche de contenu donnée. Spécifiez une requête de mot clé appropriée (ou une requête pour des types d’informations sensibles) afin que la recherche renvoie uniquement les boîtes aux lettres source pertinentes pour votre enquête. Si nécessaire, affinez la requête de recherche pour limiter l’étendue des résultats de recherche et des boîtes aux lettres source renvoyés.
  
> [!NOTE]
> Si la recherche de contenu source ne renvoie aucun résultat, aucune découverte électronique inaltérable n’est créée lorsque vous exécutez le script à l’étape 3. Il se peut que vous deviez modifier la requête de recherche, puis réexécuter la recherche de contenu pour renvoyer des résultats de recherche. 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a>Utiliser le centre &amp; de sécurité conformité pour rechercher toutes les boîtes aux lettres

1. [Accédez au centre de sécurité &amp; conformité d'Office 365](go-to-the-securitycompliance-center.md). 
    
2. Cliquez sur recherches de **recherche &amp; **, sur **recherche de contenu**, puis sur **nouvelle** ![icône](media/O365-MDM-CreatePolicy-AddIcon.gif)ajouter.
    
3. Sur la page **Nouvelle recherche**, saisissez un nom pour la recherche de contenu. 
    
4. Sous **Dans quels emplacements voulez-vous effectuer la recherche ?**, cliquez sur **Rechercher dans toutes les boîtes aux lettres**, puis sur **Suivant**.
    
5. Dans la zone sous **Que voulez-vous que nous recherchions ?**, entrez une requête de recherche dans la zone. Vous pouvez spécifier des mots clés, des propriétés de message telles que les dates d’envoi et de réception, ou des propriétés de document telles que les noms de fichier ou la date de dernière modification d’un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, comme AND, OR, NOT ou NEAR, ou vous pouvez également rechercher des informations sensibles (telles que les numéros de sécurité sociale) dans les messages. Pour plus d’informations sur la création de requêtes de recherche, consultez la rubrique [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).
    
6. Cliquez sur **Rechercher** pour enregistrer les paramètres de recherche et commencer la recherche. 
    
    Après un certain temps, une estimation des résultats de la recherche affichés dans le volet d'informations. L’estimation inclut la taille totale et le nombre d’éléments pour les résultats de recherche. Une fois la recherche terminée, vous pouvez prévisualiser les résultats de recherche. Si nécessaire, cliquez ****![sur Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) l'actualisation pour mettre à jour les informations dans le volet d'informations. 
    
7.  Si nécessaire, affinez la requête de recherche pour limiter l’étendue des résultats de recherche, puis redémarrez la recherche. 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a>Utiliser le centre de sécurité & Compliance Center PowerShell pour rechercher toutes les boîtes aux lettres

Vous pouvez également utiliser la cmdlet **New-ComplianceSearch** pour effectuer une recherche dans toutes les boîtes aux lettres de votre organisation. La première étape consiste à [se connecter au centre de &amp; sécurité conformité Office 365 PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).
  
Voici un exemple d'utilisation de PowerShell pour effectuer une recherche dans toutes les boîtes aux lettres de votre organisation. La requête de recherche renvoie tous les messages envoyés entre le 1er janvier 2015 et le 30 juin 2015 contenant l’expression « financial report » dans l’objet. La première commande crée la recherche et la deuxième commande l'exécute. 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

Pour plus d'informations, consultez la rubrique [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a>Vérifier le nombre de boîtes aux lettres source dans la recherche de contenu

Une recherche de contenu renvoie un maximum de 1 000 boîtes aux lettres source qui contiennent les résultats de la recherche. S'il y a plus de 1 000 boîtes aux lettres qui contiennent du contenu correspondant à la requête de recherche, seules les 1 000 premières boîtes aux lettres avec le plus de résultats de recherche sont incluses dans la recherche de contenu que vous avez créée à l'étape précédente. Par conséquent, si plus de 1 000 boîtes aux lettres contiennent des résultats de recherche, certaines de ces boîtes aux lettres ne seront pas incluses dans la liste des boîtes aux lettres source copiées dans la nouvelle recherche de découverte électronique inaltérable créée à l'étape 3. 
  
Pour vous aider à créer une recherche de contenu ne comportant pas plus de 1 000 boîtes aux lettres source, procédez comme suit pour exécuter un script qui affiche le nombre de boîtes aux lettres sources (qui contiennent les résultats de la recherche) renvoyées par la recherche de contenu que vous avez créée à l'étape 1. 
  
1. Enregistrez le texte suivant dans un fichier de script PowerShell à l'aide du suffixe de nom de fichier. ps1. Par exemple, vous pouvez l'enregistrer dans un fichier nommé `SourceMailboxes.ps1`.
    
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

2. Dans le centre de sécurité & Compliance Center PowerShell, accédez au dossier dans lequel se trouve le script que vous avez créé à l'étape précédente, puis exécutez le script. par exemple:
    
    ```
    .\SourceMailboxes.ps1
    ```

3. Lorsque vous y êtes invité par le script, entrez le nom de la recherche de contenu que vous avez créée à l’étape 1.
    
    Le script affiche le nombre de boîtes aux lettres source contenant les résultats de la recherche.
    
Si le nombre de boîtes aux lettres source est supérieur à 1 000, essayez de créer deux recherches de contenu (ou plus). Par exemple, recherchez la moitié des boîtes aux lettres de votre organisation dans la première recherche de contenu, et l’autre moitié dans la deuxième. Vous pouvez également modifier les critères de recherche afin de réduire le nombre de boîtes aux lettres contenant les résultats de recherche. Par exemple, vous pouvez inclure une plage de dates ou affiner la requête de mot-clé.
  
## <a name="step-2-connect-to-the-security--compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Étape 2: se connecter au centre \& de sécurité conformité et à Exchange Online en une seule session PowerShell à distance

L'étape suivante consiste à connecter Windows PowerShell au centre de sécurité &amp; conformité et à votre organisation Exchange Online. Cela est nécessaire, car le script que vous exécutez à l'étape 3 requiert l'accès aux cmdlets de recherche de &amp; contenu dans le centre de sécurité conformité et les cmdlets de découverte électronique inaltérable dans Exchange Online.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide du suffixe de nom de fichier .ps1. Par exemple, vous pouvez l'enregistrer dans un fichier nommé `ConnectEXO-CC.ps1`.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell, accédez au dossier dans lequel se trouve le script que vous avez créé à l'étape précédente, puis exécutez le script; par exemple:
    
    ```
    .\ConnectEXO-CC.ps1
    ```

Comment savoir si cela a fonctionné ? Après avoir exécuté le script, les cmdlets du centre &amp; de sécurité conformité et d'Exchange Online sont importées dans votre session PowerShell locale. Si vous ne recevez aucune erreur, la connexion est établie. Un test rapide consiste à exécuter une cmdlet &amp; du centre de sécurité conformité (par exemple, **install-UnifiedCompliancePrerequisite** ) et une cmdlet Exchange Online, telle que **Get-Mailbox**. 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a>Étape 3 : exécuter le script pour créer une recherche de découverte électronique inaltérable à partir de la recherche de contenu

Une fois que vous avez créé la session PowerShell double à l'étape 2, l'étape suivante consiste à exécuter un script qui convertira une recherche de contenu existante en une recherche de découverte électronique inaltérable. Voici ce que fait le script :
  
- Il vous invite à indiquer le nom de la recherche de contenu à convertir.
    
- Il vérifie que l’exécution de la recherche de contenu est terminée. Si la recherche de contenu ne renvoie aucun résultat, la découverte électronique inaltérable n’est pas créée.
    
- Il enregistre la liste des boîtes aux lettres source de la recherche de contenu comportant les résultats de recherche dans une variable.
    
- Il crée une recherche de découverte électronique inaltérable, avec les propriétés suivantes. Notez que la nouvelle recherche n’est pas démarrée. Vous le démarrerez à l’étape 4.
    
  - **Name** : le nom de la nouvelle recherche utilise ce format: \<nom de la recherche\>de contenu _MBSearch1. Si vous exécutez à nouveau le script et que vous utilisez la même recherche de contenu source, la \<recherche sera nommée nom\>de la recherche de contenu _MBSearch2.
    
  - **Boîtes aux lettres source** : toutes les boîtes aux lettres de la recherche de contenu qui contiennent les résultats de la recherche. 
    
  - **Requête de recherche** : la nouvelle recherche utilise la requête de recherche de la recherche de contenu. Si la recherche de contenu inclut l’ensemble du contenu (lorsque la requête de recherche est vide), la nouvelle recherche comporte également une requête de recherche vide et inclut tout le contenu trouvé dans les boîtes aux lettres source. 
    
  - **Estimer uniquement** la recherche: la nouvelle recherche est marquée comme une recherche d'estimation uniquement. Après le démarrage, elle ne copie pas les résultats de la recherche dans une boîte aux lettres de découverte. 
    
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l'aide du suffixe de nom de fichier .ps1. Par exemple, vous pouvez l'enregistrer dans un fichier nommé `CreateMBSearchFromComplianceSearch.ps1`.
    
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

2. Dans la session Windows PowerShell que vous avez créée à l'étape 2, accédez au dossier dans lequel se trouve le script que vous avez créé à l'étape précédente, puis exécutez le script. par exemple:
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. Lorsque vous y êtes invité par le script, tapez le nom de la recherche de contenu que vous souhaitez convertir dans une recherche de découverte électronique inaltérable (par exemple, la recherche que vous avez créée à l'étape 1), puis appuyez sur **entrée**.
    
    Si le script réussit, une recherche de découverte électronique inaltérable est créée avec l'état **NotStarted**. Exécutez la commande  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` pour afficher les propriétés de la nouvelle recherche. 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a>Étape 4 : démarrer la recherche de découverte électronique inaltérable

Le script exécuté à l'étape 3 crée une recherche de découverte électronique inaltérable, mais ne la lance pas. L'étape suivante consiste à lancer la recherche afin d'obtenir une estimation des résultats de recherche.
  
1. In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
2. Dans l'affichage Liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3.
    
3. ![Cliquez **** sur l'icône](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> recherche de recherche estimer les **résultats** de recherche pour lancer la recherche et obtenir une estimation de la taille totale et du nombre d'éléments renvoyés par la recherche. 
    
    Les estimations sont affichées dans le volet d'informations. Cliquez **** ![sur Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) l'icône Actualiser pour mettre à jour les informations affichées dans le volet d'informations. 
    
4. Pour prévisualiser les résultats une fois la recherche terminée, cliquez sur **Aperçu des résultats de recherche** dans le volet d'informations.
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a>Étapes suivantes après la création et l’exécution de la recherche de découverte électronique inaltérable

Après avoir créé et démarré la recherche de découverte électronique inaltérable créée par le script à l’étape 3, vous pouvez utiliser le flux de travail de découverte électronique inaltérable normal pour effectuer différentes actions de découverte électronique sur les résultats de recherche.
  
### <a name="create-an-in-place-hold"></a>Créer une conservation inaltérable

1. In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
2. Dans l'affichage liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3, puis **** ![cliquez sur modifier](media/O365_MDM_CreatePolicy_EditIcon.gif)l'icône modifier.
    
3. Dans la page **Conservation inaltérable**, cochez la case **Mettre en attente le contenu correspondant à la requête de recherche des boîtes aux lettres sélectionnées**, puis sélectionnez l'une des options suivantes : 
    
  - **Bloquer** indéfiniment: choisissez cette option pour placer les éléments renvoyés par la recherche sur une conservation indéfinie. Les éléments en attente seront conservés jusqu'à ce que vous supprimiez la boîte aux lettres de la recherche ou que vous supprimiez la recherche. 
    
  - **Spécifier le nombre de jours de conservation des éléments par rapport à leur date de réception** : choisissez cette option pour conserver les éléments pour une période spécifique. La durée est calculée à compter de la date de réception ou de création de l'élément de boîte aux lettres. 
    
4. Cliquez sur **Enregistrer** pour créer la conservation inaltérable et relancer la recherche. 
    
[Revenir au début](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a>Copier les résultats de recherche

1. In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
2. Dans la vue de liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3.
    
3. Cliquez **** ![sur icône](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)recherche de recherche, puis cliquez sur **copier les résultats** de la recherche dans la liste déroulante. 
    
4. Dans **Copier les résultats de recherche**, choisissez parmi les options suivantes :
    
    - **Inclure les éléments** impossibles à Rechercher: activez cette case à cocher pour inclure les éléments de boîte aux lettres qui n'ont pas pu être recherchés (par exemple, les messages avec des pièces jointes de types de fichiers qui n'ont pas pu être indexés par Exchange Search). 
    
    - **Activer** la déduplication: activez cette case à cocher pour exclure les messages en double. Une seule instance d'un message est copiée vers la boîte aux lettres de découverte. 
    
    - **Activer la journalisation complète** : activez cette case à cocher pour inclure un journal complet dans les résultats de la recherche. 
    
    - **M'envoyer un message une fois la copie terminée** : activez cette case à cocher pour recevoir une notification par courrier électronique lorsque la recherche est terminée. 
    
    - **Copier les résultats vers cette boîte aux lettres de découverte** : cliquez sur **Parcourir** pour sélectionner la boîte aux lettres de découverte dans laquelle vous souhaitez copier les résultats de la recherche. 
    
5. Cliquez sur **Copier** pour lancer le processus de copie des résultats de la recherche dans la boîte aux lettres de découverte spécifiée. 
    
6. Cliquez **** ![sur Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) l'icône Actualiser pour mettre à jour les informations sur l'état de copie affiché dans le volet d'informations. 
    
7. Une fois que la copie est terminée, cliquez sur **Ouvrir** pour ouvrir la boîte aux lettres de découverte afin d’afficher les résultats de recherche. 
  
### <a name="export-the-search-results"></a>Exporter les résultats de recherche

1. In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.
    
2. Dans l'affichage Liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3, puis cliquez sur **Exporter vers un fichier PST**.
    
3. Dans la fenêtre **Outil d'exportation au format PST de la découverte électronique**, effectuez les opérations suivantes : 
    
    - Cliquez sur **Parcourir** pour spécifier l'emplacement où vous souhaitez télécharger le fichier PST. 
    
    - Cochez la case **Activer la déduplication** pour exclure les messages en double. Une seule instance d'un message sera incluse dans le fichier PST. 
    
    - Cochez la case **Inclure les éléments impossibles à rechercher** pour inclure les éléments de boîte aux lettres qu'il n'est pas possible de rechercher (par exemple, les messages avec des pièces jointes dans des types de fichiers qu'Exchange Search ne peut pas indexer). Les éléments impossibles à rechercher sont exportés dans un fichier PST distinct. 
    
4. Cliquez sur **Démarrer** pour exporter les résultats de recherche vers un fichier PST. 
    
    Une fenêtre contenant des informations sur l'état du processus d'exportation s'affiche.
