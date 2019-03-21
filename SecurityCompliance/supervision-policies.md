---
title: Stratégies de surveillance dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Présentation des stratégies de surveillance dans Office 365
ms.openlocfilehash: c22abdf315b2301ae9c63b26f548eff302df8e2a
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2019
ms.locfileid: "30720274"
---
# <a name="supervision-policies-in-office-365"></a>Stratégies de surveillance dans Office 365

Les stratégies de surveillance dans Office 365 vous permettent de capturer les communications des employés pour les examiner par les réviseurs désignés. Vous pouvez définir des stratégies spécifiques qui capturent les messages internes et externes, Microsoft teams ou les communications tierces au sein de votre organisation. Les relecteurs peuvent alors examiner les messages pour s'assurer qu'ils sont conformes aux standards de messages de votre organisation et les résoudre avec le type de classification. Ces stratégies peuvent également vous aider à surmonter de nombreux défis de conformité modernes, notamment la surveillance de types croissants de canaux de communication, l'augmentation du volume des données de message et la mise en conformité réglementaire & risques d'amendes.

Dans certaines organisations, le support informatique et le groupe de gestion de la conformité peuvent séparer les tâches. Office 365 prend en charge la séparation entre la configuration du client et la prise en charge des stratégies de surveillance, ainsi que la configuration des stratégies et l'action sur les communications capturées. Par exemple, le groupe informatique d'une organisation peut être responsable de la configuration des autorisations de rôle et des groupes afin de prendre en charge les stratégies de surveillance configurées et gérées par l'équipe de conformité de l'organisation.

## <a name="scenarios-for-supervision-policies"></a>Scénarios de surveillance des stratégies

Les stratégies de surveillance peuvent faciliter la surveillance des communications dans votre organisation dans plusieurs domaines:

- **Stratégies d'entreprise**

    Les employés doivent respecter une utilisation acceptable, des normes éthiques et d'autres stratégies d'entreprise dans toutes leurs communications professionnelles. Les stratégies de surveillance peuvent détecter les violations de stratégie et vous aider à prendre des mesures correctives pour limiter ces types d'incidents. Par exemple, vous pouvez surveiller votre organisation pour détecter les éventuelles violations de ressources humaines telles que le harcèlement ou l'utilisation d'un langage inapproprié ou choquant dans les communications des employés.

- **Gestion des risques**

    Les organisations sont responsables de toutes les communications distribuées au sein de leur infrastructure et des systèmes réseau d'entreprise. L'utilisation de stratégies de surveillance pour aider à identifier et à gérer les risques juridiques et les risques potentiels peut aider à réduire les risques avant qu'ils puissent endommager les opérations de l'entreprise. Par exemple, vous pouvez surveiller votre organisation afin d'obtenir des communications non autorisées pour des projets confidentiels, tels que les acquisitions à venir, les fusions, les informations de résultats, les réorganisations ou les modifications de l'équipe de leadership.

- **Conformité réglementaire**

    La plupart des organisations doivent se conformer à certains types de normes de conformité réglementaire dans le cadre de leurs procédures d'utilisation normales. Ces réglementations obligent souvent les organisations à mettre en place un certain type de processus de surveillance ou de supervision pour la messagerie appropriée pour leur secteur d'activité. La règle 3110 de l'autorité réglementaire du secteur financier (FINRA) est un excellent exemple d'une obligation pour les organisations de mettre en place des procédures de surveillance pour surveiller les activités de ses employés et les types d'entreprises dans lesquelles elle s'engage. Un autre exemple doit être de surveiller les concessionnaires de courtiers de votre organisation afin de se protéger contre les activités potentielles de blanchiment de fonds, de commerce d'initié, de collusion ou de corruption. Les stratégies de surveillance peuvent aider votre organisation à répondre à ces exigences en fournissant un processus à la fois pour surveiller et rendre compte des communications de l'entreprise.

## <a name="feature-components"></a>Composants fonctionnels

### <a name="supervision-policy"></a>Stratégie de supervision

Vous allez créer des stratégies de surveillance dans le centre de sécurité & Compliance Center. Ces stratégies définissent les communications et les utilisateurs qui font l'objet d'une vérification dans votre organisation, définissent les conditions personnalisées que les communications doivent respecter et spécifie qui doit effectuer des révisions. Les utilisateurs inclus dans le groupe de rôles examen de surveillance peuvent configurer des stratégies et toute personne à laquelle ce rôle est attribué peut accéder à la page surveillance sous gouvernance des données dans le centre de sécurité & de la sécurité d'Office 365.

