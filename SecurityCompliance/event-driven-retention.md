---
title: Vue d’ensemble des rétentions basées sur des événements
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Dans Office 365, vous pouvez baser une période de rétention sur l’occurrence d’un type spécifique d’événement grâce aux étiquettes. L’événement déclenche le début de la période de rétention, et les actions de rétention d’une étiquette sont appliquées sur tout le contenu portant l’étiquette en question pour ce type d’événement. Les rétentions basées sur des événements sont généralement utilisées dans le cadre d’un processus de gestion des enregistrements.
ms.openlocfilehash: ceb4b2fde10e43235d8d310243fe56cce1a2b240
ms.sourcegitcommit: a79eb9907759d4cd849c3f948695a9ff890b19bf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2019
ms.locfileid: "30866360"
---
# <a name="overview-of-event-driven-retention"></a>Vue d’ensemble des rétentions basées sur des événements

Lorsque vous conservez du contenu, la période de rétention est souvent basée sur l’ancienneté du contenu. Par exemple, vous pouvez conserver des documents pendant sept ans à compter de leur création, puis les supprimer. Cependant, dans Office 365, vous pouvez baser une période de rétention sur l’occurrence d’un type spécifique d’événement grâce aux étiquettes. L’événement déclenche le début de la période de rétention, et les actions de rétention d’une étiquette sont appliquées sur tout le contenu portant l’étiquette en question pour ce type d’événement.
  
Par exemple, vous pouvez utiliser des étiquettes avec des rétentions basées sur des événements pour les éléments suivants :
  
- **Employés quittant l’organisation** Supposons que les enregistrements d’un employé doivent être conservés pendant 10 ans après le départ de l’employé en question de l’organisation. Après un délai de 10 ans, tous les documents liés à l’embauche, aux performances et à la cessation d’emploi de cet employé doivent être supprimés. L’événement qui déclenche la période de rétention de 10 ans est le départ de l’employé de l’organisation. 
    
- **Expiration des contrats** Supposons que tous les enregistrements liés aux contrats doivent être conservés pendant cinq ans à compter de l’expiration du contrat. L’événement qui déclenche la période de rétention de cinq ans est l’expiration du contrat. 
    
- **Durée de vie des produits** Votre organisation a peut-être des exigences de rétention liées à la dernière date de fabrication de produits pour le contenu tel que des spécifications techniques. Dans ce cas, la dernière date de fabrication est l’événement qui déclenche la période de rétention. 
    
Les rétentions basées sur des événements sont généralement utilisées dans le cadre d’un processus de gestion des enregistrements. Il faut alors prendre en compte les points suivants :
  
