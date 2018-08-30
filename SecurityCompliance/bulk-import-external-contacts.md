---
title: Importation en bloc des contacts externes à Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: End User
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: Découvrez comment les administrateurs peuvent utiliser Exchange Online PowerShell et un fichier CSV en bloc importer des contacts externes à la liste d’adresses globale.
ms.openlocfilehash: 4bde56d49ccf94dc91993df90e1ae693e25c961a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527590"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a><span data-ttu-id="2c2fa-103">Importation en bloc des contacts externes à Exchange Online</span><span class="sxs-lookup"><span data-stu-id="2c2fa-103">Bulk import external contacts to Exchange Online</span></span>

<span data-ttu-id="2c2fa-104">**Cet article est destiné aux administrateurs. Vous essayez d’importer des contacts à votre propre boîte aux lettres ? Voir [Importer des contacts dans Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span><span class="sxs-lookup"><span data-stu-id="2c2fa-104">**This article is for administrators. Are you trying to import contacts to your own mailbox? See [Import contacts to Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span></span>
   
<span data-ttu-id="2c2fa-p101">Votre entreprise a-t-elle beaucoup de contacts professionnels existante que vous souhaitez inclure dans le carnet d’adresses partagé (également appelée la liste d’adresses globale) dans Exchange Online ? Vous souhaitez ajouter des contacts externes en tant que membres des groupes de distribution, tout comme vous pouvez avec des utilisateurs au sein de votre entreprise ? Si ce cas, vous pouvez utiliser Exchange Online PowerShell et un fichier CSV (valeurs séparées par des virgules) en bloc importer des contacts externes dans Exchange Online. Il est un processus en trois étapes :</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p101">Does your company have lots of existing business contacts that you want to include in the shared address book (also called the global address list) in Exchange Online? Do you want to add external contacts as members of distribution groups, just like you can with users inside your company? If so, you can use Exchange Online PowerShell and a CSV (Comma Separated Value) file to bulk import external contacts into Exchange Online. It's a three-step process:</span></span>
  
[<span data-ttu-id="2c2fa-109">Étape 1 : Créer un fichier CSV qui contient des informations sur les contacts externes</span><span class="sxs-lookup"><span data-stu-id="2c2fa-109">Step 1: Create a CSV file that contains information about the external contacts</span></span>](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[<span data-ttu-id="2c2fa-110">Étape 2 : Créer des contacts externes avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c2fa-110">Step 2: Create the external contacts with PowerShell</span></span>](#step-2-create-the-external-contacts-with-powershell) 

[<span data-ttu-id="2c2fa-111">Étape 3 : Ajouter des informations sur les propriétés des contacts externes</span><span class="sxs-lookup"><span data-stu-id="2c2fa-111">Step 3: Add information to the properties of the external contacts</span></span>](#step-3-add-information-to-the-properties-of-the-external-contacts)

<span data-ttu-id="2c2fa-112">Après avoir effectué ces étapes pour importer des contacts, vous pouvez effectuer ces tâches supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="2c2fa-112">After you complete these steps to import contacts, you can perform these additional tasks:</span></span>
  
- [<span data-ttu-id="2c2fa-113">Ajouter des contacts externes plus</span><span class="sxs-lookup"><span data-stu-id="2c2fa-113">Add more external contacts</span></span>](bulk-import-external-contacts.md#AddMore)
  
- [<span data-ttu-id="2c2fa-114">Masquer les contacts externes à partir du carnet d’adresses partagé</span><span class="sxs-lookup"><span data-stu-id="2c2fa-114">Hide external contacts from the shared address book</span></span>](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a><span data-ttu-id="2c2fa-115">Étape 1 : Créer un fichier CSV qui contient des informations sur les contacts externes</span><span class="sxs-lookup"><span data-stu-id="2c2fa-115">Step 1: Create a CSV file that contains information about the external contacts</span></span>

<span data-ttu-id="2c2fa-116">La première étape consiste à créer un fichier CSV qui contient des informations sur chaque contact externe que vous souhaitez importer vers Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-116">The first step is to create a CSV file that contains information about each external contact that you want to import to Exchange Online.</span></span> 
  
1. <span data-ttu-id="2c2fa-117">Copiez le texte suivant dans un fichier texte dans le bloc-notes et enregistrez-le sur votre bureau sous forme de fichier CSV à l’aide d’un suffixe de nom de fichier de .csv ; par exemple, ExternalContacts.csv.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-117">Copy the following text to a text file in NotePad, and save it to your desktop as a CSV file by using a filename suffix of .csv; for example, ExternalContacts.csv.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="2c2fa-118">Si votre langue contient des caractères spéciaux (tels que **å**, **ä**et **ö** en suédois), enregistrez le fichier CSV avec UTF-8 ou autre codage Unicode lorsque vous enregistrez le fichier dans le bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-118">If your language contains special characters (such as **å**, **ä**, and **ö** in Swedish) save the CSV file with UTF-8 or other Unicode encoding when you save the file in NotePad.</span></span> 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    <span data-ttu-id="2c2fa-p102">La première ligne, ou ligne d’en-tête du fichier CSV répertorie les propriétés des contacts qui peuvent être utilisés lors de leur importation vers Exchange Online. Chaque nom de la propriété est séparée par une virgule. Chaque ligne sous la ligne d’en-tête représente les valeurs de propriété pour l’importation d’un seul contact externe.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p102">The first row, or header row, of the CSV file lists the properties of contacts that can be used when you import them to Exchange Online. Each property name is separated by a comma. Each row under the header row represents the property values for importing a single external contact.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="2c2fa-p103">Ce texte inclut des exemples de données que vous pouvez supprimer. Mais ne pas supprimer ou modifier la première ligne (en-tête). Il contient toutes les propriétés pour les contacts externes.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p103">This text includes sample data, which you can delete. But don't delete or change the first (header) row. It contains all of the properties for the external contacts.</span></span> 
  
2. <span data-ttu-id="2c2fa-125">Ouvrez le fichier CSV dans Microsoft Excel pour modifier le fichier CSV, car il est beaucoup plus facile à utiliser Excel pour modifier le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-125">Open the CSV file in Microsoft Excel to edit the CSV file because it's much easier to use Excel to edit the CSV file.</span></span>
    
3. <span data-ttu-id="2c2fa-p104">Créer une ligne pour chaque contact que vous souhaitez importer vers Exchange Online. Remplissez autant de cellules que possible. Ces informations s’affichera dans le carnet d’adresses partagé pour chaque contact.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p104">Create a row for each contact that you want to import to Exchange Online. Populate as many of the cells as possible. This information will be displayed in the shared address book for each contact.</span></span> 
    
    > [!IMPORTANT]
    >  <span data-ttu-id="2c2fa-p105">Les propriétés suivantes (qui sont les quatre premiers éléments dans la ligne d’en-tête) sont requises pour créer un contact externe et doit être renseignées dans le fichier CSV : **ExternalEmailAddress**, **nom**, **FirstName**, **LastName**. La commande PowerShell que vous exécutez à l’étape 2 utilise les valeurs de ces propriétés pour créer des contacts.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p105">The following properties (which are the first four items in the header row) are required to create an external contact and must be populated in the CSV file: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**. The PowerShell command that you run in Step 2 will use the values for these properties to create the contacts.</span></span> 

## <a name="step-2-create-the-external-contacts-with-powershell"></a><span data-ttu-id="2c2fa-131">Étape 2 : Créer des contacts externes avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c2fa-131">Step 2: Create the external contacts with PowerShell</span></span>

<span data-ttu-id="2c2fa-132">L’étape suivante consiste à utiliser le fichier CSV que vous avez créé à l’étape 1 et PowerShell en bloc importer les contacts externes répertoriés dans le fichier CSV vers Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-132">The next step is to use the CSV file that you created in Step 1 and PowerShell to bulk import the external contacts listed in the CSV file to Exchange Online.</span></span> 
  
1.  <span data-ttu-id="2c2fa-p106">Se connecter à PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Veillez à utiliser le nom d’utilisateur et le mot de passe pour votre compte d’administrateur général Office 365 lorsque vous vous connectez à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p106">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Be sure to use the user name and password for your Office 365 global administrator account when you connect to Exchange Online PowerShell.</span></span> 
    
2. <span data-ttu-id="2c2fa-136">Après la connexion à Exchange Online PowerShell, accédez au dossier Bureau où vous avez enregistré le fichier CSV à l’étape 1 ; par exemple `C:\Users\Administrator\desktop`.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-136">After you connect PowerShell to Exchange Online, go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="2c2fa-137">Exécutez la commande suivante pour créer des contacts externes :</span><span class="sxs-lookup"><span data-stu-id="2c2fa-137">Run the following command to create the external contacts:</span></span>

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    <span data-ttu-id="2c2fa-p107">Elle peut prendre un certain temps pour créer de nouveaux contacts, en fonction du nombre que vous importez. Lorsque la commande est terminée en cours d’exécution, PowerShell affiche une liste de nouveaux contacts qui ont été créées.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p107">It might take a while to create the new contacts, depending on how many you're importing. When the command is finished running, PowerShell displays a list of the new contacts that were created.</span></span> 
    
4. <span data-ttu-id="2c2fa-140">Pour afficher les nouveaux contacts externes, accédez au centre d’administration Exchange (CAE), puis cliquez sur **destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-140">To view the new external contacts, go to the Exchange admin center (EAC), and then click **Recipients** \> **Contacts**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="2c2fa-141">Pour obtenir des instructions pour la connexion au CAE, consultez la rubrique [Exchange admin center dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197).</span><span class="sxs-lookup"><span data-stu-id="2c2fa-141">For instructions for connecting to the EAC, see [Exchange admin center in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197).</span></span> 
  
5. <span data-ttu-id="2c2fa-142">Si nécessaire, cliquez sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour la liste et afficher les contacts externes qui ont été importés.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-142">If necessary, click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the list and see the external contacts that were imported.</span></span> 
    
    <span data-ttu-id="2c2fa-143">Les contacts importés apparaîtra dans le carnet d’adresses partagé dans Outlook et Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-143">The imported contacts will appear in the shared address book in Outlook and Outlook on the web.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2c2fa-144">Vous pouvez également afficher les contacts dans le centre d’administration Office 365 en accédant aux **utilisateurs** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-144">You can also view the contacts in the Office 365 admin center by going to **Users** \> **Contacts**.</span></span> 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a><span data-ttu-id="2c2fa-145">Étape 3 : Ajouter des informations sur les propriétés des contacts externes</span><span class="sxs-lookup"><span data-stu-id="2c2fa-145">Step 3: Add information to the properties of the external contacts</span></span>

<span data-ttu-id="2c2fa-p108">Une fois que vous exécutez la commande à l’étape 2, les contacts externes sont créés, mais ils ne contiennent pas les informations de contact ou l’organisation, qui est les plus d’informations à partir de la plupart des cellules dans le fichier CSV. C’est pourquoi lorsque vous créez de nouveaux contacts externes, uniquement les propriétés requises sont remplies. Ne vous inquiétez pas si vous n’avez pas toutes les informations renseignées dans le fichier CSV. Si ce n’est pas fait, il n’est ajouté.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p108">After you run the command in Step 2, the external contacts are created, but they don't contain any of the contact or organization information, which is the information from the most of the cells in the CSV file. This is because when you create new external contacts, only the required properties are populated. Don't worry if you don't have all the information populated in the CSV file. If it's not there, it won't be added.</span></span>
  
1.  <span data-ttu-id="2c2fa-p109">Se connecter à PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p109">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="2c2fa-152">Accédez au dossier Bureau où vous avez enregistré le fichier CSV à l’étape 1 ; par exemple `C:\Users\Administrator\desktop`.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-152">Go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="2c2fa-153">Exécutez les deux commandes suivantes pour ajouter d’autres propriétés à partir du fichier CSV pour les contacts externes que vous avez créé à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-153">Run the following two commands to add the other properties from the CSV file to the external contacts that you created in Step 2.</span></span>
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > <span data-ttu-id="2c2fa-p110">Le paramètre _Manager_ peut poser. Si la cellule est vide dans le fichier CSV, vous obtiendrez une erreur et aucune des informations de la propriété sera ajouté au contact. Si vous n’avez pas besoin de spécifier un gestionnaire, puis supprimez simplement ` -Manager $_.Manager ` de la commande PowerShell précédente.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p110">The  _Manager_ parameter might be problematic. If the cell is blank in the CSV file, you will get an error and none of the property information will be added to the contact. If you don't need to specify a manager, then just delete  ` -Manager $_.Manager ` from the previous PowerShell command.</span></span> 
  
    <span data-ttu-id="2c2fa-157">Là encore, il peut prendre un certain temps pour mettre à jour les contacts, en fonction du nombre que vous avez importé à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-157">Again, it might take a while to update the contacts, depending on how many you imported in Step 1.</span></span> 
    
4. <span data-ttu-id="2c2fa-158">Pour vérifier que les propriétés ont été ajoutées aux contacts :</span><span class="sxs-lookup"><span data-stu-id="2c2fa-158">To verify that the properties were added to the contacts:</span></span> 
    
1. <span data-ttu-id="2c2fa-159">Dans le CAE, accédez à **Destinataires** \> **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-159">In the EAC, go to **Recipients** \> **Contacts**.</span></span>
    
2. <span data-ttu-id="2c2fa-160">Cliquez sur un contact, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) pour afficher les propriétés du contact.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-160">Click a contact and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) to display the contact's properties.</span></span> 
    
<span data-ttu-id="2c2fa-p111">Voilà ! Les utilisateurs peuvent afficher les contacts et des informations supplémentaires dans le carnet d’adresses Outlook et Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p111">That's it! Users can see the contacts and the additional information in the address book Outlook and Outlook on the web.</span></span>
  
## <a name="add-more-external-contacts"></a><span data-ttu-id="2c2fa-163">Ajouter des contacts externes plus</span><span class="sxs-lookup"><span data-stu-id="2c2fa-163">Add more external contacts</span></span>

<span data-ttu-id="2c2fa-p112">Vous pouvez répéter les étapes 1 à l’étape 3 pour ajouter de nouveaux contacts externes dans Exchange Online. Vous ou les utilisateurs de votre société pouvant ajouter une nouvelle ligne dans le fichier CSV pour le nouveau contact. Ensuite, vous pouvez exécuter les commandes PowerShell d’étape 2 et étape 3 pour créer et ajouter des informations aux nouveaux contacts.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p112">You can repeat Steps 1 through Step 3 to add new external contacts in Exchange Online. You or users in your company can just add a new row in the CSV file for the new contact. Then you can run the PowerShell commands from Step 2 and Step 3 to create and add information to the new contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2c2fa-p113">Lorsque vous exécutez la commande pour créer des contacts, vous pouvez obtenir une erreur indiquant que les contacts qui ont été créées précédemment déjà existent. Mais n’importe quel contact ajouté au fichier CSV est créé.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p113">When you run the command to create new contacts, you might get an error saying that the contacts that were created earlier already exist. But any new contact added to the CSV file is created.</span></span> 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a><span data-ttu-id="2c2fa-169">Masquer les contacts externes à partir du carnet d’adresses partagé ></span><span class="sxs-lookup"><span data-stu-id="2c2fa-169">Hide external contacts from the shared address book></span></span>

<span data-ttu-id="2c2fa-p114">Certaines entreprises peuvent utiliser des contacts externes uniquement pour pouvoir être ajoutés en tant que membres des groupes de distribution. Dans ce scénario, ils souhaitent masquer les contacts externes à partir du carnet d’adresses partagé. Voici comment :</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p114">Some companies may use external contacts only so they can be added as members of distribution groups. In this scenario, they may want to hide external contacts from the shared address book. Here's how:</span></span>
  
1.  <span data-ttu-id="2c2fa-p115">Se connecter à PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="2c2fa-p115">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="2c2fa-175">Pour masquer un seul contact externe, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-175">To hide a single external contact, run the following command.</span></span>
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    <span data-ttu-id="2c2fa-176">Par exemple, pour masquer Pilar Pinilla dans le carnet d’adresses partagé, exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="2c2fa-176">For example, to hide Pilar Pinilla from the shared address book, run this command:</span></span>

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. <span data-ttu-id="2c2fa-177">Pour masquer tous les contacts externes à partir du carnet d’adresses partagé, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2c2fa-177">To hide all external contacts from the shared address book, run this command:</span></span>

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

<span data-ttu-id="2c2fa-178">Une fois les masquer, contacts externes ne sont pas affichés dans le carnet d’adresses partagé, mais vous pouvez toujours ajouter en tant que membres d’un groupe de distribution.</span><span class="sxs-lookup"><span data-stu-id="2c2fa-178">After you hide them, external contacts aren't displayed in the shared address book, but you can still add them as members of a distribution group.</span></span>
