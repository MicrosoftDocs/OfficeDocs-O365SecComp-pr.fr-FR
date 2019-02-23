---
title: Vue d’ensemble des stratégies de suppression de documents
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/12/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 55e8d858-f278-482b-a198-2e62d6a2e6e5
description: Votre organisation peut être amenée à conserver des documents pendant une période de temps en raison de la conformité, de la légalité ou d'autres exigences professionnelles. Toutefois, si votre organisation conserve les documents plus longtemps que nécessaire, vous risquez de créer des risques légaux inutiles. Avec une stratégie de suppression de documents, vous pouvez réduire de manière proactive les risques en supprimant des documents dans un site après une période de temps spécifique (par exemple, vous pouvez supprimer des documents dans les sites OneDrive entreprise de l'utilisateur cinq ans après la création des documents).
ms.openlocfilehash: 9f1355e8a522900aa47ef20ef580918ab5584b99
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218434"
---
# <a name="overview-of-document-deletion-policies"></a>Vue d’ensemble des stratégies de suppression de documents

> [!IMPORTANT]
> Pour aller plus loin, nous vous recommandons d'utiliser une stratégie de rétention ou &amp; des étiquettes créées dans le centre de sécurité conformité au lieu d'une stratégie de suppression de documents. Les stratégies de suppression de documents continueront à fonctionner côte à côte avec des stratégies de rétention, mais si vous devez conserver ou supprimer du contenu n'importe où dans Office 365, nous vous recommandons d'utiliser une stratégie de rétention. Pour plus d'informations, consultez [la rubrique utiliser une stratégie de rétention au lieu de ces fonctionnalités](retention-policies.md#use-a-retention-policy-instead-of-these-features).
  
Votre organisation peut être amenée à conserver des documents pendant une période de temps en raison de la conformité, de la légalité ou d'autres exigences professionnelles. Toutefois, si votre organisation conserve les documents plus longtemps que nécessaire, vous risquez de créer des risques légaux inutiles. Avec une stratégie de suppression de documents, vous pouvez réduire de manière proactive les risques en supprimant des documents dans un site après une période de temps spécifique (par exemple, vous pouvez supprimer des documents dans les sites OneDrive entreprise de l'utilisateur cinq ans après la création des documents).
  
Les stratégies de suppression de documents sont puissantes mais flexibles, par exemple, vous pouvez:
  
- permettre aux propriétaires de sites de choisir parmi les stratégies que vous créez et gérez de manière centralisée ; permettre également aux propriétaires de sites de refuser complètement s’ils décident qu’une stratégie ne s’applique pas à leur contenu ;
    
- appliquer une stratégie unique obligatoire sur tous les sites d’une collection de sites, comme tous les sites OneDrive Entreprise, ou même appliquer une stratégie sur toutes les collections de sites créées à partir d’un modèle de collection de sites spécifique, tel que le modèle du site d’équipe ;
    
- fournir une stratégie par défaut avec une règle par défaut qui sera appliquée automatiquement sans aucune action requise par les propriétaires de sites ;
    
- créer une stratégie qui inclut plusieurs règles de suppression parmi lesquelles un propriétaire de site peut effectuer son choix.
    
Vous créez et gérez des stratégies de suppression de documents à l'aide du centre de stratégies de suppression de **** documents, que vous pouvez trouver &amp; sous rétention dans le centre de sécurité conformité Office 365. Vous pouvez également créer le centre de stratégies manuellement en [créant la collection de sites](https://go.microsoft.com/fwlink/p/?LinkID=404342) et en choisissant **Centre de stratégie de conformité** dans l'onglet **entreprise** . Chaque client ne peut avoir qu'un seul centre de stratégie de suppression de documents et il sera créé automatiquement si vous démarrez &amp; à partir du centre de sécurité conformité. 
  
