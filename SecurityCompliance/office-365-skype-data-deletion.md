---
title: Office 365 Skype pour la suppression des données métiers
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
description: Une explication de la suppression des données dans Skype pour les entreprises.
ms.openlocfilehash: f3ddd0ad0797c465857919e8f7b28341492769ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528355"
---
# <a name="skype-for-business-data-deletion-in-office-365"></a>Skype pour la suppression des données métiers dans Office 365

Skype Entreprise prend en charge l'archivage des messages instantanés de pair à pair et entre plusieurs utilisateurs, et des activités de chargement de contenu dans les réunions. La fonctionnalité d'archivage requiert Exchange et est contrôlée par l'attribut Archive permanente de la boîte aux lettres Exchange de l'utilisateur, qui archive les messages électroniques et le contenu Skype Entreprise.

Tout l'archivage réalisé dans Skype Entreprise est considéré comme « archivage de niveau utilisateur », car vous l'activez et le désactivez pour un ou plusieurs utilisateurs ou groupes d'utilisateurs spécifiques en créant, configurant et appliquant une stratégie d'archivage de niveau utilisateur à ces utilisateurs. Il n'existe aucun contrôle direct des paramètres d'archivage à partir du Centre d'administration Skype Entreprise.

Les types de contenu suivants ne sont pas archivés dans Skype pour les entreprises : 
- Transferts de fichiers pair à pair
- Audio/vidéo pour les messages instantanés et conférences pair à pair
- Partage d'applications pour les messages instantanés et les conférences pair à pair
- Annotations de conférence 

## <a name="meeting-content-retention"></a>Rétention de contenu de réunion
Les clients qui utilisent Skype pour les entreprises peuvent télécharger le contenu à un Skype pour la réunion d’entreprise en tant que pièces jointes, telles que des présentations PowerPoint, les fichiers OneNote et autres fichiers. La période de rétention pour le contenu qui a été téléchargé vers une réunion est la suivante :
- **Réunion unique** - contenu est conservé pendant 15 jours à partir du moment où la dernière personne quitte la réunion.
- **Réunion périodique** - contenu est conservé pendant 15 jours après que la dernière personne quitte la dernière session de la réunion. Le minuteur de rétention réinitialise si un utilisateur connecte à la même session de conférence dans 15 jours. Par exemple, supposons qu'un Skype pour une réunion d’affaires est planifiée chaque semaine pour une année, et un fichier est téléchargé vers la réunion au cours de la première instance. Si au moins une personne rejoint la session de conférence toutes les semaines, le fichier est conservé dans Skype pour les serveurs d’entreprise en ligne pour l’ensemble de l’année plus 15 jours après que la dernière personne quitte la dernière réunion de la série.
- Contenu de la **réunion Conférence maintenant** - est conservé pendant 8 heures après l’heure de fin de la réunion.

> [!NOTE]
> Si un utilisateur sans licence désactivé (par exemple, si **msRTCSIP-userenabled** est définie sur *False*) et puis renouveler une licence ou réactivée, contenu de la réunion n’est pas conservé.

## <a name="meeting-expiration"></a>Expiration de réunion
Les utilisateurs peuvent accéder à une réunion spécifique après la fin, sous réserve des périodes d’expiration suivantes :
- **Réunion unique** - réunion expire 14 jours après l’heure de fin de la réunion planifiée.
- **Réunion périodique avec date de fin** - réunion expire 14 jours après l’heure de fin prévue de la dernière occurrence de réunion.
- **Réunion Conférence maintenant** - réunion expire au bout de 8 heures.

## <a name="whiteboard-collaboration"></a>Collaboration avec tableau blanc
Les annotations effectuées sur des tableaux blancs seront visible par tous les participants. Lorsque vous enregistrez un tableau blanc, le tableau blanc et toutes les annotations seront stockées sur un Skype pour Business server, et il sera conservé sur le serveur en fonction des stratégies d’expiration du contenu de réunion définis par l’administrateur.

## <a name="audio-test-service"></a>Service de Test audio
Un exemple de short (environ 5 secondes) de votre voix est enregistré lors de l’appel du Service de Test Audio. L’exemple de voix est utilisée par vous permettent de vérifier et/ou de vérifier la qualité du son de votre Skype pour l’appel d’entreprise en fonction de la qualité de l’enregistrement. Lorsque l’appel de Service de Test Audio se termine, l’exemple de voix est supprimé.

## <a name="persistent-group-chat"></a>Conversation de groupe persistante
Conversation de groupe permanent stocke le contenu de conversation de groupe. Si activé, l’administrateur peut contrôler la période de rétention, le serveur sur lequel ces informations sont stockées, si l’historique de conversation de groupe est archivé en conformité ou à d’autres fins et toutes les propriétés sur une salle de gérer/modifier. Les utilisateurs avec différents rôles ont accès différent pour les données persistantes, comme suit :
- Les administrateurs peuvent supprimer les ancien contenu (par exemple, le contenu publié avant une date donnée) à partir d’une salle de conversation pour conserver la taille de la base de données de grandir considérablement. Ou bien, ils peuvent supprimer ou remplacer les messages inapproprié pour une salle de conversation donnée (ou considéré comme inapproprié).
- Les utilisateurs finaux, y compris les auteurs de messages, ne peut pas supprimer du contenu à partir d’une salle de conversation.
- Responsables de salle de conversation peuvent désactiver les salles mais ne peut pas supprimer les salles. Seuls les administrateurs peuvent supprimer une salle de conversation après sa création.