- Les étiquettes basées sur des événements classent aussi généralement du contenu en tant qu’enregistrement. Pour obtenir plus d’informations, consultez la rubrique [Utilisation de la recherche de contenu pour trouver tout le contenu portant une étiquette spécifique](labels.md#using-content-search-to-find-all-content-with-a-specific-retention-label-applied-to-it).
    
- Un document qui a été déclaré comme enregistrement, mais dont l’événement déclencheur ne s’est pas encore produit, est conservé indéfiniment (les enregistrements ne peuvent pas être supprimés définitivement) jusqu’à ce qu’un événement déclenche la période de rétention du document en question.
    
- Les étiquettes basées sur des événements déclenchent généralement une révision de destruction à la fin de la période de rétention afin qu’un gestionnaire d’enregistrements puisse manuellement examiner et supprimer le contenu. Pour obtenir plus d’informations, consultez l’article [Vue d’ensemble des révisions de destruction](disposition-reviews.md).
    
Une étiquette basée sur un événement a les mêmes fonctionnalités que les étiquettes dans Office 365. Pour obtenir plus d’informations, consultez l’article [Vue d’ensemble des étiquettes](labels.md).
    
## <a name="understanding-the-relationship-between-event-types-labels-events-and-asset-ids"></a>Compréhension de la relation entre les types d’événements, les étiquettes, les événements et les ID d’élément

Pour utiliser correctement les rétentions basées sur des événements, il est important de comprendre la relation entre les types d’événements, les étiquettes, les événements et les ID d’élément comme illustré ci-dessous. Vous trouverez une explication après le diagramme.
  
![Diagramme illustrant le type d’événement, les étiquettes, les événements et les ID d’élément](media/a5141a6b-61ca-4a60-9ab0-24e6bb45bbdb.png)
  
![Diagramme illustrant le type d’événement, les étiquettes, les événements et les ID d’élément](media/ce89a91f-49aa-4b5a-933c-ac3a13dccd5d.png)
  
1. Créez des étiquettes pour différents types de contenu et associez-les à un type d’événement. Par exemple, les étiquettes pour différents types de fichiers et d’enregistrements de produit sont associées à un type d’événement nommé Durée de vie des produits, car ces enregistrements doivent être conservés pendant 10 ans à compter de la fin de vie du produit.
    
2. Les utilisateurs (généralement des gestionnaires d’enregistrements) appliquent ces étiquettes au contenu et saisissent un ID d’élément pour chaque élément (pour les documents SharePoint et OneDrive). Dans cet exemple, l’ID d’élément est un nom de produit ou un code utilisé par l’organisation. Par conséquent, une étiquette est appliquée aux enregistrements de chaque produit, et chaque enregistrement a une propriété qui contient un ID d’élément. Le diagramme représente **tout le contenu** pour tous les enregistrements de produit dans une organisation, et chaque élément porte l’ID d’élément du produit de l’enregistrement dont il s’agit. 
    
3. Durée de vie des produits est le type d’événement ; un produit spécifique qui arrive en fin de vie est un événement. Lorsqu’un événement de ce type d’événement se produit (dans ce cas, quand un produit arrive en fin de vie), créez un événement qui spécifie les éléments suivants :
    
  - Un ID d’élément (pour les documents SharePoint et OneDrive).
    
  - Des mots clés (pour les éléments Exchange) Dans cet exemple, l’organisation utilise un code de produit dans les messages contenant des enregistrements de produit. Le mot clé pour les éléments Exchange est donc identique à l’ID d’élément pour les documents SharePoint et OneDrive.
    
  - La date à laquelle l’événement est survenu. Cette date est utilisée comme point de départ de la période de rétention. Cette date ne peut être que la date actuelle ou une date future, pas une date passée.
    
4. Une fois que vous avez créé un événement, la date de cet événement est synchronisée avec tout le contenu portant une étiquette de ce type d’événement et qui contient le mot clé ou l’ID d’élément spécifié. Comme pour toute étiquette, cette synchronisation peut prendre jusqu’à 7 jours. Dans le diagramme ci-dessus, la période de rétention de tous les éléments entourés en rouge est déclenchée par cet événement. En d’autres termes, quand ce produit arrive en fin de vie, cet événement déclenche la période de rétention pour les enregistrements de ce produit.
    
Il est important de comprendre que si vous ne spécifiez aucun mot clé ou ID d’élément pour un événement, la période de rétention de **tout le contenu** portant une étiquette de ce type d’événement est déclenchée par l’événement. Cela signifie que dans le diagramme ci-dessus, la conservation serait déclenchée pour tout le contenu. Ce n’est peut-être pas ce que vous souhaitez faire. 
  
Enfin, n’oubliez pas que chaque étiquette a ses propres paramètres de rétention. Dans cet exemple, ils indiquent tous 10 ans, mais il est possible qu’un événement déclenche des étiquettes dont la période de rétention est différente.
  
## <a name="how-to-set-up-event-driven-retention"></a>Configuration des rétentions basées sur des événements

Voici le niveau le plus haut du flux de travail pour la rétention basée sur des événements. Vous trouverez les étapes détaillées ci-après.
  
![Diagramme du flux de travail de la configuration des rétentions basées sur des événements](media/161146d9-e0fc-4248-abc1-a18045eaad5c.png)
  
### <a name="step-1-create-a-label-whose-retention-period-is-based-on-an-event"></a>Étape 1 : créer une étiquette dont la période de rétention est basée sur des événements

Dans le Centre de sécurité &amp; conformité, dans le volet de navigation de gauche, sous **Classifications**, sélectionnez **Étiquettes** \> **Créer une étiquette**.
  
Lorsque vous créez l’étiquette, activez la rétention, puis sélectionnez l’option indiquée ci-dessous pour conserver ou supprimer le contenu basé sur un événement. Cela signifie que les paramètres de rétention ne rentrent pas en vigueur avant l’étape 5, lorsque vous créez un événement sur la page **Événements**. 
  
Notez que les rétentions basées sur des événements sont généralement utilisées pour le contenu classé comme enregistrement. Pour cette raison, lorsque vous créez des étiquettes basées sur un événement, vous choisissez généralement l’option pour **utiliser une étiquette pour classer le contenu en tant que « Enregistrement »**.
  
Notez également que les rétentions basées sur des événements requièrent des paramètres de rétention qui :
  
- Conservent le contenu.
    
- suppriment automatiquement le contenu ou déclenchent une révision de destruction à la fin de la période de rétention.
    
![Option pour baser une étiquette sur un événement](media/a4902281-5196-4194-9737-f30231d95861.png)
  
### <a name="step-2-choose-an-event-type-for-that-label"></a>Étape 2 : choisir un type d’événement pour cette étiquette

Dans les paramètres d’étiquette, après avoir choisi l’option pour baser l’étiquette sur **un événement**, vous pourrez sélectionner l’option **Choisir un type d’événement**. Un type d’événement est simplement une description générale d’un événement auquel vous voulez associer une étiquette.
  
Par exemple, si vous créez un type d’événement nommé Durée de vie des produits, vous allez créer des étiquettes basées sur un événement avec des noms qui décrivent les types de contenu auxquels vous souhaitez appliquer des étiquettes. Par exemple, « Fichiers de développement des produits » ou « Enregistrements de la décision commerciale des produits ».
  
Notez qu’une fois que vous sélectionnez un type d’événement et créez l’étiquette, le type d’événement ne peut pas être modifié.
  
![Options permettant de créer ou de sélectionner un type d’événement](media/8b7afe79-72cb-462e-81d4-b5ddbe899dbc.png)
  
### <a name="step-3-publish-or-auto-apply-the-label"></a>Étape 3 : publier ou appliquer automatiquement l’étiquette

Comme pour toute étiquette, vous devez publier ou appliquer automatiquement une étiquette basée sur un événement afin qu’elle soit appliquée manuellement ou automatiquement au contenu. Faites-le sur la page **Étiquettes**. Notez que les étiquettes qui classent le contenu en tant qu’enregistrement peuvent être uniquement publiées et appliquées manuellement au contenu ; elles ne peuvent pas être appliquées automatiquement au contenu. 
  
![Options permettant de publier ou d’appliquer automatiquement une étiquette](media/c9232c54-bbc0-40d2-abc2-122d5d1e70af.png)
  
### <a name="step-4-enter-an-asset-id"></a>Étape 4 : saisissez un ID d’élément

Une fois qu’une étiquette basée sur un événement a été appliquée au contenu, vous pouvez entrer un ID d’élément pour chaque élément. Par exemple, votre organisation peut utiliser :
  
- Des codes de produit que vous pouvez utiliser pour conserver le contenu relatif à un produit spécifique.
    
- Des codes de projet que vous pouvez utiliser pour conserver le contenu relatif à un projet spécifique.
    
- ID d’employé à utiliser pour conserver uniquement le contenu d’une personne spécifique.
    
Il faut comprendre que la propriété ID d’élément est tout simplement une autre propriété de document dans SharePoint et OneDrive Entreprise. Votre organisation utilise peut-être déjà d’autres propriétés de document et d’ID pour classer le contenu. Si tel est le cas, vous pouvez également utiliser ces propriétés et valeurs lorsque vous créez un événement : consultez l’étape 6 ci-dessous. L’essentiel est que votre organisation doit utiliser une association propriété:valeur dans les propriétés du document pour associer cet élément à un type d’événement.
  
![Zone de texte pour saisir un ID d’élément](media/6d31628e-7162-4370-a8d7-de704aafa350.png)
  
### <a name="step-5-create-an-event"></a>Étape 5 : créer un événement

Lorsqu’une instance précise de ce type d’événement se produit (par exemple, un produit arrive en fin de vie), accédez à la page Événements dans le Centre de sécurité &amp; conformité, et créez un événement. Vous devez déclencher manuellement un événement en le créant.
  
![Page Événements dans le Centre de sécurité et conformité](media/811bddfb-a7e9-4990-bf5e-abe0dfb91809.png)
  
### <a name="step-6-choose-the-same-event-type-used-by-the-label-in-step-2"></a>Étape 6 : choisir le même type d’événement utilisé par l’étiquette à l’étape 2

Lorsque vous créez l’événement, sélectionnez le type d’événement utilisé par l’étiquette à l’étape 2 : par exemple, Durée de vie des produits. Seule la période de rétention du contenu portant les étiquettes de ce type d’événement sera déclenchée.
  
![Option dans les paramètres d’événement permettant de choisir un type d’événement](media/11663591-5628-419e-9537-61eb8f5c741f.png)
  
### <a name="step-7-enter-keywords-or-an-asset-id"></a>Étape 7 : saisir des mots clés ou un ID d’élément

Réduisez désormais l’étendue du contenu en spécifiant les ID d’élément pour le contenu SharePoint et OneDrive ou des mots clés pour le contenu Exchange. Pour les ID d’élément, la rétention est appliquée uniquement pour le contenu portant la paire propriété:valeur spécifiée. Si un ID d’élément n’est pas saisi, **tout le contenu** portant des étiquettes de ce type d’événement obtient la même date de rétention qui leur est appliquée. 
  
Il faut comprendre que l’ID d’élément est simplement une autre propriété du document dans SharePoint et OneDrive Entreprise. Si vous utilisez la propriété AssetID, vous devez saisir ComplianceAssetID:\<valeur\> dans la zone des ID d’élément illustrée ci-dessous.
  
Votre organisation a peut-être appliqué d’autres propriétés et ID aux documents liés à ce type d’événement. Par exemple, si vous avez besoin de détecter les enregistrements d’un produit spécifique, l’ID peut être une combinaison de votre propriété personnalisée ProductID et de la valeur « XYZ ». Dans ce cas, vous devez saisir ProductID:XYZ dans la zone pour des ID d’élément illustrée ci-dessous.
  
Pour les éléments Exchange, vous pouvez inclure des mots clés. Vous pouvez affiner votre requête à l’aide d’opérateurs de recherche comme AND, OR et NOT. Pour obtenir plus d’informations sur les opérateurs, consultez l’article [Requêtes par mots clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).
  
Enfin, sélectionnez la date à laquelle l’événement est survenu. Cette date est utilisée comme point de départ de la période de rétention. Après avoir créé un événement, la date de cet événement est synchronisée avec tout le contenu portant une étiquette de ce type d’événement, de cet ID d’élément et de ces mots clés. Comme pour toute étiquette, cette synchronisation peut prendre jusqu’à 7 jours.
  
![Page Paramètres des événements](media/40d3c9db-f624-49a5-b38a-d16bcce20231.png)
  
## <a name="use-content-search-to-find-all-content-with-a-specific-label-or-asset-id"></a>Utilisation de la recherche de contenu pour rechercher tout le contenu portant une étiquette ou un ID d’élément spécifique

Une fois que les étiquettes sont attribuées au contenu, vous pouvez utiliser la recherche de contenu dans le Centre de sécurité &amp; conformité pour rechercher tout le contenu classé avec une étiquette spécifique ou qui contient un ID d’élément spécifique.
  
Lorsque vous créez une recherche de contenu, procédez comme suit :
  
- Pour trouver tout le contenu portant une étiquette spécifique, sélectionnez la condition **Balise de conformité**, puis saisissez le nom d’étiquette en partie ou en intégralité et utilisez un caractère générique. 
    
- Pour trouver tout le contenu portant un ID d’élément spécifique, saisissez la propriété **ComplianceAssetID** et une valeur, telle que ComplianceAssetID:\<valeur\>. 
    
Pour obtenir plus d’informations, reportez-vous à la rubrique [Requêtes par mots-clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).
  
## <a name="permissions"></a>Autorisations

Pour accéder à la page **Événements**, les réviseurs doivent être membres du groupe de rôles possédant le rôle **Gestion de la destruction** et le rôle **Journaux d’audit en lecture seule**. Nous vous recommandons de créer un nouveau groupe de rôles appelé Réviseurs de destruction, d’ajouter ces deux rôles à ce groupe de rôles, puis d’ajouter des membres au groupe de rôles. 
  
Pour obtenir plus d’informations, consultez l’article [Octroi de l’accès au Centre de sécurité &amp; conformité Office 365 aux utilisateurs](grant-access-to-the-security-and-compliance-center.md).
  
## <a name="automate-events-by-using-powershell"></a>Automatisation des événements à l’aide de PowerShell

Dans le centre de sécurité &amp; conformité Office 365, vous pouvez uniquement créer des événements manuellement ; il n’est pas possible de déclencher automatiquement un événement lorsqu’il se produit. Toutefois, vous pouvez utiliser un script PowerShell pour automatiser les rétentions basées sur des événements à partir de vos applications métier.
  
Nous travaillons actuellement sur les API afin que vous puissiez connecter vos applications métier (par exemple, RH, CRM ou des applications financières) aux rétentions basées sur des événements. Par exemple, vous pourrez connecter votre système de RH aux rétentions basées sur des événements. Ainsi, lorsqu’un employé quitte l’organisation, l’événement de ce type d’événement se déclenche automatiquement.
  
En attendant, voici les cmdlets PowerShell disponibles pour les rétentions basées sur des événements :
  
- [Get-ComplianceRetentionEventType](https://go.microsoft.com/fwlink/?linkid=873002)
    
- [New-ComplianceRetentionEventType](https://go.microsoft.com/fwlink/?linkid=873004)
    
- [Remove-ComplianceRetentionEventType](https://go.microsoft.com/fwlink/?linkid=873005)
    
- [Set-ComplianceRetentionEventType](https://go.microsoft.com/fwlink/?linkid=873006)
    
- [Get-ComplianceRetentionEvent](https://go.microsoft.com/fwlink/?linkid=873001)
    
- [New-ComplianceRetentionEvent](https://go.microsoft.com/fwlink/?linkid=873003)
    

