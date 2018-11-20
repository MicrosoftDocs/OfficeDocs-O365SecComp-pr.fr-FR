---
title: Configurer les limites de conformité pour les enquêtes eDiscovery dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 1b45c82f-26c8-44fb-9f3b-b45436fe2271
description: Limites de conformité permet de créer des limites logiques au sein d’une organisation Office 365 qui contrôlent les emplacements de contenu utilisateur qui permet de rechercher un gestionnaire de découverte électronique. Limites de conformité utilisent des autorisations de recherche (également appelé conformité sécurité filtres) de filtrage pour contrôler les boîtes aux lettres, les sites SharePoint et OneDrive comptes pouvant être explorées par des utilisateurs spécifiques.
ms.openlocfilehash: 2bebd29fa7701ba07aae7170142263aeaec5569e
ms.sourcegitcommit: c7264f3a6a97f1ff544544e2c722e7825e265fa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2018
ms.locfileid: "26299238"
---
# <a name="set-up-compliance-boundaries-for-ediscovery-investigations-in-office-365"></a>Configurer les limites de conformité pour les enquêtes eDiscovery dans Office 365

Limites de conformité créer des limites logiques au sein d’une organisation Office 365 qui contrôlent les emplacements de contenu utilisateur (telles que les boîtes aux lettres, les sites SharePoint et comptes OneDrive) qui peuvent de rechercher des gestionnaires de découverte électronique. En outre, la conformité des limites contrôler qui peut accéder cas eDiscovery permet de gérer le département juridique, des ressources humaines ou autres enquêtes au sein de votre organisation. Les limites de la conformité est souvent nécessaire pour les entreprises nations multiples doivent respecter la réglementation et les intrus géographiques et pour le secteur public, qui est souvent répartis en différents organismes. Dans Office 365, aide des limites de conformité vous respectez ces exigences lors de l’exécution de contenu recherches et la gestion des enquêtes avec cas eDiscovery.
  
Nous allons utiliser l’exemple dans l’illustration suivante afin d’expliquer comment fonctionnent les limites de conformité.
  
![Limites de conformité se composent des filtres de recherche des autorisations qui contrôlent l’accès aux cas eDisocovery par les groupes de contrôler l’accès aux agences et les rôles d’administration](media/5c206cc8-a6eb-4d6b-a3a5-21e158791f9a.png)
  
Dans cet exemple, Contoso LTD est une organisation Office 365 qui se compose de deux filiales, Fourth Coffee et Coho Winery. L’entreprise nécessite qu’investigateurs et gestionnaires de découverte électronique peuvent uniquement rechercher les boîtes aux lettres Exchange, les comptes OneDrive et sites SharePoint dans leur agence. En outre, les gestionnaires de découverte électronique et investigateurs ne pouvant voir cas eDiscovery dans les dans leur agence, et ils peuvent accéder uniquement les cas ils sont membre. Voici comment les limites de conformité répondre à ces exigences.
  
- Les autorisations de recherche les emplacements de contenu investigateurs et les gestionnaires de découverte peuvent rechercher de fonctionnalité dans les contrôles de recherche de contenu de filtrage. Cela signifie que les gestionnaires de découverte électronique et investigateurs dans l’Agence Fourth Coffee peuvent uniquement rechercher des emplacements de contenu de la filiale Fourth Coffee. La même restriction s’applique à la filiale de Coho Winery.
    
    Rôle de groupes de contrôler qui peut voir les cas eDiscovery de sécurité Office 365 &amp; centre de conformité. Cela signifie qu’investigateurs et les gestionnaires de découverte électronique peuvent afficher uniquement les cas eDiscovery dans leur agence.
    
- Groupes de rôles également contrôlent qui peut attribuer des membres à une affaire eDiscovery. Cela signifie investigateurs et les gestionnaires de découverte électronique peuvent affecter uniquement des membres à cas ils se sont membres de.
    
Voici le processus de configuration des limites de conformité :
  
