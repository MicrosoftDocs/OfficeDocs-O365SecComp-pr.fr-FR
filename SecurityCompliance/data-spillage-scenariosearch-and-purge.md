---
title: scénario de fuite de données de série de solutions eDiscovery-recherche et vidage
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MET150
ms.assetid: d945f7dd-f62f-4ca7-b3e7-469824cfd493
description: Utilisez les outils de découverte électronique et de recherche Office 365 pour gérer et répondre à un incident de débordement de données dans votre organisation.
ms.openlocfilehash: 50fab420ae0769e4675c5b6ff31307fa195d3950
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296597"
---
# <a name="ediscovery-solution-series-data-spillage-scenario---search-and-purge"></a>série de solutions eDiscovery: scénario de fuite de données-recherche et purge

 **Qu'est-ce que la fuite de données et pourquoi?** Le débordement de données se fait lorsqu'un document confidentiel est publié dans un environnement non approuvé. Lors de la détection d'un incident de débordement de données, il est important d'évaluer rapidement la taille et les emplacements du détournement, d'examiner les activités de l'utilisateur et de purger définitivement les données propagées du système. 
  
## <a name="data-spillage-scenario"></a>Scénario de fuite de données

Vous êtes responsable de la sécurité des informations chez contoso. Vous êtes informé d'une situation de débordement de données dans laquelle un employé a volontairement partagé un document hautement confidentiel avec plusieurs personnes par courrier électronique. Vous souhaitez évaluer rapidement qui a reçu ce document en interne et en externe. Une fois identifié, vous aimeriez partager les résultats de la demande de devis avec d'autres investigateurs à réviser, puis supprimer définitivement les données d'Office 365. Une fois l'enquête terminée, vous souhaitez générer un rapport avec la preuve de la suppression permanente et d'autres détails de cas pour toute référence ultérieure.
  
### <a name="scope-of-this-article"></a>Portée de cet article

Ce document fournit une liste d'instructions sur la suppression définitive d'un message d'Office 365 afin qu'il ne soit pas accessible ou récupérable. Pour supprimer un message et le restaurer jusqu'à l'expiration de la période de rétention des éléments supprimés, consultez la rubrique [Rechercher et supprimer des messages électroniques dans votre organisation Office 365](search-for-and-delete-messages-in-your-organization.md).
  
## <a name="workflow-for-managing-data-spillage-incidents"></a>Flux de travail pour la gestion des incidents de fuite de données

Voici comment gérer un incident de fuite de données:

![Flux de travail en 8 étapes pour la gestion des incidents de débordement de données](media/O365-eDiscoverySolutions-DataSpillage-workflow.png)
  
