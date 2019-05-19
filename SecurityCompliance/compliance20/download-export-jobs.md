---
title: Télécharger l’exportation des travaux
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 56ed8eac259974b43ca0cd26b2bd0c339a5fc05b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155146"
---
# <a name="download-export-jobs"></a>Télécharger l’exportation des travaux

Toutes les données exportées sont ajoutées à un objet BLOB Microsoft Azure. Cela fournit plusieurs options pour gérer les données en aval. Il existe plusieurs façons d’accéder à un objet BLOB Azure. L’une des méthodes consiste à utiliser l’Explorateur de stockage Azure. Cette méthode prend en charge la connexion, la navigation et le téléchargement simples. Pour plus d’informations, reportez-vous à<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer>

1.  Pour télécharger du contenu à la fin d’une opération d’exportation, accédez à l’onglet exportations et sélectionnez un travail d’exportation.

2.  Copiez le texte dans la section «emplacements» de la fenêtre mobile.

![](../media/eDiscoExportJob.png)

3.  Ouvrez l’Explorateur de stockage Azure et cliquez sur le bouton «se connecter»

![](../media/AzureStorageConnect.png)

4.  Sélectionnez «utiliser un URI de signature d’accès partagé», puis cliquez sur suivant.

![](../media/AzureStorageConnect2.png)

5.  Collez le texte de l’emplacement dans la zone de texte URI, puis cliquez sur suivant.

![](../media/AzureStorageConnect3.png)

6.  Cliquez sur se connecter.

![](../media/AzureStorageConnect4.png)

Cette opération ajoute l’exportation en tant qu’objet dans les comptes de stockage/services SAS/conteneurs d’objets BLOB. Vous serez en mesure d’explorer l’exportation et de télécharger l’ensemble ou des parties de l’exportation.

![](../media/AzureStorageConnect5.png)