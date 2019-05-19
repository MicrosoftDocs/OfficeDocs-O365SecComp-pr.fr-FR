---
title: Stratégies de surveillance dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
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
description: En savoir plus sur les stratégies de surveillance dans Office 365
ms.openlocfilehash: 2948cc0440bf481e3f0e90e76a23392233d81cc8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156476"
---
# <a name="supervision-policies-in-office-365"></a>Stratégies de surveillance dans Office 365

Les stratégies de surveillance dans Office 365 vous permettent de capturer les communications des employés pour les examiner par les réviseurs désignés. Vous pouvez définir des stratégies spécifiques qui capturent les messages internes et externes, Microsoft teams ou les communications tierces au sein de votre organisation. Les relecteurs peuvent alors examiner les messages pour s’assurer qu’ils sont conformes aux standards de messages de votre organisation et les résoudre avec le type de classification. 

Ces stratégies peuvent également vous aider à surmonter de nombreux défis de conformité modernes, notamment:

- Surveillance de types croissants de canaux de communication
- Augmentation du volume des données de message
- Respect de la réglementation & risques d’amendes

Dans certaines organisations, le support informatique et le groupe de gestion de la conformité peuvent séparer les tâches. Office 365 prend en charge la séparation entre la configuration de la fonctionnalité de stratégie de surveillance et la configuration des stratégies pour les communications capturées. Par exemple, le groupe informatique d’une organisation peut être responsable de la configuration des autorisations de rôle et des groupes afin de prendre en charge les stratégies de surveillance configurées et gérées par l’équipe de conformité de l’organisation.

