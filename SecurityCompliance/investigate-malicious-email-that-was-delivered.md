---
title: Rechercher et identifier les courriers électroniques malveillants remis dans Office 365
keywords: TIMailData-Inline, incident de sécurité, incident, PowerShell ATP, programmes malveillants de messagerie, utilisateurs compromis, hameçonnage par courrier électronique, programmes malveillants de messagerie, lire les en-têtes de courrier électronique, lire les en-têtes, lire les en-têtes de messages électroniques
ms.author: tracyp
author: msfttracyp
manager: dansimp
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
ms.openlocfilehash: 59f0a678b2f91351e9f11987d17acb3b87e4239d
ms.sourcegitcommit: ff370e93b792204547694139ef99bc0848304570
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2019
ms.locfileid: "36852786"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-in-office-365"></a>Rechercher et identifier les courriers électroniques malveillants remis dans Office 365

[Office 365 Advanced Threat Protection](office-365-atp.md) vous permet d’examiner les activités qui permettent de mettre en péril les personnes de votre organisation et de protéger votre organisation. Par exemple, si vous participez à l’équipe de sécurité de votre organisation, vous pouvez rechercher et enquêter sur les messages électroniques suspects qui ont été remis. Vous pouvez le faire à l’aide de l' [Explorateur de menaces (ou des détections en temps réel)](threat-explorer.md).
  
## <a name="before-you-begin"></a>Avant de commencer...

Assurez-vous que les conditions suivantes sont remplies :
  
- Votre organisation dispose d' [Office 365 protection avancée contre les menaces](office-365-atp.md) et des [licences sont attribuées aux utilisateurs](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).
    
- La [journalisation d’audit Office 365](turn-audit-log-search-on-or-off.md) est activée pour votre organisation. 
    
- Votre organisation a défini des stratégies pour le blocage du courrier indésirable, anti-programme malveillant, anti-hameçonnage, etc. Consultez la rubrique [Protégez-vous contre les menaces dans Office 365](protect-against-threats.md).
    
- Vous êtes un administrateur général Office 365 ou vous avez l’administrateur de sécurité ou le rôle de recherche et de purge affecté dans le centre &amp; de sécurité et de conformité. Consultez [la rubrique autorisations dans le centre &amp; de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md). Pour certaines actions, vous devez également avoir un nouveau rôle aperçu affecté. 

#### <a name="preview-role-permissions"></a>Aperçu des autorisations de rôle

Pour effectuer certaines actions, telles que l’affichage des en-têtes de message ou le téléchargement du contenu d’un message électronique, vous devez disposer d’un nouveau rôle appelé *Aperçu* ajouté à un autre groupe de rôles Office 365 approprié. Le tableau suivant clarifie les rôles et les autorisations requis.

|Activité  |Groupe de rôles |Prévisualiser le rôle nécessaire ?  |
|---------|---------|---------|
|Utilisation de l’Explorateur de menaces (et des détections en temps réel) pour analyser les menaces     |Administrateur général Office 365 <br> Administrateur de sécurité <br> Lecteur de sécurité     | Non   |
|Utiliser l’Explorateur de menaces (et les détections en temps réel) pour afficher les en-têtes des messages électroniques, ainsi que pour afficher un aperçu et télécharger des messages électroniques mis en quarantaine    |Administrateur général Office 365 <br> Administrateur de sécurité <br>Lecteur de sécurité   |       Non  |
|Utiliser l’Explorateur de menaces pour afficher les en-têtes et télécharger les messages électroniques remis aux boîtes aux lettres     |Administrateur général Office 365 <br>Administrateur de sécurité <br> Lecteur de sécurité <br> Aperçu   |   Oui      |

> [!NOTE]
> L' *Aperçu* est un rôle et non un groupe de rôles ; le rôle aperçu doit être ajouté à un groupe de rôles existant pour Office 365. Le rôle administrateur général Office 365 est affecté au centre d’administration Microsoft 365[https://admin.microsoft.com](https://admin.microsoft.com)(), et les rôles Administrateur de sécurité et lecteur de sécurité sont affectés dans le centre de sécurité &[https://protection.office.com](https://protection.office.com)de sécurité Office 365 (). Pour en savoir plus sur les rôles et les autorisations, consultez [la rubrique autorisations dans le centre de sécurité & conformité d’Office 365](permissions-in-the-security-and-compliance-center.md).

## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Rechercher et supprimer les e-mails suspects qui ont été remis

L’Explorateur de menaces est un rapport puissant qui peut servir plusieurs objectifs, tels que la recherche et la suppression de messages, l’identification de l’adresse IP d’un expéditeur de courrier malveillant ou le démarrage d’un incident en vue d’une nouvelle enquête. La procédure suivante décrit l’utilisation de l’Explorateur pour rechercher et supprimer des courriers électroniques malveillants provenant de boîtes aux lettres de destinataires.

1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou scolaire pour Office 365. Vous accédez au centre de sécurité &amp; conformité. 
    
2. Dans le volet de navigation de gauche, choisissez **Explorateur**de **gestion** \> des menaces.

    ![Explorateur avec les champs d’action de remise et d’emplacement de remise.](media/ThreatExFields.PNG)

    Vous remarquerez peut-être la nouvelle colonne **actions spéciales** . Cette fonctionnalité vise à indiquer aux administrateurs le résultat du traitement d’un message électronique. La colonne **actions spéciales** est accessible au même endroit que l' **action de remise** et l’emplacement de **remise**. Les actions spéciales peuvent être mises à jour à la fin de la chronologie du courrier électronique de l’Explorateur de menaces, qui est une nouvelle fonctionnalité visant à améliorer l’expérience de la chasse des administrateurs.

3. Pour afficher une chronologie par courrier électronique, cliquez sur l’objet d’un message électronique, puis cliquez sur **chronologie du courrier électronique**. (Il apparaît dans les autres en-têtes, tels que **Résumé** ou **Détails**.)

    Une fois que vous avez ouvert la chronologie du courrier, vous devez voir un tableau indiquant les événements de post-remise pour ce message. S’il n’y a pas d’autres événements pour le courrier électronique, vous devriez voir un seul événement pour la remise d’origine qui indique un résultat comme **bloqué** avec un verdict comme **hameçonnage**. L’onglet permet également d’exporter toute la chronologie du courrier électronique, ce qui exporte tous les détails de l’onglet et les détails de l’e-mail (par exemple, l’objet, l’expéditeur, le destinataire, le réseau et l’ID du message).

    La chronologie du courrier diminue en fonction de la randomisation, car il y a moins de temps passé à vérifier différents emplacements pour essayer de comprendre les événements qui se sont produits depuis que le courrier électronique est arrivé. Lorsque plusieurs événements se produisent à la même heure ou proches de celle-ci dans un message électronique, ces événements apparaissent dans un affichage chronologie. 
    
    Certains événements qui ont lieu après la livraison de votre courrier sont capturés dans la colonne **actions spéciales** . Le fait de combiner les informations de la chronologie du courrier électronique avec les actions spéciales prises lors de la remise après envoi permet aux administrateurs de savoir comment fonctionnent leurs stratégies, où le courrier électronique a été finalement routé et, dans certains cas, ce qu’est l’évaluation finale. 

