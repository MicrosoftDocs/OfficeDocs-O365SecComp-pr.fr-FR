---
title: Recherche de boîtes aux lettres en nuage pour les utilisateurs locaux dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: Utilisez l’outil de recherche de contenu dans le centre de sécurité & conformité pour rechercher et exporter des données de conversation MicrosoftTeams (appelées conversations 1xN) pour les utilisateurs locaux dans un déploiement hybride Exchange.
ms.openlocfilehash: 4bc63c4a908aba61b0f289d347d1434222ec2ed8
ms.sourcegitcommit: a97e7da9a1f870540f0bdcba7be5fb6f8bd12f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2019
ms.locfileid: "35756856"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a>Recherche de boîtes aux lettres en nuage pour les utilisateurs locaux dans Office 365

Si votre organisation a un déploiement hybride Exchange et a activé Microsoft Teams, les utilisateurs peuvent utiliser l’application de conversation teams pour la messagerie instantanée. Pour l’utilisateur en nuage, les données de conversation de Teams (également appelées conversations 1xN) sont enregistrées dans leur boîte aux lettres principale en nuage. Lorsqu’un utilisateur local utilise l’application de conversation d’équipe, sa boîte aux lettres principale est située en local. Pour contourner cette limitation, Microsoft a publié une nouvelle fonctionnalité dans laquelle une zone de stockage en nuage (appelée boîte aux lettres en nuage pour les utilisateurs locaux) est créée pour stocker les données de conversation des équipes pour les utilisateurs locaux. Cela vous permet d’utiliser l’outil de recherche de contenu dans le centre de conformité & Compliance pour rechercher et exporter des données de conversation de teams pour des utilisateurs locaux. 
  
Voici les conditions requises et les limites de configuration des boîtes aux lettres en nuage pour les utilisateurs locaux:
  
- Les comptes d’utilisateur dans votre service d’annuaire local (par exemple, Active Directory) doivent être synchronisés avec Azure Active Directory, le service d’annuaire dans Office 365. Cela signifie qu’un compte d’utilisateur de messagerie est créé dans Office 365 et qu’il est associé à un utilisateur dont la boîte aux lettres principale se trouve dans l’organisation locale.

- L’utilisateur dont la boîte aux lettres principale se trouve dans l’organisation locale doit disposer d’une licence Microsoft teams et d’une licence Exchange Online plan 1.
    
- La boîte aux lettres en nuage pour les utilisateurs locaux est utilisée uniquement aux données de conversation des équipes de magasin. Un utilisateur local ne peut pas se connecter à la boîte aux lettres en nuage ou accéder de quelque manière que ce soit. Il ne peut pas être utilisé pour envoyer ou recevoir des messages électroniques. 
    
