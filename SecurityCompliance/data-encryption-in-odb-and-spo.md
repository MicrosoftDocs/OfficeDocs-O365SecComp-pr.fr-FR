---
title: Chiffrement de données dans OneDrive Entreprise et SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 6501b5ef-6bf7-43df-b60d-f65781847d6c
ms.collection:
- M365-security-compliance
description: Maîtrisez les notions de base du chiffrement de la sécurité de données dans OneDrive Entreprise et SharePoint Online.
ms.openlocfilehash: a43db3da6e4663aee4437689ff51276972298872
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223213"
---
# <a name="data-encryption-in-onedrive-for-business-and-sharepoint-online"></a><span data-ttu-id="352b8-103">Chiffrement de données dans OneDrive Entreprise et SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="352b8-103">Data Encryption in OneDrive for Business and SharePoint Online</span></span>

<span data-ttu-id="352b8-104">Maîtrisez les notions de base du chiffrement de la sécurité de données dans OneDrive Entreprise et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="352b8-104">Understand the basic elements of encryption for data security in OneDrive for Business and SharePoint Online.</span></span>
  
## <a name="overview"></a><span data-ttu-id="352b8-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="352b8-105">Overview</span></span>

<span data-ttu-id="352b8-p101">Office 365 est un environnement hautement sécurisé qui fournit une protection étendue à de nombreux niveaux : sécurité de centre de données physique, sécurité réseau, sécurité d'accès, sécurité des applications et sécurité des données. Cet article s'intéresse plus particulièrement à l'aspect du chiffrement de la sécurité des données lors de leur transport et de leur stockage pour OneDrive Entreprise et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="352b8-p101">Office 365 is a highly secure environment that offers extensive protection in multiple layers: physical data center security, network security, access security, application security, and data security. This article specifically focuses on the in-transit and at-rest encryption side of data security for OneDrive for Business and SharePoint Online.</span></span>
  
<span data-ttu-id="352b8-108">Pour obtenir une description de la sécurité Office 365 dans son ensemble, consultez le livre [blanc sur la sécurité dans office 365](https://go.microsoft.com/fwlink/p/?LinkId=270895).</span><span class="sxs-lookup"><span data-stu-id="352b8-108">For a description of Office 365 security as a whole, see [Security in Office 365 White Paper](https://go.microsoft.com/fwlink/p/?LinkId=270895).</span></span>
  
<span data-ttu-id="352b8-109">Observez le fonctionnement du chiffrement des données dans la vidéo suivante.</span><span class="sxs-lookup"><span data-stu-id="352b8-109">Watch how data encryption works in the following video.</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/dea0dec4-4077-4095-9a32-19b94ea2da4b?autoplay=false]
  
## <a name="encryption-of-data-in-transit"></a><span data-ttu-id="352b8-110">Chiffrement des données lors de leur transport</span><span class="sxs-lookup"><span data-stu-id="352b8-110">Encryption of data in transit</span></span>

<span data-ttu-id="352b8-111">Dans OneDrive Entreprise et SharePoint Online, il existe deux scénarios dans lesquels les données entrent et sortent des centres de données.</span><span class="sxs-lookup"><span data-stu-id="352b8-111">In OneDrive for Business and SharePoint Online, there are two scenarios in which data enters and exits the datacenters.</span></span>
  
- <span data-ttu-id="352b8-p102">**Communication du client avec le serveur** La communication vers OneDrive Entreprise sur Internet utilise des connexions SSL/TLS. Toutes les connexions SSL sont établies à l'aide de clés 2 048 bits.</span><span class="sxs-lookup"><span data-stu-id="352b8-p102">**Client communication with the server** Communication to OneDrive for Business across the Internet uses SSL/TLS connections. All SSL connections are established using 2048-bit keys.</span></span> 
    
- <span data-ttu-id="352b8-p103">**Déplacement de données entre des centres de données** La raison principale du déplacement de données entre des centres de données est de permettre la récupération d'urgence via la géo-réplication. Par exemple, les deltas de stockage d'objets blob et les journaux de transaction SQL Server transitent par ce canal. Alors que ces données sont déjà transmises par le biais d'un réseau privé, elles sont encore mieux protégées à l'aide du meilleur chiffrement de sa catégorie.</span><span class="sxs-lookup"><span data-stu-id="352b8-p103">**Data movement between datacenters** The primary reason to move data between datacenters is for geo-replication to enable disaster recovery. For instance, SQL Server transaction logs and blob storage deltas travel along this pipe. While this data is already transmitted by using a private network, it is further protected with best-in-class encryption.</span></span> 
    