[Module Étape 1: gérer les personnes pouvant accéder à la demande de devis et définir les limites de conformité](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries)<br/>
[Étape 2: créer un cas eDiscovery](#step-2-create-an-ediscovery-case)<br/>
[Étape 3: Rechercher les données déversées](#step-3-search-for-the-spilled-data)<br/>
[Étape 4: vérifier et valider les résultats de la demande de devis](#step-4-review-and-validate-case-findings)<br/>
[Étape 5: utiliser le journal de suivi des messages pour vérifier le mode de partage des données propagées](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared)<br/>
[Étape 6: préparer les boîtes aux lettres](#step-6-prepare-the-mailboxes)<br/>
[Étape 7: supprimer définitivement les données propagées](#step-7-permanently-delete-the-spilled-data)<br/>
[Étape 8: vérifier, fournir une preuve de suppression et d'audit](#step-8-verify-provide-a-proof-of-deletion-and-audit)<br/>

## <a name="things-to-know-before-you-start"></a>Éléments à savoir avant de commencer

- Lorsqu'une boîte aux lettres est en attente, un message supprimé reste dans le dossier éléments récupérables jusqu'à ce que la période de rétention expire ou que la conservation soit libérée. L' [étape 6](#step-6-prepare-the-mailboxes) explique comment supprimer le blocage des boîtes aux lettres. Vérifiez la gestion des enregistrements ou les services juridiques avant de supprimer la conservation. Votre organisation peut avoir une stratégie qui détermine si une boîte aux lettres en attente ou un incident de débordement de données est prioritaire. 
    
- Pour contrôler les boîtes aux lettres utilisateur qu'un enquêteur de fuite de données peut rechercher et gérer les personnes pouvant accéder à l'incident, vous pouvez configurer les limites de conformité et créer un groupe de rôles personnalisé, décrit à l' [étape 1](#optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries). Pour ce faire, vous devez être membre du groupe de rôles gestion de l'organisation ou disposer du rôle de gestion des rôles. Si vous ou un administrateur de votre organisation avez déjà défini les limites de conformité, vous pouvez ignorer l'étape 1.
    
- Pour créer un cas, vous devez être membre du groupe de rôles gestionnaire eDiscovery ou être membre d'un groupe de rôles personnalisé auquel est attribué le rôle de gestion des cas. Si vous n'êtes pas membre [du groupe de rôles gestionnaire eDiscovery](assign-ediscovery-permissions.md), demandez à un administrateur Office 365 de vous ajouter.
    
- Pour supprimer les données propagées dans votre organisation, vous devez utiliser la commande [Search-Mailbox-DeleteContent](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Search-Mailbox?view=exchange-ps) dans Exchange Online PowerShell. En outre, pour utiliser le paramètre *DeleteContent* , vous devez également être membre d'un groupe de rôles dans Exchange Online auquel le rôle d'importation/exportation de boîte aux lettres est attribué. Consultez la section «Ajouter un rôle à un groupe de rôles» dans [gérer des groupes de rôles](https://technet.microsoft.com/library/jj657480%28v=exchg.150%29.aspx).
    
- Pour effectuer une recherche dans le journal d'audit Office 365 activités de découverte électronique à l'étape 8, l'audit doit être activé pour votre organisation. Vous pouvez rechercher des activités qui ont eu lieu au cours des 90 derniers jours. Pour en savoir plus sur l'activation et l'utilisation de l'audit, consultez la section [audit du processus d'enquête sur la fuite de données](#auditing-the-data-spillage-investigation-process) à l'étape 8. 
    
## <a name="optional-step-1-manage-who-can-access-the-case-and-set-compliance-boundaries"></a>Module Étape 1: gérer les personnes pouvant accéder à la demande de devis et définir les limites de conformité

En fonction de votre pratique de l'organisation, vous devez contrôler qui peut accéder au cas eDiscovery utilisé pour examiner un incident de débordement de données et définir des limites de conformité. Pour ce faire, la méthode la plus simple consiste à ajouter des enquêteurs en tant que membres d'un groupe de rôles existant dans le centre de sécurité & de sécurité Office 365, puis à ajouter le groupe de rôles en tant que membre du cas de découverte électronique. Pour plus d'informations sur les groupes de rôles eDiscovery intégrés et sur la façon d'ajouter des membres à un cas de découverte électronique, consultez [la rubrique &amp; attribution d'autorisations eDiscovery dans le centre de sécurité conformité Office 365](assign-ediscovery-permissions.md).
  
Vous pouvez également créer un nouveau groupe de rôles qui s'aligne sur les besoins de votre organisation. Par exemple, vous souhaiterez peut-être un groupe d'investigateurs de débordement de données dans l'Organisation pour accéder à tous les cas de débordement de données et collaborer dessus. Pour ce faire, vous pouvez créer un groupe de rôles «enquêteur de fuite de données», attribuer les rôles appropriés (exportation, déChiffrement RMS, révision, aperçu, recherche de conformité et gestion des cas), en ajoutant les investigations de débordement de données au groupe de rôles, puis en ajoutant le Groupe de rôles en tant que membre du cas de découverte électronique de fuite de données. Pour obtenir des instructions détaillées sur la façon de procéder, voir [configurer les limites de conformité pour les enquêtes de découverte électronique dans Office 365](set-up-compliance-boundaries.md) . 
  
## <a name="step-2-create-an-ediscovery-case"></a>Étape 2: créer un cas eDiscovery

Un cas de découverte électronique offre un moyen efficace de gérer votre enquête sur la fuite de données. Vous pouvez ajouter des membres au groupe de rôles que vous avez créé à l'étape 1, ajouter le groupe de rôles en tant que membre d'un nouveau cas eDiscovery, effectuer des recherches itératives pour trouver les données déplacées, exporter un rapport pour partager, suivre l'état de la demande de devis, puis renvoyer aux détails du c ASE si nécessaire. EnVisagez d'établir une convention d'affectation de noms pour les cas eDiscovery utilisés pour les incidents de déversement de données, et fournissez autant d'informations que possible dans le nom et la description de l'incident, de sorte que vous puissiez trouver et consulter à l'avenir, si nécessaire.
  
Pour créer un nouvel incident, vous pouvez utiliser eDiscovery dans le centre &amp; de sécurité conformité. Voir «créer un nouveau cas» dans [les cas de découverte électronique dans le centre de sécurité & de la sécurité d'Office 365](ediscovery-cases.md#step-2-create-a-new-case).
  
## <a name="step-3-search-for-the-spilled-data"></a>Étape 3: Rechercher les données déversées

À présent que vous avez créé un cas et un accès géré, vous pouvez utiliser le cas pour effectuer une recherche itérative afin de trouver les données déduites et identifier les boîtes aux lettres qui contiennent les données déduites. Vous allez utiliser la même requête de recherche que celle que vous avez utilisée pour rechercher les messages électroniques afin de supprimer ces mêmes messages à l' [étape 7](#step-7-permanently-delete-the-spilled-data).
  
Pour créer une recherche de contenu associée à un cas de découverte électronique, voir «Création et exécution d'une recherche de contenu associée à un cas» dans [cas de découverte électronique dans le centre de sécurité & de la sécurité d'Office 365](ediscovery-cases.md#step-5-create-and-run-a-content-search-associated-with-a-case).
  
 **Important:** Les mots clés que vous utilisez dans la requête de recherche peuvent contenir les données propagées réelles que vous recherchez. Par exemple, si vous recherchez des documents contenant un numéro de sécurité sociale et que vous utilisez le mot clé de recherche en tant que, vous devez supprimer la requête par la suite afin d'éviter toute aggravation. Consultez [la rubrique Suppression de la requête de recherche](#deleting-the-search-query) à l'étape 8. 
  
## <a name="step-4-review-and-validate-case-findings"></a>Étape 4: vérifier et valider les résultats de la demande de devis

Après avoir créé une recherche de contenu, vous devez vérifier et valider les résultats de la recherche et vérifier qu'ils consistent uniquement sur les messages électroniques qui doivent être supprimés. Dans une recherche de contenu, vous pouvez prévisualiser un échantillon aléatoire de 1 000 messages électroniques sans exporter les résultats de la recherche pour éviter d'autres dépassements de données. Pour en savoir plus sur les limitations d'aperçu, consultez la rubrique [limites de recherche de contenu &amp; dans le centre de sécurité conformité Office 365](limits-for-content-search.md).
  
Si vous avez plus de 1 000 boîtes aux lettres ou plus de 100 messages électroniques par boîte aux lettres à réviser, vous pouvez diviser la recherche initiale en plusieurs recherches à l'aide de mots clés ou de conditions supplémentaires, tels que la plage de dates ou l'expéditeur/destinataire et consulter les résultats de chaque recherche. restaur. Notez toutes les requêtes de recherche à utiliser lors de la suppression des messages à l' [étape 7](#step-7-permanently-delete-the-spilled-data).

Si une licence Office 36 E5 est attribuée à un dépositaire ou à un utilisateur final, vous pouvez examiner jusqu'à 10 000 résultats de recherche à la fois à l'aide d'Office 365 Advanced eDiscovery. S'il y a plus de 10 000 messages électroniques à examiner, vous pouvez diviser la requête de recherche par plage de dates et examiner chaque résultat individuellement à mesure que les résultats de la recherche sont triés par date. Dans Advanced eDiscovery, vous pouvez baliser les résultats de la recherche à l'aide de la fonctionnalité **étiquette en tant que** dans le panneau Aperçu et filtrer les résultats de la recherche en fonction de la balise que vous avez marquée. Cette fonction est utile lorsque vous collaborez avec un réviseur secondaire. En utilisant des outils d'analyse supplémentaires dans Advanced eDiscovery, tels que la reconnaissance optique de caractères, le Threading de messagerie électronique et le codage prédictif, vous pouvez rapidement traiter et examiner des milliers de messages et les baliser pour révision. Voir [Quick Setup for Office 365 Advanced eDiscovery](quick-setup-for-advanced-ediscovery.md).

Lorsque vous trouvez un message électronique contenant des données déduites, vérifiez les destinataires du message afin de déterminer s'il a été partagé en externe. Pour poursuivre le suivi d'un message, vous pouvez collecter les informations et la plage de dates de l'expéditeur de sorte que vous puissiez utiliser les journaux de suivi des messages, comme décrit à l' [étape 5](#step-5-use-message-trace-log-to-check-how-spilled-data-was-shared).

Afer vous avez vérifié les résultats de la recherche, vous souhaiterez peut-être partager vos découvertes avec d'autres personnes pour une révision secondaire. Les personnes auxquelles vous avez attribué le cas à l'étape 1 peuvent passer en revue le contenu de la découverte électronique avancée et eDiscovery et approuver les résultats de la recherche de cas. Vous pouvez également générer un rapport sans exporter le contenu réel. Vous pouvez également utiliser ce même rapport comme preuve de suppression, comme décrit à l' [étape 8](#step-8-verify-provide-a-proof-of-deletion-and-audit).
  
 **Pour générer un rapport statistique:**
  
1. Accédez à la page de **recherche** dans le cas de découverte électronique, puis cliquez sur la recherche pour laquelle vous souhaitez générer un rapport. 
    
2. Sur la page de menu volant, cliquez sur **plus d' _GT_ exporter le rapport**.
 
      La page exporter le rapport s'affiche.

    ![Sélectionnez la recherche, puis cliquez sur plus d' > exporter le rapport sur la page de menu volant](media/O365-eDiscoverySolutions-DataSpillage-ExportReport1.png)
    
3. Sélectionnez **tous les éléments, y compris ceux dont le format n'est pas reconnu, sont chiffrés ou n'ont pas été indexés pour d'autres raisons** , puis cliquez sur **générer un rapport**.

4. Dans le cas de découverte électronique, cliquez sur **Exporter** pour afficher la liste des travaux d'exportation. Vous devrez peut-être **** cliquer sur Actualiser pour mettre à jour la liste afin d'afficher le travail d'exportation que vous venez de créer.

5. Cliquez sur le travail d'exportation, puis sur **Télécharger** le rapport sur la page de menu volant.
 
    ![Sur la page exporter, cliquez sur Exporter, puis cliquez sur Télécharger le rapport.](media/O365-eDiscoverySolutions-DataSpillage-ExportReport2.png)

Le rapport Résumé de l' **exportation** contient le nombre d'emplacements trouvés avec les résultats et la taille des résultats de la recherche. Vous pouvez utiliser cette fonction pour effectuer une comparaison avec le rapport généré après suppression et fournir une preuve de suppression. Le rapport de **résultats** contient un résumé plus détaillé des résultats de la recherche, y compris l'objet, l'expéditeur, les destinataires, si le courrier électronique a été lu, les dates et la taille de chaque message. Si l'une des informations contenues dans ce rapport contient des données propagées réelles, veillez à supprimer définitivement le fichier results. csv une fois l'examen terminé.

Pour plus d'informations sur l'exportation des rapports, voir [exporter un rapport de recherche de contenu](export-a-content-search-report.md).
    
## <a name="step-5-use-message-trace-log-to-check-how-spilled-data-was-shared"></a>Étape 5: utiliser le journal de suivi des messages pour vérifier le mode de partage des données propagées

Pour plus d'informations sur le partage de messages avec des données mises en page, vous pouvez éventuellement interroger les journaux de suivi des messages avec les informations relatives à l'expéditeur et la plage de dates que vous avez collectées à l'étape 4. Notez que la période de rétention pour le suivi des messages est de 30 jours pour les données en temps réel et de 90 jours pour les données historiques.
  
Vous pouvez utiliser le suivi des messages dans le centre de sécurité & Compliance Center ou utiliser les cmdlets correspondantes dans Exchange Online PowerShell. Il est important de noter que le suivi des messages ne propose pas de garanties complètes quant à l'intégralité des données renvoyées. Pour plus d'informations sur l'utilisation du suivi des messages, voir: 
  
- [Suivi des messages dans le centre de &amp; sécurité conformité Office 365](https://support.office.com/article/3e64f99d-ac33-4aba-91c5-9cb4ca476803.aspx)
    
- [Nouveau suivi des messages dans le centre &amp; de sécurité conformité Office 365](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/)
    
## <a name="step-6-prepare-the-mailboxes"></a>Étape 6: préparer les boîtes aux lettres

Une fois que vous avez examiné et vérifié que les résultats de la recherche contiennent uniquement les messages qui doivent être supprimés, vous devez collecter une liste des adresses de messagerie des boîtes aux lettres affectées à utiliser à l'étape 7 lorsque vous exécutez la commande **Search-Mailbox-DeleteContent** . Vous devrez peut-être également préparer les boîtes aux lettres avant de pouvoir supprimer définitivement les messages électroniques selon que la récupération d'élément unique est activée ou non sur les boîtes aux lettres qui contiennent les données déversées ou si une de ces boîtes aux lettres est en attente.
  
### <a name="get-a-list-of-addresses-of-mailboxes-with-spilled-data"></a>Obtenir la liste des adresses des boîtes aux lettres avec des données déduites

Il existe deux façons de collecter une liste d'adresses de messagerie de boîtes aux lettres avec des données déduites.

**Option 1: obtenir la liste des adresses des boîtes aux lettres avec des données déduites**

1. Ouvrez le cas eDiscovery, accédez à la page de **recherche** et sélectionnez la recherche de contenu appropriée. 
    
2. Sur la page de la fenêtre volante, cliquez sur **afficher les résultats**.
    
3. Dans la liste déroulante **résultats individuels** , cliquez sur **statistiques de recherche**.
    
4. Dans la liste déroulante **type** , cliquez sur **emplacements principaux**.
    
    ![Obtenir la liste des boîtes aux lettres qui contiennent des résultats de recherche sur la page des sites de niveau supérieur dans les statistiques de recherche](media/O365-eDiscoverySolutions-DataSpillage-TopLocations.png)

    La liste des boîtes aux lettres qui contiennent les résultats de la recherche s'affiche. Le nombre d'éléments dans chaque boîte aux lettres qui correspondent à la requête de recherche est également affiché.
    
5. Copiez les informations de la liste et enregistrez-les dans un fichier ou cliquez sur **Télécharger** pour télécharger les informations dans un fichier CSV. 
    
**Option 2: obtenir des emplacements de boîte aux lettres à partir du rapport d'exportation**

Ouvrez le rapport de synthèse d'exportation que vous avez téléchargé à l' [étape 4](#step-4-review-and-validate-case-findings). Dans la première colonne du rapport, l'adresse de messagerie de chaque boîte aux lettres est indiquée sous **emplacements**.
  
### <a name="prepare-the-mailboxes-so-you-can-delete-the-spilled-data"></a>Préparer les boîtes aux lettres afin de pouvoir supprimer les données déduites

Si la récupération d'élément unique est activée ou si une boîte aux lettres est placée en conservation, un message supprimé définitivement (purgé) est conservé dans le dossier éléments récupérables. Par conséquent, avant de pouvoir purger les données débloquées, vous devez vérifier les configurations de boîte aux lettres existantes et désactiver la récupération d'élément unique et supprimer les stratégies de rétention de blocage ou Office 365. N'oubliez pas que vous pouvez préparer une boîte aux lettres à la fois, puis exécuter la même commande sur différentes boîtes aux lettres ou créer un script PowerShell pour préparer plusieurs boîtes aux lettres en même temps.

- Voir «étape 1: collecte des informations sur la boîte aux lettres» dans [supprimer des éléments du dossier éléments récupérables des boîtes aux lettres en nuage](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-1-collect-information-about-the-mailbox) pour obtenir des instructions sur la manière de vérifier si la récupération d'élément unique est activée ou si la boîte aux lettres est placée en conservation ou si elle est affectée à un stratégie de rétention. 
    
- Pour obtenir des instructions sur la désactivation de la récupération d'élément unique, voir «étape 2: préparer la boîte aux lettres» dans [supprimer des éléments du dossier éléments récupérables des boîtes aux lettres en nuage](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-2-prepare-the-mailbox) . 
    
- Pour obtenir des instructions sur la suppression d'une stratégie de conservation ou de rétention d'une boîte aux lettres, consultez la section «étape 3: supprimer toutes les suspensions de la boîte aux lettres» dans [la rubrique Suppression des éléments du dossier éléments récupérables des boîtes aux lettres en nuage](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-3-remove-all-holds-from-the-mailbox) . 

- Consultez la section «étape 4: supprimer le délai de conservation de la boîte aux lettres» dans [la rubrique supprimer des éléments du dossier éléments récupérables des boîtes aux lettres en nuage](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-4-remove-the-delay-hold-from-the-mailbox) pour obtenir des instructions sur la suppression du blocage de retard placé sur la boîte aux lettres après la suppression d'un type de conservation.
    
 **Important:** Vérifiez auprès de votre gestion des enregistrements ou de vos services juridiques avant de supprimer une stratégie de conservation ou de rétention. Votre organisation peut avoir une stratégie qui détermine si une boîte aux lettres en attente ou un incident de débordement de données est prioritaire. 
  
Veillez à rétablir les configurations précédentes de la boîte aux lettres après avoir vérifié que les données déversées ont été définitivement supprimées. Consultez les détails de l' [étape 7](#step-7-permanently-delete-the-spilled-data).

## <a name="step-7-permanently-delete-the-spilled-data"></a>Étape 7: supprimer définitivement les données propagées

À l'aide des emplacements de boîte aux lettres que vous avez collectés et préparés à l'étape 6, ainsi que de la requête de recherche créée et affinée à l'étape 3 pour rechercher les messages électroniques contenant les données indésirables, vous pouvez maintenant supprimer définitivement les données propagées. Comme expliqué précédemment, vous devez disposer du rôle d'exportation d'importation de boîte aux lettres dans Exchange Online pour supprimer les messages à l'aide de la procédure suivante.
  
1. [Connectez-vous à Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).
    
2. Exécutez la commande suivante :
    
    ```
    Search-Mailbox -Identity <mailbox identity> -SearchDumpster -DeleteContent $true -SearchQuery <search query>
    ```
  
3. Réexécutez la commande précédente pour chaque boîte aux lettres qui contient les données dépropagées en remplaçant la valeur du paramètre Identity; par exemple:

    ```
    Search-Mailbox -Identity sarad@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

    ```
    Search-Mailbox -Identity janets@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
    ```

   ```
   Search-Mailbox -Identity pilarp@contoso.onmicrosoft.com -SearchQuery <search query> -DeleteContent
   ```
  
Comme indiqué précédemment, vous pouvez également créer un [script PowerShell](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6) et l'exécuter par rapport à une liste de boîtes aux lettres de sorte que le script supprime les données dépassées dans chaque boîte aux lettres.
  
## <a name="step-8-verify-provide-a-proof-of-deletion-and-audit"></a>Étape 8: vérifier, fournir une preuve de suppression et d'audit

La dernière étape du flux de travail de gestion d'un incident de fuite de données consiste à vérifier que les données déplacées ont été définitivement supprimées de la boîte aux lettres en accédant au cas eDiscovery et en réexécutant la même requête de recherche qui a été utilisée pour confirmer qu'aucun résultat n'a été obtenu. e renvoyé. Une fois que vous avez confirmé que les données déplacées ont été définitivement supprimées, vous pouvez exporter un rapport et l'inclure (en même temps que le rapport d'origine) comme preuve de suppression. Vous pouvez ensuite [Fermer le cas](ediscovery-cases.md#optional-step-9-close-a-case), ce qui vous permettra de le rouvrir si vous y faites référence à l'avenir. En outre, vous pouvez également rétablir les boîtes aux lettres à leur état précédent, supprimer la requête de recherche utilisée pour trouver les données déversées, et Rechercher des enregistrements d'audit des tâches effectuées lors de la gestion de l'incident de fuite de données. 
  
### <a name="reverting-the-mailboxes-to-their-previous-state"></a>Rétablissement des boîtes aux lettres à leur état précédent

Si vous avez modifié une configuration de boîte aux lettres à l'étape 6 afin de préparer les boîtes aux lettres avant la suppression des données déversées, vous devrez les rétablir à leur état précédent. Voir «étape 6: rétablir l'état précédent de la boîte aux lettres» dans [supprimer des éléments du dossier éléments récupérables des boîtes aux lettres en nuage](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#step-6-revert-the-mailbox-to-its-previous-state).
  
### <a name="deleting-the-search-query"></a>Suppression de la requête de recherche

Si les mots clés de la requête de recherche que vous avez créée et utilisée à l'étape 3 contiennent certaines de ces données, vous devez supprimer la requête de recherche pour éviter toute dépassements de données.
  
1. Dans le centre de sécurité & Compliance Center, ouvrez le cas eDiscovery, accédez à la page de **recherche** et sélectionnez la recherche de contenu appropriée.
    
2. Sur la page de la fenêtre volante, cliquez sur **supprimer**.

    ![Sélectionnez la recherche, puis cliquez sur supprimer sur la page de menu volant](media/O365-eDiscoverySolutions-DataSpillage-DeleteSearch.png)
    
### <a name="auditing-the-data-spillage-investigation-process"></a>Audit du processus d'enquête de fuite de données

Vous pouvez rechercher dans le journal d'audit Office 365 des activités eDiscovery effectuées pendant l'enquête. Vous pouvez également effectuer des recherches dans le journal d'audit pour renvoyer les enregistrements d'audit créés lors de l'exécution de la commande **Search-Mailbox-DeleteContent** pour supprimer les données déplacées. Pour plus d'informations, voir:

- [Effectuer des recherches dans le journal d’audit dans le Centre de sécurité et de conformité Office 365](search-the-audit-log-in-security-and-compliance.md)

- [Rechercher des activités eDiscovery dans le journal d'audit Office 365](search-for-ediscovery-activities-in-the-audit-log.md)

- Consultez la section «activités auditées-journal d'audit de l'administrateur Exchange» dans [Search the Audit Log in the Office 365 Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities) pour obtenir des instructions sur la recherche d'enregistrements d'audit liés à l'exécution des cmdlets dans Exchange Online.
  

