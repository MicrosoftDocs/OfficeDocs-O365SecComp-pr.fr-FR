---
title: Créer une notice de suspension légale
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 7d2746699a427fa3c7ad3afd7cf791c61cd55249
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213094"
---
# <a name="create-a-legal-hold-notice"></a>Créer une notice de suspension légale

À l'aide des communications des dépositaires avancés (aperçu), les organisations peuvent gérer leur flux de travail pour communiquer avec des dépositaires. Grâce à l'outil de communication, les équipes juridiques peuvent envoyer, collecter et suivre systématiquement les notifications de conservation légale. Le processus de création flexible permet également à teams de personnaliser le flux de travail de notification de blocage et le contenu des notifications envoyées aux dépositaires. 

L'article décrit les étapes du flux de travail de notification de blocage.

## <a name="step-1-specify-communication-details"></a>Étape 1: spécifier les détails de communication

La première étape consiste à spécifier les détails appropriés pour les notifications de suspension légale ou autres communications de dépositaire. 

1. Dans le centre de sécurité & Compliance Center, accédez à **eDiscovery _GT_ Advanced eDiscovery (Preview)** pour afficher la liste des incidents de votre organisation.
   
2. Cliquez sur l'onglet **communications** , puis sur **nouvelle communication**.
   
3. Sur la page **communication de nom** , spécifiez les détails de communication (obligatoires) suivants.

    - **Name**: il s'agit du nom de la communication.
    
    - **Officier émetteur**: la liste déroulante affiche la liste des membres d'un cas. Chaque notification envoyée aux dépositaires est envoyée au nom de l'officier émetteur spécifié.

4. Cliquez sur **Suivant**.

## <a name="step-2-define-the-portal-content"></a>Étape 2: définir le contenu du portail

Ensuite, vous pouvez créer et ajouter le contenu de la notification de suspension. Dans la page **définir le contenu du portail** , dans l'assistant créer une **communication** , spécifiez le contenu de la notification de suspension. Ce contenu sera automatiquement ajouté aux notifications d'émission, de réÉmission, de rappel et de signalisation. De plus, ce contenu s'affichera dans le portail de conformité du dépositaire. 

Pour créer le contenu du portail:

1. Tapez (ou coupez-coller dans un autre document) votre notification de blocage dans la zone de texte du contenu du portail. 

2. Insérez des variables de fusion dans votre notification pour personnaliser l'avis et partager le portail de conformité des dépositaires.

