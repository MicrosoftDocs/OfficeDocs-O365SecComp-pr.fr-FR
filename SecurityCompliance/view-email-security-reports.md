---
title: Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/07/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
description: Découvrez comment trouver et utiliser les rapports de sécurité de messagerie pour votre organisation avec Office 365 pour entreprises. Rapports de sécurité de messagerie sont disponibles dans la sécurité &amp; centre de conformité.
ms.openlocfilehash: 670317707c5695161f23615fb87fe93258e8d95b
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749328"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a>Afficher les rapports de sécurité de messagerie de la sécurité &amp; centre de conformité

Une série de rapports de sécurité de messagerie sont disponibles dans le [sécurité &amp; centre de conformité](https://security.microsoft.com) pour vous aider à voir la façon dont des fonctionnalités anti-spam et contre les programmes malveillants dans Office 365 sont protège votre organisation. Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez afficher ces rapports dans la sécurité &amp; centre de conformité en accédant aux **rapports** \> **tableau de bord**.
  
![La sécurité &amp; tableau de bord de centre de conformité peut vous aider à voir où travaille protection contre les menaces avancées](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Vos rapports de sécurité de messagerie sont les suivantes :
  
- [Rapport d’état de Protection de menace](view-email-security-reports.md#tps) 
    
- [Rapport des détections de programmes malveillants](view-email-security-reports.md#maldet)
    
- [Rapport de programmes malveillants supérieure](#top-malware-report)
    
- [État des expéditeurs et destinataires principaux](view-email-security-reports.md#topsenders)
    
- [Rapport de messagerie usurpation d’identité](#spoof-mail-report)
    
- [Rapport des détections de courrier indésirable](#spam-detections-report)
    
- [Rapport envoyés et reçus par courrier électronique](view-email-security-reports.md#sentreceivedemail)
    
- [Rapport de messages signalés par les utilisateurs](view-email-security-reports.md#userreported) (nouveau) ! 
    
## <a name="threat-protection-status-report"></a>Rapport d’état de Protection de menace

Nouveau rapport **d’État de Protection de menace** est un rapport dynamique qui affiche la messagerie qui a été détecté et bloqué par Exchange Online Protection. Ce rapport affiche des informations sur le courrier identifié comme une tentative de hameçonnage ou de programmes malveillants. 

> [!NOTE]
> Un rapport d’état de Protection de menace est disponible pour les clients qui ont des [Office 365 DAV](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP) ; Toutefois, les informations qui s’affiche dans le rapport d’état de Protection des menaces pour les clients disposant contiendra probablement que les clients EOP peuvent afficher des données différentes. Par exemple, clients EOP peuvent afficher plus d’informations sur les logiciels malveillants détectés dans le courrier électronique, mais pas plus d’informations sur [les fichiers malveillants détecté dans SharePoint Online, OneDrive ou les équipes Microsoft](atp-for-spo-odb-and-teams.md), une fonctionnalité spécifique DAV. ([En savoir plus sur les rapports DAV](view-reports-for-atp.md)).
  
Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **État de Protection de menace**.
  
![Rapport d’état de Protection de menace](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
Lorsque vous ouvrez le rapport d’état de Protection de menace, le rapport montre les données pour les sept derniers jours par défaut ; Vous pouvez toutefois, cliquez sur **filtres** et modifier la plage de dates pendant 90 jours de détail. Ce rapport est utile pour l’affichage de l’efficacité et l’impact des fonctionnalités d’Exchange Online Protection de votre organisation et pour l’analyse des tendances à long terme. 
  
![Filtres du rapport d’état de la Protection des menaces](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
Vous pouvez également choisir si, pour afficher les données pour le courrier électronique identifié comme malveillants, e-mail identifié comme un hameçonnage tente ou courrier identifié comme contenant des programmes malveillants.
  
![Options d’affichage du rapport état de la Protection des menaces](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a>Rapport des détections de programmes malveillants

Le rapport des **Détections de programmes malveillants** indique le nombre de messages entrant et sortant ont été détecté comme contenant des programmes malveillants de votre organisation. 
  
Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **Détections de programmes malveillants**.
  
![Exemple de rapport Détections de programmes malveillants](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
Similaire à d’autres rapports, comme le rapport d’état de Protection de menace, le rapport affiche données pour les sept derniers jours par défaut. Toutefois, vous pouvez choisir de **filtres** pour modifier la plage de dates. 
  
## <a name="top-malware-report"></a>Rapport de programmes malveillants supérieure

Le rapport de **Programmes malveillants haut** montre les différents types de programme malveillant détecté par Exchange Online. 
  
Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **Malveillant haut**.
  
![SCC - EOP principaux programmes malveillants](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
Lorsque vous placez sur un coin du graphique en secteurs, vous pouvez voir le nom d’un type de programmes malveillants et le nombre de messages a été détecté comme ayant que les logiciels malveillants.
  
Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.
  
![Ce rapport présente les principaux programmes malveillants détectés pour votre organisation](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
Sous le graphique, vous verrez une liste de programmes malveillants détectés et le nombre de messages a été détecté comme ayant que les logiciels malveillants.
  
## <a name="top-senders-and-recipients-report"></a>État des expéditeurs et destinataires principaux

Le rapport **principaux expéditeurs et destinataires** est un graphique en secteurs vos principaux expéditeurs d’e-mails. 
  
Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **principaux expéditeurs et destinataires**.
  
![Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux rapports \> tableau de bord \> principaux expéditeurs et destinataires](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
Lorsque vous placez sur un coin du graphique en secteurs, vous pouvez voir un nombre de messages envoyés ou reçus.
  
Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.
  
Utilisez la liste **Afficher les données de** choisir d’afficher les données pour émetteurs, destinataires, destinataires du courrier indésirable et destinataires des programmes malveillants. Vous pouvez également voir qui a reçu le programme malveillant détecté par la protection contre les menaces avancées. 
  
![Utilisez la liste Afficher les données pour afficher des informations spécifiques](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
Sous le graphique, vous verrez qui les expéditeurs de courriers supérieure ou destinataires ont été, ainsi que d’un nombre de messages envoyés ou reçus pour la période de temps donnée.
  
## <a name="spoof-mail-report"></a>Rapport de messagerie usurpation d’identité

Le rapport de **Messagerie de l’usurpation d’identité** indique le nombre de messages messagerie usurpation d’identité ont été détecté et parmi ceux-ci, celles qui ont été considérés comme étant « bon » (mail usurpation d’identité pour des raisons professionnelles légitimes). 
  
Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **Messagerie usurpation d’identité**.
  
![Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux rapports \> tableau de bord \> messagerie usurpation d’identité](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
Lorsque vous placez sur un jour dans le graphique, vous pouvez voir le nombre de messages messagerie usurpation d’identité fournie par le biais de.
  
Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.
  
## <a name="spam-detections-report"></a>Rapport des détections de courrier indésirable

Le rapport de **Détections de courrier indésirable** présente tout le contenu du courrier indésirable bloqué par Exchange Online. 
  
Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **Détections de courrier indésirable**.
  
![Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux rapports \> tableau de bord \> détections de courrier indésirable d’EOP](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
Lorsque vous placez sur un jour dans le graphique, vous pouvez voir le nombre d’éléments ont été bloqué dans la journée, ainsi que la manière dont les éléments sont classés. Par exemple, vous pouvez voir le nombre de messages de courrier indésirable ont été filtré, et le nombre d’éléments provenant d’une adresse IP (Internet Protocol) bloqués.
  
Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.
  
![Le rapport des détections de courrier indésirable indique le nombre de messages de courrier indésirable ont été bloqué ou filtré](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
Sous le graphique, vous verrez une liste d’éléments de courrier indésirable détectés. Sélectionnez un élément pour afficher des informations supplémentaires, telles que si l’élément de courrier indésirable a été entrants ou sortants, son ID de message et son destinataire.
  
## <a name="sent-and-received-email-report"></a>Rapport envoyés et reçus par courrier électronique

Le rapport **envoyé et le courrier entrant** est un rapport dynamique qui affiche des informations sur les e-mails entrants et sortants, y compris les détections de courrier indésirable, les logiciels malveillants et e-mail identifié comme « bon ». 
  
Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), accédez aux **rapports** \> **tableau de bord** \> **envoyés et le courrier entrant**.
  
![Pour afficher ce rapport, de la sécurité &amp; centre de conformité, accédez aux rapports \> tableau de bord \> envoyés et le courrier entrant](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
Lorsque vous placez sur un jour dans le graphique, vous pouvez voir le nombre de messages est arrivé, et comment ces messages sont classés. Par exemple, vous pouvez voir le nombre de messages qui ont été détecté comme contenant des programmes malveillants, et combien ont été identifiés comme courrier indésirable.
  
Cliquez (ou appuyez) le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, où vous pouvez obtenir une vue plus détaillée de l’état.
  
Vous pouvez utiliser la liste **décomposer par** pour afficher les informations par type ou par le sens (entrant et sortant). 
  
![Utilisez la liste arrêt vers le bas par pour afficher les informations par type ou la direction](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
Sous le graphique, vous verrez une liste de catégories de messagerie, tels que **GoodMail**, **SpamContentFiltered**et ainsi de suite. Sélectionnez une catégorie pour afficher des informations supplémentaires, telles que les actions qui ont été prises pour les logiciels malveillants et si la messagerie est entrant ou sortant.
  
![Ce rapport vous informe des autres détections de message, anti-spam et contre les programmes malveillants](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report-new"></a>Rapport de messages signalés par les utilisateurs (nouveau) !

Le rapport **messages signalés par les utilisateurs** présente des informations sur les messages électroniques que les utilisateurs ont signalé comme indésirable, les tentatives de hameçonnage ou bon courrier électronique à l’aide [complément de Message de rapport](enable-the-report-message-add-in.md).
  
Plus d’informations sont disponibles pour chaque message, y compris le motif de livraison, une telle exception de stratégie de courrier indésirable ou règle de flux de messagerie configurées pour votre organisation. Pour afficher plus d’informations, sélectionnez un élément dans la liste des rapports à l’utilisateur, puis afficher les informations sur les onglets **Résumé** et les **Détails** . 
  
![Le rapport Messages User-Reported indique aux utilisateurs de messages marquées comme indésirable, pas indésirable ou hameçonnage tentatives.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
Pour afficher ce rapport, dans le [sécurité &amp; centre de conformité](https://security.microsoft.com), effectuez l’une des opérations suivantes :
  
- Accédez à **gestion de menace** \> **tableau de bord** \> **messages signalés par les utilisateurs**.
    
- Accédez à **gestion de menace** \> **révision** \> **messages signalés par les utilisateurs**.
    
![Dans la sécurité &amp; centre de conformité, cliquez sur gestion des menaces \> révision \> messages indiqué par utilisateur](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> Dans la commande pour le rapport messages signalés par les utilisateurs de fonctionner correctement, **l’enregistrement d’audit doit être activée** pour votre environnement Office 365. Cela s’effectue généralement par toute personne ayant le rôle journaux d’Audit affecté dans Exchange Online. Pour plus d’informations, voir [recherche des journaux d’audit d’activer Office 365 activé ou désactivé](turn-audit-log-search-on-or-off.md). 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a>Les autorisations requises pour afficher ces rapports ?

Pour pouvoir afficher et utiliser les rapports décrits dans cet article, **vous devez disposer d’un rôle approprié est affecté de la sécurité &amp; centre de conformité et le centre d’administration Exchange**.

- Pour la sécurité &amp; centre de conformité, vous devez disposer d’un des rôles suivants est attribué :
    - Gestion de l’organisation
    - Administrateur de sécurité
    - Lecteur de sécurité

- Pour Exchange Online, vous devez disposer d’un des rôles suivants est attribué :
    - Gestion de l’organisation
    - Gestion de l’organisation en affichage seul
    - Rôle Destinataires en affichage uniquement
    - Gestion de la conformité

Pour plus d’informations, voir les ressources suivantes :

- [Autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md)

- [Autorisations des fonctionnalités dans Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a>Que se passe-t-il si les rapports ne sont pas affichant les données ?

Si vous ne voyez pas les données dans vos rapports, vérifiez que vos stratégies sont correctement configurés. Pour plus d’informations, consultez la rubrique [protection contre le courrier indésirable et anti-programme malveillant dans Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Voir aussi

[Protection contre le courrier indésirable pour Office 365](anti-spam-protection.md)
  
[Rapports et vues d’ensemble de sécurité Office 365 &amp; centre de conformité](reports-and-insights-in-security-and-compliance.md)
  
[Créer une planification pour un état de la sécurité &amp; centre de conformité](create-a-schedule-for-a-report.md)
  
[Configurer et télécharger un rapport personnalisé dans la sécurité &amp; centre de conformité](set-up-and-download-a-custom-report.md)
  

