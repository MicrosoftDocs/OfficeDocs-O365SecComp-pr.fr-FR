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
# <a name="bulk-import-external-contacts-to-exchange-online"></a>Importation en bloc des contacts externes à Exchange Online

**Cet article est destiné aux administrateurs. Vous essayez d’importer des contacts à votre propre boîte aux lettres ? Voir [Importer des contacts dans Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**
   
Votre entreprise a-t-elle beaucoup de contacts professionnels existante que vous souhaitez inclure dans le carnet d’adresses partagé (également appelée la liste d’adresses globale) dans Exchange Online ? Vous souhaitez ajouter des contacts externes en tant que membres des groupes de distribution, tout comme vous pouvez avec des utilisateurs au sein de votre entreprise ? Si ce cas, vous pouvez utiliser Exchange Online PowerShell et un fichier CSV (valeurs séparées par des virgules) en bloc importer des contacts externes dans Exchange Online. Il est un processus en trois étapes :
  
[Étape 1 : Créer un fichier CSV qui contient des informations sur les contacts externes](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[Étape 2 : Créer des contacts externes avec PowerShell](#step-2-create-the-external-contacts-with-powershell) 

[Étape 3 : Ajouter des informations sur les propriétés des contacts externes](#step-3-add-information-to-the-properties-of-the-external-contacts)

Après avoir effectué ces étapes pour importer des contacts, vous pouvez effectuer ces tâches supplémentaires :
  
- [Ajouter des contacts externes plus](bulk-import-external-contacts.md#AddMore)
  
- [Masquer les contacts externes à partir du carnet d’adresses partagé](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a>Étape 1 : Créer un fichier CSV qui contient des informations sur les contacts externes

La première étape consiste à créer un fichier CSV qui contient des informations sur chaque contact externe que vous souhaitez importer vers Exchange Online. 
  
1. Copiez le texte suivant dans un fichier texte dans le bloc-notes et enregistrez-le sur votre bureau sous forme de fichier CSV à l’aide d’un suffixe de nom de fichier de .csv ; par exemple, ExternalContacts.csv.
    
    > [!TIP]
    > Si votre langue contient des caractères spéciaux (tels que **å**, **ä**et **ö** en suédois), enregistrez le fichier CSV avec UTF-8 ou autre codage Unicode lorsque vous enregistrez le fichier dans le bloc-notes. 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    La première ligne, ou ligne d’en-tête du fichier CSV répertorie les propriétés des contacts qui peuvent être utilisés lors de leur importation vers Exchange Online. Chaque nom de la propriété est séparée par une virgule. Chaque ligne sous la ligne d’en-tête représente les valeurs de propriété pour l’importation d’un seul contact externe. 
    
    > [!NOTE]
    > Ce texte inclut des exemples de données que vous pouvez supprimer. Mais ne pas supprimer ou modifier la première ligne (en-tête). Il contient toutes les propriétés pour les contacts externes. 
  
2. Ouvrez le fichier CSV dans Microsoft Excel pour modifier le fichier CSV, car il est beaucoup plus facile à utiliser Excel pour modifier le fichier CSV.
    
3. Créer une ligne pour chaque contact que vous souhaitez importer vers Exchange Online. Remplissez autant de cellules que possible. Ces informations s’affichera dans le carnet d’adresses partagé pour chaque contact. 
    
    > [!IMPORTANT]
    >  Les propriétés suivantes (qui sont les quatre premiers éléments dans la ligne d’en-tête) sont requises pour créer un contact externe et doit être renseignées dans le fichier CSV : **ExternalEmailAddress**, **nom**, **FirstName**, **LastName**. La commande PowerShell que vous exécutez à l’étape 2 utilise les valeurs de ces propriétés pour créer des contacts. 

## <a name="step-2-create-the-external-contacts-with-powershell"></a>Étape 2 : Créer des contacts externes avec PowerShell

L’étape suivante consiste à utiliser le fichier CSV que vous avez créé à l’étape 1 et PowerShell en bloc importer les contacts externes répertoriés dans le fichier CSV vers Exchange Online. 
  
1.  Se connecter à PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Veillez à utiliser le nom d’utilisateur et le mot de passe pour votre compte d’administrateur général Office 365 lorsque vous vous connectez à Exchange Online PowerShell. 
    
2. Après la connexion à Exchange Online PowerShell, accédez au dossier Bureau où vous avez enregistré le fichier CSV à l’étape 1 ; par exemple `C:\Users\Administrator\desktop`.
    
3. Exécutez la commande suivante pour créer des contacts externes :

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    Elle peut prendre un certain temps pour créer de nouveaux contacts, en fonction du nombre que vous importez. Lorsque la commande est terminée en cours d’exécution, PowerShell affiche une liste de nouveaux contacts qui ont été créées. 
    
4. Pour afficher les nouveaux contacts externes, accédez au centre d’administration Exchange (CAE), puis cliquez sur **destinataires** \> **Contacts**. 
    
    > [!TIP]
    > Pour obtenir des instructions pour la connexion au CAE, consultez la rubrique [Exchange admin center dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197). 
  
5. Si nécessaire, cliquez sur **Actualiser** ![icône Actualiser](media/O365-MDM-Policy-RefreshIcon.gif) pour mettre à jour la liste et afficher les contacts externes qui ont été importés. 
    
    Les contacts importés apparaîtra dans le carnet d’adresses partagé dans Outlook et Outlook sur le web.
    
    > [!NOTE]
    > Vous pouvez également afficher les contacts dans le centre d’administration Office 365 en accédant aux **utilisateurs** \> **Contacts**. 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a>Étape 3 : Ajouter des informations sur les propriétés des contacts externes

Une fois que vous exécutez la commande à l’étape 2, les contacts externes sont créés, mais ils ne contiennent pas les informations de contact ou l’organisation, qui est les plus d’informations à partir de la plupart des cellules dans le fichier CSV. C’est pourquoi lorsque vous créez de nouveaux contacts externes, uniquement les propriétés requises sont remplies. Ne vous inquiétez pas si vous n’avez pas toutes les informations renseignées dans le fichier CSV. Si ce n’est pas fait, il n’est ajouté.
  
1.  Se connecter à PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Accédez au dossier Bureau où vous avez enregistré le fichier CSV à l’étape 1 ; par exemple `C:\Users\Administrator\desktop`.
    
3. Exécutez les deux commandes suivantes pour ajouter d’autres propriétés à partir du fichier CSV pour les contacts externes que vous avez créé à l’étape 2.
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > Le paramètre _Manager_ peut poser. Si la cellule est vide dans le fichier CSV, vous obtiendrez une erreur et aucune des informations de la propriété sera ajouté au contact. Si vous n’avez pas besoin de spécifier un gestionnaire, puis supprimez simplement ` -Manager $_.Manager ` de la commande PowerShell précédente. 
  
    Là encore, il peut prendre un certain temps pour mettre à jour les contacts, en fonction du nombre que vous avez importé à l’étape 1. 
    
4. Pour vérifier que les propriétés ont été ajoutées aux contacts : 
    
1. Dans le CAE, accédez à **Destinataires** \> **Contacts**.
    
2. Cliquez sur un contact, puis cliquez sur **Modifier** ![icône Modifier](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) pour afficher les propriétés du contact. 
    
Voilà ! Les utilisateurs peuvent afficher les contacts et des informations supplémentaires dans le carnet d’adresses Outlook et Outlook sur le web.
  
## <a name="add-more-external-contacts"></a>Ajouter des contacts externes plus

Vous pouvez répéter les étapes 1 à l’étape 3 pour ajouter de nouveaux contacts externes dans Exchange Online. Vous ou les utilisateurs de votre société pouvant ajouter une nouvelle ligne dans le fichier CSV pour le nouveau contact. Ensuite, vous pouvez exécuter les commandes PowerShell d’étape 2 et étape 3 pour créer et ajouter des informations aux nouveaux contacts.
  
> [!NOTE]
> Lorsque vous exécutez la commande pour créer des contacts, vous pouvez obtenir une erreur indiquant que les contacts qui ont été créées précédemment déjà existent. Mais n’importe quel contact ajouté au fichier CSV est créé. 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a>Masquer les contacts externes à partir du carnet d’adresses partagé >

Certaines entreprises peuvent utiliser des contacts externes uniquement pour pouvoir être ajoutés en tant que membres des groupes de distribution. Dans ce scénario, ils souhaitent masquer les contacts externes à partir du carnet d’adresses partagé. Voici comment :
  
1.  Se connecter à PowerShell à votre organisation Exchange Online. Pour obtenir des instructions détaillées, voir [se connecter à Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Pour masquer un seul contact externe, exécutez la commande suivante.
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    Par exemple, pour masquer Pilar Pinilla dans le carnet d’adresses partagé, exécutez cette commande :

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. Pour masquer tous les contacts externes à partir du carnet d’adresses partagé, exécutez la commande suivante :

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

Une fois les masquer, contacts externes ne sont pas affichés dans le carnet d’adresses partagé, mais vous pouvez toujours ajouter en tant que membres d’un groupe de distribution.
