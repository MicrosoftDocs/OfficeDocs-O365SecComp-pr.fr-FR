---
title: Filtrer les données lors de l’importation des fichiers PST vers Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Utilisez la nouvelle fonctionnalité d’importation intelligente dans le service Office 365 importation pour filtrer les éléments qui sont réellement importées pour les boîtes aux lettres cible. Importation intelligente vous permet de décider de manière proactive les données à importer et les éléments à laisser. Importation intelligente fournit également insights sur les données que vous importez vers Office 365. '
ms.openlocfilehash: 723a2e05a1f5d256e99bcf8497643435d0c98a23
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527513"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a>Filtrer les données lors de l’importation des fichiers PST vers Office 365

Utilisez la nouvelle fonctionnalité d’importation intelligente dans le service Office 365 importation pour filtrer les éléments dans les fichiers PST sont réellement importées pour les boîtes aux lettres cible. Voici comment cela fonctionne :
  
- Après avoir créé et soumettre une tâche d’importation PST, fichiers PST sont téléchargés vers une zone de stockage Azure dans le nuage de Microsoft.
    
- Office 365 analyse les données dans les fichiers PST, de manière sécurisée, en identifiant l’âge des types de message différent dans les fichiers PST et les éléments de boîte aux lettres.
    
- Lorsque l’analyse est terminée et que les données sont prêtes à importer, vous avez la possibilité d’importer toutes les données dans les fichiers PST ou supprimer les données importées en définissant des filtres qui déterminent quelles données obtient importées. Par exemple, vous pouvez soit :
    
  - Importer uniquement les éléments d’un certain âge.
    
  - Importer les types de message sélectionné.
    
  - Exclure les messages envoyés ou reçus par des personnes spécifiques.
    
- Après avoir configuré les paramètres de filtre, Office 365 importe uniquement les données qui répond aux critères de filtrage pour les boîtes aux lettres cible spécifiées dans la tâche d’importation.
    
Le graphique suivant illustre le processus d’importation Intelligent et met en évidence les tâches et les tâches effectuées par Office 365.
  
