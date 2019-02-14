---
title: Office 365 DAV fiable en pièce jointe
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/08/2019
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
description: La fonctionnalité pièces jointes sûres assure une vérification clic du temps de pièces jointes. Les pièces jointes fiables à utiliser pour protéger votre organisation contre les personnes malveillantes fichiers envoyer ou recevoir de courrier électronique.
ms.openlocfilehash: 48beec9b581055c0f4928434eaa8378ae2812e2c
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995325"
---
# <a name="office-365-atp-safe-attachments"></a>Office 365 DAV fiable en pièce jointe

## <a name="overview-of-office-365-atp-safe-attachments"></a>Vue d’ensemble des pièces jointes de DAV Safe Office 365

Pièces jointes fiables de DAV (ainsi que les [Liens sécurisés DAV](atp-safe-links.md)) fait partie d' [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV). La fonctionnalité pièces jointes sûres DAV vérifie si les pièces jointes sont malveillants, puis intervient pour protéger votre organisation. La fonctionnalité pièces jointes sûres DAV protège votre organisation en fonction des [stratégies de pièces jointes sûres DAV](set-up-atp-safe-attachments-policies.md) qui sont définis par des administrateurs de sécurité Office 365 globale. 
  
Protection DAV peut également être étendue aux fichiers dans SharePoint Online, OneDrive pour les entreprises et Teams Microsoft. Pour plus d’informations, voir [Office 365 avancée protection contre les menaces pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md).
       
## <a name="how-it-works"></a>Fonctionnement

La fonctionnalité pièces jointes sûres DAV vérifie les pièces jointes des personnes de votre organisation. Lorsqu’une stratégie de pièces jointes sûres DAV est en place et une personne faisant que stratégie affiche leur messagerie électronique dans Office 365, les pièces jointes et les actions appropriées proviennent, en fonction de vos stratégies de pièces jointes sûres DAV. Selon la façon dont vos stratégies définies, personnes peuvent continuer à travailler sans même savoir qu’ils ont été envoyés à des fichiers malveillants.
  
Voici deux exemples de pièces jointes fiables DAV au travail.
  
- **Exemple 1 : pièce jointe** Supposons que Lee reçoit un message électronique comportant une pièce jointe. Si elle n’est pas évidente pour Lee que la pièce jointe est fiable ou réellement contienne un programme malveillant conçu pour dérober des informations d’identification de Lee. Dans l’organisation de Lee, un administrateur de sécurité défini une stratégie de pièces jointes sûres DAV quelques jours. Avec la fonctionnalité pièces jointes sûres DAV, la pièce jointe est ouvert et testée dans un environnement virtuel avant Lee les reçoit. Si la pièce jointe est déterminée malveillante, il sera automatiquement supprimé. Si la pièce jointe est fiable, il s’ouvre normalement lorsque Lee clique dessus. 
    
- **L’exemple 2 : fichier dans SharePoint Online** Supposons que Jean a reçu un fichier et il téléchargé dans une bibliothèque SharePoint Online. Jean partage le lien vers le fichier avec le reste de l’équipe, ne pas savoir que le fichier est réellement malveillant. Heureusement, [DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) détecte le fichier malveillant et bloque. Quelques jours plus tard, Chris accède à ouvrir le document. Bien que Chris peuvent voir que le fichier existe, Chris ne peut pas ouvrir ou partagez-le, ce qui empêche l’ordinateur de Chris et autres personnes à partir du fichier malveillant. 
    
