---
title: Recherche en nuage des boîtes aux lettres pour les utilisateurs locaux dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/4/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: Utiliser l’outil de recherche de contenu de sécurité Office 365 &amp; centre de conformité pour rechercher et exporter les données de conversation MicrosoftTeams (appelées conversations 1xN) pour les utilisateurs locaux dans un déploiement Exchange hybride.
ms.openlocfilehash: a504dfcf4c82bec036137b90312c01a0b2326ccc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527911"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a>Recherche en nuage des boîtes aux lettres pour les utilisateurs locaux dans Office 365

Si votre organisation a un déploiement hybride Exchange et a activé Teams Microsoft, les utilisateurs peuvent utiliser l’application de conversation équipes pour la messagerie instantanée. L’utilisateur basée sur le cloud, les données de conversation équipes (également appelées 1xN conversations) sont enregistrées dans leur boîte aux lettres principale basée sur le cloud. Lorsqu’un utilisateur local utilise l’application de conversation de l’équipe, leur boîte aux lettres principale est situé sur site. Pour contourner cette limitation, Microsoft a publié une nouvelle fonctionnalité dans lequel une zone de stockage en nuage (appelée une boîte aux lettres en nuage pour les utilisateurs locaux) est créée pour stocker les données de conversation équipes pour les utilisateurs locaux. Cela vous permet d’utiliser l’outil de recherche de contenu de sécurité Office 365 &amp; des équipes de centre de conformité pour rechercher et exporter des données de conversation pour les utilisateurs locaux. 
  
Voici les conditions requises et la limitation pour la configuration et à configurer et en nuage des boîtes aux lettres pour les utilisateurs locaux de recherche :
  
- Les comptes d’utilisateurs dans votre service d’annuaire local (par exemple, Active Directory) doivent être synchronisées avec Azure Active Directory, le service d’annuaire dans Office 365. Cela signifie qu’un compte d’utilisateur de messagerie est créé dans Office 365 et est associé à un utilisateur de boîte aux lettres principale se trouve dans l’organisation locale.
    
- La boîte aux lettres en nuage pour les utilisateurs locaux est utilisée pour stocker uniquement les équipes conversation données. Un utilisateur local ne peut pas se connecter à la boîte aux lettres en nuage ou accéder en aucune façon. Il ne peut pas être utilisé pour envoyer ou recevoir des messages électroniques. 
    
