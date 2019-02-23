---
title: FAQ sur l'importation de fichiers PST dans Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 2fe71b05-f5a2-4182-ade7-4dc5cabdfd51
description: "Forum aux questions pour les administrateurs sur l'utilisation du service d'importation Office 365 pour importer les fichiers PST de votre Organizaiton dans des boîtes aux lettres Office 365. "
ms.openlocfilehash: 9ca2e206a1d06c1398181c51e41b4dc68d8d965c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218404"
---
# <a name="faq-about-importing-pst-files-to-office-365"></a>FAQ sur l'importation de fichiers PST dans Office 365

**Cet article est destiné aux administrateurs. Voulez-vous importer des fichiers PST dans votre propre boîte aux lettres? Voir [importer le courrier, les contacts et le calendrier à partir d'un fichier. pst Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)**|
   
Voici quelques questions fréquemment posées sur l'utilisation du service d'importation Office 365 pour importer en bloc des fichiers PST dans des boîtes aux lettres Office 365. Pour plus d'informations sur l'importation de fichiers PST, voir [vue d'ensemble de l'importation de fichiers PST dans Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84).
  
## <a name="using-network-upload-to-import-pst-files"></a>Utilisation du chargement réseau pour importer des fichiers PST

Pour obtenir des instructions pas à pas, consultez la rubrique [utiliser le chargement réseau pour importer des fichiers PST dans Office 365](use-network-upload-to-import-pst-files.md).
  
 **Quelles sont les autorisations requises pour créer des travaux d'importation dans le service d'importation Office 365?**
  
Vous devez disposer du rôle d'exportation d'importation de boîte aux lettres dans Exchange Online pour importer des fichiers PST dans des boîtes aux lettres Office 365. Par défaut, ce rôle n'est affecté à aucun groupe de rôles dans Exchange Online. Vous pouvez ajouter le rôle exportation d'importation de boîte aux lettres au groupe de rôles gestion de l'organisation. Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d'exportation d'importation de boîte aux lettres, puis vous ajouter vous-même ou d'autres utilisateurs en tant que membre. Pour plus d'informations, consultez les sections «ajouter un rôle à un groupe de rôles» ou «créer un groupe de rôles» dans [gérer des groupes de rôles dans Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
De plus, pour créer des travaux d'importation dans le centre &amp; de sécurité conformité Office 365, l'une des conditions suivantes doit être vraie:
  
- Vous devez disposer du rôle destinataires de messagerie dans Exchange Online. Par défaut, ce rôle est affecté aux groupes gestion de l'organisation et rôles de gestion des destinataires.
    
    Ou
    
- Vous devez être un administrateur général dans votre organisation Office 365.
    
> [!TIP]
> EnVisagez de créer un nouveau groupe de rôles dans Exchange Online spécialement destiné à l'importation de fichiers PST dans Office 365. Pour le niveau minimal de privilèges requis pour importer des fichiers PST, attribuez les rôles importation de boîte aux lettres et destinataires des messages au nouveau groupe de rôles, puis ajoutez des membres. 
  
 **Où le téléchargement réseau est-il disponible?**
  
Le chargement réseau est actuellement disponible aux États-Unis, au Canada, au Brésil, au Royaume-Uni, en France, en Europe, en Inde, à l'Asie de l'est, au sud-est, au Japon, en République de Corée et en Australie. Le chargement réseau sera bientôt disponible dans d'autres régions.
  
 **Quelle est la tarification pour l'importation de fichiers PST à l'aide du chargement réseau?**
  
L'utilisation du chargement réseau pour importer des fichiers PST est gratuite.
  
Cela signifie également que, après la suppression des fichiers PST de la zone de stockage Azure, ils ne figurent plus dans la liste des fichiers pour une tâche d'importation terminée dans le centre d'administration Office 365. Bien qu'une tâche d'importation puisse toujours être répertoriée sur la page **importer des données dans Office 365** , la liste des fichiers PST peut être vide lorsque vous affichez les détails des anciens travaux d'importation. 
  
 **Quelle version du format de fichier PST est prise en charge pour l'importation dans Office 365?**
  
Il existe deux versions du format de fichier PST: ANSI et Unicode. Nous vous recommandons d'importer les fichiers qui utilisent le format de fichier PST Unicode. Toutefois, les fichiers qui utilisent le format de fichier PST ANSI, tels que ceux pour les langues qui utilisent un jeu de caractères codés sur deux octets (DBCS), peuvent également être importés dans Office 365. Pour plus d'informations sur l'importation de fichiers PST ANSI, reportez-vous à l'étape 4 dans [utiliser le chargement réseau pour importer les fichiers PST de votre organisation dans Office 365](use-network-upload-to-import-pst-files.md#step-4-create-the-pst-import-mapping-file).
  
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
  
## <a name="using-drive-shipping-to-import-pst-files"></a>Utilisation de l'expédition de disque pour importer des fichiers PST

Pour obtenir des instructions pas à pas, voir [use Drive Shipping to import PST Files to Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md).
  
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
  
Une fois que votre disque dur est reçu dans le centre de données Microsoft, il faut entre 7 et 10 jours ouvrés pour télécharger les fichiers PST dans la zone de stockage Microsoft Azure de votre organisation. Les fichiers PST seront téléchargés vers un conteneur d'objets BLOB Azure nommé **ingestiondata**. 
  
 **Combien de temps faut-il pour importer un fichier PST dans une boîte aux lettres?**
  
Une fois les fichiers PST téléchargés vers la zone de stockage Azure, Office 365 analyse les données dans les fichiers PST (de manière sûre et sécurisée) pour identifier l'âge des éléments et les différents types de messages inclus dans les fichiers PST. Une fois cette analyse terminée, vous aurez la possibilité d'importer toutes les données des fichiers PST ou de définir des filtres pour contrôler les données importées. Une fois le travail d'importation démarré, un fichier PST est importé dans une boîte aux lettres Office 365 à un taux d'au moins 24 Go par jour. Si ce taux ne répond pas à vos besoins, vous pouvez envisager d'utiliser d'autres méthodes pour importer des données de courrier électronique dans Office 365. Pour plus d'informations, consultez la rubrique [méthodes de migration de plusieurs comptes de messagerie vers Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
Si différents fichiers PST sont importés dans des boîtes aux lettres cibles différentes, le processus d'importation se produit en parallèle; en d'autres termes, chaque paire de dossiers personnels/de boîtes aux lettres est importée simultanément. De même, si plusieurs fichiers PST sont importés dans la même boîte aux lettres, ils seront importés simultanément.
  
 **Après que Microsoft a téléchargé mes fichiers PST sur Azure, combien de temps sont-ils conservés dans Azure avant d'être supprimés?**
  
Tous les fichiers PST de l'emplacement de stockage Azure de votre organisation (dans un conteneur BLOB nommé **ingestiondata** ), sont supprimés 30 jours après la création de la tâche d'importation la plus récente sur &amp; la page d' **importation** dans le centre de sécurité et de conformité. 
  
Cela signifie également que, après la suppression des fichiers PST de la zone de stockage Azure, ils ne figurent plus dans la liste des fichiers pour une tâche d'importation terminée &amp; dans le centre de sécurité conformité. Bien qu'une tâche d'importation puisse toujours être répertoriée sur la page d' &amp; **importation** dans le centre de sécurité conformité, la liste des fichiers PST peut être vide lorsque vous affichez les détails des anciens travaux d'importation. 
  
 **Quelle version du format de fichier PST est prise en charge pour l'importation dans Office 365?**
  
Il existe deux versions du format de fichier PST: ANSI et Unicode. Nous vous recommandons d'importer les fichiers qui utilisent le format de fichier PST Unicode. Toutefois, les fichiers qui utilisent le format de fichier PST ANSI, tels que ceux pour les langues qui utilisent un jeu de caractères codés sur deux octets (DBCS), peuvent également être importés dans Office 365. Pour plus d'informations sur l'importation de fichiers PST ANSI, reportez-vous à l'étape 3 de la section [use Drive Shipping to import PST Files to Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
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
