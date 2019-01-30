---
title: Créer une notification de conservation légale
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 9949fcc5876e1d0fa2f877333c5a9e5abae8c2a7
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607741"
---
# <a name="create-a-legal-hold-notice"></a>Créer une notification de conservation légale

Communications de dépositaire eDiscovery avancées (Preview), les organisations peuvent de gérer leur travail autour de communiquer avec dépositaires. Par le biais de l’outil de communication, les équipes juridiques peuvent systématiquement envoyer, collecter et suivre les notifications de conservation légale. Le processus de création flexible permet également aux équipes de personnaliser le flux de travail de notification de suspension et le contenu dans les messages envoyés à dépositaires. 

L’article décrit les étapes décrites dans le flux de travail de notification de suspension.

## <a name="step-1-specify-communication-details"></a>Étape 1 : Spécifier les détails de communication

La première étape consiste à spécifier les détails appropriés pour les notifications de conservation légale ou autres communications dépositaire. 

1. Dans le centre de conformité & sécurité, accédez à **eDiscovery > eDiscovery avancées (Preview)** pour afficher la liste des incidents dans votre organisation.
   
2. Cliquez sur l’onglet **Communications** , puis cliquez sur **nouveau système de communication**.
   
3. Dans la page **communication nom** , spécifiez les informations suivantes de la communication (obligatoire).

    - **Nom**: nom de la communication.
    
    - **Responsable de l’émission**: la liste déroulante affiche la liste des membres de l’incident. Chaque notification est envoyée au dépositaires envoyée au nom de l’agent de délivrance spécifié.

4. Cliquez sur **Suivant**.

## <a name="step-2-define-the-portal-content"></a>Étape 2 : Définir le contenu du portail

Ensuite, vous pouvez créer et ajouter le contenu de l’avis de suspension. Dans la page **contenu du portail définir** dans l’Assistant **créer communication** , spécifiez le contenu de l’avis de suspension. Ce contenu est automatiquement ajouté à l’avis d’émission, relancer, rappel et escalade. En outre, ce contenu s’affiche dans le portail de conformité de la dépositaire. 

Pour créer le contenu du portail :

1. Type (ou couper et système de collage automatique d’un autre document) votre attente Notez que dans la zone de texte pour le contenu du portail. 

2. Insérer des variables de fusion dans votre avis pour personnaliser la communication et de partager le portail de conformité dépositaire.

3. Cliquez sur **Suivant**.

  >[!Tip]
  >Pour en savoir que plus sur le peuvent personnaliser le contenu et le format du contenu du portail, voir [l’aide de l’éditeur de Communications](using-communications-editor.md).

## <a name="step-3-set-the-required-notifications"></a>Étape 3 : Définir les notifications requises

Une fois que vous avez défini le contenu de la notification de la suspension, vous pouvez configurer les flux de travail autour de l’envoi et de gestion du processus de notification. Les notifications sont des messages électroniques qui sont envoyés à notifier et suivi de dépositaires. Chaque dépositaire ajouté à la communication reçoivent une notification même. 

Pour configurer et envoyer une notification de la suspension, vous devez inclure d’émission, réattribution et libérer les notifications.

### <a name="issuance-notification"></a>Notification d’émission 

Une fois la communication est créée, la **Notification d’émission** est lancée par l’agent de délivrance spécifié. La notification d’émission est la première communication envoyée au dépositaire pour les informer des obligations de conservation. 

Pour créer une notification d’émission :

1. Dans la fenêtre **d’émission** , cliquez sur **Modifier**.
   
2. Si nécessaire, ajoutez des membres cas supplémentaires ou personnel pour les champs **Cc** et **Cci** . Pour ajouter plusieurs utilisateurs à ces champs, séparez les adresses de messagerie par un point-virgule.
   
3. Spécifiez le **sujet** de la mention (requis).
   
4. Spécifier le contenu ou l’instruction supplémentaire que vous souhaitez fournir le dépositaire (requis). Notez que le contenu du portail que vous défini à l’étape 2 est ajouté à la fin de la notification d’émission. 
   
5. Cliquez sur **Enregistrer**. 

### <a name="re-issuance-notification"></a>Notification de réattribution 

Fur et à la casse, dépositaires peuvent être nécessaires pour conserver des données supplémentaires au maximum qu’a été indiqué précédemment. Une fois que vous mettez à jour le contenu de l’avis de suspension, la notification réattribution les dépositaires sur les modifications apportées à leurs obligations de conservation des alertes.

Pour créer une notification réattribution : 

1. Dans la fenêtre **relancez** , cliquez sur **Modifier**.
   
2. Si nécessaire, ajoutez des membres cas supplémentaires ou personnel pour les champs **Cc** et **Cci** . Pour ajouter plusieurs utilisateurs à ces champs, séparez les adresses de messagerie par un point-virgule.
   
3. Spécifiez le **sujet** de la mention (requis).
   
4. Spécifier le contenu ou l’instruction supplémentaire que vous souhaitez fournir le dépositaire (requis). Notez que le contenu du portail que vous défini à l’étape 2 est ajouté à la fin de l’avis de réattribution.
   
5. Cliquez sur **Enregistrer**.

>[!Note]
>Si une notification de la suspension est modifiée, la notification réattribution est automatiquement envoyée à tous les dépositaires affectés à l’avis. Une fois que la notification est envoyée, dépositaires demandera de confirmer nouveau leur avis de suspension. Si vous avez configuré tous les workflows rappel ou escalade, ces également renouveler démarrera. 

