---
title: Définir des stratégies Office 365 DAV fiables liens
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: bdd5372d-775e-4442-9c1b-609627b94b5d
ms.collection: M365-security-compliance
description: Définir des stratégies de liens fiables pour protéger votre organisation contre les liens malveillants dans les fichiers Word, Excel, PowerPoint et Visio, ainsi que dans les messages électroniques.
ms.openlocfilehash: 834b83efe505a399fd3744e97533b92f2fc156f4
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995255"
---
# <a name="set-up-office-365-atp-safe-links-policies"></a>Définir des stratégies Office 365 DAV fiables liens

> [!IMPORTANT]
> Cet article est destiné aux entreprises. Si vous êtes un utilisateur vous recherchez des informations sur les liens sécurisés dans Outlook, voir [sécurité Outlook.com avancés](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

[Liens approuvés DAV](atp-safe-links.md), une fonctionnalité d' [Office 365 avancée protection contre les menaces](office-365-atp.md) (DAV), peuvent aider à protéger votre organisation à partir des liens malveillants utilisés dans les attaques par hameçonnage et d’autres attaques. Si vous avez nécessaires [les autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md), vous pouvez définir des stratégies de liens fiables DAV pour s’assurer que lorsque les utilisateurs cliquent sur les adresses web (URL), votre organisation est protégée. Vos stratégies de liens fiables DAV peuvent être configurées pour analyser les URL dans le message électronique et les URL dans les documents Office.
  
[Nouvelles fonctionnalités sont continuellement ajoutées au DAV](office-365-atp.md#new-features-are-continually-being-added-to-atp). Ajout de nouvelles fonctionnalités, vous devrez peut-être ajuster vos stratégies DAV fiables liens existants.

## <a name="what-to-do"></a>Procédure 
  
1. [Passez en revue les composants requis](#review-the-prerequisites).
    
2. [Réviser et modifier la stratégie de liens fiables DAV par défaut qui s’applique à tout le monde](#define-an-atp-safe-links-policy-that-applies-to-everyone). Par exemple, vous pouvez [configurer votre liste des URL bloqué personnalisé pour les liens sécurisés DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md).
    
3. [Ajouter ou modifier des stratégies pour les destinataires de courriers électroniques spécifiques](#add-a-policy-for-specific-email-recipients), en y compris [la configuration de votre liste des URL « Pas de rewrite » personnalisé pour les liens sécurisés DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
4. [Découvrez les options de stratégie de liens fiables DAV](#learn-about-atp-safe-links-policy-options) (dans cet article), notamment les paramètres pour les modifications récentes apportées.
    
## <a name="step-1-review-the-prerequisites"></a>Étape 1 : Vérifier les conditions préalables

- Assurez-vous que votre organisation dispose [d’Office 365 avancée protection contre les menaces](office-365-atp.md).
    
- Assurez-vous que vous disposez des autorisations nécessaires. Pour définir (ou modifier) les stratégies de vente, vous devez posséder un des rôles décrits dans le tableau suivant : <br>

    |Rôle  |Où/procédure affecté  |
    |---------|---------|
    |Administrateur Global d’Office 365 |La personne qui s’inscrit à acheter Office 365 est un administrateur global par défaut. (Voir [les rôles d’administration sur Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) pour en savoir plus).         |
    |Administrateur de sécurité |Centre d’administration Active Directory Azure ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
    |Gestion de l’organisation en ligne Exchange |Centre d’administration Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>ou <br>  Applets de commande PowerShell (voir [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

    Pour en savoir plus sur les rôles et autorisations, voir [des autorisations de sécurité Office 365 &amp; centre de conformité](permissions-in-the-security-and-compliance-center.md).

- Assurez-vous que les clients Office sont configurés pour utiliser l' [Authentification moderne](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) (il s’agit de protection DAV fiables liens dans les documents Office).
    
- [Découvrez les options de stratégie de liens fiables DAV](#learn-about-atp-safe-links-policy-options) (dans cet article). 

- Autoriser jusqu'à 30 minutes pour votre stratégie de nouveau ou mis à jour pour se propager sur tous les centres de données Office 365.
    
## <a name="step-2-define-or-review-the-atp-safe-links-policy-that-applies-to-everyone"></a>Étape 2 : Définir (ou passez en revue) la stratégie de liens fiables DAV qui s’applique à tout le monde

Lorsque vous avez [Contre les menaces avancées Office 365](office-365-atp.md), vous aurez une stratégie par défaut des liens fiables DAV qui s’applique à tout le monde dans votre organisation. Assurez-vous de consulter et si nécessaire, modifiez votre stratégie par défaut.
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **stratégie \> ** **Liens fiables**.
    
3. Dans la section **stratégies qui s’appliquent à toute l’organisation** , sélectionnez **par défaut**, puis choisissez **Modifier** (le bouton Modifier ressemble à un crayon).<br/>![Cliquez sur Modifier pour modifier votre stratégie par défaut pour la protection des liens fiables](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
4. Dans la section **bloquer les URL suivantes** , spécifiez une ou plusieurs URL que vous souhaitez empêcher les utilisateurs de votre organisation de se connecter. (Voir [configurer une liste d’URL bloquée personnalisée à l’aide de liens fiables DAV](set-up-a-custom-blocked-urls-list-wtih-atp.md)).
    
5. Dans la section **paramètres qui s’appliquent au contenu, à l’exception du courrier électronique** , activez (ou désactivez) les options que vous souhaitez utiliser. (Nous vous conseillons de sélectionner toutes les options.) 
    
6. Sélectionnez **Save (Enregistrer)**.
    
## <a name="step-3-add-or-edit-atp-safe-links-policies-that-apply-to-specific-email-recipients"></a>Étape 3 : Ajouter (ou modifier) des stratégies de liens fiables DAV qui s’appliquent aux destinataires de courriers électroniques spécifiques

Une fois que vous avez passé en revue (ou modifier) la stratégie de liens fiables DAV par défaut qui s’applique à tout le monde, l’étape suivante consiste à définir des stratégies supplémentaires qui s’appliquent à des destinataires spécifiques. Par exemple, vous pouvez spécifier des exceptions à votre stratégie par défaut en définissant une stratégie supplémentaire. 
  
1. Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous avec votre compte professionnel ou de l’école. 
    
2. Dans la navigation de gauche, sous **Gestion des menaces**, choisissez **une stratégie**.
    
3. Choisissez **les liens sécurisés**.
    
4. Dans la section **stratégies qui s’appliquent à des destinataires spécifiques** , choisissez **Nouveau** (nouveau bouton ressemble à un signe plus ( **+**)).<br/>![Cliquez sur Nouveau pour ajouter une stratégie de liens sécurisés pour les destinataires de messages électroniques spécifique](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
5. Indiquez un nom, une description et des paramètres pour votre stratégie.<br/>**Exemple :** Pour configurer une stratégie appelée « sans direct par clic » qui n’autorise pas les personnes dans un certain groupe dans votre organisation pour cliquer sur un site Web spécifique sans protection liens fiables DAV, vous pouvez spécifier les éléments suivants de le paramètres recommandés : 
    
  - Dans la zone **nom** , ne tapez aucun direct aux clics publicitaires.
    
  - Dans la zone **Description** , tapez une description comme empêche les personnes à certains groupes provenant du clic par le biais d’un site Web sans la vérification des liens fiables DAV.
    
  - Dans la section **Sélectionnez l’action** , cliquez **sur**.
    
  - Sélectionnez **Les pièces jointes fiables à utiliser pour analyser du contenu téléchargeable**.
    
  - Si cette option est disponible, sélectionnez **Appliquer sans échec des liens vers des messages envoyés au sein de l’organisation**.
    
  - Sélectionnez **ne pas autoriser l’utilisateur de clic vers l’URL d’origine**.
    
  - (Cette étape est facultative) Dans la section **ne pas réécrire les URL suivantes** , spécifiez une ou plusieurs URL sont considérés comme sûrs pour votre organisation. (Voir [configurer une liste d’URL personnalisée du « Pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md))
    
  - Dans la section **Appliquée à** , sélectionnez **le destinataire est un membre du**, puis les groupes que vous souhaitez inclure dans votre stratégie de. Cliquez sur **Ajouter**, puis cliquez sur **OK**.
    
6. Sélectionnez **Save (Enregistrer)**.
    
## <a name="step-4-learn-about-atp-safe-links-policy-options"></a>Étape 4 : En savoir plus sur les options de stratégie de liens fiables DAV

Comme vous configurez ou modifiez vos stratégies de liens fiables DAV, verront plusieurs options disponibles. Au cas où vous vous demandez ces options, le tableau suivant décrit chaque option et son effet. N’oubliez pas qu’il existe deux types principaux de stratégies de liens fiables DAV pour définir ou modifier :
- une [stratégie par défaut](#default-policy-options) qui s’applique à tout le monde 
- autres [stratégies définies pour des destinataires spécifiques](#policies-that-apply-to-specific-email-recipients) 

### <a name="default-policy-options"></a>Options de stratégie par défaut

Options de stratégie par défaut s’appliquent à tout le monde dans votre organisation.

|Cette option  |Effectue cette action  |
|---------|---------|
| **Bloquer les URL suivantes** <br/>    | Permet à votre organisation d’avoir une liste personnalisée d’URL qui sont bloqués automatiquement. Lorsque les utilisateurs cliquent sur une URL dans cette liste, il est dirigé vers une [page d’avertissement](atp-safe-links-warning-pages.md) qui explique pourquoi l’URL est bloquée.<br/> Pour en savoir plus, voir [configurer une liste d’URL bloquée personnalisée à l’aide de liens fiables DAV      |
| **Office 365 ProPlus, Office pour iOS et Android** <br/>    | Lorsque cette option est sélectionnée, les liens sécurisés DAV protection est appliquée aux URL dans les documents qui sont ouvrir dans Office 365 ProPlus (Word, Excel et PowerPoint sous Windows ou Mac OS), des documents Office sur iOS ou Android appareils, 2016 Visio sur Windows et Office Online (Word En ligne, PowerPoint Online, Excel Online et OneNote en ligne), fournies à que l’utilisateur s’est connecté à Office 365. <br/><br/>Si vous voyez uniquement **2016 Office sur Windows**, puis les mises à jour de la fonctionnalité ne parviennent pas à encore votre environnement Office 365 (et ils sont bientôt disponible). En attendant, protection liens fiables DAV s’applique à Word 2016, 2016 Excel, PowerPoint 2016 ou 2016 Visio en cours d’exécution sur Windows.            |
| **Ne suivez pas lorsque les utilisateurs cliquent sur les liens sécurisés DAV** <br/>  | Lorsque cette option est sélectionnée, cliquez sur données pour l’URL dans les documents Word, Excel, PowerPoint et Visio n’est pas stocké.  <br/> |
|**Ne laissez pas vos utilisateurs cliquez sur par le biais de DAV fiables des liens vers des URL d’origine** <br/> |Lorsque cette option est sélectionnée, les utilisateurs ne peut pas continuer au-delà d’une [page d’avertissement](atp-safe-links-warning-pages.md) à une URL qui est définie comme étant malveillants.  <br/> |

### <a name="policies-that-apply-to-specific-email-recipients"></a>Stratégies qui s’appliquent aux destinataires de courriers électroniques spécifique

|Cette option  |Effectue cette action  |
|---------|---------|
|**Off** <br/> |N’analyse pas les URL dans les messages électroniques.  <br/> Vous permet de définir une règle d’exception, par exemple une règle qui n’analyse pas les URL dans les messages électroniques pour un groupe spécifique de destinataires.  <br/> |
|**Sur** <br/> |Réécrit URL aux utilisateurs d’itinéraire par le biais de protection des liens fiables DAV lorsque les utilisateurs cliquent sur les URL dans les messages électroniques.  <br/> Vérifie une URL lorsque vous cliquez sur par rapport à une liste d’URL bloquées ou malveillants.  <br/> |
|**Pièces jointes fiables permet d’analyser le contenu téléchargeable** <br/> |Lorsque cette option est sélectionnée, les URL qui pointent vers le contenu téléchargeable sont analysés.  <br/> |
|**Appliquez les liens sécurisés pour les messages envoyés au sein de l’organisation** <br/> | Lorsque cette option est disponible et activée, protection liens fiables DAV est appliquée pour les messages envoyés entre les personnes dans votre organisation, fournie les comptes de messagerie sont hébergées dans Office 365 les courriers électroniques.  <br/> |
|**Ne suivent pas les clics de l’utilisateur** <br/> |Lorsque cette option est sélectionnée, cliquez sur données pour l’URL dans le courrier provenant d’expéditeurs externes n’est pas stocké. Cliquez sur URL de suivi pour les liens dans les messages électroniques envoyés au sein de l’organisation n’est pas actuellement pris en charge.  <br/> |
|**Ne pas autoriser les utilisateurs à l’URL d’origine** <br/> |Lorsque cette option est sélectionnée, les utilisateurs ne peut pas continuer au-delà d’une [page d’avertissement](atp-safe-links-warning-pages.md) à une URL qui est définie comme étant malveillants.  <br/> |
|**Pas réécrire les URL suivantes** <br/> |Laisse les URL en tant qu’ils reçoivent. Tenir à jour une liste personnalisée d’URL fiables qui n’ont pas besoin d’analyse pour un groupe spécifique de destinataires de courriers électroniques dans votre organisation.  Pour plus d’informations, y compris les modifications récentes apportées pour prendre en charge pour le caractère générique astérisque, consultez [configurer une liste d’URL personnalisée du « Pas de rewrite » à l’aide de liens fiables DAV](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) (\*).<br/> |
   
## <a name="next-steps"></a>Étapes suivantes

Une fois vos stratégies de liens fiables DAV sont mis en place, vous pouvez voir comment fonctionne pour votre entreprise DAV en affichant des rapports. Voir les ressources suivantes pour en savoir plus :

- [Afficher les rapports de Protection de menace avancées d’Office 365](view-reports-for-atp.md)

- [Utiliser l’Explorateur de solutions de sécurité &amp; centre de conformité](use-explorer-in-security-and-compliance.md)

Maîtriser les nouvelles fonctionnalités en DAV. visitez le site de la [Feuille de route Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365) et découvrez les [nouvelles fonctionnalités qui sont ajoutées à DAV](office-365-atp.md#new-features-are-continually-being-added-to-atp).