- Vous devez envoyer une demande au Support Microsoft à votre organisation de données de recherche pour les équipes de conversation dans les boîtes aux lettres en nuage pour les utilisateurs locaux. Voir [une demande de support de Microsoft pour activer cette fonctionnalité dans la sécurité de classement &amp; centre de conformité](#filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center) dans cet article. 
    
 **Remarque :** Conversations du canal équipes sont toujours stockées dans la boîte aux lettres en nuage qui est associé à l’équipe. Cela signifie que vous pouvez utiliser la recherche de contenu à canal recherche conversations sans ont à une demande de prise en charge du fichier. Pour plus d’informations sur la recherche des équipes de canal conversations, voir [recherche des équipes de Microsoft et des groupes d’Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups).
  
## <a name="how-it-works"></a>Fonctionnement

Si un utilisateur activé pour les équipes Microsoft a une boîte aux lettres locale et leur identité/compte d’utilisateur a été synchronisée dans le nuage, Microsoft crée une boîte aux lettres en nuage pour stocker les données de conversation 1xN équipes. Une fois que les données de conversation d’équipes sont stockées dans la boîte aux lettres en nuage, il est indexé pour la recherche. Cela vous permet d’utiliser la recherche de contenu (et les recherches associées aux cas eDiscovery) pour rechercher, afficher un aperçu et exporter des données de conversation équipes pour les utilisateurs locaux. Vous pouvez également utiliser ** \*ComplianceSearch** applets de commande de sécurité Office 365 &amp; PowerShell du centre de conformité pour rechercher des équipes de données de conversation pour les utilisateurs locaux. 
  
Le graphique suivant montre comment les équipes conversation données pour les utilisateurs sur site de flux de travail est disponible pour la recherche, à afficher et exporter.
  
![Nuage de stockage pour les utilisateurs locaux dans Microsoft Teams](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
Outre cette nouvelle fonctionnalité, vous pouvez toujours utiliser recherche de contenu à rechercher, afficher un aperçu et exporter des équipes contenu dans le site de SharePoint en nuage et boîte aux lettres Exchange associées aux données de conversation dans la boîte aux lettres Exchange Online pour chaque Team Microsoft et les équipes de 1xN utilisateurs en nuage.

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center"></a>Une demande de support de Microsoft pour activer cette fonctionnalité dans la sécurité de classement &amp; centre de conformité

Vous devez introduire une demande avec Support de Microsoft permettent à votre organisation d’utiliser l’interface utilisateur graphique de la sécurité &amp; centre de conformité pour rechercher des équipes de données de conversation dans les boîtes aux lettres en nuage pour les utilisateurs locaux. Notez que cette fonctionnalité est disponible dans Office 365 sécurité &amp; PowerShell du centre de conformité. Vous n’êtes pas obligé de soumettre une demande de prise en charge à l’aide de PowerShell pour rechercher des données de conversation équipes pour les utilisateurs locaux. 
  
Inclure les informations suivantes lorsque vous soumettez la demande de Support Microsoft :
  
- Le nom de domaine par défaut de votre organisation Office 365.
    
- Le nom du client et l’ID de client de votre organisation Office 365. Vous trouverez dans le portail d’Azure Active Directory (sous **Gérer** \> **Propriétés**). Consultez la rubrique [Rechercher votre ID de client Office 365](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b).
    
- Le titre ou la description de l’objectif de la demande de prise en charge suivantes : « Activer la recherche de contenu d’Application pour les utilisateurs locaux ». Cela permettra d’acheminer la demande vers l’équipe d’ingénierie eDiscovery Office 365 qui vous allez implémenter la demande. 
    
Après la modification d’ingénierie, Support Microsoft vous envoie une date estimée de déploiement. Notez que le processus de déploiement ne dure 2 à 3 semaines après avoir envoyé la demande de prise en charge. 
  
### <a name="what-happens-after-this-feature-is-enabled"></a>Que se passe-t-il après que cette fonctionnalité est activée ?

Une fois que cette fonctionnalité est déployée dans votre organisation Office 365, les modifications suivantes sont apportées à la recherche de contenu et dans les recherches associées à une découverte électronique cas dans la sécurité &amp; centre de conformité :
  
- La case à cocher **Office ajouter le contenu d’application pour les utilisateurs locaux** est ajoutée sous les **emplacements** de la recherche de contenu. 
    
    ![La case à cocher « Ajouter le contenu d’application Office pour les utilisateurs locaux » est ajouté à l’interface de recherche de contenu](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- Les utilisateurs locaux sont affichés dans le sélecteur d’emplacements de contenu qui vous permet de sélectionner les boîtes aux lettres de l’utilisateur à rechercher. 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a>Recherche de conversation équipes contenue dans les boîtes aux lettres en nuage pour les utilisateurs locaux

Une fois que la fonctionnalité a été activée, vous pouvez utiliser la recherche de contenu dans la sécurité &amp; centre de conformité pour rechercher des équipes de données de conversation dans les boîtes aux lettres en nuage pour les utilisateurs locaux. 
  
1. Dans la sécurité &amp; centre de conformité, accédez à **recherche &amp; enquête** \> **recherche de contenu**
    
2. Dans la page de **recherche** , cliquez sur ![icône Ajouter](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **nouvelle recherche**.
    
    Comme expliqué précédemment, la case à cocher **Office ajouter le contenu d’application pour les utilisateurs locaux** s’affiche sous **emplacements**. Notez qu’il est sélectionné par défaut.
    
3. Créez la requête de mot clé et ajouter des conditions à la requête de recherche si nécessaire. Pour rechercher l’équipe uniquement chats des données, vous pouvez ajouter la requête suivante dans la zone **mots clés** : 
    
    ```
    kind:im
    ``` 

4. À ce stade, vous pouvez choisir une des options suivantes sous **emplacements**:
    
    - **Tous les emplacements** - Sélectionnez cette option pour rechercher les boîtes aux lettres de tous les utilisateurs de votre organisation. Lorsque la case à cocher est activée, toutes les boîtes aux basée sur le cloud pour les utilisateurs locaux sont également examinés. 
    
    - **Emplacements spécifiques** - Sélectionnez cette option, puis cliquez sur **Modifier** \> choisissez utilisateur, des groupes ou équipes pour rechercher les boîtes aux lettres spécifiques. Comme expliqué précédemment, le sélecteur d’emplacements vous permet de rechercher des utilisateurs locaux. 
    
5. Enregistrer et exécuter la recherche. Les résultats de la recherche à partir des boîtes aux lettres en nuage pour les utilisateurs locaux peuvent être affichés comme des autres résultats de recherche. Vous pouvez en outre, vous pouvez exporter les résultats de recherche (y compris les données de conversation équipes) vers un fichier PST. Pour plus d’informations, voir : 
    
    - [Créer une nouvelle recherche](content-search.md#create-a-new-search)
    
    - [Aperçu des résultats de la recherche](content-search.md#preview-search-results)
    
    - [Exporter les résultats de recherche de contenu à partir de la sécurité de 365 Office &amp; centre de conformité](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a>Utilisation de PowerShell pour les données de recherche pour les équipes de conversation dans le nuage des boîtes aux lettres pour les utilisateurs locaux

Vous pouvez utiliser les applets de commande **New-ComplianceSearch** et **Set-ComplianceSearch** de sécurité Office 365 &amp; PowerShell du centre de conformité pour rechercher la boîte aux lettres en nuage pour les utilisateurs locaux. Comme expliqué précédemment, vous n’êtes pas obligé de soumettre une demande de prise en charge à l’aide de PowerShell pour rechercher des données de conversation équipes pour les utilisateurs locaux. 
  
1. [Se connecter à Office 365 sécurité &amp; centre de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
    
2. Exécuter le PowerShell suivante pour créer un nouveau contenu recherche les boîtes aux lettres en nuage des utilisateurs locaux.
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    Le paramètre *IncludeUserAppContent* est utilisé pour spécifier la boîte aux lettres en nuage pour les utilisateurs qui sont spécifiés par le paramètre *ExchangeLocation* . *AllowNotFoundExchangeLocationsEnabled* permet de boîtes aux lettres en nuage pour les utilisateurs locaux. Lorsque vous utilisez la `$true` valeur pour ce paramètre, la recherche n’essaie pas de valider l’existence de la boîte aux lettres avant l’exécution. Cela est nécessaire pour rechercher les boîtes aux lettres en nuage pour les utilisateurs locaux, car ces types de boîtes aux lettres ne pas résoudre en tant que boîtes aux lettres ordinaires. 
    
    L’exemple suivant recherche les équipes conversations (qui sont des messages instantanés) qui contiennent le mot clé « redstone » dans la boîte aux lettres en nuage de Sara Davis, qui est un utilisateur local dans l’organisation Contoso.
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   Après avoir créé une nouvelle recherche, veillez à utiliser l’applet de commande **Start-ComplianceSearch** pour lancer la recherche. 
  
Pour plus d’informations à l’aide de ces applets de commande, voir :
  
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [Set-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a>Problèmes connus

- Actuellement, vous ne pouvez recherche, aperçu et exporter du contenu dans le nuage des boîtes aux lettres pour les utilisateurs locaux. Placer une boîte aux lettres en nuage pour un utilisateur local sur une suspension associée à une découverte électronique cas ou affecter à une stratégie de rétention Office 365 n'est pas pris en charge. 
    
- Le sélecteur d’emplacement de contenu pour la découverte électronique conserve affiche les utilisateurs locaux et vous permettra de sélectionner les. Toutefois, comme expliqué que la suspension n’est pas appliquée à l’utilisateur local.
    
## <a name="frequently-asked-questions"></a>Questions fréquemment posées

 **Où se trouvent les boîtes aux lettres en nuage pour les utilisateurs locaux ?**
  
Boîtes aux lettres en nuage sont créées et stockées dans le même centre de données en tant que votre organisation Office 365. 
  
 **Existe-t-il d’autres exigences autre que la soumission d’une demande de prise en charge ?**
  
 Comme expliqué précédemment, les identités des utilisateurs avec des boîtes aux lettres sur les prem doivent être synchronisées avec votre organisation en nuage afin qu’un compte d’utilisateur de messagerie correspondant est créé pour chaque compte d’utilisateur local dans Office 365. En outre, votre organisation doit disposer d’un abonnement à Office 365 entreprise, par exemple un abonnement à Office 365 entreprise E1, E3 ou E5. 
  
 **Existe-t-il un risque de perdre les données de conversation équipes si la boîte aux lettres locale de l’utilisateur est migré vers le nuage ?**
  
Non. Lorsque vous migrez les boîtes aux lettres principal d’un utilisateur local vers le nuage, les données de conversation équipes pour cet utilisateur migrent vers leur nouvelle en nuage boîte aux lettres principale.
  
 **Puis-je appliquer un blocage eDiscovery ou des stratégies de rétention Office 365 pour les utilisateurs locaux ?**
  
Non.
  
 **Peut rechercher de recherche de contenu équipes anciennes conversations pour les utilisateurs locaux avant l’heure de mon organisation envoyé la demande pour activer cette fonctionnalité ?**
  
Microsoft commencé à stocker les données de conversation équipes pour les utilisateurs locaux sur le 31 janvier 2018. Par conséquent, si l’identité d’un utilisateur d’équipes locale a été synchronisée entre Active Directory et Azure Active Directory depuis cette date, leurs données de conversation équipes seront stockées dans une boîte aux lettres en nuage et une recherche à l’aide de la recherche de contenu. Microsoft fonctionne également sur le stockage des données de conversation des équipes d’avant le 31 janvier 2018 dans les boîtes aux lettres en nuage pour les utilisateurs locaux. Informations complémentaires sur cette sera bientôt disponibles.
