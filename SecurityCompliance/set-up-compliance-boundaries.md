---
title: Configurer les limites de conformité pour les enquêtes eDiscovery dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: Utilisez des limites de conformité pour créer des limites logiques au sein d’une organisation Office 365 qui contrôlent les emplacements de contenu utilisateur qu’un gestionnaire eDiscovery peut rechercher. Les limites de conformité utilisent le filtrage des autorisations de recherche (également appelé filtres de sécurité de conformité) pour contrôler les boîtes aux lettres, les sites SharePoint et les comptes OneDrive pouvant être recherchés par des utilisateurs spécifiques.
ms.openlocfilehash: abca7624cb5aa97c85686fc570a653c88b6b8b6b
ms.sourcegitcommit: d55dab629ce1f8431b8370afde4131498dfc7471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2019
ms.locfileid: "36675445"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a>Configurer les limites de conformité pour les enquêtes eDiscovery dans Office 365

Les limites de conformité créent des limites logiques au sein d’une organisation Office 365 qui contrôlent les emplacements de contenu utilisateur (par exemple, les boîtes aux lettres, les sites SharePoint et les comptes OneDrive) que les gestionnaires eDiscovery peuvent rechercher. En outre, les limites de conformité contrôlent qui peut accéder à des cas eDiscovery utilisés pour gérer les enquêtes juridiques, les ressources humaines ou d’autres enquêtes au sein de votre organisation. Il est souvent nécessaire de respecter les frontières de conformité pour les sociétés multinationales qui doivent respecter des organisations et des réglementations géographiques, qui sont souvent divisées en différents organismes. Dans Office 365, les limites de conformité vous aident à répondre à ces exigences lors de la recherche de contenu et de la gestion des enquêtes avec des cas eDiscovery.
  
Nous utilisons l’exemple de l’illustration suivante pour expliquer le fonctionnement des limites de conformité.
  
