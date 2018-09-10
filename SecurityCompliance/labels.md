---
title: Vue d’ensemble des étiquettes
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/22/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Dans Office 365, les étiquettes vous aident à entreprendre les bonnes actions sur le contenu approprié. Grâce aux étiquettes, vous pouvez classer les données au sein de votre organisation à des fins de gouvernance, et appliquer des règles de rétention basées sur cette classification. Vous pouvez également utiliser des étiquettes pour implémenter la gestion des enregistrements dans Office 365.
ms.openlocfilehash: e08a1772a7e04f459b80762e3da17600ef84c95a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013748"
---
# <a name="overview-of-labels"></a>Vue d’ensemble des étiquettes

Au sein de votre organisation, il existe probablement divers types de contenu devant faire l’objet d’actions différentes afin de respecter des réglementations du secteur et des stratégies internes. Par exemple, vous pouvez avoir les types de contenu suivants :
  
- Formulaires fiscaux qui doivent être **conservés** pendant une période minimale de temps. 
    
- Documents de presse qui doivent être **définitivement supprimés** après une certaine date. 
    
- Recherche concurrentielle qui doit être **conservée**, puis **définitivement supprimée**. 
    
- Permis de travail qui doivent être **enregistrés** afin de ne pas être modifiés ou supprimés. 
    
Dans tous ces cas, les étiquettes dans Office 365 vous aident à entreprendre les bonnes actions sur le contenu approprié. Grâce aux étiquettes, vous pouvez classer les données au sein de votre organisation à des fins de gouvernance, et appliquer des règles de rétention basées sur cette classification.
  
Grâce aux étiquettes, vous pouvez effectuer les actions suivantes :
  
- **Permettre aux personnes de votre organisation d’appliquer manuellement une étiquette** à du contenu dans Outlook sur le web, Outlook 2010 et versions ultérieures, OneDrive, SharePoint et les groupes Office 365. Les utilisateurs ont souvent une meilleure connaissance du type de contenu qu’ils utilisent. Ils peuvent donc les classer et y faire appliquer la stratégie appropriée. 
    
- **Appliquer des étiquettes au contenu automatiquement** s’il répond à des conditions spécifiques, comme lorsque le contenu contient : 
    
  - des types spécifiques d’informations sensibles ;
    
  - des mots clés spécifiques correspondant à une requête que vous créez.
    
    La possibilité d’appliquer automatiquement des étiquettes à du contenu est importante pour les raisons suivantes :
    
  - Vous n’avez pas à former les utilisateurs à l’ensemble de vos classifications.
    
  - Vous n’avez pas à dépendre des utilisateurs pour classer tout le contenu correctement.
    
  - Les utilisateurs n’ont plus à connaître les stratégies de gouvernance des données : à la place, ils peuvent se concentrer sur leur travail.
    
    Notez que les étiquettes à appliquer automatiquement requièrent un abonnement Office 365 Entreprise E5.
    
- **Appliquer une étiquette par défaut à une bibliothèque de documents** dans les sites de groupes Office 365 et SharePoint, afin que tous les documents figurant dans cette bibliothèque obtiennent l’étiquette par défaut. 
    
- **Mettre en œuvre la gestion des enregistrements dans Office 365**, notamment les e-mails et les documents. Vous pouvez utiliser une étiquette pour classer du contenu en tant qu’enregistrement. Lorsque cela se produit, l’étiquette ne peut pas être modifiée ou supprimée, et le contenu ne peut pas être modifié ou supprimé. 
    
Vous créez et gérez des étiquettes sur la page **Étiquettes** dans le Centre de sécurité &amp; conformité Office 365. 
  
![Page Étiquettes](media/42d1865d-f0f5-436d-8e09-0e547302c816.png)
 
## <a name="how-labels-work-with-label-policies"></a>Fonctionnement des étiquettes avec les stratégies d’étiquette

Rendre les étiquettes disponibles aux membres de votre organisation afin qu’ils puissent classer du contenu est un processus en deux étapes. Tout d’abord, créez les étiquettes, puis publiez-les dans les emplacements de votre choix. Lorsque vous publiez des étiquettes, une stratégie d’étiquette est créée.
  
![Diagramme des rôles et des tâches pour les étiquettes](media/4082bc7d-c04c-4b9a-8a26-7f12565d3311.png)
  
Les étiquettes sont des blocs de construction indépendants et réutilisables, qui sont inclus dans une stratégie d’étiquette et publiés dans différents emplacements. Les étiquettes peuvent être réutilisées au sein de nombreuses stratégies. L’objectif principal de la stratégie d’étiquette est de regrouper un ensemble d’étiquettes et de spécifier les emplacements où vous souhaitez que ces étiquettes apparaissent.
  
![Diagramme des étiquettes, des stratégies d’étiquette et des emplacements](media/eee42516-adf0-4664-b5ab-76727a9a3511.png)
  