## <a name="encryption-of-data-at-rest"></a><span data-ttu-id="352b8-117">Chiffrement des données lors de leur stockage</span><span class="sxs-lookup"><span data-stu-id="352b8-117">Encryption of data at rest</span></span>

<span data-ttu-id="352b8-118">Le chiffrement lors du stockage comprend deux composants : le chiffrement au niveau du disque BitLocker et le chiffrement par fichier du contenu client.</span><span class="sxs-lookup"><span data-stu-id="352b8-118">Encryption at rest includes two components: BitLocker disk-level encryption and per-file encryption of customer content.</span></span>
  
<span data-ttu-id="352b8-p104">BitLocker est déployé pour OneDrive entreprise et SharePoint Online dans le service. Le chiffrement par fichier est également dans OneDrive entreprise et SharePoint Online dans Office 365 les environnements mutualisés et les nouveaux environnements dédiés qui sont basés sur la technologie mutualisée.</span><span class="sxs-lookup"><span data-stu-id="352b8-p104">BitLocker is deployed for OneDrive for Business and SharePoint Online across the service. Per-file encryption is also in OneDrive for Business and SharePoint Online in Office 365 multi-tenant and new dedicated environments that are built on multi-tenant technology.</span></span>
  
<span data-ttu-id="352b8-p105">Alors que BitLocker chiffre toutes les données sur un disque, le chiffrement par fichier va plus loin en ajoutant une clé de chiffrement unique pour chaque fichier. En outre, chaque mise à jour de chaque fichier est chiffrée à l'aide de sa propre clé de chiffrement. Avant d'être stockées, les clés permettant d'accéder au contenu chiffré sont stockées dans un emplacement physiquement distinct du contenu. Chaque étape de ce chiffrement utilise la méthode AES (Advanced Encryption Standard) avec des clés 256 bits et est conforme à la norme FIPS (Federal Information Processing Standard) 140-2. Le contenu chiffré est réparti sur un certain nombre de conteneurs dans l'ensemble du centre de données, et chaque conteneur possède des informations d'identification uniques. Ces informations sont stockées dans un emplacement physique distinct du contenu ou des clés de contenu.</span><span class="sxs-lookup"><span data-stu-id="352b8-p105">While BitLocker encrypts all data on a disk, per-file encryption goes even further by including a unique encryption key for each file. Further, every update to every file is encrypted using its own encryption key. Before they're stored, the keys to the encrypted content are stored in a physically separate location from the content. Every step of this encryption uses Advanced Encryption Standard (AES) with 256-bit keys and is Federal Information Processing Standard (FIPS) 140-2 compliant. The encrypted content is distributed across a number of containers throughout the datacenter, and each container has unique credentials. These credentials are stored in a separate physical location from either the content or the content keys.</span></span>
  
<span data-ttu-id="352b8-127">Pour plus d'informations sur la conformité FIPS 140-2, voir [fips 140-2 Compliance](https://go.microsoft.com/fwlink/?LinkId=517625).</span><span class="sxs-lookup"><span data-stu-id="352b8-127">For additional information about FIPS 140-2 compliance, see [FIPS 140-2 Compliance](https://go.microsoft.com/fwlink/?LinkId=517625).</span></span>
  
<span data-ttu-id="352b8-p106">Le chiffrement au niveau des fichiers sur REST tire parti du stockage BLOB afin de fournir une croissance de stockage quasiment illimitée et d'activer une protection sans précédent. Tout le contenu du client dans OneDrive entreprise et SharePoint Onlinewill être migré vers le stockage BLOB. Voici comment les données sont sécurisées:</span><span class="sxs-lookup"><span data-stu-id="352b8-p106">File-level encryption at rest takes advantage of blob storage to provide for virtually unlimited storage growth and to enable unprecedented protection. All customer content in OneDrive for Business and SharePoint Onlinewill be migrated to blob storage. Here's how that data is secured:</span></span>
  
