---
title: Valeurs BCL
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/5/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
description: Les vers de publipostage en bloc ont des modèles d'envoi différents, ainsi que des pratiques de création de contenu et d'acquisition de liste variées. Certains sont de bons vers de publipostage en bloc et envoient des messages désirés comportant un contenu pertinent à leurs abonnés. Ces messages entraînent peu de réclamations de la part des destinataires. D'autres vers de publipostage en bloc envoient des messages non sollicités qui s'apparentent fortement à du courrier indésirable et entraînent de nombreuses réclamations de la part des destinataires. Pour distinguer ces types de vers de publipostage en bloc, une évaluation BCL (Bulk Complaint Level) est réalisée sur les messages qui en proviennent. Les évaluations BCL vont de 1 à 9 selon la probabilité de réclamations dues au ver de publipostage en bloc. Un expéditeur disposant d'une évaluation BCL de 9 peut entraîner un grand nombre de réclamations de la part des destinataires, tandis qu'un autre expéditeur ayant une évaluation BCL de 3 n'en générera probablement pas beaucoup. Microsoft utilise des sources internes et tierces pour identifier le courrier en masse et déterminer l'évaluation BCL appropriée. Cette évaluation est présentée dans l'en-tête X-Microsoft-Antispam de chaque message. Pour plus d'informations sur cet en-tête de message, voir En-têtes de messages anti-courrier indésirable.
ms.openlocfilehash: adf179ba4a309f2ed22275179013b576888960c6
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026261"
---
# <a name="bulk-complaint-level-values"></a>Valeurs BCL

Les vers de publipostage en bloc ont des modèles d'envoi différents, ainsi que des pratiques de création de contenu et d'acquisition de liste variées. Certains sont de bons vers de publipostage en bloc et envoient des messages désirés comportant un contenu pertinent à leurs abonnés. Ces messages entraînent peu de réclamations de la part des destinataires. D'autres vers de publipostage en bloc envoient des messages non sollicités qui s'apparentent fortement à du courrier indésirable et entraînent de nombreuses réclamations de la part des destinataires. Pour distinguer ces types de vers de publipostage en bloc, une évaluation BCL (Bulk Complaint Level) est réalisée sur les messages qui en proviennent. Les évaluations BCL vont de 1 à 9 selon la probabilité de réclamations dues au ver de publipostage en bloc. Un expéditeur disposant d'une évaluation BCL de 9 peut entraîner un grand nombre de réclamations de la part des destinataires, tandis qu'un autre expéditeur ayant une évaluation BCL de 3 n'en générera probablement pas beaucoup. Microsoft utilise des sources internes et tierces pour identifier le courrier en masse et déterminer l'évaluation BCL appropriée. Cette évaluation est présentée dans l'en-tête **X-Microsoft-Antispam** de chaque message. Pour plus d'informations sur cet en-tête de message, voir [En-têtes de messages anti-courrier indésirable](anti-spam-message-headers.md). 
  
Vous pouvez vous servir des valeurs BCL pour définir le niveau de filtrage en bloc souhaité pour votre organisation en suivant les étapes décrites dans la rubrique [Configuration de vos stratégies de filtrage du courrier indésirable](configure-your-spam-filter-policies.md).
  
D'autres valeurs BCL sont ajoutées et seront incluses ici à l'avenir. Le tableau suivant répertorie et décrit les valeurs BCL actuellement utilisées.
  
|||
|:-----|:-----|
|**Valeur BCL** <br/> |**Description** <br/> |
|0  <br/> |Le message ne provient pas d'un expéditeur en bloc.  <br/> |
|1, 2, 3  <br/> |Le message provient d'un expéditeur en bloc qui génère peu de réclamations.  <br/> |
|4, 5, 6, 7  <br/> |Le message provient d'un expéditeur en bloc qui génère un nombre moyen de réclamations.  <br/> |
|8, 9  <br/> |Le message provient d'un expéditeur en bloc qui génère un grand nombre de réclamations  <br/> |
   