1. Lorsque vous publiez des étiquettes, celles-ci sont incluses dans une stratégie d’étiquette. Une même étiquette peut être incluse dans plusieurs stratégies.
    
2. Les stratégies d’étiquette définissent les emplacements où publier les étiquettes.
    
## <a name="only-one-label-at-a-time"></a>Une seule étiquette à la fois

Il est important de savoir que le contenu comme un e-mail ou un document ne peut porter qu’une seule étiquette à la fois :
  
- En ce qui concerne les étiquettes attribuées manuellement par les utilisateurs finaux, les utilisateurs peuvent supprimer ou modifier l’étiquette attribuée.
    
- Si du contenu porte une étiquette à appliquer automatiquement, celle-ci peut être remplacée par une étiquette attribuée manuellement par un utilisateur final.
    
- Si du contenu porte une étiquette attribuée manuellement par un utilisateur final, celle-ci ne peut pas être remplacée par une étiquette à appliquer automatiquement.
    
- S’il existe plusieurs règles qui attribuent une étiquette à appliquer automatiquement et que le contenu remplit les critères de plusieurs règles, l’étiquette de la règle la plus ancienne est attribuée.
    
Les étiquettes attribuées manuellement sont attribuées explicitement ; les étiquettes à appliquer automatiquement sont attribuées implicitement ; une étiquette explicite est prioritaire sur une étiquette implicite. Pour obtenir plus d’informations, consultez la section [Principes de rétention et priorité](labels.md#principles) indiquée ci-après.
  
## <a name="how-long-it-takes-for-labels-to-take-effect"></a>Délai d’activation des étiquettes

Lorsque vous publiez ou appliquez automatiquement des étiquettes, elles ne prennent pas effet immédiatement :
  
1. La stratégie d’étiquette doit d’abord être synchronisée à partir du Centre de sécurité &amp; conformité avec les emplacements définis dans la stratégie.
    
2. Ensuite, l’emplacement a parfois besoin de temps pour rendre les étiquettes manuelles disponibles aux utilisateurs finaux ou appliquer automatiquement des étiquettes au contenu. Le temps nécessaire dépend de l’emplacement et du type d’étiquette.
    
### <a name="manual-labels"></a>Étiquettes manuelles

Si vous publiez des étiquettes sur SharePoint ou OneDrive, cela peut prendre un jour pour que ces étiquettes soient visibles aux utilisateurs finaux. De plus, si vous publiez des étiquettes sur Exchange, cela peut prendre 7 jours pour que ces étiquettes soient visibles aux utilisateurs finaux, et la boîte aux lettres doit contenir au moins 10 Mo de données.
  
![Diagramme de la date d’effet des étiquettes manuelles](media/b19f3a10-f625-45bf-9a53-dd14df02ae7c.png)
  
### <a name="auto-apply-labels"></a>Étiquettes à appliquer automatiquement

Si vous appliquez des étiquettes automatiquement au contenu répondant à des conditions spécifiques, il peut prendre sept jours pour que ces étiquettes soient appliquées à tout le contenu remplissant les conditions.
  
![Diagramme de la date d’effet des étiquettes à appliquer automatiquement](media/b8c00657-477a-4ade-b914-e643ef97a10d.png)
  
### <a name="how-to-check-on-the-status-of-exchange-labels"></a>Vérification du statut des étiquettes Exchange

Dans Exchange Online, les étiquettes deviennent disponibles aux utilisateurs finaux par l’intermédiaire d’un processus qui s’exécute tous les sept jours. À l’aide de Powershell, vous pouvez découvrir la date de la dernière exécution du processus et déterminer la date de sa prochaine exécution.
  
1. [Connectez-vous à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=799773).
    
2. Exécutez les commandes suivantes :
    
  ```
  $logProps = Export-MailboxDiagnosticLogs <user> -ExtendedProperties
  ```

  ```
  $xmlprops = [xml]($logProps.MailboxLog)
  ```

  ```
  $xmlprops.Properties.MailboxTable.Property | ? {$_.Name -like "ELC*"}
  ```

    Dans les résultats, la propriété (UTC) `ELCLastSuccessTimeStamp` indique la date à laquelle le système a traité votre boîte aux lettres pour la dernière fois. Si ce n’est pas arrivé depuis la création de la stratégie, les étiquettes n’apparaîtront pas. Pour forcer le traitement, exécutez `Start-ManagedFolderAssistant -Identity <user>`.
    
    Si les étiquettes n’apparaissent pas dans Outlook sur le web comme prévu, veillez à vider le cache dans votre navigateur (CTRL + F5).
    
## <a name="label-policies-and-locations"></a>Stratégies d’étiquette et emplacements

Différents types d’étiquettes peuvent être publiés dans différents emplacements, en fonction du descriptif de l’étiquette.
  
|**Si l’étiquette est...**|**La stratégie d’étiquette peut être appliquée à...**|
|:-----|:-----|
|Publiée aux utilisateurs finaux  <br/> |Exchange, SharePoint, OneDrive et aux groupes Office 365  <br/> |
|Appliquée automatiquement en fonction des types d’informations sensibles  <br/> |Exchange (toutes les boîtes aux lettres uniquement), SharePoint, OneDrive  <br/> |
|Appliquée automatiquement en fonction d’une requête  <br/> |Exchange, SharePoint, OneDrive et aux groupes Office 365  <br/> |
   
Notez que dans Exchange, les étiquettes à appliquer automatiquement (pour les requêtes et les types d’informations sensibles) sont appliquées uniquement aux messages récemment envoyés (données en transit), pas à tous les éléments actuellement dans la boîte aux lettres (données au repos). Par ailleurs, les étiquettes à appliquer automatiquement pour les types d’informations sensibles ne peuvent s’appliquer qu’à toutes les boîtes aux lettres. Vous ne pouvez pas sélectionner des boîtes aux lettres spécifiques.
  
Notez que les dossiers publics Exchange et Skype ne prennent pas en charge les étiquettes.
  
## <a name="how-labels-enforce-retention"></a>Application de la rétention par les étiquettes

Des étiquettes peuvent appliquer exactement les mêmes actions de rétention qu’une stratégie de rétention. Vous pouvez utiliser des étiquettes pour implémenter un plan de contenu complexe (ou plan fichier). Pour obtenir plus d’informations sur le fonctionnement de la rétention, consultez l’article [Vue d’ensemble des stratégies de rétention](retention-policies.md).
  
En outre, une étiquette dispose de deux options de rétention qui sont disponibles uniquement dans une étiquette et pas dans une stratégie de rétention. Avec une étiquette, vous pouvez effectuer les actions suivantes :
  
- Déclencher une révision de destruction à la fin de la période de rétention, afin que les documents SharePoint et OneDrive soient vérifiés avant d’être supprimés. Pour obtenir plus d’informations, consultez l’article [Vue d’ensemble des révisions de destruction](disposition-reviews.md).
    
- Démarrer la période de rétention à compter de la date d’étiquetage du contenu, au lieu de l’ancienneté du contenu ou de la date de sa dernière modification.
    
![Paramètres de rétention avec les options spécifiques des étiquettes](media/c49118c9-6279-4661-94db-deffa76e27ac.png)
  
## <a name="where-published-labels-can-appear-to-end-users"></a>Emplacements des étiquettes publiées visibles aux utilisateurs finaux

Si votre étiquette est attribuée au contenu par les utilisateurs finaux, vous pouvez la publier pour :
  
- Outlook sur le web
    
- Outlook 2010 et versions ultérieures
    
- OneDrive
    
- SharePoint
    
- Les groupes Office 365 (le site de groupe et la boîte aux lettres de groupe dans Outlook sur le web)
    
Les sections indiquées ci-dessous montrent comment les étiquettes s’affichent aux membres de votre organisation dans différentes applications.
  
### <a name="outlook-on-the-web"></a>Outlook sur le web

Pour étiqueter un élément dans Outlook sur le web, cliquez sur l’élément \> **Attribuer une stratégie** \> choisissez l’étiquette. 
  
![Menu Attribuer une stratégie dans Outlook sur le web](media/146a23cf-e478-4595-b2e8-f707fc4e6ea3.png)
  
Après avoir appliqué l’étiquette, vous pouvez l’afficher, ainsi que son action, en haut de l’élément. Si un e-mail est classé et associé à une période de rétention, vous pouvez connaître en un clin d’œil la date d’expiration de l’e-mail.
  
![Étiquette affectée à la messagerie dans Outlook sur le web](media/16f6c91b-5eab-4574-9d13-6d12be00a783.png)
  
Vous pouvez également appliquer des étiquettes à des dossiers. Dans ce cas, tenez compte des points suivants :
  
- Tous les éléments du dossier héritent automatiquement de cette même étiquette, **à l’exception** des éléments auxquels une étiquette a été appliquée explicitement. Les éléments étiquetés explicitement conservent leur étiquette. Pour obtenir plus d’informations, consultez la section relative aux principes de rétention ci-après. 
    
- Si vous modifiez ou supprimez l’étiquette par défaut d’un dossier, l’étiquette est également modifiée ou supprimée pour tous les éléments dans le dossier **à l’exception** des éléments portant des étiquettes explicites. 
    
- Si vous déplacez un élément portant une étiquette par défaut d’un dossier vers un autre dossier portant une étiquette par défaut différente, l’élément reçoit la nouvelle étiquette par défaut.
    
- Si vous déplacez un élément portant une étiquette par défaut d’un dossier vers un autre dossier ne portant pas d’étiquette par défaut, l’ancienne étiquette par défaut est supprimée.
    
### <a name="outlook-2010-and-later"></a>Outlook 2010 et versions ultérieures

Pour étiqueter un élément dans Outlook sur le web, cliquez sur l’élément \> sur le **Ruban** \> **Attribuer une stratégie** \> choisissez l’étiquette. 
  
![Bouton Attribuer une stratégie](media/30684dea-dd73-4e4a-9185-8e29f403b6ca.png)
  
Après avoir appliqué l’étiquette, vous pouvez l’afficher, ainsi que son action, en haut de l’élément. Si un e-mail est classé et associé à une période de rétention, vous pouvez connaître en un clin d’œil la date d’expiration de l’e-mail.
  
Vous pouvez également appliquer des étiquettes aux dossiers. Le processus est le même pour Outlook 2010 et versions ultérieures que pour Outlook sur le web : consultez la section précédente pour obtenir plus d’informations.
  
### <a name="onedrive-and-sharepoint"></a>OneDrive et SharePoint

Pour étiqueter un document (notamment les fichiers OneNote) dans OneDrive ou SharePoint, sélectionnez l’élément \> dans le coin supérieur droit, sélectionnez **Ouvrir le volet d’informations**![icône Volet d’informations](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) \> **Appliquer une étiquette** \> choisissez l’étiquette. 
  
Notez que vous pouvez également appliquer une étiquette à un ensemble de dossiers ou de documents, et que vous pouvez définir une étiquette par défaut pour une bibliothèque de documents : consultez la section ci-après pour obtenir plus d’informations.
  
![Liste Appliquer l’étiquette pour un élément dans SharePoint](media/151cc83c-da57-45b0-9cd1-fd2f28a31083.png)
  
Après avoir appliqué une étiquette à un élément, vous pouvez l’afficher dans le volet d’informations lorsque cet élément est sélectionné.
  
![Étiquette appliquée apparaissant dans le volet d’informations](media/d06e585e-29f7-4c8c-afef-629c97268b8e.png)
  
Vous pouvez également créer un affichage de la bibliothèque qui contient la colonne **Étiquettes** ou la colonne **Élément est un enregistrement**, afin que vous puissiez voir en un clin d’œil les étiquettes attribuées à tous les éléments, et les éléments qui sont des enregistrements. Toutefois, notez que vous ne pouvez pas filtrer l’affichage par la colonne **Élément est un enregistrement**. 
  
![Colonne Bibliothèque pour les étiquettes apparaissant dans l’affichage personnalisé](media/e3392627-c0a3-405e-bb57-55f27c34cfdd.png)
  
### <a name="office-365-groups"></a>Groupes Office 365

Lorsque vous publiez des étiquettes à un groupe Office 365, les étiquettes apparaissent dans le site de groupe et la boîte aux lettres de groupe dans Outlook sur le web. L’expérience d’application d’une étiquette au contenu est identique à celle illustrée ci-dessus pour la messagerie et les documents.
  
## <a name="applying-a-label-automatically-based-on-conditions"></a>Application d’une étiquette automatiquement en fonction de conditions

L’une des fonctionnalités les plus puissantes des étiquettes est la possibilité de les appliquer automatiquement au contenu qui remplit certaines conditions. Dans ce cas, les membres de votre organisation ne doivent pas appliquer ces étiquettes : Office 365 s’en charge à leur place.
  
![Diagramme des rôles et des tâches pour les étiquettes à appliquer automatiquement](media/32f2f2fd-18a8-43fd-839d-72ad7a43e069.png)
  
Les étiquettes à appliquer automatiquement sont puissantes pour les raisons suivantes :
  
- Vous n’avez pas à former les utilisateurs à l’ensemble de vos classifications.
    
- Vous n’avez pas à dépendre des utilisateurs pour classer tout le contenu correctement.
    
- Les utilisateurs n’ont plus à connaître les stratégies de gouvernance des données : ils peuvent se concentrer sur leur travail.
    
Vous pouvez choisir d’appliquer automatiquement des étiquettes au contenu quand celui-ci inclut :
  
- des types spécifiques d’informations sensibles ;
    
- des mots clés spécifiques correspondant à une requête que vous créez.
    
![Page Choisir une condition pour l’étiquette à appliquer automatiquement](media/c0b7a3ef-bda0-494c-941d-f1f93753ecdd.png)
  
Notez que les étiquettes à appliquer automatiquement requièrent un abonnement Office 365 Entreprise E5 et que cela peut prendre jusqu’à sept jours pour que les étiquettes à appliquer automatiquement soient appliquées à tout le contenu remplissant les conditions, comme décrit ci-dessus.
  
### <a name="auto-apply-labels-to-content-with-specific-types-of-sensitive-information"></a>Application automatique d’étiquettes au contenu incluant des types spécifiques d’informations sensibles

Lorsque vous créez des étiquettes à appliquer automatiquement pour des informations sensibles, vous observez la même liste de modèles de stratégies que lorsque vous créez une stratégie de prévention contre la perte de données (DLP). Chaque modèle de stratégie est préconfiguré pour rechercher des types spécifiques d’informations sensibles. Par exemple, le modèle présenté ici recherche les numéros d’identification fiscale individuels américains (ITIN), les numéros de sécurité sociale et les numéros de passeport. Pour en savoir plus sur la protection contre la perte de données, consultez l’article [Vue d’ensemble des stratégies de protection contre la perte de données](data-loss-prevention-policies.md).
  
![Modèles de stratégie avec des types d’informations sensibles](media/dafd87d4-c7bb-439a-ac7b-193c018f98a5.png)
  
Après avoir sélectionné un modèle de stratégie, vous pouvez ajouter ou supprimer tout type d’informations sensibles, et vous pouvez modifier le nombre d’instances et la précision de correspondance. Dans l’exemple présenté ici, une étiquette sera appliquée automatiquement uniquement dans les cas suivants :
  
- Le contenu comprend entre 1 et 9 instances de l’un de ces trois types d’informations sensibles. Vous pouvez supprimer la valeur **max** pour la définir sur **any**.
    
- Le type d’informations sensibles détecté a une précision de correspondance (ou niveau de confiance) minimale de 75. De nombreux types d’informations sensibles sont définis avec plusieurs modèles. Tandis qu’un modèle avec une précision de correspondance plus élevée nécessite un nombre de preuves plus important (par exemple, des mots clés, des dates ou des adresses), un modèle avec une précision de correspondance inférieure nécessite moins de preuves. En d’autres termes, plus la précision de correspondance **min** est faible, plus il est facile de faire correspondre le contenu à la condition. 
    
    Si vous modifiez la précision de correspondance (ou niveau de confiance), vous devez utiliser l’un des niveaux de confiance utilisés dans un modèle pour ce type d’informations sensibles, comme défini dans [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
    
![Options permettant d’identifier les types d’informations sensibles](media/de255881-f596-4c8d-8359-e974e3a0819a.png)
  
### <a name="auto-apply-labels-to-content-with-specific-keywords"></a>Application automatique d’étiquettes au contenu avec des mots clés spécifiques

Vous pouvez appliquer automatiquement des étiquettes au contenu remplissant certaines conditions. Les conditions actuellement disponibles prennent en charge l’application d’une étiquette au contenu comprenant des mots ou des phrases spécifiques. Vous pouvez affiner votre requête à l’aide des opérateurs de recherche tels que AND, OR et NOT. Pour obtenir plus d’informations sur ces opérateurs, consultez l’article [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).
  
La prise en charge de l’ajout de propriétés utilisables dans une requête (par exemple, **subject:**) sera bientôt disponible. 
  
Notez que les étiquettes basées sur une requête utilisent l’index de recherche pour identifier le contenu.
  
![Éditeur de requête](media/ac5b8e5e-7453-4ec7-905c-160df57298d3.png)
  
## <a name="applying-a-default-label-to-all-content-in-a-sharepoint-library-folder-or-document-set"></a>Application d’une étiquette par défaut à tout le contenu dans une bibliothèque, un dossier ou un ensemble de documents SharePoint

En plus de permettre aux utilisateurs d’appliquer une étiquette à des documents individuels, vous pouvez également appliquer une étiquette par défaut à une bibliothèque, à un dossier ou à un ensemble de documents SharePoint, afin que tous les documents dans cet emplacement héritent de cette étiquette par défaut.
  
Pour une bibliothèque de documents, cette opération s’effectue sur la page **Paramètres de la bibliothèque**. Lorsque vous choisissez l’étiquette par défaut, vous pouvez également choisir de l’appliquer à tous les éléments présents dans la bibliothèque. 
  
Par exemple, si vous avez une balise pour des documents marketing et vous savez qu’une bibliothèque de documents spécifique contient uniquement ce type de contenu, vous pouvez rendre la balise Document marketing par défaut pour tous les documents de cette bibliothèque.
  
![Option Appliquer l’étiquette sur la page Paramètres de la bibliothèque](media/0787d651-63dc-43b4-8768-716a5ecc64ec.png)
  
Si vous appliquez une étiquette par défaut à des éléments existants dans la bibliothèque, le dossier ou l’ensemble de documents, procédez comme suit :
  
- Tous les éléments de la bibliothèque, du dossier ou de l’ensemble de documents héritent automatiquement de cette même étiquette, **à l’exception** des éléments auxquels une étiquette a été appliquée explicitement. Les éléments étiquetés explicitement conservent leur étiquette. Pour obtenir plus d’informations, consultez la section [Principes de rétention et priorité](labels.md#principles) indiquée ci-après.
    
- Si vous modifiez ou supprimez l’étiquette par défaut d’une bibliothèque, d’un dossier ou de l’ensemble de documents, l’étiquette est également modifiée ou supprimée pour tous les éléments dans la bibliothèque, le dossier ou l’ensemble de documents, **à l’exception** des éléments portant des étiquettes explicites. 
    
- Si vous déplacez un élément portant une étiquette par défaut d’une bibliothèque, d’un dossier ou d’un ensemble de documents vers une autre bibliothèque, un autre dossier ou un autre ensemble de documents, l’élément conserve son étiquette par défaut existante, même si l’étiquette par défaut du nouvel emplacement est différente.
    
## <a name="applying-a-label-to-email-by-using-rules"></a>Application d’une étiquette à la messagerie à l’aide de règles

Dans Outlook 2010 ou versions ultérieures, vous pouvez créer des règles pour appliquer une étiquette ou une stratégie de rétention.
  
Par exemple, vous pouvez créer une règle qui applique une étiquette spécifique de tous les messages envoyés vers un groupe de distribution spécifique ou à partir de celui-ci.
  
Pour créer une règle, faites un clic droit sur un élément \> **Règles** \> **Créer une règle** \> **Options avancées** \> **Assistant de règles** \> **appliquez la stratégie de rétention**.
  
![Assistant de règles avec option pour appliquer les stratégies de rétention](media/eeb2407c-15b6-4224-99cf-e0a00034d8ea.png)
  
## <a name="classifying-content-without-applying-any-actions"></a>Classification de contenu sans appliquer d’action

Lorsque vous créez une étiquette, vous pouvez le faire sans activer de rétention ou d’autres actions, comme illustré ci-dessous. Dans ce cas, vous pouvez utiliser une étiquette comme simple étiquette de texte sans y appliquer la moindre action.
  
Par exemple, vous pouvez créer une étiquette nommée « Réviser plus tard » sans action, puis appliquer automatiquement cette étiquette au contenu avec des types d’informations sensibles ou au contenu recherché.
  
![Page Paramètres d’étiquette avec rétention désactivée](media/17ce863b-a823-426e-aaad-83718465f762.png)
  
## <a name="using-labels-for-records-management"></a>Utilisation d’étiquettes pour la gestion des enregistrements

À un niveau élevé, la gestion des enregistrements implique les points suivants :
  
- Le contenu important est classé comme un enregistrement par les utilisateurs.
    
- Un enregistrement ne peut pas être modifié ou supprimé.
    
- Les enregistrements sont finalement supprimés à l’issue de l’expiration de leur durée de vie.
    
Vous pouvez utiliser des étiquettes pour implémenter une stratégie de gestion des enregistrements simple et cohérente dans Office 365, tandis que les autres fonctionnalités de gestion des enregistrements telles que le Centre des enregistrements s’appliquent uniquement au contenu SharePoint. De plus, vous pouvez entreprendre des actions de rétention sur des enregistrements afin qu’ils soient automatiquement supprimés à la fin de leur cycle de vie.
  
Lorsque vous créez une étiquette, vous pouvez l’utiliser pour classer le contenu en tant qu’enregistrement.
  
![Classification de contenu en tant que case à cocher Enregistrement](media/9c300739-d5d0-41d2-88dd-137f1cfc9cb6.png)
  
Lorsqu’un élément est étiqueté en tant qu’enregistrement, quatre événements se produisent :
  
- L’élément ne peut pas être supprimé définitivement.
    
- L’élément ne peut pas être modifié.
    
- L’étiquette ne peut pas être modifiée.
    
- L’étiquette ne peut pas être supprimée.
    
### <a name="who-can-classify-content-as-a-record"></a>Utilisateur autorisé à classer du contenu en tant qu’enregistrement

Pour le contenu SharePoint, tous les utilisateurs du groupe Membres par défaut (le niveau d’autorisation Collaboration) peuvent appliquer une étiquette d’enregistrement au contenu. Seul l’administrateur de collection de sites peut supprimer ou modifier cette étiquette une fois que celle-ci a été appliquée. Par ailleurs, une étiquette qui classe du contenu en tant qu’enregistrement doit être appliquée manuellement ; elle ne peut pas être appliquée automatiquement.
  
### <a name="records-and-folders"></a>Enregistrements et dossiers

Vous pouvez appliquer une étiquette à un dossier dans Exchange, SharePoint ou OneDrive. Si un dossier est étiqueté en tant qu’enregistrement et que vous déplacez un élément dans le dossier, l’élément est étiqueté en tant qu’enregistrement. Lorsque vous déplacez l’élément hors du dossier, l’élément reste étiqueté en tant qu’enregistrement.
  
### <a name="records-cant-be-deleted"></a>Impossible de supprimer les enregistrements

Si vous tentez de supprimer un enregistrement dans Exchange, l’élément est déplacé vers le dossier Éléments récupérables, comme décrit dans la rubrique [Fonctionnement d’une stratégie de rétention avec du contenu sur place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
Si vous tentez de supprimer un enregistrement dans SharePoint, vous recevez une erreur indiquant que l’élément n’a pas été supprimé, et l’élément reste dans la bibliothèque.
  
![Message indiquant que l’élément n’a pas été supprimé de SharePoint](media/d0020726-1593-4a96-b07c-89b275e75c49.png)
  
Si vous tentez de supprimer un enregistrement dans OneDrive, l’élément est déplacé vers la bibliothèque de conservation et de préservation des documents, comme décrit dans la rubrique [Fonctionnement d’une stratégie de rétention avec du contenu sur place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).
  
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a>Utilisation d’une étiquette comme condition dans une stratégie DLP

Une étiquette peut appliquer des actions de **rétention** sur le contenu. En outre, vous pouvez utiliser une étiquette comme condition dans une stratégie prévention contre la perte de données (DLP). Cela signifie qu’une stratégie DLP peut appliquer des actions de **protection**, telles que la restriction d’accès, au contenu portant une étiquette spécifique. 
  
Pour obtenir plus d’informations, consultez la rubrique [Utilisation d’une étiquette comme condition dans une stratégie DLP](data-loss-prevention-policies.md#using-a-label-as-a-condition-in-a-dlp-policy).
  
## <a name="using-the-label-activity-explorer-and-the-data-governance-reports"></a>Utilisation de l’Explorateur d’activité des étiquettes et des rapports de gouvernance des données

Après avoir publié ou appliqué automatiquement vos étiquettes, vous voudrez vérifier qu’elles s’appliquent correctement au contenu. Pour contrôler vos étiquettes, vous pouvez utiliser les éléments suivants :
  
- **Explorateur d’activité des étiquettes**. Grâce à l’explorateur (voir ci-après), vous pouvez rapidement rechercher et afficher l’activité des étiquettes pour tout le contenu au sein de SharePoint et OneDrive Entreprise au cours des 30 derniers jours. Pour obtenir plus d’informations, consultez l’article [Afficher l’activité des étiquettes pour les documents](view-label-activity-for-documents.md).
    
- **Rapports de gouvernance des données**. Grâce à ces rapports, vous pouvez rapidement afficher les activités et les tendances des étiquettes pour tout le contenu dans Exchange, SharePoint et OneDrive Entreprise au cours des 90 derniers jours. Pour obtenir plus d’informations, consultez l’article [Affichage des rapports de gouvernance des données](view-the-data-governance-reports.md).
    
![Explorateur d’activité des étiquettes](media/671ca0cd-1457-40b4-9917-b663360afd95.png)
  
## <a name="using-content-search-to-find-all-content-with-a-specific-label-applied-to-it"></a>Utilisation de la recherche de contenu pour rechercher tout le contenu portant une étiquette spécifique

Une fois que les étiquettes sont attribuées au contenu, par les utilisateurs ou automatiquement, vous pouvez utiliser la recherche de contenu dans le Centre de sécurité &amp; conformité pour rechercher tout le contenu classé avec une étiquette spécifique.
  
![Page Recherche de contenu](media/564d5dfe-285a-4a7e-800e-907b12a1b273.png)
  
Lorsque vous créez une recherche de contenu, sélectionnez la condition **Balise de conformité**, puis saisissez l’intégralité ou une partie du nom de l’étiquette et utilisez un caractère générique. Pour obtenir plus d’informations, consultez l’article [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).
  
![Condition Balise de conformité](media/82d6af16-59f8-462f-babb-c894b2917018.png)
  
## <a name="the-principles-of-retention-or-what-takes-precedence"></a>Principes de rétention et priorité

Il est possible, voire même probable, que le contenu fasse l’objet de plusieurs stratégies de rétention, chacune avec une action (conservation, suppression ou les deux) et une période de rétention différentes. Laquelle est prioritaire ? Au plus haut niveau, sachez que le contenu conservé par une stratégie ne peut pas être supprimé définitivement par une autre stratégie.
  
![Diagramme des principes de rétention](media/1693d6ec-b340-4805-9da3-89aa41bc6afb.png)
  
Pour comprendre comment les différentes étiquettes avec des actions de rétention s’appliquent au contenu, prenez en compte les principes de rétention suivants :
  
1. **La rétention l’emporte sur la suppression.** Supposons qu’une stratégie de rétention stipule de supprimer la messagerie Exchange au bout de trois ans, mais qu’une autre stratégie de rétention stipule de la conserver pendant cinq ans, puis de la supprimer. Le contenu atteignant trois ans est supprimé et masqué des utilisateurs, mais est conservé dans le dossier Éléments récupérables jusqu’à ce que le contenu atteigne cinq ans, avant d’être définitivement supprimé. 
    
2. **La plus longue période de rétention l’emporte. ** Si du contenu est soumis à plusieurs stratégies de rétention, il est conservé jusqu’à la fin de la période de rétention la plus longue. 
    
3. **L’inclusion explicite l’emporte sur l’inclusion implicite. ** Il faut donc prendre en compte les points suivants : 
    
    1. Si une étiquette avec des paramètres de rétention est attribuée manuellement par un utilisateur à un élément, par exemple, un e-mail Exchange ou un document OneDrive, cette étiquette est prioritaire sur une stratégie assignée au niveau du site ou de la boîte aux lettres et une étiquette par défaut attribuée par la bibliothèque de documents. Par exemple, si l’étiquette explicite stipule que la période de rétention est de dix ans, mais que la stratégie appliquée au site indique que la période de rétention est de cinq ans, l’étiquette est prioritaire. Notez que les étiquettes appliquées automatiquement sont considérées comme implicites et non explicites, car elles sont appliquées automatiquement par Office 365.
    
    2. Si une stratégie de rétention inclut un emplacement spécifique, tel que la boîte aux lettres d’un utilisateur spécifique ou compte OneDrive Entreprise, cette stratégie l’emporte sur une autre stratégie de rétention qui s’applique à l’ensemble des boîtes aux lettres ou des comptes OneDrive Entreprise des utilisateurs, mais n’inclut pas spécifiquement la boîte aux lettres de l’utilisateur en question.
    
4. **La période de suppression la plus courte l’emporte. ** De même, si du contenu est soumis à plusieurs stratégies de suppression (sans aucune rétention), il est supprimé à la fin de la période de rétention la plus courte. 
    
Notez que les principes de rétention opèrent comme un flux de partage du haut vers le bas : si les règles appliquées par toutes les stratégies ou étiquettes sont identiques sur un même niveau, le flux passe au niveau inférieur pour déterminer la règle prioritaire à appliquer.
  
Enfin, une stratégie de rétention ou une étiquette ne peut pas supprimer définitivement du contenu placé en conservation pour eDiscovery. Lorsque cette conservation est levée, le contenu est de nouveau éligible pour le processus de nettoyage décrit ci-dessus.
  
## <a name="use-labels-instead-of-these-features"></a>Utilisation des étiquettes au lieu de ces fonctionnalités

Les étiquettes peuvent facilement être rendues disponibles pour l’ensemble d’une organisation et son contenu dans Office 365, y compris Exchange, SharePoint, OneDrive et les groupes Office 365. Si vous devez classer du contenu ou gérer des enregistrements dans Office 365, nous vous recommandons d’utiliser des étiquettes.
  
Il existe plusieurs autres fonctionnalités utilisées auparavant pour classer du contenu ou gérer des enregistrements dans Office 365. Celles-ci sont répertoriées ci-après. Ces fonctionnalités continuent de fonctionner parallèlement aux étiquettes créées dans le Centre de sécurité &amp; conformité. Notez que, bien qu’il existe des instances où l’implémentation d’étiquettes diffère des fonctionnalités précédentes, la nouvelle génération d’étiquettes préside l’avenir de la gestion des enregistrements dans Office 365. Par conséquent, pour la gouvernance des données, nous vous recommandons d’utiliser des étiquettes plutôt que ces fonctionnalités.
  
### <a name="exchange-online"></a>Exchange Online

- [Balises de rétention et stratégies de rétention](https://go.microsoft.com/fwlink/?linkid=846125), aussi appelées [gestion des enregistrements de messagerie (MRM)](https://go.microsoft.com/fwlink/?linkid=846126) (suppression uniquement) 
    
### <a name="sharepoint-online-and-onedrive-for-business"></a>Sharepoint Online et OneDrive Entreprise

- [Configuration en place de gestion des enregistrements](https://support.office.com/article/7707a878-780c-4be6-9cb0-9718ecde050a) (rétention) 
    
- [Présentation du Centre des enregistrements](https://support.office.com/article/bae6ca5a-7b19-40e0-b433-e3613a747c2c) (rétention) 
    
- [Stratégies de gestion des informations](intro-to-info-mgmt-policies.md) (suppression uniquement) 
    
## <a name="permissions"></a>Autorisations

Les membres de votre équipe de conformité appelés à créer des étiquettes nécessitent des autorisations pour le Centre de sécurité &amp; conformité. Par défaut, votre administrateur client a accès à cet emplacement et peut accorder l’accès aux responsables de la mise en conformité et à d’autres personnes au Centre de sécurité &amp; conformité, sans leur donner toutes les autorisations d’un administrateur client. Pour ce faire, nous vous recommandons d’accéder à la page **Autorisations** du Centre de sécurité &amp; conformité, de modifier le groupe de rôles **Administrateur de conformité** et d’ajouter des membres à ce groupe de rôles. 
  
Pour obtenir plus d’informations, consultez l’article [Octroi de l’accès au Centre de sécurité &amp; conformité Office 365 aux utilisateurs](grant-access-to-the-security-and-compliance-center.md).
  
Ces autorisations sont requises uniquement pour créer et appliquer des étiquettes et une stratégie d’étiquette. L’application d’une stratégie ne nécessite pas d’accès au contenu.
  
## <a name="find-the-powershell-cmdlets-for-labels"></a>Trouver les cmdlets PowerShell pour les étiquettes

Pour utiliser les cmdlets, vous devez effectuer les actions suivantes :
  
1. [Se connecter au Centre de sécurité &amp; conformité Office 365 à l’aide de PowerShell à distance](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Utiliser ces [cmdlets du Centre de sécurité &amp; conformité Office 365](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
## <a name="more-information"></a>Plus d’informations

- [Vue d’ensemble des stratégies de rétention](retention-policies.md)
    

