---
title: "valeurs de niveau de réclamation en bloc" ms. Author: krowley Author: kccross Manager: laurawi ms. Date: 3/5/2015 ms. audience: professionnel ms. topic: article ms. service: O365-seccomp ms. Custom: TN2DMC localization_priority: normal Search. appverid:
- MET150 ms. AssetID: a5b03b3c-37dd-429e-8e9b-2c1b25031794 ms. collection:
    - M365-Security-Description de la conformité: «les expéditeurs de courriers électroniques varient en fonction de leurs pratiques d'envoi de tterns, de création de contenu et d'acquisition de liste. Certains sont des expéditeurs de publipostage en bloc qui envoient des messages désirés avec du contenu pertinent à leurs abonnés. Ces messages génèrent peu de réclamations de la part des destinataires. D'autres expéditeurs de courriers électroniques envoient des messages non sollicités qui ressemblent beaucoup au courrier indésirable et génèrent de nombreuses plaintes de la part Pour distinguer ces types d'expéditeurs de courrier en nombre, les messages provenant de publipostages en bloc reçoivent une évaluation BCL (Bulk Complaint Level). Les évaluations de BCL vont de 1 à 9 en fonction de la probabilité que le courrier en nombre génère des plaintes. Un expéditeur ayant une notation BCL 9 peut générer de nombreuses plaintes de la part des destinataires, tandis qu'une évaluation de la bibliothèque BCL 3 ne peut pas générer de nombreuses plaintes. Microsoft utilise des sources internes et tierces pour identifier le courrier en nombre et déterminer le BCL approprié. Cette évaluation est exposée dans l'en-tête X-Microsoft-antispam de chaque message. Pour plus d'informations sur cet en-tête de message, voir en-têtes de message anti-courrier indésirable.
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
   

