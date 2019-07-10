---
title: Afficher les rapports de sécurité de messagerie &amp; dans le centre de sécurité conformité
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 05/21/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection:
- M365-security-compliance
description: Découvrez comment rechercher et utiliser des rapports de sécurité de messagerie pour votre organisation. Les rapports de sécurité de messagerie sont disponibles &amp; dans le centre de sécurité conformité.
ms.openlocfilehash: 17a8114ec1d4af9a665c235e38461f281f4fe83f
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598550"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a>Afficher les rapports de sécurité de messagerie &amp; dans le centre de sécurité conformité

Un grand nombre de rapports sont disponibles dans [le &amp; Centre de sécurité conformité](https://protection.office.com) pour vous aider à découvrir comment les fonctionnalités de sécurité de messagerie, telles que les fonctionnalités de blocage du courrier indésirable, de programmes malveillants et de chiffrement dans Office 365 protègent votre organisation. Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez afficher ces rapports dans le centre &amp; de sécurité conformité en accédant au **tableau de bord** **rapports** \> .
  
![Tableau de bord où se trouve le fonctionnement de la protection avancée contre les menaces](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Vos rapports de sécurité de messagerie incluent les éléments suivants:
- [Rapport](#encryption-report) de chiffrement (Nouveau!)
- [Rapport d’état de protection contre les menaces](#threat-protection-status-report) 
- [Rapport de détection des programmes malveillants](#malware-detections-report) 
- [Premier rapport de programmes malveillants](#top-malware-report)
- [Rapport des expéditeurs et des destinataires principaux](#top-senders-and-recipients-report)
- [Rapport des détections d’usurpation](#spoof-detections-report)
- [Rapport de détections de courrier indésirable](#spam-detections-report)
- [Rapport de courrier électronique envoyé et reçu](#sent-and-received-email-report)
- [Rapport sur les messages signalés par l’utilisateur](#user-reported-messages-report)
    
## <a name="encryption-report"></a>Rapport de chiffrement

(**Nouveau!**) Le **rapport** de chiffrement affiche des informations sur les messages électroniques qui ont été chiffrés, via les stratégies de votre organisation ou par le biais de contrôles utilisateur final. L’équipe de sécurité de votre organisation peut utiliser les informations contenues dans ce rapport pour identifier des modèles et appliquer ou ajuster de façon proactive des stratégies pour les messages électroniques sensibles.

Pour afficher ce rapport, accédez au **rapport**de chiffrement du **tableau de bord** \> des **rapports** \> dans le centre de sécurité & conformité.

![Rapport de chiffrement](media/encryptionreport-defaultview.png) 

Lors de la première ouverture du rapport, vous verrez des données sur les méthodes de chiffrement utilisées sur les messages électroniques pour les sept (7) derniers jours. Vous pouvez modifier la plage de dates et les détails affichés dans le rapport en cliquant sur **filtres** dans le coin supérieur droit de l’écran.

![Filtres du rapport de chiffrement](media/encryptionreport-filters.png)   

Vous pouvez également utiliser le menu dépanner **par** pour afficher les données en utilisant un modèle de chiffrement (ou une méthode).

![Méthode de chiffrement ou modèle](media/encryptionreport-breakdownby.png)

De plus, vous pouvez utiliser le menu **afficher les données par** pour afficher le nombre de messages chiffrés sur les cinq domaines destinataires.

![Affichage du rapport de chiffrement des données par menu](media/encryptionreport-viewdataby.png)

Avec la flexibilité du nouveau rapport de chiffrement, vous pouvez afficher les tendances et prendre les mesures appropriées. Par exemple, si vous voyez un grand nombre de messages électroniques chiffrés par les utilisateurs, vous souhaiterez peut-être ajouter une stratégie de chiffrement pour automatiser le chiffrement pour certains cas d’utilisation. (Pour obtenir de l’aide, reportez-vous à la rubrique [définition de règles de flux de messagerie pour chiffrer les messages électroniques dans Office 365](define-mail-flow-rules-to-encrypt-email.md).) En guise d’exemple, si un certain nombre de modèles de chiffrement sont disponibles mais que personne ne les utilise, vous pouvez découvrir si les utilisateurs ont besoin d’une formation pour cette fonctionnalité. 

Ce rapport permet à l’équipe de sécurité et de conformité de votre organisation de surveiller le mode d’utilisation du chiffrement des messages et d’indiquer si d’autres actions sont nécessaires. Pour en savoir plus sur le chiffrement, consultez la rubrique [chiffrement des messages électroniques dans Office 365](email-encryption.md).

## <a name="threat-protection-status-report"></a>Rapport d’état de protection contre les menaces

Le rapport d' **État de protection contre les menaces** est un rapport intelligent qui affiche des messages malveillants détectés et bloqués par Exchange Online Protection. Ce rapport est utile pour afficher le courrier électronique identifié comme un programme malveillant ou une tentative de hameçonnage dans le temps (jusqu’à 90 jours), et permet aux administrateurs de sécurité d’identifier les tendances ou de déterminer si les stratégies ont besoin d’être ajustées.

> [!NOTE]
> Un rapport d’état de protection contre les menaces est disponible pour les clients qui ont [Office 365 ATP](office-365-atp.md) ou [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP); Toutefois, les informations affichées dans le rapport d’état de protection contre les menaces pour les clients ATP contiennent probablement des données différentes de celles que peuvent afficher les clients EOP. Par exemple, les clients EOP peuvent afficher des informations sur les programmes malveillants détectés dans les messages électroniques, mais pas les informations sur les [fichiers malveillants détectés dans SharePoint Online, OneDrive ou Microsoft teams](atp-for-spo-odb-and-teams.md), une capacité spécifique à la protection avancée contre les menaces. ([En savoir plus sur les rapports ATP](view-reports-for-atp.md).)
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à **rapports** \> **tableau de bord** \> de **protection contre les menaces**.
  
![Rapport d’état de protection contre les menaces](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
Lorsque vous ouvrez pour la première fois le rapport d’état de protection contre les menaces, le rapport affiche les données des sept derniers jours par défaut; Toutefois, vous pouvez cliquer sur **filtres** et modifier la plage de dates pour un maximum de 90 jours de détail. (Si vous utilisez un abonnement d’évaluation, vous pouvez être limité à 30 jours de données.)

Ce rapport est utile pour l’affichage de l’efficacité et de l’impact des [fonctionnalités Exchange Online Protection](eop/eop-features.md)de votre organisation et pour des tendances à long terme. 
  
![Filtres de rapport d’état de protection contre les menaces](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
Vous pouvez également choisir d’afficher les données pour les e-mails identifiés comme malveillants, les e-mails identifiés comme des tentatives de hameçonnage ou par e-mail identifiés comme contenant des programmes malveillants.
  
![Options d’affichage des rapports d’état de protection contre les menaces](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a>Rapport de détection des programmes malveillants

Le rapport détections de **programmes malveillants** indique le nombre de messages entrants et sortants détectés comme contenant des programmes malveillants pour votre organisation. 
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à **rapports** \> **tableau de bord** \> des **programmes malveillants**.
  
![Exemple de rapport de détection de programmes malveillants](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
À l’instar d’autres rapports, comme le [rapport d’état de protection contre les menaces](#threat-protection-status-report), le rapport affiche les données des sept derniers jours par défaut. Toutefois, vous pouvez choisir des **filtres** pour modifier la plage de dates. 
  
## <a name="top-malware-report"></a>Premier rapport de programmes malveillants

Le rapport des **principaux programmes malveillants** indique les différents types de programmes malveillants détectés par [Exchange Online](eop/eop-features.md). 
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à **rapports** \> **tableau de bord** \> des **principaux programmes malveillants**.
  
![Programmes malveillants SCC-EOP principaux](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
Lorsque vous placez le curseur de la souris sur un coin du graphique en secteurs, vous pouvez voir le nom d’un type de programme malveillant et le nombre de messages détectés comme présentant ce programme malveillant.
  
Cliquez (ou appuyez) sur le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, dans laquelle vous pouvez obtenir une vue plus détaillée du rapport.
  
![Ce rapport présente les principaux programmes malveillants détectés pour votre organisation.](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
Sous le graphique, vous verrez une liste de programmes malveillants détectés et le nombre de messages détectés comme présentant ce programme malveillant.
  
## <a name="top-senders-and-recipients-report"></a>Rapport des expéditeurs et des destinataires principaux

Le rapport des **expéditeurs et des destinataires principaux** est un graphique en secteurs illustrant les principaux expéditeurs de vos courriers électroniques. 
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à **rapports** \> **tableau de bord** \> **des expéditeurs et destinataires principaux**.
  
![Pour afficher ce rapport, dans le centre &amp; de sécurité conformité, accédez à \> rapports \> tableau de bord des expéditeurs et destinataires principaux](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
Lorsque vous placez le curseur de la souris sur un coin du graphique en secteurs, vous pouvez voir le nombre de messages envoyés ou reçus.
  
Cliquez (ou appuyez) sur le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, dans laquelle vous pouvez obtenir une vue plus détaillée du rapport.
  
Utilisez la liste **afficher les données pour** déterminer si vous souhaitez afficher les données des destinataires, des expéditeurs, des destinataires de courrier indésirable et des programmes malveillants les plus fréquents. Vous pouvez également consulter la personne qui a reçu un programme malveillant détecté par [Exchange Online Protection](eop/exchange-online-protection-overview.md). 
  
![Utiliser la liste afficher les données pour afficher des informations spécifiques](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
Sous le graphique, vous verrez les expéditeurs et destinataires de courriers les plus fréquents, ainsi que le nombre de messages envoyés ou reçus pendant la période donnée.
  
## <a name="spoof-detections-report"></a>Rapport des détections d’usurpation

Le rapport des détections d' **usurpation** indique le nombre de messages d’usurpation d’identité détectés et ceux qui ont été considérés comme «corrects» (courrier infalsifiable pour des raisons professionnelles légitimes). 
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à rapports **tableau de bord** \> **** des **rapports** \> .
  
![Dans le centre &amp; de sécurité conformité, accédez à \> rapports \> tableau de bord de courrier frauduleux](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
Lorsque vous placez le curseur de la souris sur un jour dans le graphique, vous pouvez voir le nombre de messages d’usurpation d’adresse.
  
Cliquez (ou appuyez) sur le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, dans laquelle vous pouvez obtenir une vue plus détaillée du rapport. Pour en savoir plus sur la protection contre les falsifications, consultez la rubrique [anti-spoofing protection in Office 365](anti-spoofing-protection.md).
  
## <a name="spam-detections-report"></a>Rapport de détections de courrier indésirable

Le rapport détections du **courrier** indésirable affiche tout le contenu du courrier indésirable bloqué par Exchange Online. 
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à **rapports** \> **tableau de bord** \> de **courrier**indésirable.
  
![Pour afficher ce rapport, dans le centre &amp; de sécurité conformité, accédez à \> rapports \> tableau de bord de courriers indésirables EOP](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
Lorsque vous placez le curseur de la souris sur un jour du graphique, vous pouvez voir le nombre d’éléments qui ont été bloqués cette journée, ainsi que la catégorie de ces éléments. Par exemple, vous pouvez voir le nombre de messages indésirables filtrés et le nombre d’éléments provenant d’une adresse IP (Internet Protocol) bloquée.
  
Cliquez (ou appuyez) sur le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, dans laquelle vous pouvez obtenir une vue plus détaillée du rapport.
  
![Le rapport des détections de courrier indésirable indique le nombre de messages indésirables bloqués ou filtrés](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
Sous le graphique, vous verrez une liste d’éléments de courrier indésirable détectés. Sélectionnez un élément pour afficher des informations supplémentaires, par exemple si l’élément de courrier indésirable a été entrant ou sortant, son ID de message et son destinataire. Pour en savoir plus sur la protection contre le courrier indésirable, consultez la rubrique [Office 365 e-mail anti-spam protection](anti-spam-protection.md).
  
## <a name="sent-and-received-email-report"></a>Rapport de courrier électronique envoyé et reçu

Le rapport de **courrier électronique envoyé et reçu** est un rapport intelligent qui affiche des informations sur les messages entrants et sortants, notamment les détections de courrier indésirable, les programmes malveillants et la messagerie électronique identifiés comme étant «en qualité». 
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), accédez à **rapports** \> **tableau de bord** \> des **messages envoyés et reçus**.
  
![Pour afficher ce rapport, dans le centre &amp; de sécurité conformité, accédez à \> rapports \> tableau de bord des messages envoyés et reçus](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
Lorsque vous placez le curseur de la souris sur un jour dans le graphique, vous pouvez voir le nombre de messages qui ont été reçus et la façon dont ces messages sont catégorisés. Par exemple, vous pouvez voir le nombre de messages détectés comme contenant des programmes malveillants et le nombre de messages identifiés comme courrier indésirable.
  
Cliquez (ou appuyez) sur le rapport pour l’ouvrir dans une nouvelle fenêtre de navigateur, dans laquelle vous pouvez obtenir une vue plus détaillée du rapport.
  
Vous pouvez utiliser la liste **décomposer par** pour afficher les informations par type ou par direction (entrante et sortante). 
  
![Utiliser la liste décomposer par pour afficher les informations par type ou sens](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
Sous le graphique, vous verrez une liste de catégories de courrier, telle que **GoodMail**, **SpamContentFiltered**, etc. Sélectionnez une catégorie pour afficher des informations supplémentaires, telles que des actions qui ont été effectuées pour les programmes malveillants, et si le courrier électronique a été entrant ou sortant.
  
![Ce rapport vous indique le blocage des programmes malveillants, le courrier indésirable et les autres détections de messages.](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)

Pour en savoir plus sur l’intelligence de messagerie, consultez la rubrique Assistant [flux de messagerie dans Office 365](mail-flow-intelligence-in-office-365.md).
  
## <a name="user-reported-messages-report"></a>Rapport sur les messages signalés par l’utilisateur

Le rapport **messages signalés** par l’utilisateur affiche des informations sur les messages électroniques que les utilisateurs ont signalés comme courriers indésirables, tentatives de hameçonnage ou courrier électronique à l’aide du [complément de message de rapport](enable-the-report-message-add-in.md).
  
Des détails sont disponibles pour chaque message, notamment la raison de remise, une exception de stratégie de courrier indésirable ou une règle de flux de messagerie configurée pour votre organisation. Pour afficher les détails, sélectionnez un élément dans la liste rapports utilisateur, puis affichez les informations sous les onglets **Résumé** et **Détails** . 
  
![Le rapport messages signalés par l’utilisateur affiche les messages marqués comme courriers indésirables, non légitimes ou par tentatives de hameçonnage.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
Pour afficher ce rapport, dans le [Centre &amp; de sécurité conformité](https://protection.office.com), effectuez l’une des opérations suivantes:
  
- Accédez au **** \> **tableau de bord** \> gestion **des menaces-messages signalés par l’utilisateur**.
    
- Accédez à **** \> **examen** \> **des menaces-messages signalés par l’utilisateur**.
    
![Dans le centre &amp; de sécurité conformité, choisissez gestion \> des \> menaces-vérifier les messages signalés par l’utilisateur](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> Pour que le rapport des messages signalés par l’utilisateur fonctionne correctement, la **journalisation d’audit doit être activée** pour votre environnement Office 365. Cette opération est généralement réalisée par une personne disposant du rôle journaux d’audit dans Exchange Online. Pour plus d’informations, voir [activer ou désactiver la recherche dans le journal d’audit Office 365](turn-audit-log-search-on-or-off.md). 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a>Quelles sont les autorisations nécessaires pour afficher ces rapports?

Pour afficher et utiliser les rapports décrits dans cet article, **vous devez disposer d’un rôle approprié pour le centre de sécurité &amp; et le centre d’administration Exchange**.

- Pour le centre &amp; de sécurité conformité, vous devez disposer de l’un des rôles suivants:
    - Gestion de l’organisation
    - Administrateur de la sécurité (qui peut être affecté dans le centre d’administration Azure[https://aad.portal.azure.com](https://aad.portal.azure.com)Active Directory ()
    - Lecteur de sécurité

- Pour Exchange Online, vous devez disposer de l’un des rôles suivants, qui est affecté dans le centre[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)d’administration Exchange () ou avec des applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Gestion de l’organisation
    - Gestion de l’organisation en affichage seul
    - Rôle Destinataires en affichage uniquement
    - Gestion de la conformité

Pour en savoir plus, consultez les ressources suivantes:

- [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Autorisations des fonctionnalités dans Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a>Qu’en est-il si les rapports n’affichent pas de données?

Si vous ne voyez pas de données dans vos rapports, vérifiez que vos stratégies sont correctement configurées. Pour en savoir plus, consultez la rubrique Protégez-vous [contre les menaces dans Office 365](protect-against-threats.md).
  
## <a name="related-topics"></a>Sujets associés

[Protection contre le courrier indésirable pour Office 365](anti-spam-protection.md)
  
[Rapports et informations dans le centre de sécurité &amp; conformité Office 365](reports-and-insights-in-security-and-compliance.md)
  
[Créer une planification pour un rapport dans le centre &amp; de sécurité conformité](create-a-schedule-for-a-report.md)
  
[Configurer et télécharger un rapport personnalisé dans le centre de &amp; sécurité conformité](set-up-and-download-a-custom-report.md)
  

