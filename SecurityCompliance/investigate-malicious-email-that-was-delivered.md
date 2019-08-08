---
title: Rechercher et identifier les courriers électroniques malveillants remis dans Office 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 08/07/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: Découvrez comment utiliser les fonctionnalités d’analyse et de réponse aux menaces pour rechercher et examiner des courriers électroniques malveillants.
ms.openlocfilehash: 1f558614d77577408a824b3c6181aae22753ab0f
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230558"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-in-office-365"></a>Rechercher et identifier les courriers électroniques malveillants remis dans Office 365

[Office 365 Advanced Threat Protection](office-365-atp.md) vous permet d’examiner les activités qui permettent aux utilisateurs de protéger votre organisation. Par exemple, si vous participez à l’équipe de sécurité de votre organisation, vous pouvez rechercher et enquêter sur les messages électroniques suspects qui ont été remis à vos utilisateurs. Vous pouvez le faire à l’aide de l' [Explorateur de menaces (ou des détections en temps réel)](threat-explorer.md).
  
## <a name="before-you-begin"></a>Avant de commencer...

Assurez-vous que les conditions suivantes sont remplies :
  
- Votre organisation dispose d' [Office 365 protection avancée contre les menaces](office-365-atp.md) et des [licences sont attribuées aux utilisateurs](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).
    
- La [journalisation d’audit Office 365](turn-audit-log-search-on-or-off.md) est activée pour votre organisation. 
    
- Votre organisation a défini des stratégies pour le blocage du courrier indésirable, anti-programme malveillant, anti-hameçonnage, etc. Consultez la rubrique Protégez-vous [contre les menaces dans Office 365](protect-against-threats.md).
    
- Vous êtes un administrateur général Office 365 ou vous avez l’administrateur de sécurité ou le rôle de recherche et de purge affecté dans le centre &amp; de sécurité et de conformité. Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Traitement des e-mails suspects

Les utilisateurs malveillants peuvent envoyer des courriers électroniques à vos utilisateurs pour essayer d’envoyer leurs informations d’identification et accéder à vos secrets d’entreprise. Pour éviter cela, vous devez utiliser les services de protection contre les menaces dans Office 365, y compris [Exchange Online Protection](eop/exchange-online-protection-overview.md) et [Advanced Threat Protection](office-365-atp.md). Toutefois, il arrive qu’un agresseur puisse envoyer un message électronique à vos utilisateurs contenant une URL et, par la suite, faire pointer cette URL vers du contenu malveillant (programmes malveillants, etc.). Par ailleurs, vous pouvez vous rendre compte que l’utilisateur de votre organisation a été compromis et que, pendant qu’il a été compromis, un utilisateur malveillant a utilisé ce compte pour envoyer des courriers électroniques à d’autres utilisateurs de votre entreprise. Dans le cadre du nettoyage de ces deux scénarios, vous souhaiterez peut-être supprimer les messages électroniques des boîtes de réception des utilisateurs. Dans ce cas, vous pouvez utiliser l' [Explorateur de menaces (ou les détections en temps réel)](threat-explorer.md) pour rechercher et supprimer ces messages électroniques.

## <a name="where-re-routed-emails-are-located-after-actions-are-taken"></a>Où se trouvent les messages électroniques reroutés une fois les actions effectuées

L’Explorateur de menaces les détections en temps réel ont ajouté les champs de l’action de remise et de l’emplacement de remise au lieu de l’état de remise. Cela a pour effet d’obtenir une image plus complète de l’emplacement de vos courriers électroniques. Une partie de cette modification est de faciliter la chasse aux personnes qui effectuent des opérations de sécurité, mais le résultat net est de savoir en un clin d’œil l’emplacement des messages électroniques problématiques.

L’état de remise est désormais divisé en deux colonnes:

- **Action de remise** : quel est le statut de ce courrier électronique?
- **Emplacement de remise** : où ce message électronique a-t-il été routé?

L’action de remise est l’action entreprise sur un courrier électronique en raison de stratégies ou de détections existantes. Voici les actions possibles qu’un courrier électronique peut effectuer:

- **Remis** : le courrier électronique a été remis à la boîte de réception ou au dossier d’un utilisateur et l’utilisateur peut y accéder directement.
- **Courrier** indésirable – le courrier électronique a été envoyé vers le dossier de courrier indésirable de l’utilisateur ou le dossier supprimé, et l’utilisateur a accès aux courriers électroniques dans son dossier de courrier indésirable ou supprimé.
- **Bloqué** : tous les messages électroniques mis en quarantaine, qui ont échoué ou qui ont été supprimés. Cette inaccessibilité est entièrement inaccessible par l’utilisateur.
- **Remplacé** : tout message électronique où des pièces jointes malveillantes sont remplacées par des fichiers. txt qui indiquent que la pièce jointe était malveillante.
 
Emplacement de remise: affiche les résultats des stratégies et des détections qui exécutent une post-remise. Elle est liée à une action de remise. Ce champ a été ajouté pour permettre de mieux comprendre l’action entreprise lors de la détection d’un message problématique. Voici les valeurs possibles de l’emplacement de remise:

- **Boîte de réception ou dossier** : le courrier électronique se trouve dans la boîte de réception ou dans un dossier (en fonction de vos règles de messagerie électronique).
- **Local ou externe** : la boîte aux lettres n’existe pas sur le Cloud, mais elle est locale.
- **Dossier courrier** indésirable – courrier électronique dans le dossier courrier indésirable d’un utilisateur.
- **Dossier éléments supprimés** : le courrier électronique dans le dossier éléments supprimés d’un utilisateur.
- **Quarantaine** : message en quarantaine et absent de la boîte aux lettres d’un utilisateur.
- **Échec** : la messagerie n’a pas pu atteindre la boîte aux lettres.
- **Ignoré** : le courrier électronique est perdu dans le flux de messagerie.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Rechercher et supprimer les e-mails suspects qui ont été remis

