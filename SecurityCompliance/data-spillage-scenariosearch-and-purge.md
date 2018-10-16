---
title: solution série données débordements scénario de découverte électronique - recherche et purge
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d945f7dd-f62f-4ca7-b3e7-469824cfd493
description: Utiliser les outils de recherche et de découverte électronique Office 365 pour gérer et répondre à un incident débordements de données dans votre organisation.
ms.openlocfilehash: 4da8efdb6f5d129e08d85f9b6c94726a7d099cb3
ms.sourcegitcommit: dd58ed6fd424272e361bc3c109ecd6d63d673048
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2018
ms.locfileid: "25566875"
---
# <a name="ediscovery-solution-series-data-spillage-scenario---search-and-purge"></a>série de solution eDiscovery : scénario débordements de données - recherche et purge

 **What ' s débordements de données et ce doivent savoir ?** Débordements de données est lorsque l’utilisateur relâche un document confidentiel dans un environnement non fiable. Lorsqu’un incident débordements de données est détecté, il est important évaluer rapidement la taille et l’emplacement de l’écoulement, examinez les activités utilisateur et puis vider définitivement les données dispersées à partir du système. 
  
## <a name="data-spillage-scenario"></a>Scénario de débordements de données

Vous êtes un responsable de la sécurité informations responsable chez Contoso. Vous êtes informé d’une situation débordements de données où un employé partagé sans le savoir un document hautement confidentiel avec plusieurs personnes par courrier électronique. Vous voulez évaluer rapidement qui a reçu ce document interne et externe. Une fois identifié, vous souhaitez partager les conclusions cas avec les autres investigateurs et passez en revue, puis supprimer définitivement les données à partir d’Office 365. Une fois l’enquête terminée, vous souhaitez générer un rapport avec la preuve de suppression définitive et d’autres détails d’un incident pour toute référence ultérieure.
  
### <a name="scope-of-this-article"></a>Portée de cet article

Ce document fournit une liste des instructions sur la façon de supprimer définitivement un message dans Office 365 afin qu’il ne soit pas accessible ou récupérables. Pour supprimer un message et rendre récupérables avant l’expiration de la période de rétention des éléments supprimés, voir [Rechercher et supprimer des messages électroniques dans votre organisation Office 365](search-for-and-delete-messages-in-your-organization.md).
  
## <a name="workflow-for-managing-data-spillage-incidents"></a>Flux de travail pour la gestion des incidents débordements de données

Voici une façon de gérer un incident débordements de données :

![Étape 8 flux de travail pour la gestion des incidents débordements de données](media/O365-eDiscoverySolutions-DataSpillage-workflow.png)
  
