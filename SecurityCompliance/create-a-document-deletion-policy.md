---
title: Création d’une stratégie de suppression de documents
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
ms.assetid: 41b2ed73-eb8d-4429-945e-a8197894585a
description: Les organisations doivent souvent conserver des documents pendant une certaine période de temps en raison des réglementations de conformité, juridiques, ou autres. Toutefois, conserver des documents plus longtemps que nécessaire peut exposer l’organisation à un risque juridique.
ms.openlocfilehash: 6bf4c0604708608ad7af064f4b32b57d33208a39
ms.sourcegitcommit: ede6230c2df398dc0a633e8f32ee0bfede0d5142
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "25002657"
---
# <a name="create-a-document-deletion-policy"></a>Création d’une stratégie de suppression de documents

> [!IMPORTANT]
> Aller plus loin, nous vous conseillons d’utiliser une stratégie de rétention ou étiquettes créées dans la sécurité &amp; centre de conformité au lieu d’une stratégie de suppression de documents. Stratégies de suppression de documents continueront de fonctionner en côte à côte des stratégies de rétention, mais si vous devez conserver ou supprimer du contenu n’importe où dans Office 365, nous vous conseillons d’utiliser une stratégie de rétention. Pour plus d’informations, voir [utiliser une stratégie de rétention au lieu de ces fonctionnalités](retention-policies.md#use-a-retention-policy-instead-of-these-features). 
  
Les organisations doivent souvent conserver des documents pendant une certaine période de temps en raison des réglementations de conformité, juridiques, ou autres. Toutefois, conserver des documents plus longtemps que nécessaire peut exposer l’organisation à un risque juridique.
  
Avec une stratégie de suppression de documents, vous pouvez réduire proactive des risques en supprimant des documents dans un site après une période de temps spécifique, par exemple, vous pouvez supprimer les documents dans OneDrive des utilisateurs pour les professionnels sites cinq ans après les documents ont été créés. 
  
Après avoir créé une stratégie de suppression de documents, vous pouvez l’affecter à un modèle de collection de sites, pour que la stratégie soit disponible pour toutes les collections de sites créées à partir de ce modèle. Vous pouvez également affecter une stratégie à une collection de sites spécifique, qui remplace toutes les stratégies qui ont pu être affectées au modèle pour cette collection de sites.
  
![Page d’accueil du centre de stratégies de suppression de documents](media/IP-Document-Deletion-Policy-Center-home-page.png)
  
## <a name="policy-templates"></a>Modèles de stratégie

Vous pouvez créer une stratégie de suppression de document de A à Z ou vous pouvez utiliser l’un des exemples de stratégie. Le Centre des stratégies de conformité inclut des exemples de stratégie que vous pouvez utiliser en l’état ou que vous pouvez utiliser comme point de départ, pour ensuite les renommer ou les modifier.
  
![Stratégies de suppression d’exemple de document](media/IP-Sample-deletion-policies.png)
  
## <a name="examples-of-how-to-use-document-deletion-policies"></a>Exemples

Une collection de sites ou d’un modèle de collection de sites peut avoir une stratégies supplémentaires qui lui est affectés et chacune de ces stratégies peut avoir une ou plusieurs règles. Toutefois, il peut y avoir qu’une seule stratégie est active par site, et il peut y avoir qu’une seule règle de suppression qui est active à tout moment pour les bibliothèques au sein du site.
  
![Schéma montrant la relation entre les stratégies](media/IP-Two-policies-four-rules.png)
  
En outre, vous pouvez sélectionner une stratégie comme stratégie obligatoire ou par défaut, et vous pouvez sélectionner une règle de suppression comme règle par défaut : 
  
- **Stratégie obligatoire** Lorsqu’une stratégie est marquée comme étant obligatoire, stratégie qu’une seule peut être affectée à la collection de sites ou du modèle. La stratégie doit être marquée comme valeur par défaut et sera appliquée à tous les sites. Les propriétaires de sites ne peut pas refuser la stratégie.
    
- **Stratégie par défaut** Lorsqu’une stratégie est définie comme valeur par défaut, la stratégie est automatiquement active dans tous les sites auxquels il est affecté à aucune action requise par le propriétaire du site.
    
- **Règle par défaut** Lorsqu’une règle de suppression est définie comme valeur par défaut, elle est automatiquement appliquée à toutes les bibliothèques dans les sites qui utilisent la stratégie.
    
Les exemples suivants expliquent quand vous pouvez utiliser une stratégie obligatoire ou des stratégies et règles par défaut.
  
### <a name="example-1-apply-a-single-policy-with-a-single-rule-to-a-site-collection-template"></a>Exemple 1 : Appliquer une stratégie unique avec une règle unique à un modèle de collection de sites

Vous pouvez appliquer une stratégie de suppression de documents à un large éventail de contenus non structurés (tous les sites OneDrive Entreprise ou tous les sites d’équipe, par exemple). Si vous souhaitez vous assurer qu’une stratégie de suppression de documents unique est active dans tous les sites créés à partir d’un modèle de collection de sites, vous pouvez :
  
1. créer une stratégie unique avec une règle de suppression par défaut unique ;
    
2. définir la stratégie comme étant obligatoire et par défaut ;
    
3. affecter la stratégie à un modèle de collection de sites.
    
Dans cet exemple, la règle de suppression par défaut sera appliquée à toutes les bibliothèques dans toutes les collections de sites créées à partir du modèle, et les propriétaires de sites ne peuvent pas refuser la stratégie. Il s’agit de la façon la plus simple d’appliquer de façon large et rigide une stratégie de suppression de documents.
  
![Schéma montrant une seule stratégie obligatoire](media/IP-Example-1-doc-deletion-policies.png)
  
### <a name="example-2-apply-a-single-policy-with-several-rules-to-a-site-collection-template"></a>Exemple 2 : Appliquer une stratégie unique avec plusieurs règles à un modèle de collection de sites

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

1. Dans la 365Security Office &amp; centre de conformité, accédez à **gestion de données** \> **rétention**. Sous **Supprimer**, cliquez sur **Gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive for Business**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.
    
    La première fois que vous accédez à partir de la sécurité &amp; centre de conformité pour le centre de stratégie de suppression de documents, le centre de la stratégie est automatiquement créé pour vous. Vous pouvez également créer manuellement le centre de la stratégie en fonction [de la collection de sites](http://go.microsoft.com/fwlink/p/?LinkID=404342) **Centre de stratégie de conformité** sur l’onglet **entreprise** . 
    
2. Choisissez les **stratégies de suppression**.
    
    ![Option de suppression des stratégies](media/IP-Deletion-Policies-option.png)
  
3. Choisissez **Suivant**.
    
4. Entrez un nom de stratégie et une description. Il se peut que les propriétaires de sites choisissent une stratégie pour leur site en fonction de ce nom et de cette description. Par conséquent, donnez suffisamment d’informations pour qu’ils choisissent la stratégie correcte.
    
5. Pour créer une règle, choisissez **Nouveau**.
    
6. Entrez un nom et choisissez les options suivantes :
    
  - Choisir la règle sera définitivement supprimer les documents ou de les supprimer dans la Corbeille. La Corbeille fournit un filet de deuxième niveau avant la suppression définitive d’un élément à partir d’un site. Pour plus d’informations sur la Corbeille, voir [Vider la Corbeille ou restaurer vos fichiers](http://go.microsoft.com/fwlink/p/?LinkID=404348).
    
  - Indiquez si la date de suppression est calculée à partir de la date de création d’un document ou de la date de dernière modification.
    
  - Entrez un nombre de jours, de mois ou d’années comme période de temps au bout de laquelle un document sera supprimé.
    
  - Indiquez si la règle est une règle par défaut. La première règle que vous créez est automatiquement définie comme règle par défaut. Une règle par défaut est appliquée automatiquement à toutes les bibliothèques dans les sites qui utilisent la stratégie.
    
![Page Nouvelle règle de suppression](media/IP-New-deletion-rule.png)
  
7. Cliquez sur **Enregistrer**.
    
8. Créez des règles supplémentaires si vous souhaitez que les propriétaires de sites puissent choisir différentes règles à appliquer à leur site. La règle par défaut, le cas échéant, s’appliquera si le propriétaire du site n’effectue aucune action.
    
9. Pour supprimer une règle d’une stratégie, sélectionnez la règle, cliquez sur **Supprimer**, puis cliquez sur **OK**.
    
    > [!NOTE]
    > Si vous supprimez une règle, la stratégie ne contient-elle pas d’une règle par défaut, puis aucune règle ne sera en vigueur pour cette stratégie — en d’autres termes, aucun document ne sera supprimé. 
  
![Message de confirmation de la suppression de la règle de la stratégie](media/IP-Remove-rule-from-policy-message.png)
  
## <a name="assign-the-document-deletion-policy-to-a-site-collection-template"></a>Affectation de la stratégie de suppression de documents à un modèle de collection de sites

En affectant une stratégie à un modèle de collection de sites, vous mettez la stratégie à la disposition de toutes les collections de sites créées à partir de ce modèle, y compris les collections de sites existantes et les collections de sites créées à l’avenir.
  
Il est important de comprendre que la période de temps spécifiée pour un document de stratégie de suppression signifie l’heure dans la mesure où le document a été créé ou modifié, pas l’heure dans la mesure où la stratégie a été attribuée. Lorsque vous attribuez la stratégie pour la première fois, tous les documents dans le site sont évaluées et, si elles répondent aux critères, ils seront supprimés. Cela s’applique à tous les documents existants, pas seulement nouveaux documents créés dans la mesure où la stratégie a été attribuée.
  
1. Dans la sécurité &amp; centre de conformité, accédez à **gestion de données** \> **rétention**. Sous **Supprimer**, cliquez sur **Gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive for Business**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.
    
2. Choisissez **Attributions de stratégies pour les modèles**.
    
    ![Option d’attributions des stratégies pour les modèles](media/IP-Policy-Assignments-for-Templates-option.png)
  
3. Choisissez **Suivant**.
    
4. Effectuez l’une des opérations suivantes :
    
  - Pour affecter la stratégie à un modèle de collection de sites tel que le modèle de site d’équipe, sélectionnez **Affecter au modèle de collection de sites**, puis sélectionnez le modèle de collection de sites.
    
  - Pour affecter la stratégie à un lecteur des utilisateurs pour les entreprises, choisissez **affecter à OneDrive pour le modèle d’entreprise**, mis en surbrillance ci-dessous.
    
    > [!NOTE]
    > Lorsque vous affectez une stratégie à un modèle de collection de sites, cette stratégie est disponible à la fois pour les collections de sites existantes créées à partir de ce modèle et pour les collections de sites créées à l’avenir. 
  
![Page Choisir un modèle affichant l’option OneDrive](media/IP-Choose-a-template.png)
  
5. Cliquez sur **Enregistrer**.
    
    > [!NOTE]
    > Chaque modèle peut avoir qu’un seul ensemble de stratégies qui lui est affecté. Si vous voyez une erreur indiquant que ce modèle possède déjà des stratégies qui lui est affectés, choisissez **Annuler** \> **affecter à la Collection de sites** dans le volet de navigation gauche \> sélectionner une collection de sites pour afficher et gérer l’ensemble des stratégies qui sont déjà affecté. 
  
6. Cliquez sur **Gérer les stratégies affectées**, sélectionnez les stratégies que vous souhaitez attribuer, puis choisissez si une stratégie est la stratégie par défaut. Lorsque vous définissez une stratégie par défaut, tous les sites sont affectés automatiquement à la stratégie disposent de la stratégie active aucune action requise par le propriétaire du site.
    
    ![Page Ajouter et gérer les stratégies](media/IP-Add-and-manage-policies-page.png)
  
7. Cliquez sur **Enregistrer**.
    
8. Si vous souhaitez appliquer la stratégie sur tous les sites sans autoriser les propriétaires de sites à la refuser, choisissez **Marquer la stratégie comme obligatoire**. Lorsque vous définissez une stratégie comme obligatoire, seule cette stratégie unique peut être affectée au modèle de collection de sites. La stratégie doit également être marquée comme stratégie par défaut.
    
    Si cette option est grisée, choisissez **Gérer les stratégies affectées** et assurez-vous qu’au moins une stratégie est affectée et définie comme stratégie par défaut. 
    
9. Cliquez sur **Enregistrer**.
    
## <a name="assign-the-document-deletion-policy-to-a-site-collection"></a>Affectation de la stratégie de suppression de documents à une collection de sites

En affectant une stratégie à une collection de sites spécifique, vous mettez la stratégie à disposition uniquement de cette collection de sites spécifique. Cela signifie que vous pouvez adapter des stratégies plus étroitement au contenu dans la collection de sites. En outre, les stratégies affectées à une collection de sites spécifique remplacent toutes les stratégies qui sont affectées au modèle pour cette collection de sites. Par exemple, une stratégie affectée à la collection de sites du département des ventes (créée à partir du modèle du site d’équipe) remplace toutes les stratégies affectées au modèle de site d’équipe.
  
Il est important de comprendre que la période de temps spécifiée pour un document de stratégie de suppression signifie l’heure dans la mesure où le document a été créé ou modifié, pas l’heure dans la mesure où la stratégie a été attribuée. Lorsque vous attribuez la stratégie pour la première fois, tous les documents dans le site sont évaluées et, si elles répondent aux critères, ils seront supprimés. Cela s’applique à tous les documents existants, pas seulement nouveaux documents créés dans la mesure où la stratégie a été attribuée.
  
1. Dans la sécurité &amp; centre de conformité, accédez à **gestion de données** \> **rétention**. Sous **Supprimer**, sélectionnez **Gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive for Business**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.
    
2. Choisissez **Attributions de stratégies pour les collections de sites**.
    
    ![Option d’attributions des stratégies pour les collections de sites](media/IP-Policy-Assignments-for-Site-Collections-option.png)
  
3. Choisissez **Suivant**.
    
4. Choisissez **Choisir une collection de sites**. Recherche de la collection de sites par nom ou URL, sélectionnez la collection de sites, cliquez sur **Enregistrer**.
    
    > [!NOTE]
    > Chaque collection de sites peut avoir qu’un seul ensemble de stratégies qui lui est affecté. Si vous voyez une erreur indiquant que cette collection de sites déjà dispose des stratégies qui lui est affectés, choisissez **Annuler** \> **affecter à la Collection de sites** et sélectionnez une collection de sites pour afficher et gérer l’ensemble des stratégies qui sont déjà affectés. 
  
![Page Choisir une collection de sites](media/IP-Choose-a-site-collection-page.png)
  
5. Cliquez sur **Gérer les stratégies affectées**, sélectionnez les stratégies que vous souhaitez attribuer, puis choisissez si une stratégie est la stratégie par défaut. Lorsque vous définissez une stratégie par défaut, tous les sites sont affectés automatiquement à la stratégie disposent de la stratégie active aucune action requise par le propriétaire du site.
    
    ![Page Ajouter et gérer les stratégies](media/IP-Add-and-manage-policies-page.png)
  
6. Cliquez sur **Enregistrer**.
    
7. Si vous souhaitez appliquer la stratégie sur tous les sites sans autoriser les propriétaires de sites à refuser, choisissez **Marquer la stratégie comme obligatoire**. Lorsque vous définissez une stratégie comme obligatoire, seule cette stratégie unique peut être affectée à la collection de sites. La stratégie doit également être marquée comme stratégie par défaut.
    
    Si cette option est grisée, choisissez **Gérer les stratégies affectées** et assurez-vous qu’au moins une stratégie est affectée et définie comme stratégie par défaut. 
    
8. Cliquez sur **Enregistrer**.
    
## <a name="delete-a-policy-assignment"></a>Suppression d’une affectation de stratégie

Lorsque vous supprimez une affectation, les stratégies affectées ne s’appliquent plus à aucun site dans la collection de sites ou le modèle de collection de sites.
  
1. Dans la sécurité &amp; centre de conformité, accédez à **gestion de données** \> **rétention**. Sous **Supprimer**, sélectionnez **Gérer les stratégies de suppression de documents pour SharePoint Online et OneDrive for Business**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.
    
2. Choisissez **Attributions de stratégies pour les modèles** ou **Attributions de stratégies pour les collections de sites**.
    
3. Sélectionnez l’élément de l’affectation, cliquez sur **Supprimer l’élément**.
    
    ![Commande de suppression d’élément pour l’attribution des stratégies](media/IP-Delete-policy-assignment.png)
  
## <a name="delete-a-policy"></a>Suppression d’une stratégie

Vous ne pouvez pas supprimer une stratégie qui est en cours d’utilisation. Avant de supprimer une stratégie, vous devez tout d’abord supprimer toutes les affectations pour les collections de sites et modèles de collection de sites qui incluent cette stratégie, voir la section précédente.
  
1. Dans la sécurité &amp; centre de conformité \> choisissez **Gestion des données** \> **rétention** dans le volet de navigation gauche \> sous **Supprimer** \> **suppression de documents de gérer les stratégies pour SharePoint Online et OneDrive pour les entreprises**. Le centre de stratégie de suppression de Document s’ouvre dans un nouvel onglet de navigateur.
    
2. Choisissez ** stratégies de suppression **.
    
    ![Option de suppression des stratégies](media/IP-Deletion-Policies-option.png)
  
3. Sélectionnez la stratégie.
    
4. Dans le ruban \> onglet **éléments** \> **Supprimer la stratégie**.
    
    ![Bouton Supprimer la stratégie sur le ruban](media/IP-Remove-Policy-button-on-Ribbon.png)
  
5. Si la stratégie est en cours d’utilisation, le système vous demandera si vous souhaitez supprimer la stratégie de toutes les collections de sites où il est utilisé. Si vous êtes sûr, cliquez sur **OK**.
    
    ![Message de confirmation de suppression de stratégie](media/IP-Delete-policy-confirmation.png)
  
## <a name="see-also"></a>Voir aussi

[Vue d’ensemble des stratégies de suppression de documents](document-deletion-policies.md)

[Application ou suppression d’une stratégie de suppression de documents pour un site](apply-or-remove-a-document-deletion-policy-for-a-site.md)
 