Pièces jointes sûres DAV analyse prend place dans la même zone où résident vos données d’Office 365. Pour plus d’informations sur la zone géographique de centre de données, voir [où se trouvent vos données situées ?](https://products.office.com/where-is-your-data-located?geo=All) 

Stratégies de pièces jointes sûres DAV peuvent être appliquées à des personnes spécifiques ou des groupes dans votre organisation, ou à tout votre domaine. En outre, les stratégies de pièces jointes sûres DAV peuvent être configurées pour utiliser des pièces jointes d’espace réservé alors que les pièces jointes réelles sont analysés. Pour plus d’informations, voir **[configurer les stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)**. 
  
## <a name="how-to-get-atp-safe-attachments"></a>Comment obtenir des pièces jointes fiables DAV

Tout d’abord, assurez-vous que votre abonnement comprend la [Protection contre les menaces avancées](office-365-atp.md). DAV est inclus dans les abonnements, tels que [Microsoft 365 pour entreprises](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation A5, etc.. Si votre organisation a un abonnement à Office 365 qui n’inclut pas d’Office 365 DAV, vous pouvez acheter potentiellement DAV comme module complémentaire. Pour plus d’informations, voir [plans Office 365 avancée protection contre les menaces et les prix](https://products.office.com/exchange/advance-threat-protection) et [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

Ensuite, assurez-vous que vos stratégies de pièces jointes sûres DAV sont définis. (Voir [définir des stratégies Office 365 DAV approuvés en pièce jointe](set-up-atp-safe-attachments-policies.md)) Fonctionnalités de pièces jointes sûres DAV sont actifs quand :
  
- Stratégies de pièces jointes sûres DAV sont définies. (Voir [définir des stratégies de pièces jointes sûres DAV dans Office 365](set-up-atp-safe-attachments-policies.md)).
    
- Les utilisateurs ont connecté à Office 365 à l’aide de leur compte professionnel ou de l’école. (Voir [se connecter à Office ou Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426)).

Pour définir (ou modifier) les stratégies de vente, vous devez posséder un des rôles décrits dans le tableau suivant :

|Rôle  |Où/procédure affecté  |
|---------|---------|
|Administrateur Global d’Office 365 |La personne qui s’inscrit à acheter Office 365 est un administrateur global par défaut. (Voir [les rôles d’administration sur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) pour en savoir plus).         |
|Administrateur de sécurité |Centre d’administration Active Directory Azure ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Gestion de l’organisation en ligne Exchange |Centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>Comment savoir si la protection des pièces jointes sûres DAV est en place

Une fois que vous avez [défini (ou révisé) vos stratégies de pièces jointes sûres DAV](set-up-atp-safe-attachments-policies.md), un excellent moyen de voir comment fonctionne le service est en [affichage des rapports de protection contre les menaces avancées](view-reports-for-atp.md).
  
Le tableau suivant décrit quelques exemples de scénarios. Dans tous les cas, nous supposons que l’organisation a un abonnement à Office 365 qui inclut la protection contre les menaces avancées.
  
|**Exemple de scénario**|**Protection des pièces jointes sûres DAV applicable dans ce cas ?**|
|:-----|:-----|
|Organisation de Pat a Office 365 entreprise E5, mais n’a encore défini des stratégies pour les pièces jointes fiables DAV.  <br/> |non. Bien que la fonctionnalité est disponible, au moins une stratégie de pièces jointes sûres DAV doit être définie dans l’ordre pour la protection des pièces jointes sûres DAV mettre en place.  <br/> |
|Lee est un employé dans le service des ventes de Contoso. Organisation de Lee possède une stratégie de pièces jointes sûres DAV en place qui s’applique aux employés finance uniquement.  <br/> |non. Dans ce cas, employés finance aurait protection pièces jointes sûres DAV, mais les autres employés, y compris le service commercial, serait pas jusqu'à ce que les stratégies qui incluent ces groupes sont définies.  <br/> |
|Hier, un administrateur Office 365 à l’organisation de Jean définie une stratégie de pièces jointes sûres DAV qui s’applique à tous les employés. Journée, Jean a reçu un message électronique qui contient une pièce jointe.  <br/> |Oui. Dans cet exemple, Jean possède une licence pour la protection contre les menaces avancées, et une stratégie de pièces jointes sûres DAV incluant Jean a été définie. Il est généralement d’environ 30 minutes pour une nouvelle stratégie prennent effet sur les centres de données ; dans la mesure où un jour écoulé dans ce cas, la stratégie doit être en vigueur.  <br/> |
|Organisation de Chris a Office 365 entreprise E5 avec les stratégies de pièces jointes sûres DAV en place pour tout le monde dans l’organisation. Chris reçoit un message électronique comportant une pièce jointe et transfère le message à d’autres personnes qui se trouvent en dehors de l’organisation.  <br/> |Protection des pièces jointes sûres DAV est en place pour les messages qui reçoit Chris. Si les organisations de destinataires ont également des stratégies de pièces jointes sûres DAV en place, Chris transfère le message serait soumis à ces stratégies lorsque le message transféré arrive.  <br/> |
|Organisation de Marie a des stratégies de pièces jointes sûres DAV en place et [DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md) a été activée. Marie suppose que tous les fichiers dans SharePoint Online a été analysé et qu’il sont fiable pour ouvrir ou télécharger.<br/> |Protection des pièces jointes sûres DAV est en place en fonction des stratégies définies ; Toutefois, cela ne signifie pas que chaque fichier dans SharePoint Online, OneDrive, ou de l’entreprise Microsoft Teams est analysé. (Pour plus d’informations, voir [DAV pour SharePoint, OneDrive et les équipes Microsoft](atp-for-spo-odb-and-teams.md)).<br/> |
   
## <a name="submitting-files-for-malware-analysis"></a>Envoi de fichiers pour l’analyse de programmes malveillants

- Si vous recevez un fichier que vous voulez poser Microsoft pour analyser, visitez le site [Envoyer un fichier pour l’analyse de programmes malveillants](https://aka.ms/wdsi/submit).

- Si vous recevez un message électronique (avec ou sans pièce jointe) que vous souhaitez envoyer à Microsoft pour analyse, utilisez le [complément de Message de rapport](enable-the-report-message-add-in.md).
  