![Page d’accueil du centre de stratégies de suppression de documents](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="when-to-use-document-deletion-policies"></a>Quand utiliser les stratégies de suppression de documents

En plus des stratégies de suppression de documents, Office 365 fournit les stratégies de rétention suivantes pour le contenu de site :
  
- [Gestion des enregistrements](https://go.microsoft.com/fwlink/p/?LinkID=404250)
    
- [Stratégies de gestion des informations pour les types de contenu, les listes et les bibliothèques](https://go.microsoft.com/fwlink/p/?LinkID=404239)
    
- [Stratégies de site](https://go.microsoft.com/fwlink/p/?LinkID=404242)
    
Chaque type de stratégie convient le mieux pour un type spécifique de site ou de données. Par exemple, votre organisation peut avoir un site hautement structuré qui utilise des types de contenu tels qu’un site financier pour des contrats ou une base de connaissances pour des articles. Dans ce cas, vous pouvez utiliser des stratégies de type de contenu. Il se peut que votre organisation doive conserver des documents juridiques et, dans ce cas, vous pouvez utiliser des types de contenu et un centre des enregistrements pour mettre en œuvre un plan de gestion de fichiers.
  
Les stratégies de suppression de documents ne remplacent pas les stratégies de gestion des enregistrements ou de gestion des informations, qui fonctionnent mieux avec des données structurées et des types de contenu. Au lieu de cela, vous devez utiliser des stratégies de suppression de documents lorsque vous avez besoin de gérer largement la suppression automatique des données non structurées comme les sites d'équipe et les sites OneDrive entreprise.
  
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

Une fois que vous avez créé une stratégie de suppression de documents, vous pouvez l'affecter à un modèle de collection de sites, par exemple, vous pouvez affecter une stratégie au modèle OneDrive entreprise afin qu'elle comprenne le site OneDrive de chaque utilisateur. Lorsque vous affectez une stratégie à un modèle de collection de sites, cette méthode s'applique à toutes les collections de sites déjà créées à partir de ce modèle, en plus des collections de sites créées à partir de ce modèle à l'avenir.
  
![Page Choisir un modèle affichant l’option OneDrive](media/IP-Choose-a-template.png)
  
Vous pouvez également affecter une stratégie à une collection de sites spécifique pour remplacer toutes les stratégies affectées à ce modèle de collection de sites. Par exemple, vous pouvez affecter des stratégies au modèle de site d’équipe, mais les remplacer ensuite en appliquant un ensemble de stratégies différent à une collection de sites spécifique créée à partir de ce modèle.
  
### <a name="one-mandatory-policy-or-several-policies-to-choose-from"></a>Une stratégie obligatoire ou un éventail de plusieurs stratégies dans lequel effectuer un choix

Lorsque vous affectez une stratégie, vous pouvez la rendre obligatoire pour que seule cette stratégie puisse être affectée et appliquée à tous les sites de la collection de sites. Les propriétaires de sites ne peuvent pas refuser une stratégie obligatoire, ce qui signifie que les documents du site seront soumis à la stratégie de suppression, quelle qu’elle soit.
  
Au lieu de rendre une stratégie unique obligatoire, vous pouvez aussi affecter plusieurs stratégies à une collection de sites, ce qui permet à chaque propriétaire de site de choisir la stratégie à appliquer à son site, ou même de la refuser complètement. Par exemple, vous pouvez créer une stratégie pour des documents commerciaux généraux et une autre stratégie pour des documents financiers ayant une planification de rétention différente. Un propriétaire de site connaît souvent mieux le contenu de son site et donc la stratégie de suppression de documents à appliquer. Chaque site ne peut avoir qu’une seule stratégie qui lui est appliquée.
  
### <a name="one-rule-or-several-rules-to-choose-from"></a>Une règle ou plusieurs règles parmi lesquelles choisir

À son tour, chaque stratégie peut contenir de nombreuses règles, par exemple, une stratégie de suppression pour des documents d'entreprise généraux peut avoir deux règles:
  
- Les documents qui n'ont pas besoin d'une rétention en fonction des obligations légales ou d'un besoin d'entreprise permanent ne doivent pas être conservés pendant une période de création de plus d'un an.
    
- les documents nécessaires pour une utilisation commerciale active en cours qui sont requis pendant plus d’un an, ne doivent pas être conservés plus de trois ans après leur création.
    
Un propriétaire de site peut déterminer que son site contient des documents d'entreprise généraux, sélectionner cette stratégie de suppression, puis sélectionner la règle appropriée dans la stratégie. Vous pouvez sélectionner uniquement une règle à partir de la stratégie actuellement appliquée au site (et non à partir d'une stratégie), et la règle s'applique à toutes les bibliothèques de documents du site.
  
## <a name="the-relationship-of-site-collections-policies-and-rules"></a>Relation entre les collections de sites, les stratégies et les règles

La relation de base est la suivante :
  
Une ou plusieurs stratégies peuvent être affectées à une collection de sites ou à un modèle de collection de sites, et chacune d'entre elles peut avoir une ou plusieurs règles. Toutefois, il ne peut y avoir qu'une seule stratégie active par site, et il ne peut y avoir qu'une seule règle de suppression active à tout moment pour les bibliothèques au sein du site.
  
![Schéma montrant la relation entre les stratégies](media/IP-Two-policies-four-rules.png)
  
## <a name="document-deletion-policies-are-inherited"></a>Les stratégies de suppression de documents sont héritées

Comme les autorisations, la navigation et de nombreuses autres fonctionnalités de site, les stratégies de suppression de documents sont héritées. Un propriétaire de site peut sélectionner une stratégie de suppression de documents pour son site, et tous les sous-sites héritent de la stratégie du parent. Le propriétaire d’un sous-site peut annuler l’héritage en sélectionnant une stratégie et une règle différentes, et cette stratégie s’applique à tous les sous-sites tant que l’héritage n’est pas de nouveau annulé.
  
## <a name="assigning-document-deletion-policies-for-the-first-time"></a>Première affectation de stratégies de suppression de documents

Il est important de comprendre que la période spécifiée pour une stratégie de suppression de documents signifie le temps écoulé depuis que le document a été créé ou modifié, et non le moment où la stratégie a été affectée. Par exemple, vous pouvez créer une stratégie de suppression de documents qui supprime définitivement les documents deux ans après leur création, puis affecter cette stratégie à un modèle de collection de sites à partir duquel plusieurs collections de sites ont été créées quatre ou cinq ans auparavant. Dans ce cas, il est probable que les collections de sites existantes contiennent de nombreux documents qui sont déjà plus anciens que les deux années spécifiés par la stratégie de suppression, ce qui signifie que beaucoup de contenu seront supprimés peu après l'affectation de la stratégie de suppression de documents pour le premier périodes.
  
Lorsque vous affectez la stratégie pour la première fois, tous les documents du site sont évalués et supprimés s’ils répondent aux critères. Cela s’applique à tous les documents existants, et non simplement aux documents créés depuis l’affectation de la stratégie. Et n’oubliez pas que la période de temps est liée à l’âge de chaque document, et non au moment de la première affectation de la stratégie.
  
Par conséquent, avant d’affecter une stratégie à un site pour la première fois, vous devez d’abord tenir compte de l’âge du contenu existant et de la façon dont la stratégie peut avoir une incidence sur le contenu existant. Vous pouvez également communiquer la nouvelle stratégie aux propriétaires de sites avant de l’affecter, pour leur donner le temps d’évaluer les incidences éventuelles.
  
## <a name="time-lag-for-propagating-policies"></a>Décalage de la propagation des stratégies

Une fois que vous avez affecté des stratégies à une collection de sites, les propriétaires de sites utilisent le lien **Stratégies de suppression de documents** sur la page **Paramètres du site** pour afficher et appliquer les stratégies disponibles pour le site. 
  
Le lien **stratégies de suppression de documents** ne s'affiche pas, sauf si des stratégies ont été affectées à la collection de sites. De plus, le lien ne s'affiche pas immédiatement après que des stratégies ont été affectées au site; le lien des stratégies de **Suppression de documents** peut prendre jusqu'à 24 heures. 
  
## <a name="permissions"></a>Autorisations

Les membres de votre équipe de conformité qui utiliseront le centre de stratégies de suppression de documents doivent disposer d’autorisations d’accès à la fois au centre de stratégies et aux collections de sites auxquels des stratégies seront appliquées. Nous vous recommandons de :
  
1. Créez un groupe de sécurité qui contient tous les utilisateurs du centre de stratégies de suppression de documents, très probablement votre équipe de gestion des stratégies de conformité. Pour plus d'informations, voir [gérer les groupes de sécurité à extension messagerie](https://go.microsoft.com/fwlink/p/?LinkID=404345) . 
    
2. Dans le centre de stratégie de suppression de documents, affectez des autorisations de propriétaire de collection de sites au groupe de sécurité. Pour plus d'informations, consultez la rubrique [autorisations pour les administrateurs de collections de sites](https://go.microsoft.com/fwlink/p/?LinkID=404346) . 
    
3. Dans chaque collection de sites à laquelle vous devez affecter des stratégies de suppression de documents, affectez des autorisations de propriétaire de collection de sites au groupe de sécurité.
    
## <a name="how-document-deletion-policies-work-with-hold-policies"></a>Fonctionnement des stratégies de suppression de documents avec des stratégies de blocage

Une stratégie de blocage garantit que tout le contenu est conservé pendant une période de temps donnée, tandis qu’une stratégie de suppression de documents garantit que tout le contenu est supprimé après une période de temps spécifique.
  
Si vous devez conserver des documents pendant une période de temps fixe, vous pouvez utiliser une stratégie de blocage avec une stratégie de suppression. Par exemple, vous pourriez bloquer des documents pendant trois ans après leur modification, puis configurer une stratégie de suppression pour supprimer ces documents trois ans après leur dernière modification.
  
Notez qu’une stratégie de suppression ne peut pas substituer un blocage. Si un site est bloqué et qu’une stratégie de suppression supprime un document, le document sera conservé dans la bibliothèque de conservation comme s’il avait été supprimé manuellement.
  
## <a name="see-also"></a>Voir aussi

[Application ou suppression d’une stratégie de suppression de documents pour un site](apply-or-remove-a-document-deletion-policy-for-a-site.md)

[Création d’une stratégie de suppression de documents](create-a-document-deletion-policy.md)


