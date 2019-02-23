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
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: "Pour les administrateurs: Découvrez comment utiliser le service d'importation dans le centre &amp; de sécurité conformité Office 365 pour importer en bloc des données de messagerie (fichiers PST) vers des boîtes aux lettres utilisateur dans Exchange Online. Cette rubrique présente les questions fréquemment posées et explique le fonctionnement du processus d'importation PST."
ms.openlocfilehash: b6f32a6b5552773c197003ddac41c138539bb6ef
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218044"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a>Overview of importing your organization PST files to Office 365

> [!NOTE]
> Cet article est destiné aux administrateurs. Essayez-vous d'importer des fichiers PST dans votre propre boîte aux lettres? Voir [importer le courrier, les contacts et le calendrier à partir d'un fichier. pst Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)

Vous pouvez utiliser le service d'importation dans le centre de &amp; sécurité conformité Office 365 pour importer rapidement des fichiers PST dans des boîtes aux lettres Exchange Online dans votre organisation Office 365. Vous pouvez importer des fichiers PST dans Office 365 de deux manières:
   
- **Chargement réseau** ![Chargement](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) sur le Cloud: Téléchargez les fichiers PST sur le réseau vers un emplacement de stockage Azure temporaire dans le Cloud Microsoft. Ensuite, vous utilisez le service d'importation Office 365 pour importer les données PST dans les boîtes aux lettres de votre organisation Office 365. 

- **Livraison de disque** ![Disque](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) dur: copiez les fichiers PST sur un disque dur chiffré par BitLocker, puis expédiez physiquement le lecteur à Microsoft. Lorsque Microsoft reçoit le disque dur, le personnel du centre de données télécharge les données vers un emplacement de stockage Azure temporaire dans le Cloud Microsoft. Ensuite, vous utilisez le service d'importation Office 365 pour importer les données dans les boîtes aux lettres de votre organisation Office 365.

## <a name="step-by-step-instructions"></a>Instructions pas à pas
  
Consultez l'une des rubriques suivantes pour obtenir des instructions détaillées pour importer en bloc les fichiers PST de votre organisation dans Office 365. 
   
- [Utiliser le chargement réseau pour importer des fichiers PST vers Office 365](use-network-upload-to-import-pst-files.md)
- [Utiliser l’expédition de disque pour importer des fichiers PST dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>Fonctionnement de l'importation de fichiers PST

Voici une illustration et une description du processus d'importation de fichiers PST complet. L'illustration montre le flux de travail principal et souligne les différences entre les modes de chargement réseau et de livraison de disque.
  
![Flux de travail du processus d'importation PST](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **Téléchargez les outils d'importation PST et la clé vers l'emplacement de stockage privé Azure** : la première étape consiste à télécharger l'outil et la clé d'accès utilisés pour télécharger les fichiers PST ou les copier sur un disque dur. Vous les obtenez à partir de la page d' **importation** dans le &amp; Centre de sécurité conformité Office 365. La clé vous fournit (ou le personnel du centre de données Microsoft en cas de livraison) avec les autorisations nécessaires pour télécharger des fichiers PST vers un emplacement de stockage Azure privé et sécurisé. Cette clé d'accès est propre à votre organisation et empêche tout accès non autorisé à vos fichiers PST une fois qu'ils sont téléchargés vers le Cloud Microsoft. Notez que l'importation de fichiers PST dans Office 365 ne nécessite pas que votre organisation dispose d'un abonnement Azure distinct. 
    
2. **Charger ou copier les fichiers PST** : l'étape suivante varie selon que vous utilisez le chargement réseau ou la livraison de lecteur pour importer des fichiers PST. Dans les deux cas, vous utiliserez l'outil et la clé de stockage sécurisée que vous avez obtenus à l'étape précédente.
    
    - **Chargement réseau** L'outil AzCopy. exe (téléchargé à l'étape 1) permet de télécharger et de stocker vos fichiers PST dans un emplacement de stockage Azure dans le Cloud Microsoft. Notez que l'emplacement de stockage Azure sur lequel vous chargez vos fichiers PST doit résider dans le même centre de centres Microsoft régional où se trouve votre organisation Office 365. 
    
      Pour les télécharger, les fichiers PST que vous souhaitez importer vers Office 365 doivent être situés dans un partage de fichiers ou un serveur de fichiers de votre organisation.
    
    - **Livraison de disque** L'outil outil waimportexport. exe (téléchargé à l'étape 1) est utilisé pour copier vos fichiers PST sur le disque dur. Cet outil chiffre le disque dur avec BitLocker, puis copie les fichiers PST sur le disque dur. Comme le chargement réseau, les fichiers PST que vous souhaitez copier sur le disque dur doivent être situés dans un partage de fichiers ou un serveur de fichiers de votre organisation.
    
