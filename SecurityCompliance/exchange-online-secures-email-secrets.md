---
title: Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/24/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
description: En plus du Centre Office 365 confiance qui fournit des informations de conformité, de confidentialité et de sécurité pour Office 365, vous voudrez peut-être savoir comment Office 365 vous aide à protéger les clés secrètes que vous fournissez dans ses centres de données. Nous utilisons une technologie appelée Gestionnaire de clé distribué (DKM).
ms.openlocfilehash: a8fe1a2c9393958a391ec69a9a476a06de8c7576
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528626"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a>Procédure de sécurisation des informations confidentielles dans votre courrier électronique dans Exchange Online

Cet article décrit la façon dont Microsoft protège les informations confidentielles figurant dans vos courriers électroniques dans ses centres de données.
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a>Comment sécurisons-nous les informations confidentielles que vous indiquez ?

En plus du Centre Office 365 confiance qui fournit des [informations de conformité pour Office 365, de confidentialité et de sécurité](https://go.microsoft.com/fwlink/?linkid=874644), vous voudrez peut-être savoir comment Office 365 vous aide à protéger les clés secrètes que vous fournissez dans ses centres de données. Nous utilisons une technologie appelée Gestionnaire de clé distribué (DKM).
  
Le Gestionnaire de clés distribuées (DKM) est une fonctionnalité côté client qui utilise un ensemble de clés secrètes pour chiffrer et déchiffrer des informations. Seuls les membres d’un groupe de sécurité spécifiques dans les services de domaine Active Directory peuvent accéder à ces clés dans le but de déchiffrer les données chiffrées par le Gestionnaire de clés distribuées. Dans Exchange Online, seuls certains comptes de service sous lesquels les processus Exchange sont exécutés font partie de ce groupe de sécurité. Dans le cadre de la procédure opérationnelle standard dans le centre de données, les informations d’identification qui font partie de ce groupe de sécurité ne sont communiquées à aucun être humain, et par conséquent aucun être humain n’a accès aux clés qui peuvent déchiffrer les informations confidentielles.
  
À des fins de débogage, de résolution des problèmes ou d’audit, un administrateur de centre de données doit demander un accès élevé pour obtenir des informations d’identification temporaires qui font partie du groupe de sécurité. Ce processus requiert plusieurs niveaux d’approbation juridique. Si l’accès est accordé, toutes les activités font l’objet d’une journalisation et d’un audit. En outre, l’accès est accordé uniquement pour un intervalle de temps défini suite auquel il expire automatiquement.
  
Pour une protection supplémentaire, la technologie DKM inclut l’archivage et la substitution de clé automatisés. Ainsi, vous pouvez continuer à accéder à votre contenu plus ancien sans devoir utiliser la même clé indéfiniment.

  
## <a name="where-does-exchange-online-make-use-of-dkm"></a>Où le Gestionnaire de clés distribuées est-il utilisé dans Exchange Online ?

Microsoft utilise le Gestionnaire de clés distribuées pour chiffrer vos informations confidentielles dans les centres de données Exchange Online. Par exemple :
  
- Les informations d’identification de compte de messagerie pour les comptes connectés. Les comptes connectés sont des comptes tiers, tels que les comptes de messagerie Hotmail, Gmail et Yahoo!.
    
- Les droits de touches racine de gestion des services (RMS). Il s’agit des clés de client qui sont que soit importés à partir de RMS Azure ou de déploiements de RMS Services de domaine Active Directory local du client qui sont utilisés pour chiffrer et déchiffrer les messages électroniques avec RMS ou Office 365 Message Encryption (OME).
    
## <a name="related-topics"></a>Voir aussi

[Chiffrement dans Office 365](encryption.md)
  
[Informations de référence technique de chiffrement dans Office 365](technical-reference-details-about-encryption.md)
  
[Service d’assurance de sécurité Office 365 &amp; centre de conformité](https://go.microsoft.com/fwlink/?linkid=874645)
  

