---
title: Choisir entre Mobile Device Manager pour Office 365 et Microsoft Intune
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/3/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c93d9ab9-efb2-4349-9b93-30c30562ee22
description: Microsoft Intune et gestion des périphériques mobiles intégrées à Office 365 les deux vous permettent de gérer les appareils mobiles dans votre organisation. Mais il existe des différences fondamentales, décrites dans cette rubrique.
ms.openlocfilehash: 339399e2e518c22fa9f0f7482fc527990f1a8541
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22527567"
---
# <a name="choose-between-mdm-for-office-365-and-microsoft-intune"></a>Choisir entre Mobile Device Manager pour Office 365 et Microsoft Intune

Microsoft Intune et gestion des périphériques mobiles intégrées à Office 365 les deux vous permettent de gérer les appareils mobiles dans votre organisation. Mais il existe des différences fondamentales, décrites dans le tableau suivant.
  
> [!NOTE]
> Vous pouvez gérer les utilisateurs et leurs appareils mobiles à l’aide de Intune et Office 365 dans la même organisation cliente Office 365. Configuration Intune et Mobile Device Manager vous permet de choisir la solution qui consiste le mieux à des utilisateurs spécifiques et leurs périphériques. Si vous avez deux options disponibles, vous pouvez choisir si vous gérez des périphériques d’un utilisateur avec Mobile Device Manager pour Office 365 ou la solution Intune plus riche. 
  
||||
|:-----|:-----|:-----|
|**Fonctionnalités** <br/> |**GPM pour Office 365** <br/> |**Microsoft Intune** <br/> |
|Coût  <br/> |Fourni avec le nombre d’abonnements Office 365 commerciale.  <br/> |Requiert un abonnement payant pour Microsoft Intune ou peut être acheté avec la Suite de mobilité d’entreprise.  <br/> |
|La gestion des périphériques  <br/> |Gérez des périphériques à l’aide de la [accédez à l’Office 365 Security &amp; centre de conformité](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) Office 365.  <br/> |Si vous utilisez Intune par lui-même, vous gérez des périphériques à l’aide de la console d’administration Intune.  <br/> Si vous intégrez Intune avec System Center 2012 Configuration Manager, vous utilisez la console Configuration Manager pour gérer les périphériques locaux et dans le nuage.  <br/> |
|Vous pouvez gérer des appareils  <br/> |Gestion en nuage pour iOS, Android et Windows périphériques  <br/> |Gestion en nuage pour iOS, Mac OS X, Android, Windows 8.1 (téléphone et PC) et versions ultérieures pour inclure Windows 10. <br/> |
|Fonctionnalités clés  <br/> |Garantir que les documents et messagerie d’entreprise Office 365 est accessible uniquement sur les téléphones et les tablettes qui sont gérés par votre société et qui sont compatibles avec vos stratégies informatiques.  <br/> Définir et gérer les stratégies de sécurité, comme le code confidentiel au niveau de verrouillage et jailbreak détection de périphérique, afin d’empêcher les utilisateurs non autorisés d’accéder à la messagerie d’entreprise et des données sur un périphérique lorsqu’il est perdu ou volé.  <br/> Supprimer les données d’entreprise Office 365 à partir de périphériques d’un employé tout en conservant leurs données personnelles en place.  <br/> Vous trouverez des détails dans les [fonctionnalités de gestion des périphériques mobiles intégrées à Office 365](https://support.office.com/article/a1da44e5-7475-4992-be91-9ccec25905b0).  <br/> |Mobile Device Manager pour les fonctionnalités d’Office 365, plus :  <br/> Permettent aux utilisateurs d’accéder en toute sécurité des ressources d’entreprise avec des certificats, Wi-Fi, VPN et profils de messagerie.  <br/> S’inscrire et gérer des collections de périphériques appartenant à l’entreprise, la simplification du déploiement de stratégie et d’application.  <br/> Déployer les applications dans des magasins internes line-of-business applications pour les utilisateurs.  <br/> Autoriser les utilisateurs à accéder en toute sécurité les informations d’entreprise à l’aide de l’Office mobile et ligne des applications qu’ils connaissent, tout en garantissant la sécurité des données en vous aidant à limiter les actions telles que copier, couper, coller, enregistrent en tant que, pour seulement ces applications gérées par Intune.  <br/> Activer le plus sécurisé navigation sur le web à l’aide de l’application Intune gérées navigateur.  <br/> Gérer les ordinateurs du nuage sans qu’aucune infrastructure nécessaire à l’aide de Intune ou connectez-vous Intune pour le Gestionnaire de Configuration pour gérer l’ensemble de vos périphériques, y compris les PC, Mac, Linux et UNIX serveurs et les périphériques mobiles à partir d’une console unique.  <br/> Un abonnement Intune permet également de configurer les stratégies MAM (gestion des applications mobiles) à l’aide du portail Azure, même si les périphériques de personnes ne sont pas inscrits dans Intune. Voir [protéger les données d’application à l’aide de stratégies MAM](https://go.microsoft.com/fwlink/?LinkId=825439).<br/> |


## <a name="related-topics"></a>Voir aussi
   
En savoir plus sur Microsoft Intune avec la formation vidéo [Microsoft Cloud Services : gérer Office 365 et Intune](https://support.office.com/article/c1224e20-3d49-4f40-99ee-fd0991880376.aspx), proposée par apprentissage LinkedIn.
  