3. **Créer un fichier de mappage d'importation PST** -une fois que les fichiers PST ont été téléchargés vers l'emplacement de stockage Azure ou copiés sur un disque dur, l'étape suivante consiste à créer un fichier de valeurs séparées par des virgules (CSV) qui spécifie les boîtes aux lettres utilisateur dans lesquelles les fichiers PST seront importés (a ND un fichier PST peut être importé dans la boîte aux lettres principale d'un utilisateur ou dans sa boîte aux lettres d'archivage). Le service d'importation Office 365 utilisera les informations pour importer les fichiers PST. 
    
4. **Créer une tâche d'importation PST** : l'étape suivante consiste à créer une tâche d'importation PST **** sur la page d'importation &amp; dans le centre de sécurité et d'envoyer le fichier de mappage d'importation PST créé à l'étape précédente. Pour le chargement réseau (étant donné que les fichiers PST ont été téléchargés vers Azure), Office 365 analyse les données dans les fichiers PST, puis vous offre la possibilité de définir des filtres qui contrôlent les données importées dans les boîtes aux lettres spécifiées dans le fichier de mappage d'importation PST. 
    
    Pour le lecteur, quelques éléments supplémentaires se produisent à ce stade du processus.
    
    - Vous expédiez physiquement le disque dur à un centre de données Microsoft (l'adresse d'expédition pour le centre de données Microsoft s'affiche lors de la création de la tâche d'importation).
    
    - Lorsque Microsoft reçoit le disque dur, le personnel du centre de données télécharge les fichiers PST sur le disque dur vers l'emplacement de stockage Azure de votre organisation. Comme expliqué précédemment, vos fichiers PST sont téléchargés vers un emplacement de stockage Azure qui réside dans le même centre de donnée régional Microsoft où se trouve votre organisation Office 365.
    
      > [!NOTE]
      > Les fichiers PST sur le disque dur sont téléchargés vers Azure dans les 7 à 10 jours ouvrables après que Microsoft a reçu le disque dur. 
  
      Comme le processus de chargement réseau, Office 365 analyse les données dans les fichiers PST et vous donne la possibilité de définir des filtres qui contrôlent les données importées dans les boîtes aux lettres spécifiées dans le fichier de mappage d'importation PST.
    
    - Microsoft vous renvoie le disque dur. 
    
5. **Filtrer les données PST qui seront importées vers des boîtes aux lettres** -une fois la tâche d'importation créée (et après que les fichiers PST d'une tâche d'expédition de disque sont téléchargés vers l'emplacement de stockage Azure) Office 365 analyse les données dans les fichiers PST (en toute sécurité et en toute sécurité) en l'identification de l'âge des éléments et des différents types de messages inclus dans les fichiers PST; Lorsque l'analyse est terminée et que les données sont prêtes à être importées, vous avez la possibilité d'importer toutes les données contenues dans les fichiers PST ou vous pouvez réduire les données importées en définissant des filtres qui contrôlent les données à importer. 
    
6. **Démarrer le travail d'importation PST** : une fois la tâche d'importation démarrée, Office 365 utilise les informations du fichier de mappage d'importation PST pour importer les fichiers PST à partir de l'emplacement de stockage Azure vers les boîtes aux lettres utilisateur. Les informations d'État relatives à la tâche d'importation (y compris les informations relatives à chaque fichier PST **** importé) sont affichées dans &amp; la page d'importation dans le centre de sécurité et de conformité. Une fois le travail d'importation terminé, l'état du travail est défini sur **terminé**.
  
## <a name="why-import-email-data-to-office-365"></a>Pourquoi importer des données de courrier électronique dans Office 365?

- L'importation de fichiers PST dans des boîtes aux lettres utilisateur est une façon de migrer le courrier électronique de votre organisation vers Office 365.
    
- Vous pouvez utiliser la fonctionnalité d' [importation intelligente](filter-data-when-importing-pst-files.md) pour filtrer les éléments des fichiers PST qui sont réellement importés dans les boîtes aux lettres cible. Cela vous permet de réduire les données importées en définissant des filtres qui contrôlent les données à importer. 
    
