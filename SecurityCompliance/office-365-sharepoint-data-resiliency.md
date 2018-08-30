---
title: Résistance des données SharePoint Office 365
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
description: Vue d’ensemble de la résistance des données dans SharePoint Online dans Office 365.
ms.openlocfilehash: ba6259e8e582a4abcf0f184b162177119a57718f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528103"
---
# <a name="sharepoint-online-data-resiliency"></a>Résistance des données en ligne SharePoint
Un principe clé de SharePoint Online est de ne jamais avoir une seule copie de tout élément de données. SharePoint Online utilise la réplication de SQL Server, qui est un ensemble de technologies pour copier et distribuer des objets de données et la base de données à partir d’une base de données vers un autre et ensuite une synchronisation entre les bases de données pour assurer la cohérence. 

Par exemple, lorsqu’un utilisateur enregistre un fichier dans SharePoint Online, le fichier est mémorisé chiffré et stocké dans le stockage Blob Azure. Service d’objet Blob Azure fournit des mécanismes pour garantir l’intégrité des données à la fois au niveau des couches application et de transport. Cet article décrit en détail ces mécanismes du point de vue client et le service. Vérification MD5 est facultatif pour les opérations PUT et GET ; Toutefois, il fournit un procédé pratique pour garantir l’intégrité des données sur le réseau à l’aide de HTTP. En outre, étant donné que le protocole HTTPS assure le transport layer security supplémentaires MD5 de vérification n’est pas nécessaire lorsque vous vous connectez via HTTPS comme il le serait redondant. Service d’objet Blob Azure fournit un support de stockage durable et utilise sa propre vérifier l’intégrité des données stockées. Le MD5 qui sont utilisés lors de l’interaction avec une application sont fournies pour vérifier l’intégrité des données lors du transfert de données entre l’application et le service via HTTP. 

Pour garantir l’intégrité des données de l’objet Blob Azure service utilise les hachages MD5 des données de deux manières différentes. Il est important de comprendre comment ces valeurs sont calculées, transmises, stockées et éventuellement appliqués pour concevoir votre application à utiliser pour l’intégrité des données de manière appropriée. Pour plus d’informations, voir [Vue d’ensemble de Windows Azure Blob MD5](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx). 

Métadonnées et des pointeurs vers le fichier sont stockés dans une base de données SQL Server (la base de données). Tous les segments – fichiers, fichiers et mise à jour delta – sont stockées en tant qu’objets BLOB dans le stockage Azure répartis de manière aléatoire entre plusieurs comptes de stockage Azure. La base de données SQL est hébergé sur une baie RAID 10 est en miroir synchrone à une autre baie de stockage RAID 10 en rack distinct dans le même centre de données. Envoi de journaux asynchrone est ensuite utilisée pour répliquer les données vers une autre baie de stockage RAID 10 dans un deuxième centre de données. En plus de la protection des données avec RAID 10 et réplication synchrone et asynchrone, sauvegardes planifiée des données sont extraites qui sont répliqué également de manière asynchrone pour le deuxième centre de données. 

Dans SharePoint Online, les sauvegardes de données sont effectuées toutes les 12 heures et conservés pendant 14 jours. SharePoint Online utilise également un système de secours à chaud qui inclut des centres de données géographiquement distincts associés au sein du même client emplacement région de données (par exemple, Chicago et San Antonio pour les clients qui ont mis en service leur client aux États-Unis) configuré comme actif/actif. Par exemple, il existe des utilisateurs live dont Chicago centre de données principal et San Antonio comme un centre de données de basculement et les utilisateurs qui ont San Antonio, ainsi que leur centre de données principal Chicago en tant que leurs centres de données de basculement live. 