---
title: Vue d’ensemble de la protection contre la perte de données
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/12/2019
audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: Les stratégies de protection contre la perte de données (DLP) disponibles dans le Centre de sécurité &amp; conformité vous permettent d’identifier, de surveiller et de protéger automatiquement des informations sensibles dans Office 365.
ms.openlocfilehash: 1f82af2c61138fd33f849a5cb13fcee1259cafd7
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230768"
---
# <a name="overview-of-data-loss-prevention"></a>Vue d’ensemble de la protection contre la perte de données

> [!NOTE]
> Des fonctionnalités de protection contre la perte de données ont récemment été ajoutées à la conversation Microsoft Teams et aux messages de canal pour les utilisateurs titulaires d’une licence de Conformité avancée Office 365, disponible sous la forme d’une option autonome et incluse dans Office 365 E5 et Microsoft 365 E5 Conformité. Pour en savoir plus sur les conditions d'octroi de licences, voir [Conseils sur les gestionnaires de licences au niveau client de Microsoft 365](https://docs.microsoft.com/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance).

Pour respecter les normes de l'entreprise et les réglementations du secteur, les organisations doivent protéger les informations sensibles et empêcher leur divulgation accidentelle. Les informations sensibles peuvent être des données financières ou des informations d’identification personnelle (PII) telles que les numéros de carte de crédit, les numéros de sécurité sociale ou les dossiers médicaux. Les stratégies de protection contre la perte de données (DLP) disponibles dans le Centre de sécurité et conformité Office 365 vous permettent d’identifier, de surveiller et de protéger automatiquement des informations sensibles dans Office 365.
  
Avec une stratégie DLP, vous pouvez :
  
- **Identifier les informations sensibles à de nombreux emplacements, comme Exchange Online, SharePoint Online, OneDrive Entreprise et Microsoft Teams.**
    
    Par exemple, vous pouvez identifier un document contenant un numéro de carte de crédit stocké sur un site OneDrive Entreprise ou vous pouvez surveiller uniquement les sites OneDrive de personnes spécifiques.
    
- **Empêcher le partage accidentel d’informations sensibles**. 
    
    Par exemple, vous pouvez identifier un document ou un message électronique contenant un dossier médical partagé avec des personnes extérieures à votre organisation, puis bloquer automatiquement l’accès à ce document ou bloquer l’envoi du message.
    
- **Surveiller et protéger les informations sensibles dans les versions de bureau d’Excel, de PowerPoint et de Word.**
    
    Comme dans Exchange Online, SharePoint Online et OneDrive Entreprise, ces programmes de bureau Office incluent les mêmes fonctionnalités pour identifier les informations sensibles et appliquer les stratégies DLP. DLP assure une surveillance continue en cas de partage de contenu dans ces programmes Office.
    
- **Aider les utilisateurs à découvrir comment assurer la conformité sans interrompre leur flux de travail.**
    
    Vous pouvez informer vos utilisateurs sur les stratégies DLP et les aider à maintenir la conformité sans bloquer leur travail. Par exemple, si un utilisateur tente de partager un document contenant des informations sensibles, une stratégie DLP peut lui envoyer une notification par courrier électronique et afficher un conseil de stratégie dans le contexte de la bibliothèque de documents, qui lui permet de remplacer la stratégie s’il a une raison professionnelle de le faire. Les mêmes conseils de stratégie s’affichent également dans Outlook sur le web, Outlook, Excel, PowerPoint et Word.
    
- **Consulter les rapports DLP présentant le contenu qui correspond aux stratégies DLP de votre organisation.**
    
    Pour évaluer la manière dont votre organisation se conforme à une stratégie DLP, vous pouvez voir le nombre de correspondances obtenues par chaque stratégie et chaque règle. Si une stratégie DLP autorise les utilisateurs à remplacer un conseil de stratégie et signaler un faux positif, vous pouvez également afficher ce que les utilisateurs ont signalé.
    
Vous créez et gérez des stratégies DLP sur la page Protection contre la perte de données dans le Centre de conformité et sécurité d’Office 365.
  
![Page Protection contre la perte de données dans le Centre de conformité et sécurité Office 365](media/943fd01c-d7aa-43a9-846d-0561321a405e.png)
  
## <a name="what-a-dlp-policy-contains"></a>Contenu d’une stratégie DLP

Une stratégie DLP contient quelques éléments de base :
  
- Emplacements de protection du contenu : **emplacements** comme Exchange Online, SharePoint Online et sites OneDrive Entreprise, ainsi que conversations et messages du canal Microsoft Teams. 
    
- Circonstances de protection du contenu en appliquant des **règles** comprenant les éléments suivants : 
    
  - **Conditions** auxquelles le contenu doit correspondre avant que la règle ne soit appliquée. Par exemple, une règle doit être configurée pour rechercher uniquement du contenu incluant des numéros de sécurité sociale partagés avec des personnes extérieures à votre organisation. 
    
  - **Actions** que la règle doit effectuer automatiquement lorsque du contenu correspondant aux conditions est trouvé. Par exemple, une règle peut être configurée pour bloquer l’accès à un document et envoyer à l’utilisateur et au responsable de la conformité une notification par courrier électronique. 
    
Vous pouvez utiliser une règle pour répondre à une exigence de protection particulière, puis utiliser une stratégie DLP pour regrouper des spécifications requises communes en matière de protection, par exemple l’ensemble des règles requises pour se conformer à une réglementation spécifique.
  
Par exemple, vous pouvez avoir une stratégie DLP qui vous aide à détecter la présence d’informations visées par la loi américaine sur l’assurance maladie (Health Insurance Portability Accountability Act, ou HIPAA). Cette stratégie DLP peut contribuer à protéger les données HIPAA (quoi) sur tous les sites SharePoint Online et tous les sites OneDrive Entreprise (où) en recherchant les documents contenant ces informations sensibles partagées avec des personnes extérieures à votre organisation (conditions), et en bloquant l’accès au document et en envoyant une notification (actions). Ces conditions sont stockées en tant que règles individuelles et regroupées sous la forme d’une stratégie DLP pour simplifier la gestion et la création de rapports.
  