[(Facultatif) Étape 1 : Gérer qui peut accéder à la casse et définir des limites de conformité](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)<br/>
[Étape 2 : Créer un cas de découverte électronique](#step-2-create-an-ediscovery-case)<br/>
[Étape 3 : Recherche des données dispersées](#step-3-search-for-the-spilled-data)<br/>
[Étape 4 : Passez en revue et valider les conclusions cas](#step-4-review-and-validate-case-findings)<br/>
[Étape 5 : Utiliser le message de journal de suivi pour vérifier les données comment dispersées a été partagée](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)<br/>
[Étape 6 : Préparer les boîtes aux lettres](#step-6-prepare-the-mailboxes)<br/>
[Étape 7 : Supprimer définitivement les données dispersées](#step-7-permanently-delete-the-spilled-data)<br/>
[Étape 8 : Vérifier, fournir une preuve de suppression et d’audit](#step-8-verify-provide-a-proof-of-deletion-and-audit)<br/>

## <a name="things-to-know-before-you-start"></a>Choses à savoir avant de commencer

- Lorsqu’une boîte aux lettres est en attente, un message supprimé reste dans le dossier éléments récupérables jusqu'à ce que la période de rétention expire ou que le blocage est terminé. [Étape 6](#step-6-prepare-the-mailboxes) décrit comment supprimer la suspension à partir des boîtes aux lettres. Renseignez-vous auprès de votre gestion des enregistrements ou les services juridiques avant la suppression de la suspension. Votre organisation peut avoir une stratégie qui définit si une boîte aux lettres sur blocage ou un incident débordements de données est prioritaire. 
    
- Pour contrôler les boîtes aux lettres utilisateur un enquêteur débordements de données peut rechercher et gérer les personnes autorisées à accéder le cas, vous pouvez définir des limites de conformité et créer un groupe de rôles personnalisé, qui est décrite à [l’étape 1](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries). Pour ce faire, vous devez être membre du groupe de rôles de gestion de l’organisation ou attribuer le rôle de gestion du rôle. Si vous ou dans l’administrateur de votre organisation a déjà des limites de jeu de conformité, vous pouvez ignorer l’étape 1.
    
- Pour créer un cas, vous devez être membre du groupe de rôles de gestionnaire de découverte électronique ou être membre d’un groupe de rôles personnalisé qui a attribué le rôle de gestion des cas. Si vous n’êtes pas un membre, demandez à un administrateur Office 365 [vous ajouter au groupe de rôles gestionnaire eDiscovery](assign-ediscovery-permissions.md).
    
- Pour supprimer les données sont insérées dans votre organisation, vous devez utiliser la commande [Search-Mailbox-DeleteContent](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox?view=exchange-ps) dans Exchange Online PowerShell. En outre, pour utiliser le paramètre *DeleteContent* , vous devez également être membre d’un groupe de rôles dans Exchange Online qui a attribué le rôle de boîte aux lettres importer exporter. Voir la section « Ajouter un rôle à un groupe de rôles » dans [Gérer les groupes de rôles](https://technet.microsoft.com/library/jj657480%28v=exchg.150%29.aspx).
    
- Pour rechercher les activités de découverte de journal d’audit Office 365 à l’étape 8, l’audit doit être activé pour votre organisation. Vous pouvez rechercher des activités qui ont été effectuées au cours des 90 derniers jours. Pour en savoir plus sur l’activation et utiliser l’audit, consultez la section [le processus d’investigation débordements données d’audit](#auditing-the-data-spillage-investigation-process) à l’étape 8. 
    
## <a name="optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries"></a>(Facultatif) Étape 1 : Gérer qui peut accéder à la casse et définir des limites de conformité

En fonction de votre organisation pratique, vous devez contrôler l’accès le cas de découverte électronique utilisé pour identifier un incident débordements de données et de configurer des limites de conformité. Pour ce faire, la plus simple consiste à ajoutez investigateurs en tant que membres d’un groupe de rôles existant dans la sécurité pour Microsoft Office 365 et le centre de conformité, puis ajoutez le groupe de rôles en tant que membre du cas eDiscovery. Pour plus d’informations sur les groupes de rôles intégrés eDiscovery et comment ajouter des membres à un cas eDiscovery, voir [attribuer des autorisations de sécurité Office 365 eDiscovery &amp; centre de conformité](assign-ediscovery-permissions.md).
  
Vous pouvez également créer un nouveau groupe de rôles qui s’aligne sur les besoins de votre organisation. Par exemple, vous pouvez souhaiter un groupe d’investigateurs débordements de données dans l’organisation pour accéder et collaborer sur tous les cas de débordements de données. Vous pouvez le faire en créant un groupe de rôles de « Données débordements enquêteur », attribution des rôles appropriés (exportation, déchiffrement RMS, révision, Preview, recherche de conformité et gestion des cas), ajout investigateurs débordements données au groupe de rôles et puis en ajoutant le groupe de rôles en tant que membre du cas eDiscovery données débordements. Pour obtenir des instructions détaillées sur la procédure à suivre, voir [définir des limites de conformité pour les enquêtes eDiscovery dans Office 365](set-up-compliance-boundaries.md) . 
  
## <a name="step-2-create-an-ediscovery-case"></a>Étape 2 : Créer un cas de découverte électronique

Un cas eDiscovery offre un moyen efficace pour gérer votre investigation débordements de données. Vous pouvez ajouter des membres au groupe de rôles que vous avez créé à l’étape 1, ajoutez le groupe de rôles en tant que membre d’un nouveau cas de découverte électronique, effectuer des recherches itératifs pour rechercher les données dispersées, exporter un état à partager, suivre l’état de la casse et puis faire référence aux détails de la c ASE si nécessaire. Envisagez d’établir une convention d’affectation de noms pour les cas de découverte électronique utilisé pour les incidents débordements de données et fournir autant d’informations que possible dans le cas nom et la description afin de localiser et de faire ultérieurement si nécessaire.
  
Pour créer un nouveau cas, vous pouvez utiliser la découverte électronique dans la sécurité &amp; centre de conformité. Consultez la rubrique « Créer un nouveau cas » en [cas de découverte de la sécurité pour Microsoft Office 365 et le centre de conformité](ediscovery-cases.md#step-2-create-a-new-case).
  
## <a name="step-3-search-for-the-spilled-data"></a>Étape 3 : Recherche des données dispersées

Maintenant que vous avez créé un cas et un accès géré, vous pouvez utiliser le cas de façon itérative Rechercher pour trouver les données dispersées et identifier les boîtes aux lettres qui contiennent les données dispersées. Vous allez utiliser la même requête de recherche que vous avez utilisé pour rechercher les messages électroniques pour supprimer ces messages même à [l’étape 7](#step-7-permanently-delete-the-spilled-data).
  
Pour créer un contenu recherches associé à un cas eDiscovery, consultez la rubrique « Créer et exécuter qu'une recherche de contenu associée à un cas » en [cas de découverte de la sécurité pour Microsoft Office 365 et le centre de conformité](ediscovery-cases.md#step-5-create-and-run-a-content-search-associated-with-a-case).
  
 **Important :** Les mots clés que vous utilisez dans la requête de recherche peuvent contenir des données réelles dispersées que vous recherchez. Par exemple, si vous recherchez des documents contenant un numéro de sécurité sociale et que vous utilisez comme mots clés de recherche de l’informatique, vous devez supprimer la requête par la suite pour éviter de débordements. Consultez la rubrique [suppression de la requête de recherche](#deleting-the-search-query) à l’étape 8. 
  
## <a name="step-4-review-and-validate-case-findings"></a>Étape 4 : Passez en revue et valider les conclusions cas

Après avoir créé une recherche de contenu, vous devez passer en revue et valider que la recherche des résultats et vérifiez qu’ils se composent uniquement des messages électroniques qui doivent être supprimés. Dans une recherche de contenu, vous pouvez afficher un aperçu un sondage de 1 000 messages électroniques sans exporter les résultats de recherche pour éviter de débordements de données. Vous pouvez en savoir plus sur les limitations de l’aperçu à [limites pour la recherche de contenu de sécurité Office 365 &amp; centre de conformité](limits-for-content-search.md).
  
Si vous avez plus de 1 000 boîtes aux lettres ou plus de 100 messages électroniques par boîte aux lettres pour passer en revue, vous pouvez diviser la recherche initiale en plusieurs recherches à l’aide de mots clés supplémentaires ou des expéditeurs/destinataires ou une plage de dates et passez en revue les résultats de chaque recherche individuellement. Veillez à noter vers le bas toutes les requêtes de recherche à utiliser lorsque vous supprimez des messages à [l’étape 7](#step-7-permanently-delete-the-spilled-data).

Si un dépositaire ou un utilisateur final est attribué une licence Office 36 E5, vous pouvez examiner jusqu'à 10 000 résultats de recherche à l’aide d’Office 365 avancée de découverte électronique. S’il y a plus de 10 000 messages électroniques pour passer en revue, vous pouvez diviser la requête de recherche par plage de dates et passez en revue chaque résultat individuellement et en tant que les résultats sont triés par date de recherche. D’eDiscovery avancé, vous pouvez ajouter une balise à l’aide de la fonctionnalité **d’étiquette en tant que** dans le panneau d’aperçu des résultats de recherche et filtrer les résultats de recherche à la balise que vous l’avez étiqueté. Cela est utile lorsque vous collaborez avec un réviseur secondaire. À l’aide des outils supplémentaires analytique d’eDiscovery avancée, telles que la reconnaissance optique de caractères, les threads de messagerie et de codage prédictive, en rapidement traiter et passez en revue des milliers de messages et les marquer pour une révision supplémentaire. Voir [le programme d’installation rapide pour la découverte Office 365 avancés](quick-setup-for-advanced-ediscovery.md).

Lorsque vous avez trouvé un message électronique qui contient des données dispersées, vérifiez les destinataires du message pour déterminer si elle a été partagée en externe. Trace supplémentaire un message, vous pouvez collecter des informations sur l’expéditeur et la plage de dates afin de pouvoir utiliser les journaux de suivi des messages, qui est décrite à [l’étape 5](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared).

Permet de vous vérifié les résultats de recherche, vous souhaiterez peut-être partager vos résultats avec d’autres personnes pour une révision secondaire. Personnes qui vous a assigné au cas à l’étape 1 peuvent examiner le contenu cas eDiscovery et découverte avancée et approuver des constatations cas. Vous pouvez également générer un rapport sans exporter le contenu réel. Vous pouvez également utiliser le même rapport comme preuve de suppression, qui est décrite à [l’étape 8](#step-8-verify-provide-a-proof-of-deletion-and-audit).
  
 **Pour générer un rapport de statistique :**
  
1. Accédez à la page de **recherche** dans le cas de découverte électronique, cliquez sur la recherche que vous souhaitez générer un rapport. 
    
2. Dans la page mobile, cliquez sur **plus > Exporter rapport**.
 
      La page de rapport d’exportation s’affiche.

    ![Sélectionnez la recherche, puis cliquez sur Autres > Exporter le rapport dans la page flottant](media/O365-eDiscoverySolutions-DataSpillage-ExportReport1.png)
    
3. Sélectionnez **tous les éléments, y compris celles qui ont un format non reconnu, sont chiffrées, ou n’ont pas été indexés pour d’autres raisons** , puis cliquez sur **Générer un rapport**.

4. Dans le cas de découverte électronique, cliquez sur **Exporter** pour afficher la liste des travaux de l’exportation. Vous devrez peut-être cliquer sur **Actualiser** pour mettre à jour la liste pour afficher la tâche d’exportation que vous venez de créer.

5. Cliquez sur la tâche d’exportation, puis cliquez sur **Télécharger** le rapport dans la page mobile.
 
    ![Dans la page Exporter, cliquez sur l’exportation, puis cliquez sur « Télécharger le rapport »](media/O365-eDiscoverySolutions-DataSpillage-ExportReport2.png)

Le rapport de **Synthèse exporter** contient le nombre d’emplacements trouvés dans les résultats et la taille des résultats de recherche. Vous pouvez utiliser ce à comparer avec le rapport généré après suppression et fournir une preuve de suppression. Le rapport de **résultats** contient une synthèse plus détaillée des résultats de recherche, y compris l’objet, expéditeur, destinataires, si le message électronique a été lu, dates et taille de chaque message. Si les détails de ce rapport contient ces données dispersées réelles, veillez à supprimer définitivement le fichier Results.csv lors de l’enquête est terminée.

Pour plus d’informations sur l’exportation des rapports, consultez la rubrique [Exporter un rapport de recherche de contenu](export-a-content-search-report.md).
    
## <a name="step-5-use-message-trace-log-to-check-how-spilled-data-was-shared"></a>Étape 5 : Utiliser le message de journal de suivi pour vérifier les données comment dispersées a été partagée

Pour examiner si le message électronique avec des données dispersées a été partagée, vous pouvez éventuellement interroger les journaux de suivi des messages avec les informations de l’expéditeur et les informations de plage de date que vous avez rassemblées à l’étape 4. Notez que la période de rétention pour le suivi des messages est de 30 jours de données en temps réel et les données d’historique de 90 jours.
  
Vous pouvez utiliser le suivi des messages dans le centre de conformité & de sécurité ou utiliser les applets de commande correspondante dans Exchange Online PowerShell. Il est important de noter que toute garantie sur la conformité des données renvoyées ne propose pas de suivi des messages. Pour plus d’informations sur l’utilisation du suivi des messages, voir : 
  
- [Suivi de sécurité Office 365 des messages &amp; centre de conformité](https://support.office.com/article/3e64f99d-ac33-4aba-91c5-9cb4ca476803.aspx)
    
- [Nouveau suivi des messages de la sécurité Office 365 &amp; centre de conformité](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)
    
## <a name="step-6-prepare-the-mailboxes"></a>Étape 6 : Préparer les boîtes aux lettres

Une fois que vous passez en revue et validez que les résultats de recherche contient uniquement les messages qui doivent être supprimés, vous devez recueillir une liste d’adresses de messagerie des boîtes aux lettres affectés à utiliser à l’étape 7, lorsque vous exécutez la commande **Search-Mailbox-DeleteContent** . Vous pouvez aussi avoir préparer les boîtes aux lettres avant de pouvoir supprimer définitivement les messages électroniques en fonction de la récupération d’élément unique est activée ou non sur les boîtes aux lettres qui contiennent les données dispersées ou si une de ces boîtes aux lettres est sur le blocage.
  
### <a name="get-a-list-of-addresses-of-mailboxes-with-spilled-data"></a>Obtenir une liste d’adresses de boîtes aux lettres avec les données dispersées

Il existe deux façons pour collecter une liste d’adresses de messagerie des boîtes aux lettres avec les données dispersées.

**Option 1 : Obtenir une liste d’adresses de boîtes aux lettres avec les données dispersées**

1. Ouvrez le cas de découverte électronique, accédez à la page de **recherche** et sélectionnez la recherche de contenu appropriée. 
    
2. Dans la page mobile, cliquez sur **Afficher les résultats**.
    
3. Dans la liste déroulante **les résultats** , cliquez sur **les statistiques de recherche**.
    
4. Dans la liste déroulante **Type** , cliquez sur **emplacements supérieurs**.
    
    ![Obtenir la liste des boîtes aux lettres qui contiennent des résultats de la recherche dans la page emplacements supérieure dans les statistiques de recherche](media/O365-eDiscoverySolutions-DataSpillage-TopLocations.png)

    Une liste des boîtes aux lettres qui contiennent des résultats de la recherche s’affiche. Le nombre d’éléments dans chaque boîte aux lettres qui correspondent à la requête de recherche est également affiché.
    
5. Copier les informations dans la liste et enregistrez-le dans un fichier ou cliquez sur **Télécharger** pour télécharger les informations dans un fichier CSV. 
    
**Option 2 : Obtenir les emplacements de boîte aux lettres à partir du rapport d’exportation**

Ouvrez le rapport de synthèse exporter que vous avez téléchargé à [l’étape 4](#step-4-review-and-validate-case-findings). Dans la première colonne dans le rapport, l’adresse de messagerie de chaque boîte aux lettres est répertorié sous **emplacements**.
  
### <a name="prepare-the-mailboxes-so-you-can-delete-the-spilled-data"></a>Préparer les boîtes aux lettres, vous pouvez supprimer les données dispersées

Si la récupération d’élément unique est activée ou si une boîte aux lettres est mis en attente, un message (purgé) définitivement supprimé est conservé dans le dossier éléments récupérables. Donc avant que vous pouvez vider les données dispersées, vous devez vérifier la configuration de boîte aux lettres existante et désactiver la récupération d’élément unique et supprimer toute attente ou la stratégie de rétention d’Office 365. N’oubliez pas que vous pouvez préparer une boîte aux lettres à la fois, puis exécuter la même commande sur différentes boîtes aux lettres ou créer un script PowerShell pour préparer plusieurs boîtes aux lettres en même temps.

- Voir « étape 1 : collecter des informations sur la boîte aux lettres » dans la zone [Supprimer des éléments dans les éléments récupérables dossier du nuage des boîtes aux lettres sur Maintenez](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-1-collect-information-about-the-mailbox) pour obtenir des instructions sur la façon de vérifier si la récupération d’élément unique est activée ou si la boîte aux lettres est mis en attente ou elle est attribuée à un stratégie de rétention. 
    
- Consultez la rubrique « étape 2 : préparer la boîte aux lettres » dans la zone [Supprimer des éléments dans les éléments récupérables dossier du nuage des boîtes aux lettres sur Maintenez](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-2-prepare-the-mailbox) pour obtenir des instructions sur la désactivation de récupération d’élément unique. 
    
- Consultez la rubrique « étape 3 : supprimer toutes les suspensions à partir de la boîte aux lettres » dans la zone [Supprimer des éléments dans les éléments récupérables dossier du nuage des boîtes aux lettres sur Maintenez](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-3-remove-all-holds-from-the-mailbox) pour obtenir des instructions sur la façon de supprimer une stratégie de blocage ou de rétention d’une boîte aux lettres. 

- Consultez la rubrique « étape 4 : supprimer le délai d’attente à partir de la boîte aux lettres » dans la zone [Supprimer des éléments dans les éléments récupérables dossier du nuage des boîtes aux lettres sur Maintenez](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-4-remove-the-delay-hold-from-the-mailbox) pour obtenir des instructions sur la suppression de la suspension de délai d’attente est placée sur la boîte aux lettres après la suppression de n’importe quel type de suspension.
    
 **Important :** Renseignez-vous auprès de votre gestion des enregistrements ou les services juridiques avant la suppression d’une stratégie de blocage ou de rétention. Votre organisation peut avoir une stratégie qui définit si une boîte aux lettres sur blocage ou un incident débordements de données est prioritaire. 
  
N’oubliez pas de rétablir la boîte aux lettres pour les configurations précédentes après avoir vérifié que les données dispersées a été définitivement supprimées. Voir les détails à [l’étape 7](#step-7-permanently-delete-the-spilled-data).

## <a name="step-7-permanently-delete-the-spilled-data"></a>Étape 7 : Supprimer définitivement les données dispersées

Utilisant les emplacements de boîte aux lettres collectées que vous avez préparé à l’étape 6 et la requête de recherche qui a été créée et affinée à l’étape 3 pour rechercher les messages électroniques qui contiennent les données dispersées, vous pouvez désormais supprimer définitivement les données dispersées. Comme expliqué précédemment, vous devez disposer du rôle de boîte aux lettres importer exporter dans Exchange Online pour supprimer des messages à l’aide de la procédure suivante.
  
1. [Connectez-vous à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
2. Exécutez la commande suivante :
    
    ```
    Search-Mailbox -Identity <mailbox identity> -SearchDumpster -DeleteContent $true -SearchQuery <search query>
    ```
  
3. Exécutez de nouveau la commande précédente pour chaque boîte aux lettres qui contient les données dispersées, en remplaçant la valeur pour le paramètre Identity ; par exemple :

    ```
    Search-Mailbox -Identity sarad@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

    ```
    Search-Mailbox -Identity janets@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

   ```
   Search-Mailbox -Identity pilarp@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
   ```
  
Comme indiqué précédemment, vous pouvez également créer un [script powershell](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6) et exécuter par rapport à une liste de boîtes aux lettres afin que le script supprime les données dispersées dans chaque boîte aux lettres.
  
## <a name="step-8-verify-provide-a-proof-of-deletion-and-audit"></a>Étape 8 : Vérifier, fournir une preuve de suppression et d’audit

La dernière étape de flux de travail pour gérer un incident débordements de données consiste à vérifier que les données dispersées a été définitivement supprimées de la boîte aux lettres en accédant au cas eDiscovery et réexécuter la même requête de recherche qui a été utilisée pour ne supprimer ces données afin de confirmer qu’aucune ar de résultats e renvoyée. Après avoir vérifié que les données dispersées a été définitivement supprimées, vous pouvez exporter un rapport et inclure (ainsi que l’état d’origine) comme preuve de suppression. Vous pouvez ensuite [Fermer le cas](ediscovery-cases.md#optional-step-9-close-a-case), afin de pouvoir ouvrir à nouveau si vous avez vous y référer ultérieurement. En outre, vous pouvez également rétablir des boîtes aux lettres à leur état précédent, supprimer la requête de recherche utilisée pour rechercher les données dispersées, pour auditer les enregistrements des tâches effectuées lors de la gestion de l’incident débordements de données de recherche. 
  
### <a name="reverting-the-mailboxes-to-their-previous-state"></a>Restauration des boîtes aux lettres à leur état antérieur

Si vous avez modifié toutes les configurations de boîte aux lettres à l’étape 6 pour préparer les boîtes aux lettres avant que les données dispersées a été supprimées, vous devrez les restaurer à leur état antérieur. Voir « étape 6 : rétablir la boîte aux lettres à son état antérieur » de [Supprimer des éléments dans les éléments récupérables dossier de boîtes aux lettres en nuage sur contenir](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-6-revert-the-mailbox-to-its-previous-state).
  
### <a name="deleting-the-search-query"></a>Suppression de la requête de recherche

Si les mots clés dans la requête de recherche que vous avez créé et utilisé dans l’étape 3 contient certains ou tous les données réelles dispersées, vous devez supprimer la requête de recherche afin d’éviter les débordements de données.
  
1. Dans la sécurité et le centre de conformité, ouvrez le cas de découverte électronique, accédez à la page de **recherche** et sélectionnez la recherche de contenu appropriée.
    
2. Dans la page mobile, cliquez sur **Supprimer**.

    ![Sélectionnez la recherche, puis cliquez sur Supprimer dans la page flottant](media/O365-eDiscoverySolutions-DataSpillage-DeleteSearch.png)
    
### <a name="auditing-the-data-spillage-investigation-process"></a>Le processus d’investigation débordements données d’audit

Vous pouvez rechercher le journal d’audit de Office 365 pour les activités de découverte électronique qui ont été effectuées lors de l’enquête. Vous pouvez également rechercher le journal d’audit pour retourner les enregistrements d’audit qui ont été créées lorsque vous avez exécuté la commande **Search-Mailbox-DeleteContent** pour supprimer les données dispersées. Pour plus d’informations, voir :

- [Effectuer des recherches dans le journal d’audit dans le Centre de sécurité et de conformité Office 365](search-the-audit-log-in-security-and-compliance.md)

- [Rechercher des activités de découverte électronique dans le journal d’audit d’Office 365](search-for-ediscovery-activities-in-the-audit-log.md)

- Consultez la section « Audit des activités - journal d’audit de l’administrateur Exchange » dans la [recherche, ouvrez une session de l’audit dans la sécurité pour Microsoft Office 365 et le centre de conformité](search-the-audit-log-in-security-and-compliance.md#audited-activities) pour obtenir des conseils sur la recherche pour les enregistrements d’audit liés à l’exécution des applets de commande dans Exchange Online.
  