- Vous devez soumettre une demande au support Microsoft pour permettre à votre organisation de rechercher des données de conversation teams dans les boîtes aux lettres en nuage pour les utilisateurs locaux. Consultez la rubrique [classement d’une demande auprès du support Microsoft pour activer cette fonctionnalité](#filing-a-request-with-microsoft-support-to-enable-this-feature) dans cet article. 
    
 **Remarque:** Les conversations de canal teams sont toujours stockées dans la boîte aux lettres en nuage qui est associée à l’équipe. Cela signifie que vous pouvez utiliser la recherche de contenu pour rechercher des conversations de canal sans avoir besoin de classer une demande de support. Pour plus d’informations sur la recherche de conversations de canal dans Teams, consultez la rubrique [recherche de groupes Microsoft teams et Office 365](content-search.md#searching-microsoft-teams-and-office-365-groups).
  
## <a name="how-it-works"></a>Mode de fonctionnement

Si un utilisateur à extension de Microsoft teams dispose d’une boîte aux lettres locale et que son compte d’utilisateur/son identité a été synchronisé dans le nuage, Microsoft crée une boîte aux lettres en nuage pour stocker les données de conversation des équipes 1xN. Une fois que les données de conversation de teams sont stockées dans la boîte aux lettres en nuage, elles sont indexées pour la recherche. Cela vous permet d’utiliser la recherche de contenu (et les recherches associées aux cas eDiscovery) pour rechercher, prévisualiser et exporter des données de conversation de teams pour des utilisateurs locaux. Vous pouvez également utiliser ** \*** des applets de commande ComplianceSearch dans le centre de conformité & de sécurité PowerShell pour rechercher des données de conversation teams pour les utilisateurs locaux. 
  
Le graphique suivant illustre le flux de travail de la façon dont les données de conversation de teams pour les utilisateurs locaux sont disponibles pour la recherche, l’aperçu et l’exportation.
  
![Stockage informatique pour les utilisateurs locaux de Microsoft teams](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
En plus de cette nouvelle fonctionnalité, vous pouvez toujours utiliser la recherche de contenu pour rechercher, prévisualiser et exporter du contenu de teams dans le site SharePoint en nuage et la boîte aux lettres Exchange associée à chaque équipe Microsoft Team et 1xN teams données de conversation dans la boîte aux lettres Exchange Online pour utilisateurs en nuage.

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature"></a>Classement d’une demande auprès du support Microsoft pour activer cette fonctionnalité

Vous devez classer une demande auprès du support Microsoft pour permettre à votre organisation d’utiliser l’interface utilisateur graphique dans le centre de sécurité & conformité afin de rechercher des données de conversation teams dans les boîtes aux lettres en nuage pour les utilisateurs locaux. Cette fonctionnalité est disponible dans le centre de sécurité & PowerShell Center. Vous n’êtes pas obligé de soumettre une demande de support pour utiliser PowerShell pour rechercher des données de conversation teams pour les utilisateurs locaux. 
  
Incluez les informations suivantes lorsque vous soumettez la demande au support Microsoft:
  
- Nom de domaine par défaut de votre organisation Office 365.
    
- Le nom du client et l’ID de client de votre organisation Office 365. Vous pouvez les trouver dans le portail Azure Active Directory (sous **gérer** \> les **Propriétés**). Voir [trouver votre ID de client Office 365](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b).
    
- Le titre ou la description du but de la demande de support: «activer la recherche de contenu d’application pour les utilisateurs locaux». Cela permet d’acheminer la demande vers l’équipe d’ingénierie eDiscovery d’Office 365 qui mettra en œuvre la demande. 
    
Une fois le changement d’ingénierie effectué, le support Microsoft vous enverra une estimation de la date de déploiement. Le processus de déploiement prend généralement entre 2 et 3 semaines après l’envoi de la demande de support. 
  
### <a name="what-happens-after-this-feature-is-enabled"></a>Que se passe-t-il après l’activation de cette fonctionnalité?

Une fois que cette fonctionnalité est déployée dans votre organisation Office 365, les modifications suivantes sont apportées lors de la recherche de contenu et dans les recherches associées à un cas eDiscovery dans le centre de sécurité & Compliance Center:
  
- La case à cocher **Ajouter le contenu de l’application Office pour les utilisateurs locaux** est ajoutée sous l' **emplacement** de la recherche de contenu. 
    
    ![La case à cocher «Ajouter le contenu d’une application Office pour les utilisateurs locaux» est ajoutée à l’interface utilisateur de recherche de contenu](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- Les utilisateurs locaux sont affichés dans le sélecteur d’emplacements de contenu, qui vous permet de sélectionner des boîtes aux lettres utilisateur à rechercher. 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a>Recherche de contenu de conversation de teams dans des boîtes aux lettres en nuage pour les utilisateurs locaux

Une fois que la fonctionnalité est activée, vous pouvez utiliser la recherche de contenu dans le centre de sécurité & conformité pour rechercher des données de conversation teams dans les boîtes aux lettres en nuage pour les utilisateurs locaux. 
  
1. Dans le centre de sécurité & conformité, accédez à recherche de **contenu** de **recherche** \>
    
2. Sur la page **recherche** , cliquez ![sur Ajouter](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) une icône **nouvelle recherche**.
    
    Comme expliqué précédemment, la case à cocher **Ajouter le contenu de l’application Office pour les utilisateurs locaux** s’affiche sous **emplacements**. Elle est sélectionnée par défaut.
    
3. Créez la requête de mot clé et ajoutez des conditions à la requête de recherche si nécessaire. Pour rechercher uniquement les données de conversation d’équipe, vous pouvez ajouter la requête suivante dans la zone **Mots clés** : 
    
    ```
    kind:im
    ``` 

4. À ce stade, vous pouvez choisir l’une des options suivantes sous **locations**:
    
    - **Tous les emplacements:** Sélectionnez cette option pour rechercher les boîtes aux lettres de tous les utilisateurs de votre organisation. Lorsque la case est cochée, toutes les boîtes aux lettres en nuage pour les utilisateurs locaux seront également recherchées. 
    
    - **Emplacements spécifiques:** Sélectionnez cette option, puis cliquez sur **modifier** \> : choisir un utilisateur, des groupes ou des équipes pour effectuer des recherches dans des boîtes aux lettres spécifiques. Comme expliqué précédemment, le sélecteur d’emplacements vous permet de rechercher des utilisateurs locaux. 
    
5. Enregistrez et exécutez la recherche. Tous les résultats de recherche provenant des boîtes aux lettres en nuage pour les utilisateurs locaux peuvent être prévisualisés comme n’importe quel autre résultat de recherche. Vous pouvez également exporter les résultats de la recherche (y compris les données de conversation Teams) vers un fichier PST. Pour plus d’informations, reportez-vous aux rubriques suivantes : 
    
    - [Create a search](content-search.md#create-a-search)
    
    - [Preview search results](content-search.md#preview-search-results)
    
    - [Exporter les résultats de la recherche de contenu](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a>Utilisation de PowerShell pour rechercher des données de conversation de teams dans des boîtes aux lettres en nuage pour les utilisateurs locaux

Vous pouvez utiliser les cmdlets **New-ComplianceSearch** et **Set-ComplianceSearch** dans le centre de sécurité & Compliance Center PowerShell pour effectuer des recherches dans la boîte aux lettres en nuage pour les utilisateurs locaux. Comme expliqué précédemment, vous n’avez pas besoin de soumettre une demande de support pour utiliser PowerShell pour rechercher des données de conversation teams pour les utilisateurs locaux. 
  
1. [Connectez-vous à la sécurité & Centre de conformité PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
    
2. Exécutez la commande PowerShell suivante pour créer une recherche de contenu qui recherche dans les boîtes aux lettres en nuage des utilisateurs locaux.
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    Le paramètre *IncludeUserAppContent* est utilisé pour spécifier la boîte aux lettres en nuage pour le ou les utilisateurs spécifiés par le paramètre *exchangelocation permet* . Le *AllowNotFoundExchangeLocationsEnabled* autorise les boîtes aux lettres en nuage pour les utilisateurs locaux. Lorsque vous utilisez la `$true` valeur de ce paramètre, la recherche n’essaie pas de valider l’existence de la boîte aux lettres avant de l’exécuter. Cela est nécessaire pour effectuer des recherches dans les boîtes aux lettres en nuage pour les utilisateurs locaux, car ces types de boîtes aux lettres ne sont pas résolus comme des boîtes aux lettres normales. 
    
    L’exemple suivant recherche les conversations de Teams (c’est-à-dire les messages instantanés) qui contiennent le mot clé «Redstone» dans la boîte aux lettres en nuage d’Sara Davis, qui est un utilisateur local de l’organisation contoso.
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   Après avoir créé une recherche, veillez à utiliser la cmdlet **Start-ComplianceSearch** pour exécuter la recherche. 
  
Pour plus d’informations sur ces applets de commande, voir:
  
- [New-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [Set-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [Start-ComplianceSearch](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a>Problèmes connus

- Actuellement, vous pouvez uniquement Rechercher, prévisualiser et exporter du contenu dans des boîtes aux lettres en nuage pour les utilisateurs locaux. Le fait de placer une boîte aux lettres en nuage pour un utilisateur local sur une conservation associée à un cas eDiscovery ou de l’affecter à une stratégie de rétention Office 365 n’est pas pris en charge. 
    
- Le sélecteur d’emplacement de contenu pour les conservations eDiscovery affiche les utilisateurs locaux et vous permet de les sélectionner. Toutefois, comme expliqué précédemment, la conservation ne sera pas appliquée à l’utilisateur local.
    
## <a name="frequently-asked-questions"></a>Questions fréquemment posées

 **Où se trouvent les boîtes aux lettres en nuage pour les utilisateurs locaux situés?**
  
Les boîtes aux lettres en nuage sont créées et stockées dans le même centre de informations que votre organisation Office 365. 
  
 **Existe-t-il d’autres autres exigences que la soumission d’une demande de support?**
  
 Comme expliqué précédemment, les identités des utilisateurs avec des boîtes aux lettres local doivent être synchronisées avec votre organisation en nuage afin qu’un compte d’utilisateur de messagerie correspondant soit créé pour chaque compte d’utilisateur local dans Office 365. Votre organisation doit également avoir un abonnement Office 365 Enterprise, tel qu’un abonnement Office 365 Enterprise E1, E3 ou E5. 
  
 **Y a-t-il un risque de perdre les données de conversation de teams si la boîte aux lettres locale de l’utilisateur est migrée vers le nuage?**
  
Non. Lorsque vous migrez la boîte aux lettres principale d’un utilisateur local vers le Cloud, les données de conversation de teams pour cet utilisateur seront migrées vers leur nouvelle boîte aux lettres principale en nuage.
  
 **Puis-je Appliquer une conservation eDiscovery ou des stratégies de rétention Office 365 à des utilisateurs locaux?**
  
Non.
  
 **La recherche de contenu CAN peut-elle trouver des conversations d’ancienne teams pour les utilisateurs locaux avant que mon organisation ait soumis la demande d’activation de cette fonctionnalité?**
  
Microsoft a commencé à stocker les données de conversation de teams pour les utilisateurs locaux le 31 janvier 2018. Par conséquent, si l’identité d’un utilisateur de teams sur site a été synchronisée entre Active Directory et Azure Active Directory depuis cette date, les données de conversation de teams sont stockées dans une boîte aux lettres en nuage et sont consultables à l’aide de la recherche de contenu. Microsoft travaille également sur le stockage des données de conversation teams depuis le 31 janvier 2018 dans les boîtes aux lettres en nuage pour les utilisateurs locaux. Pour plus d’informations, reportez-vous bientôt.

 * * Les utilisateurs locaux ont-ils besoin d’une licence pour stocker les données de conversation des équipes dans une boîte aux lettres en nuage? 
  
Oui. Pour stocker les données de conversation des équipes pour un utilisateur local dans une boîte aux lettres en nuage, une licence Microsoft teams et une licence Exchange Online plan doivent être attribuées à l’utilisateur dans Office 365 (ou Microsoft 365).