- L'importation de données de courrier électronique dans Office 365 permet de répondre aux besoins de conformité de votre organisation en vous permettant de:
    
  - Activez les [boîtes aux lettres](enable-archive-mailboxes.md) d'archivage et un [archivage illimité](unlimited-archiving.md) pour fournir aux utilisateurs un espace de stockage supplémentaire pour les boîtes aux lettres. 
    
  - Placez les boîtes aux lettres en [conservation pour litige](https://go.microsoft.com/fwlink/?linkid=841243) afin de conserver le contenu. 
    
  - Utilisez l' [outil de recherche de contenu](content-search.md) pour rechercher du contenu de boîte aux lettres. 
    
  - Utiliser des [cas eDiscovery](ediscovery-cases.md) pour gérer les enquêtes légales de votre organisation 
    
  - Utilisez les [stratégies](retention-policies.md) de rétention dans le centre de sécurité &amp; conformité pour contrôler la durée de conservation du contenu des boîtes aux lettres, puis supprimez le contenu après l'expiration de la période de rétention. 
    
- L'importation de données dans Office 365 contribue à la protection contre la perte de données. Les données de messagerie électronique importées vers Office 365 héritent des fonctionnalités de haute disponibilité d'Exchange Online.
    
- Les données de messagerie électronique dans Office 365 sont accessibles aux utilisateurs de tous les appareils, car elles sont stockées dans le Cloud.
    
## <a name="importing-sharepoint-data-to-office-365"></a>Importation de données SharePoint dans Office 365

Vous pouvez également importer des fichiers et des documents sur des sites SharePoint et des comptes OneDrive dans votre organisation Office 365. Pour plus d'informations, consultez les articles suivants:

- [Migrer vers SharePoint Online](https://docs.microsoft.com/sharepointmigration/migrate-to-sharepoint-online)

- [Présentation de l'outil de migration SharePoint](https://docs.microsoft.com/sharepointmigration/introducing-the-sharepoint-migration-tool)

- [Migrer vers SharePoint Online à l’aide de PowerShell](https://docs.microsoft.com/sharepointmigration/overview-spmt-ps-cmdlets)

- [Migrer votre contenu de partage de fichiers vers SharePoint Online à l'aide de la zone de données Azure](https://docs.microsoft.com/sharepointmigration/how-to-migrate-file-share-content-to-spo-using-azuredatabox)


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a>Forum aux questions sur l'importation de fichiers PST dans Office 365
  
Voici quelques questions fréquemment posées sur l'utilisation du service d'importation Office 365 pour importer en bloc des fichiers PST dans des boîtes aux lettres Office 365. 
  
- [Utilisation du chargement réseau pour importer des fichiers PST](#using-network-upload-to-import-pst-files)
  
- [Utilisation de l'expédition de disque pour importer des fichiers PST](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a>Utilisation du chargement réseau pour importer des fichiers PST

 **Quelles sont les autorisations requises pour créer des travaux d'importation dans le service d'importation Office 365?**
  
Vous devez disposer du rôle d'exportation d'importation de boîte aux lettres dans Exchange Online pour importer des fichiers PST dans des boîtes aux lettres Office 365. Par défaut, ce rôle n'est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle exportation d'importation de boîte aux lettres au groupe de rôles gestion de l'organisation. Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d'exportation d'importation de boîte aux lettres, puis vous ajouter vous-même ou d'autres utilisateurs en tant que membre. Pour plus d'informations, consultez les sections «ajouter un rôle à un groupe de rôles» ou «créer un groupe de rôles» dans [gérer des groupes de rôles dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
De plus, pour créer des travaux d'importation dans le centre &amp; de sécurité conformité Office 365, l'une des conditions suivantes doit être vraie:
  
- Vous devez disposer du rôle destinataires de messagerie dans Exchange Online. Par défaut, ce rôle est affecté aux groupes gestion de l'organisation et rôles de gestion des destinataires.
    
    Ou
    
- Vous devez être un administrateur général dans votre organisation Office 365.
    
> [!TIP]
> EnVisagez de créer un nouveau groupe de rôles dans Exchange Online spécialement destiné à l'importation de fichiers PST dans Office 365. Pour le niveau minimal de privilèges requis pour importer des fichiers PST, attribuez les rôles importation de boîte aux lettres et destinataires des messages au nouveau groupe de rôles, puis ajoutez des membres. 
  
 **Où le téléchargement réseau est-il disponible?**
  
Le chargement réseau est actuellement disponible aux États-Unis, au Canada, au Brésil, au Royaume-Uni, en Europe, en Inde, en Asie du sud-est, au Japon, en République de Corée et en Australie. Le chargement réseau sera bientôt disponible dans d'autres régions.
  
 **Quelle est la tarification pour l'importation de fichiers PST à l'aide du chargement réseau?**
  
L'utilisation du chargement réseau pour importer des fichiers PST est gratuite.
  
Cela signifie également que, après la suppression des fichiers PST de la zone de stockage Azure, ils ne figurent plus dans la liste des fichiers pour une tâche d'importation terminée dans le centre d'administration Office 365. Bien qu'une tâche d'importation puisse toujours être répertoriée sur la page **importer des données dans Office 365** , la liste des fichiers PST peut être vide lorsque vous affichez les détails des anciens travaux d'importation. 
  
 **Quelle version du format de fichier PST est prise en charge pour l'importation dans Office 365?**
  
Il existe deux versions du format de fichier PST: ANSI et Unicode. Nous vous recommandons d'importer les fichiers qui utilisent le format de fichier PST Unicode. Toutefois, les fichiers qui utilisent le format de fichier PST ANSI, tels que ceux pour les langues qui utilisent un jeu de caractères codés sur deux octets (DBCS), peuvent également être importés dans Office 365. Pour plus d'informations sur l'importation de fichiers PST ANSI, voir l'étape 4 dans [utiliser le chargement réseau pour importer des fichiers PST vers Office 365](https://go.microsoft.com/fwlink/p/?LinkId=823074).
  
En outre, les fichiers PST d'Outlook 2007 et versions ultérieures peuvent être importés dans Office 365.
  
 **Après avoir téléchargé mes fichiers PST dans la zone de stockage Azure, combien de temps sont-ils conservés dans Azure avant d'être supprimés?**
  
Lorsque vous utilisez la méthode de chargement réseau pour importer des fichiers PST, vous les Téléchargez dans un conteneur d'objets BLOB Azure nommé **ingestiondata**. Si aucune tâche d'importation n'est en cours sur la page d' **importation** dans &amp; le centre de sécurité et de conformité, tous les fichiers PST du conteneur **ingestiondata** dans Azure sont supprimés 30 jours après la création de la tâche d'importation la plus récente dans le fichier Security &amp;Centre de conformité. Cela signifie également que vous devez créer une nouvelle tâche d'importation dans le &amp; Centre de sécurité conformité (décrit à l'étape 5 dans les instructions de chargement réseau) dans les 30 jours suivant le téléchargement des fichiers PST vers Azure. 
  
Cela signifie également que, après la suppression des fichiers PST de la zone de stockage Azure, ils ne figurent plus dans la liste des fichiers pour une tâche d'importation terminée &amp; dans le centre de sécurité conformité. Bien qu'une tâche d'importation puisse toujours être répertoriée sur la page d' &amp; **importation** dans le centre de sécurité conformité, la liste des fichiers PST peut être vide lorsque vous affichez les détails des anciens travaux d'importation. 
  
 **Combien de temps faut-il pour importer un fichier PST dans une boîte aux lettres?**
  
Cela dépend de la capacité de votre réseau, mais il faut généralement plusieurs heures pour que chaque téraoctet (to) de données soit téléchargé vers la zone de stockage Azure de votre organisation. Une fois les fichiers PST copiés dans la zone de stockage Azure, un fichier PST est importé dans une boîte aux lettres Office 365 à un taux d'au moins 24 Go par jour. Si ce taux ne répond pas à vos besoins, vous pouvez envisager d'autres méthodes de migration des données de messagerie vers Office 365. Pour plus d'informations, consultez la rubrique [méthodes de migration de plusieurs comptes de messagerie vers Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Si différents fichiers PST sont importés dans des boîtes aux lettres cibles différentes, le processus d'importation se produit en parallèle; en d'autres termes, chaque paire de dossiers personnels/de boîtes aux lettres est importée simultanément. De même, si plusieurs fichiers PST sont importés dans la même boîte aux lettres, ils seront importés simultanément.
  
 **Existe-t-il une limite de taille de message lors de l'importation de fichiers PST?**
  
OK. Si un fichier PST contient un élément de boîte aux lettres dont la taille est supérieure à 150 Mo, l'élément est ignoré pendant le processus d'importation.
  
 **Les propriétés des messages, telles que la date d'envoi ou de réception du message, la liste des destinataires et d'autres propriétés, sont-elles conservées lorsque les fichiers PST sont importés dans une boîte aux lettres Office 365?**
  
OK. Les métadonnées du message d'origine ne sont pas modifiées pendant le processus d'importation.
  
 **Existe-t-il une limite au nombre de niveaux dans une hiérarchie de dossiers pour un fichier PST que je souhaite importer dans une boîte aux lettres?**
  
OK. Vous ne pouvez pas importer un fichier PST qui comporte 300 ou plusieurs niveaux de dossiers imbriqués.
  
 **Puis-je utiliser le chargement réseau pour importer des fichiers PST dans une boîte aux lettres inactive dans Office 365?**
  
Oui, cette fonctionnalité est désormais disponible.
  
 **Puis-je utiliser le chargement réseau pour importer des fichiers PST dans une boîte aux lettres d'archivage en ligne dans un déploiement hybride Exchange?**
  
Oui, cette fonctionnalité est désormais disponible.
  
 **Puis-je utiliser le chargement réseau pour importer des fichiers PST dans des dossiers publics dans Exchange Online?**
  
Non, vous ne pouvez pas importer de fichiers PST dans des dossiers publics.
  
### <a name="using-drive-shipping-to-import-pst-files"></a>Utilisation de l'expédition de disque pour importer des fichiers PST

 **Quelles sont les autorisations requises pour créer des travaux d'importation dans le service d'importation Office 365?**
  
Vous devez disposer du rôle d'exportation d'importation de boîte aux lettres pour importer des fichiers PST vers des boîtes aux lettres Office 365. Par défaut, ce rôle n'est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle exportation d'importation de boîte aux lettres au groupe de rôles gestion de l'organisation. Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d'exportation d'importation de boîte aux lettres, puis vous ajouter vous-même ou d'autres utilisateurs en tant que membre. Pour plus d'informations, consultez les sections «ajouter un rôle à un groupe de rôles» ou «créer un groupe de rôles» dans [gérer des groupes de rôles dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
De plus, pour créer des travaux d'importation dans le centre &amp; de sécurité conformité Office 365, l'une des conditions suivantes doit être vraie:
  
- Vous devez disposer du rôle destinataires de messagerie dans Exchange Online. Par défaut, ce rôle est affecté aux groupes gestion de l'organisation et rôles de gestion des destinataires.
    
    Ou
    
- Vous devez être un administrateur général dans votre organisation Office 365.
    
> [!TIP]
> EnVisagez de créer un nouveau groupe de rôles dans Exchange Online spécialement destiné à l'importation de fichiers PST dans Office 365. Pour le niveau minimal de privilèges requis pour importer des fichiers PST, attribuez les rôles importation de boîte aux lettres et destinataires des messages au nouveau groupe de rôles, puis ajoutez des membres. 
  
 **Où la livraison de disque est-elle disponible?**
  
La livraison de disque est actuellement disponible aux États-Unis, au Canada, au Brésil, au Royaume-Uni, en Europe, en Inde, à l'Asie de l'est, en Asie du sud-est, au Japon, en République de Corée et en Australie. La livraison des disques sera bientôt disponible dans d'autres régions.
  
 **Quels sont les accords de licence commerciale qui prennent en charge la livraison?**
  
Drive Shipping to import PST Files to Office 365 est disponible par le biais d'un contrat d'entreprise Microsoft (EA). La livraison de lecteur n'est pas disponible via un contrat de produits et de services Microsoft (MPSA).
  
 **Quelles sont les tarifs pour l'utilisation de l'expédition de disque pour importer des fichiers PST vers Office 365?**
  
Le coût d'utilisation de l'expédition de disque pour importer des fichiers PST vers des boîtes aux lettres Office 365 est de $2 USD par Go de données. Par exemple, si vous livrez un disque dur contenant 1 000 Go de fichiers PST, le coût est de $2 000 USD. Vous pouvez collaborer avec un partenaire pour régler les frais d'importation. Pour plus d'informations sur la recherche d'un partenaire, consultez [la rubrique trouver votre partenaire ou revendeur Office 365](https://go.microsoft.com/fwlink/p/?LinkId=785197).
  
 **Quels types de disques durs sont pris en charge pour la livraison de disque?**
  
Seuls les disques durs internes 2,5 pouce SSD ou 2,5 ou 3,5 pouces SATA II/III sont pris en charge pour être utilisés avec le service d'importation Office 365. Vous pouvez utiliser des disques durs jusqu'à 10 to. Pour les tâches d'importation, seul le premier volume de données du disque dur sera traité. Le volume de données doit être au format NTFS. Lorsque vous copiez des données sur un disque dur, vous pouvez les attacher directement à l'aide d'un connecteur SATA II/III de 2,5 pouces ou de l'attacher de façon externe à l'aide d'un adaptateur USB externe de 2,5 pouce ou 2,5 ou 3,5.
  
> [!IMPORTANT]
> Les disques durs externes équipés d'un adaptateur USB intégré ne sont pas pris en charge par le service d'importation Office 365. De plus, le disque à l'intérieur de la casse d'un disque dur externe ne peut pas être utilisé. Veuillez ne pas livrer de disques durs externes. 
  
 **Combien de disques durs puis-je livrer pour une tâche d'importation unique?**
  
Vous pouvez expédier un maximum de 10 disques durs pour une tâche d'importation unique.
  
 **Après avoir livré mon disque dur, combien de temps faut-il pour accéder au centre de données Microsoft?**
  
Cela dépend de plusieurs facteurs, tels que la proximité du centre de données Microsoft et le type d'option d'expédition que vous avez utilisé pour livrer votre disque dur (par exemple, livraison le jour suivant, livraison sur deux jours ou livraison en masse). Avec la plupart des expéditeurs, vous pouvez utiliser le numéro de suivi pour suivre l'état de votre remise.
  
 **Une fois mon disque dur atteint dans le centre de données Microsoft, combien de temps faut-il pour charger mes fichiers PST sur Azure?**
  
Une fois que votre disque dur est reçu dans le centre de données Microsoft, il faut entre 7 et 10 jours ouvrés pour télécharger les fichiers PST dans la zone de stockage Microsoft Azure de votre organisation. Les fichiers PST seront téléchargés vers un conteneur d'objets BLOB Azure nommé `ingestiondata`. 
  
 **Combien de temps faut-il pour importer un fichier PST dans une boîte aux lettres?**
  
Une fois les fichiers PST téléchargés vers la zone de stockage Azure, Office 365 analyse les données dans les fichiers PST (de manière sûre et sécurisée) pour identifier l'âge des éléments et les différents types de messages inclus dans les fichiers PST. Une fois cette analyse terminée, vous aurez la possibilité d'importer toutes les données des fichiers PST ou de définir des filtres pour contrôler les données importées. Une fois le travail d'importation démarré, un fichier PST est importé dans une boîte aux lettres Office 365 à un taux d'au moins 24 Go par jour. Si ce taux ne répond pas à vos besoins, vous pouvez envisager d'utiliser d'autres méthodes pour importer des données de courrier électronique dans Office 365. Pour plus d'informations, consultez la rubrique [méthodes de migration de plusieurs comptes de messagerie vers Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Si différents fichiers PST sont importés dans des boîtes aux lettres cibles différentes, le processus d'importation se produit en parallèle; en d'autres termes, chaque paire de dossiers personnels/de boîtes aux lettres est importée simultanément. De même, si plusieurs fichiers PST sont importés dans la même boîte aux lettres, ils seront importés simultanément.
  
 **Après que Microsoft a téléchargé mes fichiers PST sur Azure, combien de temps sont-ils conservés dans Azure avant d'être supprimés?**
  
Tous les fichiers PST de l'emplacement de stockage Azure de votre organisation (dans un `ingestiondata`conteneur BLOB nommé) sont supprimés 30 jours après la création de la tâche d'importation la plus récente sur la &amp; page d' **importation** dans le centre de sécurité et de conformité. 
  
Cela signifie également que, après la suppression des fichiers PST de la zone de stockage Azure, ils ne figurent plus dans la liste des fichiers pour une tâche d'importation terminée &amp; dans le centre de sécurité conformité. Bien qu'une tâche d'importation puisse toujours être répertoriée sur la page d' &amp; **importation** dans le centre de sécurité conformité, la liste des fichiers PST peut être vide lorsque vous affichez les détails des anciens travaux d'importation. 
  
 **Quelle version du format de fichier PST est prise en charge pour l'importation dans Office 365?**
  
Il existe deux versions du format de fichier PST: ANSI et Unicode. Nous vous recommandons d'importer les fichiers qui utilisent le format de fichier PST Unicode. Toutefois, les fichiers qui utilisent le format de fichier PST ANSI, tels que ceux pour les langues qui utilisent un jeu de caractères codés sur deux octets (DBCS), peuvent également être importés dans Office 365. Pour plus d'informations sur l'importation de fichiers PST ANSI, reportez-vous à l'étape 3 de la section [utilisation du livre de livraison pour importer les fichiers PST de votre organisation dans Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
En outre, les fichiers PST d'Outlook 2007 et versions ultérieures peuvent être importés dans Office 365.
  
 **Existe-t-il une limite de taille de message lors de l'importation de fichiers PST?**
  
OK. Si un fichier PST contient un élément de boîte aux lettres dont la taille est supérieure à 150 Mo, l'élément est ignoré pendant le processus d'importation.
  
 **Les propriétés des messages, telles que la date d'envoi ou de réception du message, la liste des destinataires et d'autres propriétés, sont-elles conservées lorsque les fichiers PST sont importés dans une boîte aux lettres Office 365?**
  
OK. Les métadonnées du message d'origine ne sont pas modifiées pendant le processus d'importation
  
 **Existe-t-il une limite au nombre de niveaux dans une hiérarchie de dossiers pour un fichier PST que je souhaite importer dans une boîte aux lettres?**
  
OK. Vous ne pouvez pas importer un fichier PST qui comporte 300 ou plusieurs niveaux de dossiers imbriqués.
  
 **Puis-je utiliser l'expédition de disque pour importer des fichiers PST dans une boîte aux lettres inactive dans Office 365?**
  
Oui, cette fonctionnalité est désormais disponible.
  
 **Puis-je utiliser l'expédition de disque pour importer des fichiers PST dans une boîte aux lettres d'archivage en ligne dans un déploiement hybride Exchange?**
  
Oui, cette fonctionnalité est désormais disponible.
  
 **Puis-je utiliser l'expédition de disque pour importer des fichiers PST dans des dossiers publics dans Exchange Online?**
  
Non, vous ne pouvez pas importer de fichiers PST dans des dossiers publics.
  
 **Est-ce que Microsoft peut effacer mon disque dur avant de me le remettre?**
  
Non, Microsoft ne peut pas effacer les disques durs avant de les livrer aux clients. Les disques durs vous sont renvoyés dans le même État que celui dans lequel ils étaient reçus par Microsoft.
  
 **Microsoft peut-il broyer mon disque dur au lieu de l'expédier de nouveau à moi?**
  
Non, Microsoft ne peut pas détruire votre disque dur. Les disques durs vous sont renvoyés dans le même État que celui dans lequel ils étaient reçus par Microsoft.
  
 **Quels services de messagerie sont pris en charge pour la livraison de retour?**
  
Si vous êtes un client aux États-Unis ou en Europe, Microsoft utilise FedEx pour retourner votre disque dur. Pour toutes les autres régions, Microsoft utilise DHL.
  
 **Quels sont les frais d'expédition de retour?**
  
Les frais d'expédition de retour varient en fonction de la proximité du centre de données Microsoft auquel vous avez envoyé votre disque dur. Microsoft facturera votre compte FedEx ou DHL pour retourner votre disque dur. Le coût de l'expédition de retour est votre responsabilité.
  
 **Puis-je utiliser un service de livraison par courrier personnalisé, tel qu'FedEx Custom Shipping, pour livrer mon disque dur à Microsoft?**
  
Oui.
  
 **Si j'ai besoin de livrer mon disque dur à un autre pays, y a-t-il quelque chose que je dois faire?**
  
Le disque dur que vous livrez à Microsoft peut être amené à franchir les bordures internationales. Dans ce cas, vous devez vous assurer que le disque dur et les données qu'il contient sont importés et/ou exportés conformément à la législation applicable. Avant d'expédier un disque dur, vérifiez auprès de vos conseillers que votre lecteur et vos données peuvent être légalement expédiées vers le centre de données Microsoft spécifié. Cela permet de s'assurer qu'il parvient à Microsoft en un temps opportun.
