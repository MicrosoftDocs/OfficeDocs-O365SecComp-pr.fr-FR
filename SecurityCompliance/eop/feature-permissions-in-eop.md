---
title: Autorisations des fonctionnalités dans EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/30/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 34674847-a6b7-4a7e-9eaa-b64f22bc150d
description: Les autorisations nécessaires à l'exécution de tâches de gestion de Microsoft Exchange Online Protection (EOP) varient selon les fonctionnalités gérées.
ms.openlocfilehash: fe39403e60664b0340f01070ccec22b674b5bc62
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027471"
---
# <a name="feature-permissions-in-eop"></a>Autorisations des fonctionnalités dans EOP

Les autorisations nécessaires à l'exécution de tâches de gestion de Microsoft Exchange Online Protection (EOP) varient selon les fonctionnalités gérées. 
  
Pour configurer EOP, vous devez être un administrateur global Office 365 ou un administrateur d'entreprise Exchange (le groupe de rôles Gestion de l'organisation).
  
## <a name="exchange-online-protection-permissions"></a>Autorisations Exchange Online Protection

Consultez le tableau suivant afin de déterminer les autorisations requises pour gérer les fonctionnalités EOP. Si une fonctionnalité affiche plusieurs groupes de rôles, seul l'un de ces groupes de rôles doit vous être attribué pour que vous puissiez exploiter cette même fonctionnalité.
  
|**Fonctionnalité**|**Autorisations requises**|
|:-----|:-----|
|Ant-programme malveillant  <br/> |[Gestion de l'organisation](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Anti-spam  <br/> |[Gestion de l'organisation](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Gestion de l'hygiène](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Règles de flux de messagerie  <br/> |[Gestion de l'organisation](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Records Management](http://technet.microsoft.com/library/0e0c95ce-6109-4591-b86d-c6cfd44d21f5.aspx) <br/> |
|Domaines  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> |
|Protection contre les menaces avancées (DAV)  <br/> |[Gestion de l'organisation](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Gestion de l'hygiène](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Connecteurs Office 365  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> |
|Suivi des messages  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> |
|Configuration de l'organisation  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> |
|Mise en quarantaine  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Utilisateurs, contacts et groupes de rôles  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Groupes de sécurité et groupes de distribution  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Affichage des rapports  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) : les utilisateurs ont accès aux rapports de protection du courrier électronique.  <br/> [View-Only Recipients](http://technet.microsoft.com/library/37e66b92-81d3-412f-b7a9-e1bb8cbeb468.aspx) : les utilisateurs ont accès aux rapports de protection du courrier électronique.  <br/> [Compliance Management](http://technet.microsoft.com/library/b91b23a4-e9c7-4bd0-9ee3-ec5cb498da15.aspx) : les utilisateurs ont accès aux rapports de protection du courrier électronique et aux rapports de protection contre la perte de données (si leur abonnement comprend les fonctionnalités associées).  <br/> |
   

