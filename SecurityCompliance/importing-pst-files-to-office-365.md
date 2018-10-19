---
title: Overview of importing your organization PST files to Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.IngestionHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: 'Pour les administrateurs : en savoir plus sur l’utilisation du service d’importation de sécurité Office 365 &amp; centre de conformité pour l’importation de données de messagerie (fichiers PST) pour les boîtes aux lettres dans Exchange Online. Cette rubrique fournit des questions fréquentes et explique comment fonctionne le processus d’importation PST.'
ms.openlocfilehash: 3a6c3db966513be5c63588dac75643ffc1962323
ms.sourcegitcommit: 8294182d4dd124f035a221de0b90159ef7eec4ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "25639673"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a>Overview of importing your organization PST files to Office 365

> [!NOTE]
> Cet article est destiné aux administrateurs. Vous essayez d’importer des fichiers PST à votre propre boîte aux lettres ? Voir [messagerie importation, contacts et calendrier à partir d’un fichier Outlook .pst](https://go.microsoft.com/fwlink/p/?LinkID=785075)

Vous pouvez utiliser le service d’importation de sécurité Office 365 &amp; centre de conformité à PST rapidement en bloc-importer les fichiers aux boîtes aux lettres Exchange Online dans votre organisation Office 365. Il existe deux méthodes que vous pouvez importer des fichiers PST vers Office 365 :
   
- **Téléchargement du réseau** ![Téléchargement nuage](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) -télécharger les fichiers PST sur le réseau vers un emplacement de stockage Azure temporaire dans le nuage de Microsoft. Ensuite, vous utilisez le service Office 365 importer pour importer les données PST aux boîtes aux lettres dans votre organisation Office 365. 

- **Lecteur de livraison** ![Disque dur](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) - copiez les fichiers PST sur un disque dur chiffré BitLocker et puis livrées physiquement le lecteur à Microsoft. Lorsque Microsoft reçoit le disque dur, le personnel du centre de données télécharger les données vers un emplacement de stockage Azure temporaire dans le nuage de Microsoft. Ensuite, vous utilisez le service Office 365 importer pour importer les données aux boîtes aux lettres dans votre organisation Office 365.

## <a name="step-by-step-instructions"></a>Instructions pas à pas
  
Consultez les rubriques suivantes pour obtenir des instructions pas à pas pour l’importation en bloc des fichiers PST de votre organisation vers Office 365. 
   
- [Utiliser le chargement réseau pour importer des fichiers PST vers Office 365](use-network-upload-to-import-pst-files.md)
- [Utiliser l’expédition de disque pour importer des fichiers PST dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>Fonctionne de l’importation des fichiers PST

Voici une illustration et une description du processus d’importation PST terminée. L’illustration montre le flux de travail principal et met en évidence les différences entre le téléchargement de réseau et le lecteur de modes de livraison.
  
![Flux de travail de processus d’importation PST](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **Télécharger le fichier PST importer les outils et l’emplacement de stockage Azure clé Private** - la première étape consiste à télécharger la clé de l’outil et d’accès utilisée pour télécharger les fichiers PST ou de les copier dans un disque dur. Vous obtenez à partir de la page **Importer** de sécurité Office 365 &amp; centre de conformité. La clé fournit vous (ou personnel du centre de données Microsoft dans le cas d’expédition du lecteur) avec les autorisations nécessaires pour télécharger des fichiers PST vers un emplacement de stockage Azure privé et sécurisé. Cette clé d’accès est unique à votre organisation et permet d’empêcher tout accès non autorisé à vos fichiers PST après leur téléchargement vers le nuage Microsoft. Notez que l’importation de fichiers PST vers Office 365 ne nécessite pas votre organisation à un abonnement Azure distinct. 
    
2. **Télécharger ou copier le fichier PST des fichiers** - l’étape suivante dépend de si vous utilisez téléchargement réseau ou l’expédition du lecteur pour importer des fichiers PST. Dans les deux cas, vous allez utiliser l’outil et la clé de stockage sécurisé que vous avez obtenu à l’étape précédente.
    
    - **Téléchargement du réseau** L’outil AzCopy.exe (téléchargé à l’étape 1) est utilisé pour transférer et stocker vos fichiers PST dans un emplacement de stockage Azure dans le nuage de Microsoft. Notez que l’emplacement de stockage Azure que vous téléchargez vos fichiers PST réside dans le même Microsoft Centre de données régional où se trouve votre organisation Office 365. 
    
      Pour les télécharger, les fichiers PST que vous souhaitez importer vers Office 365 doivent se trouver dans un partage de fichiers ou un serveur de fichiers dans votre organisation.
    
    - **Lecteur de livraison** L’outil WAImportExport.exe (téléchargé à l’étape 1) est utilisé pour copier les fichiers PST sur le disque dur. Cet outil chiffre le disque dur avec BitLocker, puis copie les fichiers pst sur le disque dur. Comme le téléchargement du réseau, les fichiers PST que vous souhaitez copier sur le disque dur n’ont doit être situé dans un partage de fichiers ou un serveur de fichiers dans votre organisation.
    
3. **Créer un fichier de mappage d’importation PST** - une fois que les fichiers PST ont été téléchargés vers l’emplacement de stockage Azure ou copiés sur un disque dur, l’étape suivante consiste à créer un fichier de valeurs séparées (CSV) qui spécifie les fichiers de boîtes aux lettres le fichier PST utilisateur seront importées à (a ND un fichier PST peut être importé dans leur boîte aux lettres d’archivage ou de boîte aux lettres principale d’un utilisateur). Le service Office 365 importer utilisera les informations à importer les fichiers PST. 
    
4. **Tâche d’importation de créer un fichier PST** - l’étape suivante consiste à créer une tâche d’importation PST dans la page **Importer** dans la sécurité &amp; centre de conformité et soumettre le fichier de mappage d’importation PST créé à l’étape précédente. Pour le téléchargement du réseau (étant donné que les fichiers PST ont été téléchargés vers Azure) Office 365 analyse les données dans les fichiers PST et vous donne la possibilité de définir des filtres qui déterminent quelles données obtient réellement importées pour les boîtes aux lettres spécifiés dans le fichier de mappage d’importation PST. 
    
    Pour l’envoi de lecteur, quelques opérations supplémentaires ont lieu à ce stade du processus.
    
    - Vous livrez physiquement le disque dur pour un centre de données (l’adresse d’expédition pour le centre de données Microsoft s’affiche lors de la création de la tâche d’importation)
    
    - Lorsque Microsoft reçoit le disque dur, personnel du centre de données pour télécharger les fichiers pst sur le disque dur à l’emplacement de stockage Azure pour votre organisation. Comme expliqué précédemment, les fichiers PST sont téléchargés vers un emplacement de stockage Azure qui réside dans le même centre de données Microsoft régional où se trouve votre organisation Office 365.
    
      > [!NOTE]
      > Les fichiers PST sur le disque dur sont téléchargés vers Azure dans 7 à 10 jours après que Microsoft a reçu le disque dur. 
  
      Comme le processus de téléchargement réseau, Office 365 analyse les données dans les fichiers PST et vous donne la possibilité de définir des filtres qui déterminent quelles données obtient réellement importées pour les boîtes aux lettres spécifiés dans le fichier de mappage d’importation PST.
    
    - Le disque dur vous de Microsoft est fourni. 
    
5. **Filtre les données PST qui seront importées dans des boîtes aux lettres** - après la tâche d’importation est créée (et les fichiers PST à partir d’une tâche de livraison lecteur sont téléchargées vers l’emplacement de stockage Azure) Office 365 analyse les données dans les fichiers PST (en toute sécurité) par identification de l’âge des éléments et les différents types de messages inclus dans les fichiers PST. Lorsque l’analyse est terminée et que les données sont prêtes à importer, vous avez la possibilité d’importer toutes les données contenues dans les fichiers PST, ou vous pouvez ajuster les données importées en définissant des filtres qui déterminent quelles données obtient importées. 
    
6. **Démarrer le travail d’importation PST** - après le démarrage de la tâche d’importation, Office 365 utilise les informations dans le fichier de mappage d’importation PST pour importer les fichiers PST à partir de l’emplacement de stockage Azure annuel aux boîtes aux lettres de l’utilisateur. Informations de statut de la tâche d’importation (y compris les informations sur chaque fichier PST à importer) s’affiche dans la page **Importer** dans la sécurité &amp; centre de conformité. Lorsque la tâche d’importation est terminée, le statut de la tâche est défini sur **terminé**.
  
## <a name="why-import-email-data-to-office-365"></a>Pourquoi importer des données de messagerie vers Office 365 ?

- Importation des fichiers PST dans les boîtes aux lettres est un moyen de migration de messagerie de votre organisation vers Office 365.
    
- Vous pouvez utiliser la fonctionnalité [d’Importation Intelligent](filter-data-when-importing-pst-files.md) pour filtrer les éléments dans les fichiers PST sont réellement importées pour les boîtes aux lettres cible. Ce vous ajustez les données importées en définissant des filtres qui vous permet de contrôle les données sont importées. 
    
- Importation de données de messagerie vers Office 365 vous aide à gérer les besoins de conformité de votre organisation en vous permettant de :
    
  - Activer des [boîtes aux lettres d’archivage](enable-archive-mailboxes.md) et [l’archivage illimité](unlimited-archiving.md) pour permettre aux utilisateurs d’espace de stockage de boîtes aux lettres supplémentaires. 
    
  - Placer les boîtes aux lettres en [Attente pour litige](https://go.microsoft.com/fwlink/?linkid=841243) pour conserver le contenu. 
    
  - Utiliser l' [outil de recherche de contenu de](content-search.md) recherche de contenu de la boîte aux lettres. 
    
  - Utiliser des [cas eDiscovery](ediscovery-cases.md) pour gérer les enquêtes légales de votre organisation 
    
  - Utiliser des [stratégies de rétention](retention-policies.md) dans la sécurité &amp; centre de conformité pour contrôler la durée de conservation de contenu de la boîte aux lettres, puis supprimer le contenu après expiration de la période de rétention. 
    
- Importation de données dans Office 365, vous aide à protéger contre la perte de données. Données de messagerie qui sont importées dans Office 365 hérite les fonctionnalités de haute disponibilité d’Exchange Online.
    
- Données de messagerie dans Office 365 sont accessibles aux utilisateurs de tous les périphériques, car il est stocké dans le nuage.
    
## <a name="importing-sharepoint-data-to-office-365"></a>Importation de données SharePoint dans Office 365

Vous pouvez également importer des fichiers et des documents à des sites SharePoint et les comptes de OneDrive dans votre organisation Office 365. Pour plus d’informations, voir les articles suivants :

- [Migrer vers SharePoint Online](https://docs.microsoft.com/sharepointmigration/migrate-to-sharepoint-online)

- [Présentation de l’outil de migration SharePoint](https://docs.microsoft.com/sharepointmigration/introducing-the-sharepoint-migration-tool)

- [Migrer vers SharePoint Online à l’aide de PowerShell](https://docs.microsoft.com/sharepointmigration/overview-spmt-ps-cmdlets)

- [Migrer votre contenu de partage de fichiers vers SharePoint Online à l’aide de la zone de données Azure](https://docs.microsoft.com/sharepointmigration/how-to-migrate-file-share-content-to-spo-using-azuredatabox)


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a>Forum aux questions sur l’importation de fichiers PST vers Office 365
  
Voici quelques questions fréquemment posées sur l’utilisation du service Office 365 importer pour l’importation en bloc des fichiers PST aux boîtes aux lettres Office 365. 
  
- [À l’aide de téléchargement réseau pour importer des fichiers PST](#using-network-upload-to-import-pst-files)
  
- [À l’aide de livraison de lecteur pour importer des fichiers PST](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a>À l’aide de téléchargement réseau pour importer des fichiers PST

 **Quelles sont les autorisations nécessaires pour créer des tâches d’importation dans le Service d’importation Office 365 ?**
  
Vous devez être le rôle importer exporter des boîtes aux lettres dans Exchange Online pour importer des fichiers PST aux boîtes aux lettres Office 365. Par défaut, ce rôle n’est pas affecté à un groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle de boîte aux lettres importer exporter au groupe de rôles de gestion de l’organisation. Ou vous pouvez créer un nouveau groupe de rôles, attribuer le rôle de boîte aux lettres importer exporter et puis ajouter d’autres utilisateurs en tant que membre. Pour plus d’informations, voir le « ajouter un rôle à un groupe de rôles » ou la « créer un groupe de rôles » sections du [rôle de gérer les groupes dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
En outre, pour créer l’importation des travaux de sécurité Office 365 &amp; centre de conformité, une des opérations suivantes doivent être remplie :
  
- Vous devez être affecté le rôle destinataires de messagerie dans Exchange Online. Par défaut, ce rôle est attribué aux groupes de rôles de gestion de l’organisation et la gestion des destinataires.
    
    Ou
    
- Vous devez être un administrateur global dans votre organisation Office 365.
    
> [!TIP]
> Envisagez de créer un nouveau groupe de rôles dans Exchange Online est spécifiquement conçu pour l’importation des fichiers PST vers Office 365. Pour le niveau minimal de privilèges nécessaires pour importer des fichiers PST, attribuer les rôles destinataires de messagerie et de boîte aux lettres importer exporter vers le nouveau groupe de rôles et ajouter des membres. 
  
 **Où le téléchargement du réseau est disponible ?**
  
Téléchargement du réseau est actuellement disponible dans les États-Unis, Canada, Brésil, le Royaume-Uni, pour l’Europe, Inde, Asie de l’est, Asie du Sud-est, Japon, République de Corée et Australie. Téléchargement du réseau sera disponible dans plusieurs régions bientôt.
  
 **Quel est le prix d’importation des fichiers PST à l’aide de téléchargement du réseau ?**
  
À l’aide de téléchargement réseau pour importer des fichiers PST est gratuite.
  
Cela signifie également que, une fois que les fichiers PST sont supprimés de la zone de stockage Azure, qu’ils sont affichés n’est plus dans la liste des fichiers d’un travail d’importation dans le centre d’administration d’Office 365. Bien qu’une tâche d’importation peut toujours être répertoriée dans la page **Importer des données à Office 365** , la liste des fichiers PST peut être vide lorsque vous affichez les détails des anciens travaux d’importation. 
  
 **Quelle version du format de fichier PST est pris en charge pour l’importation vers Office 365 ?**
  
Il existe deux versions du format de fichier PST : ANSI et Unicode. Nous vous recommandons d’importer les fichiers qui utilisent le format de fichier Unicode PST. Toutefois, les fichiers qui utilisent le format de fichier PST ANSI, telles que celles pour les langues qui utilisent un caractère codé sur deux octets (DBCS) set, peuvent également être importées vers Office 365. Pour plus d’informations sur l’importation des fichiers PST ANSI, voir l’étape 4 dans [utiliser le réseau télécharger pour importer des fichiers PST vers Office 365](https://go.microsoft.com/fwlink/p/?LinkId=823074).
  
En outre, les fichiers PST d’Outlook 2007 et versions ultérieures peuvent être importés dans Office 365.
  
 **Une fois dans la zone de stockage Azure télécharger mes fichiers PST, combien de temps ils restent dans Azure avant qu’ils sont supprimées ?**
  
Lorsque vous utilisez la méthode de téléchargement du réseau pour importer des fichiers PST, téléchargez-les à un conteneur d’objets blob Azure nommé **ingestiondata**. S’il existe des tâches d’importation en cours dans la page **Importer** dans la sécurité &amp; centre de conformité), puis tous les fichiers PST dans le conteneur **ingestiondata** Azure sont supprimés de 30 jours après la dernière tâche d’importation a été créée dans la sécurité &amp;Centre de conformité. Cela signifie également que vous devez créer une nouvelle tâche d’importation de la sécurité &amp; fichiers de centre de conformité (décrit à l’étape 5 dans les instructions de téléchargement réseau) dans les 30 jours de téléchargement PST sur Azure. 
  
Cela signifie également que, une fois que les fichiers PST sont supprimés de la zone de stockage Azure, qu’ils sont affichés n’est plus dans la liste des fichiers d’un travail d’importation de la sécurité &amp; centre de conformité. Bien qu’une tâche d’importation peut toujours être répertoriée dans la page **Importer** dans la sécurité &amp; centre de conformité, la liste des fichiers PST peut être vide lorsque vous affichez les détails des anciens travaux d’importation. 
  
 **Combien de temps faut-il pour importer un fichier PST dans une boîte aux lettres ?**
  
Cela dépend de la capacité de votre réseau, mais il est généralement plusieurs heures pour chaque téraoctet (To) de données d’être téléchargés depuis la zone de stockage Azure pour votre organisation. Une fois que les fichiers PST sont copiés dans la zone de stockage Azure, un fichier PST est importé dans une boîte aux lettres Office 365 à un taux d’au moins 24 Go par jour. Si cette fréquence ne répond pas à vos besoins, vous pouvez envisager d’autres méthodes de migration de données de messagerie vers Office 365. Pour plus d’informations, voir [comment migrer plusieurs comptes de messagerie vers Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Si différents fichiers PST sont importées dans les boîtes aux lettres cible différent, le processus d’importation se produit en parallèle ; en d’autres termes, chaque paire de PST/boîte aux lettres est importée simultanément. De même, si plusieurs fichiers PST sont importées dans la même boîte aux lettres, ils seront importées simultanément.
  
 **Existe-t-il une limite de taille de message lors de l’importation des fichiers PST ?**
  
Oui. Si un fichier PST contient un élément de boîte aux lettres est supérieur à 150 Mo, l’élément sera ignoré pendant le processus d’importation.
  
 **Sont les propriétés de message, tel que lorsque le message a été envoyé ou reçu, la liste des destinataires et d’autres propriétés, conservées lorsque les fichiers PST sont importées dans une boîte aux lettres Office 365 ?**
  
Oui. Les métadonnées de message d’origine n’est pas modifiée pendant le processus d’importation.
  
 **Y a-t-il une limite au nombre de niveaux dans une hiérarchie de dossiers d’un fichier PST que vous voulez importer dans une boîte aux lettres ?**
  
Oui. Vous ne pouvez pas importer un fichier PST qui possède au moins 300 niveaux de dossiers imbriqués.
  
 **Puis-je utiliser le téléchargement du réseau pour importer des fichiers PST vers une boîte aux lettres inactive dans Office 365 ?**
  
Oui, cette fonctionnalité est maintenant disponible.
  
 **Puis-je utiliser le téléchargement réseau pour importer des fichiers PST vers une boîte aux lettres d’archive en ligne dans un déploiement Exchange hybride ?**
  
Oui, cette fonctionnalité est maintenant disponible.
  
 **Puis-je utiliser le téléchargement du réseau pour importer des fichiers PST aux dossiers publics dans Exchange Online ?**
  
Non, vous ne pouvez pas importer les fichiers PST aux dossiers publics.
  
### <a name="using-drive-shipping-to-import-pst-files"></a>À l’aide de livraison de lecteur pour importer des fichiers PST

 **Quelles sont les autorisations nécessaires pour créer des tâches d’importation dans le Service d’importation Office 365 ?**
  
Vous devez attribuer le rôle de boîte aux lettres importer exporter pour importer des fichiers PST aux boîtes aux lettres Office 365. Par défaut, ce rôle n’est pas affecté à un groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle de boîte aux lettres importer exporter au groupe de rôles de gestion de l’organisation. Ou vous pouvez créer un nouveau groupe de rôles, attribuer le rôle de boîte aux lettres importer exporter et puis ajouter d’autres utilisateurs en tant que membre. Pour plus d’informations, voir le « ajouter un rôle à un groupe de rôles » ou la « créer un groupe de rôles » sections du [rôle de gérer les groupes dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
En outre, pour créer l’importation des travaux de sécurité Office 365 &amp; centre de conformité, une des opérations suivantes doivent être remplie :
  
- Vous devez être affecté le rôle destinataires de messagerie dans Exchange Online. Par défaut, ce rôle est attribué aux groupes de rôles de gestion de l’organisation et la gestion des destinataires.
    
    Ou
    
- Vous devez être un administrateur global dans votre organisation Office 365.
    
> [!TIP]
> Envisagez de créer un nouveau groupe de rôles dans Exchange Online est spécifiquement conçu pour l’importation des fichiers PST vers Office 365. Pour le niveau minimal de privilèges nécessaires pour importer des fichiers PST, attribuer les rôles destinataires de messagerie et de boîte aux lettres importer exporter vers le nouveau groupe de rôles et ajouter des membres. 
  
 **Où lecteur est commercialisé disponible ?**
  
Lecteur de livraison est actuellement disponible dans les États-Unis, Canada, Brésil, le Royaume-Uni, pour l’Europe, Inde, Asie de l’est, Asie du Sud-est, Japon, République de Corée et Australie. Lecteur de livraison sera disponible dans plusieurs régions bientôt.
  
 **Les contrats de licence commerciaux prennent en charge la livraison de lecteur ?**
  
Lecteur de transaction pour importer des fichiers PST vers Office 365 est disponible via un Microsoft Enterprise accord. Lecteur de livraison n’est pas disponible par le biais de Microsoft Products Services contrat (MPSA).
  
 **Quel est le prix pour l’utilisation du lecteur d’expédition pour importer des fichiers PST vers Office 365 ?**
  
Le coût de livraison de lecteur permet d’importer des fichiers PST aux boîtes aux lettres Office 365 est 2 dollars par Go de données. Par exemple, si vous livrez un disque dur qui contient les 1 000 Go (1 To) des fichiers PST, le coût est de 2 000 dollars. Vous pouvez travailler avec un partenaire pour régler les frais d’importation. Pour plus d’informations sur la recherche d’un partenaire, voir [Rechercher votre partenaire Office 365 ou un revendeur](https://go.microsoft.com/fwlink/p/?LinkId=785197).
  
 **Quels types de disques durs sont prises en charge pour l’envoi du lecteur ?**
  
Uniquement de 2,5 pouces à semi-conducteurs (SSD) des lecteurs ou 2,5 ou 3,5 pouces SATA II/III des disques durs internes sont prises en charge pour une utilisation avec le service Office 365 importation. Vous pouvez utiliser des disques durs jusqu'à 10 To. Pour les tâches d’importation, est traité uniquement le premier volume de données sur le disque dur. Le volume de données doit être au format NTFS. Lors de la copie des données sur un disque dur, vous pouvez joindre directement à l’aide d’un 2,5 pouces SSD 2,5 ou 3,5 pouces connecteur SATA II/III ou vous pouvez joindre en externe à l’aide d’un 2,5 pouces SSD externe ou 2,5 ou 3,5 adaptateur SATA II/III USB de pouce.
  
> [!IMPORTANT]
> Les disques durs externes qui sont fournis avec un adaptateur USB intégré ne sont pas pris en charge par le service Office 365 importation. En outre, le disque à l’intérieur de la casse d’un disque dur externe ne peut pas être utilisé. Veuillez ne pas envoyer des disques durs externes. 
  
 **Nombre de disques durs puis-je livrées pour une tâche d’importation unique ?**
  
Vous pouvez livrer un maximum de 10 disques durs pour une tâche d’importation unique.
  
 **Une fois que j’ai expédier mon disque dur, combien de temps faut-il pour atteindre le centre de données Microsoft ?**
  
Cela dépend de plusieurs éléments, tels que votre proximité du centre de données Microsoft et quel type d’option de livraison que vous avez utilisé pour envoyer votre disque dur (par exemple, livraison le jour suivant, deux jours ou sol-). Avec la plupart des expéditeurs, vous pouvez utiliser le numéro de suivi pour suivre l’état de votre remise.
  
 **Une fois que votre disque dur arrive dans le centre de données Microsoft, combien de temps faut-il pour télécharger mes fichiers PST vers Azure ?**
  
Une fois que votre disque dur est reçu sur le centre de données Microsoft, il faudra entre 7 à 10 jours pour télécharger les fichiers PST vers la zone de stockage Microsoft Azure pour votre organisation. Les fichiers PST seront téléchargés à un conteneur d’objets blob Azure nommé `ingestiondata`. 
  
 **Combien de temps faut-il pour importer un fichier PST dans une boîte aux lettres ?**
  
Une fois que les fichiers PST sont téléchargés vers la zone de stockage Azure, Office 365 analyse les données dans les fichiers PST (de façon sécurisée) pour identifier l’âge des éléments et les différents types de messages inclus dans les fichiers PST. Lorsque cette analyse est terminée, vous aurez la possibilité d’importer toutes les données dans les fichiers PST ou définir les filtres qui contrôlent les données obtient importées. Après le démarrage de la tâche d’importation, un fichier PST est importé dans une boîte aux lettres Office 365 à un taux d’au moins 24 Go par jour. Si cette fréquence ne répond pas à vos besoins, vous pouvez envisager d’autres méthodes pour l’importation de données de messagerie vers Office 365. Pour plus d’informations, voir [comment migrer plusieurs comptes de messagerie vers Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Si différents fichiers PST sont importées dans les boîtes aux lettres cible différent, le processus d’importation se produit en parallèle ; en d’autres termes, chaque paire de PST/boîte aux lettres est importée simultanément. De même, si plusieurs fichiers PST sont importées dans la même boîte aux lettres, ils seront importées simultanément.
  
 **Une fois que Microsoft télécharge mes fichiers PST dans Azure, combien de temps ils restent dans Azure avant qu’ils sont supprimées ?**
  
Tous les fichiers PST dans l’emplacement de stockage Azure pour votre organisation (dans le conteneur d’objets blob nommé `ingestiondata`), sont supprimés de 30 jours après la dernière tâche d’importation a été créée dans la page **Importer** dans la sécurité &amp; centre de conformité. 
  
Cela signifie également que, une fois que les fichiers PST sont supprimés de la zone de stockage Azure, qu’ils sont affichés n’est plus dans la liste des fichiers d’un travail d’importation de la sécurité &amp; centre de conformité. Bien qu’une tâche d’importation peut toujours être répertoriée dans la page **Importer** dans la sécurité &amp; centre de conformité, la liste des fichiers PST peut être vide lorsque vous affichez les détails des anciens travaux d’importation. 
  
 **Quelle version du format de fichier PST est pris en charge pour l’importation vers Office 365 ?**
  
Il existe deux versions du format de fichier PST : ANSI et Unicode. Nous vous recommandons d’importer les fichiers qui utilisent le format de fichier Unicode PST. Toutefois, les fichiers qui utilisent le format de fichier PST ANSI, telles que celles pour les langues qui utilisent un caractère codé sur deux octets (DBCS) set, peuvent également être importées vers Office 365. Pour plus d’informations sur l’importation des fichiers PST ANSI, voir l’étape 3 dans le [lecteur de transaction pour importer des fichiers de votre organisation PST vers Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
En outre, les fichiers PST d’Outlook 2007 et versions ultérieures peuvent être importés dans Office 365.
  
 **Existe-t-il une limite de taille de message lors de l’importation des fichiers PST ?**
  
Oui. Si un fichier PST contient un élément de boîte aux lettres est supérieur à 150 Mo, l’élément sera ignoré pendant le processus d’importation.
  
 **Sont les propriétés de message, tel que lorsque le message a été envoyé ou reçu, la liste des destinataires et d’autres propriétés, conservées lorsque les fichiers PST sont importées dans une boîte aux lettres Office 365 ?**
  
Oui. Les métadonnées de message d’origine n’est pas modifiée pendant le processus d’importation
  
 **Y a-t-il une limite au nombre de niveaux dans une hiérarchie de dossiers d’un fichier PST que vous voulez importer dans une boîte aux lettres ?**
  
Oui. Vous ne pouvez pas importer un fichier PST qui possède au moins 300 niveaux de dossiers imbriqués.
  
 **Puis-je utiliser expédition lecteur pour importer des fichiers PST vers une boîte aux lettres inactive dans Office 365 ?**
  
Oui, cette fonctionnalité est maintenant disponible.
  
 **Puis-je utiliser expédition lecteur pour importer des fichiers PST vers une boîte aux lettres d’archive en ligne dans un déploiement Exchange hybride ?**
  
Oui, cette fonctionnalité est maintenant disponible.
  
 **Puis-je utiliser expédition lecteur pour importer des fichiers PST aux dossiers publics dans Exchange Online ?**
  
Non, vous ne pouvez pas importer les fichiers PST aux dossiers publics.
  
 **Microsoft peut réinitialiser votre disque dur avant de leur expédier me ?**
  
Non, Microsoft ne peut pas effacer les disques durs avant leur expédition retour aux clients. Disques durs sont renvoyées pour vous dans le même état que si elles ont été reçues par Microsoft.
  
 **Peut Microsoft détruire votre disque dur au lieu de livraison retour à moi ?**
  
Non, Microsoft ne peut pas détruire votre disque dur. Disques durs sont renvoyées pour vous dans le même état que si elles ont été reçues par Microsoft.
  
 **Les services de courrier sont pris en charge pour les frais de retour ?**
  
Si vous êtes un client dans des États-Unis ou Europe, Microsoft utilise FedEx pour renvoyer votre disque dur. Pour toutes les autres régions, Microsoft utilise DHL.
  
 **Quels sont les frais d’expédition retour ?**
  
Renvoyer les frais d’expédition varient, selon votre proximité qui vous ont été livrés votre disque dur pour le centre de données Microsoft. Microsoft sera bill votre compte FedEx ou DHL pour renvoyer votre disque dur. Le coût de la transaction de retour est de votre responsabilité.
  
 **Puis-je utiliser un service de livraison courier personnalisés, tels que FedEx personnalisé transaction, d’envoyer votre disque dur à Microsoft ?**
  
Oui.
  
 **Si j’ai d’envoyer votre disque dur vers un autre pays, existe-t-il que dois-je faire ?**
  
Le disque dur qui vous envoyer à Microsoft devront traverser des frontières internationales. Si c’est le cas, vous êtes chargé de s’assurer que le disque dur et les données qu’il contient sont importées et/ou exportées conformément à la législation applicable. Avant de livrer un disque dur, vérifiez auprès de vos conseillers pour vérifier que votre lecteur et les données peuvent légalement être copiées vers le centre de données Microsoft spécifié. Cela vous permet de vérifier qu’il connecte à Microsoft en temps voulu.
