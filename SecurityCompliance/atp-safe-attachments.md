---
title: Pièces jointes sécurisées ATP Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 04/04/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6e13311e-92ae-495e-a619-56d770199170
ms.collection:
- M365-security-compliance
description: La fonctionnalité pièces jointes fiables permet de vérifier le temps de cliquer sur les pièces jointes des messages électroniques. Utilisez des pièces jointes fiables pour protéger votre organisation des fichiers malveillants envoyés ou reçus par courrier électronique.
ms.openlocfilehash: 933a533a6deb52a41d1412e319c6fb6840046390
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32250964"
---
# <a name="office-365-atp-safe-attachments"></a>Pièces jointes sécurisées ATP Office 365

## <a name="overview-of-office-365-atp-safe-attachments"></a>Vue d'ensemble des pièces jointes approuvées pour Office 365 ATP

Les pièces jointes sécurisées ATP (ainsi que les [liens fiables ATP](atp-safe-links.md)) font partie d' [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP). La fonctionnalité de pièces jointes approuvées ATP vérifie si les pièces jointes sont malveillantes et prend des mesures pour protéger votre organisation. La fonctionnalité de pièces jointes approuvées ATP protège votre organisation en fonction des [stratégies de pièces jointEs approuvéEs ATP](set-up-atp-safe-attachments-policies.md) définies par vos administrateurs Office 365 global ou de sécurité. 
  
La protection contre l'ATP peut également être étendue aux fichiers dans SharePoint Online, OneDrive entreprise et Microsoft Teams. Pour en savoir plus, consultez la rubrique [Office 365 Advanced Threat Protection for SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md).

## <a name="how-it-works"></a>Mode de fonctionnement

La fonctionnalité pièces jointes approuvées ATP vérifie les pièces jointes de courrier électronique pour les personnes de votre organisation. Lorsqu'une stratégie de pièces jointes approuvées ATP est en place et qu'une personne concernée par cette stratégie affiche son courrier électronique dans Office 365, ses pièces jointes sont vérifiées et les actions appropriées sont prises, en fonction des stratégies de pièces jointes approuvées ATP. En fonction de la définition de vos stratégies, les utilisateurs peuvent continuer à travailler sans jamais savoir qu'ils ont reçu des fichiers malveillants.
  
Voici deux exemples de pièces jointes approuvées ATP au travail.
  
- **Exemple 1: pièce jointe de message électronique** Supposons que Lee reçoit un message électronique comportant une pièce jointe. Il n'est pas évident de savoir si cette pièce jointe est fiable ou si elle contient en réalité des programmes malveillants conçus pour voler les informations d'identification utilisateur de Lee. Dans l'organisation de Lee, un administrateur de sécurité a défini une stratégie de pièces jointes approuvées ATP il y a quelques jours. Avec la fonctionnalité pièces jointes approuvées ATP, la pièce jointe est ouverte et testée dans un environnement virtuel avant que Lee la reçoive. Si la pièce jointe est considérée comme malveillante, elle sera automatiquement supprimée. Si la pièce jointe est sécurisée, elle s'ouvre comme prévu lorsque Lee clique dessus.

- **Exemple 2: fichier dans SharePoint Online** Supposons que Jean a reçu un fichier et l'a téléchargé dans une bibliothèque dans SharePoint Online. Jean partage le lien vers le fichier avec le reste de l'équipe, sans savoir que le fichier est réellement malveillant. Heureusement, la protection avancée contre les menaces [pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md) détecte le fichier malveillant et le bloque. Quelques jours plus tard, Chris ouvre le document. Bien que Chris puisse voir le fichier, Chris ne peut pas l'ouvrir ou le partager, ce qui empêche l'ordinateur de Chris et d'autres personnes du fichier malveillant.

Les stratégies de pièces jointes approuvées ATP peuvent être appliquées à des personnes ou des groupes spécifiques de votre organisation ou à votre domaine entier. En outre, les stratégies de pièces jointes approuvées ATP peuvent être configurées pour utiliser les pièces jointes des espaces réservés pendant l'analyse des pièces jointes réelles. Pour en savoir plus, consultez la rubrique **[configurer des stratégies de pièces jointEs approuvéES ATP dans Office 365](set-up-atp-safe-attachments-policies.md)**.

