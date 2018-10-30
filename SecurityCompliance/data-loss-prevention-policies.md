---
title: Vue d’ensemble des stratégies de protection contre la perte de données
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 1966b2a7-d1e2-4d92-ab61-42efbb137f5e
description: Avec une stratégie de protection contre la perte données de sécurité Office 365 &amp; centre de conformité, vous pouvez identifier, analyser et protéger automatiquement les informations sensibles dans Office 365.
ms.openlocfilehash: b342686f38d734a0eff0df896204d7a2f4bfde6a
ms.sourcegitcommit: 81e06e09bf5ca8e3f51b164d6251b1c35b3285cf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "25829195"
---
# <a name="overview-of-data-loss-prevention-policies"></a>Vue d’ensemble des stratégies de protection contre la perte de données

Pour être conforme aux réglementations métiers, les organisations doivent protéger les informations sensibles et sa divulgation accidentelle. Données financières ou les informations d’identification personnelle (PII) comme numéros de carte de crédit, numéros de sécurité sociale ou des enregistrements d’intégrité sont des exemples d’informations sensibles que vous pouvez éviter la fuite en dehors de votre organisation. Avec une stratégie de protection contre la perte données de sécurité Office 365 &amp; centre de conformité, vous pouvez identifier, analyser et protéger automatiquement les informations sensibles dans Office 365.
  
Avec une stratégie DLP, vous pouvez :
  
- **Identifier les informations sensibles sur de nombreux sites, tels que Exchange Online, SharePoint Online et OneDrive for Business.**
    
    Par exemple, vous pouvez identifier n’importe quel document contenant un numéro de carte de crédit qui est stocké dans n’importe quel site Business OneDrive, ou vous pouvez surveiller les sites OneDrive des personnes spécifiques.
    
- **Empêcher le partage accidentel d’informations sensibles** 
    
    Par exemple, vous pouvez identifier un document ou un courrier électronique contenant un enregistrement d’intégrité qui est partagé avec des personnes extérieures à votre organisation, et puis automatiquement bloquer l’accès à ce document ou bloquer le message électronique d’être envoyés.
    
- **Surveiller et protéger les informations sensibles dans les versions de bureau d’Excel 2016, de PowerPoint 2016 et de Word 2016**
    
    Comme dans Exchange Online, SharePoint Online et OneDrive entreprise, ces applications bureautiques Office 2016 incluent les mêmes capacités pour identifier les informations sensibles et appliquer les stratégies DLP. DLP fournit une surveillance en continu lorsque des personnes partagent le contenu de ces programmes Office 2016.
    
- **aider les utilisateurs à respecter les règles de conformité sans interrompre leur flux de travail ; et**
    
    Vous pouvez informer vos utilisateurs stratégies DLP et leur permettre de rester conforme sans blocage leur travail. Par exemple, si un utilisateur tente de partager un document contenant des informations sensibles, une stratégie DLP peut à la fois leur envoyer une notification par courrier électronique et les afficher un Conseil de stratégie dans le contexte de la bibliothèque de documents qui leur permet de remplacer la stratégie s’ils disposent d’une entreprise justification. Les conseils de stratégie même apparaissent également dans Outlook sur le web, Outlook 2013 et ultérieures, Excel 2016, 2016 PowerPoint et Word 2016.
    
- **Afficher DLP les rapports affichant le contenu qui établit une correspondance avec les stratégies DLP de votre organisation.**
    
    Pour évaluer la façon dont votre organisation se conforme à une stratégie DLP, vous pouvez voir combien établit une correspondance avec chaque stratégie et règle possède au fil du temps. Si une stratégie DLP permet aux utilisateurs de remplacer un Conseil de stratégie et de signaler un faux positif, vous pouvez également afficher ce que les utilisateurs ont signalés.
    
Créer et gérer des stratégies DLP dans la page de prévention de perte de données de sécurité Office 365 &amp; centre de conformité.
  
![Page de protection contre la perte de données de sécurité Office 365 &amp; centre de conformité](media/943fd01c-d7aa-43a9-846d-0561321a405e.png)
  
## <a name="what-a-dlp-policy-contains"></a>Contenu d’une stratégie DLP

Une stratégie DLP contient quelques éléments de base :
  
- WHERE protéger le contenu - **emplacements** tels que Exchange Online, SharePoint Online et OneDrive pour les sites de l’entreprise. 
    
- Circonstances de protection du contenu en appliquant des **règles** comprenant les éléments suivants : 
    
  - **Conditions** , le contenu doit correspondre avant que la règle est appliquée, par exemple, recherchez uniquement contenu contenant les numéros de sécurité sociale qui a été partagé avec des personnes extérieures à votre organisation. 
    
  - **Actions** que vous voulez que la règle exécute automatiquement lorsque du contenu répondant aux conditions est trouvé, par exemple, bloquer l’accès au document et envoyer à l’utilisateur et au responsable de la mise en conformité une notification par courrier électronique. 
    
Vous pouvez utiliser une règle pour répondre à une demande de protection spécifiques et ensuite utiliser une stratégie DLP pour regrouper les exigences de protection courants, tels que toutes les règles nécessaires pour se conformer à une réglementation spécifique.
  
Par exemple, vous pouvez avoir une stratégie DLP qui vous permet de détecter la présence d’informations peuvent être les Health Insurance Portability Accountability Act (HIPAA). Cette stratégie DLP peut protéger les données HIPAA (que) sur tous les sites SharePoint Online et OneDrive tous les sites de commerce (where) en recherchant tout document contenant ces informations sensibles sont partagées avec des personnes extérieures à votre organisation (la conditions) bloque l’accès au document et envoyer de notification (actions). Ces conditions sont stockées sous forme de règles individuelles et regroupées comme une stratégie DLP pour simplifier la gestion et création de rapports.
  
![Diagramme affichant la stratégie DLP contenant les règles et les emplacements](media/c006860c-2d00-42cb-aaa4-5b5638d139f7.png)
  