![Les limites de conformité consistent en des filtres d’autorisations de recherche qui contrôlent l’accès aux agences et aux groupes de rôles d’administrateur qui contrôlent l’accès aux cas eDiscovery](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
Dans cet exemple, contoso LTD est une organisation Office 365 qui se compose de deux filiales, Fourth Coffee et Coho Winery. Pour les entreprises, les responsables et les enquêteurs eDiscovery peuvent uniquement effectuer des recherches dans les boîtes aux lettres Exchange, les comptes OneDrive et les sites SharePoint de leur Agence. En outre, les gestionnaires eDiscovery et les investigateurs peuvent uniquement voir les cas eDiscovery dans leur Agence et ils peuvent uniquement accéder aux cas dont ils sont membres. Voici comment les limites de conformité répondent à ces exigences.
  
- La fonctionnalité de filtrage des autorisations de recherche dans la recherche de contenu contrôle les emplacements de contenu que les responsables eDiscovery et les enquêteurs peuvent rechercher. Cela signifie que les responsables de la découverte électronique et les investigateurs de la quatrième succursale peuvent uniquement Rechercher des emplacements de contenu dans la filiale Fourth Coffee. La même restriction s’applique à la filiale Coho Winery.
    
    Les groupes de rôles contrôlent les personnes qui peuvent voir les cas eDiscovery dans le centre de sécurité & conformité. Cela signifie que les responsables et les enquêteurs eDiscovery ne peuvent voir que les cas eDiscovery dans leur Agence.
    
- Les groupes de rôles déterminent également qui peut assigner des membres à un cas eDiscovery. Cela signifie que les responsables et les investigations eDiscovery peuvent uniquement affecter des membres aux cas dont ils sont eux-mêmes membres.
    
Voici le processus de configuration des limites de conformité:
  
[Étape 1: identifier un attribut d’utilisateur pour définir vos agences](#step-1-identify-a-user-attribute-to-define-your-agencies)

[Étape 2: classer une demande auprès du support Microsoft pour synchroniser l’attribut utilisateur avec les comptes OneDrive](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[Étape 3: créer un groupe de rôles pour chaque agence](#step-3-create-a-role-group-for-each-agency)

[Étape 4: créer un filtre d’autorisations de recherche pour appliquer la limite de conformité](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[Étape 5: créer un cas de découverte électronique pour les enquêtes intra-organismes](#step-5-create-an-ediscovery-case-for-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a>Étape 1: identifier un attribut d’utilisateur pour définir vos agences

La première étape consiste à choisir un attribut Azure Active Directory à utiliser qui définira vos agences. Cet attribut est utilisé pour créer le filtre d’autorisations de recherche qui limite un gestionnaire de découverte électronique pour rechercher uniquement les emplacements de contenu des utilisateurs auxquels une valeur spécifique est attribuée pour cet attribut. Par exemple, supposons que Contoso décide d’utiliser l’attribut **Department** . La valeur de cet attribut pour les utilisateurs de la filiale Fourth Coffee serait `FourthCoffee` et la valeur pour les utilisateurs de la filiale Coho Winery serait `CohoWinery`. À l’étape 4, vous utilisez `attribute:value` cette paire (par exemple, *Department: fourthcoffee*) pour limiter les emplacements de contenu utilisateur que les gestionnaires eDiscovery peuvent rechercher. 
  
Voici une liste d’attributs d’utilisateur Azure Active Directory que vous pouvez utiliser pour les limites de conformité:
  
- Company
    
- CustomAttribute1 — CustomAttribute15
    
- Service
    
- Bureau

- C (code du pays à deux lettres)
    
Bien que d’autres attributs utilisateur soient disponibles, en particulier pour les boîtes aux lettres Exchange, les attributs répertoriés ci-dessus sont les seuls ceux actuellement pris en charge par OneDrive.
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a>Étape 2: classer une demande auprès du support Microsoft pour synchroniser l’attribut utilisateur avec les comptes OneDrive

L’étape suivante consiste à classer une demande auprès du support Microsoft pour synchroniser l’attribut Azure Active Directory que vous avez choisi à l’étape 1 sur tous les comptes OneDrive de votre organisation. Une fois cette synchronisation effectuée, l’attribut (et sa valeur) que vous avez choisi à l’étape 1 seront mappés à une propriété gérée masquée dans SharePoint nommé `ComplianceAttribute`. Utilisez cet attribut pour créer le filtre d’autorisations de recherche pour OneDrive à l’étape 4.
  
Incluez les informations suivantes lorsque vous soumettez la demande au support Microsoft:
  
- Le nom de domaine par défaut de votre organisation Office 365
    
- Nom de l’attribut Azure Active Directory (à partir de l’étape 1)
    
- Le titre ou la description de l’objet de la demande de support: «activer la synchronisation OneDrive entreprise avec Azure Active Directory pour les filtres de sécurité de conformité». Cela permet d’acheminer la demande vers l’équipe d’ingénierie eDiscovery d’Office 365 qui mettra en œuvre la demande.
    
Une fois le changement d’ingénierie effectué et l’attribut synchronisé sur OneDrive, le support Microsoft vous enverra le numéro de build dans lequel la modification a été apportée, ainsi qu’une date de déploiement estimée. Le processus de déploiement prend généralement entre 4 et 6 semaines après l’envoi de la demande de support.
  
 **Important:** Vous pouvez effectuer les étapes 3 à 5 avant le déploiement de la modification. Toutefois, l’exécution de recherches de contenu ne renverra pas les documents à partir des sites OneDrive spécifiés dans le filtre d’autorisations de recherche tant que la modification n’a pas été déployée. 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a>Étape 3: créer un groupe de rôles pour chaque agence

L’étape suivante consiste à créer les groupes de rôles dans le centre de sécurité & conformité qui s’alignera avec vos agences. Nous vous recommandons de créer un groupe de rôles en copiant le groupe de gestionnaires eDiscovery intégré, en ajoutant les membres appropriés et en supprimant les rôles qui peuvent ne pas être applicables à vos besoins. Pour plus d’informations sur les rôles liés à la découverte électronique, consultez [la rubrique Assign eDiscovery Permissions in the Office 365 Security & Compliance Center](assign-ediscovery-permissions.md).
  
Pour créer les groupes de rôles, accédez à la page **autorisations** dans le centre de sécurité & conformité et créez un groupe de rôles pour chaque équipe de chaque agence qui utilisera des limites de conformité et des cas eDiscovery pour gérer les enquêtes. 
  
À l’aide du scénario de limites de conformité contoso, quatre groupes de rôles doivent être créés et les membres appropriés ajoutés à chacun d’eux.
  
- Gestionnaires eDiscovery Fourth Coffee
    
- Quatrièmes enquêteurs pour les cafés
    
- Gestionnaires de découverte électronique Coho Winery
    
- Investigateurs Coho Winery
  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a>Étape 4: créer un filtre d’autorisations de recherche pour appliquer la limite de conformité

Une fois que vous avez créé des groupes de rôles pour chaque agence, l’étape suivante consiste à créer les filtres d’autorisations de recherche qui associent chaque groupe de rôles à son agence spécifique et définit la limite de conformité proprement dite. Vous devez créer un filtre d’autorisations de recherche pour chaque agence. Pour plus d’informations sur la création de filtres d’autorisations de sécurité, consultez la rubrique [configurer le filtrage des autorisations pour la recherche de contenu](permissions-filtering-for-content-search.md).
  
Voici la syntaxe utilisée pour créer un filtre d’autorisations de recherche utilisé pour les limites de conformité.

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<ComplianceAttribute>  -eq '<AttributeVale> '", "Site_<ComplianceAttribute>  -eq '<AttributeValue>' -or Site_Path -like '<SharePointURL>*'" -Action <Action >
```
  
Voici une description de chaque paramètre de la commande:
  
-  `FilterName`: Spécifie le nom du filtre. Utilisez un nom qui décrit ou identifie l’Agence dans laquelle le filtre est utilisé. 
    
-  `Users`: Spécifie les utilisateurs ou groupes auxquels ce filtre est appliqué aux actions de recherche de contenu qu’ils effectuent. Pour les limites de conformité, ce paramètre spécifie les groupes de rôles (que vous avez créés à l’étape 3) de l’organisme pour lequel vous créez le filtre. Remarque Il s’agit d’un paramètre à valeurs multiples qui vous permet d’inclure un ou plusieurs groupes de rôles, séparés par des virgules. 
    
-  `Filters`: Spécifie les critères de recherche pour le filtre. Pour les limites de conformité, définissez les filtres suivants. Chacune d’entre elles s’applique à un emplacement de contenu. 
    
    -  `Mailbox`: Spécifie les boîtes aux lettres dans lesquelles les groupes de `Users` rôles définis dans le paramètre peuvent effectuer des recherches. Pour les limites de conformité, *ComplianceAttribute* est le même attribut que celui que vous avez identifié à l’étape 1 et *AttributeValue* spécifie l’Agence. Ce filtre permet aux membres du groupe de rôles de rechercher uniquement les boîtes aux lettres d’une agence spécifique; par exemple, `"Mailbox_Department -eq 'FourthCoffee'"`. 
    
    -  `Site`: Spécifie les comptes OneDrive que les groupes de rôles définis `Users` dans le paramètre peuvent rechercher. Pour le filtre OneDrive, utilisez la chaîne `ComplianceAttribute`réelle. Correspond au même attribut que celui que vous avez identifié à l’étape 1 et qui est synchronisé avec les comptes OneDrive à la suite de la demande de support que vous avez envoyée à l’étape 2;  *AttributeValue* spécifie l’Agence. Ce filtre permet aux membres du groupe de rôles de rechercher uniquement les comptes OneDrive d’une agence spécifique; par exemple, `"Site_ComplianceAttribute -eq 'FourthCoffee'"`.
    
    -  `Site_Path`: Spécifie les sites SharePoint que les groupes de rôles définis `Users` dans le paramètre peuvent rechercher. Le *SharePointURL* spécifie les sites de l’Agence que les membres du groupe de rôles peuvent rechercher; par exemple, `"Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"` Notez que `Site` les `Site_Path` filtres et sont connectés par un opérateur **-ou** .
    
     > [!NOTE]
     > La syntaxe du `Filters` paramètre inclut une *liste de filtres*. Une liste de filtres est un filtre qui inclut un filtre de boîte aux lettres et un filtre de site séparés par une virgule. Dans l’exemple précédent, Notez qu’une virgule sépare **Mailbox_ComplianceAttribute** et **Site_ComplianceAttribute**: `-Filters "Mailbox_<ComplianceAttribute>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq '<AttributeValue>' -or Site_Path -like '<SharePointURL>*'"`. Lorsque ce filtre est traité lors de l’exécution d’une recherche de contenu, deux filtres d’autorisations de recherche sont créés à partir de la liste Filtres: un filtre de boîte aux lettres et un filtre de site. Une alternative à l’utilisation d’une liste de filtres consiste à créer deux filtres d’autorisations de recherche distincts pour chaque agence: un filtre d’autorisations de recherche pour l’attribut de boîte aux lettres et un filtre pour les attributs de site. Dans les deux cas, les résultats seront identiques. L’utilisation d’une liste de filtres ou la création de filtres d’autorisations de recherche distincts est une question de préférence.

-  `Action`: Spécifie le type d’action de recherche de conformité auquel le filtre est appliqué. Par exemple, `-Action Search` applique uniquement le filtre lorsque les membres du groupe de rôles défini dans le `Users` paramètre exécutent une recherche de contenu. Dans ce cas, le filtre ne doit pas être appliqué lors de l’exportation des résultats de la recherche. Pour les limites de conformité `-Action All` , utilisez de sorte que le filtre s’applique à toutes les actions de recherche. 
    
    Pour obtenir la liste des actions de recherche de contenu, voir la section «New-ComplianceSecurityFilter» dans la rubrique [configurer le filtrage des autorisations pour la recherche de contenu](permissions-filtering-for-content-search.md#new-compliancesecurityfilter).

Voici des exemples de deux filtres d’autorisations de recherche qui seraient créés pour prendre en charge le scénario de limites de conformité contoso. Ces deux exemples incluent une liste de filtres séparés par des virgules, dans laquelle les filtres de boîte aux lettres et de site sont inclus dans le même filtre des autorisations de recherche et sont séparés par une virgule.
  
 **Fourth Coffee**

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 **Coho Winery**

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-intra-agency-investigations"></a>Étape 5: créer un cas eDiscovery pour les enquêtes intra-Agence

La dernière étape consiste à créer un cas eDiscovery dans le centre de sécurité & conformité, puis à ajouter le groupe de rôles que vous avez créé à l’étape 3 en tant que membre du cas. Il en résulte deux caractéristiques importantes de l’utilisation des limites de conformité:
  
- Seuls les membres du groupe de rôles ajouté à la casse seront en mesure de voir et d’y accéder dans le centre de sécurité & conformité. Par exemple, si le quatrième groupe de rôles enquêteur de café est le seul membre d’un cas, les membres du quatrième groupe de rôles gestionnaires eDiscovery (ou membres de n’importe quel autre groupe de rôles) ne pourront pas voir ou accéder à l’incident.
    
- Quand un membre du groupe de rôles affecté à un cas exécute une recherche associée à l’incident, il pourra uniquement effectuer des recherches dans les emplacements de contenu au sein de son agence (qui est défini par le filtre d’autorisations de recherche que vous avez créé à l’étape 4.)


Pour créer un cas et affecter des membres:
    
1. Accédez à la page de **découverte électronique** dans le centre de sécurité & conformité et créez un cas. 
    
2. Dans la liste des cas de découverte électronique, cliquez sur le nom de la demande de devis que vous avez créée.
    
3. Dans la page de menu contextuel **gérer ce cas** , sous gérer les ![groupes de](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **rôles**, cliquez sur Ajouter une icône **Ajouter**.
    
    ![Ajouter un groupe de rôles en tant que membre d’un cas de découverte électronique](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. Dans la liste des groupes de rôles, sélectionnez l’un des groupes de rôles que vous avez créés à l’étape 3, puis cliquez sur **Ajouter**.
    
5. Cliquez sur **Enregistrer** dans le menu volant **gérer cet incident** pour enregistrer la modification. 

## <a name="compliance-boundary-limitations"></a>Limitations des limites de conformité

Gardez les limites suivantes à l’esprit lors de la gestion des cas eDiscovery et des investigations qui utilisent des limites de conformité.
  
- Lors de la création et de l’exécution d’une recherche de contenu, vous pouvez sélectionner des emplacements de contenu qui se trouvent en dehors de votre Agence. Toutefois, en raison du filtre des autorisations de recherche, le contenu de ces emplacements ne sera pas inclus dans les résultats de la recherche.
    
- Les limites de conformité ne s’appliquent pas aux conservations dans les cas eDiscovery. Cela signifie qu’un gestionnaire de découverte électronique dans une Agence peut placer un utilisateur dans une autre agence en attente. Toutefois, la limite de conformité est appliquée si le gestionnaire eDiscovery recherche les emplacements de contenu de l’utilisateur qui a été placé en conservation. Cela signifie que le gestionnaire eDiscovery ne pourra pas rechercher les emplacements de contenu de l’utilisateur, même s’il était en mesure de mettre l’utilisateur en attente.
    
    En outre, les statistiques de conservation s’appliquent uniquement aux emplacements de contenu de l’Agence.
    
- Les filtres d’autorisations de recherche ne sont pas appliqués aux dossiers publics Exchange.

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a>Recherche et exportation de contenu dans des environnements multigéographiques

Les filtres d’autorisations de recherche vous permettent également de contrôler où le contenu est acheminé pour l’exportation et sur lequel le centre de données peut être recherché lors de la recherche d’emplacements de contenu dans un [environnement multi-géo SharePoint](https://go.microsoft.com/fwlink/?linkid=860840).
  
- **Exporter les résultats de la recherche:** Vous pouvez exporter les résultats de la recherche à partir de boîtes aux lettres Exchange, de sites SharePoint et de comptes OneDrive à partir d’un centre de donnée spécifique. Cela signifie que vous pouvez spécifier l’emplacement de centre de contenu à partir duquel les résultats de la recherche seront exportés.

    Utilisez le paramètre **Region** pour les cmdlets **New-ComplianceSecurityFilter** ou **Set-ComplianceSecurityFilter** pour créer ou modifier le centre de réacheminement de l’exportation.
  
    |**Valeur du paramètre**|**Emplacement du centre de**|
    |:-----|:-----|
    |NAM  <br/> |Amérique du Nord (les centres de déplacement sont aux États-Unis)  <br/> |
    |EUR  <br/> |Europe  <br/> |
    |APC  <br/> |Asie-Pacifique  <br/> |
    |CAN <br/> |Canada|
    |||
    
- **Recherches de contenu de routage:** Vous pouvez acheminer les recherches de contenu de sites SharePoint et de comptes OneDrive vers un centre de données satellite. Cela signifie que vous pouvez spécifier l’emplacement du centre de recherche dans lequel les recherches seront exécutées.
    
    Utilisez les valeurs suivantes pour les valeurs du paramètre **Region** afin de contrôler le centre de données dans lequel les recherches de contenu s’exécuteront lors de la recherche de sites SharePoint et d’emplacements OneDrive. 
  
    |**Valeur du paramètre**|**Emplacements de routage de centre de distribution pour SharePoint**|
    |:-----|:-----|
    |NAM  <br/> |Contacter  <br/> |
    |EUR  <br/> |Europe  <br/> |
    |APC  <br/> |Asie-Pacifique  <br/> |
    |CAN  <br/> |Contacter  <br/> |
    |AUS  <br/> |Asie-Pacifique  <br/> |
    |KOR  <br/> |Centre de centre par défaut de l’Organisation  <br/> |
    |GBR  <br/> |Europe  <br/> |
    |JPN  <br/> |Asie-Pacifique  <br/> |
    |IND  <br/> |Asie-Pacifique  <br/> |
    |BARRÉ  <br/> |Contacter  <br/> |
    |||

   Si vous ne spécifiez pas le paramètre **Region** pour un filtre d’autorisations de recherche, la région SharePoint par défaut de l’organisation sera recherchée, puis les résultats de la recherche sont exportés vers le centre de contenu le plus proche.

> [!TIP]
> Pour simplifier le concept, le paramètre **Region** contrôle le centre de données qui permet de rechercher du contenu dans SharePoint et OneDrive. Cela ne s’applique pas à la recherche de contenu dans Exchange car les recherches de contenu Exchange ne sont pas liées par l’emplacement géographique des centres de données. De même, la valeur du paramètre **Region** peut également dicter le centre de contenu dans lequel les exportations sont acheminées. Il est souvent nécessaire de contrôler le déplacement des données entre des cartes géographiques.<br/><br/>Si vous utilisez Advanced eDiscovery, la recherche de contenu dans SharePoint et OneDrive n’est pas liée par l’emplacement géographique des centres de données. Pour plus d’informations sur Advanced eDiscovery, reportez-vous à [la rubrique Overview of the Advanced eDiscovery solution in Microsoft 365](compliance20/overview-ediscovery-20.md).

Voici des exemples d’utilisation du paramètre **Region** lors de la création de filtres d’autorisation de recherche pour les limites de conformité. Cela suppose que la filiale Fourth Coffee soit située en Amérique du Nord et que Coho Winery se trouve en Europe. 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
Gardez les points suivants à l’esprit lors de la recherche et de l’exportation de contenu dans des environnements multigéographiques.
  
- Le paramètre **Region** ne contrôle pas les recherches de boîtes aux lettres Exchange. Tous les centres de données sont recherchés lorsque vous effectuez des recherches dans des boîtes aux lettres. Pour limiter l’étendue des boîtes aux lettres Exchange pouvant faire l’objet d’une **** recherche, utilisez le paramètre Filters lors de la création ou de la modification d’un filtre d’autorisations de recherche. 
    
- S’il est nécessaire pour un gestionnaire eDiscovery d’effectuer des recherches dans plusieurs régions SharePoint, vous devez créer un compte d’utilisateur différent pour ce gestionnaire eDiscovery qui peut être utilisé dans le filtre d’autorisations de recherche pour spécifier la région dans laquelle les sites SharePoint ou Les comptes OneDrive sont situés. Pour plus d’informations sur la configuration de ces paramètres, consultez la section «recherche de contenu dans un environnement multi-géo SharePoint» dans [recherche de contenu dans Office 365](content-search.md#searching-for-content-in-a-sharepoint-multi-geo-environment).
    
- Lors de la recherche de contenu dans SharePoint et OneDrive, le paramètre **Region** dirige les recherches vers l’emplacement principal ou satellite où le gestionnaire eDiscovery effectuera des investigations eDiscovery. Si un gestionnaire eDiscovery recherche des sites SharePoint et OneDrive en dehors de la région spécifiée dans le filtre des autorisations de recherche, aucun résultat de recherche n’est renvoyé. 
    
- Lors de l’exportation des résultats de recherche, le contenu de tous les emplacements de contenu (y compris Exchange, Skype entreprise, SharePoint, OneDrive et d’autres services Office 365 que vous pouvez rechercher à l’aide de l’outil de recherche de contenu) est téléchargé vers l’emplacement de stockage Azure dans Centre de donnée spécifié par le paramètre **Region** . Cela permet aux organisations de respecter la conformité en ne permettant pas d’exporter du contenu à travers les bordures contrôlées. Si aucune région n’est spécifiée dans le filtre d’autorisations de recherche, le contenu est téléchargé vers la région par défaut de l’organisation. 
    
- Vous pouvez modifier un filtre d’autorisations de recherche existant pour ajouter ou modifier la région en exécutant la commande suivante:

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a>Questions fréquemment posées

 **Qui peut créer et gérer des filtres d’autorisations de recherche (à l’aide des cmdlets New-ComplianceSecurityFilter et Set-ComplianceSecurityFilter)?**
  
Pour créer, afficher et modifier des filtres d’autorisations de recherche, vous devez être membre du groupe de rôles gestion de l’organisation dans le centre de sécurité & conformité.
  
 **Si un gestionnaire eDiscovery est affecté à plusieurs groupes de rôles qui s’étendent sur plusieurs agences, comment puis-je rechercher du contenu dans une ou l’autre.**
  
Le gestionnaire eDiscovery peut ajouter des paramètres à leur requête de recherche pour limiter la recherche à une agence spécifique. Par exemple, si une organisation a spécifié la propriété **CustomAttribute10** pour différencier les agences, elles peuvent ajouter les éléments suivants à leur requête de recherche pour rechercher des boîtes aux lettres et des `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`comptes OneDrive dans une agence spécifique:.
  
 **Que se passe-t-il si la valeur de l’attribut utilisé comme attribut de conformité dans un filtre d’autorisations de recherche est modifiée?**
  
Il faut trois jours pour qu’un filtre d’autorisations de recherche applique la limite de conformité si la valeur de l’attribut utilisé dans le filtre est modifiée. Par exemple, dans le scénario contoso, imaginons qu’un utilisateur de la quatrième Agence café est transféré à l’Agence Coho Winery. Par conséquent, la valeur de l’attribut **Department** de l’objet User est modifiée de *fourthcoffee* à *cohowinery*. Dans ce cas, la découverte électronique et les investisseurs de quatrième café obtiendront des résultats de recherche pour cet utilisateur pendant trois jours après la modification de l’attribut. De même, il faut trois jours avant que les gestionnaires eDiscovery et les investigations de Coho Winery obtiennent des résultats de recherche pour l’utilisateur. 
  
 **Un gestionnaire eDiscovery peut-il voir le contenu de deux limites de conformité distinctes?**
  
Oui. Pour ce faire, vous pouvez ajouter l’utilisateur à des groupes de rôles disposant d’une visibilité aux deux agences.
  
 **Les filtres d’autorisations de recherche fonctionnent-ils pour les conservations de cas eDiscovery, les stratégies de rétention Office 365 ou DLP?**
  
Non, pas pour le moment.
  
 **Si je spécifie une région pour contrôler l’emplacement d’exportation du contenu, mais je n’ai pas d’organisation SharePoint dans cette région, puis-je toujours effectuer des recherches dans SharePoint?**
  
Si la région spécifiée dans le filtre d’autorisations de recherche n’existe pas dans votre organisation, la zone par défaut sera recherchée.
  
 **Quel est le nombre maximal de filtres d’autorisations de recherche pouvant être créés dans une organisation?**
  
Il n’y a pas de limite au nombre de filtres d’autorisations de recherche pouvant être créés dans une organisation. Toutefois, les performances de recherche seront affectées lorsqu’il y aura plus de 100 filtres d’autorisations de recherche. Pour conserver le plus petit nombre de filtres d’autorisations de recherche dans votre organisation, créez des filtres qui combinent les règles pour Exchange, SharePoint et OneDrive dans un seul filtre des autorisations de recherche lorsque cela est possible.
