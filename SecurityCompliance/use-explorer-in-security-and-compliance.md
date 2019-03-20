---
title: Utiliser Threat Explorer dans le centre &amp; de sécurité conformité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/10/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Découvrez l'Explorateur (également appelé Explorateur de menaces) dans le &amp; Centre de sécurité conformité.
ms.openlocfilehash: 0c86792d8ed84b43b28bde31004dc95d2fa2b547
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693613"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>Utiliser Threat Explorer dans le centre &amp; de sécurité conformité

Si votre organisation dispose d' [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md)et que vous disposez des autorisations nécessaires, vous pouvez utiliser l'Explorateur de menaces pour identifier et analyser les menaces. Par exemple, vous pouvez identifier et supprimer un courrier électronique malveillant qui a été remis, ou consulter un programme malveillant qui a été intercepté par les fonctionnalités de sécurité d'Office 365. L'Explorateur de menaces (également appelé Explorateur) est un outil puissant quasiment en temps réel pour aider les équipes des opérations de sécurité à examiner et à répondre &amp; aux menaces dans le centre de sécurité conformité.
  
![Accéder à l'Explorateur \> de gestion des menaces](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Pour utiliser l'Explorateur, dans le &amp; Centre de sécurité conformité, accédez à l' **Explorateur**de **gestion** \> des menaces.

> [!IMPORTANT]
> Office 365 Threat Intelligence est désormais Office 365 Advanced Threat Protection Plan 2, ainsi que d'autres fonctionnalités de protection contre les menaces. Pour en savoir plus, consultez les [offres et tarifs office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection) et la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
      
## <a name="explorer-overview"></a>Vue d'ensemble de l'Explorateur

L'Explorateur affiche des informations sur les programmes malveillants suspects et les messages hameçons dans Office 365, ainsi que d'autres menaces et risques de sécurité pour votre organisation. Lorsque vous ouvrez l'Explorateur pour la première fois, l'affichage par défaut affiche les détections de programmes malveillants par courrier électronique pour les 7 derniers jours. Explorer peut également afficher les fonctionnalités de protection de la sécurité dans Office 365, notamment les [liens fiables](atp-safe-links.md) et [les pièces jointes fiables](atp-safe-attachments.md) , et peut être modifié pour afficher les données des 30 derniers jours. Si vous disposez d'une version d'évaluation de commun pour Office 365 Advanced Threat Protection Plan 2 ou Office 365 E5, vous ne verrez que les détections et les données de messagerie des 7 derniers jours.
  
![L'Explorateur affiche des informations sur les programmes malveillants principaux et les utilisateurs ciblés](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
Utilisez le menu Affichage pour modifier les informations affichées.
  
![Menu Affichage de l'Explorateur](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
L'Explorateur dispose de plusieurs fonctionnalités de filtrage et d'interrogation qui vous permettent d'explorer les détails, tels que les principaux utilisateurs ciblés, les principales familles de programmes malveillants, la technologie de détection et bien plus encore. Chaque type de rapport offre plusieurs façons d'afficher et d'explorer les données.

> [!IMPORTANT]
> N'utilisez pas de caractères génériques, tels qu'un astérisque (*) ou un point d'interrogation (?), avec l'Explorateur. Lorsque vous effectuez une recherche dans le champ Subject pour les messages électroniques, l'Explorateur effectue une correspondance partielle et génère des résultats similaires à une recherche par caractères génériques.

## <a name="email--malware"></a>Courrier \> malveillant de messagerie

Cet affichage montre les messages électroniques identifiés comme contenant des programmes malveillants.  

Afficher les informations dans le graphique par famille de programmes malveillants, domaine de l'expéditeur, adresse IP de l'expéditeur, état de protection (actions prises par les fonctionnalités et stratégies de protection contre les menaces dans Office 365) et technologie de détection (comment le programme malveillant a été détecté).  

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

Sous le graphique, affichez les détails des principales familles de programmes malveillants, des utilisateurs ciblés le plus ciblés et d'autres détails sur des messages spécifiques. 

## <a name="email--phish"></a>Courrier \> hameçon

Cet affichage montre les messages électroniques identifiés comme des tentatives de hameçonnage.  

Afficher les informations par domaine de l'expéditeur, adresse IP de l'expéditeur et état de protection (actions prises par vos stratégies et fonctionnalités de protection contre les menaces dans Office 365). 

![Afficher les données sur l'e-mail identifiées comme tentatives de hameçonnage](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

Sous le graphique, affichez plus de détails sur des messages spécifiques. 

## <a name="email--user-reported"></a>E-mail \> signalé par l'utilisateur

Cet affichage montre le courrier électronique que les utilisateurs ont signalés comme courrier indésirable, non légitime ou courrier électronique de hameçonnage.  

Afficher les informations par type de rapport (indique que l'utilisateur a déterminé qu'il s'agit d'un courrier indésirable, n'est pas un courrier indésirable ou un hameçonnage), et par raison du motif de remise (pourquoi les messages ont été envoyés à un emplacement spécifique, comme une stratégie de filtrage du courrier indésirable, une règle de flux de messagerie, une liste d'expéditeurs etc.).  

![Afficher des données sur les utilisateurs de messagerie signalés comme indésirables, non légitimes ou par hameçonnage](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d'objet, l'adresse IP de l'expéditeur, l'utilisateur qui a signalé le message comme courrier indésirable, légitime, ou hameçon, et bien plus encore. 

## <a name="email--all-mail"></a>Courrier \> électronique de tous les messages

Cette vue affiche une vue d'ensemble de l'activité de messagerie, y compris le courrier électronique identifié comme malveillant en raison d'un hameçonnage ou d'un programme malveillant, ainsi que tous les messages non malveillants (e-mail normal, courrier indésirable et courrier en nombre). 

> [!NOTE]
> Si vous obtenez une erreur indiquant un **trop grand nombre de données à afficher**, ajoutez un filtre et, si nécessaire, Affinez la plage de dates que vous visualisez. 

Pour appliquer un filtre, choisissez **expéditeur**, sélectionnez un élément dans la liste, puis cliquez sur le bouton Actualiser. Dans notre exemple, nous avons utilisé la **technologie de détection** en tant que filtre (plusieurs options sont disponibles). Afficher les informations de l'expéditeur, du domaine de l'expéditeur, des destinataires, de l'objet, du nom de fichier de la pièce jointe, de la famille de programmes malveillants, du statut de protection (actions effectuées par vos stratégies et fonctionnalités de protection contre les menaces dans Office 365), de la technologie de détection (comment le programme malveillant a été détecté) et plus d'. 

![Afficher les données sur les messages détectés par la technologie de détection](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

Sous le graphique, affichez plus de détails sur des messages électroniques spécifiques, tels que la ligne d'objet, le destinataire, l'expéditeur, l'État, etc. 

## <a name="content--malware"></a>Programme \> malveillant de contenu

Cet affichage montre les fichiers identifiés comme étant malveillants par Office 365 protection avancée contre les menaces dans SharePoint Online, OneDrive entreprise et Microsoft Teams.

Afficher des informations par famille de programmes malveillants, technologie de détection (comment le programme malveillant a été détecté) et charge de travail (OneDrive, SharePoint ou Teams). 

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

Sous le graphique, affichez plus de détails sur des fichiers spécifiques, tels que le nom de fichier de la pièce jointe, la charge de travail, la taille du fichier, la dernière personne qui a modifié le fichier, etc. 
  
## <a name="new-click-to-filter-capabilities"></a>(Nouveau!) Fonctionnalités de cliquer-filtrer

La nouveauté d'Explorer est la possibilité de cliquer pour filtrer. Lorsque vous cliquez sur un élément dans la légende, cet élément devient un filtre pour le rapport. Par exemple, supposons que nous examinons l'affichage programmes malveillants dans l'Explorateur:
  
![Accéder à l'Explorateur \> de gestion des menaces](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Si **** vous cliquez sur détonation de la protection avancée contre les menaces dans ce graphique, les résultats sont les suivants: 
  
![Explorateur filtré pour afficher uniquement les résultats de la déTonation ATO](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
Dans cet affichage, nous examinons à présent les données des fichiers qui ont été détonants par [les pièces jointEs approuvées par Office 365 ATP](atp-safe-attachments.md). Sous le graphique, nous pouvons voir des détails sur des messages électroniques spécifiques qui avaient des pièces jointes détectées par des pièces jointes sûres ATP.
  
![Détails spécifiques sur les messages électroniques avec des pièces jointes détectées](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
La sélection d'un ou de plusieurs éléments active le menu **actions** , qui offre plusieurs choix parmi lesquels choisir pour les éléments sélectionnés. 
  
![La sélection d'un élément active le menu actions](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
La possibilité de filtrer un clic et d'accéder à des détails spécifiques peut vous faire gagner du temps lors de l'enquête sur les menaces.
  
## <a name="how-do-i-get-explorer"></a>Comment puis-je obtenir Explorer?

L'Explorateur est inclus dans [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md). 

Vous devez disposer des autorisations appropriées, telles que celles accordées à un administrateur de sécurité ou à un lecteur de sécurité, afin d'afficher et d'utiliser l'Explorateur. Pour en savoir plus, consultez [la rubrique autorisations dans le &amp; Centre de sécurité conformité Office 365](permissions-in-the-security-and-compliance-center.md).
  
## <a name="related-topics"></a>Voir aussi

[Rapports et informations dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md)
  
[Rechercher et identifier les messages électroniques malveillants qui ont été remis (Office 365 Threat Invesitgation and Response)](investigate-malicious-email-that-was-delivered.md)
  
[Protection contre le courrier indésirable et les programmes malveillants dans Office 365](anti-spam-and-anti-malware-protection.md)
  