1. <span data-ttu-id="352b8-p107">Tout le contenu est chiffré, potentiellement avec plusieurs clés, et réparti dans l'ensemble du centre de données. Chaque fichier à stocker est divisé en un ou plusieurs blocs, en fonction de sa taille. Ensuite, chaque bloc est chiffré à l'aide de sa propre clé unique. Les mises à jour sont traitées de la même façon : le jeu de modifications, ou deltas, soumis par un utilisateur est divisé en blocs, et chacun est chiffré avec sa propre clé.</span><span class="sxs-lookup"><span data-stu-id="352b8-p107">All content is encrypted, potentially with multiple keys, and distributed across the datacenter. Each file to be stored is broken into one or more chunks, depending its size. Then, each chunk is encrypted using its own unique key. Updates are handled similarly: the set of changes, or deltas, submitted by a user is broken into chunks, and each is encrypted with its own key.</span></span>
    
2. <span data-ttu-id="352b8-p108">Tous ces blocs (fichiers, parties de fichiers et deltas de mise à jour) sont stockés sous la forme d'objets blob dans le magasin d'objets blob. Ils sont également répartis au hasard entre plusieurs conteneurs d'objets blob.</span><span class="sxs-lookup"><span data-stu-id="352b8-p108">All of these chunks—files, pieces of files, and update deltas—are stored as blobs in our blob store. They also are randomly distributed across multiple blob containers.</span></span>
    
3. <span data-ttu-id="352b8-137">La « carte » utilisée pour ré-assembler le fichier à partir de ses composants est stockée dans la base de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="352b8-137">The "map" used to re-assemble the file from its components is stored in the Content Database.</span></span>
    
4. <span data-ttu-id="352b8-p109">Chaque conteneur d'objets blob dispose de ses propres informations d'identification uniques par type d'accès (lecture, écriture, énumération et suppression). Chaque jeu d'informations d'identification est conservé dans le magasin de clés sécurisé et est régulièrement actualisé.</span><span class="sxs-lookup"><span data-stu-id="352b8-p109">Each blob container has its own unique credentials per access type (read, write, enumerate, and delete). Each set of credentials is held in the secure Key Store and is regularly refreshed.</span></span>
    
<span data-ttu-id="352b8-140">En d'autres termes, trois types de magasins sont impliqués dans le chiffrement par fichier lors du stockage, chacun doté d'une fonction distincte :</span><span class="sxs-lookup"><span data-stu-id="352b8-140">In other words, there are three different types of stores involved in per-file encryption at rest, each with a distinct function:</span></span>
  
- <span data-ttu-id="352b8-p110">Le contenu est stocké sous la forme d'objets blob chiffrés dans le magasin correspondant. La clé permettant d'accéder à chaque bloc de contenu est chiffrée et stockée séparément dans la base de données de contenu. Le contenu lui-même ne fournit aucun indice quant à sa méthode de déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="352b8-p110">Content is stored as encrypted blobs in the blob store. The key to each chunk of content is encrypted and stored separately in the content database. The content itself holds no clue as to how it can be decrypted.</span></span>
    
- <span data-ttu-id="352b8-p111">La base de données de contenu est une base de données SQL Server. Elle contient la carte nécessaire à la localisation et à la reconstitution de l'ensemble des objets blob de contenu figurant dans le magasin d'objets blobs, ainsi que les clés nécessaires au déchiffrement de ces objets.</span><span class="sxs-lookup"><span data-stu-id="352b8-p111">The Content Database is a SQL Server database. It holds the map required to locate and reassemble all of the content blobs held in the blob store as well as the keys needed to decrypt those blobs.</span></span>
    
<span data-ttu-id="352b8-p112">Chacun de ces trois composants de stockage (magasin d'objets blob, base de données de contenu et magasin de clés) est séparé physiquement. Les informations contenues dans n'importe lequel des composants sont inutilisables en l'état, ce qui permet de garantir un niveau de sécurité sans précédent. Sans accès aux trois composants, il est impossible d'extraire les clés permettant d'accéder aux blocs, de les déchiffrer pour les rendre utilisables, de les associer avec leurs blocs correspondants, de déchiffrer un bloc ou de reconstituer un document à partir de ses blocs constitutifs.</span><span class="sxs-lookup"><span data-stu-id="352b8-p112">Each of these three storage components—the blob store, the Content Database, and the Key Store—is physically separate. The information held in any one of the components is unusable on its own. This provides an unprecedented level of security. Without access to all three it is impossible to retrieve the keys to the chunks, decrypt the keys to make them usable, associate the keys with their corresponding chunks, decrypt any chunk, or reconstruct a document from its constituent chunks.</span></span>
  