### <a name="locations"></a>Emplacements

Pour rechercher et protection des informations sensibles dans Office 365, si ces informations sont situées dans Exchange Online, SharePoint Online, OneDrive entreprise ou une stratégie DLP. Vous pouvez facilement choisir de protéger tous les comptes de OneDrive, ou les sites SharePoint sites spécifiques ou les comptes ou toutes les boîtes aux lettres. Notez qu’il n’est pas encore possible de sélectionner uniquement les boîtes aux lettres d’utilisateurs spécifiques.
  
![Options pour les emplacements dans lesquels une stratégie DLP peut être appliquée](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
Notez que si vous choisissez d’inclure ou exclure des sites SharePoint spécifiques ou les comptes de OneDrive, une stratégie DLP peut contenir pas plus de 100 ces inclusions et exclusions. Bien que cette limite existe, comprendre que vous pouvez dépasser cette limite en appliquant une stratégie qui s’applique aux emplacements entières ou une stratégie à l’échelle de l’organisation.
  
### <a name="rules"></a>Règles

Les règles sont qu’appliquer des besoins de votre entreprise sur le contenu de votre organisation. Une stratégie contient une ou plusieurs règles et chaque règle se compose de conditions et actions. Pour chaque règle, lorsque les conditions sont remplies, les actions sont effectuées automatiquement. Règles sont exécutées dans l’ordre, en commençant par la règle de priorité la plus élevée de chaque stratégie.
  
Une règle offre également des options pour avertir les utilisateurs (avec conseils de stratégie et notifications par courrier électronique) et administrateurs (avec les rapports d’incidents électroniques) contenu déclenchant la règle.
  
Voici les composants d’une règle, chacune décrite ci-dessous.
  
![Sections de l’éditeur de règles DLP](media/1859d504-b9c2-45ed-961b-a0092251acc2.png)
  
#### <a name="conditions"></a>Conditions

Les conditions sont importantes, car ils déterminent quels types d’informations que vous recherchez et une opération à effectuer. Par exemple, vous pouvez choisir d’ignorer le contenu qui contiennent des nombres passport, sauf si le contenu contient plus de dix de ces numéros et est partagé avec des personnes extérieures à votre organisation.
  
Conditions de se concentrent sur le **contenu**, telles que les types d’informations sensibles que vous recherchez, ainsi que sur le **contexte**, tel que qui le document est partagé avec. Vous pouvez utiliser des conditions pour affecter des actions différentes à différents niveaux de risque, par exemple, sensible contenu partagé en interne peut être de réduire les risques et nécessitent des actions moins nombreuses que sensible contenu partagé avec des personnes en dehors de l’organisation. 
  
![Liste affichant les conditions DLP disponibles](media/0fa43f90-d007-4506-ae93-43e8424fe103.png)
  
Les conditions actuellement disponibles peuvent déterminer si :
  
- Contenu contient un type d’informations sensibles.
    
- Contenu contient une étiquette. Pour plus d’informations, voir le ci-dessous section [à l’aide d’une étiquette comme une condition dans une stratégie DLP](data-loss-prevention-policies.md#label).
    
- Le contenu est partagé avec des personnes extérieures ou internes à votre organisation.
    
#### <a name="types-of-sensitive-information"></a>Types d’informations sensibles

Une stratégie DLP permet de protéger les informations sensibles, qui sont définies comme un **type d’informations sensibles**. Office 365 inclut des définitions pour de nombreux types d’informations sensibles courantes dans plusieurs régions différentes qui sont prêtes à utiliser, par exemple un numéro de carte de crédit, numéros de compte bancaire, nationales numéros d’identification et les numéros de passeport. 
  
![Liste des types d’informations sensibles disponibles](media/3eaa9911-bc94-44be-902f-363dbf3b07fe.png)
  
Lorsqu’une stratégie DLP recherche pour un type d’informations sensibles comme un numéro de carte de crédit, il ne s’affiche simplement un nombre à 16 chiffres. Chaque type d’informations sensibles est défini et détecté à l’aide d’une combinaison de :
  
- Mots clés
    
- Fonctions internes pour valider les sommes de contrôle ou la composition
    
- Évaluation d’expressions régulières pour rechercher des correspondances au modèle
    
- Autres examens de contenu
    
Cela permet d’obtenir un degré de précision tout en réduisant le nombre de faux positifs qui peut interrompre œuvres détection DLP.
  
#### <a name="actions"></a>Actions

Lorsque le contenu correspond à une condition dans une règle, vous pouvez appliquer les actions pour protéger automatiquement le contenu.
  
![Liste des actions DLP disponibles](media/8aef17fc-1e99-4ac7-adfc-0f2c9c1a0697.png)
  
Avec les actions disponibles maintenant, vous pouvez :
  
- **Restreindre l’accès au contenu** Pour le contenu du site, cela signifie que les autorisations pour le document sont réservées pour tout le monde sauf les administrateur de collection de sites principal, le propriétaire du document et la personne qui a modifié le document. Ces personnes peuvent supprimer les informations sensibles dans le document ou prendre d’autres mesures correctives. Lorsque le document est en conformité, les autorisations d’origine seront restaurées automatiquement. Lorsque l’accès à un document est bloqué, le document s’affiche avec une icône de Conseil de stratégie spécifiques dans la bibliothèque sur le site. 
    
    ![Conseil de stratégie montrant que l’accès au document est bloqué](media/b6cefed3-d212-43d7-8534-4b92b26ebd50.png)
  
    Pour le contenu du courrier électronique, cette action bloque le message envoyé. Selon la configuration de la règle DLP, l’expéditeur s’affiche un rapport de non-remise ou (si la règle utilise une notification) une notification de Conseil et/ou de messagerie de stratégie.
    
    ![Que les destinataires non autorisés doivent être supprimés à partir du message d’avertissement](media/302f9994-912d-41e7-861f-8a4539b3c285.png)
  
#### <a name="user-notifications-and-user-overrides"></a>Notifications d’utilisateur et les substitutions par l’utilisateur

Vous pouvez utiliser des notifications et que vous remplace pour informer vos utilisateurs stratégies DLP et leur permettre de rester conforme sans blocage leur travail. Par exemple, si un utilisateur tente de partager un document contenant des informations sensibles, une stratégie DLP peut à la fois leur envoyer une notification par courrier électronique et les afficher un Conseil de stratégie dans le contexte de la bibliothèque de documents qui leur permet de remplacer la stratégie s’ils disposent d’une entreprise justification.
  
![Utilisateur et les notifications de l’utilisateur remplace les sections de l’éditeur de règles DLP](media/37b560d4-6e4e-489e-9134-d4b9daf60296.png)
  
Le courrier électronique peut informer la personne qui a envoyé, partagé ou la dernière modification du contenu et, pour le contenu du site, l’administrateur de collection de sites principal et le propriétaire du document. En outre, vous pouvez ajouter ou supprimer une personne vous choisissez à partir de la notification par courrier électronique.
  
Outre l’envoi d’une notification par courrier électronique, une notification de l’utilisateur affiche un Conseil de stratégie :
  
- Dans Outlook 2013 et versions ultérieures et Outlook sur le web.
    
- Pour le document sur un SharePoint Online ou OneDrive pour le site de l’entreprise.
    
- Dans Excel, 2016, 2016 PowerPoint et Word 2016, lorsque le document est stocké sur un site inclus dans une stratégie DLP.
    
La notification par courrier électronique et le Conseil de stratégie expliquent pourquoi le contenu est en conflit avec une stratégie DLP. Si vous choisissez, l’info-bulle notification et la stratégie de messagerie permet aux utilisateurs de remplacer une règle par un faux positif de création de rapports ou fournir une justification. Cela peut vous aider à former les utilisateurs sur vos stratégies DLP et les appliquer sans empêcher les utilisateurs d’effectuer leur travail. Plus d’informations sur les substitutions et de faux positifs sont également connectés pour la création de rapports (voir ci-dessous sur les rapports DLP) et inclus dans l’incident rapports (section suivante), afin que le responsable de la conformité permettre consulter régulièrement cette information.
  
Voici un Conseil de stratégie Aperçu dans un OneDrive pour un compte professionnel.
  
![Conseil de stratégie pour un document dans un compte OneDrive](media/f9834d35-94f0-4511-8555-0fe69855ce6d.png)
  
#### <a name="incident-reports"></a>Rapports d’incident

Lorsqu’une règle est mis en correspondance, vous pouvez envoyer un rapport d’incident à votre responsable de la conformité (ou les personnes que vous choisissez) avec des détails de l’événement. Ce rapport consacrée des informations sur l’élément qui a été mis en correspondance, le contenu réel qui correspondent à la règle et le nom de la personne qui a modifié le contenu. Pour les messages électroniques, le rapport inclut également en tant que pièce jointe au message d’origine qui correspond à une stratégie DLP.
  
![Page de configuration de rapports d’incident](media/31c6da0e-981c-415e-91bf-d94ca391a893.png)
  
## <a name="grouping-and-logical-operators"></a>Opérateurs logiques et de regroupement

Souvent votre stratégie DLP présente simple, par exemple pour identifier tout le contenu qui contient un numéro de sécurité sociale américain. Toutefois, dans d’autres scénarios, votre stratégie DLP devront identifier des données plus faiblement définies.
  
Par exemple, pour identifier le contenu soumis à l’us Health Insurance Act (HIPAA), vous devez rechercher :
  
- Contenu qui contient des types spécifiques d’informations sensibles, telles qu’un numéro de sécurité sociale américain ou le numéro de l’application de Drug Enforcement Agency (DEA).
    
    AND
    
- Le contenu qui est plus difficile à identifier, telles que les communications relatives aux soins d’un patient ou les descriptions des services médicaux fournis. Identification de ce contenu nécessite de mots clés à partir des listes de mot clé très volumineuses, telles que l’International Classification de maux (ICD-9-CM ou ICD-10-CM).
    
Vous pouvez facilement identifier ces données faiblement définies à l’aide des opérateurs de regroupement et logiques (AND, OR). Lorsque vous créez une stratégie DLP, vous pouvez :
  
- Groupe de types d’informations sensibles.
    
- Sélectionnez l’opérateur logique entre les types d’informations sensibles au sein d’un groupe et entre les groupes eux-mêmes.
    
### <a name="choosing-the-operator-within-a-group"></a>L’opérateur au sein d’un groupe

Dans un groupe, vous pouvez choisir si tout ou partie des conditions de ce groupe doivent être satisfaites pour le contenu pour la correspondance de la règle.
  
![Groupe affichant les opérateurs dans le groupe](media/6a12f1e8-112d-48ee-9a73-82b3dd0542e7.png)
  
### <a name="adding-a-group"></a>Ajout d’un groupe

Vous pouvez rapidement ajouter un groupe, ce qui peut avoir ses propres conditions et l’opérateur de ce groupe.
  
![Ajouter le bouton groupe](media/5f72f292-d1f3-4f11-a911-a9f71e10abf6.png)
  
### <a name="choosing-the-operator-between-groups"></a>L’opérateur entre les groupes

Entre les groupes, vous pouvez choisir si les conditions dans un groupe ou tous les groupes doivent être satisfaites pour le contenu pour la correspondance de la règle.
  
Par exemple, la stratégie **Américaine HIPAA** intégrée a une règle qui utilise l’opérateur **et** entre les groupes afin qu’il identifie le contenu qui contient : 
  
- dans le groupe **Identificateurs PII** (au moins un SSN numéro **ou** DEA) 
    
    **ET**
    
- dans le groupe **Termes médicaux** (au moins un mot-clé de mot clé **ou** ICD-10-CM ICD-9-CM) 
    
![Groupes affichant l’opérateur entre les groupes](media/354aa77f-569c-4847-9dfe-605ee2bb28d1.png)
  
## <a name="the-priority-by-which-rules-are-processed"></a>La priorité par lequel les règles sont traitées.

Lorsque vous créez des règles dans une stratégie, une priorité dans l’ordre dans lequel il est créé - ce qui signifie que la règle créée a tout d’abord la priorité est attribuée à chaque règle, la règle créée deuxième a priorité de la deuxième et ainsi de suite. Une fois que vous créez une règle, sa priorité ne peut pas être modifiée, sauf à supprimer et recréer.
  
![Règles dans l’ordre de priorité](media/f7dc06bf-bc6f-485c-bcdb-606edbcf6565.png)
  
Lorsque le contenu est évalué par rapport aux règles, les règles sont traitées dans l’ordre de priorité. Si le contenu correspond à plusieurs règles, les règles sont traitées dans l’ordre de priorité et l’action plus restrictive est appliquée. Par exemple, si le contenu correspond à toutes les règles suivantes, la règle 3 est appliqué car il s’agit de la priorité la plus élevée, la règle la plus restrictive :
  
- Règle 1 : signale uniquement les utilisateurs
    
- Règle 2 : informe les utilisateurs, restreint l’accès et autorise les substitutions par l’utilisateur
    
- Règle 3 : informe les utilisateurs, restreint l’accès et ne permet pas les substitutions par l’utilisateur
    
- Règle 4 : signale uniquement les utilisateurs
    
- Règle 5 : restreint l’accès
    
- Règle 6 : informe les utilisateurs, restreint l’accès et ne permet pas les substitutions par l’utilisateur
    
Dans cet exemple, notez que les correspondances pour toutes les règles sont enregistrées dans les journaux d’audit et affichées dans les rapports DLP, bien seulement la règle la plus restrictive est appliquée.
  
En ce qui concerne les conseils de stratégie, notez que :
  
- Uniquement le Conseil de stratégie à partir de la priorité la plus élevée, règle la plus restrictive s’affichera. Par exemple, un Conseil de stratégie à partir d’une règle qui bloque l’accès au contenu s’affichera sur un Conseil de stratégie à partir d’une règle qui envoie une notification. Cela empêche des personnes de voir une cascade de conseils de stratégie.
    
- Si les conseils de stratégie de la règle la plus restrictive autorisent les utilisateurs à remplacer la règle, toute autre règle également mise en correspondance avec le contenu est aussi remplacée.
    
## <a name="tuning-rules-to-make-them-easier-or-harder-to-match"></a>Pour les rendre plus facile ou plus difficile à respecter les règles de réglage

Une fois que les personnes créer et activer leurs stratégies DLP, ils parfois exécuter ces problèmes en :
  
- Trop de contenu **n’est pas** des informations sensibles établit une correspondance avec les règles - en d’autres termes, trop de faux positifs. 
    
- Trop peu de contenu que les informations sensibles **est** établit une correspondance avec les règles, en d’autres termes, les mesures de protection ne sont pas appliqués sur les informations sensibles. 
    
Pour résoudre ces problèmes, vous pouvez régler vos règles en ajustant le nombre d’instances et correspondent à la précision pour le rendre plus difficiles ou plus faciles à respecter les règles de contenu. Chaque type d’informations sensibles utilisé dans une règle possède à la fois une instance count et correspondent à la précision.
  
### <a name="instance-count"></a>Nombre d’instances

Nombre d’instances signifie simplement le nombre d’occurrences d’un type spécifique d’informations sensibles doit être présent pour le contenu pour la correspondance de la règle. Par exemple, contenu correspondra à la règle ci-dessous si les numéros de passeport sont identifiés entre 1 et 9 américain ou britannique unique.
  
Notez que le nombre d’instances inclut uniquement les correspondances **unique** pour les types d’informations sensibles et les mots clés. Par exemple, si un message électronique contient 10 occurrences portant le même numéro de carte de crédit, les 10 occurrences compter en tant qu’une seule instance d’un numéro de carte de crédit. 
  
Pour utiliser le nombre d’instances pour adapter les règles, les instructions sont simple :
  
- Pour faciliter la règle à respecter, diminuer le nombre **min** et/ou l’augmentation du nombre **maximal** . Vous pouvez également définir **max** à **tout** en supprimant la valeur numérique. 
    
- Pour rendre la règle plus difficile à respecter, augmentez le nombre **min** . 
    
En règle générale, vous utilisez des actions moins restrictives, telles que l’envoi des notifications de l’utilisateur, dans une règle avec un nombre inférieur d’instances (par exemple, 1-9). Et que vous utilisez des actions plus restrictives, telles que la restriction de l’accès au contenu sans autoriser les substitutions par l’utilisateur, dans une règle avec un nombre d’instances plus élevé (par exemple, 10-any).
  
![Instance de compte dans l’éditeur de règles](media/e7ea3c12-72c5-4bb3-9590-c924c665e84d.png)
  
### <a name="match-accuracy"></a>Exactitude de la correspondance

Comme indiqué ci-dessus, un type d’informations sensibles défini et détecté à l’aide d’une combinaison de différents types d’éléments de preuve. Généralement, un type d’informations sensibles est défini par plusieurs de ces combinaisons, appelés modèles. Un modèle qui nécessite moins de preuve a un exactitude de la correspondance inférieur (ou un niveau de confiance) lors d’un modèle qui nécessite que des signes plus dispose d’un plus précise de correspondance (ou un niveau de confiance). Pour plus d’informations sur les modèles réels et les niveaux de confiance utilisés par chaque type d’informations sensibles, voir [Rechercher quels types d’informations sensibles](what-the-sensitive-information-types-look-for.md).
  
Par exemple, le type d’informations sensibles appelé numéro de carte de crédit est défini par deux modèles :
  
- Un motif en toute confiance 65 % qui requiert :
    
  - Un nombre au format d’un numéro de carte de crédit.
    
  - Nombre qui transmet la somme de contrôle.
    
- Un motif en toute confiance 85 % qui requiert :
    
  - Un nombre au format d’un numéro de carte de crédit.
    
  - Nombre qui transmet la somme de contrôle.
    
  - Un mot clé ou une date d’expiration au format approprié.
    
Vous pouvez utiliser ces confiance niveaux (ou l’exactitude de la correspondance) dans vos règles. En règle générale, vous utilisez des actions moins restrictives, telles que l’envoi des notifications de l’utilisateur, dans une règle avec l’exactitude de la correspondance inférieur. Et que vous utilisez des actions plus restrictives, telles que la restriction de l’accès au contenu sans autoriser les substitutions par l’utilisateur, dans une règle avec l’exactitude de la correspondance supérieur.
  
Il est important de comprendre que lorsqu’un type spécifique d’informations sensibles, comme un numéro de carte de crédit, est identifié dans le contenu, uniquement un niveau de confiance unique est renvoyé :
  
- Si toutes les correspondances sont pour un seul modèle, le niveau de confiance pour ce modèle est renvoyé.
    
- Pour plus d’un modèle de correspondances (autrement dit, des correspondances avec deux niveaux de confiance différents), un niveau de confiance supérieur les modèles seul seul est renvoyé. Il s’agit de la difficulté. Par exemple, pour une carte de crédit, si les modèles de 65 % et de 85 % sont mis en correspondance, le niveau de confiance retournées pour que le type d’informations sensibles est supérieure à 90 % car les signes plus signifie plus de confiance.
    
Ainsi, si vous souhaitez créer deux règles mutuellement pour la carte de crédit, un pour l’exactitude de la correspondance de 65 % et un pour l’exactitude de la correspondance de 85 %, les plages pour l’exactitude de la correspondance se présente comme suit. La première règle récupère uniquement les correspondances de la chaîne de 65 %. La deuxième règle chercher établit une correspondance avec **au moins une** correspondance de 85 % et **peut avoir** autres correspondances de confiance inférieur. 
  
![Deux règles avec des plages différentes pour l’exactitude de la correspondance](media/21bdfe36-7a91-4347-8098-11809a92f9a4.png)
  
Pour ces raisons, les instructions pour la création de règles avec correspondance différentes précisions sont :
  
- Le niveau de confiance plus faible utilise généralement la même valeur pour les fonctions **min** et **max** (pas dans une plage). 
    
- Le niveau de confiance plus élevé est généralement une plage à partir de juste au-dessus du niveau de confiance inférieur à 100.
    
- Les niveaux de confiance entre allant généralement juste au-dessus du niveau de confiance inférieur juste en dessous du niveau de confiance plus élevé.
    
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a>Utilisation d’une étiquette comme condition dans une stratégie DLP

Vous pouvez créer une étiquette, puis :
  
- **Publier** , afin que les utilisateurs finaux peuvent voir et appliquer manuellement l’étiquette pour le contenu. 
    
- **Auto-appliquer** à du contenu qui correspond aux conditions que vous choisissez. 
    
Pour plus d’informations sur les étiquettes, voir [vue d’ensemble des étiquettes de rétention](labels.md).
  
Après avoir créé une étiquette, vous pouvez ensuite utiliser cette étiquette comme une condition dans vos stratégies DLP. Par exemple, vous pouvez souhaiter car :
  
- Vous avez publié un label nommé **confidentiel**, afin que les personnes de votre organisation peuvent appliquer manuellement l’étiquette aux documents et confidentiel email. À l’aide de cette étiquette comme une condition dans votre stratégie DLP, vous pouvez restreindre le contenu intitulé **confidentiel** d’être partagés avec des personnes extérieures à votre organisation. 
    
- Vous créé un label nommé **Alpine House** pour un projet du même nom, puis appliqués automatiquement cette étiquette pour le contenu contenant les mots clés « Alpine House ». À l’aide de cette étiquette comme une condition dans votre stratégie DLP, vous pouvez afficher un Conseil de stratégie aux utilisateurs finaux lorsqu’ils sont sur le point de partager ce contenu avec une personne extérieure à votre organisation. 
    
- Vous avez publié un label nommé **enregistrement taxe**, afin que votre gestionnaire d’enregistrements peut appliquer manuellement l’étiquette pour le contenu qui doit être considéré comme un enregistrement. À l’aide de cette étiquette comme une condition dans votre stratégie DLP, vous pouvez rechercher le contenu avec cette étiquette conjointement avec d’autres types d’informations sensibles telles que ITINs ou de sécurité sociale ; appliquer les actions de protection contenu intitulé **enregistrement taxe**; obtenir des rapports sur les activités détaillées à propos de la stratégie DLP dans les rapports DLP et des données du journal d’audit. 
    
- Vous avez publié une étiquette appelée **Équipe dirigeante exécutif - critiques** pour les boîtes aux lettres Exchange et les comptes de OneDrive d’un groupe de cadres. À l’aide de cette étiquette comme une condition dans votre stratégie DLP, vous pouvez appliquer les actions de rétention et de protection sur le même sous-ensemble de contenu et les utilisateurs. 
    
À l’aide des étiquettes comme une condition dans vos règles DLP, pourrez vous appliquer de façon sélective des actions de protection sur un ensemble spécifique de contenu, les emplacements ou les utilisateurs.
  
![Étiquettes comme une condition](media/5b1752b4-a129-4a88-b010-8dcf8a38bb09.png)

### <a name="support-for-sensitivity-labels-is-coming"></a>Prise en charge des étiquettes de sensibilité est bientôt

Notez que vous pouvez utiliser actuellement une étiquette de rétention uniquement en tant qu’une condition, pas une [étiquette de sensibilité](sensitivity-labels.md). Nous sommes actuellement en train de prise en charge pour l’utilisation d’une étiquette de sensibilité dans cette condition.
  
### <a name="how-this-feature-relates-to-other-features"></a>Comment cette fonctionnalité est lié à d’autres fonctionnalités

Plusieurs fonctionnalités peuvent être appliquées au contenu contenant des informations sensibles :
  
- Une [étiquette de rétention](labels.md#applying-a-retention-label-automatically-based-on-conditions) et une [stratégie de rétention](retention-policies.md) peuvent appliquer des actions de **rétention** sur ce contenu. 
    
- Une stratégie DLP peut appliquer les actions de **protection** sur ce contenu. Et avant d’appliquer ces actions, une stratégie DLP peut requérir d’autres conditions à respecter en plus du contenu qui contient une étiquette. 
    
![Diagramme des fonctionnalités qui peuvent s’appliquent à des informations sensibles](media/dd410f97-a3a3-455c-a1e9-7ed8ae6893d6.png)
  
Notez qu’une stratégie DLP est une fonctionnalité de détection plus riche à une stratégie d’étiquette ou de rétention appliquée à des informations sensibles. Une stratégie DLP peut appliquer les mesures de protection du contenu qui contient des informations sensibles, et si le contenu sont supprimées les informations sensibles, ces mesures de protection sont annulées à la prochaine qu'analyse du contenu. Mais si une stratégie de rétention ou une étiquette est appliqué au contenu contenant des informations sensibles, qui est une action unique qui n’est pas annulée même si les informations sensibles supprimé.
  
En utilisant une étiquette comme une condition dans une stratégie DLP, vous pouvez appliquer les actions de rétention et de protection sur le contenu avec cette étiquette. Vous pouvez considérer de contenu contenant une étiquette exactement comme contenant des informations sensibles de contenu : une étiquette et un type d’informations sensibles sont des propriétés utilisées pour la classification de contenu, afin que vous pouvez appliquer les actions de ce contenu.
  
![Diagramme de la stratégie DLP à l’aide d’étiquette en tant que condition](media/4538fd8f-fb74-4743-bc22-a5de33adfebb.png)
  
## <a name="simple-settings-vs-advanced-settings"></a>Paramètres simples et paramètres avancés

Lorsque vous créez une stratégie DLP, vous allez choisir entre les paramètres de simples ou avancées :
  
- **Paramètres simples** facilitent créer le type les plus courantes de stratégie DLP sans l’aide de l’éditeur de règles pour créer ou modifier des règles. 
    
- **Paramètres avancés** permet de l’éditeur de règles pour vous donner le contrôle total sur tous les paramètres de votre stratégie DLP. 
    
Ne vous inquiétez pas, en coulisses, paramètres simples et avancée de travail exactement les mêmes, par application de règles composés des conditions et actions--uniquement avec les paramètres simples, vous ne voyez pas l’éditeur de règles. C’est un moyen rapide pour créer une stratégie DLP.
  
### <a name="simple-settings"></a>Paramètres simples

Le scénario le plus courant DLP est de loin, création d’une stratégie pour protéger le contenu contenant des informations sensibles d’être partagés avec des personnes en dehors de votre organisation et exécute une action de réparation automatique comme restriction qui peuvent accéder au contenu, l’envoi des notifications de l’administrateur ou de l’utilisateur final et l’audit de l’événement d’enquête ultérieure. DLP permet d’empêcher la divulgation d’informations sensibles par inadvertance.
  
Pour simplifier cet objectif, lorsque vous créez une stratégie DLP, vous pouvez choisir **d’utiliser les paramètres simples**. Ces paramètres fournissent tout ce dont vous avez besoin pour implémenter la stratégie DLP les plus courantes, sans devoir ouvrir l’éditeur de règles.
  
![Options de DLP pour les paramètres simples et avancées](media/33c93824-ead5-43b6-9c3e-fd1630c92a7d.png)
  
### <a name="advanced-settings"></a>Paramètres avancés

Si vous avez besoin créer des stratégies DLP plus personnalisées, vous pouvez choisir **d’utiliser les paramètres avancés**.
  
Les paramètres avancés vous offrent de l’éditeur de règles, qui ont un contrôle total sur toutes les options possibles, y compris le nombre d’instances et correspondent à la précision (niveau de confiance) pour chaque règle.
  
Pour accéder rapidement à une section, cliquez sur un élément dans la partie supérieure de l’éditeur de règles pour accéder à la section ci-dessous.
  
![Menu de navigation supérieure de l’éditeur de règles DLP](media/c527b97f-ca53-4c79-ad19-1a63be8a8ecc.png)
  
## <a name="dlp-policy-templates"></a>Modèles de stratégies de protection contre la perte de données (DLP)

La première étape de création d’une stratégie DLP consiste à choisir les informations à protéger. À partir d’un modèle de DLP, vous enregistrez le travail de création d’un nouvel ensemble de règles à partir de zéro et de déterminer les types d’informations doivent être inclus par défaut. Vous pouvez ensuite ajouter à ou modifier ces exigences de réglage de la règle afin de répondre aux besoins spécifiques de votre organisation.
  
Un modèle de stratégie DLP préconfiguré peut vous aider à détecter des types spécifiques d’informations sensibles, telles que les données HIPAA, données PCI-DSS, données Gramm-Leach-Bliley Act ou informations d’identification personnelle locale spécifique (P.I.). Pour faciliter leur permet de rechercher et assurez la protection des informations sensibles courants, les modèles de stratégie inclus dans Office 365 déjà contient les types d’informations sensibles les plus courants nécessaires pour commencer.
  
![Liste des modèles de stratégies de protection contre la perte de données avec focus sur le modèle pour le Patriot Act des États-Unis](media/791b2403-430b-4987-8643-cc20abbd8148.png)
  
Votre organisation peut également disposer de ses propres besoins spécifiques, auquel cas vous pouvez créer une stratégie DLP à partir de zéro en choisissant l’option de **stratégie personnalisée** . Une stratégie personnalisée est vide et ne contient aucune règle prédéfini. 
  
## <a name="roll-out-dlp-policies-gradually-with-test-mode"></a>Déployer progressivement des stratégies DLP avec le mode test

Lorsque vous créez vos stratégies DLP, vous devez envisager de les déployer progressivement à évaluer leur impact et leur efficacité de test avant de les appliquer pleinement. Par exemple, vous ne voulez pas qu’une nouvelle stratégie DLP involontairement bloquer l’accès à des milliers de documents qui nécessitent un accès à personnes afin d’effectuer leur travail.
  
Si vous créez des stratégies DLP ayant un impact potentiel volumineux, nous vous recommandons de cet ordre :
  
1. **Démarrer en mode test sans conseils de stratégie** , puis utilisez la DLP rapports et des rapports de n’importe quel incident pour évaluer l’impact. Vous pouvez utiliser les rapports DLP permet d’afficher le nombre, emplacement, type et gravité de correspondances de stratégies. En fonction des résultats, vous pouvez régler les règles selon vos besoins. En mode test, les stratégies DLP aura aucun impact sur la productivité des personnes travaillant dans votre organisation. 
    
2. **Passer en mode Test avec les notifications et les conseils de stratégie** afin que vous pouvez commencer à apprendre aux utilisateurs sur vos stratégies de conformité et de les préparer pour les règles qui sont sur le point d’être appliquée. À ce stade, vous pouvez également demander aux utilisateurs de signaler les faux positifs afin que vous pouvez affiner les règles. 
    
3. **Démarrez l’application complète sur les stratégies** afin que les actions dans les règles sont appliquées et le contenu de le protégé. Continuez à surveiller les rapports DLP et tous les rapports d’incidents ou notifications pour vous assurer que les résultats sont ce que vous prévoyez. 
    
![Options pour l’utilisation du mode de test et l’activation de la stratégie](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
Vous pouvez désactiver une stratégie DLP à tout moment, ce qui affecte toutes les règles de la stratégie. Toutefois, chaque règle peut également être désactivée individuellement en basculant son statut dans l’éditeur de règles.
  
![Options de désactivation d’une règle dans une stratégie](media/f7b258ff-1b8b-4127-b580-83c6492f2bef.png)
  
## <a name="dlp-reports"></a>Rapports DLP

Après avoir créé et activer vos stratégies DLP, vous souhaiterez vérifier qu’ils sont destinés à vous le travail et pour vous aider à rester en conformité avec. Avec les rapports DLP, vous pouvez rapidement afficher le nombre de stratégie DLP et règle établit une correspondance avec le temps et le nombre de faux positifs et remplace. Pour chaque rapport, vous pouvez filtrer ces correspondances par emplacement, délai et même réduire à une stratégie spécifique, règle ou d’action.
  
Grâce aux rapports DLP, vous pouvez obtenir une vue d’ensemble des activités et :
  
- Vous concentrer sur des périodes spécifiques et comprendre les motifs des pics et des tendances
    
- Découvrez les processus métiers enfreignant les stratégies de conformité de votre organisation.
    
- Comprendre l’impact professionnel des stratégies DLP
    
En outre, vous pouvez utiliser les rapports DLP pour affiner vos stratégies DLP lorsque vous les exécutez.
  
![Rapports de tableau de bord dans le centre de conformité et de sécurité](media/6d741252-a0ce-4429-95ba-6c857ecc9a7e.png)
  
## <a name="how-dlp-policies-work"></a>Fonctionnement des stratégies DLP

DLP détecte les informations sensibles à l’aide d’une analyse approfondie du contenu (et pas d’une simple analyse de texte). Cette analyse approfondie utilise les correspondances de mots clés, les correspondances de dictionnaire, l’évaluation des expressions régulières, les fonctions internes et d’autres méthodes pour détecter le contenu qui correspond à vos stratégies DLP. Seul un petit pourcentage de vos données peut être considéré comme sensible. Une stratégie DLP peut identifier, surveiller et protéger automatiquement ces données uniquement, sans gêner ou affecter les personnes travaillant avec le reste de votre contenu.
  
### <a name="policies-are-synced"></a>Synchronisation des stratégies

Après avoir créé une stratégie DLP dans la sécurité &amp; centre de conformité, il a stockées dans un magasin central de stratégie, puis synchronisé avec différentes sources de contenu, y compris :
  
- Exchange Online et d’y pour Outlook sur le web et Outlook 2013 et versions ultérieures
    
- Sites OneDrive Entreprise
    
- Sites SharePoint Online
    
- Programmes de bureau Office 2016 (Excel 2016, PowerPoint 2016 et Word 2016)
    
Une fois que la stratégie de synchronisés aux emplacements adéquats, il commence à évaluer le contenu et appliquer des actions.
  
### <a name="policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites"></a>Évaluation des stratégies dans les sites OneDrive Entreprise et SharePoint Online

Sur tous les sites SharePoint Online et OneDrive pour les sites, les documents sont constamment — qu’ils sont continuellement en cours de création, modifié, partagé et ainsi de suite. Cela signifie que les documents peuvent entrer en conflit ou devenir compatibles avec une stratégie DLP à tout moment. Par exemple, une personne peut télécharger un document qui ne contient des informations sensibles aucune à leur site d’équipe, mais plus tard, une autre personne peut modifier le même document et ajouter des informations sensibles.
  
Pour cette raison, les stratégies DLP vérifient les correspondances de stratégie fréquemment dans les documents en arrière-plan. Vous pouvez considérer ceci comme une évaluation asynchrone des stratégies.
  
Voici comment cela fonctionne. Dans personnes ajouter ou modifier des documents dans leurs sites, le moteur de recherche analyse le contenu, afin que vous pouvez rechercher ultérieurement. Lorsque cela se produit, du contenu analysé également des informations sensibles et pour vérifier si elle est partagée. Toutes les informations sensibles sont trouvées sont stockées en toute sécurité dans l’index de recherche, afin que l’équipe de conformité uniquement peut accéder, mais pas les utilisateurs. Chaque stratégie DLP que vous avez activé exécute en arrière-plan (de façon asynchrone), vérification recherche fréquemment pour tout contenu qui correspond à une stratégie et en appliquant les actions pour protéger contre les fuites par inadvertance.
  
![Diagramme indiquant comment la stratégie DLP évalue le contenu en mode asynchrone](media/bdf73099-039a-4909-ae89-ac12c41992ba.png)
  
Enfin, les documents peuvent entrer en conflit avec une stratégie DLP, mais ils peuvent également y devenir conformes. Par exemple, si une personne ajoute des numéros de carte de crédit à un document, une stratégie DLP peut alors bloquer l’accès au document automatiquement. Toutefois, si cette personne supprime ensuite les informations sensibles, l’action (dans ce cas, le blocage) est annulée automatiquement à la prochaine évaluation du document par rapport à la stratégie.
  
DLP évalue tout contenu qui peut être indexé. Pour plus d’informations sur les types de fichiers sont analysés par défaut, voir les [extensions de nom de fichier et analysés par défaut des types de fichiers dans SharePoint Server 2013](https://go.microsoft.com/fwlink/p/?LinkID=627430).
  
### <a name="policy-evaluation-in-exchange-online-outlook-2013-and-later-and-outlook-on-the-web"></a>Évaluation de la stratégie dans Exchange Online, Outlook 2013 et versions ultérieures et Outlook sur le web

Lorsque vous créez une stratégie DLP qui inclut Exchange Online en tant qu’emplacement, la stratégie de synchronisées depuis le Office 365 Security &amp; centre de conformité à Exchange Online, puis à partir d’Exchange Online pour Outlook sur le web et Outlook 2013 et versions ultérieures.
  
Lorsqu’un message est en cours de composition dans Outlook, l’utilisateur peut voir les conseils de stratégie, comme le contenu en cours de création est évalué par rapport aux stratégies DLP. Et après l’envoi d’un message, elle est évaluée par rapport aux stratégies DLP dans le cadre normal du flux de messagerie, ainsi que les règles de transport Exchange et des stratégies DLP créées dans le centre d’administration Exchange (voir la section suivante pour plus d’informations). Les stratégies DLP analyse le message et les pièces jointes.
  
### <a name="policy-evaluation-in-the-office-2016-desktop-programs"></a>Évaluation des stratégies dans les programmes de bureau Office 2016

Excel 2016, 2016 PowerPoint et Word 2016 incluent la même fonctionnalité pour identifier les informations sensibles et appliquer des stratégies DLP en tant que SharePoint Online et OneDrive for Business. Ces programmes Office 2016 synchroniser leurs stratégies DLP directement à partir de la banque centrale stratégie et évaluent en permanence le contenu sur les stratégies DLP lorsque personnes travaillent avec des documents ouverts à partir d’un site qui est inclus dans une stratégie DLP.
  
Évaluation de la stratégie DLP dans 2016 Office est conçue ne pas pour avoir une incidence sur les performances des programmes ou la productivité des personnes travaillant sur le contenu. Si elles travaillez sur un document de grande taille ou ordinateur de l’utilisateur est occupé, il peut prendre quelques secondes pour un Conseil de stratégie s’affichent.
  
## <a name="permissions"></a>Autorisations

Les membres de votre équipe de conformité qui créeront des stratégies DLP besoin des autorisations pour la sécurité &amp; centre de conformité. Par défaut, votre administrateur client auront accès à cet emplacement et permettent aux règlements et autres personnes à accéder à la sécurité &amp; centre de conformité, sans octroyer toutes les autorisations d’un administrateur de client. Pour ce faire, il est recommandé que vous :
  
1. Créez un groupe dans Office 365 et ajoutez-y des responsables de la mise en conformité.
    
2. Créer un groupe de rôles dans la page **autorisations** de la sécurité &amp; centre de conformité. 
    
3. Ajoutez le groupe Office 365 au groupe de rôles.
    
Pour plus d’informations, voir [Give users access to the Office 365 Compliance Center](grant-access-to-the-security-and-compliance-center.md).
  
Ces autorisations sont requises uniquement pour créer et appliquer une stratégie DLP. L’application d’une stratégie ne nécessite pas d’accès au contenu.
  
## <a name="find-the-dlp-cmdlets"></a>Recherchez les cmdlets DLP

Pour utiliser la plupart des applets de commande pour la sécurité &amp; centre de conformité, vous devez :
  
1. [Se connecter au Centre de sécurité &amp; conformité Office 365 à l’aide de PowerShell à distance](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Utilisez une de ces [Office 365 sécurité &amp; centre de conformité des applets de commande](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
Toutefois, les rapports DLP doivent extraire des données dans Office 365, notamment Exchange Online. Pour cette raison, les applets de commande pour les rapports DLP sont disponibles dans Exchange Online Powershell--pas de sécurité &amp; Powershell du centre de conformité. Par conséquent, pour utiliser les applets de commande pour les rapports DLP, vous devez :
  
1. [Connexion à Exchange Online à l'aide de Remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Utilisez une de ces applets de commande pour les rapports DLP :
    
  - [Get-DlpDetectionsReport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
  - [Get-DlpDetailReport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    
## <a name="more-information"></a>Plus d’informations

- [Créer une stratégie DLP à partir d’un modèle](create-a-dlp-policy-from-a-template.md)
    
- [Envoi des notifications et affichage des conseils de stratégie pour les stratégies DLP](use-notifications-and-policy-tips.md)
    
- [Créer une stratégie DLP pour protéger les documents avec l’ICF ou d’autres propriétés](protect-documents-that-have-fci-or-other-properties.md)
    
- [Contenu des modèles de stratégie DLP](what-the-dlp-policy-templates-include.md)
    
- [Éléments recherchés par les types d’informations sensibles](what-the-sensitive-information-types-look-for.md)
    
- [Éléments recherchés par les fonctions DLP](what-the-dlp-functions-look-for.md)
    
- [Créer un type d’informations sensibles personnalisé](create-a-custom-sensitive-information-type.md)
    

