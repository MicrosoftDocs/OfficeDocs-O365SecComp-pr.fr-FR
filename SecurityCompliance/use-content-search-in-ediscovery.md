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
# <a name="use-content-search-in-your-ediscovery-workflow"></a>Utilisation de la recherche de contenu dans votre flux de travail de découverte électronique

La fonctionnalité de recherche de contenu de sécurité Office 365 &amp; centre de conformité vous permet de rechercher toutes les boîtes aux lettres dans votre organisation. Contrairement à la découverte électronique locale dans Exchange Online (où vous pouvez rechercher jusqu'à 10 000 boîtes aux lettres), il n’existe aucune limite pour le nombre de boîtes aux lettres cible en une seule recherche. Pour les scénarios qui nécessitent que vous devez effectuer des recherches à l’échelle de l’organisation, vous pouvez utiliser la recherche de contenu pour rechercher toutes les boîtes aux lettres. Ensuite, vous pouvez utiliser les fonctionnalités de flux de travail de découverte électronique locale pour effectuer d’autres tâches liées à la découverte électronique, telles que le blocage de boîtes aux lettres mises sur et de résultats de recherche d’exportation. Par exemple, supposons que vous avez rechercher toutes les boîtes aux lettres pour identifier les dépositaires spécifiques qui réagissent à une affaire juridique. Vous pouvez utiliser la recherche de contenu de la sécurité &amp; centre de conformité pour rechercher toutes les boîtes aux lettres dans votre organisation pour identifier ceux qui sont sensible à la casse. Vous pouvez utiliser cette liste de boîtes aux lettres dépositaire en tant que les boîtes aux lettres source pour une recherche de découverte électronique locale dans Exchange Online. À l’aide de In-Place eDiscovery vous permet également à placer une suspension sur les boîtes aux lettres source, copier les résultats de recherche dans une boîte aux lettres de découverte et d’exporter les résultats de recherche.
  
Cette rubrique inclut un script que vous pouvez exécuter pour créer une recherche de découverte électronique locale dans Exchange Online à l’aide de la liste des boîtes aux lettres sources et de requête de recherche à partir d’une recherche créée dans la sécurité &amp; centre de conformité. Voici une vue d’ensemble du processus :
  
[Étape 1 : créer une recherche de contenu pour consulter toutes les boîtes aux lettres de votre organisation](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[Étape 2 : Se connecter à la sécurité &amp; centre de conformité et Exchange Online dans une seule session PowerShell distante](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[Étape 3 : exécuter le script pour créer une recherche de découverte électronique inaltérable à partir de la recherche de contenu](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[Étape 4 : démarrer la recherche de découverte électronique inaltérable](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a>Étape 1 : créer une recherche de contenu pour consulter toutes les boîtes aux lettres de votre organisation

La première étape consiste à utiliser la sécurité &amp; centre de conformité (ou sécurité & PowerShell du centre de conformité) pour créer une recherche de contenu qui recherche toutes les boîtes aux lettres dans votre organisation. Il n’existe aucune limite pour le nombre de boîtes aux lettres pour une recherche de contenu unique. Spécifiez une requête de mot clé approprié (ou une requête pour des types d’informations sensibles) afin que la recherche retourne uniquement les boîtes aux lettres sources qui sont pertinents pour votre investigation. Si nécessaire, affinez la requête de recherche pour limiter l’étendue des résultats de recherche et de boîtes aux lettres sources qui sont retournés.
  
> [!NOTE]
> Si la recherche de contenu source ne renvoie aucun résultat, aucune découverte électronique inaltérable n’est créée lorsque vous exécutez le script à l’étape 3. Il se peut que vous deviez modifier la requête de recherche, puis réexécuter la recherche de contenu pour renvoyer des résultats de recherche. 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a>Utilisez la sécurité &amp; centre de conformité pour rechercher toutes les boîtes aux lettres

1. [De la sécurité Office 365 &amp; centre de conformité](go-to-the-securitycompliance-center.md). 
    
2. Cliquez sur **recherche &amp; enquête**et cliquez sur **recherche de contenu**, puis cliquez sur **Nouveau** ![icône Ajouter](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
3. Sur la page **Nouvelle recherche**, saisissez un nom pour la recherche de contenu. 
    
4. Sous **Dans quels emplacements voulez-vous effectuer la recherche ?**, cliquez sur **Rechercher dans toutes les boîtes aux lettres**, puis sur **Suivant**.
    
5. Dans la zone sous **que voulez-vous rechercher les ?**, tapez une requête de recherche dans la zone. Vous pouvez spécifier des mots clés, message propriétés telles qu’envoyés et reçus de dates, ou des propriétés de document telles que les noms de fichiers ou la date de dernière modification un document. Vous pouvez utiliser des requêtes plus complexes qui utilisent un opérateur booléen, tels que AND, OR pas ou de proximité, ou vous pouvez également rechercher des informations sensibles (telles que les numéros de sécurité sociale) dans les messages. Pour plus d’informations sur la création de requêtes de recherche, voir [requêtes de mot clé pour la recherche de contenu](keyword-queries-and-search-conditions.md).
    
6. Cliquez sur **Rechercher** pour enregistrer les paramètres de recherche et commencer la recherche. 
    
    Après un certain temps, une estimation des résultats de recherche affichés dans le volet détails. L’estimation inclut la taille totale et le nombre d’éléments des résultats de recherche. Une fois que la recherche est terminée, vous pouvez afficher les résultats de recherche. Si nécessaire, cliquez sur **Actualiser**![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations contenues dans le volet de détails. 
    
7.  Si nécessaire, affinez la requête de recherche pour limiter l’étendue des résultats de recherche, puis redémarrez la recherche. 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a>Utiliser PowerShell du centre de conformité et sécurité pour rechercher toutes les boîtes aux lettres

Vous pouvez également utiliser l’applet de commande **New-ComplianceSearch** pour rechercher toutes les boîtes aux lettres dans votre organisation. La première étape consiste à [se connecter à Office 365 sécurité &amp; PowerShell du centre de conformité](https://go.microsoft.com/fwlink/p/?LinkID=627084).
  
Voici un exemple d’utilisation de PowerShell pour rechercher toutes les boîtes aux lettres dans votre organisation. La requête de recherche renvoie tous les messages envoyés entre le 1er janvier 2015 et le 30 juin 2015 et qui contiennent la phrase « rapports financiers » dans la ligne d’objet. La première commande crée la recherche, et la deuxième commande s’exécute à la recherche. 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

Pour plus d'informations, consultez la rubrique [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a>Vérifier le nombre de boîtes aux lettres source dans la recherche de contenu

Une recherche de contenu retourne un maximum de 1 000 boîtes aux lettres sources qui contiennent des résultats de la recherche. S’il n’y a plus de 1 000 boîtes aux lettres qui contiennent du contenu qui correspond à la requête de recherche, uniquement haut 1 000 boîtes aux lettres avec les résultats de recherche la plupart sont inclus dans la recherche de contenu que vous avez créé à l’étape précédente. Ainsi, si plus de 1 000 boîtes aux lettres contient les résultats de la recherche, certains de ces boîtes aux lettres ne sont pas inclus dans la liste des boîtes aux lettres sources copiés à la nouvelle recherche de découverte sur Place créée à l’étape 3. 
  
Pour vous aider à créer une recherche de contenu avec pas plus de boîtes aux lettres sources 1 000, suivez ces étapes pour exécuter un script qui affiche le nombre de boîtes aux lettres source (qui contient les résultats de la recherche) renvoyé par la recherche de contenu que vous avez créé à l’étape 1. 
  
1. Enregistrez le texte suivant dans un fichier de script PowerShell à l’aide d’un suffixe de nom de fichier de .ps1. Par exemple, vous pourriez enregistrer dans un fichier nommé `SourceMailboxes.ps1`.
    
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

2. Dans PowerShell de centre de conformité et de sécurité, accédez au dossier où se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :
    
    ```
    .\SourceMailboxes.ps1
    ```

3. Lorsque vous y êtes invité par le script, entrez le nom de la recherche de contenu que vous avez créée à l’étape 1.
    
    Le script affiche le nombre de boîtes aux lettres source contenant les résultats de la recherche.
    
S’il n’y a plus de 1 000 boîtes aux lettres source, essayez de créer des recherches de contenu de deux (ou plus). Par exemple, la moitié des boîtes aux lettres de votre organisation de recherche dans une recherche de contenu et l’autre moitié dans une autre recherche de contenu. Vous pouvez également modifier les critères de recherche pour réduire le nombre de boîtes aux lettres qui contiennent des résultats de la recherche. Par exemple, vous pourriez inclure une plage de dates ou d’affiner la requête de mot clé.
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a>Étape 2 : Se connecter à la sécurité &amp; centre de conformité et Exchange Online dans une seule session PowerShell distante

L’étape suivante consiste à connecter Windows PowerShell pour la sécurité &amp; centre de conformité et de votre organisation Exchange Online. Cela est nécessaire car le script que vous exécutez l’étape 3 nécessite un accès pour les applets de commande de recherche de contenu dans la sécurité &amp; centre de conformité et les applets de commande In-Place eDiscovery dans Exchange Online.
  
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de .ps1. Par exemple, vous pourriez enregistrer dans un fichier nommé `ConnectEXO-CC.ps1`.
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. Sur votre ordinateur local, ouvrez Windows PowerShell, accédez au dossier où se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :
    
    ```
    .\ConnectEXO-CC.ps1
    ```

Comment savoir si cela a fonctionné ? Après avoir exécuté le script, les applets de commande de la sécurité &amp; centre de conformité et Exchange Online sont importés dans votre session PowerShell locale. Si vous ne recevez des erreurs, vous connecté avec succès. Un test rapide consiste à exécuter une sécurité &amp; centre de conformité cmdlet — par exemple, **Install-UnifiedCompliancePrerequisite** et une applet de commande Exchange Online, telles que **Get-Mailbox**. 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a>Étape 3 : exécuter le script pour créer une recherche de découverte électronique inaltérable à partir de la recherche de contenu

Après avoir créé la session PowerShell double à l’étape 2, l’étape suivante consiste à exécuter un script qui convertit une recherche de contenu existante à une recherche de découverte électronique locale. Voici ce que fait le script :
  
- Il vous invite à indiquer le nom de la recherche de contenu à convertir.
    
- Il vérifie que l’exécution de la recherche de contenu est terminée. Si la recherche de contenu ne renvoie aucun résultat, la découverte électronique inaltérable n’est pas créée.
    
- Il enregistre la liste des boîtes aux lettres source de la recherche de contenu comportant les résultats de recherche dans une variable.
    
- Il crée une recherche de découverte électronique inaltérable, avec les propriétés suivantes. Notez que la nouvelle recherche n’est pas démarrée. Vous le démarrerez à l’étape 4.
    
  - **Nom** : le nom de la nouvelle recherche utilise ce format : \<nom de la recherche de contenu\>_MBSearch1. Si vous exécutez de nouveau le script et utilisez la même source de contenu de recherche, la recherche sera nommée \<nom de la recherche de contenu\>_MBSearch2.
    
  - **Boîtes aux lettres sources** - toutes les boîtes aux lettres à partir de la recherche de contenu qui contiennent des résultats de la recherche. 
    
  - **Requête de recherche** - la nouvelle recherche utilise la requête de recherche à partir de la recherche de contenu. Si la recherche de contenu inclut tout le contenu (où la requête de recherche est vide) la nouvelle recherche aura également une requête de recherche vide et inclut tout le contenu trouvé dans les boîtes aux lettres source. 
    
  - **Estimer la recherche uniquement** - la nouvelle recherche est marqué comme une recherche estimate uniquement. Elle ne copie des résultats de la recherche à une boîte aux lettres de découverte après le démarrage. 
    
1. Enregistrez le texte suivant dans un fichier de script Windows PowerShell à l’aide d’un suffixe de nom de fichier de ps1. Par exemple, vous pourriez enregistrer dans un fichier nommé `CreateMBSearchFromComplianceSearch.ps1`.
    
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

2. Dans la session Windows PowerShell que vous avez créé à l’étape 2, accédez au dossier où se trouve le script que vous avez créé à l’étape précédente, puis exécutez le script ; par exemple :
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. Lorsque vous y êtes invité par le script, tapez le nom de la recherche de contenu que vous souhaitez convertir en une-recherche de découverte électronique (par exemple, la recherche que vous avez créé à l’étape 1), puis appuyez sur **entrée**.
    
    Si le script réussit, une recherche de découverte électronique inaltérable est créée avec l'état **NotStarted**. Exécutez la commande  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` pour afficher les propriétés de la nouvelle recherche. 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a>Étape 4 : démarrer la recherche de découverte électronique inaltérable

Le script exécuté à l’étape 3 crée une recherche de découverte électronique inaltérable, mais ne la démarre pas. L’étape suivante consiste à démarrer la recherche afin d’obtenir une estimation des résultats de recherche.
  
1. Dans le centre d’administration Exchange (CAE), accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.
    
2. Dans l'affichage Liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3.
    
3. Cliquez sur **recherche** ![icône de recherche](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **estimation des résultats de recherche** pour lancer la recherche et de renvoyer une estimation de la taille totale et le nombre d’éléments renvoyés par la recherche. 
    
    Les estimations sont affichées dans le volet détails. Cliquez sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations affichées dans le volet de détails. 
    
4. Pour prévisualiser les résultats une fois la recherche terminée, cliquez sur **Aperçu des résultats de recherche** dans le volet d'informations.
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a>Étapes suivantes après la création et l’exécution de la recherche de découverte électronique inaltérable

Après avoir créé et démarré la recherche de découverte électronique inaltérable créée par le script à l’étape 3, vous pouvez utiliser le flux de travail de découverte électronique inaltérable normal pour effectuer différentes actions de découverte électronique sur les résultats de recherche.
  
### <a name="create-an-in-place-hold"></a>Créer une conservation inaltérable

1. Dans le CAE, accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.
    
2. Dans la liste affichée, sélectionnez la recherche de découverte électronique locale que vous avez créé à l’étape 3, puis cliquez sur **Modifier** ![icône Modifier](media/O365_MDM_CreatePolicy_EditIcon.gif).
    
3. Dans la page **Conservation inaltérable**, cochez la case **Mettre en attente le contenu correspondant à la requête de recherche des boîtes aux lettres sélectionnées**, puis sélectionnez l'une des options suivantes : 
    
  - **Maintenez la touche indéfiniment** - choisissez cette option pour placer les éléments renvoyés par la recherche sur une durée indéterminée. Éléments en attente seront conservés jusqu'à ce que vous supprimez la boîte aux lettres de la recherche ou le supprimez de la recherche. 
    
  - **Spécifiez le numéro de jours pendant lesquels conserver les éléments par rapport à leur date de réception** : sélectionnez cette option pour contenir les éléments pour une période spécifique. La durée est calculée à partir de la date d’un élément de boîte aux lettres est reçu ou créé. 
    
4. Cliquez sur **Enregistrer** pour créer la conservation inaltérable et relancer la recherche. 
    
[Return to top](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a>Copier les résultats de recherche

1. Dans le CAE, accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.
    
2. Dans la vue de liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3.
    
3. Cliquez sur **recherche** ![icône de recherche](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), puis cliquez sur **Copier les résultats de recherche** dans la liste déroulante. 
    
4. Dans **Copier les résultats de recherche**, sélectionnez l'une des options suivantes :
    
    - **Inclure les éléments impossibles à rechercher** : Activez cette case à cocher pour inclure les éléments de boîte aux lettres qui n’ont pas pu être recherchés (par exemple, les messages avec pièces jointes des types de fichiers qui n’ont pas pu être indexés par la recherche Exchange). 
    
    - **Activer la déduplication** - Activez cette case à cocher pour exclure les messages en double. Une seule instance d’un message est copiée dans la boîte aux lettres de découverte. 
    
    - **Activer la journalisation complète** - Activez cette case à cocher pour inclure un journal complet dans les résultats de recherche. 
    
    - **Envoyez-moi un courrier lorsque la copie est terminée** : Activez cette case à cocher pour obtenir une notification par courrier électronique lors de la recherche est terminée. 
    
    - **Copier les résultats de cette boîte aux lettres de découverte** - cliquez sur **Parcourir** pour sélectionner la boîte aux lettres de découverte où vous souhaitez que les résultats de recherche copiés dans. 
    
5. Cliquez sur **Copier** pour lancer le processus permettant de copier les résultats de la recherche vers la boîte aux lettres de découverte spécifiée. 
    
6. Cliquez sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour les informations sur l’état de copie est affiché dans le volet détails. 
    
7. Lorsque la copie est terminée, cliquez sur **Ouvrir** pour ouvrir la boîte aux lettres et afficher les résultats de la recherche. 
  
### <a name="export-the-search-results"></a>Exporter les résultats de recherche

1. Dans le CAE, accédez à **gestion de la conformité** \> **In-Place eDiscovery &amp; contenir**.
    
2. Dans l'affichage Liste, sélectionnez la recherche de découverte électronique inaltérable que vous avez créée à l'étape 3, puis cliquez sur **Exporter vers un fichier PST**.
    
3. Dans la fenêtre **Outil d'exportation au format PST de la découverte électronique**, effectuez les opérations suivantes : 
    
    - Cliquez sur **Parcourir** pour spécifier l'emplacement où vous souhaitez télécharger le fichier PST. 
    
    - Cochez la case **Activer la déduplication** pour exclure les messages en double. Une seule instance d'un message sera incluse dans le fichier PST. 
    
    - Cochez la case **Inclure les éléments impossibles à rechercher** pour inclure les éléments de boîte aux lettres qu'il n'est pas possible de rechercher (par exemple, les messages avec des pièces jointes dans des types de fichiers qu'Exchange Search ne peut pas indexer). Les éléments impossibles à rechercher sont exportés dans un fichier PST distinct. 
    
4. Cliquez sur **Démarrer** pour exporter les résultats de recherche vers un fichier PST. 
    
    Une fenêtre contenant des informations sur l'état du processus d'exportation s'affiche.
