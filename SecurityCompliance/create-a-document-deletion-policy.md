---
title: Création d’une stratégie de suppression de documents
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 41b2ed73-eb8d-4429-945e-a8197894585a
description: Les organisations doivent souvent conserver des documents pendant une certaine période de temps en raison des réglementations de conformité, juridiques, ou autres. Toutefois, conserver des documents plus longtemps que nécessaire peut exposer l’organisation à un risque juridique.
ms.openlocfilehash: e8f85f4cc9ae541d8a962dfb270e5216c912ac7d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153916"
---
# <a name="create-a-document-deletion-policy"></a>Création d’une stratégie de suppression de documents

> [!IMPORTANT]
> Pour aller plus loin, nous vous recommandons d’utiliser une stratégie de rétention ou des étiquettes de rétention créées dans le centre de conformité Microsoft 365 &amp; , le centre de sécurité Microsoft 365 ou le centre de sécurité conformité Office 365 au lieu d’une stratégie de suppression de documents. Les stratégies de suppression de documents continueront à fonctionner côte à côte avec des stratégies de rétention, mais si vous devez conserver ou supprimer du contenu n’importe où dans Office 365, nous vous recommandons d’utiliser une stratégie de rétention. Pour plus d’informations, consultez [la rubrique utiliser une stratégie de rétention au lieu de ces fonctionnalités](retention-policies.md#use-a-retention-policy-instead-of-these-features). 
  
Les organisations doivent souvent conserver des documents pendant une certaine période de temps en raison des réglementations de conformité, juridiques, ou autres. Toutefois, conserver des documents plus longtemps que nécessaire peut exposer l’organisation à un risque juridique.
  
Avec une stratégie de suppression de documents, vous pouvez réduire de manière proactive les risques en supprimant des documents dans un site après une période de temps spécifique (par exemple, vous pouvez supprimer des documents dans les sites OneDrive entreprise de l’utilisateur cinq ans après la création des documents). 
  
Après avoir créé une stratégie de suppression de documents, vous pouvez l’affecter à un modèle de collection de sites, pour que la stratégie soit disponible pour toutes les collections de sites créées à partir de ce modèle. Vous pouvez également affecter une stratégie à une collection de sites spécifique, qui remplace toutes les stratégies qui ont pu être affectées au modèle pour cette collection de sites.
  
![Page d’accueil du centre de stratégies de suppression de documents](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="policy-templates"></a>Modèles de stratégie

Vous pouvez créer une stratégie de suppression de document de A à Z ou vous pouvez utiliser l’un des exemples de stratégie. Le Centre des stratégies de conformité inclut des exemples de stratégie que vous pouvez utiliser en l’état ou que vous pouvez utiliser comme point de départ, pour ensuite les renommer ou les modifier.
  
![Stratégies de suppression d’exemple de document](media/IP-Sample-deletion-policies.png)
  
## <a name="examples-of-how-to-use-document-deletion-policies"></a>Exemples

Une collection de sites ou un modèle de collection de sites peut avoir plusieurs stratégies qui lui sont affectées, et chacune de ces stratégies peut avoir une ou plusieurs règles. Toutefois, il ne peut y avoir qu’une seule stratégie active par site, et il ne peut y avoir qu’une seule règle de suppression active à tout moment pour les bibliothèques au sein du site.
  
![Schéma montrant la relation entre les stratégies](media/IP-Two-policies-four-rules.png)
  
En outre, vous pouvez sélectionner une stratégie comme stratégie obligatoire ou par défaut, et vous pouvez sélectionner une règle de suppression comme règle par défaut : 
  
- **Stratégie obligatoire** Lorsqu’une stratégie est marquée comme obligatoire, une seule stratégie peut être affectée à la collection de sites ou au modèle. La stratégie doit être marquée comme valeur par défaut et sera appliquée à tous les sites. Les propriétaires de sites ne peuvent pas refuser la stratégie.
    
- **Stratégie par défaut** Lorsqu’une stratégie est définie par défaut, la stratégie est automatiquement active dans tous les sites auxquels elle est affectée sans action requise par le propriétaire du site.
    
- **Règle par défaut** Lorsqu’une règle de suppression est définie par défaut, elle est automatiquement appliquée à toutes les bibliothèques dans les sites qui utilisent la stratégie.
    
Les exemples suivants expliquent quand vous pouvez utiliser une stratégie obligatoire ou des stratégies et règles par défaut.
  
### <a name="example-1-apply-a-single-policy-with-a-single-rule-to-a-site-collection-template"></a>Exemple 1 : Appliquer une stratégie unique avec une règle unique à un modèle de collection de sites

Vous pouvez appliquer une stratégie de suppression de documents à un large éventail de contenus non structurés (tous les sites OneDrive Entreprise ou tous les sites d’équipe, par exemple). Si vous souhaitez vous assurer qu’une stratégie de suppression de documents unique est active dans tous les sites créés à partir d’un modèle de collection de sites, vous pouvez :
  
1. créer une stratégie unique avec une règle de suppression par défaut unique ;
    
2. définir la stratégie comme étant obligatoire et par défaut ;
    
3. affecter la stratégie à un modèle de collection de sites.
    
Dans cet exemple, la règle de suppression par défaut sera appliquée à toutes les bibliothèques dans toutes les collections de sites créées à partir du modèle, et les propriétaires de sites ne peuvent pas refuser la stratégie. Il s’agit de la façon la plus simple d’appliquer de façon large et rigide une stratégie de suppression de documents.
  
![Schéma montrant une seule stratégie obligatoire](media/IP-Example-1-doc-deletion-policies.png)
  
### <a name="example-2-apply-a-single-policy-with-several-rules-to-a-site-collection-template"></a>Exemple 2: appliquer une stratégie unique avec plusieurs règles à un modèle de collection de sites

Les propriétaires de sites sont souvent les mieux placés pour savoir quel type de contenu leur site contient, donc vous pouvez choisir de les autoriser à sélectionner la règle de suppression qui s’applique le mieux à leur site. Vous pouvez également autoriser les propriétaires de sites à refuser une stratégie entièrement.
  
Simultanément, vous pouvez toujours créer et gérer centralement les stratégies. Vous pouvez également sélectionner une stratégie et une règle comme stratégie et règle par défaut, pour que la stratégie soit toujours active tant que le propriétaire du site n’en choisit pas une autre ou la refuse. Si vous souhaitez offrir une telle flexibilité aux propriétaires de sites, vous pouvez :
  
1. créer une stratégie unique avec plusieurs règles de suppression et définir une règle par défaut ;
    
2. définir la stratégie comme stratégie par défaut ;
    
3. affecter la stratégie à un modèle de collection de sites.
    
Les propriétaires de sites peuvent choisir l’une des règles de suppression alternatives, refuser la stratégie, ou ne rien faire et être soumis à la stratégie et à la règle par défaut.
  
![Schéma montrant une stratégie comportant beaucoup de règles](media/IP-Example-2-doc-deletion-policies.png)
  
### <a name="example-3-apply-several-policies-with-one-or-more-rules-to-a-site-collection"></a>Exemple 3 : Appliquer plusieurs stratégies avec une ou plusieurs règles à une collection de sites

Cet exemple fournit le maximum de flexibilité pour les propriétaires de sites car ils peuvent choisir parmi plusieurs stratégies, et après avoir sélectionné une règle, ils peuvent souvent effectuer un choix parmi plusieurs règles. Une stratégie et une règle sont définies comme stratégie et règle par défaut, pour que la stratégie soit toujours active tant que le propriétaire du site n’en choisit pas une autre ou la refuse. Notez que si vous ne définissez pas une stratégie et une règle par défaut, aucune stratégie ou aucune règle ne sera active pour les bibliothèques de documents dans le site tant que le propriétaire du site ne prendra pas des mesures pour les sélectionner et les appliquer.
  
Contrairement aux deux exemples précédents, ces stratégies sont affectées à une collection de sites spécifique, et non au modèle de collection de sites. Cela signifie que les stratégies peuvent être adaptées plus spécifiquement au contenu dans une collection de sites donnée.
  
Les stratégies et les règles sont héritées. Les propriétaires de sites peuvent sélectionner une stratégie et une règle pour leur site, et tous les sous-sites héritent de la stratégie du parent. Toutefois, le propriétaire d’un sous-site peut annuler l’héritage en sélectionnant une stratégie et une règle différentes, qui s’appliquent à leur tour à tous les sous-sites tant que l’héritage n’est pas de nouveau annulé.
  
Pour configurer ce scénario, vous pouvez :
  
1. créer plusieurs stratégies contenant chacune une ou plusieurs règles ;
    
2. définir une stratégie et une règle par défaut ;
    
3. affecter les stratégies à une collection de sites spécifique.
    
En outre, les stratégies et les règles sont adaptées à une collection de sites spécifique, où les propriétaires de sites peuvent annuler l’héritage en sélectionnant la stratégie et la règle qui s’appliquent le mieux à leur site.
  
![Schéma montrant de nombreuses stratégies et règles](media/IP-Example-3-doc-deletion-policies.png)
  
## <a name="create-a-document-deletion-policy"></a>Création d’une stratégie de suppression de documents

1. Dans le centre de &amp; conformité Office 365Security, accédez à **conservation**de la **gestion** \> des données. Sous **supprimer**, cliquez sur **gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive entreprise**. Le centre de stratégies de suppression de documents s’ouvre dans un nouvel onglet du navigateur.
    
    La première fois que vous naviguez depuis &amp; le centre de sécurité conformité vers le centre de stratégie de suppression de documents, le centre de stratégies est automatiquement créé pour vous. Vous pouvez également créer manuellement le centre de stratégies en [créant la collection de sites](http://go.microsoft.com/fwlink/p/?LinkID=404342) et en choisissant **Centre de stratégies de conformité** sous l’onglet **entreprise** . 
    
2. Choisissez **stratégies de suppression**.
    
    ![Option de suppression des stratégies](media/IP-Deletion-Policies-option.png)
  
3. Choisissez **Suivant**.
    
4. Entrez un nom de stratégie et une description. Il se peut que les propriétaires de sites choisissent une stratégie pour leur site en fonction de ce nom et de cette description. Par conséquent, donnez suffisamment d’informations pour qu’ils choisissent la stratégie correcte.
    
5. Pour créer une règle, choisissez **Nouveau**.
    
6. Entrez un nom et choisissez les options suivantes :
    
  - Indiquez si la règle supprimera définitivement les documents ou les placera dans la Corbeille. La Corbeille fournit un filet de sécurité de deuxième niveau avant la suppression définitive d’un élément d’un site. Pour plus d’informations sur la corbeille, reportez-vous à [la section vidage de la Corbeille ou restauration de vos fichiers](http://go.microsoft.com/fwlink/p/?LinkID=404348).
    
  - Indiquez si la date de suppression est calculée à partir de la date de création d’un document ou de la date de dernière modification.
    
  - Entrez un nombre de jours, de mois ou d’années comme période de temps au bout de laquelle un document sera supprimé.
    
  - Indiquez si la règle est une règle par défaut. La première règle que vous créez est automatiquement définie comme règle par défaut. Une règle par défaut est appliquée automatiquement à toutes les bibliothèques dans les sites qui utilisent la stratégie.
    
![Page Nouvelle règle de suppression](media/IP-New-deletion-rule.png)
  
7. Cliquez sur **Enregistrer**.
    
8. Créez des règles supplémentaires si vous souhaitez que les propriétaires de sites puissent choisir différentes règles à appliquer à leur site. La règle par défaut, le cas échéant, s’appliquera si le propriétaire du site n’effectue aucune action.
    
9. Pour supprimer une règle d’une stratégie, sélectionnez-la, cliquez sur **supprimer**, puis cliquez sur **OK**.
    
    > [!NOTE]
    > Si vous supprimez une règle et que la stratégie ne contient pas de règle par défaut, aucune règle n’est appliquée à cette stratégie (en d’autres termes, aucun document n’est supprimé). 
  
![Message de confirmation de la suppression de la règle de la stratégie](media/IP-Remove-rule-from-policy-message.png)
  
## <a name="assign-the-document-deletion-policy-to-a-site-collection-template"></a>Affectation de la stratégie de suppression de documents à un modèle de collection de sites

En affectant une stratégie à un modèle de collection de sites, vous mettez la stratégie à la disposition de toutes les collections de sites créées à partir de ce modèle, y compris les collections de sites existantes et les collections de sites créées à l’avenir.
  
Il est important de comprendre que la période spécifiée pour une stratégie de suppression de documents signifie le temps écoulé depuis que le document a été créé ou modifié, et non le moment où la stratégie a été affectée. Lorsque vous affectez la stratégie pour la première fois, tous les documents du site sont évalués et supprimés s’ils répondent aux critères. Cela s’applique à tous les documents existants, et non simplement aux documents créés depuis l’affectation de la stratégie.
  
1. Dans le centre &amp; de sécurité conformité, accédez à **conservation**de **gestion** \> des données. Sous **supprimer**, cliquez sur **gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive entreprise**. Le centre de stratégies de suppression de documents s’ouvre dans un nouvel onglet du navigateur.
    
2. Choisissez **Attributions de stratégies pour les modèles**.
    
    ![Option d’attributions des stratégies pour les modèles](media/IP-Policy-Assignments-for-Templates-option.png)
  
3. Choisissez **Suivant**.
    
4. Effectuez l’une des opérations suivantes :
    
  - Pour affecter la stratégie à un modèle de collection de sites tel que le modèle de site d’équipe, sélectionnez **Affecter au modèle de collection de sites**, puis sélectionnez le modèle de collection de sites.
    
  - Pour affecter la stratégie à un seul lecteur pour les entreprises, choisissez **affecter au modèle OneDrive entreprise**, mis en surbrillance ci-dessous.
    
    > [!NOTE]
    > Lorsque vous affectez une stratégie à un modèle de collection de sites, cette stratégie est disponible à la fois pour les collections de sites existantes créées à partir de ce modèle et pour les collections de sites créées à l’avenir. 
  
![Page Choisir un modèle affichant l’option OneDrive](media/IP-Choose-a-template.png)
  
5. Cliquez sur **Enregistrer**.
    
    > [!NOTE]
    > Chaque modèle ne peut avoir qu’un seul ensemble de règles qui lui est affecté. Si vous voyez une erreur indiquant que ce modèle a déjà des stratégies qui lui sont attribuées, sélectionnez **Annuler** \> l' **affectation à la collection de sites** dans le volet de navigation \> de gauche sélectionnez une collection de sites pour afficher et gérer l’ensemble des stratégies déjà présentes attribuée. 
  
6. Choisissez **Gérer les stratégies affectées**, sélectionnez les stratégies à affecter, puis indiquez si une stratégie est la stratégie par défaut. Lorsque vous définissez une stratégie par défaut, tous les sites affectés à la stratégie ont automatiquement la stratégie active sans action requise par le propriétaire du site.
    
    ![Page Ajouter et gérer les stratégies](media/IP-Add-and-manage-policies-page.png)
  
7. Cliquez sur **Enregistrer**.
    
8. Si vous souhaitez appliquer la stratégie sur tous les sites sans autoriser les propriétaires de sites à la refuser, choisissez **Marquer la stratégie comme obligatoire**. Lorsque vous définissez une stratégie comme obligatoire, seule cette stratégie unique peut être affectée au modèle de collection de sites. La stratégie doit également être marquée comme stratégie par défaut.
    
    Si cette option est grisée, choisissez **Gérer les stratégies affectées** et assurez-vous qu’au moins une stratégie est affectée et définie comme stratégie par défaut. 
    
9. Cliquez sur **Enregistrer**.
    
## <a name="assign-the-document-deletion-policy-to-a-site-collection"></a>Affectation de la stratégie de suppression de documents à une collection de sites

En affectant une stratégie à une collection de sites spécifique, vous mettez la stratégie à disposition uniquement de cette collection de sites spécifique. Cela signifie que vous pouvez adapter des stratégies plus étroitement au contenu dans la collection de sites. En outre, les stratégies affectées à une collection de sites spécifique remplacent toutes les stratégies qui sont affectées au modèle pour cette collection de sites. Par exemple, une stratégie affectée à la collection de sites du département des ventes (créée à partir du modèle du site d’équipe) remplace toutes les stratégies affectées au modèle de site d’équipe.
  
Il est important de comprendre que la période spécifiée pour une stratégie de suppression de documents signifie le temps écoulé depuis que le document a été créé ou modifié, et non le moment où la stratégie a été affectée. Lorsque vous affectez la stratégie pour la première fois, tous les documents du site sont évalués et supprimés s’ils répondent aux critères. Cela s’applique à tous les documents existants, et non simplement aux documents créés depuis l’affectation de la stratégie.
  
1. Dans le centre &amp; de sécurité conformité, accédez à **conservation**de **gestion** \> des données. Sous **supprimer**, choisissez **gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive entreprise**. Le centre de stratégies de suppression de documents s’ouvre dans un nouvel onglet du navigateur.
    
2. Choisissez **Attributions de stratégies pour les collections de sites**.
    
    ![Option d’attributions des stratégies pour les collections de sites](media/IP-Policy-Assignments-for-Site-Collections-option.png)
  
3. Choisissez **Suivant**.
    
4. Choisissez **choisir une collection de sites**. Recherchez la collection de sites par nom ou URL, sélectionnez la collection de sites, puis cliquez sur **Enregistrer**.
    
    > [!NOTE]
    > Chaque collection de sites ne peut avoir qu’un seul ensemble de règles qui lui est affecté. Si vous voyez une erreur indiquant que des stratégies ont déjà été affectées à cette collection de sites, choisissez **Annuler** \> l' **affectation à la collection de sites** et sélectionnez une collection de sites pour afficher et gérer l’ensemble des stratégies déjà affectées. 
  
![Page Choisir une collection de sites](media/IP-Choose-a-site-collection-page.png)
  
5. Choisissez **Gérer les stratégies affectées**, sélectionnez les stratégies à affecter, puis indiquez si une stratégie est la stratégie par défaut. Lorsque vous définissez une stratégie par défaut, tous les sites affectés à la stratégie ont automatiquement la stratégie active sans action requise par le propriétaire du site.
    
    ![Page Ajouter et gérer les stratégies](media/IP-Add-and-manage-policies-page.png)
  
6. Cliquez sur **Enregistrer**.
    
7. Si vous souhaitez appliquer la stratégie sur tous les sites sans autoriser les propriétaires de sites à refuser, choisissez **Marquer la stratégie comme obligatoire**. Lorsque vous définissez une stratégie comme obligatoire, seule cette stratégie unique peut être affectée à la collection de sites. La stratégie doit également être marquée comme stratégie par défaut.
    
    Si cette option est grisée, choisissez **Gérer les stratégies affectées** et assurez-vous qu’au moins une stratégie est affectée et définie comme stratégie par défaut. 
    
8. Cliquez sur **Enregistrer**.
    
## <a name="delete-a-policy-assignment"></a>Suppression d’une affectation de stratégie

Lorsque vous supprimez une affectation, les stratégies affectées ne s’appliquent plus à aucun site dans la collection de sites ou le modèle de collection de sites.
  
1. Dans le centre &amp; de sécurité conformité, accédez à **conservation**de **gestion** \> des données. Sous **supprimer**, choisissez **gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive entreprise**. Le centre de stratégies de suppression de documents s’ouvre dans un nouvel onglet du navigateur.
    
2. Choisissez **Attributions de stratégies pour les modèles** ou **Attributions de stratégies pour les collections de sites**.
    
3. Sélectionnez l’élément d’affectation, puis cliquez sur **Supprimer l’élément**.
    
    ![Commande de suppression d’élément pour l’attribution des stratégies](media/IP-Delete-policy-assignment.png)
  
## <a name="delete-a-policy"></a>Suppression d’une stratégie

Vous ne pouvez pas supprimer une stratégie en cours d’utilisation. Avant de pouvoir supprimer une stratégie, vous devez d’abord supprimer toutes les affectations aux collections de sites et aux modèles de collection de sites qui incluent cette stratégie — consultez la section précédente.
  
1. Dans le centre &amp; \> de sécurité conformité, choisissez **conservation** de la **gestion** \> des \> données dans le volet de navigation de gauche sous **supprimer** \> **gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive pour les entreprises**. Le centre de stratégies de suppression de documents s’ouvre dans un nouvel onglet du navigateur.
    
2. Choisissez * * stratégies de suppression * *.
    
    ![Option de suppression des stratégies](media/IP-Deletion-Policies-option.png)
  
3. Sélectionnez la stratégie.
    
4. Dans l’onglet \> **** \> éléments du ruban, supprimez la **stratégie**.
    
    ![Bouton Supprimer la stratégie sur le ruban](media/IP-Remove-Policy-button-on-Ribbon.png)
  
5. Si la stratégie est en cours d’utilisation, un message vous demande si vous souhaitez supprimer la stratégie de toutes les collections de sites où elle est utilisée. Si vous êtes sûr, choisissez **OK**.
    
    ![Message de confirmation de suppression de stratégie](media/IP-Delete-policy-confirmation.png)
  
## <a name="see-also"></a>Voir également


  [Vue d’ensemble des stratégies de suppression de documents](document-deletion-policies.md)

[Application ou suppression d’une stratégie de suppression de documents pour un site](apply-or-remove-a-document-deletion-policy-for-a-site.md)
 