[Étape 1 : Identifier un attribut d’utilisateur pour définir votre agences](#step-1-identify-a-user-attribute-to-define-your-agencies)

[Étape 2 : Fichier d’une demande de support Microsoft pour synchroniser l’attribut utilisateur aux comptes OneDrive](#step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts)

[Étape 3 : Créer un groupe de rôles pour chaque organisme](#step-3-create-a-role-group-for-each-agency)

[Étape 4 : Créer un filtre d’autorisations de recherche pour appliquer la limite de la conformité](#step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary)

[Étape 5 : Créer un cas de découverte électronique pour une enquête intra-agence](#step-5-create-an-ediscovery-case-for-an-intra-agency-investigations)
  
## <a name="step-1-identify-a-user-attribute-to-define-your-agencies"></a>Étape 1 : Identifier un attribut d’utilisateur pour définir votre agences

La première étape consiste à choisir un attribut d’Azure Active Directory à utiliser qui définit votre agences. Cet attribut permet de créer le filtre recherche les autorisations qui limite une découverte électronique gestionnaire recherche uniquement les emplacements de contenu des utilisateurs qui sont attribués à une valeur spécifique pour cet attribut. Par exemple, que Contoso décide d’utiliser l’attribut de **service** . La valeur de cet attribut pour les utilisateurs de la filiale Fourth Coffee serait `FourthCoffee` et la valeur pour les utilisateurs de filiale de Coho Winery serait `CohoWinery`. À l’étape 4, vous allez utiliser cette `attribute:value` emplacements des gestionnaires de découverte peuvent rechercher du contenu paire (par exemple, *Service : FourthCoffee* ) pour limiter l’utilisateur. 
  
Voici une liste des attributs utilisateur Azure Active Directory que vous pouvez utiliser les limites de conformité :
  
- Company
    
- CountryCode
    
- CustomAttribute1 - CustomAttribute15
    
- Service
    
- Bureau
    
Bien que plusieurs attributs de l’utilisateur sont disponibles, en particulier pour les boîtes aux lettres Exchange, les attributs répertoriés ci-dessus sont les seules actuellement pris en charge par OneDrive.
  
## <a name="step-2-file-a-request-with-microsoft-support-to-synchronize-the-user-attribute-to-onedrive-accounts"></a>Étape 2 : Fichier d’une demande de support Microsoft pour synchroniser l’attribut utilisateur aux comptes OneDrive

L’étape suivante consiste à introduire une demande de support Microsoft pour synchroniser l’attribut Azure Active Directory que vous avez choisi à l’étape 1 pour tous les comptes de OneDrive dans votre organisation. Une fois cette synchronisation se produit, l’attribut (et sa valeur) que vous avez choisi à l’étape 1 est mappé sur une propriété gérée masquée dans SharePoint nommé `ComplianceAttribute`. Cet attribut vous permet de créer un filtre recherche les autorisations pour OneDrive à l’étape 4.
  
Inclure les informations suivantes lorsque vous soumettez la demande de support technique de Microsoft :
  
- Le nom de domaine par défaut de votre organisation Office 365
    
- Le nom de l’attribut Azure Active Directory (à l’étape 1)
    
- Le titre ou la description de l’objectif de la demande de prise en charge suivantes : « Activer OneDrive pour Business la synchronisation avec Azure Active Directory pour la conformité filtres de sécurité ». Cela permettra d’acheminer la demande vers l’équipe d’ingénierie eDiscovery Office 365 qui vous allez implémenter la demande.
    
Après la modification et l’attribut est synchronisé avec OneDrive, Support Microsoft vous enverra le numéro de version de la modification et une date estimée de déploiement. Notez que le processus de déploiement ne dure 4 à 6 semaines après avoir envoyé la demande de prise en charge.
  
 **Important :** Vous pouvez effectuer étape 3 à 5 avant le déploiement de la modification. Mais les recherches de contenu en cours d’exécution ne renverront des documents à partir des sites OneDrive spécifiés dans le filtre d’autorisations recherche jusqu'à ce qu’après le déploiement de la modification. 
  
## <a name="step-3-create-a-role-group-for-each-agency"></a>Étape 3 : Créer un groupe de rôles pour chaque organisme

L’étape suivante consiste à créer les groupes de rôles de sécurité Office 365 &amp; centre de conformité sont adaptés à votre agences. Nous vous conseillons de créer un nouveau groupe de rôles en copiant le groupe responsables de découverte électronique intégrés, ajout de membres appropriés et suppression de rôles ne soient pas applicables à vos besoins. Pour plus d’informations sur les rôles liés à la découverte électronique, consultez la rubrique [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
  
Pour créer les groupes de rôles, accédez à la page **autorisations** de sécurité &amp; centre de conformité et créer un groupe de rôles pour chaque équipe dans chaque agence qui utilise les limites de la conformité et les cas eDiscovery pour gérer les enquêtes. 
  
À l’aide du scénario des limites de conformité Contoso, quatre groupes de rôles doivent être créés et les membres appropriés ajoutés à chacune d’elles.
  
- Fourth Coffee eDiscovery responsables
    
- Quatrième investigateurs cafés
    
- Coho Winery eDiscovery responsables
    
- Coho Winery investigateurs
    

  
## <a name="step-4-create-a-search-permissions-filter-to-enforce-the-compliance-boundary"></a>Étape 4 : Créer un filtre d’autorisations de recherche pour appliquer la limite de la conformité
<a name="step4"> </a>

Une fois que vous avez créé des groupes de rôles pour chaque agence, l’étape suivante consiste à créer des filtres d’autorisations de recherche qu’associer chaque groupe de rôles à son agence spécifique et définit la limite de conformité proprement dite. Vous devez créer un filtre d’autorisations de recherche pour chaque agence. Pour plus d’informations sur la création des filtres d’autorisations de sécurité, voir [configurer les autorisations pour la recherche de contenu de filtrage](permissions-filtering-for-content-search.md).
  
Voici la syntaxe qui est utilisée pour créer un filtre d’autorisations de recherche utilisé pour des limites de conformité.

```
New-ComplianceSecurityFilter -FilterName <name of filter> -Users <role groups> -Filters "Mailbox_<Compliance attribute from Step 1>  -eq '<AttributeVale> '", "Site_ComplianceAttribute  -eq <AttributeValue>' -or Site_Path -like <SharePointURL> *'" -Action <Action >
```
  
Voici une description de chaque paramètre de la commande :
  
-  `FilterName`-Spécifie le nom du filtre. Utilisez un nom qui décrit ou identifie l’agence qui filtrent sera utilisé dans. 
    
-  `Users`-Spécifie les utilisateurs ou groupes qui reçoivent ce filtre appliqué aux actions de recherche de contenu qu’ils effectuent. Les limites de la conformité, ce paramètre spécifie les groupes de rôles (que vous avez créé à l’étape 3) dans l’Agence que vous créez le filtre. Notez que ceci est un paramètre à valeurs multiples afin d’inclure un ou plusieurs groupes de rôles, séparées par des virgules. 
    
-  `Filters`-Spécifie les critères de recherche pour le filtre. Pour les limites de conformité, vous allez définir les filtres suivants. Chacune d’elles s’applique à un emplacement de contenu utilisateur. 
    
  -  `Mailbox`-Spécifie les boîtes aux lettres qui les groupes de rôles définis dans le `Users` paramètre peut effectuer des recherches. Les limites de conformité, *ComplianceAttribute* est le même attribut que vous avez identifié à l’étape 1 et *AttributeValue* Spécifie l’Agence. Ce filtre permettre aux membres du groupe de rôles pour qu’il recherche les boîtes aux lettres dans une agence spécifique ; par exemple, `"Mailbox_Department -eq 'FourthCoffee'"` . 
    
  -  `Site`-Spécifie les comptes OneDrive les groupes de rôles définis dans le `Users` paramètre peut effectuer des recherches. Pour le filtre OneDrive, utilisez la chaîne réelle `ComplianceAttribute`; Cela permet de mapper à l’attribut de même que vous avez identifié à l’étape 1 et qui est synchronisé avec les comptes de OneDrive à la suite de la demande de prise en charge que vous avez soumis à l’étape 2 ;  *AttributeValue* Spécifie l’Agence. Ce filtre permettre aux membres du groupe de rôles pour qu’il recherche les comptes de OneDrive dans une agence spécifique ; par exemple, `"Site_ComplianceAttribute -eq 'FourthCoffee'"`.
    
  -  `Site_Path`-Spécifie les sites SharePoint que les groupes de rôles définis dans le `Users` paramètre peut effectuer des recherches. Le *SharePointURL* spécifie les sites dans l’Agence membres du groupe de rôles peuvent effectuer des recherches ; par exemple,`Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'"`
    
-  `Action`-Spécifie le type d’action de recherche de conformité le filtre est appliqué à. Par exemple, `-Action Search` serait uniquement appliquer le filtre lorsque les membres des groupes de rôles définis dans le `Users` paramètre exécute une recherche de contenu. Dans ce cas, le filtre n’est appliqué lors de l’exportation des résultats de la recherche. Les limites de conformité, utilisez `-Action All` afin que le filtre s’applique à toutes les actions de recherche. 
    
    Pour obtenir la liste des actions de recherche de contenu, consultez la section « New-ComplianceSecurityFilter » dans [Configure les autorisations de filtrage pour la recherche de contenu](permissions-filtering-for-content-search.md#new-compliancesecurityfilter).
    
Voici quelques exemples de filtres deux recherche autorisations qui seront créés pour prendre en charge le scénario des limites de conformité Contoso.
  
 **Fourth Coffee**

```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_ComplianceAttribute -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL
```
   
 **Zones de Coho Winery**

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_ComplianceAttribute -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL
```

## <a name="step-5-create-an-ediscovery-case-for-an-intra-agency-investigations"></a>Étape 5 : Créer un cas de découverte électronique pour une enquête intra-agence

L’étape finale consiste à créer un nouveau cas eDiscovery dans la sécurité &amp; centre de conformité, puis ajoutez le groupe de rôles, que vous avez créé à l’étape 3 : en tant que membre de la casse. Ainsi, deux points importants de l’utilisation des limites de conformité :
  
- Seuls les membres du groupe de rôles ajoutés au cas seront en mesure de voir et accéder à la casse de la sécurité &amp; centre de conformité. Par exemple, si le groupe de rôles Fourth Coffee investigateurs est le seul membre d’un cas, les membres du groupe de rôles de gestionnaires de découverte électronique Fourth Coffee (ou les membres de n’importe quel autre groupe de rôles) ne sont pas être en mesure de voir ou d’accéder à la casse.
    
- Lorsqu’un membre du groupe de rôles affecté à un cas exécute une recherche associée à la casse, ils ne seront en mesure de rechercher les emplacements de contenu au sein de leur agence (qui est définie par le filtre d’autorisations de recherche que vous avez créé à l’étape 4.)


Pour créer un nouveau cas et affecter des membres :
    
1. Accédez à la page de **découverte** de la sécurité &amp; centre de conformité et de créer un nouveau cas. 
    
2. Dans la liste des cas eDiscovery, cliquez sur le nom du dossier que vous venez de créer.
    
3. Dans la page flottant **gérer ce cas** , sous **groupes de rôles gérer**, cliquez sur ![icône Ajouter](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **Ajouter**.
    
    ![Ajouter un groupe de rôles en tant que membre d’un cas de découverte électronique](media/f8b4b557-01b9-4388-85be-b5b5ab7c5629.png)
  
4. Dans la liste des groupes de rôles, sélectionnez un des groupes de rôles que vous avez créé à l’étape 3 et cliquez sur **Ajouter**.
    
5. Dans la fenêtre **gérer ce cas** mobile pour enregistrer la modification, cliquez sur **Enregistrer** . 

## <a name="compliance-boundary-limitations"></a>Limitations de limite de conformité

N’oubliez pas les limites suivantes lors de la gestion des cas eDiscovery et des investigations qui utilisent des limites de conformité.
  
- Lors de la création et l’exécution d’une recherche de contenu, vous pouvez sélectionner les emplacements de contenu qui sont en dehors de votre agence. Toutefois, en raison du filtre d’autorisations de recherche, le contenu à partir de ces emplacements ne sont pas inclus dans les résultats de recherche.
    
- Limites de conformité ne s’appliquent pas suspensions dans les cas eDiscovery. Par conséquent, qu'un Gestionnaire de découverte électronique dans une agence permettre placer un utilisateur dans une autre agence en attente. Toutefois, la limite de conformité sera appliquée si le Gestionnaire de découverte électronique recherche les emplacements de contenu de l’utilisateur qui a été mis en attente. Cela signifie que le Gestionnaire de découverte ne sont pas être en mesure de rechercher les emplacements de contenu de l’utilisateur, même s’ils ont été en mesure de mettre l’utilisateur en attente.
    
    En outre, maintenez la touche statistiques seront applique uniquement aux emplacements de contenu dans l’Agence.
    
- Autorisations les filtres de recherche ne sont pas appliquées aux dossiers publics Exchange.

## <a name="searching-and-exporting-content-in-multi-geo-environments"></a>Recherche et exportation de contenu dans des environnements Multi-localisés

Autorisations les filtres de recherche vous permettent de contrôler où le contenu est acheminé pour l’exportation et les centres de données pouvant être recherchées lors de la recherche des sites SharePoint et les comptes de OneDrive dans un [environnement SharePoint Multi-localisés](https://go.microsoft.com/fwlink/?linkid=860840):
  
- Exporter les résultats de la recherche à partir d’un centre de données spécifique. Cela signifie que vous pouvez spécifier que les résultats seront exportés à partir de la recherche emplacement du centre de données.
    
- Itinéraire recherche des sites SharePoint et les comptes de OneDrive pour un centre de données satellites. Cela signifie que vous pouvez spécifier l’emplacement du centre de données où les recherches seront exécutera.
    
Utilisez le paramètre de la **région** pour les applets de commande **New-ComplianceSecurityFilter** ou **Set-ComplianceSecurityFilter** pour créer ou modifier l’exportation est acheminée via le centre de données.
  
|**Valeur du paramètre**|**Emplacement du centre de données**|
|:-----|:-----|
|NAM  <br/> |Amérique du Nord (données réelles centres sont aux États-Unis)  <br/> |
|EUR  <br/> |Europe  <br/> |
|APC  <br/> |Asie-Pacifique  <br/> |
|CAN <br/> |Canada
   
De même, vous pouvez utiliser les valeurs suivantes pour les valeurs de paramètre **Region** pour contrôler les recherches de contenu s’exécute dans lors de la recherche des sites SharePoint et OneDrive le centre de données. Notez que le tableau suivant présente également l’exportations seront acheminées par le biais du centre de données. 
  
|**Valeur du paramètre**|**Emplacements de routage pour l’exportation du centre de données**|
|:-----|:-----|
|NAM  <br/> |US  <br/> |
|EUR  <br/> |Europe  <br/> |
|APC  <br/> |Asie-Pacifique  <br/> |
|CAN  <br/> |US  <br/> |
|AUS  <br/> |Asie-Pacifique  <br/> |
|KOR  <br/> |Centre de données de l’organisation par défaut  <br/> |
|GBR  <br/> |Europe  <br/> |
|JPN  <br/> |Asie-Pacifique  <br/> |
|IND  <br/> |Asie-Pacifique  <br/> |
|LAM  <br/> |US  <br/> |
   
 **Remarque :** Si vous ne spécifiez pas le paramètre Region pour un filtre d’autorisations de recherche, la région de SharePoint par défaut organisations portera, puis les résultats de recherche sont exportés vers le centre de données le plus proche. 
  
Voici des exemples d’utilisation de la **-région** paramètre lors de la création des filtres d’autorisation de recherche les limites de conformité. Cela suppose que la filiale Fourth Coffee se trouve en Amérique du Nord et que les zones de Coho Winery est en Europe. 
  
```
New-ComplianceSecurityFilter -FilterName "Fourth Coffee Security Filter" -Users "Fourth Coffee eDiscovery Managers", "Fourth Coffee Investigators" -Filters "Mailbox_Department -eq 'FourthCoffee'", "Site_Department -eq 'FourthCoffee' -or Site_Path -like 'https://contoso.sharepoint.com/sites/FourthCoffee*'" -Action ALL -Region NAM
```

```
New-ComplianceSecurityFilter -FilterName "Coho Winery Security Filter" -Users "Coho Winery eDiscovery Managers", "Coho Winery Investigators" -Filters "Mailbox_Department -eq 'CohoWinery'", "Site_Department -eq 'CohoWinery' -or Site_Path -like 'https://contoso.sharepoint.com/sites/CohoWinery*'" -Action ALL -Region EUR
```
   
Gardez les éléments suivants à l’esprit lors de la recherche et l’exportation de contenu dans des environnements multi-localisés.
  
- Le paramètre de **région** ne contrôle pas les recherches de boîtes aux lettres Exchange ; Pour rechercher tous les centres de données lorsque vous recherchez des boîtes aux lettres. Pour limiter l’étendue de quels Exchange boîtes aux lettres pouvant être recherchées, utilisez le paramètre de **filtre** lors de la création ou modification d’un filtre d’autorisations de recherche. 
    
- S’il est nécessaire pour un gestionnaire à rechercher dans plusieurs régions SharePoint eDiscovery, vous devez créer un autre compte d’utilisateur qu’eDiscovery manager qui peut être utilisé dans le filtre d’autorisations de recherche pour spécifier la région de substitution où le Sites SharePoint ou les comptes de OneDrive sont trouvent.
    
- Lorsque vous recherchez du contenu dans SharePoint et OneDrive, le paramètre **Region** dirige les recherches soit la principale ou satellite l’emplacement où le Gestionnaire de découverte électronique mener des enquêtes eDiscovery. Si un gestionnaire de découverte électronique recherche des sites SharePoint et OneDrive en dehors de la zone qui est spécifié dans le filtre d’autorisations de recherche, aucun résultat de recherche ne s’afficheront. 
    
- Lors de l’exportation des résultats de la recherche, le contenu de tous les emplacements de contenu (y compris Exchange, Skype pour OneDrive entreprise, SharePoint et autres services Office 365 que vous pouvez rechercher à l’aide de l’outil de recherche de contenu) sera téléchargé à l’emplacement de stockage Azure dans le Centre de données qui est spécifiée par le paramètre **Region** . Les organisations peuvent ainsi rester au sein de la conformité en n’autorisant ne pas de contenu doivent être exportées au-delà des frontières contrôlés. Si aucune région n’est spécifiée dans le filtre d’autorisations de recherche, le contenu est téléchargé vers la région de l’organisation par défaut. 
    
- Vous pouvez modifier un filtre d’autorisations recherche existant pour ajouter ou modifier la région en exécutant la commande suivante :

    ```
    Set-ComplianceSecurityFilter -FilterName <Filter name>  -Region <Region>
    ```
 
## <a name="frequently-asked-questions"></a>Questions fréquemment posées

 **Qui peut créer et gérer des filtres d’autorisations de recherche (à l’aide de New-ComplianceSecurityFilter et des applets de commande Set-ComplianceSecurityFilter) ?**
  
Pour créer, afficher et modifier les filtres des autorisations de recherche, vous devez être membre du groupe de rôles de gestion de l’organisation de la sécurité &amp; centre de conformité.
  
 **Si un gestionnaire de découverte électronique est affecté à plus d’un groupe de rôles qui s’étend sur plusieurs agences, comment ils des recherches de contenu dans une agence ou l’autre ?**
  
Le Gestionnaire de découverte électronique peut ajouter des paramètres à sa requête de recherche qui restreint la recherche à une agence spécifique. Par exemple, si une organisation a spécifié à la propriété **CustomAttribute10** pour différencier les agences gouvernementales, ils peuvent ajoutez le code suivant à leur requête de recherche pour rechercher les boîtes aux lettres et les comptes de OneDrive dans une agence spécifique : `CustomAttribute10:<value> AND Site_ComplianceAttribute:<value>`.
  
 **Que se passe-t-il si la valeur de l’attribut est utilisé en tant que l’attribut de conformité dans un filtre d’autorisations de recherche est modifiée ?**
  
Elle accepte jusqu'à 3 jours pour un filtre d’autorisations de recherche appliquer la limite de la conformité si la valeur de l’attribut est utilisé dans le filtre est modifiée. Par exemple, dans le scénario Contoso Supposons qu’un utilisateur de l’Agence Fourth Coffee est transféré vers l’Agence Coho Winery. Par conséquent, la valeur de l’attribut de **service** de l’objet utilisateur est modifiée à partir de *FourthCoffee* à *CohoWinery* . Dans ce cas, les investisseurs et eDiscovery Fourth Coffee seront obtenir des résultats de recherche pour cet utilisateur pour les 3 jours après la modification de l’attribut. De même, il aura jusqu'à 3 jours avant les gestionnaires de découverte électronique Coho Winery et investigateurs obtenez des résultats de recherche pour l’utilisateur. 
  
 **Un gestionnaire de découverte électronique voyez du contenu à partir de deux frontières de conformité distincte ?**
  
Oui. Pour ce faire, vous pouvez ajouter l’utilisateur à des groupes de rôles qui ont accès aux deux agences.
  
 **De recherche autorisations filtres pour suspensions cas eDiscovery, les stratégies de rétention Office 365 ou DLP ?**
  
Non, pas pour l’instant
  
 **Si vous indiquer une région au contrôle où le contenu est exporté, mais je n’ai pas une organisation SharePoint dans cette zone, puis-je toujours recherche SharePoint ?**
  
Si la zone spécifiée dans le filtre d’autorisations de recherche n’existe pas dans votre organisation, la zone par défaut est examinée.
  
 **Quel est le nombre maximal de filtres des autorisations de recherche qui peuvent être créés dans une organisation ?**
  
Il n’existe aucune limite au nombre de filtres des autorisations de recherche qui peuvent être créés dans une organisation. Toutefois, les performances de recherche seront affectées quand il y a plus de 100 filtres d’autorisations de recherche. Pour conserver le nombre de filtres d’autorisations de recherche dans votre organisation plus petit possible, créer des filtres qui associent des règles pour Exchange, SharePoint et OneDrive dans un filtre d’autorisations de recherche unique la mesure du possible.
