---
title: FAQ sur l'administration déléguée
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d6a87ce8-2c22-433a-b430-5eab14f6afdc
description: Cette rubrique contient des questions fréquemment posées et la réponse à ces questions pour les partenaires et les revendeurs Microsoft qui veulent effectuer des tâches d'administration Office 365 déléguée, y compris la capacité à gérer Exchange Online Protection (EOP) pour d'autres locataires (entreprises).
ms.openlocfilehash: b6096e835f90a0d5f22a39a5df76e52f1a25a79d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027491"
---
# <a name="delegated-administration-faq"></a>FAQ sur l'administration déléguée

Cette rubrique contient des questions fréquemment posées et la réponse à ces questions pour les partenaires et les revendeurs Microsoft qui veulent effectuer des tâches d'administration Office 365 déléguée, y compris la capacité à gérer Exchange Online Protection (EOP) pour d'autres locataires (entreprises).
  
 **Q. Je suis revendeur et je dois gérer les locataires de mon client. Comment cela fonctionne-t-il ?**
  
R. Si vous êtes un partenaire ou un revendeur Microsoft et que vous vous êtes inscrit pour devenir gestionnaire Microsoft, vous pouvez demander l'autorisation d'administrer ses locataires dans le Centre d'administration Office 365. C'est ce qu'on appelle l'administration déléguée. Elle vous permet de gérer son locataire Office 365 (notamment les paramètres EOP) comme si vous étiez administrateur au sein de son organisation Les étapes permettant d'effectuer une administration déléguée sont les suivantes :
  
1. Inscrivez-vous pour devenir [partenaire Microsoft Office 365](https://aka.ms/cloudbenefits).
    
2. Inscrivez-vous à l'administration déléguée Office 365. Avant que vous puissiez administrer le compte d'un client, celui-ci doit vous fournir les autorisations d'administrateur délégué. Pour obtenir leur approbation, vous devez d'abord [leur envoyer une offre d'administration déléguée](https://go.microsoft.com/fwlink/?LinkId=396829). (Vous pouvez également proposer l'administration déléguée à votre client ultérieurement.) 
    
3. Créez le compte d'administrateur délégué à l'aide des étapes répertoriées dans l'article [Ajouter ou supprimer des relations de partenariat](https://go.microsoft.com/fwlink/?LinkId=396831).
    
Consultez l'article [Partenaires : développez votre activité et gérez votre compte Office 365](https://go.microsoft.com/fwlink/?LinkId=301485) pour plus d'informations sur la configuration d'une administration déléguée Office 365. 
  
 **Q. Je suis un client, pas un revendeur, comment puis-je configurer un administrateur délégué pour mes sous-locataires ?**
  
R. Pour le moment, l'administration déléguée est uniquement disponible pour les revendeurs et les partenaires. Cependant, nous avons fourni un exemple de script Windows PowerShell qui vous aidera à appliquer des stratégies à vos sous-locataires (entreprises). Pour plus d'informations, voir [Exemple de script pour l'application de paramètres EOP à plusieurs locataires](sample-script-for-applying-eop-settings-to-multiple-tenants.md).
  
 **Q. Puis-je empêcher mon administration de sous-locataires de modifier ma stratégie ?**
  
R. Office 365 ne dispose actuellement pas de cette fonctionnalité.
  
 **Q. Puis-je disposer de la création de rapports consolidés dans l'ensemble de mes sous-locataires ?**
  
R. La création de rapports consolidés dans l'ensemble des entreprises que vous gérez n'est pas disponible pour les rapports du Centre d'administration Office 365 pour le moment. Cependant, vous pouvez créer des rapports via Windows PowerShell distant ou le [service web de création de rapports Office 365](https://go.microsoft.com/fwlink/?LinkId=279926). 
  

