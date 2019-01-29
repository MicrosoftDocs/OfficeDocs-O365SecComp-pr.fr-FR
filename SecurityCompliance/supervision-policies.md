---
title: Stratégies de surveillance dans Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Présentation des stratégies de surveillance dans Office 365
ms.openlocfilehash: 0c76ba5b17277d8bd441810415e7e9acd1adbf36
ms.sourcegitcommit: 3cb775e60b3806b66568ed2f9664c17ef96ca8de
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2019
ms.locfileid: "29603524"
---
# <a name="supervision-policies-in-office-365"></a>Stratégies de surveillance dans Office 365

Stratégies de surveillance dans Office 365 permettent de capturer les communications des employés pour l’examen des réviseurs désignés. Vous pouvez définir des stratégies spécifiques à capturer e-mail interne et externe, Teams Microsoft ou tiers-3 rd communications dans votre organisation. Relecteurs peuvent ensuite examiner les messages pour vous assurer qu’ils sont conformes aux normes de votre organisation et résolvez-les avec un type de classification. Ces stratégies peuvent également vous aider à résoudre de nombreux défis de conformité moderne, y compris la surveillance des types augmentation des canaux de communication, augmentation du volume de données de message et l’application de la réglementation & le risque d’amendes.

Dans certaines organisations, il peut être une séparation des tâches entre la prise en charge de l’informatique et le groupe de gestion de la conformité. Office 365 prend en charge la séparation de configuration du client avec prise en charge des fonctionnalités de la stratégie de surveillance et la configuration des stratégies et agissant sur les communications capturées. Par exemple, le groupe IT pour une organisation peut être chargé de définir les autorisations de rôle et les groupes pour prendre en charge les stratégies de surveillance qui sont configurés et gérés par l’équipe de conformité de l’organisation.

## <a name="scenarios-for-supervision-policies"></a>Scénarios de stratégies de surveillance

Stratégies de surveillance peuvent aider les communications de surveillance dans votre organisation dans plusieurs domaines :

- **Stratégies d’entreprise**

    Les employés doivent être conformes à bon usage, des normes éthiques et autres stratégies d’entreprise dans toutes leurs communications professionnelles. Stratégies de surveillance peuvent détecter les violations de stratégie et vous aider à prendre des mesures correctives pour atténuer ces types d’incidents. Par exemple, vous pouvez contrôler votre organisation pour les violations de ressources humaines potentiels comme harcèlement ou l’utilisation du langage inapproprié ou choquant dans les communications des employés.

- **Gestion des risques**

    Organisations sont chargées pour toutes les communications sont distribuées au sein de leur infrastructure et les systèmes de réseau d’entreprise. À l’aide de stratégies de surveillance pour aider à identifier et gérer les risques et les risques juridiques peut aider à réduire les risques avant qu’ils peuvent endommager les opérations d’entreprise. Par exemple, vous pouvez contrôler votre organisation pour les communications non autorisées pour les projets confidentielles comme acquisitions à venir, fusions, aux divulgations comme bénéfices, réorganisation ou des modifications de l’équipe de direction.

- **Conformité aux exigences réglementaires**

    La plupart des organisations doivent être conformes à un type de normes réglementaires dans le cadre de leurs procédures de fonctionnement normales. Ces réglementations requièrent souvent que les organisations à implémenter un certain type de surveillance ou processus supervision de messagerie qui est approprié pour son activité. La règle de financières du secteur réglementaires autorité (FINRA) 3110 est un bon exemple d’une condition requise pour les organisations à avoir des procédures de surveillance en place pour surveiller les activités de ses employés et les types d’entreprises dans lequel elle s’exécute automatiquement. Un autre exemple peut être nécessaire pour surveiller la courtiers dans votre organisation pour remédier à blanchiment potentiel, initiés, collusion ou activités corruption. Stratégies de surveillance peuvent aider votre organisation à répondre à ces exigences en fournissant un processus à surveiller et rapport de communications d’entreprise.

## <a name="feature-components"></a>Composants de la fonctionnalité

### <a name="supervision-policy"></a>Stratégie de surveillance