3. Cliquez sur **Suivant**.

  >[!Tip]
  >Pour en savoir plus sur la personnalisation du contenu et du format du contenu du portail, consultez [la rubrique utiliser l'éditeur de communications](using-communications-editor.md).

## <a name="step-3-set-the-required-notifications"></a>Étape 3: définir les notifications requises

Une fois que vous avez défini le contenu de la notification de mise en attente, vous pouvez configurer les flux de travail pour l'envoi et la gestion du processus de notification. Les notifications sont des messages électroniques qui sont envoyés pour informer et suivre les dépositaires. Chaque dépositaire ajouté à la communication reçoit la même notification. 

Pour configurer et envoyer une notification de mise en attente, vous devez inclure les notifications d'émission, de ré-émission et de publication.

### <a name="issuance-notification"></a>Notification d'émission 

Une fois la communication créée, la **notification d'émission** est initiée par le responsable émetteur spécifié. La notification d'émission est la première communication envoyée au dépositaire pour l'informer de ses obligations de conservation. 

Pour créer une notification d'émission:

1. Dans la vignette **émission** , cliquez sur **modifier**.
   
2. Si nécessaire, ajoutez des membres de cas supplémentaires ou du personnel dans les champs **CC** et **CCI** . Pour ajouter plusieurs utilisateurs à ces champs, séparez les adresses de messagerie par un point-virgule.
   
3. Spécifiez l' **objet** de l'avis (obligatoire).
   
4. Spécifiez le contenu ou les instructions supplémentaires que vous souhaitez fournir au dépositaire (obligatoire). Notez que le contenu du portail que vous avez défini à l'étape 2 est ajouté à la fin de l'avis d'émission. 
   
5. Cliquez sur **Enregistrer**. 

### <a name="re-issuance-notification"></a>Notification de nouvelle émission 

En cas de progression, les dépositaires peuvent être tenus de conserver des données supplémentaires ou moins que celles précédemment demandées. Une fois que vous avez mis à jour le contenu de la notification d'attente, la notification de nouvelle émission alerte les dépositaires des modifications apportées à leurs obligations de conservation.

Pour créer une notification de ré-émission: 

1. Dans la **** vignette de réémission, cliquez sur **modifier**.
   
2. Si nécessaire, ajoutez des membres de cas supplémentaires ou du personnel dans les champs **CC** et **CCI** . Pour ajouter plusieurs utilisateurs à ces champs, séparez les adresses de messagerie par un point-virgule.
   
3. Spécifiez l' **objet** de l'avis (obligatoire).
   
4. Spécifiez le contenu ou les instructions supplémentaires que vous souhaitez fournir au dépositaire (obligatoire). Notez que le contenu du portail que vous avez défini à l'étape 2 est ajouté à la fin de l'avis de ré-émission.
   
5. Cliquez sur **Enregistrer**.

>[!Note]
>Si une notification de mise en attente est modifiée, la notification de nouvelle émission est automatiquement envoyée à tous les dépositaires affectés à l'avis. Après l'envoi de la notification, les dépositaires seront invités à relancer leur avis de mise en attente. Si vous avez configuré des flux de travail de rappel ou de remontée, ceux-ci redémarrent également. 

### <a name="release-notification"></a>Notification de publication

Une fois qu'un problème est résolu ou qu'un dépositaire n'est plus soumis à la conservation du contenu, vous pouvez libérer le dépositaire à partir d'un cas. Si le dépositaire a déjà émis une notification de mise en attente, la notification de publication peut être utilisée pour informer les dépositaires qu'ils ont été libérés de leur obligation.

Pour créer une notification de publication: 

1. Dans la vignette de **publication** , cliquez sur **modifier**.
   
2. Si nécessaire, ajoutez des membres de cas supplémentaires ou du personnel dans les champs **CC** et **CCI** . Pour ajouter plusieurs utilisateurs à ces champs, séparez les adresses de messagerie par un point-virgule.
   
3. Spécifiez l' **objet** de l'avis (obligatoire).
   
4. Spécifiez le contenu ou les instructions supplémentaires que vous souhaitez fournir au dépositaire (obligatoire).
   
5. Cliquez sur **Enregistrer** et passez à l'étape suivante. 

## <a name="optional-step-4-set-the-optional-notifications"></a>Module Étape 4: définir les notifications facultatives

Si vous le souhaitez, vous pouvez simplifier le flux de travail pour le suivi des dépositaires qui ne répondent pas en créant et en planifiant des notifications automatiques de rappel et de remontée.

### <a name="reminders"></a>Rappels

Une fois que vous avez envoyé une notification de mise en attente, vous pouvez suivre l'absence de remise des dépositaires en définissant un flux de travail de rappel. 

Pour planifier les rappels:

1. Dans la vignette **rappel** , cliquez sur **modifier**.
   
2. Activer le flux de travail de **rappel** en activant le bouton bascule d' **État** (obligatoire).
   
3. Spécifier l' **intervalle de rappel (en jours)** (requis). Il s'agit du nombre de jours d'attente avant l'envoi des premières notifications de rappel de suivi. Par exemple, si vous définissez l'intervalle de rappel sur 7 jours, le premier rappel sera envoyé 7 jours après l'émission initiale de la notification de blocage. Tous les rappels suivants seront également envoyés tous les 7 jours.
   
4. Spécifier le **nombre de rappels** (obligatoire). Ce champ indique le nombre de rappels à envoyer aux dépositaires non réactifs. Par exemple, si vous définissez le nombre de rappels sur 3, un dépositaire recevra un maximum de 3 rappels. Lorsqu'un dépositaire accuse réception de la notification de mise en attente, les rappels ne sont plus envoyés à cet utilisateur.
   
5. Spécifiez l' **objet** de l'avis (obligatoire). 
   
6. Spécifiez le contenu ou les instructions supplémentaires que vous souhaitez fournir au dépositaire (obligatoire). Notez que le contenu du portail que vous avez défini à l'étape 2 est ajouté à la fin de l'avis de rappel.
   
7. Cliquez sur **Enregistrer** et passez à l'étape suivante.

### <a name="escalations"></a>Escalades 

Dans certains cas, vous aurez peut-être besoin de moyens supplémentaires pour assurer le suivi des conservateurs qui ne répondent plus. Si un dépositaire n'accuse aucune notification de blocage après réception du nombre spécifié de rappels, l'équipe juridique peut spécifier un flux de travail pour envoyer automatiquement une notification d'escalade au dépositaire et à son responsable.

Pour planifier les escalades:

1. Dans la vignette **escalade** , cliquez sur **modifier**.
   
2. Activez le flux de travail d' **escalade** en activant le bouton bascule d' **État** .
   
3. Spécifiez l' **intervalle de réaffectation (en jours)** (requis). 
   
4. Spécifiez le **nombre de** remontées (obligatoire). Ce champ indique le nombre de demandes d'envoi aux dépositaires non réactifs. Par exemple, si vous définissez le nombre de demandes d'escalade sur 3, une notification d'escalade est envoyée au dépositaire et à son responsable un maximum de 3 fois. Lorsqu'un dépositaire accuse réception de la notification de mise en attente, les escalades ne seront plus envoyées. 
   
5. Spécifiez l' **objet** de l'avis (obligatoire). 
   
6. Spécifiez le contenu ou les instructions supplémentaires que vous souhaitez fournir au dépositaire (obligatoire). Notez que le contenu du portail que vous avez défini à l'étape 2 est ajouté à la fin de l'avis de remontée.
   
7. Cliquez sur **Enregistrer** et passez à l'étape suivante.
   
## <a name="step-5-assign-custodians"></a>Étape 5: affecter des dépositaires 

Une fois que vous avez finalisé le contenu des notifications, sélectionnez les dépositaires auxquels les notifications doivent être envoyées. 

Pour ajouter des dépositaires:

1. Attribuer des dépositaires à la communication en cliquant sur la case à cocher en regard de leur nom.

    Une fois la communication créée, le flux de travail de notification s'applique automatiquement aux dépositaires sélectionnés.
   
2. Cliquez sur **suivant** pour passer en revue les paramètres et les détails de communication.
 
>[!NOTE]
>Vous pouvez uniquement ajouter des dépositaires qui ont été ajoutés à l'incident et qui n'ont pas reçu d'autre notification dans le cas.

## <a name="step-6-review-settings"></a>Étape 6: passez en revue les paramètres

Une fois que vous avez vérifié les paramètres et cliqué sur **Envoyer** pour terminer la communication, le système démarrera automatiquement le flux de travail de communication en envoyant l'avis d'émission.