### <a name="supervised-users"></a>Utilisateurs superVisés

Avant de commencer à utiliser la surveillance, vous devez déterminer les personnes à l'aide desquelles les communications seront revues. Dans la stratégie, vous utiliserez les adresses de messagerie des utilisateurs pour identifier des individus ou des groupes de personnes à superviser. Les groupes Office 365, les listes de distribution Exchange et les canaux Microsoft teams sont des exemples de ces groupes. Vous pouvez également exclure des utilisateurs ou des groupes spécifiques de la surveillance incluse dans un groupe supervisé ou une liste de groupes.

> [!IMPORTANT]
> Les utilisateurs surveillés par des stratégies de surveillance doivent disposer d'une licence de conformité Microsoft 365 E5, d'une licence Office 365 entreprise E3 avec le complément de conformité avancé ou être inclus dans un abonnement Office 365 entreprise E5.
Si vous ne disposez pas d'un plan entreprise E5 existant et que vous souhaitez essayer de contrôler, vous pouvez vous [inscrire pour obtenir une version d'évaluation d'Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).

### <a name="reviewers"></a>Reviewers

Lorsque vous créez une stratégie de surveillance, vous déterminez également qui effectuera les révisions des messages des utilisateurs supervisés. Dans la stratégie, vous utiliserez les adresses de messagerie des utilisateurs pour identifier des individus ou des groupes de personnes afin d'examiner les communications surveillées.

### <a name="groups-for-supervised-users-and-reviewers"></a>Groupes pour les utilisateurs et les relecteurs surveillés

Pour simplifier votre configuration, créez des groupes pour les personnes dont la communication est vérifiée et les groupes pour les personnes qui examineront ces communications. Si vous utilisez des groupes, vous aurez peut-être besoin de plusieurs. Par exemple, si vous souhaitez surveiller les communications entre deux groupes distincts de personnes, ou si vous souhaitez spécifier un groupe qui n'est pas supervisé.

### <a name="supported-communication-types"></a>Types de communication pris en charge

Avec les stratégies de surveillance, vous pouvez choisir de surveiller les messages dans une ou plusieurs des plateformes de communication suivantes:

- **Courrier électronique Exchange:** Les boîtes aux lettres hébergées sur Exchange Online dans le cadre de votre abonnement Office 365 sont toutes éligibles pour la supervision des messages. Les E-mails et les pièces jointes correspondant aux conditions de stratégie de surveillance sont immédiatement disponibles pour la surveillance et les rapports de surveillance. Les types de pièces jointes prises en charge pour la surveillance sont les mêmes que pour les [types de fichiers pris en charge pour les inspections de contenu des règles de flux de messagerie](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection)
- **Microsoft teams:** Les communications de conversation et les pièces jointes associées dans les canaux Microsoft teams publics et privés, ainsi que dans les conversations individuelles, peuvent être surveillées. Les conversations teams correspondant aux conditions de stratégie de contrôle sont traitées une fois toutes les 24 heures, puis disponibles pour la surveillance et les rapports de surveillance.
- **Sources** tierces: Vous pouvez superviser les communications provenant de sources tierces (par exemple, Facebook ou DropBox) si vous avez importé ces données dans des boîtes aux lettres Office 365 de votre organisation. [Découvrez comment importer des données tierces dans Office 365](https://docs.microsoft.com/office365/securitycompliance/archiving-third-party-data).

### <a name="policy-settings"></a>Paramètres de stratégie

#### <a name="direction"></a>Direction (Sens)

Par défaut, la **direction est** la condition est affichée et ne peut pas être supprimée. Les paramètres de direction de communication d'une stratégie peuvent être choisis individuellement ou ensemble:

- **Entrant** : vous pouvez choisir **entrant** pour examiner les communications envoyées **aux** personnes que vous avez choisies de superviser **des** personnes qui ne sont pas incluses dans la stratégie.
- **Sortant** : vous pouvez choisir **sortant** si vous voulez passer en revue les communications envoyées **par** les personnes que vous avez choisies de surveiller **aux** personnes non incluses dans la stratégie.
- **Internal** : vous pouvez choisir **Internal** pour examiner les communications envoyées **entre** les personnes que vous avez identifiées dans la stratégie.

#### <a name="sensitive-information-types"></a>Types d’informations sensibles

Vous pouvez inclure des types d'informations sensibles dans le cadre de votre stratégie de supervision. Les types d'informations sensibles sont des types de données prédéfinis ou personnalisés qui peuvent vous aider à identifier et à protéger les numéros de carte de crédit, les numéros de compte bancaire, les numéros de passeport, et bien plus encore. Dans le cadre de la [protection contre la perte de données (DLP)](data-loss-prevention-policies.md)d'Office 365, la configuration des informations sensibles peut tirer parti des modèles, de la proximité des caractères, des niveaux de confiance et même des types de données personnalisés pour identifier et marquer le contenu susceptible d'être sensible. Les types d'informations sensibles par défaut sont les suivants:

- Finances
- Médecine et santé
- Politique de confidentialité
- Type d'informations personnalisées

Pour en savoir plus sur les détails des informations sensibles et les modèles inclus dans les types par défaut, consultez la rubrique [types d'informations sensibles](what-the-sensitive-information-types-look-for.md).

#### <a name="custom-keyword-dictionaries"></a>Dictionnaires de mots clés personnalisés

La configuration de dictionnaires de mots clés personnalisés (ou de lexiques) peut fournir une gestion simple des mots clés propres à votre organisation ou votre secteur d'activité et peut prendre en charge jusqu'à 100 000 termes par dictionnaire. Si nécessaire, vous pouvez appliquer plusieurs dictionnaires de mots clés personnalisés à une seule stratégie ou disposer d'un dictionnaire à Mots clés unique par stratégie. Ces dictionnaires sont affectés dans une stratégie de surveillance et peuvent être issus d'un fichier (par exemple, une liste. csv ou. txt) ou d'une liste que vous pouvez [importer dans le centre de conformité](create-a-keyword-dictionary.md).

#### <a name="conditional-settings"></a>Paramètres conditionnels

Les conditions que vous choisissez pour la stratégie s'appliquent aux communications à partir de la messagerie et des sources tierces de votre organisation (par exemple, Facebook ou DropBox).

Le tableau suivant décrit plus en plus de chaque condition.
  
|**Condition**|**Comment utiliser cette condition ?**|
|:-----|:-----|
|Un message est reçu à partir de l'un de ces domaines  <br><br> Le message n'est reçu à partir d'aucun de ces domaines | Pour appliquer la stratégie lorsque certains domaines sont inclus ou exclus d'un message reçu, entrez chaque domaine et plusieurs domaines séparés par une virgule. Chaque domaine que vous entrez sera appliqué séparément (un seul de ces domaines doit s'appliquer à la stratégie à appliquer au message). |
|Un message est envoyé à l'un de ces domaines  <br><br> Le message n'est pas envoyé à l'un de ces domaines | Pour appliquer la stratégie lorsque certains domaines sont inclus ou exclus d'un message envoyé, entrez chaque domaine et plusieurs domaines séparés par une virgule. Chaque domaine que vous entrez sera appliqué séparément (un seul de ces domaines doit s'appliquer à la stratégie à appliquer au message). |
|Le message est classé avec l'une de ces étiquettes  <br><br> Le message n'est classé avec aucune de ces étiquettes | Pour appliquer la stratégie lorsque certaines étiquettes de rétention sont incluses ou exclues dans un message. Les étiquettes de réTention doivent être configurées séparément et les étiquettes configurées peuvent être sélectionnées dans le cadre de cette condition. Chaque étiquette que vous choisissez sera appliquée séparément (une seule de ces étiquettes doit s'appliquer pour la stratégie à appliquer au message). Pour plus d'informations sur la configuration des étiquettes de rétention, consultez la rubrique [vue d'ensemble des étiquettes de](https://docs.microsoft.com/office365/securitycompliance/labels)rétention.|
|Le message contient l'un de ces mots  <br><br> Le message ne contient aucun de ces mots | Pour appliquer la stratégie lorsque certains mots ou expressions sont inclus ou exclus dans un message, entrez chaque mot ou expression sur une ligne distincte. Chaque ligne de mots que vous entrez sera appliquée séparément (une seule de ces lignes doit s'appliquer pour la stratégie à appliquer au message). Pour plus d’informations sur la saisie des mots ou des expressions, voir la section suivante [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
|La pièce jointe contient l'un de ces mots  <br><br> La pièce jointe ne contient aucun de ces mots | Pour appliquer la stratégie lorsque certains mots ou expressions sont inclus ou exclus dans une pièce jointe (par exemple, un document Word), entrez chaque mot ou expression sur une ligne distincte. Chaque ligne de mots que vous entrez sera appliquée séparément (une seule ligne doit s’appliquer pour que la stratégie s’applique à la pièce jointe). Pour plus d’informations sur la saisie des mots ou des expressions, voir la section suivante [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
|La pièce jointe est l'un de ces types de fichiers  <br><br> Aucune de ces types de fichiers n'est associée à la pièce jointe | Pour superviser les communications qui incluent ou excluent des types spécifiques de pièces jointes, entrez les extensions de fichiers (par exemple,. exe ou. pdf). Si vous souhaitez inclure ou exclure plusieurs extensions de fichiers, entrez-les sur des lignes distinctes. Il suffit que l’extension d’une seule pièce jointe corresponde pour que la stratégie s’applique.|
|La taille du message est supérieure à  <br><br> La taille du message n'est pas supérieure à | Pour examiner les messages en fonction d'une certaine taille, utilisez les conditions suivantes pour spécifier la taille maximale ou minimale qu'un message peut contenir avant d'être soumis à révision. par exemple, si vous spécifiez une **taille de Message supérieure à** \> **1,0 mo**, tous les messages qui sont 1,01 mo et plus volumineux feront l'objet d'une vérification. Vous pouvez choisir des octets, kilo-octets, mégaoctets ou gigaoctets pour cette condition.|
|La taille de la pièce jointe est supérieure à  <br><br> La pièce jointe n'est pas supérieure à | Pour examiner les messages en fonction de la taille de leurs pièces jointes, spécifiez la taille maximale ou minimale qu'une pièce jointe peut contenir avant que le message et ses pièces jointes soient soumis à révision. par exemple, si vous spécifiez une **taille de pièce jointe supérieure à** \> **2,0 mo**, tous les messages avec des pièces jointes 2,01 mo et supérieures feront l'objet d'une vérification. Vous pouvez choisir des octets, kilo-octets, mégaoctets ou gigaoctets pour cette condition.|
   
##### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Correspondance de mots et expressions avec des courriers électroniques ou des pièces jointes
<a name="Matchwords"> </a>

Chaque ligne de mots que vous entrez sera appliquée séparément (une seule ligne doit s’appliquer pour que la condition de la stratégie s’applique à la pièce jointe ou au courrier électronique). Par exemple, nous utilisons la condition, le **message contient l'un de ces mots**, avec les mots-clés «Banker» et «negociing Insider» sur des lignes distinctes. La stratégie s'applique aux messages incluant le mot «Banker» ou l'expression «negociation Insiders». Un seul de ces mots ou expression doit être présent pour que cette condition de stratégie s’applique. Les mots contenus dans le message ou dans la pièce jointe doivent correspondre exactement à ce que vous entrez.
  
##### <a name="entering-multiple-conditions"></a>Saisie de plusieurs conditions

Si vous entrez plusieurs conditions, Office 365 utilise toutes les conditions ensemble pour déterminer le moment auquel appliquer la stratégie aux éléments de communication. Lorsque vous configurez plusieurs conditions, elles doivent toutes être remplies pour que la stratégie s’applique, sauf si vous entrez une exception. Par exemple, imaginons que vous devez créer une stratégie qui doit s'appliquer si un message contient le mot «commercial» et qu'il est supérieur à 2 Mo. Toutefois, si le message contient également les mots «approuvé par Contoso Financial», la stratégie ne doit pas s'appliquer. Ainsi, dans ce cas, les trois conditions suivantes sont les suivantes:
  
- Le **message contient l'un de ces mots**, avec les mots clés «Trade»

- La **taille du message est supérieure à**, avec la valeur 2 Mo

- Le **message ne contient aucun de ces mots**, avec les mots-clés «approuvé par l'équipe financière de contoso».

#### <a name="review-percentage"></a>Vérifier le pourcentage

Vous pouvez spécifier un pourcentage de toutes les communications gérées par une stratégie de surveillance si vous souhaitez réduire la quantité de contenu à réviser. Nous allons sélectionner de manière aléatoire cette quantité de contenu à partir du pourcentage total correspondant aux conditions que vous avez choisies. Si vous souhaitez que les relecteurs examinent tous les éléments, vous pouvez entrer **100%** dans une stratégie de surveillance.

## <a name="monitoring--managing"></a>Surveillance de la gestion des &

La surveillance des résultats de vos stratégies de surveillance et l'application d'une balise de résolution est facile et pratique. Vous pouvez rapidement voir l'état des éléments vérifiés, les utilisateurs et les groupes sous surveillance, ainsi que les utilisateurs et les groupes désignés comme relecteurs.

### <a name="supervision-policy-dashboard"></a>Tableau de bord de stratégie de supervision

Le moyen le plus simple de gérer les résultats de stratégie de surveillance et de résoudre les éléments non traités est d'utiliser le tableau de bord de stratégie de supervision. Ce tableau de bord permet aux relecteurs de voir rapidement les éléments à vérifier, de prendre des mesures sur un élément et de passer en revue les résultats des éléments précédemment examinés et résolus pour chaque stratégie de surveillance. vous pouvez accéder au tableau de bord de stratégie de surveillance dans le centre de conformité Office 365 Security & à**** la **surveillance** > *de votre stratégie* > personnalisée.

#### <a name="dashboard-home"></a>Accueil du tableau de bord

La page d' **Accueil** du tableau de bord comporte plusieurs sections qui vous permettent d'effectuer rapidement des actions sur vos stratégies de surveillance. Ici, vous pouvez:

- Vérifier rapidement les points forts en attente et résolus pour la semaine
- Afficher la liste des utilisateurs et des groupes supervisés de la stratégie sélectionnée
- Afficher une liste des relecteurs et vérifier les équipes pour la stratégie sélectionnée
- Voir les plateformes de communication dont le contenu est sous surveillance pour la stratégie.

#### <a name="review-tab"></a>Onglet révision

L'onglet **révision** permet aux réviseurs de prendre des mesures et de résoudre les éléments identifiés par la stratégie sélectionnée. Ici, vous pouvez:

- Filtrer les éléments en attente, conformes, non conformes et douteux
- Baliser un élément unique comme étant conforme, non conforme ou douteable. Vous pouvez également enregistrer un commentaire avec l'élément pour clarifier l'action de marquage effectuée.
- Balise en bloc plusieurs éléments comme conformes, non conformes ou douteux. Vous pouvez également enregistrer un commentaire avec plusieurs éléments pour clarifier l'action de marquage effectuée.
- Afficher l'historique du balisage d'un élément unique, y compris la personne qui a résolu l'élément, la date et l'heure de l'action, la balise de résolution et tous les commentaires inclus.
- Reclassez les éléments consultés précédemment comme conformes, non conformes ou douteux. Vous pouvez également enregistrer un commentaire avec un ou plusieurs éléments afin de clarifier l'action de reclassification effectuée.

#### <a name="resolved-items-tab"></a>Onglet éléments résolus

L'onglet **éléments résolus** permet aux relecteurs d'afficher tous les éléments précédemment résolus pour la stratégie sélectionnée. Ici, vous pouvez:

- Afficher et trier rapidement l'objet, l'expéditeur et la date des éléments résolus.
- Afficher l'historique de classification et de commentaire d'un élément sélectionné

### <a name="other-ways-to-review-items"></a>Autres méthodes d'examen des éléments

Si les relecteurs préféreront ne pas utiliser le tableau de bord de surveillance dans Office 365, ils disposeront également d'autres options pour examiner et gérer les éléments collectés par les stratégies de surveillance.

#### <a name="outlook-on-the-web"></a>Outlook sur le web

Les utilisateurs désignés en tant que relecteurs dans une stratégie de supervision peuvent utiliser Outlook sur le Web pour passer en revue et résoudre les éléments de supervision. Le complément supervision est automatiquement installé dans Outlook sur le Web pour tous les relecteurs que vous avez spécifiés dans la stratégie. Aucune configuration supplémentaire n'est requise par votre organisation pour que les dossiers partagés de stratégie de surveillance soient disponibles pour les relecteurs configurés.

À l'aide d'Outlook sur le Web, les relecteurs peuvent:

- Afficher les éléments filtrés selon un État conforme, non conforme, suspect et résolu
- Baliser un seul élément comme conforme, non conforme, question ou résolu. Vous pouvez également enregistrer un commentaire avec l'élément pour clarifier l'action de marquage effectuée.
- Afficher l'historique du balisage d'un élément unique, y compris la personne qui a résolu l'élément, la date et l'heure de l'action, la balise de résolution et tous les commentaires inclus.
- Reclassez les éléments consultés précédemment comme conformes, non conformes ou douteux. Vous pouvez également enregistrer un commentaire avec des éléments uniques pour clarifier l'action de reclassification effectuée.

#### <a name="microsoft-outlook"></a>Microsoft Outlook

Pour passer en revue les communications identifiées par une stratégie de surveillance, les relecteurs peuvent également utiliser le complément de supervision pour Microsoft Outlook. Toutefois, les relecteurs doivent suivre certaines étapes pour les installer dans la version de bureau d'Outlook. Pour obtenir des instructions détaillées sur l'installation du complément de supervision pour Outlook, consultez la rubrique [configurer les stratégies de surveillance](configure-supervision-policies.md).

À l'aide d'Outlook, les relecteurs peuvent:

- Afficher les éléments filtrés selon un État conforme, non conforme, suspect et résolu
- Baliser un seul élément comme conforme, non conforme, question ou résolu. Vous pouvez également enregistrer un commentaire avec l'élément pour clarifier l'action de marquage effectuée.
- Afficher l'historique du balisage d'un élément unique, y compris la personne qui a résolu l'élément, la date et l'heure de l'action, la balise de résolution et tous les commentaires inclus.
- Reclassez les éléments consultés précédemment comme conformes, non conformes ou douteux. Vous pouvez également enregistrer un commentaire avec des éléments uniques pour clarifier l'action de reclassification effectuée.

## <a name="reporting"></a>Reporting

Utilisez les rapports de surveillance pour afficher l'activité de révision au niveau de la stratégie et du réviseur. Pour chaque stratégie, vous pouvez également afficher des statistiques réelles sur l'état actuel de l'activité de révision. Vous pouvez utiliser les rapports de surveillance pour:
  
- Vérifiez que vos stratégies fonctionnent comme prévu.
- Déterminez le nombre de communications identifiées pour la révision.
- Déterminez le nombre de communications non conformes et celles qui passent la révision. Ces informations peuvent vous aider à décider s'il faut affiner vos stratégies ou modifier le nombre de relecteurs.

### <a name="view-the-supervision-report"></a>Afficher le rapport de supervision

1. Connectez-vous au [Centre de sécurité _AMP_ conformité](https://protection.office.com/) à l'aide des informations d'identification d'un compte d'administrateur de votre organisation Office 365 qui dispose des autorisations nécessaires pour afficher les rapports de surveillance.
2. Accédez au **tableau de bord** **rapports** \> ou à la **supervision**. Vous verrez un widget rapport de surveillance avec une synthèse de l'activité de stratégie de surveillance actuelle.
3. Sélectionnez le widget **surveillance** pour ouvrir la page rapport détaillé.

> [!NOTE]
> Si vous ne parvenez pas à accéder à la page **rapports** , vérifiez que vous êtes membre du groupe de rôles examen de surveillance, comme décrit dans la rubrique [création d'un contrôle disponible dans votre organisation](configure-supervision-policies.md). L'inclusion dans ce groupe de rôles vous permet de créer et de gérer des stratégies de surveillance et d'exécuter le rapport.
  
### <a name="how-to-use-the-report"></a>Utilisation du rapport

Lorsqu'une stratégie de surveillance identifie un message de communication à des fins de révision, le courrier électronique est remis au dossier de surveillance du réviseur dans Outlook et Outlook sur le Web (anciennement Outlook Web App). Ce rapport répertorie chaque nom de stratégie et le nombre de communications à chaque étape du processus de révision.
  
Utilisez le rapport pour:
  
- Afficher les données de toutes les stratégies ou des stratégies spécifiques.
- Afficher les données regroupées par type de balise (comme conformité, question, etc.), réviseur ou type de message.
- Exporter des données dans un fichier CSV en fonction de la date de l'activité, de la stratégie et de l'activité du relecteur.
- Filtrer les données en fonction de la date d'activité, du type de balise, du réviseur et du type de message.

Voici une répartition des valeurs que vous pouvez voir dans la colonne **type** de balise.
  
|**Type de balise**|**Signification**|
|:-----|:-----|
| Non révisé | Nombre de messages électroniques qui n'ont pas encore été consultés. Ces messages sont en attente de vérification dans le tableau de bord de supervision Office 365 ou dans le dossier de surveillance du réviseur dans Outlook/Outlook sur le Web
| Compliant | Le nombre de messages vérifiés et marqués comme étant conformes. Ces messages doivent toujours être résolus. |
| Suspects | Le nombre de messages consultés et marqués comme suspects. Cela agit comme un indicateur; d'autres relecteurs peuvent vous aider à vérifier si un message électronique a besoin d'une enquête pour la conformité. Ces messages doivent toujours être résolus. |
| Non conforme (actif) | Nombre de messages électroniques non conformes que les relecteurs examinent actuellement. |
| Non conforme (résolu) | Nombre de messages électroniques non conformes que les relecteurs ont examinés et résolus. |
| Stratégie de correspondance | Nombre total de messages provenant d'Exchange, de teams et de sources de données tierces qui correspondent à une ou plusieurs conditions définies dans une stratégie de surveillance |
| Dans PurVIEW | Nombre total de messages provenant d'Exchange, de teams et de sources de données tierce analysés par une stratégie de surveillance |
| Résolu | Nombre total de messages provenant d'Exchange, de teams et de sources de données tierces qui ont été **** classés comme résolus|

> [!NOTE]
> Les stratégies de surveillance doivent d'abord être mises en service pour qu'elles apparaissent dans ce rapport. En outre, si des stratégies sont supprimées, les données historiques continuent d'apparaître. Toutefois, elles sont indiquées en tant que «stratégie inexistante» et la fonction d' **exportation** n'est pas disponible.

## <a name="auditing"></a>Audit

Dans certains cas, vous devrez fournir des informations aux auditeurs de réglementation ou de conformité pour prouver le contrôle des activités et des communications des employés. Il peut s'agir d'un résumé de toutes les activités de surveillance associées à une stratégie définie ou à chaque fois qu'une stratégie de surveillance a été modifiée ou mise à jour. Les stratégies de surveillance disposent de pistes d'audit intégrées pour une préparation complète des audits internes ou externes. La preuve de procédures de surveillance peut être prouvée avec un historique d'audit détaillé de toutes les actions surveillées par vos stratégies de surveillance.

Les activités de stratégie de surveillance suivantes sont vérifiées et peuvent être consultées à l'aide des journaux d'audit Office 365 unifiés:

|**Activité**|**Commandes associées**|
|:-----|:-----|
| Création d'une stratégie | [New-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2) <br> [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule) |
| Modification d'une stratégie | [Set-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2) <br> [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule) |
| Suppression d'une stratégie| [Remove-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2) |
| Affichage d'une stratégie | [Get-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2) |

Les audits peuvent être récupérés à l'aide de la fonction de recherche de journal d'audit unifiée ou à l'aide de l'applet de commande PowerShell [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) .

Par exemple, l'exemple suivant montre comment renvoyer les activités de toutes les activités de vérification de surveillance (stratégies et règles) et répertorier les informations détaillées pour chacune d'elles:

```
Search-UnifiedAuditLog -StartDate 3/1/2019 -EndDate ([System.DateTime]::Now) -RecordType DataGovernance -ResultSize 5000 | Where-Object {$_.Operations -like "*SupervisoryReview*"}  | fl CreationDate,Operations,UserIds,AuditData
```

Outre les informations fournies dans les journaux et les rapports de surveillance, vous pouvez également utiliser l'applet de commande PowerShell [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity?view=exchange-ps) pour renvoyer une liste complète et détaillée de toutes les activités de stratégie de surveillance.

## <a name="ready-to-get-started"></a>Vous êtes prêt ?

Pour commencer à configurer les stratégies de surveillance pour votre organisation, consultez la rubrique [configurer les stratégies de surveillance](configure-supervision-policies.md).