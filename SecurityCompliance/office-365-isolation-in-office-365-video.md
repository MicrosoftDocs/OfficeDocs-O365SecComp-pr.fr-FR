---
title: Isolation du locataire Office 365 dans Office 365 vidéo
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Une explication de l’isolation du locataire dans Office 365 vidéo.'
ms.openlocfilehash: 9476047d56161ec2589fdf743d7ee837ea558865
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528366"
---
# <a name="tenant-isolation-in-office-365-video"></a>Isolation du locataire dans Office 365 vidéo

> [!NOTE]
> Office 365 vidéo sera remplacé par Microsoft Stream. Pour en savoir plus sur le nouveau service vidéo entreprise qui ajoute l’aide à la décision pour la collaboration vidéo et en savoir plus sur les plans de transition pour les clients Office 365 vidéo en cours, voir [migrer vers le flux vidéo Office 365](https://docs.microsoft.com/stream/).

## <a name="introduction"></a>Présentation
Stockage Azure est utilisé pour stocker les données de plusieurs services Office 365, notamment Office 365 vidéo et balancement. Stockage Azure inclut le stockage Blob, qui est un magasin d’objets nuage hautement évolutive, basée sur REST, qui est utilisé pour stocker les données non structurées. Stockage Azure utilise un modèle de contrôle d’accès simple ; chaque abonnement Azure peut créer un ou plusieurs comptes de stockage. Chaque compte de stockage possède une clé secrète unique qui permet de contrôler l’accès à toutes les données de ce compte de stockage. Il prend en charge le scénario où le stockage est associé aux applications et les applications ont un contrôle total sur leurs données associées ; par exemple, balancement stockant du contenu dans le stockage Azure. Tout le contenu client pour balancement est stocké dans les comptes de stockage Azure partagé. Le contenu de chaque utilisateur est dans une arborescence distincte des objets BLOB dans le stockage Azure.

Les systèmes de gestion de l’accès aux environnements client (par exemple, le Azure Portal, SMAPI, etc.) sont isolées au sein d’une application Azure gérée par Microsoft. Logiquement, cela sépare l’infrastructure d’accès client dans les applications de client et de la couche de stockage.

## <a name="tenant-isolation-in-office-365-video"></a>Isolation du locataire dans Office 365 vidéo
[Office 365 vidéo](https://support.office.com/article/Meet-Office-365-Video-ca1cc1a9-a615-46e1-b6a3-40dbd99939a6) est un portail d’entreprise qui offre aux entreprises une destination hautement sécurisée, l’organisation de publication, le partage et découverte de contenu vidéo. Dans Office 365 vidéo, vidéos de chaque client sont conservés isolé et chiffrés dans tous les emplacements et qui sont uniquement disponibles pour les utilisateurs authentifiés qui ont des autorisations d’accès et les vidéos de l’organisation. Vidéo Office 365 utilise une combinaison de technologies pour y parvenir :
- SharePoint Online est utilisé pour enregistrer le fichier vidéo et les métadonnées (titre de la vidéo, description, etc.). Il fournit également la couche de sécurité et conformité (y compris l’authentification) et les fonctionnalités de recherche.
- Azure Media Services fournit transcodage, diffusion adaptative, remise sécurisée (à l’aide du chiffrement AES) et les fonctionnalités miniatures.

[Azure Media Services](https://azure.microsoft.com/services/media-services/) est une plateforme-comme-a-offre de services d’activation de bout en bout des workflows dans le nuage. La plate-forme fournit une API REST pour le téléchargement, codage, le chiffrement (avec PlayReady) et de livraison du média par le biais de centres de données Azure dans le monde entier.

Tous les téléchargements pour Office 365 vidéo se produisent via HTTPS. Lorsqu’un fichier vidéo est téléchargé, il est stocké dans SharePoint Online, et une copie du fichier est envoyée via un canal chiffré pour Azure Media Services. Azure Media Services convertit la vidéo dans plusieurs formats sont optimisées pour l’affichage (par exemple, mobile, faible bande passante, large bande passante, etc.). Ces fichiers, ainsi que le fichier d’origine acquis lors du téléchargement, sont stockés dans le stockage Blob Azure. Les fichiers sont chiffrés à l’aide d’AES 128 par l’algorithme de packaging chiffrement courantes MPEG (ou une version antérieure de PlayReady) pour la lecture et chiffrés à l’aide du chiffrement de stockage AES 256 avant d’être stocké dans le stockage Blob Azure. (À l’aide du SDK Azure Media Services Client, les clients peuvent contrôler le chiffrement est utilisé. Par exemple, un client peut appliquer cryptage du stockage Azure Media Services (AES 256) à une ressource multimédia haute valeur avant de le télécharger le stockage Blob Azure.)

Azure Media Services génère également une vignette pour la vidéo, il transmet ainsi que des métadonnées miniature vers SharePoint Online via un canal chiffré.