![Le processus d’importation Intelligent dans Office 365](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a>Avant de commencer

- Les étapes décrites dans cette rubrique supposent que vous avez créé une tâche d’importation PST dans le service Office 365 importer à l’aide de téléchargement de réseau ou de l’expédition du lecteur. Pour obtenir des instructions détaillées, consultez les rubriques suivantes :
    
  - [Utiliser le chargement réseau pour importer des fichiers PST vers Office 365](use-network-upload-to-import-pst-files.md)
    
  - [Utiliser l’expédition de disque pour importer des fichiers PST dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- Après avoir créé une tâche d’importation à l’aide de téléchargement du réseau, l’état de la tâche d’importation de l’importation de page de la sécurité Office 365 &amp; centre de conformité est définie à l' **analyse en cours**, ce qui signifie que Office 365 analyse les données dans les fichiers PST que vous téléchargé. Cliquez sur **Actualiser**![Actualiser](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) pour mettre à jour l’état de la tâche d’importation. 
    
- Lecteur de livraison des tâches d’importation, les données sont analysées par Office 365 après le personnel du centre de données Microsoft recevoir de votre disque dur et télécharger les fichiers PST vers la zone de stockage Azure pour votre organisation.
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a>Filtrer les données qui obtient importées dans des boîtes aux lettres

Une fois que vous avez créé un fichier PST importer le travail, suivez ces étapes pour filtrer les données avant de les importer vers Office 365.
  
1. Accédez à [https://protection.office.com/](https://protection.office.com/) et connectez-vous en utilisant les informations d’identification pour un compte d’administrateur de votre organisation Office 365. 
    
2. Dans le volet gauche de sécurité Office 365 &amp; centre de conformité, cliquez sur **la gouvernance des données** \> **Import**.
    
    Les travaux de l’importation de votre organisation sont répertoriés dans la page **Importer** . Notez que la valeur de **l’analyse terminée** , dans la colonne **état** indique les travaux d’importation qui ont été analysés par Office 365 et sont prêts à importer. 
    
    ![État d’analyse complète indique à Qu'office 365 a analysé les données dans des fichiers PST](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. Cliquez sur **prêt à importer dans Office 365** pour le travail d’importation que vous souhaitez effectuer. 
    
    Une page brusque s’affiche avec des informations sur les fichiers PST et autres informations sur la tâche d’importation.
    
4. Cliquez sur **Importer vers Office 365**.
    
    La page **Filtrer vos données** s’affiche. Il contient des détails de données sur les données dans les fichiers PST pour la tâche d’importation, notamment des informations sur l’âge des données. 
    
    ![Le filtre votre page données affiche les détails de données des fichiers PST de la tâche d’importation](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. Selon si vous souhaitez supprimer les données importées vers Office 365, sous **vous souhaitez filtrer vos données ?**, effectuez l’une des opérations suivantes :
    
    a. Cliquez sur **Oui, je veux filtrer avant l’importation** pour ajuster les données que vous importez, puis cliquez sur **suivant**.
    
    La page **Importer des données dans Office 365 page** s’affiche avec les détails des données détaillées de l’analyse effectuée Office 365. 
    
    ![Office 365 affiche les détails des données détaillées à partir de son analyse des fichiers PST](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    Le graphique sur cette page indique la quantité de données qui seront importées. Plus d’informations sur chaque type de message dans les fichiers PST sont affichés dans le graphique. Vous pouvez pointer le curseur sur chaque barre pour afficher des informations spécifiques sur ce type de message. Il existe également une liste déroulante avec les valeurs d’âge différentes en fonction de l’analyse des fichiers PST. Lorsque vous sélectionnez un âge dans la liste déroulante, le graphique est mis à jour pour afficher la quantité de données est importée pour l’âge sélectionné. 
    
    b. pour configurer des filtres de plus pour réduire la quantité de données qui sont importées, cliquez sur **plus d’options de filtrage**.
    
    ![Configurer les filtres dans la page options plus pour ajuster les données importées](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    Vous pouvez configurer ces filtres :
    
      - **Âge** - sélectionner un âge afin que seuls les éléments qui sont plus récents que l’âge spécifié sera importé. Voir la section [plus d’informations](filter-data-when-importing-pst-files.md#moreinfo) pour une description expliquant comment Office 365 détermine l’âge des compartiments pour le filtre **d’âge** . 
    
      - **Type** : cette section montre tous les types de message qui ont été détectés dans les fichiers PST pour la tâche d’importation. Vous pouvez désactiver une case en regard d’un type de message que vous souhaitez exclure. Notez que vous ne peut pas exclure de l’autre type de message. Voir la section [plus d’informations](filter-data-when-importing-pst-files.md#moreinfo) pour une liste d’éléments de boîte aux lettres qui sont inclus dans l’autre catégorie. 
    
      - **Utilisateurs** : vous pouvez exclure des messages envoyés ou reçus par des personnes spécifiques. Pour exclure les personnes qui figurent dans le champ : champ à : field ou Cc : champ des messages, cliquez sur **Exclure les utilisateurs** en regard de ce type de destinataire. Tapez l’adresse de messagerie (adresse SMTP) de la personne, cliquez sur **Ajouter**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) pour les ajouter à la liste des utilisateurs exclus pour ce type de destinataire, puis cliquez sur **Enregistrer** pour enregistrer la liste des utilisateurs exclus. 
    
        > [!NOTE]
        > Office 365 n’affiche pas les détails de données qui résultent de la définition du filtre de **personnes** . Toutefois, si vous définissez ce filtre pour exclure les messages envoyés ou reçus par des personnes spécifiques, ces messages seront exclus pendant le processus d’importation. 
  
    c. Cliquez sur **Appliquer** dans le **options de filtrage plus** brusque page pour enregistrer vos paramètres de filtrage. 
    
    Les données insights dans la page **Importer des données dans Office 365** sont mis à jour en fonction de vos paramètres de filtrage, y compris la quantité totale de données qui seront importées en fonction des paramètres de filtre. Notez qu’un résumé des paramètres du filtre s’affiche également. Vous pouvez cliquer sur **Modifier** en regard d’un filtre pour modifier le paramètre si nécessaire. 
    
    ![Les analyses de données sont mises à jour en fonction de vos paramètres de filtrage](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    d. Cliquez sur **suivant**.
    
    Une page d’état affiche les paramètres de filtre. Encore une fois, vous pouvez modifier les paramètres de filtre.
    
    e. Cliquez sur **Importer des données** pour démarrer l’importation. Notez que la quantité totale de données qui seront importées est affichée. 
    
    Ou
    
    a. Cliquez sur **non, je souhaite tout importer** pour importer toutes les données dans les fichiers PST vers Office 365, puis cliquez sur **suivant**.
    
    b. dans la page **Importer des données à Office 365** , cliquez sur **Importer des données** pour démarrer l’importation. Notez que la quantité totale de données qui seront importées est affichée. 
    
6. Dans la page **Importer** , cliquez sur **Actualiser** ![Actualiser](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). L’état de la tâche d’importation est affiché dans la colonne **état** . 
    
7. Cliquez sur l’importation de la tâche pour afficher des informations plus détaillées, telles que l’état de chaque fichier PST et les paramètres de filtre que vous avez configuré.

  
## <a name="more-information"></a>Plus d'informations

- Comment Office 365 détermine-t-il les incréments pour le filtre d’âge ? Lorsque Office 365 analyse un fichier PST, il se présente au niveau de l’horodatage envoyé ou reçu de chaque élément (si un élément a un horodatage envoyé et reçu, la date la plus ancienne est activée). Office 365 ressemble à la valeur de l’année pour cette valeur, puis il compare la date actuelle pour déterminer l’âge de l’élément. Ces qui est ensuite utilisés comme valeurs dans la liste déroulante pour le filtre **d’âge** . Par exemple, si un fichier PST comporte des messages à partir de 2016, 2015 et 2014, des valeurs dans le filtre **d’âge** serait **année 1**, **2 ans**et **3 ans**.
    
- Le tableau suivant répertorie les types de messages qui sont inclus dans **l’autre** catégorie dans le **Type** de filtre à la volée **d’autres options** de page (voir l’étape 5 b dans la procédure précédente). Actuellement, vous ne pouvez pas exclure les éléments dans la catégorie « Autre » lorsque vous importez des fichiers pst vers Office 365. 
    
    |**ID de classe de message**|**Éléments de boîte aux lettres qui utilisent cette classe de message**|
    |:-----|:-----|
    |IPM. Activité  <br/> |Entrées de journal  <br/> |
    |IPM. Document  <br/> |Documents et les fichiers (ne pas joints à un message électronique)  <br/> |
    |IPM. Fichier  <br/> |(les mêmes que IPM. Document)  <br/> |
    |IPM. Note.IMC.Notification  <br/> |Rapports envoyés par Internet Mail Connect, qui est la passerelle Exchange Server vers Internet  <br/> |
    |IPM. Note.Microsoft.Fax  <br/> |Messages de télécopie  <br/> |
    |IPM. Note.Rules.Oof.Template.Microsoft  <br/> |Messages d’absence de réponse automatique  <br/> |
    |IPM. Note.Rules.ReplyTemplate.Microsoft  <br/> |Réponses envoyées par une règle de boîte de réception  <br/> |
    |IPM. OLE. Classe  <br/> |Exceptions d’une série périodique  <br/> |
    |IPM. Recall.Report  <br/> |Rapports de rappel de message  <br/> |
    |IPM. À distance  <br/> |Messages de courrier à distance  <br/> |
    |IPM. Rapport  <br/> |Élément rapports d’état  <br/> |
