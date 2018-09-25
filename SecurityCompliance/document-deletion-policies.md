---
title: Vue d’ensemble des stratégies de suppression de documents
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/12/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 55e8d858-f278-482b-a198-2e62d6a2e6e5
description: Votre organisation peut être nécessaire de conserver des documents pour une période de temps en raison de la conformité, juridique, ou autres besoins. Toutefois, si votre organisation conserve les documents plus longtemps que nécessaire, vous créez un risque juridique inutile. Avec une stratégie de suppression de documents, vous pouvez réduire proactive des risques en supprimant des documents dans un site après une période de temps spécifique, par exemple, vous pouvez supprimer les documents dans OneDrive des utilisateurs pour les professionnels sites cinq ans après les documents ont été créés.
ms.openlocfilehash: 7af818dd7d9dd87eb671bdd86ef03e0b5dead1e2
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002667"
---
# <a name="overview-of-document-deletion-policies"></a>Vue d’ensemble des stratégies de suppression de documents

> [!IMPORTANT]
> Aller plus loin, nous vous conseillons d’utiliser une stratégie de rétention ou étiquettes créées dans la sécurité &amp; centre de conformité au lieu d’une stratégie de suppression de documents. Stratégies de suppression de documents continueront de fonctionner en côte à côte des stratégies de rétention, mais si vous devez conserver ou supprimer du contenu n’importe où dans Office 365, nous vous conseillons d’utiliser une stratégie de rétention. Pour plus d’informations, voir [utiliser une stratégie de rétention au lieu de ces fonctionnalités](retention-policies.md#use-a-retention-policy-instead-of-these-features).
  
Votre organisation peut être nécessaire de conserver des documents pour une période de temps en raison de la conformité, juridique, ou autres besoins. Toutefois, si votre organisation conserve les documents plus longtemps que nécessaire, vous créez un risque juridique inutile. Avec une stratégie de suppression de documents, vous pouvez réduire proactive des risques en supprimant des documents dans un site après une période de temps spécifique, par exemple, vous pouvez supprimer les documents dans OneDrive des utilisateurs pour les professionnels sites cinq ans après les documents ont été créés.
  
Stratégies de suppression de documents sont puissants et flexible — par exemple, vous pouvez :
  
- permettre aux propriétaires de sites de choisir parmi les stratégies que vous créez et gérez de manière centralisée ; permettre également aux propriétaires de sites de refuser complètement s’ils décident qu’une stratégie ne s’applique pas à leur contenu ;
    
- appliquer une stratégie unique obligatoire sur tous les sites d’une collection de sites, comme tous les sites OneDrive Entreprise, ou même appliquer une stratégie sur toutes les collections de sites créées à partir d’un modèle de collection de sites spécifique, tel que le modèle du site d’équipe ;
    
- fournir une stratégie par défaut avec une règle par défaut qui sera appliquée automatiquement sans aucune action requise par les propriétaires de sites ;
    
- créer une stratégie qui inclut plusieurs règles de suppression parmi lesquelles un propriétaire de site peut effectuer son choix.
    
Créer et gérer des stratégies de suppression de documents en utilisant le centre de stratégie de suppression de Document, vous pouvez trouver sous **rétention** de sécurité Office 365 &amp; centre de conformité. Vous pouvez également créer manuellement en fonction [de la collection de sites](https://go.microsoft.com/fwlink/p/?LinkID=404342) **Centre de stratégie de conformité** sur l’onglet **entreprise** , le centre de stratégie. Chaque client peut avoir qu’un seul centre de stratégie de suppression de documents, et il vous aurez créé automatiquement si vous démarrez à partir de la sécurité &amp; centre de conformité. 
  
![Page d’accueil du centre de stratégies de suppression de documents](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="when-to-use-document-deletion-policies"></a>Quand utiliser les stratégies de suppression de documents

En plus des stratégies de suppression de documents, Office 365 fournit les stratégies de rétention suivantes pour le contenu de site :
  
- [Gestion des enregistrements](https://go.microsoft.com/fwlink/p/?LinkID=404250)
    
- [Stratégies de gestion des informations pour les types de contenu, des listes et bibliothèques](https://go.microsoft.com/fwlink/p/?LinkID=404239)
    
- [Stratégies de site](https://go.microsoft.com/fwlink/p/?LinkID=404242)
    
Chaque type de stratégie convient le mieux pour un type spécifique de site ou de données. Par exemple, votre organisation peut avoir un site hautement structuré qui utilise des types de contenu tels qu’un site financier pour des contrats ou une base de connaissances pour des articles. Dans ce cas, vous pouvez utiliser des stratégies de type de contenu. Il se peut que votre organisation doive conserver des documents juridiques et, dans ce cas, vous pouvez utiliser des types de contenu et un centre des enregistrements pour mettre en œuvre un plan de gestion de fichiers.
  
Stratégies de suppression de documents ne remplacent enregistrements gestion ou informations stratégies de gestion, qui convient mieux aux types de contenu et les données structurées. Au lieu de cela, vous devez utiliser des stratégies de suppression de documents lorsque vous avez besoin gérer largement la suppression automatique des données non structurées telles que OneDrive pour les sites et les sites d’équipe.
  
![Schéma montrant les options de rétention pour le contenu du site](media/IP-Retention-policies-for-site-content.png)
  
Si vous appliquez une stratégie de suppression de documents à un site qui utilise déjà des stratégies de type de contenu ou des stratégies de gestion des informations pour une liste ou une bibliothèque, ces stratégies sont ignorées alors que la stratégie de suppression de documents est appliquée. Cela signifie que vous devez prévoir qu’un site n’utilise que des stratégies destinées à du contenu structuré ou non structuré, et non les deux. Pour plus d’informations sur la façon dont les stratégies de suppression de documents remplacent d’autres stratégies, consultez la rubrique [Apply or remove a document deletion policy for a site](apply-or-remove-a-document-deletion-policy-for-a-site.md).
  
Contrairement à d’autres stratégies, les stratégies de suppression de documents fonctionnent uniquement sur les bibliothèques de documents, et non sur les listes.
  
## <a name="deletion-policies-and-rules"></a>Règles et stratégies de suppression

Une stratégie de suppression de documents contient une ou plusieurs règles de suppression qui spécifient :
  
- la période de temps jusqu’à la suppression ;
    
- si la date de suppression doit être calculée à partir de la date de création du document ou de la date de dernière modification ;
    
- si le document doit être supprimé de manière permanente ou placé dans la Corbeille.
    
Si une stratégie contient plusieurs règles, les propriétaires de sites peuvent choisir la règle qui s’applique le mieux à leur contenu.
  
![Page Nouvelle règle de suppression](media/IP-New-deletion-rule.png)
  
## <a name="policies-and-assignments"></a>Stratégies et affectations

Après avoir créé une stratégie de suppression de documents, vous pouvez l’affecter à un modèle de collection de sites —, par exemple, vous pouvez affecter une stratégie pour le modèle d’entreprise OneDrive afin qu’elle comprenne les sites de OneDrive de tous les utilisateurs. Lorsque vous affectez une stratégie à un modèle de collection de sites, cela s’applique à toutes les collections de sites déjà créées à partir de ce modèle, en plus des collections de sites créés à partir de ce modèle à l’avenir.
  
![Page Choisir un modèle affichant l’option OneDrive](media/IP-Choose-a-template.png)
  
Vous pouvez également affecter une stratégie à une collection de sites spécifique pour remplacer toutes les stratégies affectées à ce modèle de collection de sites. Par exemple, vous pouvez affecter des stratégies au modèle de site d’équipe, mais les remplacer ensuite en appliquant un ensemble de stratégies différent à une collection de sites spécifique créée à partir de ce modèle.
  
### <a name="one-mandatory-policy-or-several-policies-to-choose-from"></a>Une stratégie obligatoire ou un éventail de plusieurs stratégies dans lequel effectuer un choix

Lorsque vous affectez une stratégie, vous pouvez la rendre obligatoire pour que seule cette stratégie puisse être affectée et appliquée à tous les sites de la collection de sites. Les propriétaires de sites ne peuvent pas refuser une stratégie obligatoire, ce qui signifie que les documents du site seront soumis à la stratégie de suppression, quelle qu’elle soit.
  
Au lieu de rendre une stratégie unique obligatoire, vous pouvez aussi affecter plusieurs stratégies à une collection de sites, ce qui permet à chaque propriétaire de site de choisir la stratégie à appliquer à son site, ou même de la refuser complètement. Par exemple, vous pouvez créer une stratégie pour des documents commerciaux généraux et une autre stratégie pour des documents financiers ayant une planification de rétention différente. Un propriétaire de site connaît souvent mieux le contenu de son site et donc la stratégie de suppression de documents à appliquer. Chaque site ne peut avoir qu’une seule stratégie qui lui est appliquée.
  
### <a name="one-rule-or-several-rules-to-choose-from"></a>Une règle ou plusieurs règles parmi lesquelles choisir

À son tour, chaque stratégie peut contenir plusieurs règles — par exemple, une stratégie de suppression des documents d’entreprise général peut avoir deux règles :
  
- Les documents qui n’est pas nécessaire de rétention basée sur les obligations légales ou en cours ne doivent pas être conservés pendant plus d’un an à partir de la création.
    
- les documents nécessaires pour une utilisation commerciale active en cours qui sont requis pendant plus d’un an, ne doivent pas être conservés plus de trois ans après leur création.
    
Un propriétaire de site peut déterminer que leur site contient comptabilisation documents, sélectionnez cette stratégie de suppression, puis sélectionnez la règle appropriée dans la stratégie. Vous pouvez uniquement sélectionner une règle de la stratégie qui est actuellement appliquée au site (pas de toute stratégie) et la règle s’applique à toutes les bibliothèques de documents dans le site.
  
## <a name="the-relationship-of-site-collections-policies-and-rules"></a>Relation entre les collections de sites, les stratégies et les règles

La relation de base est la suivante :
  
Une collection de sites ou d’un modèle de collection de sites peut avoir une ou plusieurs stratégies qui lui est affectés et chacune de ces stratégies peut avoir une ou plusieurs règles. Toutefois, il peut y avoir qu’une seule stratégie est active par site, et il peut y avoir qu’une seule règle de suppression qui est active à tout moment pour les bibliothèques au sein du site.
  
![Schéma montrant la relation entre les stratégies](media/IP-Two-policies-four-rules.png)
  
## <a name="document-deletion-policies-are-inherited"></a>Les stratégies de suppression de documents sont héritées

Comme les autorisations, la navigation et de nombreuses autres fonctionnalités de site, les stratégies de suppression de documents sont héritées. Un propriétaire de site peut sélectionner une stratégie de suppression de documents pour son site, et tous les sous-sites héritent de la stratégie du parent. Le propriétaire d’un sous-site peut annuler l’héritage en sélectionnant une stratégie et une règle différentes, et cette stratégie s’applique à tous les sous-sites tant que l’héritage n’est pas de nouveau annulé.
  
## <a name="assigning-document-deletion-policies-for-the-first-time"></a>Première affectation de stratégies de suppression de documents

Il est important de comprendre que la période de temps spécifiée pour un document de stratégie de suppression signifie l’heure dans la mesure où le document a été créé ou modifié, pas l’heure dans la mesure où la stratégie a été attribuée. Par exemple, vous pourrez créer une stratégie de suppression de documents qui supprime définitivement les documents deux ans après que qu’ils ont été créés, puis assigner cette stratégie à un modèle de collection de sites à partir de laquelle plusieurs collections de sites créées à quatre ou cinq ans. Dans ce cas, il est probable que les collections de sites existantes contiennent de nombreux documents qui sont déjà plus anciens que les deux années spécifiées par la stratégie de suppression, cela signifie beaucoup de contenu est supprimé après attribution de la stratégie de suppression de documents pour la première heure.
  
Lorsque vous affectez la stratégie pour la première fois, tous les documents du site sont évalués et supprimés s’ils répondent aux critères. Cela s’applique à tous les documents existants, et non simplement aux documents créés depuis l’affectation de la stratégie. Et n’oubliez pas que la période de temps est liée à l’âge de chaque document, et non au moment de la première affectation de la stratégie.
  
Par conséquent, avant d’affecter une stratégie à un site pour la première fois, vous devez d’abord tenir compte de l’âge du contenu existant et de la façon dont la stratégie peut avoir une incidence sur le contenu existant. Vous pouvez également communiquer la nouvelle stratégie aux propriétaires de sites avant de l’affecter, pour leur donner le temps d’évaluer les incidences éventuelles.
  
## <a name="time-lag-for-propagating-policies"></a>Décalage de la propagation des stratégies

Une fois que vous avez affecté des stratégies à une collection de sites, les propriétaires de sites utilisent le lien **Stratégies de suppression de documents** sur la page **Paramètres du site** pour afficher et appliquer les stratégies disponibles pour le site. 
  
Le lien **Stratégies de suppression de documents** n’apparaît pas, sauf si les stratégies ont été affectées à la collection de sites. En outre, le lien ne s’affiche pas immédiatement une fois que les stratégies ont été affectées au site, il peut prendre jusqu'à 24 heures à partir de lorsque les stratégies sont attribuées aux lorsque le lien **Stratégies de suppression de documents** apparaît. 
  
## <a name="permissions"></a>Autorisations

Les membres de votre équipe de conformité qui utiliseront le centre de stratégies de suppression de documents doivent disposer d’autorisations d’accès à la fois au centre de stratégies et aux collections de sites auxquels des stratégies seront appliquées. Nous vous recommandons de :
  
1. Créer un groupe de sécurité qui contient tous les utilisateurs du centre de stratégie de suppression de documents — probablement votre équipe de gestion des stratégies de conformité. Pour plus d’informations, voir [Groupes de sécurité Manage Mail-Enabled](https://go.microsoft.com/fwlink/p/?LinkID=404345) . 
    
2. Dans le centre de stratégie de suppression de documents, affecter la collection de sites, des autorisations de propriétaire au groupe de sécurité. Pour plus d’informations, consultez la rubrique [autorisations pour les administrateurs de collection de sites](https://go.microsoft.com/fwlink/p/?LinkID=404346) . 
    
3. Dans chaque collection de sites à laquelle vous devez affecter des stratégies de suppression de documents, affectez des autorisations de propriétaire de collection de sites au groupe de sécurité.
    
## <a name="how-document-deletion-policies-work-with-hold-policies"></a>Fonctionnement des stratégies de suppression de documents avec des stratégies de blocage

Une stratégie de blocage garantit que tout le contenu est conservé pendant une période de temps donnée, tandis qu’une stratégie de suppression de documents garantit que tout le contenu est supprimé après une période de temps spécifique.
  
Si vous devez conserver des documents pendant une période de temps fixe, vous pouvez utiliser une stratégie de blocage avec une stratégie de suppression. Par exemple, vous pourriez bloquer des documents pendant trois ans après leur modification, puis configurer une stratégie de suppression pour supprimer ces documents trois ans après leur dernière modification.
  
Notez qu’une stratégie de suppression ne peut pas substituer un blocage. Si un site est bloqué et qu’une stratégie de suppression supprime un document, le document sera conservé dans la bibliothèque de conservation comme s’il avait été supprimé manuellement.
  
## <a name="see-also"></a>Voir aussi

[Application ou suppression d’une stratégie de suppression de documents pour un site](apply-or-remove-a-document-deletion-policy-for-a-site.md)

[Création d’une stratégie de suppression de documents](create-a-document-deletion-policy.md)


