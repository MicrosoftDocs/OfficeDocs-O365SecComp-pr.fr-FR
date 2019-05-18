---
title: Importation en bloc de contacts externes vers Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
audience: End User
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: Découvrez comment les administrateurs peuvent utiliser Exchange Online PowerShell et un fichier CSV pour importer en bloc des contacts externes dans la liste d’adresses globale.
ms.openlocfilehash: 08fe7666f03c7fe60555133292be9e27a9ffa413
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152206"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a>Importation en bloc de contacts externes vers Exchange Online

**Cet article est destiné aux administrateurs. Essayez-vous d’importer des contacts dans votre propre boîte aux lettres? Voir [importer des contacts dans Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**
   
Votre entreprise a-t-elle un grand nombre de contacts professionnels existants que vous souhaitez inclure dans le carnet d’adresses partagé (également appelé liste d’adresses globale) dans Exchange Online? Voulez-vous ajouter des contacts externes en tant que membres de groupes de distribution, comme vous pouvez le faire avec des utilisateurs au sein de votre entreprise? Si c’est le cas, vous pouvez utiliser Exchange Online PowerShell et un fichier CSV (valeurs séparées par des virgules) pour importer en bloc des contacts externes dans Exchange Online. Il s’agit d’un processus en trois étapes:
  
[Étape 1: créer un fichier CSV contenant des informations sur les contacts externes](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[Étape 2: créer les contacts externes avec PowerShell](#step-2-create-the-external-contacts-with-powershell) 

[Étape 3: ajouter des informations aux propriétés des contacts externes](#step-3-add-information-to-the-properties-of-the-external-contacts)

Après avoir effectué ces étapes pour importer des contacts, vous pouvez effectuer les tâches supplémentaires suivantes:
  
- [Ajouter des contacts externes](#add-more-external-contacts)
  
- [Masquer les contacts externes dans le carnet d’adresses partagé](#hide-external-contacts-from-the-shared-address-book)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a>Étape 1: créer un fichier CSV contenant des informations sur les contacts externes

La première étape consiste à créer un fichier CSV qui contient des informations sur chaque contact externe que vous souhaitez importer vers Exchange Online. 
  
1. Copiez le texte suivant dans un fichier texte dans le bloc-notes et enregistrez-le sur votre bureau en tant que fichier CSV à l’aide d’un suffixe de nom de fichier. csv; par exemple, ExternalContacts. csv.
    
    > [!TIP]
    > Si votre langue contient des caractères spéciaux (tels que **å**, **ä**et **ö** en Suédois), enregistrez le fichier CSV avec UTF-8 ou un autre codage Unicode lorsque vous enregistrez le fichier dans le bloc-notes. 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    La première ligne, ou ligne d’en-tête, du fichier CSV répertorie les propriétés des contacts qui peuvent être utilisés lorsque vous les importez vers Exchange Online. Chaque nom de propriété est séparé par une virgule. Chaque ligne sous la ligne d’en-tête représente les valeurs de propriété pour l’importation d’un contact externe unique. 
    
    > [!NOTE]
    > Ce texte inclut des exemples de données que vous pouvez supprimer. Mais ne supprimez pas ou ne modifiez pas la première ligne (en-tête). Elle contient toutes les propriétés des contacts externes. 
  
2. Ouvrez le fichier CSV dans Microsoft Excel pour modifier le fichier CSV, car il est beaucoup plus facile d’utiliser Excel pour modifier le fichier CSV.
    
3. Créez une ligne pour chaque contact que vous souhaitez importer vers Exchange Online. Remplissez autant de cellules que possible. Ces informations s’affichent dans le carnet d’adresses partagé pour chaque contact. 
    
    > [!IMPORTANT]
    >  Les propriétés suivantes (qui sont les quatre premiers éléments de la ligne d’en-tête) sont requises pour créer un contact externe et doivent être renseignées dans le fichier CSV: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**. La commande PowerShell que vous exécutez à l’étape 2 utilisera les valeurs de ces propriétés pour créer les contacts. 

## <a name="step-2-create-the-external-contacts-with-powershell"></a>Étape 2: créer les contacts externes avec PowerShell

L’étape suivante consiste à utiliser le fichier CSV que vous avez créé à l’étape 1 et PowerShell pour importer en bloc les contacts externes figurant dans le fichier CSV vers Exchange Online. 
  
1.  Connectez PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Veillez à utiliser le nom d’utilisateur et le mot de passe de votre compte d’administrateur général Office 365 lorsque vous vous connectez à Exchange Online PowerShell. 
    
2. Une fois que vous avez connecté PowerShell à Exchange Online, accédez au dossier du bureau dans lequel vous avez enregistré le fichier CSV à l’étape 1; par exemple `C:\Users\Administrator\desktop`.
    
3. Exécutez la commande suivante pour créer les contacts externes:

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    La création des nouveaux contacts peut prendre un certain temps, selon le nombre d’importations que vous importez. Une fois l’exécution de la commande terminée, PowerShell affiche la liste des nouveaux contacts qui ont été créés. 
    
4. Pour afficher les nouveaux contacts externes, accédez au centre d’administration Exchange, puis cliquez sur **contacts**des **destinataires** \> . 
    
    > [!TIP]
    > Pour obtenir des instructions sur la connexion au centre d’administration Exchange, consultez la rubrique [Exchange Admin Center in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197). 
  
5. Si nécessaire, cliquez **** ![sur Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) l’actualisation de la liste pour afficher les contacts externes qui ont été importés. 
    
    Les contacts importés apparaissent dans le carnet d’adresses partagé d’Outlook et d’Outlook sur le Web.
    
    > [!NOTE]
    > Vous pouvez également afficher les contacts dans le centre d’administration Microsoft 365 en accédant à **utilisateurs** \> et **contacts**. 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a>Étape 3: ajouter des informations aux propriétés des contacts externes

Une fois que vous avez exécuté la commande à l’étape 2, les contacts externes sont créés, mais ils ne contiennent aucune des informations de contact ou d’organisation, c’est-à-dire les informations provenant de la plupart des cellules dans le fichier CSV. En effet, lorsque vous créez des contacts externes, seules les propriétés requises sont renseignées. Ne vous inquiétez pas si toutes les informations ne sont pas renseignées dans le fichier CSV. S’il ne s’y trouve pas, il ne sera pas ajouté.
  
1.  Connectez PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Accédez au dossier du bureau dans lequel vous avez enregistré le fichier CSV à l’étape 1; par exemple `C:\Users\Administrator\desktop`.
    
3. Exécutez les deux commandes suivantes pour ajouter les autres propriétés du fichier CSV aux contacts externes que vous avez créés à l’étape 2.
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > Le paramètre _Manager_ peut être problématique. Si la cellule est vide dans le fichier CSV, vous obtiendrez une erreur et aucune information sur la propriété ne sera ajoutée au contact. Si vous n’avez pas besoin de spécifier un gestionnaire, supprimez ` -Manager $_.Manager ` simplement de la commande PowerShell précédente. 
  
    Encore une fois, la mise à jour des contacts peut prendre un certain temps, selon le nombre d’importations que vous avez importées à l’étape 1. 
    
4. Pour vérifier que les propriétés ont été ajoutées aux contacts, procédez comme suit: 
    
1. Dans le CAE, accédez à **Destinataires** \> **Contacts**.
    
2. Cliquez sur un contact, puis sur **modifier** ![l'](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) icône modifier pour afficher les propriétés du contact. 
    
Voilà ! Les utilisateurs peuvent voir les contacts et les informations supplémentaires dans le carnet d’adresses Outlook et Outlook sur le Web.
  
## <a name="add-more-external-contacts"></a>Ajouter des contacts externes

Vous pouvez répéter les étapes 1 à 3 pour ajouter de nouveaux contacts externes dans Exchange Online. Vous ou les utilisateurs de votre entreprise pouvez simplement ajouter une nouvelle ligne dans le fichier CSV pour le nouveau contact. Ensuite, vous pouvez exécuter les commandes PowerShell de l’étape 2 et de l’étape 3 pour créer et ajouter des informations aux nouveaux contacts.
  
> [!NOTE]
> Lorsque vous exécutez la commande pour créer des contacts, vous pouvez obtenir une erreur indiquant que les contacts créés précédemment existent déjà. Toutefois, tout nouveau contact ajouté au fichier CSV est créé. 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a>Masquer les contacts externes à partir de l’adresse partagée book>

Certaines sociétés peuvent utiliser des contacts externes uniquement afin qu’ils puissent être ajoutés en tant que membres des groupes de distribution. Dans ce scénario, ils peuvent souhaiter masquer des contacts externes à partir du carnet d’adresses partagé. Voici comment procéder :
  
1.  Connectez PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, consultez la rubrique [connexion à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Pour masquer un seul contact externe, exécutez la commande suivante.
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    Par exemple, pour masquer Pilar Pinilla dans le carnet d’adresses partagé, exécutez la commande suivante:

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. Pour masquer tous les contacts externes du carnet d’adresses partagé, exécutez la commande suivante:

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

Une fois que vous les avez masquées, les contacts externes ne s’affichent pas dans le carnet d’adresses partagé, mais vous pouvez toujours les ajouter en tant que membres d’un groupe de distribution.