Vous allez créer des stratégies de surveillance dans le centre de conformité de & sécurité. Ces stratégies définissent les communications et les utilisateurs sont soumis à la révision de votre organisation, définir des conditions personnalisées que les communications doit respecter et spécifie qui doit effectuer des analyses. Utilisateurs inclus dans le groupe de rôles permettre définir les stratégies et toute personne qui a été attribué de ce rôle de supervision peuvent accéder à la page surveillance sous la gouvernance des données dans le centre de conformité de & Office 365 sécurité.

### <a name="supervised-users"></a>Utilisateurs contrôlés

Avant de commencer à l’aide de surveillance, vous devez déterminer les utilisateurs qui auront leurs communications révisées. Dans la stratégie, vous allez utiliser des adresses de messagerie d’utilisateur pour identifier des utilisateurs individuels ou des groupes de personnes à contrôler. Quelques exemples de ces groupes sont des canaux Teams Microsoft Office 365 groupes et listes de distribution basée sur Exchange. Vous pouvez également exclure des utilisateurs ou groupes spécifiques de surveillance qui sont inclus dans un groupe contrôlé ou une liste de groupes.

> [!IMPORTANT]
> Tous les utilisateurs sont contrôlés par des stratégies de surveillance doivent avoir une licence d’Office 365 entreprise E3 avec le module complémentaire de conformité avancée ou être inclus dans un abonnement à Office 365 entreprise E5. Si vous n’avez un plan d’entreprise E5 existant et essayer de surveillance, vous pouvez [inscrire à une version d’évaluation d’Office 365 entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).

### <a name="reviewers"></a>Relecteurs

Lorsque vous créez une stratégie de surveillance, vous devez également déterminer qui effectuera l’avis des messages des utilisateurs contrôlés. Dans la stratégie, vous allez utiliser des adresses de messagerie d’utilisateur pour identifier des utilisateurs individuels ou des groupes de personnes pour passer en revue les communications contrôlées.

### <a name="groups-for-supervised-users-and-reviewers"></a>Groupes d’utilisateurs contrôlés et des relecteurs

Pour simplifier votre installation, créez des personnes disposant de leurs communications révisée et les groupes pour les personnes qui validera les communications. Si vous utilisez des groupes, vous devrez peut-être plusieurs. Par exemple, si vous souhaitez surveiller les communications entre les deux groupes distincts de personnes, ou si vous souhaitez spécifier un groupe qui n’est pas sur le point d’être surveillés.

### <a name="supported-communication-types"></a>Types de communication pris en charge

Avec les stratégies de surveillance, vous pouvez choisir d’analyser les messages dans une ou plusieurs des plateformes suivantes :

- **Échanger des courriers électroniques :** Boîtes aux lettres qui sont hébergées sur Exchange Online dans le cadre de votre abonnement Office 365 sont tous les éligibles pour la surveillance de message. Les messages électroniques et les pièces jointes correspondant à des conditions de stratégie de surveillance sont immédiatement disponibles pour la surveillance et dans les rapports de surveillance. Types de pièce jointe pris en charge sont les suivants :

    - Microsoft Word (.docx)
    - Microsoft Excel (.xlsx)
    - Microsoft PowerPoint (.pptx)

