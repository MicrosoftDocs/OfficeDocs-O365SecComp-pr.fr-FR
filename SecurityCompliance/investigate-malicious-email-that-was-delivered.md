---
title: Rechercher et vérifier le courrier électronique malveillant qui a été remis (Office 365 Threat Intelligence)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection: M365-security-compliance
description: Apprenez à utiliser sur les menaces pour rechercher et vérifier la messagerie.
ms.openlocfilehash: c7492ccf2a7fa5d67b256264c6ed6fbdb06bcbc8
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995185"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a>Rechercher et vérifier le courrier électronique malveillant qui a été remis (Office 365 Threat Intelligence)

[Menaces Office 365](office-365-ti.md) vous permet d’étudier la question activités placer vos utilisateurs à risques et prennent des mesures pour protéger votre organisation. Par exemple, si vous faites partie de l’équipe de sécurité de votre organisation, vous pouvez rechercher et examiner les messages suspects qui ont été remis à vos utilisateurs. Pour cela, à l’aide de [Menace Explorer](get-started-with-ti.md#threat-explorer).
  
> [!IMPORTANT]
> À partir de février 2019 et présentant plusieurs mois suivant, sur les menaces Office 365 est devenu Office 365 Advanced Threat Protection Plan 2, avec les fonctionnalités de protection contre les menaces supplémentaires. Pour plus d’informations, voir [plans Office 365 avancée protection contre les menaces et les prix](https://products.office.com/exchange/advance-threat-protection) et [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
  
## <a name="before-you-begin"></a>Avant de commencer...

Assurez-vous que les conditions suivantes sont remplies :
  
- Votre organisation a des [Menaces Office 365](office-365-ti.md) et [attribuer des licences aux utilisateurs dans Office 365 pour entreprises](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).
    
- [Enregistrement d’audit d’Office 365](turn-audit-log-search-on-or-off.md) est activé pour votre organisation. 
    
- Votre organisation dispose de stratégies définies pour le blocage du courrier indésirable, les programmes malveillants, anti-hameçonnage et ainsi de suite. Voir [menaces de sécurité Office 365 la gestion &amp; centre de conformité](threat-management.md).
    
- Vous êtes un administrateur global d’Office 365, ou vous avez l’administrateur de sécurité ou le rôle de recherche et de Purge affecté de la sécurité &amp; centre de conformité. Voir [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Gérer les e-mails suspects

Les pirates peuvent être envoient du courrier à vos utilisateurs à essayer et l’hameçonnage leurs informations d’identification et accéder à votre entreprises secrets ! Pour éviter ce problème, vous devez utiliser les services de protection de menace offertes par Office 365, notamment Exchange Online Protection et protection contre les menaces avancées. Toutefois, il arrive parfois lorsqu’une personne malveillante peut envoyer du courrier électronique à vos utilisateurs contenant une URL et rendre uniquement une version ultérieure sur ce point URL vers du contenu malveillant (programme malveillant, etc.). Sinon, vous pouvez le constater trop tard qu’un utilisateur de votre organisation a été compromis et pendant que l’utilisateur a été compromis, une personne malveillante utilisé ce compte pour envoyer un message électronique à d’autres utilisateurs de votre société. Dans le cadre de nettoyage de ces deux scénarios, vous souhaiterez peut-être supprimer les messages électroniques de boîtes aux lettres de l’utilisateur. Dans les situations suivantes, vous pouvez tirer parti des menaces Explorer pour rechercher et supprimer les messages électroniques !
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Recherchez et supprimez le courrier électronique suspect qui a été remis

> [!TIP]
> [Threat Explorer](get-started-with-ti.md#threat-explorer) (également appelé Explorateur de solutions), un rapport puissant qui peut servir à plusieurs fins, telles que la recherche et suppression des messages, qui identifie l’adresse IP d’un expéditeur malveillant ou lancer un incident examinés. La procédure suivante se concentre sur l’utilisation de l’Explorateur pour rechercher et supprimer de messagerie des boîtes aux lettres des destinataires. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou de l’école pour Office 365. Vous accédez à la sécurité &amp; centre de conformité. 
    
2. Dans la navigation de gauche, cliquez sur **Gestion des menaces** \> **Explorer**.
    
3. Dans le menu Affichage, choisissez **tout le courrier**.<br/>![Utilisez le menu Affichage pour choisir entre le courrier et les rapports de contenu](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notez les étiquettes qui apparaissent dans le rapport, comme **remis**, **inconnu**ou **remis à indésirable**.<br/>![Threat Explorer affichant les données pour tous les messages](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Selon les actions qui ont été effectuées sur les messages électroniques pour votre organisation, vous pouvez voir des étiquettes supplémentaires, tels que **bloqué** ou **remplacement**).
    
5. Dans le rapport, choisissez **remis** pour afficher uniquement les messages électroniques que vous trouvez dans la boîte de réception des utilisateurs.<br/>![En cliquant sur « Remis à indésirable » supprime l’affichage de ces données](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Sous le graphique, passez en revue la liste de **courrier électronique** sous le graphique.<br/>![Sous le graphique, afficher la liste des messages électroniques qui ont été détectés](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. Dans la liste, sélectionnez un élément pour afficher plus d’informations sur ce message électronique. Par exemple, vous pouvez cliquer sur la ligne d’objet pour afficher des informations sur l’expéditeur, les destinataires, les pièces jointes et autres messages électroniques similaires.<br/>![Vous pouvez afficher des informations supplémentaires sur un élément, y compris les détails et les pièces jointes](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. Après l’affichage des informations sur les messages électroniques, sélectionnez un ou plusieurs éléments dans la liste pour activer **+ Actions**.
    
9. Utilisez la liste **+ Actions** pour appliquer une action, telles que **déplacer pour supprimer** les éléments. Cette opération supprime les messages sélectionnés de boîtes aux lettres des destinataires.<br/>![Lorsque vous sélectionnez un ou plusieurs messages électroniques, vous pouvez choisir parmi plusieurs actions disponibles](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Voir aussi

[Intelligence des menaces d’Office 365](office-365-ti.md)
  
[Se protéger contre les menaces dans Office 365](protect-against-threats.md)
  
[Afficher les rapports de Protection de menace avancées d’Office 365](view-reports-for-atp.md)
  