> [!TIP]
> L’Explorateur de menaces (parfois appelé Explorateur) est un rapport puissant qui peut servir plusieurs objectifs, tels que la recherche et la suppression de messages, l’identification de l’adresse IP d’un expéditeur de courrier malveillant ou le démarrage d’un incident en vue d’une nouvelle enquête. La procédure suivante décrit l’utilisation de l’Explorateur pour rechercher et supprimer des courriers électroniques malveillants provenant de boîtes aux lettres de destinataires.

Pour afficher les modifications apportées au champ d’état de remise précédent (à présent, action de remise et emplacement de remise): 

1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou scolaire pour Office 365. Vous accédez au centre de sécurité &amp; conformité. 
    
2. Dans le volet de navigation de gauche, choisissez **Explorateur**de **gestion** \> des menaces.


![Explorateur de menaces avec les champs d’action de remise et d’emplacement de remise.](media/ThreatExFields.PNG)

Vous remarquerez peut-être la nouvelle colonne «actions spéciales» dans ce graphique. Cette fonctionnalité vise à indiquer aux administrateurs le résultat du traitement d’un message électronique. Les actions spéciales peuvent être mises à jour à la fin de la *chronologie du courrier électronique*de l’Explorateur de menaces, qui est une nouvelle fonctionnalité visant à améliorer l’expérience de la chasse des administrateurs.

La chronologie par courrier électronique diminue en fonction de la randomisation, car il y a moins de temps passé à vérifier différents emplacements pour essayer de comprendre les événements qui se sont produits depuis que le courrier électronique est arrivé. Lorsque plusieurs événements se produisent à la même heure ou proches de celle-ci dans un e-mail, ces événements apparaissent dans un affichage chronologie. Certains événements qui ont lieu après la livraison de votre courrier seront capturés dans la colonne «actions spéciales». Le fait de combiner les informations de la chronologie du courrier *électronique* de ce message avec les *actions spéciales* prises lors de la livraison post-remise permettra aux administrateurs de mieux comprendre le fonctionnement de leurs stratégies, où le courrier a été finalement routé et, dans certains cas, ce qu’est le final l’évaluation était. La colonne actions spéciales est accessible au même endroit que l’action de remise et l’emplacement de remise, mais pour afficher une chronologie par courrier électronique:

1. Cliquez sur l’objet du message électronique.
2. Dans le panneau qui s’affiche, cliquez sur *chronologie du courrier électronique*. (Il apparaîtra dans les autres en-têtes, comme «résumé» ou «détails», et cetera.)

Une fois que vous avez ouvert la chronologie du courrier, vous devez voir un tableau indiquant les événements de post-remise pour ce message ou, en l’absence d’autres événements pour le courrier, vous devriez voir un seul événement pour la remise d’origine qui indiquera un résultat comme *bloqué* . avec un verdict comme le *hameçonnage*. L’onglet permet également d’exporter l’intégralité de la chronologie du courrier électronique, ce qui permet d’exporter tous les détails de l’onglet et les détails de l’e-mail (par exemple, l’objet, l’expéditeur, le destinataire, le réseau et l’ID du message).

3. Dans le menu Affichage, choisissez **tous les messages électroniques**.<br/>![Utiliser le menu Affichage pour choisir entre les rapports de courrier électronique et de contenu](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notez les étiquettes qui apparaissent dans le rapport, telles que **remis**, **inconnu**ou **remis au courrier**indésirable.<br/>![Explorateur de menaces affichant les données de tous les messages électroniques](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(En fonction des actions effectuées sur les messages électroniques de votre organisation, vous pouvez voir des étiquettes supplémentaires, telles que **bloqué** ou **remplacé**.)
    
5. Dans le rapport, choisissez **remis** pour afficher uniquement les courriels qui se sont terminés dans les boîtes de réception des utilisateurs.<br/>![Le fait de cliquer sur «remis au courrier indésirable» supprime ces données de l’affichage](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Sous le graphique, passez en revue la liste des **messages** sous le graphique.<br/>![Sous le graphique, affichez la liste des messages électroniques qui ont été détectés.](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. Dans la liste, choisissez un élément pour afficher plus d’informations sur ce message électronique. Par exemple, vous pouvez cliquer sur la ligne d’objet pour afficher des informations sur l’expéditeur, les destinataires, les pièces jointes et d’autres messages électroniques similaires.<br/>![Vous pouvez afficher des informations supplémentaires sur un élément, notamment des détails et des pièces jointes.](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. Après avoir consulté les informations sur les messages électroniques, sélectionnez un ou plusieurs éléments de la liste à activer **+ actions**.
    
9. Utilisez la liste **+ actions** pour appliquer une action, telle que **déplacer vers** les éléments supprimés. Cette opération supprime les messages sélectionnés des boîtes aux lettres des destinataires.<br/>![Lorsque vous sélectionnez un ou plusieurs messages électroniques, vous pouvez choisir parmi plusieurs actions disponibles.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Sujets associés

[Plan 2 de protection avancée contre les menaces Office 365](office-365-ti.md)
  
[Se protéger contre les menaces dans Office 365](protect-against-threats.md)
  
[Afficher les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md)
  