4. Dans le menu **affichage** , choisissez **tous les messages électroniques**.

    ![Utiliser le menu Affichage pour choisir entre les rapports de courrier électronique et de contenu](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
    Notez les étiquettes qui apparaissent dans le rapport, telles que **remis**, **inconnu**ou **remis au courrier indésirable**.

    ![Explorateur de menaces affichant les données de tous les messages électroniques](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)
    
    (En fonction des actions effectuées sur les messages électroniques de votre organisation, vous pouvez voir d’autres étiquettes, telles que **bloqué** ou **remplacé**.)
    
6. Dans le rapport, choisissez **remis** pour afficher uniquement les messages électroniques qui se sont terminés dans les boîtes de réception des utilisateurs.

    ![Le fait de cliquer sur « remis au courrier indésirable » supprime ces données de l’affichage](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
7. Sous le graphique, passez en revue la liste des **messages** sous le graphique.

    ![Sous le graphique, affichez la liste des messages électroniques qui ont été détectés.](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
8. Dans la liste, choisissez un élément pour afficher plus d’informations sur ce message électronique. Par exemple, vous pouvez cliquer sur la ligne d’objet pour afficher des informations sur l’expéditeur, les destinataires, les pièces jointes et d’autres messages électroniques similaires.

    ![Vous pouvez afficher des informations supplémentaires sur un élément](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
9. Après avoir consulté les informations sur les messages électroniques, sélectionnez un ou plusieurs éléments de la liste à activer **+ actions**.
    
10. Utilisez la liste **+ actions** pour appliquer une action, telle que **déplacer vers** les éléments supprimés. Cette option supprime les messages sélectionnés des boîtes aux lettres des destinataires.

    ![Lorsque vous sélectionnez un ou plusieurs messages électroniques, vous pouvez choisir parmi plusieurs actions disponibles.](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)

## <a name="dealing-with-suspicious-email-messages"></a>Traitement des messages électroniques suspects

Les utilisateurs malveillants peuvent envoyer des courriers électroniques à des personnes de votre organisation dans le but d’hameçoniser leurs informations d’identification et d’accéder à vos secrets d’entreprise. Pour éviter cela, vous utilisez les services de protection contre les menaces dans Office 365, y compris [Exchange Online Protection](eop/exchange-online-protection-overview.md) et [Advanced Threat Protection](office-365-atp.md). Toutefois, il arrive parfois qu’un utilisateur malveillant envoie un courrier électronique contenant un lien (URL) qui pointe uniquement vers du contenu malveillant (par exemple, un programme malveillant). Vous pouvez également vous rendre compte que la personne de votre organisation a été compromise, et qu’elle a été compromise, un agresseur a utilisé son compte pour envoyer des courriers électroniques à d’autres personnes de votre organisation. Dans le cadre de l’un de ces scénarios, vous pouvez supprimer les messages électroniques suspects des boîtes de réception des utilisateurs. Pour ce faire, vous pouvez utiliser l' [Explorateur de menaces](threat-explorer.md).

## <a name="finding-re-routed-email-messages-after-actions-are-taken"></a>Recherche de messages électroniques redirigés après la prise d’actions

L’Explorateur de menaces fournit à votre équipe des opérations de sécurité les informations dont il a besoin pour enquêter sur le courrier électronique suspect. Votre équipe des opérations de sécurité peut :

- [Afficher les en-têtes des messages et télécharger le corps du message](#view-the-email-headers-and-download-the-email-body) 

- [Vérifier l’action de remise et l’emplacement](#check-the-delivery-action-and-location)

- [Affichage de la chronologie de votre courrier électronique](#view-the-timeline-of-your-email)

### <a name="view-the-email-headers-and-download-the-email-body"></a>Afficher les en-têtes des messages et télécharger le corps du message

La possibilité d’afficher un aperçu des en-têtes des messages et de télécharger le corps d’un message est une fonctionnalité puissante dans l’Explorateur de menaces. Les [autorisations](permissions-in-the-security-and-compliance-center.md) appropriées doivent être attribuées. Voir [aperçu des autorisations de rôle](#preview-role-permissions).

Pour accéder à vos options d’en-tête et de téléchargement de messagerie, procédez comme suit : 

1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous à l’aide de votre compte professionnel ou scolaire pour Office 365. Vous accédez au centre de sécurité &amp; conformité. 
    
2. Dans le volet de navigation de gauche, choisissez **Explorateur**de **gestion** \> des menaces.

3. Cliquez sur un objet dans le tableau Threat Explorer. 

    Cette opération ouvre le lanceur, dans lequel les liens de l’aperçu de l’en-tête et du téléchargement du courrier électronique sont positionnés.

    ![Menu volant de l’Explorateur de menaces avec les liens télécharger et aperçu sur la page.](media/ThreatExplorerDownloadandPreview.PNG)

> [!IMPORTANT]
> Cette fonctionnalité ne s’affiche pas pour les messages électroniques qui n’ont jamais été trouvés dans la boîte aux lettres d’un utilisateur, ce qui peut se produire si un e-mail a été abandonné ou si sa remise a échoué. Dans les cas où les messages électroniques ont été supprimés des boîtes aux lettres des utilisateurs, les administrateurs voient s’afficher un message d’erreur « courrier introuvable ».

### <a name="check-the-delivery-action-and-location"></a>Vérifier l’action de remise et l’emplacement

Dans l' [Explorateur de menaces (et les détections en temps réel)](threat-explorer.md), **vous disposez maintenant** de colonnes de l’adresse de remise et d' **emplacement de remise** au lieu de l’ancienne colonne d’état de **remise** . Cela permet d’obtenir une image plus complète de l’emplacement de vos messages électroniques. Une partie de cette modification consiste à faciliter la chasse aux opérations de sécurité, mais le résultat net est en connaissance de cause en un clin d’œil sur l’emplacement des messages électroniques problématiques.

L’état de remise est désormais divisé en deux colonnes :

- **Action de remise** : quel est le statut de ce courrier électronique ?

- **Emplacement de remise** : où ce message électronique a-t-il été routé ?

L’action de remise est l’action entreprise sur un courrier électronique en raison de stratégies ou de détections existantes. Voici les actions possibles qu’un courrier électronique peut effectuer :

- **Remis** : le courrier électronique a été remis à la boîte de réception ou au dossier d’un utilisateur et l’utilisateur peut y accéder directement.

- **Courrier indésirable** – le courrier électronique a été envoyé vers le dossier de courrier indésirable de l’utilisateur ou le dossier supprimé, et l’utilisateur a accès aux messages électroniques dans son dossier de courrier indésirable ou supprimé.

- **Bloqué** : tous les messages électroniques mis en quarantaine, qui ont échoué ou qui ont été supprimés. (Cette inaccessibilité est entièrement inaccessible par l’utilisateur.)

- **Remplacé** : tout message électronique où des pièces jointes malveillantes sont remplacées par des fichiers. txt qui indiquent que la pièce jointe était malveillante.
 
Emplacement de remise : affiche les résultats des stratégies et des détections qui exécutent une post-remise. Elle est liée à une action de remise. Ce champ a été ajouté pour permettre de mieux comprendre l’action entreprise lors de la détection d’un message problématique. Voici les valeurs possibles de l’emplacement de remise :

- **Boîte de réception ou dossier** : le courrier électronique se trouve dans la boîte de réception ou dans un dossier (en fonction de vos règles de messagerie électronique).

- **Local ou externe** : la boîte aux lettres n’existe pas sur le Cloud, mais elle est locale.

- **Dossier courrier indésirable** : le courrier électronique se trouve dans le dossier de courrier indésirable d’un utilisateur.

- **Dossier éléments supprimés** : le courrier électronique se trouve dans le dossier éléments supprimés d’un utilisateur.

- **Quarantaine** – message en quarantaine, pas dans la boîte aux lettres d’un utilisateur.

- **Échec** : la messagerie n’a pas pu atteindre la boîte aux lettres.

- **Ignoré** : le courrier électronique est perdu dans le flux de messagerie.

### <a name="view-the-timeline-of-your-email"></a>Affichage de la chronologie de votre courrier électronique
  
La **chronologie par courrier électronique** est un champ dans l’Explorateur de menaces qui facilite la chasse à votre équipe des opérations de sécurité. Lorsque plusieurs événements se produisent ou se ferment à la même heure dans un e-mail, ces événements apparaissent dans un affichage chronologie. Certains événements qui ont lieu après la livraison à la messagerie sont capturés dans la colonne **actions spéciales** . La combinaison des informations de la chronologie d’un message électronique avec toutes les actions spéciales effectuées après la livraison permet aux administrateurs de mieux comprendre les stratégies et la gestion des menaces (par exemple, l’endroit où le courrier a été acheminé et, dans certains cas, l’évaluation finale).
  
## <a name="related-topics"></a>Sujets associés

[Office 365 protection avancée contre les menaces](office-365-ti.md)
  
[Se protéger contre les menaces dans Office 365](protect-against-threats.md)
  
[Afficher les rapports pour Office 365 protection avancée contre les menaces](view-reports-for-atp.md)
  

