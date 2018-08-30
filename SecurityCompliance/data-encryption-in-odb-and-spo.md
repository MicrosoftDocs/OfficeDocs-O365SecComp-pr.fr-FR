---
title: Chiffrement de données dans OneDrive Entreprise et SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MET150
ms.assetid: 6501b5ef-6bf7-43df-b60d-f65781847d6c
description: Maîtrisez les notions de base du chiffrement de la sécurité de données dans OneDrive Entreprise et SharePoint Online.
ms.openlocfilehash: 807ef2a195b5c29e769bd0f6757a0319b154b9d3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528754"
---
# <a name="data-encryption-in-onedrive-for-business-and-sharepoint-online"></a>Chiffrement de données dans OneDrive Entreprise et SharePoint Online

Maîtrisez les notions de base du chiffrement de la sécurité de données dans OneDrive Entreprise et SharePoint Online.
  
## <a name="overview"></a>Vue d'ensemble

Office 365 est un environnement hautement sécurisé qui fournit une protection étendue à de nombreux niveaux : sécurité de centre de données physique, sécurité réseau, sécurité d'accès, sécurité des applications et sécurité des données. Cet article s'intéresse plus particulièrement à l'aspect du chiffrement de la sécurité des données lors de leur transport et de leur stockage pour OneDrive Entreprise et SharePoint Online.
  
Pour obtenir une description de la sécurité Office 365 dans sa globalité, voir [sécurité dans Office 365 livre blanc](https://go.microsoft.com/fwlink/p/?LinkId=270895).
  
Observez le fonctionnement du chiffrement des données dans la vidéo suivante.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/dea0dec4-4077-4095-9a32-19b94ea2da4b?autoplay=false]
  
## <a name="encryption-of-data-in-transit"></a>Chiffrement des données lors de leur transport

Dans OneDrive Entreprise et SharePoint Online, il existe deux scénarios dans lesquels les données entrent et sortent des centres de données.
  
- **Communication du client avec le serveur** La communication vers OneDrive Entreprise sur Internet utilise des connexions SSL/TLS. Toutes les connexions SSL sont établies à l'aide de clés 2 048 bits. 
    
- **Déplacement de données entre des centres de données** La raison principale du déplacement de données entre des centres de données est de permettre la récupération d'urgence via la géo-réplication. Par exemple, les deltas de stockage d'objets blob et les journaux de transaction SQL Server transitent par ce canal. Alors que ces données sont déjà transmises par le biais d'un réseau privé, elles sont encore mieux protégées à l'aide du meilleur chiffrement de sa catégorie. 
    
## <a name="encryption-of-data-at-rest"></a>Chiffrement des données lors de leur stockage

Le chiffrement lors du stockage comprend deux composants : le chiffrement au niveau du disque BitLocker et le chiffrement par fichier du contenu client.
  
BitLocker est déployé pour OneDrive pour les entreprises et SharePoint Online sur le service. Chiffrement par fichier est également sur OneDrive entreprise et SharePoint Online dans Office 365 multiclients et environnements nouveau dédiés qui sont basés sur la technologie de plusieurs cliente.
  
Alors que BitLocker chiffre toutes les données sur un disque, le chiffrement par fichier va plus loin en ajoutant une clé de chiffrement unique pour chaque fichier. En outre, chaque mise à jour de chaque fichier est chiffrée à l'aide de sa propre clé de chiffrement. Avant d'être stockées, les clés permettant d'accéder au contenu chiffré sont stockées dans un emplacement physiquement distinct du contenu. Chaque étape de ce chiffrement utilise la méthode AES (Advanced Encryption Standard) avec des clés 256 bits et est conforme à la norme FIPS (Federal Information Processing Standard) 140-2. Le contenu chiffré est réparti sur un certain nombre de conteneurs dans l'ensemble du centre de données, et chaque conteneur possède des informations d'identification uniques. Ces informations sont stockées dans un emplacement physique distinct du contenu ou des clés de contenu.
  
Pour plus d’informations sur la conformité FIPS 140-2, voir [la conformité FIPS 140-2](https://go.microsoft.com/fwlink/?LinkId=517625).
  
Chiffrement au niveau des fichiers au repos tire parti du stockage blob pour prévoir la croissance de stockage quasi illimitée et activer une protection sans précédent. Tout le contenu client de OneDrive entreprise et SharePoint Onlinewill être migrée pour le stockage blob. Voici comment ces données sont-elles sécurisées :
  
1. Tout le contenu est chiffré, potentiellement avec plusieurs clés, et réparti dans l'ensemble du centre de données. Chaque fichier à stocker est divisé en un ou plusieurs blocs, en fonction de sa taille. Ensuite, chaque bloc est chiffré à l'aide de sa propre clé unique. Les mises à jour sont traitées de la même façon : le jeu de modifications, ou deltas, soumis par un utilisateur est divisé en blocs, et chacun est chiffré avec sa propre clé.
    
2. Tous ces blocs (fichiers, parties de fichiers et deltas de mise à jour) sont stockés sous la forme d'objets blob dans le magasin d'objets blob. Ils sont également répartis au hasard entre plusieurs conteneurs d'objets blob.
    
3. La « carte » utilisée pour ré-assembler le fichier à partir de ses composants est stockée dans la base de données de contenu.
    
4. Chaque conteneur d'objets blob dispose de ses propres informations d'identification uniques par type d'accès (lecture, écriture, énumération et suppression). Chaque jeu d'informations d'identification est conservé dans le magasin de clés sécurisé et est régulièrement actualisé.
    
En d'autres termes, trois types de magasins sont impliqués dans le chiffrement par fichier lors du stockage, chacun doté d'une fonction distincte :
  
- Le contenu est stocké sous la forme d'objets blob chiffrés dans le magasin correspondant. La clé permettant d'accéder à chaque bloc de contenu est chiffrée et stockée séparément dans la base de données de contenu. Le contenu lui-même ne fournit aucun indice quant à sa méthode de déchiffrement.
    
- La base de données de contenu est une base de données SQL Server. Elle contient la carte nécessaire à la localisation et à la reconstitution de l'ensemble des objets blob de contenu figurant dans le magasin d'objets blobs, ainsi que les clés nécessaires au déchiffrement de ces objets.
    
Chacun de ces trois composants de stockage (magasin d'objets blob, base de données de contenu et magasin de clés) est séparé physiquement. Les informations contenues dans n'importe lequel des composants sont inutilisables en l'état, ce qui permet de garantir un niveau de sécurité sans précédent. Sans accès aux trois composants, il est impossible d'extraire les clés permettant d'accéder aux blocs, de les déchiffrer pour les rendre utilisables, de les associer avec leurs blocs correspondants, de déchiffrer un bloc ou de reconstituer un document à partir de ses blocs constitutifs.
  