![Diagramme montrant que la stratégie DLP contient les règles et les emplacements](media/c006860c-2d00-42cb-aaa4-5b5638d139f7.png)
  
### <a name="locations"></a>Emplacements

Une stratégie DLP peut rechercher et protéger les informations sensibles dans Office 365, que ces informations se trouvent sur Exchange Online, SharePoint Online, OneDrive Entreprise ou Microsoft Teams. Vous pouvez choisir de protéger le contenu dans le courrier Exchange, les conversations et les messages de canal de Microsoft Teams, ainsi que toutes les bibliothèques SharePoint ou OneDrive, ou de sélectionner des emplacements spécifiques pour une stratégie.
  
![Options pour les emplacements dans lesquels une stratégie DLP peut être appliquée](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
Si vous optez pour l’inclusion ou l’exclusion de sites SharePoint ou de comptes OneDrive spécifiques, notez qu’une stratégie DLP ne peut pas contenir plus de 100 inclusions et exclusions. Vous pouvez néanmoins contourner cette limite en appliquant une stratégie mise en place à l’échelle de l’organisation ou une stratégie qui s’applique aux emplacements entiers.
  
### <a name="rules"></a>Rules

Les règles appliquent vos exigences professionnelles au contenu de votre organisation. Une stratégie contient une ou plusieurs règles et chaque règle se compose de conditions et d’actions. Pour chaque règle, lorsque les conditions sont remplies, les actions sont exécutées automatiquement. Les règles sont exécutées de façon séquentielle, en commençant par la règle de priorité la plus élevée dans chaque stratégie.
  
Une règle fournit également des options pour informer les utilisateurs (avec des conseils de stratégie et des notifications par courrier électronique) et les administrateurs (avec des rapports d’incident de courrier) que le contenu satisfait à la règle.
  
Les différents composants d’une règle sont décrits ci-dessous.
  
![Sections de l’éditeur de règles DLP](media/1859d504-b9c2-45ed-961b-a0092251acc2.png)
  
#### <a name="conditions"></a>Conditions

Les conditions sont importantes car elles déterminent les types d’informations que vous recherchez, et le moment auquel effectuer une action. Par exemple, vous pouvez choisir d’ignorer les documents contenant des numéros de passeport, sauf si le document contient plus de 10 numéros et est partagé avec des personnes extérieures à votre organisation.
  
Les conditions concernent le **contenu**, par exemple les types d’informations sensibles que vous recherchez et aussi le **contexte**, par exemple les personnes avec lesquelles le document est partagé. Vous pouvez utiliser les conditions pour affecter différentes actions à différents niveaux de risque. Par exemple, un contenu sensible partagé en interne peut être moins risqué et nécessiter moins d’actions qu’un contenu sensible partagé avec des personnes extérieures à l’organisation. 
  
![Liste affichant les conditions DLP disponibles](media/0fa43f90-d007-4506-ae93-43e8424fe103.png)
  
Les conditions actuellement disponibles peuvent déterminer si :
  
- Le contenu comporte un type d’informations sensibles.
    
- Le contenu comporte une étiquette. Pour plus d’informations, reportez-vous à la section ci-dessous, [Utilisation d’une étiquette comme condition dans une stratégie DLP](#using-a-label-as-a-condition-in-a-dlp-policy).
    
- Le contenu est partagé avec des personnes extérieures ou internes à votre organisation.
    
#### <a name="types-of-sensitive-information"></a>Types d’informations sensibles

Une stratégie DLP peut contribuer à protéger les informations sensibles, définies selon des **types d’informations sensibles**. Office 365 inclut les définitions de nombreux types d’informations sensibles courants dans diverses régions, prêtes pour utilisation, comme les numéros de carte de crédit, numéros de compte bancaire, numéros de carte d’identité et numéros de passeport. 
  
![Liste des types d’informations sensibles disponibles](media/3eaa9911-bc94-44be-902f-363dbf3b07fe.png)
  
Lorsqu’une stratégie DLP recherche un type d’informations sensibles tel qu’un numéro de carte de crédit, il ne recherche pas simplement un nombre à 16 chiffres. Chaque type d’information sensible est défini et détecté en utilisant une combinaison de :
  
- Mots clés
    
- Fonctions internes pour valider les sommes de contrôle ou la composition
    
- Évaluation des expressions régulières pour trouver des correspondances au modèle
    
- Autres analyses de contenu
    
La détection DLP peut ainsi atteindre un haut niveau de précision tout en réduisant le nombre de faux positifs susceptibles d’interrompre le travail.
  
#### <a name="actions"></a>Actions

Lorsque le contenu remplit une condition stipulée dans une règle, vous pouvez y appliquer des mesures de protection automatiques.
  
![Liste des actions DLP disponibles](media/8aef17fc-1e99-4ac7-adfc-0f2c9c1a0697.png)
  
Avec les actions désormais disponibles, vous pouvez :
  
- **Restreindre l’accès au contenu** Pour le contenu d’un site, cela signifie que les autorisations pour le document sont limitées pour tout le monde, sauf pour l’administrateur principal de la collection de sites, le propriétaire du document et la personne qui a modifié le document pour la dernière fois. Ces personnes peuvent supprimer les informations sensibles du document ou prendre des mesures correctives. Lorsque le document est conforme, les autorisations d’origine sont automatiquement restaurées. Lorsque l’accès à un document est bloqué, le document s’affiche avec une icône de conseil de stratégie spéciale dans la bibliothèque sur le site. 
    
    ![Conseil de stratégie montrant que l’accès au document est bloqué](media/b6cefed3-d212-43d7-8534-4b92b26ebd50.png)
  
    Pour le contenu des messages électroniques, cette action bloque l’envoi du message. Selon la configuration de la règle DLP, l’expéditeur voit une notification d’échec de remise ou (si la règle utilise une notification) un conseil de stratégie et/ou une notification de messagerie.
    
    ![Avertissement indiquant que les destinataires non autorisés doivent être supprimés du message](media/302f9994-912d-41e7-861f-8a4539b3c285.png)
  
#### <a name="user-notifications-and-user-overrides"></a>Notifications de l’utilisateur et remplacements de l’utilisateur

Vous pouvez utiliser les notifications et les remplacements pour informer vos utilisateurs sur les stratégies DLP et les aider à respecter les règles de conformité sans bloquer leur travail. Par exemple, si un utilisateur tente de partager un document contenant des informations sensibles, une stratégie DLP peut lui envoyer une notification par courrier électronique et afficher un conseil de stratégie dans le contexte de la bibliothèque de documents, qui lui permet de remplacer la stratégie s’il a une raison professionnelle de le faire.
  
![Sections Notifications de l’utilisateur et Remplacements de l’utilisateur de l’éditeur de règles DLP](media/37b560d4-6e4e-489e-9134-d4b9daf60296.png)
  
Le message électronique permet de notifier les personnes qui ont envoyé, partagé ou modifié le contenu en dernier et, pour le contenu de site, l’administrateur de la collection de sites et le propriétaire du document. De plus, vous pouvez ajouter ou supprimer les destinataires de votre choix du courrier électronique de notification.
  
En plus d’envoyer une notification par courrier électronique, une notification utilisateur affiche un conseil de stratégie :
  
- Dans Outlook et Outlook sur le web.
    
- Pour un document sur SharePoint Online ou un site OneDrive Entreprise.
    
- Dans Excel, PowerPoint et Word, lorsque le document est stocké sur un site inclus dans une stratégie DLP.
    
La notification par courrier électronique et le conseil de stratégie expliquent pourquoi un contenu est en conflit avec une stratégie DLP. Si vous le choisissez, la notification par courrier électronique et le conseil de stratégie peuvent permettre aux utilisateurs de remplacer une règle en signalant un faux positif ou en fournissant une justification professionnelle. Cela peut vous aider à informer les utilisateurs de vos stratégies DLP et à les appliquer sans interrompre le travail. Les informations sur les remplacements et les faux positifs sont également enregistrées pour la création de rapports (consultez la rubrique ci-dessous sur les rapports DLP) et incluses dans les rapports d’incident (section suivante), afin que le responsable de la mise en conformité puisse les consulter régulièrement.
  
Dans un compte OneDrive Entreprise, un conseil de stratégie se présente comme ceci.
  
![Conseil de stratégie pour un document dans un compte OneDrive](media/f9834d35-94f0-4511-8555-0fe69855ce6d.png)
  
#### <a name="incident-reports"></a>Rapports d’incident

Lorsqu’une règle est satisfaite, vous pouvez envoyer un rapport d’incident contenant les détails de l’événement à votre responsable de la mise en conformité (ou une autre personne de votre choix). Ce rapport comprend des informations sur l’élément qui a fait l’objet d’une correspondance, le contenu qui a satisfait à la règle ainsi que le nom de la personne qui a modifié le contenu en dernier. Pour les messages électroniques, le rapport inclut également sous forme de pièce jointe le message d’origine qui correspond à une stratégie DLP.
  
![Page de configuration de rapports d’incident](media/31c6da0e-981c-415e-91bf-d94ca391a893.png)
  
## <a name="grouping-and-logical-operators"></a>Opérateurs logiques et opérateurs de regroupement

Votre stratégie de protection contre la perte de données a souvent une exigence simple, par exemple, celle d’identifier tout contenu avec un numéro de sécurité sociale. Toutefois, dans d’autres scénarios, votre stratégie de protection contre la perte de données devra identifier des données plus vagues.
  
Par exemple, pour identifier le contenu soumis à la réglementation des États-Unis sur le Health Insurance Act (HIPAA), vous devez rechercher :
  
- Le contenu qui contient certains types d’informations sensibles, par exemple un numéro de sécurité sociale ou le numéro émis par l’agence du médicament (DEA).
    
    AND
    
- Le contenu plus difficile à identifier, comme les communications relatives aux soins du patient ou la description des services médicaux fournis. L’identification de ce contenu nécessite une correspondance de mots clés d’une très importante liste de mots clés, telle que la classification internationale des maladies (ICD-9-CM ou ICD-10-CM).
    
Vous pouvez facilement identifier ces données vaguement définies à l’aide d’opérateurs logiques et d’opérateurs de regroupement (ET, OU). Lorsque vous créez une stratégie de protection contre la perte de données, vous pouvez :
  
- Regrouper les types d’informations sensibles
    
- Choisir l’opérateur logique dans les types d’informations sensibles au sein d’un groupe et entre les groupes eux-mêmes.
    
### <a name="choosing-the-operator-within-a-group"></a>Choisir l’opérateur au sein d’un groupe

Dans un groupe, vous pouvez choisir si tout ou partie des conditions dans ce groupe doivent être satisfaites pour que le contenu corresponde à la règle.
  
![Groupes avec l’opérateur dans le groupe](media/6a12f1e8-112d-48ee-9a73-82b3dd0542e7.png)
  
### <a name="adding-a-group"></a>Ajout d’un groupe

Vous pouvez rapidement ajouter un groupe, qui peut avoir ses propres conditions et son propre opérateur au sein de ce groupe.
  
![Bouton Ajouter un groupe](media/5f72f292-d1f3-4f11-a911-a9f71e10abf6.png)
  
### <a name="choosing-the-operator-between-groups"></a>Choix de l’opérateur entre les groupes

Entre les groupes, vous pouvez choisir si les conditions dans un seul groupe ou tous les groupes doivent être satisfaites pour que le contenu corresponde à la règle.
  
Par exemple, le type d’informations sensibles intégrées pour la réglementation des États-Unis sur le **HIPAA** a une règle qui utilise un opérateur **ET** entre les groupes, de sorte qu’elle identifie le contenu qui contient : 
  
- le groupe **identificateurs de données personnelles** (au moins un numéro de sécurité sociale **OU** numéro DEA) 
    
    **ET**
    
- le groupe **termes médicaux** (au moins un mot-clé ICD-9-CM **OU** mot clé ICD-10-CM) 
    
![Groupes avec l’opérateur entre les groupes](media/354aa77f-569c-4847-9dfe-605ee2bb28d1.png)
  
## <a name="the-priority-by-which-rules-are-processed"></a>La priorité de traitement des règles

Lorsque vous créez des règles dans une stratégie, chaque règle se voit attribuer une priorité en fonction de son ordre de création. Cela signifie que la première règle créée a priorité sur la deuxième et ainsi de suite. 
  
![Règles dans l’ordre de priorité](media/f7dc06bf-bc6f-485c-bcdb-606edbcf6565.png)
  
Une fois que vous avez configuré plusieurs stratégies DLP, vous pouvez modifier la priorité d’une ou plusieurs stratégies. Pour ce faire, sélectionnez une stratégie, sélectionnez **Modifier la stratégie**, puis utilisez la liste **Priorité** pour préciser sa priorité.

![Définition d’une priorité pour une stratégie](media/dlp-set-policy-priority.png)

Lorsque des règles sont appliquées au contenu, elles sont traitées dans l’ordre de priorité. Si le contenu correspond à plusieurs règles, celles-ci sont traitées dans l’ordre de priorité et l’action la plus restrictive est appliquée. Par exemple, si le contenu correspond à toutes les règles suivantes, la règle 3 est appliquée, car c’est celle qui a la priorité la plus élevée et est la plus restrictive :
  
- Règle 1 : informe seulement les utilisateurs
    
- Règle 2 : informe les utilisateurs, limite l’accès et permet le remplacement de l’utilisateur
    
- Règle 3 : informe les utilisateurs, limite l’accès et ne permet pas le remplacement de l’utilisateur
    
- Règle 4 : informe seulement les utilisateurs
    
- Règle 5 : limite l’accès
    
- Règle 6 : informe les utilisateurs, limite l’accès et ne permet pas le remplacement de l’utilisateur
    
Dans cet exemple, notez que les correspondances de toutes les règles sont enregistrées dans les journaux d’audit et apparaissent dans les rapports DLP, même si seule la règle la plus restrictive est appliquée.
  
En ce qui concerne les conseils de stratégie, veuillez noter les éléments suivants :
  
- Uniquement le conseil de stratégie de la priorité la plus élevée, la règle la plus restrictive est affichée. Par exemple, un conseil de stratégie à partir d’une règle qui bloque l’accès au contenu est affiché sur un conseil de stratégie à partir d’une règle qui envoie simplement une notification. Cela évite que les personnes voient une cascade de conseils de stratégie.
    
- Si les conseils de stratégie de la règle la plus restrictive autorisent les utilisateurs à remplacer la règle, toute autre règle également mise en correspondance avec le contenu est aussi remplacée.
    
## <a name="tuning-rules-to-make-them-easier-or-harder-to-match"></a>Optimisation des règles pour une correspondance plus facile ou plus difficile

Lorsque les utilisateurs créent et activent leurs stratégies DLP, ils rencontrent parfois les problèmes suivants :
  
- Trop de contenu qui **ne constitue pas** des informations sensibles correspond aux règles. Autrement dit, le nombre de faux positifs est trop élevé. 
    
- Trop peu de contenu **qui constitue** des informations sensibles correspond aux règles. En d’autres termes, les mesures de protection ne sont pas appliquées aux informations sensibles. 
    
Pour résoudre ces problèmes, vous pouvez optimiser vos règles en ajustant le nombre d’instances et la précision de correspondance pour que le contenu corresponde plus ou moins aux règles. Chaque type d’informations sensibles utilisé dans une règle a un nombre d’instances et une précision de correspondance.
  
### <a name="instance-count"></a>Nombre d’instances

Le nombre d’instances indique simplement combien d’occurrences d’un type spécifique d’informations sensibles doivent être présentes pour que le contenu corresponde à la règle. Par exemple, le contenu correspond à la règle illustrée ci-dessous si les valeurs entre 1 et 9 sont uniques dans un pays donné. les numéros de passeport sont identifiés.
  
Notez que le nombre d’instances inclut uniquement le nombre de correspondances **uniques** avec des mots clés et des types d’informations sensibles. Par exemple, si un courrier contient 10 occurrences du même numéro de carte de paiement, ces 10 occurrences comptent pour une seule instance d’un numéro de carte de paiement. 
  
L’optimisation des règles à l’aide du nombre d’instances est simple :
  
- Pour que la règle corresponde plus facilement, diminuez la valeur **min** et/ou augmentez la valeur **max**. Vous pouvez également donner à **max** une valeur **quelconque** en supprimant la valeur numérique. 
    
- Pour que la règle corresponde plus difficilement, augmentez la valeur **min**. 
    
En règle générale, les actions moins restrictives, telles que l’envoi de notifications à l’utilisateur, s’utilisent dans une règle avec un nombre d’instances inférieur (par exemple, 1 à 9). Quant aux actions plus restrictives, telles que la limitation de l’accès au contenu sans autoriser les remplacements de l’utilisateur, elles s’utilisent dans une règle avec un nombre d’instances supérieur (par exemple, entre 10 et une valeur supérieure).
  
![Nombre d’instances dans l’éditeur de règles](media/e7ea3c12-72c5-4bb3-9590-c924c665e84d.png)
  
### <a name="match-accuracy"></a>Précision de correspondance

Comme décrit ci-dessus, un type d’informations sensibles est défini et détecté en utilisant une combinaison de différents types de critères. En règle générale, un type d’informations sensibles est défini par plusieurs de ces combinaisons, appelés modèles. Un modèle qui nécessite moins de critères a une précision de correspondance (ou niveau de confiance) inférieure, alors qu’un modèle qui nécessite plus de critères a une précision de correspondance (ou niveau de confiance) supérieure. Pour en savoir plus sur les modèles et les niveaux de confiance réels utilisés par tous les types d’informations sensibles, consultez [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
Par exemple, le type d’informations sensibles Numéro de carte bancaire est défini par deux modèles :
  
- Un modèle avec une confiance de 65 % qui nécessite :
    
  - Un nombre dans le format d’un numéro de carte bancaire.
    
  - Un nombre qui passe la somme de contrôle.
    
- Un modèle avec une confiance de 85 % qui nécessite :
    
  - Un nombre dans le format d’un numéro de carte bancaire.
    
  - Un nombre qui passe la somme de contrôle.
    
  - Un mot clé ou une date d’expiration dans le bon format.
    
Vous pouvez utiliser ces niveaux de confiance (ou précision de correspondance) dans vos règles. En règle générale, les actions moins restrictives, telles que l’envoi de notifications à l’utilisateur, s’utilisent dans une règle avec une précision de correspondance inférieure. Quant aux actions plus restrictives, telles que la limitation de l’accès au contenu sans autoriser les remplacements de l’utilisateur, elles s’utilisent dans une règle avec une précision de correspondance supérieure.
  
Il est essentiel de comprendre que lorsqu’un type spécifique d’informations sensibles, comme un numéro de carte bancaire, est identifié dans le contenu, un seul niveau de confiance est renvoyé :
  
- Si toutes les correspondances correspondent à un seul modèle, le niveau de confiance de ce modèle est renvoyé.
    
- En cas de correspondances à plusieurs modèles (par exemple, des correspondances à deux niveaux de confiance différents), un niveau de confiance supérieur à celui de chacun des modèles est renvoyé. Il s’agit de la partie délicate. Par exemple, pour une carte bancaire, si les modèles à 65 % et 85 % correspondent, le niveau de confiance renvoyé pour ce type d’informations sensibles est supérieur à 90 %, car plus de critères signifie plus de confiance.
    
Par conséquent si vous voulez créer deux règles mutuellement exclusives pour les cartes bancaires, une pour la précision de correspondance de 65 % et une pour la précision de correspondance de 85 %, les plages de précision de correspondance se présenteraient comme suit. La première règle ne prend que les correspondances au modèle à 65 %. La deuxième règle prend les correspondances avec **au moins une** correspondance à 85 % et **peut éventuellement avoir** d’autres correspondances de confiance inférieure. 
  
![Deux règles avec des plages différentes de précision de correspondance](media/21bdfe36-7a91-4347-8098-11809a92f9a4.png)
  
Pour ces raisons, les conseils pour la création de règles avec des précisions de correspondance différentes sont les suivants :
  
- En général, le niveau de confiance le plus faible utilise la même valeur pour **min** et **max** (pas un intervalle). 
    
- Le niveau de confiance le plus élevé est généralement un intervalle commençant juste au-dessus du niveau de confiance inférieur et allant jusqu’à 100.
    
- Tous les niveaux de confiance intermédiaires commencent généralement juste au-dessus du niveau de confiance inférieur pour finir juste en dessous du niveau de confiance supérieur.
    
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a>Utilisation d’une étiquette comme condition dans une stratégie DLP

Vous pouvez créer une étiquette, puis :
  
- la **publier** afin que les utilisateurs finaux y aient accès et puissent manuellement l’appliquer au contenu ; 
    
- l’**appliquer automatiquement** au contenu qui remplit les conditions que vous avez définies. 
    
Pour en savoir plus sur les étiquettes, consultez l’article [Vue d’ensemble des étiquettes de rétention](labels.md).
  
Après avoir créé une étiquette, vous pouvez l’utiliser comme condition dans vos stratégies DLP. Dans les scénarios suivants, par exemple :
  
- Vous avez publié une étiquette intitulée **Confidentiel** pour permettre aux membres de votre organisation de l’appliquer manuellement aux e-mails et documents confidentiels. L’utilisation de cette étiquette comme condition dans votre stratégie DLP vous permettra d’empêcher les utilisateurs de partager du contenu **Confidentiel** avec des personnes extérieures à votre organisation. 
    
- Vous avez créé une étiquette intitulée **Chalet alpin** pour un projet du même nom, puis automatiquement appliqué cette étiquette au contenu comportant les mots-clés « Chalet alpin ». L’utilisation de cette étiquette comme condition dans votre stratégie DLP vous permettra d’afficher un conseil de stratégie à l’attention des utilisateurs finaux qui s’apprêteront à partager ce type de contenu avec une personne extérieure à votre organisation. 
    
- Vous avez publié une étiquette intitulée **Dossier fiscal** pour permettre au personnel chargé de la gestion des dossiers de l’appliquer manuellement au contenu à classer. L’utilisation de cette étiquette comme condition dans votre stratégie DLP vous permettra de rechercher tout contenu comportant cette étiquette ainsi que d’autres types d’informations sensibles, comme les numéros individuels des contribuables ou les numéros de sécurité sociale, puis d’appliquer des mesures de protection sur le contenu comportant l’étiquette **Dossier fiscal** et de générer des rapports d’activité détaillés sur la stratégie DLP à partir des rapports DLP et des données du journal d’audit. 
    
- Vous avez publié une étiquette intitulée **Équipe de direction – Sensible** sur les boîtes aux lettres Exchange et sur les comptes OneDrive d’un groupe de cadres. L’utilisation de cette étiquette comme condition dans votre stratégie DLP vous permettra d’appliquer des mesures de rétention et de protection au même sous-ensemble de contenu et d’utilisateurs. 
    
L’utilisation d’étiquettes comme condition dans les règles DLP permet d’appliquer de façon sélective des mesures de protection à un ensemble spécifique de contenu, de sites ou d’utilisateurs.
  
![Étiquettes comme condition](media/5b1752b4-a129-4a88-b010-8dcf8a38bb09.png)

### <a name="support-for-sensitivity-labels-is-coming"></a>La prise en charge des étiquettes de confidentialité est pour bientôt

Vous pouvez actuellement utiliser uniquement une étiquette de rétention comme condition, et non une [étiquette de confidentialité](sensitivity-labels.md). Nous travaillons actuellement à l’utilisation d’une étiquette de confidentialité dans cette condition.
  
### <a name="how-this-feature-relates-to-other-features"></a>Relations entre cette fonctionnalité et d’autres fonctionnalités

Plusieurs fonctionnalités peuvent être appliquées à du contenu comportant des informations sensibles :
  
- Une [étiquette de rétention](labels.md#applying-a-retention-label-automatically-based-on-conditions) et une [stratégie de rétention](retention-policies.md) peuvent toutes deux permettre d’appliquer des mesures de **rétention** à ce type de contenu. 
    
- Et une stratégie DLP peut permettre d’y appliquer des mesures de **protection**. Avant l’application de ces mesures, une stratégie DLP peut exiger que d’autres conditions soient remplies en plus du contenu comportant une étiquette. 
    
![Diagramme illustrant des fonctionnalités applicables aux informations sensibles](media/dd410f97-a3a3-455c-a1e9-7ed8ae6893d6.png)
  
Notez qu’une stratégie DLP offre des capacités de détection plus approfondies qu’une étiquette ou qu’une stratégie de rétention appliquées à des informations sensibles. Une stratégie DLP peut déclencher l’application de mesures de protection sur du contenu comportant des informations sensibles, et si les informations sensibles sont supprimées du contenu, ces mesures de protection sont annulées lors de l’analyse de contenu suivante. Mais si une stratégie de rétention ou une étiquette est appliquée au contenu comportant des informations sensibles, il s’agit d’une mesure unique qui ne peut pas être annulée, même si les informations sensibles sont supprimées.
  
L’utilisation d’une étiquette comme condition dans une stratégie DLP vous permet d’appliquer des mesures de rétention et de protection au contenu associé à cette étiquette. Un contenu comportant une étiquette et un contenu comportant des informations sensibles sont semblables : l’étiquette et les informations sensibles sont des propriétés utilisées pour classifier le contenu dans le but d’y appliquer des mesures.
  
![Diagramme illustrant une stratégie DLP qui utilise une étiquette comme condition](media/4538fd8f-fb74-4743-bc22-a5de33adfebb.png)
  
## <a name="simple-settings-vs-advanced-settings"></a>Paramètres simples et paramètres avancés

Lorsque vous créez une stratégie DLP, vous devez choisir entre les paramètres simples ou avancés :
  
- Les **paramètres simples** permettent de créer le type le plus courant de stratégie DLP sans utiliser l’éditeur de règles pour créer ou modifier des règles. 
    
- Les **paramètres avancés** utilisent l’éditeur de règles pour vous donner un contrôle total sur chaque paramètre de votre stratégie DLP. 
    
Soyez rassuré, en réalité, les paramètres simples et avancés fonctionnent de la même manière : ils appliquent des règles composées de conditions et d’actions. La seule différence est que l’éditeur de règles n’apparaît pas avec les paramètres simples. C’est un moyen rapide de créer une stratégie DLP.
  
### <a name="simple-settings"></a>Paramètres simples

Le scénario DLP de loin le plus courant consiste à créer une stratégie pour empêcher le partage de contenu comportant des informations sensibles avec des personnes extérieures à votre organisation, et à prendre des mesures correctives automatiques telles que la restriction de l’accès au contenu, l’envoi de notifications à l’utilisateur final ou à l’administrateur et l’audit de l’événement pour examen ultérieur. Les stratégies DLP permettent d’empêcher la divulgation accidentelle d’informations sensibles.
  
Pour atteindre cet objectif plus facilement, vous pouvez choisir d’utiliser les **paramètres simples** lorsque vous créez une stratégie DLP. Ces paramètres proposent toutes les options nécessaires pour implémenter les stratégies DLP les plus courantes, sans avoir à ouvrir l’éditeur de règles.
  
![Options DLP pour les paramètres simples et avancés](media/33c93824-ead5-43b6-9c3e-fd1630c92a7d.png)
  
### <a name="advanced-settings"></a>Paramètres avancés

Si vous devez créer des stratégies DLP plus personnalisées, vous pouvez choisir d’utiliser les **paramètres avancés**.
  
Les paramètres avancés présentent l’éditeur de règles, où vous contrôlez entièrement chaque option, y compris le nombre d’instances et la précision des correspondances (niveau de confiance) pour chaque règle.
  
Pour accéder rapidement à une section, cliquez sur un élément de la navigation supérieure de l’éditeur de règles.
  
![Menu de navigation supérieur de l’éditeur de règles DLP](media/c527b97f-ca53-4c79-ad19-1a63be8a8ecc.png)
  
## <a name="dlp-policy-templates"></a>Modèles de stratégie de protection contre la perte de données (DLP)

La première étape de la création d’une stratégie DLP consiste à choisir les informations à protéger. En utilisant un modèle DLP, vous n’avez alors pas à faire l’effort de créer intégralement un ensemble de règles et d’identifier les types d’informations à inclure par défaut. Vous pouvez ensuite ajouter des éléments à ces exigences ou modifier ces dernières pour ajuster la règle afin de répondre aux besoins spécifiques de votre organisation.
  
Un modèle de stratégie DLP préconfiguré peut vous aider à détecter des types spécifiques d’informations sensibles, comme des données HIPAA, des données PCI-DSS, des données Gramm-Leach-Bliley Act ou même des informations d’identification personnelle propres aux paramètres régionaux. Pour faciliter la recherche et la protection des types d’informations sensibles courants, les modèles de stratégie inclus dans Office 365 contiennent déjà les types d’informations sensibles les plus courants, nécessaires pour commencer.
  
![Liste des modèles de stratégies de protection contre la perte de données avec focus sur le modèle pour le Patriot Act des États-Unis](media/791b2403-430b-4987-8643-cc20abbd8148.png)
  
Votre organisation peut également avoir ses exigences propres, auquel cas vous pouvez créer entièrement une stratégie DLP en choisissant l’option **Stratégie personnalisée**. Une stratégie personnalisée est vide et ne contient aucune règle prédéfinie. 
  
## <a name="roll-out-dlp-policies-gradually-with-test-mode"></a>Déployer progressivement des stratégies DLP avec le mode test

Lorsque vous créez vos stratégies DLP, vous devez envisager de les déployer progressivement pour évaluer leur impact et tester leur efficacité avant de les appliquer pleinement. Par exemple, vous ne voulez pas qu’une nouvelle stratégie DLP bloque involontairement l’accès à des milliers de documents auxquels les utilisateurs doivent accéder pour effectuer leur travail.
  
Si vous créez des stratégies DLP susceptibles d’avoir un impact important, nous vous recommandons de suivre l’ordre suivant :
  
1. **Démarrez en mode test sans conseils de stratégie**, puis utilisez les rapports DLP et les rapports d’incident pour évaluer l’impact. Vous pouvez utiliser les rapports DLP pour connaître le nombre, l’emplacement, le type et la gravité des correspondances de stratégie. En fonction des résultats, vous pouvez affiner les règles selon vos besoins. En mode test, les stratégies DLP n’auront aucun impact sur la productivité des personnes qui travaillent dans votre organisation. 
    
2. **Passez en mode test avec notifications et conseils de stratégie** pour commencer à faire découvrir vos stratégies de conformité aux utilisateurs et les préparer pour les règles qui vont être appliquées. À ce stade, vous pouvez également demander aux utilisateurs de signaler les faux positifs afin d’affiner les règles. 
    
3. **Démarrez l’application complète des stratégies** afin que les actions dans les règles soient appliquées et le contenu protégé. Continuez de surveiller les rapports DLP et tous les rapports ou notifications d’incident pour vous assurer que les résultats correspondent à ce que vous aviez prévu. 
    
![Options pour l’utilisation du mode de test et l’activation de la stratégie](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
Vous pouvez désactiver une stratégie DLP à tout moment, ce qui a une incidence sur toutes les règles de la stratégie. Toutefois, chaque règle peut également être désactivée individuellement en basculant son état dans l’éditeur de règles.
  
![Options de désactivation d’une règle dans une stratégie](media/f7b258ff-1b8b-4127-b580-83c6492f2bef.png)

Vous pouvez également modifier la priorité de plusieurs règles dans une stratégie. Pour ce faire, ouvrez une stratégie pour modification. Dans une ligne de règle, sélectionnez les points de suspension (**...**), puis choisissez une option, comme, par exemple, **Descendre** ou **Mettre à la fin**.

![Définition d’une priorité de règle](media/dlp-set-rule-priority.png)
  
## <a name="dlp-reports"></a>Rapports DLP

Après avoir créé et activé vos stratégies DLP, vous voudrez vérifier qu’elles fonctionnent comme prévu et vous aident à assurer la conformité. Avec les rapports DLP, vous pouvez rapidement consulter le nombre de correspondances de stratégie DLP et de règle dans le temps, ainsi que le nombre de faux positifs et de remplacements. Pour chaque rapport, vous pouvez filtrer ces correspondances par emplacement, par période et même affiner le filtrage sur une stratégie, règle ou action spécifique.
  
Grâce aux rapports DLP, vous pouvez obtenir une vue d’ensemble des activités et :
  
- Vous concentrer sur des périodes de temps spécifiques et comprendre les raisons des pics et des tendances.
    
- Découvrir les processus d’entreprise qui enfreignent les stratégies de conformité de votre organisation.
    
- Comprendre l’incidence des stratégies DLP sur l’entreprise.
    
En outre, vous pouvez utiliser les rapports DLP pour affiner vos stratégies DLP lorsque vous les exécutez.
  
![Tableau de bord des rapports dans le Centre de sécurité et conformité](media/6d741252-a0ce-4429-95ba-6c857ecc9a7e.png)
  
## <a name="how-dlp-policies-work"></a>Fonctionnement des stratégies DLP

DLP détecte les informations sensibles à l’aide d’une analyse approfondie du contenu (et pas d’une simple analyse de texte). Cette analyse approfondie utilise les correspondances de mots clés, les correspondances de dictionnaire, l’évaluation des expressions régulières, les fonctions internes et d’autres méthodes pour détecter le contenu qui correspond à vos stratégies DLP. Seul un petit pourcentage de vos données peut être considéré comme sensible. Une stratégie DLP peut identifier, surveiller et protéger automatiquement ces données uniquement, sans gêner ou affecter les personnes travaillant avec le reste de votre contenu.
  
### <a name="policies-are-synced"></a>Synchronisation des stratégies

Une fois qu’une stratégie DLP est créée dans le centre de conformité et de sécurité, elle est stockée dans un magasin central de stratégies, puis synchronisée avec différentes sources de contenu, notamment les suivantes :
  
- Depuis Exchange Online vers Outlook sur le web et Outlook
    
- Sites OneDrive Entreprise
    
- Sites SharePoint Online
    
- Programmes de bureau Office (Excel, PowerPoint et Word)

- Canaux et messages de conversations Microsoft Teams
    
Une fois la stratégie synchronisée avec les emplacements adéquats, elle commence à évaluer le contenu et à mettre en place des actions.
  
### <a name="policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites"></a>Évaluation des stratégies dans les sites OneDrive Entreprise et SharePoint Online

Dans l’ensemble de vos sites SharePoint Online et OneDrive Entreprise, les documents changent constamment : ils sont continuellement créés, modifiés, partagés, etc. Cela signifie que les documents peuvent à tout moment soit être en conflit, soit être conformes à la stratégie DLP. Par exemple, une personne peut télécharger un document ne contenant aucune information sensible sur le site de son équipe mais une autre personne peut ensuite modifier le même document et y ajouter des informations sensibles.
  
Pour cette raison, les stratégies DLP vérifient les correspondances de stratégie fréquemment dans les documents en arrière-plan. Vous pouvez considérer ceci comme une évaluation asynchrone des stratégies.
  
#### <a name="how-it-works"></a>Mode de fonctionnement
 
Au fur et à mesure de l’ajout ou de la modification de documents dans ses sites, le moteur de recherche analyse le contenu de sorte que vous puissiez le rechercher ultérieurement. Pendant ce temps, le contenu est également analysé pour vérifier s’il présente des informations sensibles et s’il est partagé. Les informations sensibles trouvées sont stockées en toute sécurité dans l’index de recherche, afin que seule l’équipe de conformité puisse y accéder, et pas les utilisateurs standard. Chaque stratégie DLP que vous avez activée s’exécute en arrière-plan (de façon asynchrone), en vérifiant fréquemment le contenu qui correspond à une stratégie et en appliquant des actions pour le protéger de toute divulgation accidentelle.
  
![Diagramme montrant comment la stratégie DLP évalue le contenu de façon asynchrone](media/bdf73099-039a-4909-ae89-ac12c41992ba.png)
  
Enfin, les documents peuvent entrer en conflit avec une stratégie DLP, mais ils peuvent également y devenir conformes. Par exemple, si une personne ajoute des numéros de carte de crédit à un document, une stratégie DLP peut alors bloquer l’accès au document automatiquement. Toutefois, si cette personne supprime ensuite les informations sensibles, l’action (dans ce cas, le blocage) est annulée automatiquement à la prochaine évaluation du document par rapport à la stratégie.
  
La DLP évalue le contenu pouvant être indexé. Pour plus d’informations sur les types de fichiers analysés par défaut, consultez la rubrique [Extensions de nom de fichier et types de fichier analysés par défaut dans SharePoint Server](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types).
  
### <a name="policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web"></a>Évaluation des stratégies dans Exchange Online, Outlook et Outlook sur le web

Lorsque vous créez une stratégie DLP incluant Exchange Online en tant qu’emplacement, celle-ci est synchronisée à partir du centre de conformité et de sécurité Office 365 avec Exchange Online, puis d’Exchange Online vers Outlook sur le web et Outlook.
  
Lors de la rédaction d’un message dans Outlook, l’utilisateur peut voir les conseils de stratégie, puisque le contenu en cours de création est évalué par rapport aux stratégies DLP. Une fois le message envoyé, il est évalué par rapport aux stratégies DLP comme élément normal du flux de messagerie, en même temps que les règles de flux de courrier Exchange (règles de transport) et les stratégies DLP créées dans le centre d’administration Exchange. Les stratégies DLP analysent le message ainsi que les éventuelles pièces jointes.
  
### <a name="policy-evaluation-in-the-office-desktop-programs"></a>Évaluation des stratégies dans les programmes de bureau Office

Excel, PowerPoint et Word incluent la même capacité à identifier les informations sensibles et à appliquer les stratégies DLP que SharePoint Online et OneDrive Entreprise. Ces programmes Office synchronisent leurs stratégies DLP directement à partir du magasin central de stratégies, puis évaluent en permanence le contenu par rapport aux stratégies DLP lorsque les utilisateurs travaillent avec des documents ouverts à partir d’un site inclus dans une stratégie DLP.
  
L’évaluation des stratégies DLP dans Office est conçue pour ne pas avoir d’incidence sur les performances des programmes ou la productivité des personnes qui travaillent sur le contenu. Si elles travaillent sur un document volumineux ou que l’ordinateur de l’utilisateur est occupé, l’affichage d’un conseil de stratégie peut prendre quelques secondes.

### <a name="policy-evaluation-in-microsoft-teams"></a>Évaluation des stratégies dans Microsoft Teams
 
Lorsque vous créez une stratégie DLP qui inclut Microsoft Teams comme emplacement, celle-ci est synchronisée à partir du centre de conformité et de sécurité Office 365 avec les comptes utilisateurs et les canaux et messages de conversation Microsoft Teams. Selon la configuration des stratégies DLP, lorsque quelqu’un tente de partager des informations sensibles dans une conversation ou un message de canal Microsoft Teams, le message peut être bloqué ou révoqué. Les documents qui contiennent des informations sensibles et qui sont partagés avec des invités (utilisateurs externes) ne s’ouvrent pas pour ces utilisateurs. Consultez l’article sur la [protection contre la perte de données et Microsoft Teams](dlp-microsoft-teams.md) pour obtenir plus d’informations à ce sujet.
 
## <a name="permissions"></a>Autorisations

Les membres de votre équipe de mise en conformité qui créeront des stratégies DLP ont besoin des autorisations d’accès au Centre de conformité et de sécurité. Par défaut, votre administrateur de client a accès à cet emplacement et peut autoriser des agents de conformité et d’autres personnes à accéder au Centre de sécurité et conformité, sans pour autant leur octroyer toutes les autorisations d’un administrateur de client. Pour cela, nous vous recommandons de :
  
1. Créer un groupe dans Office 365 et d’y ajouter des responsables de la mise en conformité.
    
2. Créer un groupe de rôles sur la page **Autorisations** du Centre de sécurité et de conformité. 
    
3. Ajouter le groupe Office 365 au groupe de rôles.
    
Pour plus d’informations, voir [Give users access to the Office 365 Compliance Center](grant-access-to-the-security-and-compliance-center.md).
  
Ces autorisations sont requises uniquement pour créer et appliquer une stratégie DLP. L’application d’une stratégie ne nécessite pas d’accès au contenu.
  
## <a name="find-the-dlp-cmdlets"></a>Trouver les applets de commande DLP

Pour utiliser la plupart des applets de commande du Centre de conformité et de sécurité, vous devez :
  
1. [Vous connecter au Centre de sécurité &amp; conformité Office 365 à l’aide de PowerShell à distance](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)
    
2. Utiliser l’une de ces [applets de commande de stratégie et de conformité DLP](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/export-dlppolicycollection?view=exchange-ps)
    
Toutefois, les rapports DLP doivent extraire des d’Office 365, y compris Exchange Online. Pour cette raison, les **applets de commande des rapports DLP sont disponibles dans Exchange Online Powershell (et non dans le centre de conformité &amp; sécurité Powershell)**. Par conséquent, pour utiliser les applets de commande pour les rapports DLP, vous devez :
  
1. [Vous connecter à Exchange Online à l'aide de Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)
    
2. Utilisez l’une de ces applets de commande pour les rapports DLP :
    
  - [Get-DlpDetectionsReport](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpDetectionsReport?view=exchange-ps)
    
  - [Get-DlpDetailReport](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpDetailReport?view=exchange-ps)
    
## <a name="more-information"></a>Plus d’informations

- [Création d’une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md)
    
- [Envoyer des notifications et afficher des conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md)
    
- [Créer une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés](protect-documents-that-have-fci-or-other-properties.md)
    
- [Contenu des modèles de stratégie DLP](what-the-dlp-policy-templates-include.md)
    
- [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)
    
- [Éléments recherchés par les fonctions DLP](what-the-dlp-functions-look-for.md)
    
- [Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md)
    

