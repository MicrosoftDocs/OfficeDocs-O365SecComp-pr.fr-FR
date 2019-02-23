---
title: RéSilience de données SharePoint Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Vue d'ensemble de la résilience des données dans SharePoint Online dans Office 365.
ms.openlocfilehash: 4fd17b50551639f6e11975acbc3822fb6ffa8bb2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214804"
---
# <a name="sharepoint-online-data-resiliency"></a>RéSilience des données SharePoint Online
Un principe clé pour SharePoint Online consiste à ne jamais avoir une seule copie de tout élément de données. SharePoint Online utilise la réplication SQL Server, qui est un ensemble de technologies permettant de copier et de distribuer des données et des objets de base de données d'une base de données à une autre, puis de synchroniser les bases de données pour assurer la cohérence. 

Par exemple, lorsqu'un utilisateur enregistre un fichier dans SharePoint Online, le fichier est segmenté, chiffré et stocké dans Azure BLOB Storage. Le service BLOB Azure fournit des mécanismes pour garantir l'intégrité des données à la fois au niveau de l'application et de la couche de transport. Ce billet détaille ces mécanismes du point de vue du client et du service. La vérification MD5 est facultative sur les opérations PUT et GET; Toutefois, il fournit une fonctionnalité pratique pour garantir l'intégrité des données sur le réseau lors de l'utilisation du protocole HTTP. De plus, étant donné que le protocole HTTPs assure la sécurité de la couche de transport, la vérification MD5 supplémentaire n'est pas nécessaire lors de la connexion via HTTPs, car elle serait redondante. Le service BLOB Azure fournit un support de stockage durable et utilise sa propre vérification de l'intégrité pour les données stockées. Les MD5's utilisées lors de l'interaction avec une application sont fournies pour vérifier l'intégrité des données lors du transfert de ces données entre l'application et le service via HTTP. 

Pour garantir l'intégrité des données, le service d'objets BLOB Azure utilise des hachages MD5 des données de différentes manières. Il est important de comprendre comment ces valeurs sont calculées, transmises, stockées et éventuellement appliquées pour concevoir votre application de manière appropriée afin de les utiliser pour assurer l'intégrité des données. Pour plus d'informations, consultez la rubrique [Windows Azure BLOB MD5 Overview](http://blogs.msdn.com/b/windowsazurestorage/archive/2011/02/18/windows-azure-blob-md5-overview.aspx). 

Les métadonnées et les pointeurs vers le fichier sont stockés dans une base de données SQL Server (la base de données de contenu). Tous les blocs (fichiers, fragments de fichiers et deltas de mise à jour) sont stockés en tant qu'objets BLOB dans le stockage Azure qui sont répartis de manière aléatoire entre plusieurs comptes de stockage Azure. La base de données SQL est hébergée sur une baie de stockage RAID 10 qui est mise en miroir de façon synchrone vers une autre baie de stockage RAID 10 dans un rack distinct au sein du même centre de données. La copie de journal asynchrone est ensuite utilisée pour répliquer les données vers une autre baie de stockage RAID 10 dans un deuxième centre de données. En plus de protéger les données avec RAID 10 et la réplication synchrone et asynchrone, des sauvegardes de données planifiées sont exécutées de manière asynchrone sur le deuxième centre de données. 

Dans SharePoint Online, les sauvegardes de données sont effectuées toutes les 12 heures et conservées pendant 14 jours. SharePoint Online utilise également un système de secours à chaud qui inclut des centres de données répartis géographiquement distincts au sein de la même région d'emplacement des données client (par exemple, Chicago et San Antonio pour les clients qui ont configuré leur client aux États-Unis). configuré comme actif/actif. Par exemple, il existe des utilisateurs en ligne qui ont Chicago comme Datacenter principal et San Antonio comme centre de ligne de basculement, et des utilisateurs Live qui ont San Antonio comme centre de contenu principal et Chicago comme centre de production de basculement. 