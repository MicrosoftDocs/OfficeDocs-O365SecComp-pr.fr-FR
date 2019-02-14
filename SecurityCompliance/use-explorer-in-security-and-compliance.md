---
title: Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection: M365-security-compliance
description: En savoir plus sur l’Explorateur de solutions (également appelé Threat Explorer) dans la sécurité &amp; centre de conformité.
ms.openlocfilehash: 16f5b15c6993301f4f324f4b84c3b6e61f255e0f
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995115"
---
# <a name="use-explorer-in-the-security-amp-compliance-center"></a>Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité

Si votre organisation dispose [d’Informations sur les menaces Office 365](office-365-ti.md)et que vous disposez des autorisations nécessaires, vous pouvez utiliser l’Explorateur de solutions pour identifier et analyser les menaces. Par exemple, vous pouvez identifier et supprimer le courrier électronique malveillant qui a été remis ou voir des programmes malveillants qui a été détectée par les fonctionnalités de sécurité d’Office 365. Explorateur de solutions (également appelé Explorateur menace) est une puissante près de rapports en temps réel de la sécurité &amp; centre de conformité.
  
![Accédez à gestion de menace \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Pour utiliser l’Explorateur de solutions, dans la sécurité &amp; centre de conformité, accédez à la **Gestion des menaces** \> **Explorer**.

> [!IMPORTANT]
> À partir de février 2019 et présentant plusieurs mois suivant, sur les menaces Office 365 est devenu Office 365 Advanced Threat Protection Plan 2, avec les fonctionnalités de protection contre les menaces supplémentaires. Pour plus d’informations, voir [plans Office 365 avancée protection contre les menaces et les prix](https://products.office.com/exchange/advance-threat-protection) et [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
      
## <a name="explorer-overview"></a>Vue d’ensemble de l’Explorateur de solutions

Explorateur de solutions affiche des informations sur soupçonnés d’être anti-programme malveillant dans le message électronique fichiers dans Office 365, ainsi que les menaces de sécurité et autres risques à votre organisation. Lorsque vous ouvrez Explorateur de solutions, la vue par défaut affiche les détections de programmes malveillants d’antivirus pour les 7 derniers jours. Explorateur de solutions permettre également afficher sécurité fonctionnalités de protection dans Office 365, notamment des [Liens fiables](atp-safe-links.md) et les [Pièces jointes fiables](atp-safe-attachments.md) et peut être modifié pour afficher les données pour les 30 derniers jours.
  
![Explorateur affiche des informations sur les principaux programmes malveillants et ciblé aux utilisateurs](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
Pour modifier les informations affichées, utilisez le menu Affichage.
  
![Le menu Affichage de l’Explorateur de solutions](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
Explorateur de solutions a plusieurs filtrage et interrogation des fonctionnalités qui vous permettent d’examiner les détails, tels que haut ciblés utilisateurs et familles principaux programmes malveillants. Chaque type de rapport offre plusieurs manières d’afficher et Explorer les données.

> [!IMPORTANT]
> Ne pas utiliser de caractères génériques, comme un astérisque (*) ou un point d’interrogation ( ?), avec l’Explorateur de solutions. Lorsque vous recherchez dans le champ objet pour les messages électroniques, Explorer effectuera rendement et mise en correspondance des résultats partiels similaires à une recherche par caractères génériques.

## <a name="email--malware"></a>Messagerie \> programmes malveillants

Cet affichage montre les messages électroniques identifiés comme contenant des programmes malveillants.  

Afficher des informations dans le graphique à la famille de logiciels malveillants, domaine de l’expéditeur, IP de l’expéditeur, l’état de protection (actions effectuées par vos fonctionnalités de protection des menaces et les stratégies dans Office 365) et technologie de détection (comment le programme malveillant détecté).  

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

Sous le graphique, afficher les détails des familles principaux programmes malveillants, haut destiné aux utilisateurs et plus d’informations sur des messages spécifiques. 

## <a name="email--phish"></a>Messagerie \> hameçonnage

Cet affichage montre les messages électroniques identifiés comme les tentatives de hameçonnage.  

Afficher des informations à l’état de protection (actions effectuées par vos fonctionnalités de protection des menaces et les stratégies dans Office 365), IP de l’expéditeur et le domaine de l’expéditeur. 

![Afficher les données sur le courrier électronique identifié comme tentatives de hameçonnage](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

Sous le graphique, permet d’afficher plus d’informations sur des messages spécifiques. 

## <a name="email--user-reported"></a>Messagerie \> signalés par les utilisateurs

Cet affichage montre électroniques que les utilisateurs ont signalé comme indésirable, pas indésirable ou hameçonnage e-mail.  

Afficher les informations par type de rapport (détermination de l’utilisateur que le courrier électronique a été indésirable, pas indésirable ou hameçonnage) et le motif de livraison (raisons pourquoi messagerie est passée à un emplacement spécifique, par exemple une stratégie de filtrage du courrier indésirable, une règle de flux de messagerie, une liste des expéditeurs bloqués, une liste des expéditeurs, etc.).  

![Afficher les données sur les utilisateurs de messagerie signalé comme indésirable, pas indésirable ou hameçonnage](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

Sous le graphique, permet d’afficher plus d’informations sur les e-mails spécifiques, telles que la ligne objet, adresse IP de l’expéditeur, l’utilisateur qui a signalé le message comme indésirable courrier indésirable, ou hameçonnage et non plus. 

## <a name="email--all-mail"></a>Messagerie \> tous les messages

Cet affichage présente une vue de toutes les d’activité de courrier électronique, y compris courrier identifié comme malveillants due à l’hameçonnage ou des programmes malveillants, ainsi que tous les messages non malveillantes (messagerie normal, spam et courrier indésirable). 

> [!NOTE]
> Si vous obtenez une erreur indiquant **trop grande quantité de données afficher**, ajouter un filtre et, si nécessaire, limitez la plage de dates que vous visualisez. 

Pour appliquer un filtre, choisissez **expéditeur**, sélectionnez un élément dans la liste, puis cliquez sur le bouton d’actualisation. Dans notre exemple, nous avons utilisé la **technologie de détection** comme filtre (il existe plusieurs options disponibles). Afficher des informations à l’expéditeur, domaine de l’expéditeur, destinataires, subject, nom de fichier de pièce jointe, famille de logiciels malveillants, l’état de protection (actions effectuées par vos fonctionnalités de protection des menaces et les stratégies dans Office 365), technologie de détection (comment le programme malveillant détecté), et plus. 

![Afficher les données sur l’e-mail détecté par la technologie de détection](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

Sous le graphique, permet d’afficher plus d’informations sur les messages de messagerie spécifiques, telles que la ligne objet, destinataire, expéditeur, statut et ainsi de suite. 

## <a name="content--malware"></a>Contenu \> programmes malveillants

Cet affichage indique les fichiers qui ont été identifiés comme malveillants dans SharePoint Online, OneDrive pour les entreprises et Teams Microsoft.

Afficher les informations par la technologie de détection famille, de programmes malveillants (comment le programme malveillant détecté) et la charge de travail (SharePoint, OneDrive ou équipes). 

![Afficher les données sur les programmes malveillants détectés](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

Sous le graphique, permet d’afficher plus d’informations sur les fichiers spécifiques, telles que le nom de fichier de pièce jointe, la charge de travail, la taille de fichier qui a modifié le fichier et bien plus encore. 
  
## <a name="new-click-to-filter-capabilities"></a>(Nouveau) ! Cliquez sur-filtre de fonctionnalités

Nouveau pour Explorer est la possibilité de cliquer sur pour filtrer. Liaison tardive 2018 mai, lorsque vous cliquez sur un élément dans la légende, à partir de cet élément devienne un filtre pour le rapport. Par exemple, supposons que nous cherchons à l’affichage de programmes malveillants dans l’Explorateur de solutions :
  
![Accédez à gestion de menace \> Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
En cliquant sur **DAV détonation** dans les résultats de ce graphique dans un affichage semblable à celle-ci : 
  
![Explorer filtré pour afficher uniquement les résultats de détonation assembler](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
Dans cet affichage, nous recherchons maintenant au niveau des données pour les fichiers qui ont été detonated par [Office 365 DAV approuvés en pièce jointe](atp-safe-attachments.md). Sous le graphique, nous pouvons voir plus d’informations sur les messages électroniques spécifiques qui avaient des pièces jointes qui ont été détectés par les pièces jointes sûres DAV.
  
![Détails spécifiques sur les messages électroniques contenant des pièces jointes détectés](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
Sélection d’un ou plusieurs éléments Active le menu **Actions** , ce qui offre plusieurs options parmi lesquelles choisir pour les éléments sélectionnés. 
  
![Sélection d’un élément Active le menu Actions](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
La possibilité de filtrer en un clic et accédez à des détails spécifiques permettre enregistrer beaucoup de temps dans l’analyse des menaces.
  
## <a name="how-do-i-get-explorer"></a>Comment obtenir de l’Explorateur de solutions ?

Explorer est inclus dans [Office 365 menaces](office-365-ti.md). 

Vous devez disposer des autorisations appropriées, telles que celles accordées à un administrateur de sécurité ou un lecteur de sécurité, afin d’afficher et utiliser l’Explorateur de solutions. Pour plus d’informations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).
  
## <a name="related-topics"></a>Voir aussi

[Rapports et vues d’ensemble de sécurité Office 365 &amp; centre de conformité](reports-and-insights-in-security-and-compliance.md)
  
[Rechercher et vérifier le courrier électronique malveillant qui a été remis (Office 365 Threat Intelligence)](investigate-malicious-email-that-was-delivered.md)
  
[Protection contre le courrier indésirable et les programmes malveillants dans Office 365](anti-spam-and-anti-malware-protection.md)
  