Pour obtenir une vue d’ensemble rapide des stratégies de surveillance, voir la vidéo sur la [stratégie de surveillance](https://youtu.be/C3Y8WZ7o_dI) sur le [canal des mécanismes Microsoft](https://www.youtube.com/user/OfficeGarageSeries).

Pour en savoir plus sur les améliorations et la disponibilité des fonctionnalités de surveillance, consultez la feuille de [route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).

## <a name="scenarios-for-supervision-policies"></a>Scénarios de surveillance des stratégies

Les stratégies de surveillance peuvent faciliter la surveillance des communications dans votre organisation dans plusieurs domaines:

- **Stratégies d’entreprise**

    Les employés doivent respecter une utilisation acceptable, des normes éthiques et d’autres stratégies d’entreprise dans toutes leurs communications professionnelles. Les stratégies de surveillance peuvent détecter les violations de stratégie et vous aider à prendre des mesures correctives pour limiter ces types d’incidents. Par exemple, vous pouvez surveiller votre organisation pour détecter les éventuelles violations de ressources humaines telles que le harcèlement ou l’utilisation d’un langage inapproprié ou choquant dans les communications des employés.

- **Gestion des risques**

    Les organisations sont responsables de toutes les communications distribuées au sein de leur infrastructure et des systèmes réseau d’entreprise. L’utilisation de stratégies de surveillance pour aider à identifier et à gérer les risques juridiques et les risques potentiels peut aider à réduire les risques avant qu’ils puissent endommager les opérations de l’entreprise. Par exemple, vous pouvez surveiller votre organisation afin d’obtenir des communications non autorisées pour des projets confidentiels, tels que les acquisitions à venir, les fusions, les informations de résultats, les réorganisations ou les modifications de l’équipe de leadership.

- **Conformité réglementaire**

    La plupart des organisations doivent se conformer à certains types de normes de conformité réglementaire dans le cadre de leurs procédures d’utilisation normales. Ces réglementations obligent souvent les organisations à mettre en place un certain type de processus de surveillance ou de supervision pour la messagerie appropriée pour leur secteur d’activité. La règle 3110 de l’autorité réglementaire du secteur financier (FINRA) est un excellent exemple d’une obligation pour les organisations de mettre en place des procédures de surveillance pour surveiller les activités de ses employés et les types d’entreprises dans lesquelles elle s’engage. Un autre exemple doit être de surveiller les concessionnaires de courtiers de votre organisation afin de se protéger contre les activités potentielles de blanchiment de fonds, de commerce d’initié, de collusion ou de corruption. Les stratégies de surveillance peuvent aider votre organisation à répondre à ces exigences en fournissant un processus à la fois pour surveiller et rendre compte des communications de l’entreprise.

## <a name="components"></a>Components

### <a name="supervision-policy"></a>Stratégie de supervision

Vous créez des stratégies de surveillance dans le centre de conformité. Ces stratégies définissent les communications et les utilisateurs qui font l’objet d’une vérification dans votre organisation, définissent les conditions personnalisées que les communications doivent respecter et spécifie qui doit effectuer des révisions. Les utilisateurs inclus dans le groupe de rôles examen de surveillance peuvent configurer des stratégies et quiconque disposant de ce rôle peut accéder à la page surveillance dans le centre de conformité.

### <a name="supervised-users"></a>Utilisateurs supervisés

Avant de commencer à utiliser la surveillance, vous devez déterminer qui a besoin de ses communications. Dans la stratégie, les adresses de messagerie des utilisateurs identifient des individus ou des groupes de personnes à superviser. Les groupes Office 365, les listes de distribution Exchange et les canaux Microsoft teams sont des exemples de ces groupes. Vous pouvez également exclure des utilisateurs ou des groupes spécifiques de la surveillance avec un groupe supervisé ou une liste de groupes.

> [!IMPORTANT]
> Les utilisateurs surveillés par des stratégies de surveillance doivent disposer d’une licence de conformité Microsoft 365 E5, d’une licence Office 365 entreprise E3 avec le complément de conformité avancé ou être inclus dans un abonnement Office 365 entreprise E5.
Si vous ne disposez pas d’un plan entreprise E5 existant et que vous souhaitez essayer de contrôler, vous pouvez vous [inscrire pour obtenir une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).

### <a name="reviewers"></a>Relecteurs

Lorsque vous créez une stratégie de surveillance, vous devez déterminer qui effectuera les révisions des messages des utilisateurs supervisés. Dans la stratégie, les adresses de messagerie des utilisateurs identifient des personnes ou des groupes de personnes pour examiner les communications surveillées. Tous les relecteurs doivent avoir des boîtes aux lettres hébergées sur Exchange Online.

### <a name="groups-for-supervised-users-and-reviewers"></a>Groupes pour les utilisateurs et les relecteurs surveillés

Pour simplifier votre configuration, créez des groupes pour les personnes qui ont besoin de leurs communications et des groupes pour les personnes qui examinent ces communications. Si vous utilisez des groupes, vous aurez peut-être besoin de plusieurs. Par exemple, si vous souhaitez surveiller les communications entre deux groupes distincts de personnes, ou si vous souhaitez spécifier un groupe qui n’est pas supervisé.

### <a name="supported-communication-types"></a>Types de communication pris en charge

Avec les stratégies de surveillance, vous pouvez choisir de surveiller les messages dans une ou plusieurs des plateformes de communication suivantes:

- **Courrier électronique Exchange:** Les boîtes aux lettres hébergées sur Exchange Online dans le cadre de votre abonnement Office 365 sont toutes éligibles pour la supervision des messages. Les e-mails et les pièces jointes correspondant aux conditions de stratégie de surveillance sont immédiatement disponibles pour la surveillance et les rapports de surveillance. Les types de pièces jointes prises en charge pour la surveillance sont les mêmes que pour les [types de fichiers pris en charge pour les inspections de contenu des règles de flux de messagerie](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection)
- **Microsoft teams:** Les communications de conversation et les pièces jointes associées dans les canaux Microsoft teams publics et privés, ainsi que dans les conversations individuelles, peuvent être surveillées. Les conversations teams correspondant aux conditions de stratégie de contrôle sont traitées une fois toutes les 24 heures, puis disponibles pour la surveillance et les rapports de surveillance. Utilisez les configurations de gestion de groupe suivantes pour superviser les conversations des utilisateurs individuels et les communications de canal dans teams:

    - **Pour la supervision de la conversation teams:** Affectez des utilisateurs individuels ou affectez un [groupe de distribution](https://support.office.com/article/Distribution-groups-E8BA58A8-FAB2-4AAF-8AA1-2A304052D2DE) à la stratégie de surveillance. Il s’agit des relations utilisateur/conversation 1-à-1 ou 1-n.
    - **Pour les communications de canal teams:** Affectez tous les groupes Microsoft Team Channel ou Office 365 que vous souhaitez surveiller, qui contient un utilisateur spécifique à la stratégie de surveillance. Si vous ajoutez le même utilisateur à d’autres canaux Microsoft teams ou à des groupes Office 365, veillez à ajouter ces nouveaux canaux et groupes à la stratégie de surveillance.

- **Sources** tierces: Vous pouvez superviser les communications provenant de sources tierces (par exemple, Facebook ou DropBox) pour les données importées dans les boîtes aux lettres Office 365 de votre organisation. [Découvrez comment importer des données tierces dans Office 365](https://docs.microsoft.com/office365/securitycompliance/archiving-third-party-data).

Les communications capturées sur ces plateformes sont conservées pendant sept ans pour chaque stratégie par défaut, même si les utilisateurs quittent votre organisation et que leur boîte aux lettres est supprimée.

### <a name="policy-settings"></a>Paramètres de stratégie

#### <a name="direction"></a>Direction

Par défaut, la **direction est** la condition est affichée et ne peut pas être supprimée. Les paramètres de direction de communication d’une stratégie sont choisis individuellement ou ensemble:

- **Entrant**: vous pouvez choisir **entrant** pour examiner les communications envoyées **aux** personnes que vous avez choisies de superviser **des** personnes qui ne sont pas incluses dans la stratégie.
- **Sortant**: vous pouvez choisir **sortant** si vous souhaitez consulter les communications envoyées **par** les personnes que vous avez choisies de superviser **aux** personnes qui ne sont pas incluses dans la stratégie.
- **Internal**: vous pouvez choisir **Internal** pour examiner les communications envoyées **entre** les personnes que vous avez identifiées dans la stratégie.

#### <a name="sensitive-information-types"></a>Types d’informations sensibles

Vous pouvez inclure des types d’informations sensibles dans le cadre de votre stratégie de supervision. Les types d’informations sensibles sont des types de données prédéfinis ou personnalisés qui peuvent vous aider à identifier et à protéger les numéros de carte de crédit, les numéros de compte bancaire, les numéros de passeport, et bien plus encore. Dans le cadre de la [protection contre la perte de données (DLP)](data-loss-prevention-policies.md)d’Office 365, la configuration des informations sensibles peut utiliser des modèles, la proximité des caractères, les niveaux de confiance et même les types de données personnalisés pour identifier et marquer le contenu susceptible d’être sensible. Les types d’informations sensibles par défaut sont les suivants:

- Financier
- Médecine et santé
- Confidentialité
- Type d’informations personnalisées

Pour en savoir plus sur les détails des informations sensibles et les modèles inclus dans les types par défaut, consultez la rubrique [types d’informations sensibles](what-the-sensitive-information-types-look-for.md).

#### <a name="custom-keyword-dictionaries"></a>Dictionnaires de mots clés personnalisés

Configurez des dictionnaires de mots clés personnalisés (ou des lexiques) pour fournir une gestion simple des mots clés propres à votre organisation ou votre secteur d’activité. Les dictionnaires de mots clés prennent en charge jusqu’à 100 000 termes par dictionnaire. Si nécessaire, vous pouvez appliquer plusieurs dictionnaires de mots clés personnalisés à une seule stratégie ou disposer d’un dictionnaire à Mots clés unique par stratégie. Ces dictionnaires sont affectés dans une stratégie de surveillance et peuvent être issus d’un fichier (par exemple, une liste. csv ou. txt) ou d’une liste que vous pouvez [importer dans le centre de conformité](create-a-keyword-dictionary.md).

#### <a name="offensive-language"></a>Choquant

Surveiller les messages électroniques envoyés ou reçus dans votre organisation pour une langue offensante. Le modèle utilise une combinaison d’apprentissage automatique, d’intelligence artificielle et de mots-clés pour identifier les messages électroniques inappropriés dans le cadre des exigences de surveillance du blocage du courrier indésirable et de la intimidation. Pour empêcher ou bloquer le langage offensant pour les autres communications au sein de votre organisation, créez une [stratégie de protection contre la perte de données](create-test-tune-dlp-policy.md) qui utilise un dictionnaire de [Mots clés](create-a-keyword-dictionary.md) choquant.

Le modèle de langage offensant prend actuellement en charge les mots clés anglais et surveille le corps des messages électroniques. Le modèle de langage offensant surveille le courrier électronique en fonction des types de langue suivants:

|**Type**|**Description**|
|:-----|:-----|
| **Blasphèmes** | Expressions inappropriées et gênantes pour la plupart des gens. |
| **Slurs** | Expressions qui attaquent les cultures et les ethniques. |
| **Taunts** | Expressions que taunt, condemn et ridicule. |
| **Références aux handicaps** | Expressions qui ciblent les handicaps physiques ou mentaux. |
| **Langue Squalid** | Expressions qui ciblent les intérêts sexuels et l’état physique de la propreté. |
| **Homophobia** | Expressions qui ciblent les préférences sexuelles. |
| **Racist** | Expressions qui ciblent la race et la ethnique. |
| **Extrémité** | Expressions qui ciblent la religion et les Ideologies politiques. |
| **Simul** | Expressions pour lesquelles la signification ou la prononciation est identique à celle d’un autre terme offensant. |
| **Langue Provocative** | Expressions susceptibles de provoquer une Anger ou une violence. |
| **Taboo** | Expressions généralement inappropriées dans les communications sociales polies. |
| **Langue inraffinée** | Expressions qui manquent de manière cohérente et qui sont potentiellement extrêmes et impropres. |

#### <a name="conditional-settings"></a>Paramètres conditionnels

Les conditions que vous choisissez pour la stratégie s’appliquent aux communications à partir de la messagerie et des sources tierces de votre organisation (par exemple, Facebook ou DropBox).

Le tableau suivant décrit plus en plus de chaque condition.
  
|**Condition**|**Comment utiliser cette condition ?**|
|:-----|:-----|
| **Un message est reçu à partir de l’un de ces domaines**  <br><br> **Le message n’est reçu à partir d’aucun de ces domaines** | Pour appliquer la stratégie lorsque certains domaines sont inclus ou exclus d’un message reçu, entrez chaque domaine et plusieurs domaines séparés par une virgule. Chaque domaine que vous entrez est appliqué séparément (un seul de ces domaines doit s’appliquer à la stratégie à appliquer au message). |
| **Un message est envoyé à l’un de ces domaines**  <br><br> **Le message n’est pas envoyé à l’un de ces domaines** | Pour appliquer la stratégie lorsque certains domaines sont inclus ou exclus d’un message envoyé, entrez chaque domaine et plusieurs domaines séparés par une virgule. Chaque domaine que vous entrez sera appliqué séparément (un seul de ces domaines doit s’appliquer à la stratégie à appliquer au message). |
| **Le message est classé avec l’une de ces étiquettes**  <br><br> **Le message n’est classé avec aucune de ces étiquettes** | Pour appliquer la stratégie lorsque certaines étiquettes de rétention sont incluses ou exclues dans un message. Les étiquettes de rétention doivent être configurées séparément et les étiquettes configurées dans le cadre de cette condition. Chaque étiquette que vous choisissez est appliquée séparément (une seule de ces étiquettes doit s’appliquer pour la stratégie à appliquer au message). Pour plus d’informations sur la configuration des étiquettes de rétention, consultez la rubrique [vue d’ensemble des étiquettes de](https://docs.microsoft.com/office365/securitycompliance/labels)rétention.|
| **Le message contient l’un de ces mots**  <br><br> **Le message ne contient aucun de ces mots** | Pour appliquer la stratégie lorsque certains mots ou expressions sont inclus ou exclus dans un message, entrez chaque mot ou expression sur une ligne distincte. Chaque ligne de mots que vous entrez est appliquée séparément (une seule de ces lignes doit s’appliquer à la stratégie à appliquer au message). Pour plus d’informations sur la saisie des mots ou des expressions, voir la section suivante [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
| **La pièce jointe contient l’un de ces mots**  <br><br> **La pièce jointe ne contient aucun de ces mots** | Pour appliquer la stratégie lorsque certains mots ou expressions sont inclus ou exclus dans une pièce jointe (par exemple, un document Word), entrez chaque mot ou expression sur une ligne distincte. Chaque ligne de mots que vous entrez est appliquée séparément (une seule ligne doit s’appliquer à la stratégie à appliquer à la pièce jointe). Pour plus d’informations sur la saisie des mots ou des expressions, voir la section suivante [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
| **La pièce jointe est l’un de ces types de fichiers**  <br><br> **Aucune de ces types de fichiers n’est associée à la pièce jointe** | Pour superviser les communications qui incluent ou excluent des types spécifiques de pièces jointes, entrez les extensions de fichiers (par exemple,. exe ou. pdf). Si vous souhaitez inclure ou exclure plusieurs extensions de fichiers, entrez-les sur des lignes distinctes. Il suffit que l’extension d’une seule pièce jointe corresponde pour que la stratégie s’applique.|
| **La taille du message est supérieure à**  <br><br> **La taille du message n’est pas supérieure à** | Pour examiner les messages en fonction d’une certaine taille, utilisez les conditions suivantes pour spécifier la taille maximale ou minimale qu’un message peut contenir avant d’être soumis à révision. Par exemple, si vous spécifiez une **taille de message supérieure à** \> **1,0 Mo**, tous les messages de 1,01 Mo et plus sont soumis à révision. Vous pouvez choisir des octets, kilo-octets, mégaoctets ou gigaoctets pour cette condition.|
| **La taille de la pièce jointe est supérieure à**  <br><br> **La pièce jointe n’est pas supérieure à** | Pour examiner les messages en fonction de la taille de leurs pièces jointes, spécifiez la taille maximale ou minimale qu’une pièce jointe peut contenir avant que le message et ses pièces jointes soient soumis à révision. Par exemple, si vous spécifiez une **taille de pièce jointe supérieure** \> à **2,0 Mo**, tous les messages avec des pièces jointes 2,01 Mo et supérieures sont soumis à la révision. Vous pouvez choisir des octets, kilo-octets, mégaoctets ou gigaoctets pour cette condition.|
   
##### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Correspondance de mots et expressions avec des courriers électroniques ou des pièces jointes
<a name="Matchwords"></a> Chaque ligne de mots que vous entrez est appliquée séparément (une seule ligne doit s’appliquer à la condition de stratégie à appliquer à l’e-mail ou à la pièce jointe). Par exemple, nous utilisons la condition, le **message contient l’un de ces mots**, avec les mots-clés «Banker» et «negociing Insider» sur des lignes distinctes. La stratégie s’applique aux messages qui incluent le mot «Banker» ou l’expression «negociation Insiders». Un seul de ces mots ou expression doit être présent pour que cette condition de stratégie s’applique. Les mots contenus dans le message ou dans la pièce jointe doivent correspondre exactement à ce que vous entrez.
  
##### <a name="enter-multiple-conditions"></a>Entrer plusieurs conditions

Si vous entrez plusieurs conditions, Office 365 utilise toutes les conditions ensemble pour déterminer le moment auquel appliquer la stratégie aux éléments de communication. Lorsque vous configurez plusieurs conditions, elles doivent toutes être remplies pour que la stratégie s’applique, sauf si vous entrez une exception. Par exemple, vous devez créer une stratégie qui s’applique si un message contient le mot «commercial» et est supérieur à 2 Mo. Toutefois, si le message contient également les mots «approuvé par Contoso Financial», la stratégie ne doit pas s’appliquer. Ainsi, dans ce cas, les trois conditions suivantes sont les suivantes:
  
- Le **message contient l’un de ces mots**, avec les mots clés «Trade»

- La **taille du message est supérieure à**, avec la valeur 2 Mo

- Le **message ne contient aucun de ces mots**, avec les mots-clés «approuvé par l’équipe financière de contoso»

#### <a name="review-percentage"></a>Vérifier le pourcentage

Si vous souhaitez réduire la quantité de contenu à réviser, vous pouvez spécifier un pourcentage de toutes les communications régies par une stratégie de surveillance. Un échantillon aléatoire de contenu en temps réel est sélectionné à partir du pourcentage total de contenu qui correspond aux conditions de stratégie choisies. Si vous souhaitez que les relecteurs examinent tous les éléments, vous pouvez entrer **100%** dans une stratégie de surveillance.

## <a name="monitor--manage"></a>Surveiller & gérer

Il est facile de surveiller les résultats de vos stratégies de surveillance et d’appliquer une balise de résolution. Vous pouvez rapidement voir l’état des éléments vérifiés, les utilisateurs et les groupes sous surveillance, ainsi que les utilisateurs et les groupes désignés comme relecteurs.

### <a name="supervision-policy-dashboard"></a>Tableau de bord de stratégie de supervision

Utilisez le tableau de bord de stratégie de supervision pour gérer les résultats de stratégie de surveillance et résoudre les éléments non traités. Ce tableau de bord permet aux relecteurs d’afficher les éléments devant être vérifiés, d’effectuer des actions sur un élément et de passer en revue les résultats des éléments précédemment examinés et résolus pour chaque stratégie de surveillance. Vous pouvez accéder au tableau de bord de stratégie de supervision dans le centre de conformité à**** la **surveillance** > de*votre stratégie* > personnalisée.

#### <a name="dashboard-home"></a>Accueil du tableau de bord

La page d' **Accueil** du tableau de bord comporte plusieurs sections qui vous permettent d’effectuer rapidement des actions sur vos stratégies de surveillance. Ici, vous pouvez:

- Vérifier rapidement les points forts en attente et résolus pour la semaine
- Afficher la liste des utilisateurs et des groupes supervisés de la stratégie sélectionnée
- Afficher une liste des relecteurs et vérifier les équipes pour la stratégie sélectionnée
- Voir les plateformes de communication dont le contenu est sous surveillance pour la stratégie

#### <a name="review-tab"></a>Onglet révision

L’onglet **révision** permet de classer et de résoudre les éléments identifiés par la stratégie sélectionnée. Ici, vous pouvez:

- Filtrer les éléments en attente, conformes, non conformes et douteux.
- Baliser un élément unique comme étant conforme, non conforme ou douteable. Vous pouvez également enregistrer un commentaire avec l’élément pour clarifier l’action de marquage effectuée.
- Balise en bloc plusieurs éléments comme conformes, non conformes ou douteux. Vous pouvez également enregistrer un commentaire avec plusieurs éléments pour clarifier l’action de marquage effectuée.
- Afficher l’historique du balisage pour un seul élément. Il s’agit notamment de la personne qui a résolu l’élément, de la date et de l’heure de l’action, de la balise de résolution et de tous les commentaires inclus.
- Reclassez les éléments consultés précédemment comme conformes, non conformes ou douteux. Vous pouvez également enregistrer un commentaire avec un ou plusieurs éléments afin de clarifier l’action de reclassification effectuée.

#### <a name="resolved-items-tab"></a>Onglet éléments résolus

L’onglet **éléments résolus** permet aux relecteurs d’afficher tous les éléments précédemment résolus pour la stratégie sélectionnée. Ici, vous pouvez:

- Affichage et tri rapides de l’objet, de l’expéditeur et de la date des éléments résolus
- Afficher l’historique de classification et de commentaire d’un élément sélectionné

## <a name="reports"></a>Rapports

Utilisez les rapports de surveillance pour afficher l’activité de révision au niveau de la stratégie et du réviseur. Pour chaque stratégie, vous pouvez également afficher des statistiques réelles sur l’état actuel de l’activité de révision. Vous pouvez utiliser les rapports de surveillance pour:
  
- Vérifiez que vos stratégies fonctionnent comme prévu.
- Déterminer le nombre de communications requises.
- Déterminez le nombre de communications non conformes et celles qui passent la révision. Ces informations peuvent vous aider à décider s’il faut affiner vos stratégies ou modifier le nombre de relecteurs.

### <a name="view-the-supervision-report"></a>Afficher le rapport de supervision

1. Connectez-vous au [Centre de conformité](https://compliance.microsoft.com) avec les informations d’identification d’un compte d’administrateur de votre organisation disposant des autorisations pour afficher les rapports de surveillance.
2. Accédez au **tableau de bord** **rapports** \> ou à la **surveillance** pour afficher le widget rapports de supervision avec une synthèse de l’activité de stratégie de surveillance actuelle.
3. Sélectionnez le widget **surveillance** pour ouvrir la page rapport détaillé.

> [!NOTE]
> Si vous ne parvenez pas à accéder à la page **rapports** , vérifiez que vous êtes membre du groupe de rôles examen de surveillance, comme décrit dans la rubrique [création d’un contrôle disponible dans votre organisation](configure-supervision-policies.md). L’inclusion dans ce groupe de rôles vous permet de créer et de gérer des stratégies de surveillance et d’exécuter le rapport.
  
### <a name="how-to-use-the-report"></a>Utilisation du rapport

Ce rapport répertorie chaque stratégie et le nombre de communications à chaque étape du processus de révision. Utilisez le rapport pour:
  
- Afficher les données de toutes les stratégies ou des stratégies spécifiques.
- Afficher les données regroupées par type de balise, réviseur ou type de message.
- Exporter des données dans un fichier CSV en fonction de la date de l’activité, de la stratégie et de l’activité du relecteur.
- Filtrer les données en fonction de la date d’activité, du type de balise, du réviseur et du type de message.

Voici une répartition des valeurs affichées dans la colonne **type** de balise.
  
|**Type de balise**|**Signification**|
|:-----|:-----|
| **Non révisé** | Nombre d’e-mails non vérifiés. Ces messages sont en attente de révision dans le tableau de bord de supervision Office 365.
| **Compliant** | Le nombre de messages vérifiés et marqués comme étant conformes. Ces messages nécessitent toujours une résolution. |
| **Suspects** | Le nombre de messages consultés et marqués comme suspects. Cela sert d’indicateur pour les autres réviseurs afin de vérifier si un message électronique a besoin d’une enquête pour la conformité. Ces messages nécessitent toujours une résolution. |
| **Non conforme (actif)** | Nombre de messages électroniques non conformes que les relecteurs examinent actuellement. |
| **Non conforme (résolu)** | Nombre de messages électroniques non conformes que les relecteurs ont examinés et résolus. |
| **Stratégie de correspondance** | Nombre total de messages provenant d’Exchange, de teams et de sources de données tierces qui correspondent à une ou plusieurs conditions définies dans une stratégie de surveillance |
| **Dans PurVIEW** | Nombre total de messages provenant d’Exchange, de teams et de sources de données tierce analysés par une stratégie de surveillance |
| **Resolved** | Nombre total de messages provenant d’Exchange, de teams et de sources de données tierces **** classées comme résolus|

> [!NOTE]
> Les stratégies de surveillance doivent d’abord être mises en service pour qu’elles apparaissent dans ce rapport. En outre, si des stratégies sont supprimées, les données historiques continuent d’apparaître. Toutefois, elles sont indiquées en tant que «stratégie inexistante» et la fonction d' **exportation** n’est pas disponible.

## <a name="audit"></a>Contrôlé

Dans certains cas, vous devez fournir des informations aux auditeurs de réglementation ou de conformité pour prouver le contrôle des activités et des communications des employés. Il peut s’agir d’un résumé de toutes les activités de surveillance associées à une stratégie définie ou à chaque fois qu’une stratégie de surveillance est modifiée. Les stratégies de surveillance disposent de pistes d’audit intégrées pour une préparation complète des audits internes ou externes. Des historiques d’audit détaillés de toutes les actions surveillées par vos stratégies de surveillance fournissent des preuves de procédures de surveillance.

Les activités de stratégie de surveillance suivantes sont vérifiées et disponibles dans les journaux d’audit Office 365 unifiés:

|**Activité**|**Commandes associées**|
|:-----|:-----|
| **Créer une stratégie** | [New-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2) <br> [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule) |
| **Modifier une stratégie** | [Set-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2) <br> [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule) |
| **Suppression d’une stratégie** | [Remove-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2) |
| **Afficher une stratégie** | [Get-Supervisoryreviewpolicyv2 permet](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2) |

Afficher les activités d’audit dans le journal d’audit unifié ou avec l’applet de commande PowerShell [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) .

Par exemple, l’exemple suivant montre comment renvoyer les activités de toutes les activités de vérification de surveillance (stratégies et règles) et répertorier les informations détaillées pour chacune d’elles:

```
Search-UnifiedAuditLog -StartDate 3/1/2019 -EndDate ([System.DateTime]::Now) -RecordType DataGovernance -ResultSize 5000 | Where-Object {$_.Operations -like "*SupervisoryReview*"}  | fl CreationDate,Operations,UserIds,AuditData
```

Outre les informations fournies dans les journaux et les rapports de surveillance, vous pouvez également utiliser l’applet de commande PowerShell [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity?view=exchange-ps) pour renvoyer une liste complète et détaillée de toutes les activités de stratégie de surveillance.

## <a name="ready-to-get-started"></a>Vous êtes prêt ?

Pour commencer à configurer les stratégies de surveillance pour votre organisation, consultez la rubrique [configurer les stratégies de surveillance](configure-supervision-policies.md).