### <a name="release-notification"></a>Notification de version

Après qu’une question est résolue ou si un dépositaire n’est plus soumis à conserver du contenu, vous pouvez lancer le dépositaire à partir d’un cas. Si le dépositaire a été publié précédemment un avis de suspension, la notification de version peut servir à dépositaires d’alerte qu’ils ont été publiées à partir de leur obligation.

Pour créer une notification de version : 

1. Dans la fenêtre **version** , cliquez sur **Modifier**.
   
2. Si nécessaire, ajoutez des membres cas supplémentaires ou personnel pour les champs **Cc** et **Cci** . Pour ajouter plusieurs utilisateurs à ces champs, séparez les adresses de messagerie par un point-virgule.
   
3. Spécifiez le **sujet** de la mention (requis).
   
4. Spécifier le contenu ou l’instruction supplémentaire que vous souhaitez fournir le dépositaire (requis).
   
5. Cliquez sur **Enregistrer** et passez à l’étape suivante. 

## <a name="optional-step-4-set-the-optional-notifications"></a>(Facultatif) Étape 4 : Définir les notifications facultatives

Si vous le souhaitez, vous pouvez simplifier le flux de travail pour suivi des dépositaires ne répond pas par escalade et de création et de la planification de rappel automatique notifications.

### <a name="reminders"></a>Rappels

Une fois que vous avez envoyé une notification d’attente, vous pouvez assurer un suivi avec dépositaires ne répond pas en définissant un flux de travail de rappel. 

Pour planifier les rappels :

1. Dans la fenêtre de **rappel** , cliquez sur **Modifier**.
   
2. Activer le flux de travail **relance** en activant le bouton **statut** (obligatoire).
   
3. Spécifier l' **intervalle de rappel (en jours)** (requis). Il s’agit du nombre de jours à attendre avant d’envoyer les notifications de rappel premier et le suivi. Par exemple, si vous définissez la fréquence de rappel sur 7 jours, puis premier rappel serait envoyé 7 jours après que la notification de la suspension a été émise à l’origine. Tous les rappels suivants recevraient également tous les 7 jours.
   
4. Spécifiez le **nombre de rappels** (requis). Ce champ indique combien de rappels à envoyer à dépositaires non réactifs. Par exemple, si vous définissez le nombre de rappels à 3, un dépositaire recevoir un maximum de 3 rappels. Après qu’un dépositaire reconnaît la notification de la suspension, les rappels ne recevrez à cet utilisateur.
   
5. Spécifiez le **sujet** de la mention (requis). 
   
6. Spécifier le contenu ou l’instruction supplémentaire que vous souhaitez fournir le dépositaire (requis). Notez que le contenu du portail que vous défini à l’étape 2 est ajouté à la fin de la notification de rappel.
   
7. Cliquez sur **Enregistrer** , puis la l’étape suivante.

### <a name="escalations"></a>Procédures d’escalade 

Dans certains cas, vous devrez peut-être permettant d’assurer un suivi avec dépositaires ne répond pas. Si un dépositaire ne reconnaître une notification de suspension lorsqu’il reçoit le nombre spécifié de rappels, l’équipe juridique peut spécifier un flux de travail pour envoyer automatiquement une notification d’escalade pour le dépositaire et leur responsable.

Pour planifier la transformation :

1. Dans la vignette de **réaffectation** , cliquez sur **Modifier**.
   
2. Activer le flux de travail de **réaffectation** en activant **l’état** bascule.
   
3. Spécifier l' **intervalle (en jours) d’escalade** (requis). 
   
4. Spécifiez le **nombre d’escalades** (requis). Ce champ indique combien d’escalade pour envoyer à dépositaires non réactifs. Par exemple, si vous définissez le nombre d’escalades à 3, puis un avis d’escalade doit être adressée au dépositaire et leur responsable un maximum de 3 fois. Une fois un dépositaire reconnaît la notification de la suspension, escalade ne sont plus envoyés. 
   
5. Spécifiez le **sujet** de la mention (requis). 
   
6. Spécifier le contenu ou l’instruction supplémentaire que vous souhaitez fournir le dépositaire (requis). Notez que le contenu du portail que vous défini à l’étape 2 est ajouté à la fin de l’avis de réaffectation.
   
7. Cliquez sur **Enregistrer** , puis la l’étape suivante.
   
## <a name="step-5-assign-custodians"></a>Étape 5 : Attribuer dépositaires 

Une fois que vous avez finalisé le contenu des notifications, sélectionnez les dépositaires pour envoyer les notifications. 

Pour ajouter des dépositaires :

1. Affecter des dépositaires pour la communication en cliquant sur la case à cocher en regard de son nom.

    Une fois la communication est créée, applique automatiquement le flux de travail de notification pour les dépositaires sélectionnés.
   
2. Cliquez sur **suivant** pour passer en revue les paramètres de communication et les détails.
 
>[!NOTE]
>Vous ne pouvez ajouter dépositaires qui ont été ajoutés à la casse et n’ont pas été envoyés à un autre dans le cas de notification.

## <a name="step-6-review-settings"></a>Étape 6 : Vérifier les paramètres

Une fois que vous passez en revue les paramètres et cliquez sur **Envoyer** pour terminer la communication, le système démarre automatiquement le flux de travail de communication en envoyant la notification d’émission.