- **Équipes Microsoft :** Communications de conversation et les pièces jointes publiques et privées canaux Teams Microsoft et de salles de conversation individuelles peuvent être surveillés. Conversations équipes correspondant à des conditions de stratégie de surveillance sont traitées toutes les 24 heures, puis sont disponibles pour la surveillance et dans les rapports de surveillance.
- **Sources tierces :** Vous pouvez contrôler les communications à partir de sources de tiers (comme à partir de Facebook ou échange) si vous avez importé ces données dans les boîtes aux lettres Office 365 dans votre organisation. [Découvrez comment importer des données de 3 rd tiers dans Office 365](https://docs.microsoft.com/office365/securitycompliance/archiving-third-party-data).

### <a name="policy-settings"></a>Paramètres de stratégie

#### <a name="direction"></a>Direction (Sens)

Par défaut, la condition de **Direction est** s’affiche et ne peut pas être supprimée. Paramètres de direction de communication d’une stratégie peuvent être sélectionnés individuellement ou ensemble :

- **Entrant** - vous pouvez choisir **entrant** pour passer en revue les communications sont envoyées **aux** personnes que vous avez choisi pour le contrôle **de** personnes non inclus dans la stratégie.
- **Sortant** - vous pouvez choisir **sortant** si vous souhaitez examiner les communications sont envoyées **à partir de** personnes que vous avez choisi pour le contrôle **à** d’autres personnes non inclus dans la stratégie.
- **Internal** - vous pouvez choisir **interne** pour passer en revue les communications envoyées **entre** les personnes que vous avez identifié dans la stratégie.

#### <a name="sensitive-information-types"></a>Types d’informations sensibles

Vous avez la possibilité d’inclure les types d’informations sensibles dans le cadre de votre stratégie de surveillance. Types d’informations sensibles sont deux types de données prédéfinis ou personnalisés qui peuvent aider à identifier et protéger les numéros de carte de crédit, numéros de compte bancaire, numéros de passeport et bien plus encore. Dans le cadre d’Office 365 [prévention des pertes de données (DLP)](data-loss-prevention-policies.md), la configuration des informations sensibles permettre tirer parti de modèles, proximité de caractère, niveaux de confiance et les types de données personnalisés pour aider à identifier et marquer le contenu qui peut-être être sensible. Les types d’informations sensibles par défaut sont les suivants :

- Financiers
- Médecine et santé
- Politique de confidentialité
- Type d’informations personnalisées

Pour en savoir plus sur les informations sensibles et les modèles inclus dans les types par défaut, voir [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).

#### <a name="custom-keyword-dictionaries"></a>Dictionnaires personnalisés de mot clé

Configuration des dictionnaires personnalisés de mot clé (ou lexiques) peuvent fournir une gestion simple de mots clés spécifiques à votre organisation ou d’un secteur d’activité et peut prendre en charge jusqu'à 100 000 termes par dictionnaire. Si nécessaire, vous pouvez appliquer plusieurs dictionnaires personnalisés de mot clé à une stratégie unique ou un dictionnaire de mot clé unique par stratégie. Ces dictionnaires sont affectées dans une stratégie de surveillance et peuvent provenir d’un fichier (tel qu’une liste .csv ou .txt), ou d’une liste, vous pouvez [entrer directement dans une applet de commande PowerShell](create-a-keyword-dictionary.md).

#### <a name="conditional-settings"></a>Paramètres conditionnels

Les conditions que vous choisissez pour la stratégie seront appliquera aux communications à partir de sources de courrier électronique et 3 rd tiers dans votre organisation (par exemple avec Facebook ou échange).

Le tableau suivant explique plus sur chaque condition.
  
|**Condition**|**Comment utiliser cette condition ?**|
|:-----|:-----|
|Message est reçu à partir de ces domaines  <br><br> Message n’est pas reçu à partir de ces domaines | Pour appliquer la stratégie de certains domaines inclus ou exclus dans un message reçu, entrez chaque domaine et Séparez plusieurs domaines par une virgule. Chaque domaine que vous entrez sera appliquée séparément (un seul de ces domaines doit s’appliquer de la stratégie à appliquer au message). |
|Message est envoyé à une de ces domaines  <br><br> Message n’est pas envoyé à une de ces domaines | Pour appliquer la stratégie de certains domaines inclus ou exclus dans un message envoyé, entrez chaque domaine et Séparez plusieurs domaines par une virgule. Chaque domaine que vous entrez sera appliquée séparément (un seul de ces domaines doit s’appliquer de la stratégie à appliquer au message). |
|Message est classé avec l’une de ces étiquettes  <br><br> Message est classé pas avec l’une de ces étiquettes | Pour appliquer la stratégie lors de certaines étiquettes de rétention sont inclus ou exclus dans un message. Étiquettes de rétention doivent être configurés séparément et étiquettes configurés peuvent être choisies dans le cadre de cette condition. Chaque étiquette que vous choisissez sera appliqué séparément (un seul de ces étiquettes doit s’appliquer de la stratégie à appliquer au message). Pour plus d’informations sur la configuration des étiquettes de rétention, voir [vue d’ensemble des étiquettes de rétention](https://docs.microsoft.com/office365/securitycompliance/labels).|
|Le message contient un de ces mots  <br><br> Message ne contient aucun de ces mots | Pour appliquer la stratégie des mots ou des expressions incluses ou exclues dans un message, entrez chaque mot ou expression sur une ligne distincte. Chaque ligne de mots que vous entrez sera appliquée séparément (un seul de ces lignes doit s’appliquer de la stratégie à appliquer au message). Pour plus d’informations sur la saisie des mots ou expressions, consultez la section suivante, [mise en correspondance des mots et expressions pour les messages électroniques ou des pièces jointes](supervision-policies.md#Matchwords).|
|Pièce jointe contient l’un de ces mots  <br><br> Pièce jointe ne contient aucun de ces mots | Pour appliquer la stratégie des mots ou des expressions incluses ou exclues dans une pièce jointe du message (par exemple un document Word), entrez chaque mot ou expression sur une ligne distincte. Chaque ligne de mots que vous entrez sera appliquée séparément (une seule ligne doit s’appliquer de la stratégie à appliquer à la pièce jointe). Pour plus d’informations sur la saisie des mots ou expressions, consultez la section suivante, [mise en correspondance des mots et expressions pour les messages électroniques ou des pièces jointes](supervision-policies.md#Matchwords).|
|Pièce jointe est une de ces types de fichiers  <br><br> Pièce jointe est aucun de ces types de fichier | Pour contrôler les communications qui inclure ou exclure des types de pièces jointes spécifiques, entrez les extensions de fichier (par exemple .exe ou .pdf). Si vous souhaitez inclure ou exclure plusieurs extensions de fichier, entrez ces sur des lignes distinctes. Extension qu’une pièce jointe doit correspondre pour appliquer la stratégie.|
|La taille du message est supérieure à  <br><br> Taille du message n’est pas supérieure | Pour passer en revue les messages à partir d’une certaine taille, utilisez ces conditions pour spécifier la taille minimale ou maximale, qu'un message peut être avant d’être soumis à révision. Par exemple, si vous spécifiez la **taille du Message est supérieure à** \> **Mo 1.0**, tous les messages qui sont 1,01 Mo et plus faire l’objet de révision. Vous pouvez choisir d’octets, kilo-octets, mégaoctets ou gigaoctets pour cette condition.|
|Pièce jointe est supérieure à  <br><br> Pièce jointe n’est pas supérieure | Pour passer en revue les messages en fonction de la taille de leurs pièces jointes, spécifiez la taille minimale ou maximale une pièce jointe peut être avant le message et ses pièces jointes sont soumis à révision. Par exemple, si vous spécifiez la **pièce jointe est supérieure à** \> **Mo 2.0**, tous les messages avec pièces jointes Mo 2.01 et sera plu faire l’objet de révision. Vous pouvez choisir d’octets, kilo-octets, mégaoctets ou gigaoctets pour cette condition.|
   
##### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Correspondance de mots et expressions avec des courriers électroniques ou des pièces jointes
<a name="Matchwords"> </a>

Chaque ligne de mots que vous entrez sera appliquée séparément (une seule ligne doit appliquer pour la condition de stratégie à appliquer au courrier électronique ou pièce jointe). Par exemple, nous allons utiliser la condition, **que le Message contient un de ces mots**, bancaire « mots clés » et « initiés » sur des lignes distinctes. La stratégie s’applique à tous les messages qui inclut le bancaire « word » ou la phrase « initiés ». Un seul de ces mots ou phrases doit se produire pour cette condition de stratégie s’applique. Mots dans le message ou d’une pièce jointe doivent correspondre exactement ce que vous entrez.
  
##### <a name="entering-multiple-conditions"></a>Saisie de plusieurs conditions

Si vous entrez plusieurs conditions, Office 365 utilise conjointement toutes les conditions pour déterminer le moment auquel appliquer la stratégie aux éléments de communication. Lorsque vous configurez plusieurs conditions, ils doivent tous les être remplies pour la stratégie à appliquer, sauf si vous entrez une exception. Par exemple, supposons que vous avez besoin créer une stratégie qui doit s’appliquer si un message contient le mot « Commerce » et est supérieur à 2 Mo. Toutefois, si le message contient également les mots « Approuvé par Contoso financière », la stratégie doit s’applique pas. Par conséquent, dans ce cas, les trois conditions serait comme suit :
  
- **Le message contient un de ces mots**, avec les mots clés « Commerce »

- **Taille du message est supérieure**, avec la valeur 2 Mo

- **Message ne contient aucun de ces mots**, avec les mots clés « Approuvé par l’équipe financière Contoso ».

#### <a name="review-percentage"></a>Pourcentage de révision

Vous pouvez spécifier un pourcentage de toutes les communications régi par une stratégie de surveillance si vous souhaitez réduire la quantité de contenu pour passer en revue. Sélectionnez aléatoire que quantité de contenu à partir du pourcentage total qui remplissent les conditions que vous avez choisi. Si vous souhaitez que les relecteurs pour passer en revue tous les éléments, vous pouvez entrer **100 %** d’une stratégie de surveillance.

## <a name="monitoring--managing"></a>Gestion des & de surveillance

Les résultats de vos stratégies de contrôle de surveillance et application d’une balise de résolution sont facile et pratique. Vous pouvez voir rapidement l’état des éléments révisés, les utilisateurs et groupes sous contrôle et utilisateurs et des groupes désignés en tant que réviseurs.

### <a name="supervision-policy-dashboard"></a>Tableau de bord stratégie de surveillance

Le moyen le plus simple pour gérer les résultats de stratégie de surveillance et résoudre les éléments en suspens consiste à utiliser le tableau de bord de stratégie de surveillance. Ce tableau de bord permet aux réviseurs voir rapidement les éléments qui doivent être examinées, effectuer une action sur un élément et passez en revue les résultats de précédemment examiné et résolu les éléments pour chaque stratégie de surveillance. Vous pouvez accéder à du tableau de bord de stratégie de surveillance dans le centre de conformité au niveau de la **surveillance**de & Office 365 sécurité > *Votre stratégie personnalisée* > **Open**.

#### <a name="dashboard-home"></a>Accueil du tableau de bord

La page tableau de bord **d’accueil** comporte plusieurs sections pour vous aider à effectuer une action rapidement vos stratégies de surveillance. Ici, vous pouvez :

- Révision en attente et résolue met en évidence pour la semaine
- Afficher la liste des utilisateurs contrôlés et des groupes personnalisés pour la stratégie sélectionnée
- Afficher la liste des relecteurs, passez en revue les équipes pour la stratégie sélectionnée
- Voir les plateformes ont contenu sous contrôle de la stratégie.

#### <a name="supervise-tab"></a>Contrôle onglet

L’onglet **Supervise** où relecteurs peuvent prendre des mesures et résoudre les éléments identifié par la stratégie sélectionnée. Ici, vous pouvez :

- Filtrer les éléments en attente, conformes, non conforme et suspects à
- Ajouter une balise à un seul élément conforme, non conforme ou suspects. Vous pouvez également enregistrer un commentaire avec l’élément pour clarifier l’action de liaison.
- Ajouter une balise en bloc plusieurs éléments suspects, conforme ou non conforme. Vous pouvez également enregistrer un commentaire avec plusieurs éléments pour clarifier l’action de liaison.
- Afficher l’historique de la liaison d’un seul élément, y compris la personne qui a résolu l’élément, la date et l’heure de l’action, la balise de résolution et des commentaires inclus.
- Reclasser précédemment passé en revue les éléments suspects, conforme ou non conforme. Vous pouvez également enregistrer un commentaire avec les éléments uniques ou multiples pour clarifier l’action reclassement.

#### <a name="resolved-items-tab"></a>Résolu onglet éléments

L’onglet **Éléments résolu** est où les réviseurs peuvent afficher tous les éléments précédemment résolus pour la stratégie sélectionnée. Ici, vous pouvez :

- Afficher et trier le sujet, l’expéditeur et la date d’éléments résolus rapidement.
- Afficher l’historique de classification et de commentaire de n’importe quel élément sélectionné

### <a name="other-ways-to-review-items"></a>Autres méthodes pour passer en revue les éléments

Si vous préférez relecteurs ne doit ne pas utiliser le tableau de bord de surveillance dans Office 365, ils ont également autres options pour examiner et gérer les éléments collectés par les stratégies de surveillance.

#### <a name="outlook-on-the-web"></a>Outlook sur le web

Les utilisateurs désignés comme relecteurs dans une stratégie de surveillance peuvent utiliser Outlook sur le web pour passer en revue et résolu les éléments de surveillance. Le complément de contrôle est installé automatiquement dans Outlook sur le web pour tous les relecteurs spécifiés dans la stratégie. Aucune configuration supplémentaire n’est requis par votre organisation pour les dossiers de stratégie shared surveillance soit disponible pour les réviseurs configurés.

À l’aide d’Outlook sur le web, les réviseurs peuvent :

- Afficher les éléments filtrés par état conforme, non conforme, suspect et résolu
- Ajouter une balise à un seul élément comme conforme, non conforme, suspect ou résolu. Vous pouvez également enregistrer un commentaire avec l’élément pour clarifier l’action de liaison.
- Afficher l’historique de la liaison d’un seul élément, y compris la personne qui a résolu l’élément, la date et l’heure de l’action, la balise de résolution et des commentaires inclus.
- Reclasser précédemment passé en revue les éléments suspects, conforme ou non conforme. Vous pouvez également enregistrer un commentaire avec des éléments uniques pour clarifier l’action reclassement.

#### <a name="microsoft-outlook"></a>Microsoft Outlook

Pour passer en revue les communications identifiées par une stratégie de surveillance, réviseurs peuvent également utiliser le complément de contrôle pour Microsoft Outlook. Cependant, réviseurs doivent exécuter certaines étapes de l’installer dans la version de bureau d’Outlook. Pour obtenir des instructions détaillées sur l’installation du complément de contrôle pour Outlook, voir [Configuration des stratégies de surveillance](configure-supervision-policies.md).

À l’aide d’Outlook, les réviseurs peuvent :

- Afficher les éléments filtrés par état conforme, non conforme, suspect et résolu
- Ajouter une balise à un seul élément comme conforme, non conforme, suspect ou résolu. Vous pouvez également enregistrer un commentaire avec l’élément pour clarifier l’action de liaison.
- Afficher l’historique de la liaison d’un seul élément, y compris la personne qui a résolu l’élément, la date et l’heure de l’action, la balise de résolution et des commentaires inclus.
- Reclasser précédemment passé en revue les éléments suspects, conforme ou non conforme. Vous pouvez également enregistrer un commentaire avec des éléments uniques pour clarifier l’action reclassement.

## <a name="reporting"></a>Création de rapports

Utilisez les rapports de surveillance pour afficher l’activité de révision au niveau de la stratégie et de réviseur. Pour chaque stratégie, vous pouvez également afficher les statistiques live sur l’état actuel de l’activité de révision. Vous pouvez utiliser les rapports de surveillance :
  
- Vérifiez que vos stratégies fonctionnent comme prévu.
- Découvrez combien communications sont identifiés pour révision.
- Découvrez combien communications ne sont pas conformes et ceux qui est en passant révision. Ces informations peuvent vous aider à décider s’il faut affiner vos stratégies ou modifier le nombre de relecteurs.

### <a name="view-the-supervision-report"></a>Afficher le rapport de surveillance

1. Connectez-vous à la [sécurité & centre de conformité](https://protection.office.com/) à l’aide des informations d’identification pour un compte d’administrateur de votre organisation Office 365 qui dispose d’autorisations pour afficher les rapports de surveillance.
2. Accédez à l' **rapports** \> **tableau de bord** ou de **surveillance**. Vous verrez un widget avec un résumé de l’activité de stratégie de surveillance en cours de création de rapports de surveillance.
3. Sélectionnez le widget de **surveillance** pour ouvrir la page rapport détaillé.

> [!NOTE]
> Si vous n’êtes pas en mesure d’accéder à la page **rapports** , vérifiez que vous êtes membre du groupe de rôles de supervision, comme indiqué dans [rendre disponibles dans votre organisation de surveillance](configure-supervision-policies.md). Soient inclus dans cette permet de groupe de rôle pour créer et gérer le contrôle des stratégies et exécutez le rapport.
  
### <a name="how-to-use-the-report"></a>Comment utiliser le rapport

Lorsqu’une stratégie de surveillance identifie un message de communication pour la révision, le courrier électronique est remis au dossier de surveillance du réviseur dans Outlook et Outlook web app. Ce rapport répertorie le nom de chaque stratégie et le nombre de communications à chaque étape du processus de révision.
  
Utilisez l’état :
  
- Afficher les données pour toutes les stratégies spécifiques ou.
- Afficher les données regroupement par type de balise (par exemple, conforme, Questionable, etc.), réviseur ou type de message.
- Exporter des données dans un fichier CSV en fonction de la date d’activité, la stratégie et par activité réviseur.
- Filtrer les données en fonction de la date d’activité, type de balise, réviseur et type de message.

Voici une répartition des valeurs que vous pouvez voir dans la colonne **type de balise** .
  
|**Type de balise**|**Cela signifie**|
|:-----|:-----|
| Pas de révision | Le nombre de messages électroniques qui n’ont pas encore été révisées. Ces e-mails sont en attente de révision dans le tableau de bord de surveillance Office 365 ou dans un dossier de surveillance du réviseur dans Outlook/Outlook Web App.|
| Compatible | Le nombre de messages électroniques révisé et marqué comme conforme. Ces messages doivent toujours être résolu. |
| Suspects | Le nombre de messages électroniques révisé et marqués suspect. Sous la forme d’un indicateur ; autres réviseurs peuvent aider à vérifier si un message électronique doit être une enquête de la conformité. Ces messages doivent toujours être résolu. |
| Non compatibles (actif) | Le nombre d’e-mails non conformes qui étudie relecteurs. |
| Non compatibles (résolu) | Le nombre de messages électroniques non conformes qui relecteurs étudier et de résoudre. |
| Stratégie d’accès au | (Quotidienne) le nombre total de messages à partir d’Exchange, les équipes et les sources de données de tiers qui correspondent à une ou plusieurs conditions définies dans une stratégie de surveillance |
| Dans les limites | (Quotidienne) le nombre total de messages à partir d’Exchange, les équipes et les sources de données tierces analysés par une stratégie de surveillance |
| Résolu | Le nombre total de messages à partir d’Exchange, les équipes et les sources de données tierce qui ont été identifiés comme **résolu**|

> [!NOTE]
> Stratégies de surveillance doivent tout d’abord être mis en service avant qu’ils n’apparaissent pas dans ce rapport. En outre, si les stratégies sont supprimés, les données d’historique sont toujours affichées. Cependant, ils sont indiqués comme une stratégie « inexistant » et la fonction **Exporter** n’est pas disponible.

## <a name="auditing"></a>Audit

Dans certains cas, vous devez fournir des informations à la réglementation ou auditeurs prouver la surveillance des activités des employés et les communications. Cela peut être une synthèse de toutes les activités de surveillance associée à une stratégie définie ou à tout moment une stratégie de surveillance a été modifiée ou mis à jour. Stratégies de surveillance ont des pistes d’audit intégrées de préparation terminée audits internes ou externes. Preuve de procédures de surveillance peut être démontrée avec un historique d’audit détaillées de chaque action surveillée par vos stratégies de surveillance.

Les activités de stratégie de surveillance suivantes sont auditées et peuvent être affichées à l’aide des journaux d’audit unifiées Office 365 :

|**Activité**|**Commandes associées**|
|:-----|:-----|
| Création d’une stratégie | Nouvelle SupervisoryReviewPolicy <br> Nouvelle SupervisoryReviewRule |
| Modification d’une stratégie | Set-SupervisoryReviewPolicy <br> Set-SupervisoryReviewRule |
| Suppression d’une stratégie| Remove-SupervisoryReviewPolicy |

Les audits peuvent être récupérés à l’aide de la fonction de recherche du journal d’audit unifiée ou à l’aide de l’applet de commande PowerShell [UnifiedAuditLog de la recherche](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) .

Par exemple, l’exemple suivant renvoie les activités de tous les les supervision activités (stratégies et règles) et fournit des informations détaillées pour chaque :

```
Search-UnifiedAuditLog -StartDate $startDate -EndDate $endDate -RecordType DataGovernance -ResultSize 5000 | Where-Object {$_.Operations -like "*SupervisoryReview*"} | fl CreationDate,Operations,UserIds,AuditData 
```

Outre les informations fournies dans les rapports de surveillance et les journaux, vous pouvez également utiliser l’applet de commande [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewactivity?view=exchange-ps) PowerShell pour renvoyer une liste détaillée complète de la surveillance de toutes les activités de la stratégie.

## <a name="ready-to-get-started"></a>Prêt à commencer ?

Pour commencer à configurer les stratégies de surveillance pour votre organisation, voir [Configuration des stratégies de surveillance](configure-supervision-policies.md).