> [!NOTE]
> L'analyse des pièces jointes approuvées ATP a lieu dans la région où se trouvent vos données Office 365. Pour plus d'informations sur la géographie du centre de données, voir [où se trouvent vos données?](https://products.office.com/where-is-your-data-located?geo=All) 

  
## <a name="how-to-get-atp-safe-attachments"></a>Comment obtenir des pièces jointes sûres ATP

Tout d'abord, assurez-vous que votre abonnement inclut la [protection avancée contre les menaces](office-365-atp.md). La protection avancée contre les menaces est incluse dans les abonnements, tels que [microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation a5, etc. Si votre organisation dispose d'un abonnement Office 365 qui n'inclut pas Office 365 ATP, vous pouvez acheter l'ATP en tant que module complémentaire. Pour plus d'informations, consultez la rubrique [offres et tarifs de protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection) , ainsi que la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

Ensuite, assurez-vous que vos stratégies de pièces jointes approuvées ATP sont définies. (Voir [configurer les stratégies de pièces jointEs approuvées pour Office 365 ATP](set-up-atp-safe-attachments-policies.md)) Les fonctionnalités de pièces jointes approuvées ATP sont actives dans les cas suivants:
  
- Les stratégies de pièces jointes approuvées ATP sont configurées. (Voir [configurer des stratégies de pièces jointEs approuvéES ATP dans Office 365](set-up-atp-safe-attachments-policies.md).)

- Les utilisateurs se sont connectés à Office 365 à l'aide de leur compte professionnel ou scolaire. (Voir [connexion à Office ou office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)

Pour définir (ou modifier) des stratégies ATP, vous devez disposer d'un rôle approprié. Certains exemples sont décrits dans le tableau suivant:

|Role  |WHERE/How Assigned  |
|---------|---------|
|Administrateur général Office 365 |La personne qui s'inscrit pour acheter Office 365 est un administrateur global par défaut. (Pour en savoir plus, consultez la rubrique [à propos des rôles d'administrateur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Administrateur de sécurité |Centre d'administration Azure Active Directory[https://aad.portal.azure.com](https://aad.portal.azure.com)()|
|Gestion de l'organisation Exchange Online |Centre d'administration Exchange[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>ou <br>  Applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

## <a name="how-to-know-if-atp-safe-attachments-protection-is-in-place"></a>Comment savoir si la protection des pièces jointes fiables ATP est en place?

Une fois que vous avez [défini (ou révisé) vos stratégies de pièces jointEs approuvées](set-up-atp-safe-attachments-policies.md)pour la protection avancée contre les menaces, vous pouvez voir comment le service fonctionne en [affichant des rapports pour une protection avancée contre les menaces](view-reports-for-atp.md).
  
Le tableau suivant décrit certains exemples de scénarios. Dans tous ces cas, nous partons du principe que l'organisation dispose d'un abonnement Office 365 qui inclut la protection avancée contre les menaces.
  
|**Exemple de scénario**|**Est-ce que la protection des pièces jointes fiables ATP s'applique dans ce cas?**|
|:-----|:-----|
|L'organisation de Pat a Office 365 entreprise E5, mais personne n'a défini de stratégie pour les pièces jointes approuvées à l'ATP pour le moment.  <br/> |Non. Bien que la fonctionnalité soit disponible, au moins une stratégie de pièces jointes fiables ATP doit être définie pour que la protection des pièces jointes ATP soit mise en place.  <br/> |
|Lee est un employé du service des ventes de contoso. L'organisation de Lee a une stratégie de pièces jointes approuvées ATP en place qui s'applique uniquement aux employés financiers.  <br/> |Non. Dans ce cas, les employés du service financier doivent disposer de la protection contre les pièces jointes approuvées ATP, mais les autres employés, y compris le département des ventes, ne devaient pas attendre que les stratégies incluant ces groupes soient définies.  <br/> |
|Hier, un administrateur Office 365 de la société Jean a configuré une stratégie de pièces jointes approuvées ATP qui s'applique à tous les employés. Plus tôt aujourd'hui, Jean a reçu un message électronique incluant une pièce jointe.  <br/> |Oui. Dans cet exemple, Jean a une licence pour la protection avancée contre les menaces et une stratégie de pièces jointes approuvées ATP qui inclut Jean a été défini. Il faut environ 30 minutes pour qu'une nouvelle stratégie prenne effet sur l'ensemble des centres de communication; étant donné qu'un jour a passé dans ce cas, la stratégie doit être en vigueur.  <br/> |
|L'organisation de Chris dispose d'Office 365 entreprise E5 avec des stratégies de pièces jointes approuvées pour tous les membres de l'organisation. Chris reçoit un courrier électronique qui contient une pièce jointe et le transfère à d'autres personnes qui se trouvent à l'extérieur de l'organisation.  <br/> |La protection des pièces jointes fiables ATP est mise en place pour les messages que Chris reçoit. Si les organisations de destinataires ont également des stratégies de pièces jointes approuvées ATP en place, le message que Chris Forward est soumis à ces stratégies lors de l'arrivée du message transféré.  <br/> |
|L'organisation de Marie a mis en place des stratégies de pièces jointes approuvées ATP, et la protection avancée contre les menaces [pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md) a été activée. Marie part du principe que chaque fichier de SharePoint Online a été analysé et qu'il est sûr de l'ouvrir ou de le télécharger.  <br/> |La protection des pièces jointes fiables ATP est mise en place en fonction des stratégies définies; Toutefois, cela ne signifie pas que tous les fichiers dans SharePoint Online, OneDrive entreprise ou Microsoft teams sont analysés. (Pour en savoir plus, consultez la rubrique [ATP pour SharePoint, OneDrive et Microsoft teams](atp-for-spo-odb-and-teams.md).)  <br/> |

## <a name="submitting-files-for-malware-analysis"></a>Envoi de fichiers pour l'analyse contre les programmes malveillants

- Si vous recevez un fichier que vous souhaitez demander à Microsoft d'analyser, consultez [la section soumettre un fichier pour l'analyse contre les programmes malveillants](https://aka.ms/wdsi/submit).

- Si vous recevez un message électronique (avec ou sans pièce jointe) que vous souhaitez envoyer à Microsoft pour analyse, utilisez le [complément Report message](enable-the-report-message-add-in.md).
